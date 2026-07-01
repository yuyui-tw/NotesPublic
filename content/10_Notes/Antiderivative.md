---
aliases:
  - 反導函數
tags:
  - Math
up:
related:
  - "[[Derivative]]"
annotation:
---
# 概要
**反導函數 (Antiderivative)** 是一個微分後會得到原始函數的函數，它是微分的逆運算。
一個函數的所有反導函數的集合也被稱為**不定積分 (indefinite integral)**。

# 核心概念
## 定義 (Definition)
如果對於區間 $I$ 上的所有 $x$，都有 $F'(x) = f(x)$，那麼函數 $F$ 就是函數 $f$ 在該區間上的一個**反導函數 (antiderivative)**。

## 積分常數 (The Constant of Integration, C)
如果 $F(x)$ 是 $f(x)$ 的一個反導函數，那麼對於任意常數 $C$，$G(x) = F(x) + C$ 也是 $f(x)$ 的一個反導函數。
這是因為常數的微分是零：
$$ 
G'(x) = \frac{d}{dx}(F(x) + C) = F'(x) + 0 = f(x)
$$
這個常數 $C$ 被稱為**積分常數 (constant of integration)**。它代表反導函數圖形在垂直方向上的位移。因此，一個函數會有一整組（或一族）的反導函數。

$f$ 的**一般反導函數 (general antiderivative)** 寫作：
$$ 
\int f(x) \,dx = F(x) + C
$$ 

## 初始值問題 (Initial Value Problem)
初始值問題提供一個「初始條件 (initial condition)」（即函數圖形上的一個點 $(x_0, y_0)$），讓我們能夠找到常數 $C$ 的具體值。這能從一族函數中篩選出唯一一個特定的反導函數。

**範例 (Example):**
找出 $f(x) = 2x$ 的反導函數，且該函數通過點 $(1, 4)$。
1.  **找出一般反導函數：**
    $2x$ 的反導函數是 $F(x) = x^2 + C$。
2.  **使用初始條件找出 C：**
    已知 $F(1) = 4$。
    $1^2 + C = 4$
    $1 + C = 4$
    $C = 3$
3.  **寫出特定的反導函數：**
    特定的反導函數為 $F(x) = x^2 + 3$。

# 結構/要素
## 基本反導函數公式 (Basic Antiderivative Formulas)

| 函數 $f(x)$                | 一般反導函數 $F(x)+C$           |
| :----------------------- | :------------------------ |
| $k$ (常數)                 | $kx + C$                  |
| $x^n$ ($n \neq -1$)      | $\frac{x^{n+1}}{n+1} + C$ |
| $x^{-1}$ 或 $\frac{1}{x}$ | $\ln x+C$                 |
| $e^x$                    | $e^x + C$                 |
| $a^x$                    | $\frac{a^x}{\ln a} + C$   |
| $\cos x$                 | $\sin x + C$              |
| $\sin x$                 | $-\cos x + C$             |
| $\sec^2 x$               | $\tan x + C$              |
| $\sec x \tan x$          | $\sec x + C$              |
| $\frac{1}{\sqrt{1-x^2}}$ | $\arcsin x + C$           |
| $\frac{1}{1+x^2}$        | $\arctan x + C$           |

## 性質 (Properties)
- **和/差法則 (Sum/Difference Rule):** $\int [f(x) \pm g(x)] \,dx = \int f(x) \,dx \pm \int g(x) \,dx$
- **常數倍數法則 (Constant Multiple Rule):** $\int k \cdot f(x) \,dx = k \int f(x) \,dx$

# 原理/推導
反導函數的概念是[[Fundamental Theorem of Calculus]](微積分基本定理)的基礎，該定理連結了微分與積分的概念。
找出反導函數是不定積分的核心操作。
