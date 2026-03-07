---
aliases:
  - 積分
  - Integral
tags:
  - Math
up: "[[微積分]]"
related:
  - "[[Derivative]]"
  - "[[Fundamental Theorem of Calculus]]"
  - "[[definite integral]]"
  - "[[Integration by Parts]]"
  - "[[Trigonometric Integral]]"
  - "[[Trigonometric Substitution]]"
---

# 概要 (Summary)
**積分 (Integral)** 是微積分的兩大核心概念之一，與[[Derivative|微分]]互為逆運算。它廣泛用於計算累積量，例如曲線下的面積、物體的體積、變力所作的功、物體的質心等。積分主要分為**定積分 (Definite Integral)** 與**不定積分 (Indefinite Integral)**。

# 核心概念 (Core Concepts)
## 不定積分 (Indefinite Integral)
不定積分是尋找一個函數 $f(x)$ 的**所有反導函數 (Antiderivatives)** 的過程。反導函數是指一個其導函數為 $f(x)$ 的函數 $F(x)$。其結果是一個包含任意常數 $C$ (積分常數) 的函數族。
$$ \int f(x) \,dx = F(x) + C \quad \text{其中 } F'(x) = f(x) $$
- **關鍵區別:** 結果是一個**函數族**。

## 定積分 (Definite Integral)
定積分的本質是**黎曼和的極限 (Limit of Riemann Sums)**。在幾何上，它代表函數 $f(x)$ 的圖形在區間 $[a, b]$ 上與 x 軸所圍成的**有符號面積 (Signed Area)**。
$$ \int_{a}^{b} f(x) \,dx = \lim_{n \to \infty} \sum_{i=1}^{n} f(c_i) \Delta x_i $$
- **啞變數 (Dummy Variable):** 在定積分中，積分變數 (如 $x$) 只在積分範圍內有意義，可以替換成任何其他變數而不改變其值。例如, $\int_{a}^{b} f(x) \,dx = \int_{a}^{b} f(t) \,dt$。
- **關鍵區別:** 結果是一個**數值**。

> [!NOTE] 常用求和公式 (Summation Formulas)
> - $\sum_{k=1}^{n} k^2 = \frac{n(n+1)(2n+1)}{6}$
> - $\sum_{k=1}^{n} k^3 = \left( \frac{n(n+1)}{2} \right)^2$

# 結構/要素 (Properties and Theorems)
## 定積分的基本性質 (Properties of Definite Integrals)
1.  **區間互換:** $\int_{a}^{b} f(x) \,dx = - \int_{b}^{a} f(x) \,dx$
2.  **零寬度區間:** $\int_{a}^{a} f(x) \,dx = 0$
3.  **區間可加性:** $\int_{a}^{c} f(x) \,dx + \int_{c}^{b} f(x) \,dx = \int_{a}^{b} f(x) \,dx$
4.  **線性性質:** $\int_{a}^{b} [k \cdot f(x) \pm l \cdot g(x)] \,dx = k\int_{a}^{b} f(x) \,dx \pm l\int_{a}^{b} g(x) \,dx$
5.  **比較性質:** 若在 $[a, b]$ 上 $f(x) \ge g(x)$，則 $\int_{a}^{b} f(x) \,dx \ge \int_{a}^{b} g(x) \,dx$。

## 積分均值定理 (Mean Value Theorem for Integrals)
若 $f$ 在 $[a, b]$ 上連續，則至少存在一點 $c \in [a, b]$ 使得函數值 $f(c)$ 等於該區間的函數平均值 $f_{\text{avg}}$。
$$ f(c) = f_{\text{avg}} = \frac{1}{b-a} \int_{a}^{b} f(x) \,dx $$
幾何意義上，這表示一定存在一個矩形，其高為 $f(c)$，寬為 $(b-a)$，其面積恰好等於曲線下的面積。

# 原理與應用 (Principles and Applications)
## 微積分基本定理 (Fundamental Theorem of Calculus)
積分的核心是 [[Fundamental Theorem of Calculus|微積分基本定理]]，它深刻地揭示了微分與積分之間的逆運算關係，並提供了計算定積分的系統性方法。

## 積分的應用 (Applications of Integration)
積分是將無限小的量累加起來的工具，因此應用廣泛。
- **變力作功 (Work Done by a Variable Force):** 如果一個物體在力 $F(x)$ 的作用下沿直線從 $a$ 移動到 $b$，所作的功為 $W = \int_a^b F(x) dx$。
- **質心 (Center of Mass):** 物體的質心座標可以通過積分計算得出，反映了質量的分佈情況。

# 範例 (Examples)
**不定積分**
計算 $\int x^2 \,dx$。
根據反導函數的規則，我們尋找一個函數，其導函數為 $x^2$。
$$ \int x^2 \,dx = \frac{1}{3}x^3 + C $$
**定積分**
計算 $\int_0^2 x^2 \,dx$。
使用微積分基本定理，先找到不定積分，然後代入上下限。
$$ \int_0^2 x^2 \,dx = \left[ \frac{1}{3}x^3 \right]_0^2 = \frac{1}{3}(2)^3 - \frac{1}{3}(0)^3 = \frac{8}{3} $$
這個值代表了函數 $y=x^2$ 的圖形在 $x=0$ 到 $x=2$ 之間與 x 軸圍成的面積。
