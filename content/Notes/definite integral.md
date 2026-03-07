---
aliases:
  - 定積分
  - Definite Integral
tags:
  - Math
up: "[[Integral]]"
related: "[[Fundamental Theorem of Calculus]]"
---

# 概要 (Summary)
定積分是積分學的兩大分支之一，其核心思想是「分割、近似、求和、取極限」，這個過程稱為黎曼和。它將一個連續的量（如面積、體積）分割成無數個微小部分，再將這些部分加總起來得到總量。因此，定積分在幾何與物理學中有著廣泛的應用。

# 核心概念 (Core Concepts)
## 曲線間面積 (Area Between Curves)
若在區間 $[a, b]$ 上，$f(x) \ge g(x)$，則兩曲線 $y=f(x)$ 和 $y=g(x)$ 之間所夾的面積為：
$$ A = \int_a^b [f(x) - g(x)] \,dx $$
- **對 y 軸積分:** 如果將 x 視為 y 的函數 $x=f(y)$，也可以對 y 軸進行積分來計算面積。

## 體積：切片法 (Volume: The Slicing Method)
如果一個立體在 $x$ 軸上從 $a$ 延伸到 $b$，且在 $x$ 點的截面積為 $A(x)$，則此立體的體積為：
$$ V = \int_a^b A(x) \,dx $$
這個通用方法是計算旋轉體體積的基礎。

# 結構/要素 (Methods for Calculating Volume)
## 圓盤法 (Disk Method)
當一個由 $y=R(x)$、x 軸、和直線 $x=a, x=b$ 圍成的區域繞 x 軸旋轉時，其旋轉體體積可視為一系列無限薄的圓盤體積之和。
- 截面積 $A(x) = \pi [R(x)]^2$
- 體積公式: $V = \int_a^b \pi [R(x)]^2 \,dx$

## 墊圈法 (Washer Method)
當一個由 $y=R(x)$ (外半徑) 和 $y=r(x)$ (內半徑) 在區間 $[a, b]$ 上圍成的區域繞 x 軸旋轉時，其旋轉體是一個中空的立體。
- 截面積 $A(x) = \pi [R(x)]^2 - \pi [r(x)]^2$
- 體積公式: $V = \int_a^b \pi \left( [R(x)]^2 - [r(x)]^2 \right) \,dx$

## 殼層法/圓柱殼法 (Shell Method)
當一個區域繞著一條軸旋轉時，可以將其視為由許多薄圓柱殼所組成。此方法在旋轉軸與積分變數的軸平行時特別有用。若繞 y 軸旋轉：
- 圓柱殼半徑: $r(x) = x$
- 圓柱殼高度: $h(x) = f(x)$
- 體積公式: $V = \int_a^b 2\pi \cdot r(x) \cdot h(x) \,dx = \int_a^b 2\pi x f(x) \,dx$

# 原理與其他應用 (Principles and Other Applications)
## 弧長 (Arc Length)
函數 $y=f(x)$ 在區間 $[a, b]$ 上的曲線長度（弧長），可以通過將曲線微小段視為直角三角形的斜邊，並利用畢氏定理推導得出。
- 弧長公式: $L = \int_a^b \sqrt{1 + [f'(x)]^2} \,dx$

## 旋轉體表面積 (Area of a Surface of Revolution)
將函數 $y=f(x)$ 在區間 $[a, b]$ 上的曲線繞 x 軸旋轉，所形成的旋轉體表面積為：
- 表面積公式: $S = \int_a^b 2\pi f(x) \sqrt{1 + [f'(x)]^2} \,dx$
  - 其中 $2\pi f(x)$ 是一微小段的旋轉半徑所形成的圓周長，後面的根號項則是微小的弧長。

## 奇偶函數的積分性質
- **偶函數 (Even Function, $f(-x)=f(x)$):** 若 $f$ 為偶函數，則 $\int_{-a}^a f(x) \,dx = 2 \int_0^a f(x) \,dx$。
- **奇函數 (Odd Function, $f(-x)=-f(x)$):** 若 $f$ 為奇函數，則 $\int_{-a}^a f(x) \,dx = 0$。
- 如果計算面積可視為兩倍(對稱)

# 範例 (Examples)
**計算 $y=x$ 和 $y=x^2$ 在第一象限所圍成的面積。**
1.  **找出交點:**
    $x = x^2 \implies x^2 - x = 0 \implies x(x-1) = 0$
    交點為 $x=0$ 和 $x=1$。
2.  **確定上下關係:**
    在區間 $[0, 1]$ 上，$x \ge x^2$。所以 $f(x)=x$，$g(x)=x^2$。
3.  **設立並計算積分:**
    $$ A = \int_0^1 (x - x^2) \,dx = \left[ \frac{1}{2}x^2 - \frac{1}{3}x^3 \right]_0^1 $$
    $$ = \left( \frac{1}{2}(1)^2 - \frac{1}{3}(1)^3 \right) - (0) = \frac{1}{2} - \frac{1}{3} = \frac{1}{6} $$
面積為 $1/6$。