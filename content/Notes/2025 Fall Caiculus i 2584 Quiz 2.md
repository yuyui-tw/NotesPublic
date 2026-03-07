START
9Qs
title: 2025 Fall Caiculus i 2584 Quiz 2
content:
#Math #QuizReview 

# Q1: 
Evaluate the derivative of 
$$
y=\ln (\sec x+\tan x)
$$
## A1: 
**方法 (Method):**
此導數求解需使用**連鎖律 (Chain Rule)**，因為它是一個複合函數 (對數函數內部嵌套三角函數表達式)。

**公式 (Formula):**
- **連鎖律**: 若 $y = f(g(x))$，則 $\frac{dy}{dx} = f'(g(x)) \cdot g'(x)$。
- **相關導數**:
    - $\frac{d}{dx}(\ln u) = \frac{1}{u}$
    - $\frac{d}{dx}(\sec x) = \sec x \tan x$
    - $\frac{d}{dx}(\tan x) = \sec^2 x$

**過程 (Process):**
1.  **識別內外層函數**:
    - 外層函數: $f(u) = \ln u$
    - 內層函數: $u = g(x) = \sec x + \tan x$
2.  **對外層函數微分**:
    - $f'(u) = \frac{1}{u} = \frac{1}{\sec x + \tan x}$
3.  **對內層函數微分**:
    - $g'(x) = \sec x \tan x + \sec^2 x$
4.  **應用連鎖律**:
    - $\frac{dy}{dx} = f'(g(x)) \cdot g'(x) = \left( \frac{1}{\sec x + \tan x} \right) \cdot (\sec x \tan x + \sec^2 x)$
5.  **化簡表達式**:
    - 從第二項中提取公因式 $\sec x$：
      $$ \frac{dy}{dx} = \frac{\sec x (\tan x + \sec x)}{\sec x + \tan x} $$
    - 消去分子分母的公同項 $(\sec x + \tan x)$:
      $$ \frac{dy}{dx} = \sec x $$

# Q2:
Find the limit of
$$
\lim_{ x \to 0 } \frac{{1-\cos x}}{x^{2}}
$$
## A2:
**方法 (Method):**
此極限是 $\frac{0}{0}$ 的不定型 (Indeterminate Form)，因此可以使用**羅必達法則 (L'Hôpital's Rule)**。

**公式 (Formula):**
- **羅必達法則**: 若 $\lim_{x \to c} \frac{f(x)}{g(x)}$ 的形式為 $\frac{0}{0}$ 或 $\frac{\infty}{\infty}$，則
  $$ \lim_{x \to c} \frac{f(x)}{g(x)} = \lim_{x \to c} \frac{f'(x)}{g'(x)} $$

**過程 (Process):**
1.  **驗證不定型**:
    - 當 $x \to 0$ 時，分子 $1 - \cos x \to 1 - 1 = 0$。
    - 當 $x \to 0$ 時，分母 $x^2 \to 0$。
    - 此極限確實為 $\frac{0}{0}$ 形式。
2.  **應用羅必達法則 (第一次)**:
    - 微分分子: $\frac{d}{dx}(1 - \cos x) = \sin x$。
    - 微分分母: $\frac{d}{dx}(x^2) = 2x$。
    - 新的極限為: $\lim_{x \to 0} \frac{\sin x}{2x}$。
3.  **再次驗證不定型**:
    - 當 $x \to 0$ 時，$\sin x \to 0$。
    - 當 $x \to 0$ 時，$2x \to 0$。
    - 極限仍為 $\frac{0}{0}$ 形式。
4.  **應用羅必達法則 (第二次)**:
    - 微分分子: $\frac{d}{dx}(\sin x) = \cos x$。
    - 微分分母: $\frac{d}{dx}(2x) = 2$。
    - 新的極限為: $\lim_{x \to 0} \frac{\cos x}{2}$。
5.  **計算最終極限**:
    - 代入 $x=0$:
      $$ \frac{\cos 0}{2} = \frac{1}{2} $$

# Q3: 
Find the limit of
$$
\lim_{ x \to \infty } \frac{e^{x^{2}}}{xe^{x}}
$$
## A3:
**方法 (Method):**
此極限是 $\frac{\infty}{\infty}$ 的不定型，可以比較指數的增長速率或使用**羅必達法則 (L'Hôpital's Rule)**。

**公式 (Formula):**
- **羅必達法則**: 同上題。
- **指數律**: $\frac{e^a}{e^b} = e^{a-b}$

**過程 (Process):**
1.  **驗證不定型**:
    - 當 $x \to \infty$ 時，分子 $e^{x^2} \to \infty$。
    - 當 $x \to \infty$ 時，分母 $xe^x \to \infty$。
    - 此極限確實為 $\frac{\infty}{\infty}$ 形式。
2.  **應用羅必達法則**:
    - 微分分子: $\frac{d}{dx}(e^{x^2}) = e^{x^2} \cdot 2x$。
    - 微分分母: $\frac{d}{dx}(xe^x) = 1 \cdot e^x + x \cdot e^x = e^x(1+x)$。
    - 新的極限為: 
      $$ \lim_{x \to \infty} \frac{2x \cdot e^{x^2}}{e^x(1+x)} $$
3.  **化簡並分別求極限**:
    - 我們可以將表達式拆分為兩部分：
      $$ \lim_{x \to \infty} \left( \frac{2x}{1+x} \right) \cdot \left( \frac{e^{x^2}}{e^x} \right) = \lim_{x \to \infty} \left( \frac{2x}{1+x} \right) \cdot \left( e^{x^2 - x} \right) $$
    - 計算第一部分的極限：
      $$ \lim_{x \to \infty} \frac{2x}{1+x} = \lim_{x \to \infty} \frac{2}{1/x + 1} = \frac{2}{0+1} = 2 $$
    - 計算第二部分的極限：
      $$ \lim_{x \to \infty} e^{x^2 - x} $$
      因為當 $x \to \infty$ 時，$x^2$ 的增長速度遠快於 $x$，所以 $x^2-x \to \infty$。因此，$e^{x^2-x} \to \infty$。
4.  **合併結果**:
    - 最終極限為兩部分極限的乘積：
      $$ 2 \cdot \infty = \infty $$

# Q4:
Find the limit of
$$
\lim_{ x \to 0 } \frac{{e^{x-\sin x}-1}}{x^{2}\sin x}
$$
- Use $\lim_{ t \to 0 } \frac{e^{t}-1}{t}=1$
## A4:
**方法 (Method):**
此題可利用題目提示的已知極限 $\lim_{t \to 0} \frac{e^t-1}{t}=1$，並搭配代換法與羅必達法則。

**公式 (Formula):**
- **已知極限**: $\lim_{t \to 0} \frac{e^t-1}{t}=1$
- **已知極限**: $\lim_{x \to 0} \frac{\sin x}{x}=1$
- **已知極限**: $\lim_{x \to 0} \frac{1-\cos x}{x^2}=\frac{1}{2}$ (可由Q2結果得知)

**過程 (Process):**
1.  **使用提示進行代換**:
    - 目標是湊出 $\frac{e^t-1}{t}$ 的形式。我們令 $t = x - \sin x$。當 $x \to 0$ 時，$t \to 0$。
    - 將原式變形：
      $$ \lim_{x \to 0} \left( \frac{e^{x-\sin x}-1}{x-\sin x} \right) \cdot \left( \frac{x-\sin x}{x^2 \sin x} \right) $$
    - 根據提示，第一部分的極限為 1。現在問題簡化為計算第二部分的極限。
2.  **計算第二部分極限**:
    - 我們需要計算:
      $$ \lim_{x \to 0} \frac{x-\sin x}{x^2 \sin x} $$
    - 此為 $\frac{0}{0}$ 不定型。直接使用羅必達法則會變得複雜。我們可以嘗試另一種化簡方式：將分母中的 $\sin x$ 替換為 $x$。這一步驟的依據是 $\lim_{x \to 0} \frac{\sin x}{x} = 1$，在極限運算中 $\sin x \approx x$。
      $$ \lim_{x \to 0} \frac{x-\sin x}{x^2 \cdot x} = \lim_{x \to 0} \frac{x-\sin x}{x^3} $$
3.  **應用羅必達法則**:
    - 上式仍為 $\frac{0}{0}$ 不定型。
    - **第一次羅必達**:
      $$ \lim_{x \to 0} \frac{1-\cos x}{3x^2} $$
    - 我們可以提出常數 $\frac{1}{3}$，得到:
      $$ \frac{1}{3} \lim_{x \to 0} \frac{1-\cos x}{x^2} $$
    - **使用已知極限**:
      根據 Q2 的結果，我們知道 $\lim_{x \to 0} \frac{1-\cos x}{x^2} = \frac{1}{2}$。
      $$ \frac{1}{3} \cdot \frac{1}{2} = \frac{1}{6} $$
4.  **合併結果**:
    - 原極限 = (第一部分的極限) $\cdot$ (第二部分的極限) = $1 \cdot \frac{1}{6} = \frac{1}{6}$。 

# Q5: 
Evaluate 
$$
\int_{-2}^{2}\sqrt{ 4-x^{2} }dx
$$
## A5:
**方法 (Method):**
此定積分可以透過幾何意義 (Geometric Interpretation) 來求解，會比使用三角代換等積分技巧更為快捷。

**公式 (Formula):**
- **圓的方程式**: $(x-h)^2 + (y-k)^2 = r^2$，其中 $(h,k)$ 是圓心，$r$ 是半徑。
- **圓的面積**: $A = \pi r^2$

**過程 (Process):**
1.  **識別函數圖形**:
    - 令 $y = \sqrt{4-x^2}$。
    - 將方程式兩邊平方，得到 $y^2 = 4-x^2$。
    - 移項整理得: $x^2 + y^2 = 4$。
2.  **分析幾何形狀**:
    - 這個方程式 $x^2+y^2=2^2$ 代表一個以原點 $(0,0)$ 為圓心，半徑 $r=2$ 的圓。
    - 由於原函數是 $y = \sqrt{4-x^2}$，y值恆為非負數，這表示它只代表了圓的**上半部分**，即一個**半圓**。
3.  **關聯定積分與面積**:
    - 定積分 $\int_{-2}^{2} \sqrt{4-x^2} dx$ 的計算範圍是從 $x=-2$ 到 $x=2$。
    - 這個範圍正好是該半圓的直徑所在的區間。
    - 因此，此定積分的值就等於這個半圓的面積。
4.  **計算面積**:
    - 首先計算完整圓的面積:
      $A_{circle} = \pi r^2 = \pi (2)^2 = 4\pi$
    - 半圓的面積是完整圓面積的一半:
      $A_{semicircle} = \frac{1}{2} A_{circle} = \frac{1}{2} (4\pi) = 2\pi$ 

# Q6:
Graph the function 
$$
y= \frac{8}{x^{2}+4}
$$
using the steps in the graphing procedure.
## A6:
遵照你筆記中的「函數圖形繪製策略」，我們分三步進行分析：

**1. 分析 $f(x) = \frac{8}{x^2+4}$:**
*   **定義域 (Domain)**: 分母 $x^2+4$ 恆為正，永遠不為零。因此，定義域是所有實數 $(-\infty, \infty)$。
*   **截距 (Intercepts)**:
    *   $y$ 截距 (令 $x=0$): $y = \frac{8}{0+4} = 2$。截距點為 $(0, 2)$。
    *   $x$ 截距 (令 $y=0$): $\frac{8}{x^2+4} = 0$，此方程式無解。故無 $x$ 截距。
*   **對稱性 (Symmetry)**: $f(-x) = \frac{8}{(-x)^2+4} = \frac{8}{x^2+4} = f(x)$。此為**偶函數**，圖形對稱於 $y$ 軸。
*   **漸近線 (Asymptotes)**:
    *   垂直漸近線: 無 (因為定義域為所有實數)。
    *   水平漸近線: $\lim_{x \to \pm\infty} \frac{8}{x^2+4} = 0$。水平漸近線為 $y=0$ (x軸)。

**2. 分析 $f'(x)$:**
*   **求導**: $f'(x) = \frac{0 \cdot (x^2+4) - 8 \cdot (2x)}{(x^2+4)^2} = \frac{-16x}{(x^2+4)^2}$。
*   **臨界點 (Critical Points)**: 令 $f'(x)=0$，得 $-16x=0 \implies x=0$。
*   **單調區間 (Monotonicity)**:
    *   當 $x > 0$，$f'(x) < 0$，函數在 $(0, \infty)$ 上**遞減**。
    *   當 $x < 0$，$f'(x) > 0$，函數在 $(-\infty, 0)$ 上**遞增**。
*   **局部極值 (Local Extrema)**: 在 $x=0$ 處，導數由正轉負，故 $f(0)=2$ 為**局部最大值**。

**3. 分析 $f''(x)$:**
*   **求導**:
    $$ f''(x) = \frac{-16(x^2+4)^2 - (-16x) \cdot 2(x^2+4)(2x)}{(x^2+4)^4} = \frac{-16(x^2+4) + 64x^2}{(x^2+4)^3} = \frac{48x^2 - 64}{(x^2+4)^3} = \frac{16(3x^2-4)}{(x^2+4)^3} $$
*   **潛在反曲點 (Potential Inflection Points)**: 令 $f''(x)=0$，得 $3x^2-4=0 \implies x = \pm\frac{2}{\sqrt{3}}$。
*   **凹性區間 (Concavity)**:
    *   當 $x > \frac{2}{\sqrt{3}}$ 或 $x < -\frac{2}{\sqrt{3}}$ (例如 $x=\pm 3$)，$3x^2-4 > 0$，$f''(x)>0$。圖形在 $(-\infty, -\frac{2}{\sqrt{3}})$ 和 $(\frac{2}{\sqrt{3}}, \infty)$ 區間**凹向上 (Concave Up)**。
    *   當 $-\frac{2}{\sqrt{3}} < x < \frac{2}{\sqrt{3}}$ (例如 $x=0$)，$3x^2-4 < 0$，$f''(x)<0$。圖形在 $(-\frac{2}{\sqrt{3}}, \frac{2}{\sqrt{3}})$ 區間**凹向下 (Concave Down)**。
*   **反曲點 (Inflection Points)**: 凹性在 $x = \pm\frac{2}{\sqrt{3}}$ 兩側發生改變。
    $y$ 坐標為 $f(\pm\frac{2}{\sqrt{3}}) = \frac{8}{(\frac{4}{3})+4} = \frac{8}{\frac{16}{3}} = \frac{3}{2}$。
    反曲點為 $(-\frac{2}{\sqrt{3}}, \frac{3}{2})$ 和 $(\frac{2}{\sqrt{3}}, \frac{3}{2})$。

**繪圖總結**:
1.  從 $y$ 軸左側接近，函數從 $y=0$ 開始，**遞增**且**凹向上**。
2.  到達反曲點 $(-\frac{2}{\sqrt{3}}, \frac{3}{2})$，函數繼續**遞增**，但轉為**凹向下**。
3.  到達 $y$ 軸上的局部最大值 $(0, 2)$。
4.  越過 $y$ 軸，函數開始**遞減**，維持**凹向下**。
5.  到達反曲點 $(\frac{2}{\sqrt{3}}, \frac{3}{2})$，函數繼續**遞減**，但轉為**凹向上**。
6.  最終向右趨近於無窮時，函數值逐漸趨近水平漸近線 $y=0$。
整個圖形呈鐘形，對稱於 $y$ 軸。


TARGET DECK: 

source url: 

END