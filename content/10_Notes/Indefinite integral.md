---
aliases:
  - 不定積分
tags:
  - Math
up:
  - "[[Antiderivative]]"
related:
annotation:
---
# 概要
**不定積分 (Indefinite Integral)** 代表一個函數 $f(x)$ 的**所有**反導函數的集合。
它本身不是一個單一的函數，而是一個函數族。
不定積分的結果包含一個積分常數 $C$。

# 核心概念
## 符號與定義 (Notation and Definition)
不定積分的標準寫法如下：
$$
\int f(x) \,dx = F(x) + C
$$
- $\int$ 是**積分符號 (integral sign)**。
- $f(x)$ 是**被積函數 (integrand)**。
- $dx$ 指出**積分變數 (variable of integration)** 是 $x$。
- $F(x)$ 是 $f(x)$ 的一個反導函數，滿足 $F'(x) = f(x)$。
- $C$ 是**積分常數 (constant of integration)**。

## 積分常數C的意義
`+C` 代表了所有可能的常數。
因為常數的微分為零，所以任何一個反導函數加上任意一個常數後，其微分仍然是原始的被積函數。
因此，不定積分的結果是一個包含所有這些可能性的函數族，而不是單一一個函數。
圖形上來看，`+C` 代表了函數 $F(x)$ 在y軸上的無限種可能的垂直平移。

## Antiderivative 與 Indefinite Integral 的差別
- **反導函數 (Antiderivative):** 是一個**單一的函數**。例如，$x^2$ 是 $2x$ 的一個反導函數。$x^2+3$ 也是 $2x$ 的一個反導函數。
- **不定積分 (Indefinite Integral):** 是一個**函數的集合（或稱函數族）**，包含了**所有**的反導函數。它用 $F(x)+C$ 來表示。例如，$\int 2x \,dx = x^2 + C$，這代表了所有形如 $x^2 + Constant$ 的函數。

簡單來說，不定積分是反導函數的一般表示法。

# 結構/要素
## 基本性質 (Properties)
- **常數倍數法則 (Constant Multiple Rule):**
  $$ \int k \cdot f(x) \,dx = k \int f(x) \,dx $$
- **和/差法則 (Sum/Difference Rule):**
  $$ \int [f(x) \pm g(x)] \,dx = \int f(x) \,dx \pm \int g(x) \,dx $$

## 將微分公式轉為積分公式
每一個微分公式都可以反過來寫成一個積分公式。

| 微分公式 (Differentiation)                               | 對應的積分公式 (Integration)                                       |
| :--------------------------------------------------- | :---------------------------------------------------------- |
| $\frac{d}{dx}(k) = 0$                                | $\int 0 \,dx = C$                                           |
| $\frac{d}{dx}(kx) = k$                               | $\int k \,dx = kx + C$                                      |
| $\frac{d}{dx}\left(\frac{x^{n+1}}{n+1}\right) = x^n$ | $\int x^n \,dx = \frac{x^{n+1}}{n+1} + C \quad (n \neq -1)$ |
| $\frac{d}{dx}(\ln x) = \frac{1}{x}$                  | $\int \frac{1}{x} \,dx = \ln x + C$                         |
| $\frac{d}{dx}(e^x) = e^x$                            | $\int e^x \,dx = e^x + C$                                   |
| $\frac{d}{dx}\left(\frac{a^x}{\ln a}\right) = a^x$   | $\int a^x \,dx = \frac{a^x}{\ln a} + C$                     |
| $\frac{d}{dx}(\sin x) = \cos x$                      | $\int \cos x \,dx = \sin x + C$                             |
| $\frac{d}{dx}(-\cos x) = \sin x$                     | $\int \sin x \,dx = -\cos x + C$                            |
| $\frac{d}{dx}(\tan x) = \sec^2 x$                    | $\int \sec^2 x \,dx = \tan x + C$                           |
| $\frac{d}{dx}(\sec x) = \sec x \tan x$               | $\int \sec x \tan x \,dx = \sec x + C$                      |
| $\frac{d}{dx}(\arcsin x) = \frac{1}{\sqrt{1-x^2}}$   | $\int \frac{1}{\sqrt{1-x^2}} \,dx = \arcsin x + C$          |
| $\frac{d}{dx}(\arctan x) = \frac{1}{1+x^2}$          | $\int \frac{1}{1+x^2} \,dx = \arctan x + C$                 |

# 原理/推導
不定積分是[[Fundamental Theorem of Calculus|微積分基本定理]]的第一部分的核心，該定理建立了微分和定積分之間的聯繫。
計算不定積分的過程，本質上就是尋找反導函數的過程。