---
tags:
  - Math
up: "[[Exponential and Logarithm functions]]"
related:
aliases: ["自然對數", "Natural logarithm"]
---

# 概要 (Summary)
自然對數 (Natural Logarithm)，符號為 $\ln x$，是指以歐拉數 $e$ 為底的對數，即 $\log_e x$。它與指數函數 $e^x$ 互為反函數，在描述自然增長、衰變等現象時至關重要。

# 核心概念 (Core Concepts)
- **歐拉數 (Euler's Number), $e$:** 一個重要的無理數，其近似值為 2.718。它有兩種常見的極限定義：
  1. $e = \lim_{n \to \infty} \left(1 + \frac{1}{n}\right)^n=\lim_{ t \to 0 }(1+t)^{1/t}$
  2. $e = \sum_{n=0}^{\infty} \frac{1}{n!} = \frac{1}{0!} + \frac{1}{1!} + \frac{1}{2!} + \dots$
- **反函數關係 (Inverse Relationship):**
  $$ y = \ln x \iff x = e^y $$
  這意味著 $\ln(e^x) = x$ 且 $e^{\ln x} = x$ (對於 $x>0$)。
- **積分定義 (Definition by Integral):** 自然對數也可以定義為一個定積分，表示函數 $f(t)=1/t$ 從 1 到 $x$ 的曲線下面積：
  $$ \ln x := \int_1^x \frac{1}{t} dt $$
  從這個定義可以直接推導出 $(\ln x)' = 1/x$。

![[graph of natural logarithms.png]]

# 結構/要素 (Properties)
假設 $a, b > 0$ 且 $r$ 為有理數：
1.  **乘積律 (Product Rule):** $\ln(ab) = \ln a + \ln b$
2.  **商數律 (Quotient Rule):** $\ln(a/b) = \ln a - \ln b$
3.  **指數律 (Power Rule):** $\ln(a^r) = r \cdot \ln a$
4.  **特殊值 (Special Values):**
    - $\ln 1 = 0$
    - $\ln e = 1$
5.  **導數 (Derivatives):**
    - $(\ln x)' = \frac{1}{x}$
    - $(e^x)' = e^x$
6.  **連鎖律 (Chain Rule):**
    - $(\ln(f(x)))' = \frac{f'(x)}{f(x)}$
    - $(e^{f(x)})' = e^{f(x)} \cdot f'(x)$

# 原理/推導 (Principles and Derivations)
自然對數是解形如 $\frac{dy}{dt} = ky$ 的微分方程的關鍵。這種類型的方程描述了許多自然和物理過程，例如放射性衰變、人口增長等。

**推導：指數增長模型**
假設一個量 $N$ 的增長率與其當前的大小成正比，比例常數為 $\lambda$。
$$ \frac{dN}{dt} = \lambda N $$
若初始條件為 $N(0) = N_0$，可以通過分離變數法求解：
$$ \frac{dN}{N} = \lambda dt $$
對兩邊從初始狀態到時間 $t$ 進行積分：
$$ \int_{N_0}^{N(t)} \frac{dN}{N} = \int_0^t \lambda dt $$
$$ \left[\ln N\right]_{N_0}^{N(t)} = \left[\lambda t\right]_0^t $$
$$ \ln N(t) - \ln N_0 = \lambda t $$
$$ \ln\left(\frac{N(t)}{N_0}\right) = \lambda t $$
利用反函數關係，得到指數增長公式：
$$ N(t) = N_0 e^{\lambda t} $$

# 範例 (Examples)
**求解指數方程式**
解方程式 $e^{2x} = 5$。
對兩邊取自然對數：
$$ \ln(e^{2x}) = \ln 5 $$
$$ 2x = \ln 5 $$
$$ x = \frac{\ln 5}{2} $$
