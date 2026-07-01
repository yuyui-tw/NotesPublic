---
tags:
  - Math
up: "[[微積分]]"
related:
aliases:
  - 函數
  - Function
  - 初等函數
  - Elementary function
annotation: 函數 (Function) 的基本定義、集合對應關係、核心分類（單射、滿射、對射）、基本運算與變換，以及初等函數 (Elementary Function) 的定義與分類結構
---

# 1. 導論 (Introduction & Background)

**函數 (Function)** 是描述兩個集合之間對應關係的數學概念。若原函數將定義域 (Domain) 映射至對應域 (Codomain)，則對於每一個輸入值，皆有唯一確定的輸出值落在值域 (Range) 中。

**初等函數 (Elementary Function)** 是由 **基本初等函數 (Basic Elementary Function)** 經由有限次代數運算及函數合成所構成的單變數函數。基本初等函數包括：常數函數、冪函數、指數函數、對數函數、三角函數及反三角函數。

其基本映射關係表示為：
$$ f: D \to Y $$
$$ \forall x \in D\ \exists!\ y \in Y\  s.t. f(x)=y $$

# 2. 核心 (Core Framework)

- **集合對應分類 (Classification of Mappings):**
    - **單射 (Injection / One-to-one):** 不同的輸入對應不同的輸出。
    - **滿射 (Surjection / Onto):** 值域等於對應域，所有可能的輸出都被對應到。
    - **對射 (Bijection):** 同時為單射與滿射的對應關係。對射函數為反函數存在的充要條件，詳見 [[反函數]]。
- **初等函數分類 (Classification of Elementary Functions):**
    - **代數函數 (Algebraic Function):** 可由自變數與常數經過有限次代數運算（加、減、乘、除、乘方、開方）構成的函數。
    - **超越函數 (Transcendental Function):** 不屬於代數函數的初等函數，如三角函數與指數函數。
- **函數特性 (Function Properties):**
    - **單調性 (Monotonicity):** 函數隨自變數增加而遞增或遞減的特徵，參見 [[Monotonic functions & the first derivative test]]。

# 3. 邏輯 (Operational Logic)

- **函數運算 (Operations on Functions):**
    - 基本算術運算包括加、減、乘、除四則運算。
    - 函數合成 (Composition) 的表達式為：
      $$ (f \circ g)(x) = f(g(x)) $$
- **函數變換 (Transformations):**
    - 平移變換包括垂直平移（如 $y = f(x) + k$）與水平平移（如 $y = f(x-k)$）。
    - 縮放變換包括垂直拉伸（如 $y = c \cdot f(x)$）與水平壓縮（如 $y = f(cx)$）。

# 4. 應用與脈絡 (Application & Context)

- **反函數應用 (Inverse Applications):**
    - 僅有對射函數具備反函數，詳細定義參見 [[反函數]]。
- **初等函數實例 (Elementary Function Examples):**
    - 指數與對數的運算規則參見 [[Exponential and Logarithm functions]]。
    - 反三角函數的定義域與值域限制參見 [[Inverse Trigonometric function]]。
    - **[[雙曲線函數|雙曲函數]] (Hyperbolic Function)** 可由指數函數組合而成，例如雙曲餘弦 $\cosh(x)$ 與雙曲正弦 $\sinh(x)$：
      $$ \cosh(x) = \frac{e^x + e^{-x}}{2} $$
      $$ \sinh(x) = \frac{e^x - e^{-x}}{2} $$
- **初等函數與冪級數的關聯 (Relation with Power Series):**
    - **泰勒展開 (Taylor Expansion):** 在收斂區間內，許多可微初等函數（如指數、對數、三角函數）可展開為無限項的 [[冪級數]] 或 [[泰勒級數]]（參見 [[常見函數的泰勒級數]]）。
    - **冪級數求和 (Power Series Summation):** 反之，==一個冪級數在收斂域內可藉由變數代換、逐項微積分等運算，求和並還原為閉合形式的初等函數==。
    - **實例分析:** 冪級數 $\sum_{n=0}^{\infty} \frac{(x + 2)^{2n}}{(n + 3)!}$ 在 $x \neq -2$ 時，可藉由指數函數 $e^y$ 的展開式求和還原為初等函數：
      $$ f(x) = \frac{e^{(x+2)^2} - 1 - (x+2)^2 - \frac{1}{2}(x+2)^4}{(x+2)^6} $$
      詳細還原步驟請參考 [[111學年度台綜大E0011微積分A試題解析#7. 冪級數求和（還原初等函數）]] 。
- **微積分連結 (Calculus Connections):**
    - 函數是研究極限的基礎，相關極限法則參見 [[Limit of a function and Limit laws]]。