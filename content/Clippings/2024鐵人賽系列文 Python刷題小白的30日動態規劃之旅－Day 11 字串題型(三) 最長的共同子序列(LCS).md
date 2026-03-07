---
source: https://mikalibrary.com/posts/ironman2024/ironman2024_11/#%E9%A1%8C%E7%9B%AE
tags:
  - clippings
---
## 🟨最長的共同子序列

本題取自 [Leetcode 1143. Longest Common Subsequence](https://leetcode.com/problems/longest-common-subsequence/description/)

## 題目

Given two strings `text1` and `text2`, return *the length of their **longest common subsequence***. If there is no **common subsequence**, return `0`.

A **subsequence** of a string is a new string generated from the original string with some characters (can be none) deleted without changing the relative order of the remaining characters.

For example, `"ace"` is a subsequence of `"abcde"`.

A **common subsequence** of two strings is a subsequence that is common to both strings.

```vbnet
Example 1:

Input: text1 = "abcde", text2 = "ace" 
Output: 3  
Explanation: The longest common subsequence is "ace" and its length is 3.

Example 2:

Input: text1 = "abc", text2 = "abc"
Output: 3
Explanation: The longest common subsequence is "abc" and its length is 3.

Example 3:

Input: text1 = "abc", text2 = "def"
Output: 0
Explanation: There is no such common subsequence, so the result is 0.
 

Constraints:

1 <= text1.length, text2.length <= 1000
text1 and text2 consist of only lowercase English characters.
```

## 分析

和day9遇到過的 **子字串** 定義不太相同， **子序列** 可以由給定字串(或者陣列)當中 *取出任意的片段並重新串接，但順序要維持不變* 。例如 `'abcd'` 的子序列包含 `'abd'` ，但不包含 `'ca'` (因為字母順序和原字串不同)。

兩個字串擁有 **共同子序列** ，意即某個子序列 `sub` 同時屬於字串 `t1` 、 `t2` 的子序列。

---

那麼要如何找出題目所要求的「 *最長的* **共同子序列** 」長度呢？

暴力破解(brute force)顯然是不現實的，因為每一個字母都可以取或者不取，光是暴力枚舉(enumerate)出所有的子序列就需要 `O(2^n)` 的 **指數時間** ，顯然必須尋找不同的途徑。

我們以一個簡單的例子來思考：求字串 `'abc'` 與 `acb` 的最長共同子序列長度。

答案顯然為 `2` ， `ab` 或者 `ac` 都為其所代表的解。儘管這兩個字串一共含有 `a b c` 三個共同的字母，但答案為何不是 `3` 呢？

原因就在於，子序列的排列順序必須與原本的字串相同。無法同時使用 `a b c` 三個字母，卻同時滿足和兩個字串相同的排列順序。

![alt text](https://mikalibrary.com/posts/ironman2024/ironman2024_11/Leetcode%201143.%20Longest%20Common%20Subsequence.drawio.png)

![alt text](https://mikalibrary.com/posts/ironman2024/ironman2024_11/Leetcode%201143.%20Longest%20Common%20Subsequence.drawio%20(1).png)

### 分治法

由前述討論可知，尋找LCS的過程，需要 **匹配** 相同的字母，且保證在兩個字串當中的 **順序** 相同

本題用到一個貪心( *Greedy Stratagy* )的思維：

> 若兩個字串 `text1` 、 `text2` 的字首相同 `text1[0] == text2[0]` ，則這個字首必定包含在 `text1` 、 `text2` 的\*最長共同子序列(LCS)\*當中。

- 由於我們只比較了字首，因此對於這個局部(首字母)而言，在兩個字串中 **順序** 必定是相同的(都在兩個字串的最左邊)
- 由於獲得了 **匹配** ，若不將首字母計入LCS，所得的答案有可能不是 **最長** 的共同子序列。

繼續以前述的測資為例， `'abc'` 與 `'acb'` 的LCS必定包含 `'a'` ，且其位置必為字首。

> 若兩個字串 `text1` 、 `text2` 的字首不 `text1[0] != text2[0]` ，則這兩個字首的 **至少其一** 必定 **不** 包含在 `text1` 、 `text2` 的\*最長共同子序列(LCS)\*當中。

- 因為子序列的字母 **順序** 不可擅自調換，兩個相異首字母分別固定在各自子序列的字首，則必定不為 **共同** 子序列

分析至此，我們便找到了如何逐步匹配的策略。

### 設計狀態、找出轉移式與最小問題

**狀態** ：以 `LCS(i,j)` 來代表 `text1[i:]` 、 `text2[j:]` 之間的 *最長共同子序列* 的 **長度** 。

**狀態轉移式** ：

若 `text1[i] == text2[j]` (字首相同)：

`LCS(i,j) = 1 + LCS(i+1,j+1)`

若 `text1[i] != text2[j]` (字首不同)：

`LCS(i,j) = max( LCS(i+1,j), LCS(i,j+1) )`

**邊界條件** (最小子問題)： `i < len(text1)` ， `j < len(text2)`

**母問題** (題目所求)： `LCS(0,0)`

## 實作

### Top-Down DP

```kotlin
class Solution:
    def longestCommonSubsequence(self, text1: str, text2: str) -> int:
        
        def LCS(i,j):
            if i==len(text1) or j==len(text2):
                return 0
            if text1[i] == text2[j]:
                return 1 + LCS(i+1, j+1)
            return max(LCS(i+1, j), LCS(i,j+1))

        return LCS(0,0)
```

### Bottom-Up DP

為了處理index overflow的問題並且不增加額外的邏輯判斷程式碼，最上一列與最左一行( `i==o` 或者 `j==0` )都加入一個額外的 `0` 。

配合計算順序， `dp[i][j]` 改成代表 `text1[:i]` 和 `text2{:j}` 之間的LCS(改成比較字尾而非字首)。

```go
class Solution:
    def longestCommonSubsequence(self, text1: str, text2: str) -> int:
        dp = [[0]*(len(text2)+1)]
        for i in range(len(text1)):
            row = [0]
            for j in range(len(text2)):
                if text1[i] == text2[j]:
                    row.append(1+dp[i][j])
                else:
                    row.append(max(row[j], dp[i][j+1]))
            
            dp.append(row)
        return dp[-1][-1]
```

也可以使用 *Rolling* 或者 *Inplace* 的技巧來優化，降低一維空間複雜度。

下例為 *inplace DP* 的示範：

由於inplace DP會覆寫掉上一列的資料，但轉移式會使用到 `LCS(i-1, j-1)` 以及 `LCS(i-1,j)` ，需要額外保留左上角一格的資料 `prev` 以及上面一格的 `cur`

```go
class Solution:
    def longestCommonSubsequence(self, text1: str, text2: str) -> int:
        dp = [0]*(len(text2)+1)
        for i in range(len(text1)):
            prev = 0
            for j in range(len(text2)):
                cur = dp[j+1] 
                if text1[i] == text2[j]:
                    dp[j+1] = 1+prev
                else:
                    dp[j+1] = max(dp[j:j+2])
                prev = cur
        return dp[-1]
```

## 複雜度分析

### 時間複雜度

`時間複雜度 = 狀態轉移數 x 計算複雜度`

本題的 `狀態數 = O(n1 x n2)` ， `n1 = len(text1)` ， `n2 = len(text2)`

計算複雜度為 `O(1)`

因此 **總時間複雜度** = `O(n1 x n2)`

### 空間複雜度

`空間複雜度 ＝ 狀態數 ＝ O(n1 x n2))`

若採用 *Rolling* (或者 *Inplace* ) Bottom Up DP的技巧，則降低一個維度， `空間複雜度 ＝ O(n2)`

## 進一步優化：資料前處理

以上的實作，時間複雜度上並沒有什麼問題，但若想要更進一步優化，可以想想看以下這組測資：

> `text1` 與 `text2` 很長，且彼此之間完全沒有任何一個共同的字母。(簡單舉例如 `aaa...aaa` 和 `bbb...bbb` )

答案顯然為0，然而我們還是得花 `n1 x n2` 的時間遍歷比對 `text1` 與 `text2` 當中任意的字母組合。

有沒有方法 **事先排除** 掉這些不共同的字母，來優化整體的時間花費呢？

實作範例如下：

```kotlin
class Solution:
    def longestCommonSubsequence(self, text1: str, text2: str) -> int:
        common = set(text1) & set(text2)
        t1 = [c for c in text1 if c in common]
        t2 = [c for c in text2 if c in common]
        
        def LCS(i,j):
            if i==len(t1) or j==len(t2):
                return 0
            if t1[i] == t2[j]:
                return 1 + LCS(i+1, j+1)
            return max(LCS(i+1, j), LCS(i,j+1))

        return LCS(0,0)
```

動態規劃的部分和原本相同，只是在執行LCS演算法之前，先對原始字串做一點處理：

- 取出 `text1` 與 `text2` 共通的所有字母作為 `common` (使用了Python的 `Set` 資料容器以及交集語法)
- 將 `text1` 與 `text2` 內不屬於 `common` 的字母剔除。

所獲得的新字串，再執行LCS演算法。

如此一來的成效如何呢？

### 時間複雜度

- 建立 `Set` 需要花費 `O(n1+n2)`
- 交集運算(union operation `'&'` )在worst case會花費 `O(x+y)` ，其中 `xy` 分別為兩集合的大小
- LCS演算法需要花費 `O(m1 x m2)` ，其中 `m1` 、 `m2` 分別為經處理過後的字串長度。

由於時間瓶頸仍是在LCS的部分，當 `text1` 與 `text2` 當中 **不共通** 的字母越多，就能節省越多時間。

整體而言，雖然並沒有降低時間複雜度的數量級，但平均時間可獲得顯著的下降。

### 空間複雜度

- 建立 `Set` 需要額外花費 `O(n1+n2)` 空間
- 交集運算(union operation `'&'` )不花費額外的空間
- LCS演算法需要花費 `O(m1 x m2)` ，其中 `m1` 、 `m2` 分別為經處理過後的字串長度。
- 若使用 *Rolling Bottom Up DP* ，則LCS可以降低一個維度至 `O(m)` ， `m` 為 `min(m1,m2)`

整體而言，由於 `m1` 、 `m2` 相對 `n1` 、 `n2` 亦獲得了縮減，空間複雜度並沒有數量級上顯著的增加。

(當然，建立Hashmap的空間常數必然比儲存整數的matrix大上許多)

下圖為筆者用Top-Down、Bottom-Up兩種策略，分別優化與不優化，在Leetcode上面跑出來的結果。

![alt text](https://mikalibrary.com/posts/ironman2024/ironman2024_11/image.png)

可以觀察到由於本例的遞迴層數很深，Top-Down的空間常數都相當大，Bottom-Up則在節省空間的同時也維持更快的運算速度。若同時使用Rolling和資料前處理的技巧來節省時間與空間，其效果也相當的顯著。

---

## 結語

LCS的解題概念並不複雜，其中融入了一點 *Greedy* 的思維，讓我們不必浪費O(2^n)比較所有的子序列，是我當初刷到時很喜歡的一個題型。

除了LCS本身的算法邏輯，在本題也看到透過 *資料前處理* 來進一步優化計算時間的範例。這提醒了我們：有時候除了改變算法來影響複雜度的優化， **不去算不必算的東西，也是一種優化方式** 。這無論是刷題時，或者真正實作專案時都值得借鏡。
