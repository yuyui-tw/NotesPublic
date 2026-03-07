---
tags:
  - Math
up: "[[微積分]]"
related:
aliases:
  - 函數
  - Function
---

# 概要 (Summary)
函數 (Function) 是數學中的核心概念，它描述了兩個集合之間的對應關係。具體來說，對於定義域 (Domain) 中的每一個輸入值，函數都會賦予一個唯一存在的輸出值。這個概念是微積分學的基石。
$$ f: D \to Y $$
其中 $D$ 是定義域 (Domain)，$Y$ 是對應域 (Codomain)。
$$
\forall x \in D\ \exists!\ y \in Y\  s.t. f(x)=y
$$

# 核心概念 (Core Concepts)
- **定義域 (Domain):** 函數輸入值 $x$ 的所有可能值的集合，通常表示為 $D$。需注意變數的限制，如分母不為零、根號內非負等。
- **對應域 (Codomain):** 函數輸出值可能存在的所有值的集合，表示為 $Y$。
- **值域 (Range):** 函數實際輸出的所有值的集合，是 Codomain 的子集。表示為 $\{f(x) | x \in D\}$。
- **單射、滿射、對射 (Injective, Surjective, Bijective):**
    - **單射 (Injective / One-to-one):** 不同的輸入對應不同的輸出。
    - **滿射 (Surjective / Onto):** 值域等於對應域，所有可能的輸出都被對應到。
    - **對射 (Bijective):** 同時是單射也是滿射。只有對射函數才存在反函數。

# 結構/要素 (Properties and Operations)
## 函數特性
- **遞增/遞減 (Increasing/Decreasing):**
    - 若函數的斜率 (一階導數) 在一區間內為正，則函數在該區間為遞增 (Increasing)。
    - 若斜率為負，則為遞減 (Decreasing)。

## 函數運算 (Operations on Functions)
- **基本算術:** 兩個函數 $f$ 和 $g$ 可以進行加、減、乘、除運算。
  - $(f+g)(x) = f(x) + g(x)$
  - $(f-g)(x) = f(x) - g(x)$
  - $(f \cdot g)(x) = f(x)g(x)$
  - $(f/g)(x) = f(x)/g(x)$，需滿足 $g(x) \neq 0$。
- **函數合成 (Composition):** 將一個函數的輸出作為另一個函數的輸入。
  $$ (f \circ g)(x) = f(g(x)) $$

## 函數變換 (Transformations)
- **平移 (Shifting):**
    - **垂直平移 (Vertical):** $y = f(x) + k$ (上移 $k$ 單位)
    - **水平平移 (Horizontal):** $y = f(x-k)$ (右移 $k$ 單位)
- **縮放 (Scaling):**
    - **垂直縮放 (Vertical):** $y = c \cdot f(x)$ (對 $y$ 軸作 $c$ 倍縮放)
    - **水平縮放 (Horizontal):** $y = f(cx)$ (對 $x$ 軸作 $1/c$ 倍縮放)

# 原理/推導 (Principles and Derivations)
## 反函數 (Inverse Function)
如果一個函數是對射函數，那麼它的反函數 $f^{-1}$ 存在，且滿足 $f(f^{-1}(x)) = x$ 和 $f^{-1}(f(x)) = x$。反函數的圖形與原函數的圖形對稱於直線 $y=x$。詳見 [[反函數|Inverse function]]。

## 雙曲函數 (Hyperbolic Functions)
雙曲函數是基於指數函數 $e^x$ 定義的，在物理和工程中有廣泛應用。
- **雙曲餘弦 (Hyperbolic Cosine):** $\cosh(x) = \frac{e^x + e^{-x}}{2}$
- **雙曲正弦 (Hyperbolic Sine):** $\sinh(x) = \frac{e^x - e^{-x}}{2}$

# 範例 (Examples)
考慮函數 $f(x) = x^2$：
- **定義域:** $D = \mathbb{R}$ (所有實數)
- **值域:** Range = $[0, \infty)$
- **函數變換:** 
    - $g(x) = x^2 + 2$ 是將 $f(x)$ 向上平移 2 單位。
    - $h(x) = (x-3)^2$ 是將 $f(x)$ 向右平移 3 單位。
    - $k(x) = 2x^2$ 是將 $f(x)$ 在 $y$ 方向上拉伸為原來的 2 倍。