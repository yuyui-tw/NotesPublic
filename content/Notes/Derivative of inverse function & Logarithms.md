---
aliases:
- 反函數與對數的微分
tags:
  - Math
up:
  - "[[Implicit Differentiation|隱函數微分]]"
related:
  - "[[Exponential and Logarithm functions]]"
  - "[[反函數|Inverse function]]"
annotation:
---
# 概要
1.  **反函數的微分**：介紹一個通用法則，讓我們可以透過原函數的導數來求其反函數的導數。
2.  **對數函數的微分**：將反函數的微分法則應用於自然指數函數 $e^x$，從而推導出自然對數函數 $\ln x$ 的微分公式。並進一步介紹**對數微分法 (Logarithmic Differentiation)**，這是一個處理複雜函數（特別是函數的函數次方形式）的強大技巧。

# 理論
## inverse function (反函數)
如果一個函數 $f$ 是**一對一 (one-to-one)** 的，那麼它就存在一個反函數 $f^{-1}$。

從圖形上看，$f^{-1}$ 的圖形是 $f$ 的圖形對直線 $y=x$ 的鏡像。這個幾何關係是理解其微分的關鍵：
- 假設點 $(a, b)$ 在 $f$ 的圖形上，即 $b = f(a)$
- 那麼點 $(b, a)$ 就在 $f^{-1}$ 的圖形上，即 $a = f^{-1}(b)$
- $f$ 在點 $(a, b)$ 的切線斜率是 $f'(a)$
- $f^{-1}$ 在點 $(b, a)$ 的切線斜率是 $(f^{-1})'(b)$

由於圖形是沿 $y=x$ 對稱的，兩條對應的切線斜率互為**倒數**。這提供了直觀的理解：$x$ 和 $y$ 的角色互換了，因此變化率 $\frac{dy}{dx}$ 也變成了 $\frac{dx}{dy}$。

## logarithm (對數)
自然對數函數 $y = \ln x$ 被定義為自然指數函數 $y = e^x$ 的反函數。因此，我們可以直接套用反函數的微分法則來找出它的導數。

**對數微分法 (Logarithmic Differentiation)** 是一種利用對數的特性來簡化微分過程的技巧，它並不是一個新的微分規則，而是一種巧妙的應用。其威力在於能將棘手的**乘除運算**和**次方運算**轉換為較簡單的**加減運算**和**乘法運算**。
- $\ln(ab) = \ln a + \ln b$
- $\ln(a/b) = \ln a - \ln b$
- $\ln(a^b) = b \ln a$

這個方法對於處理形如 $y = [f(x)]^{g(x)}$ 的函數特別有效。它甚至能反過來證明指數函數和冪法則的微分：
- **證明指數函數微分 ($a^x$)**: 
  - 設 $y = a^x$。兩邊取對數得 $\ln y = x \ln a$
  - 隱微分得 $\frac{1}{y} \frac{dy}{dx} = \ln a$ (==$\ln a$ is constant==)
  - 故 $\frac{dy}{dx} = y \cdot \ln a = a^x \ln a$
- **證明冪法則 ($x^n$)**: 
  - 設 $y = x^n$。兩邊取對數得 $\ln y = n \ln x$
  - 隱微分得 $\frac{1}{y} \frac{dy}{dx} = n \cdot \frac{1}{x}$
  - 故 $\frac{dy}{dx} = y \cdot \frac{n}{x} = x^n \cdot \frac{n}{x} = nx^{n-1}$

# 公式
## inverse function (反函數)
若 $g$ 是 $f$ 的反函數，即 $g(x) = f^{-1}(x)$，則 $g$ 在點 $a$ 的導數為：
$$ g'(a) = \frac{1}{f'(g(a))} $$
使用萊布尼茲符號 (Leibniz notation) 來表示會更直觀，設 $y=f(x)$，則 $x=f^{-1}(y)$：
$$ \frac{dx}{dy} = \frac{1}{\frac{dy}{dx}} $$

## logarithm (對數)
1.  **自然對數的微分**:
    $$ \frac{d}{dx}(\ln x) = \frac{1}{x} $$
配合[[Chain Rule]]:
    $$ \frac{d}{dx}(\ln u) = \frac{1}{u} \cdot \frac{du}{dx} $$
> [!NOTE] Proof
> $e^{\ln x}=x,derivative: e^{\ln x}\left( \frac{d}{dx}\ln x \right)=1$

2.  **一般對數的微分** (使用換底公式 $\log_a x = \frac{\ln x}{\ln a}$ 推導):
    $$ \frac{d}{dx}(\log_a x) = \frac{1}{x \ln a} $$
    - **證明**: 設 $y = \log_a x$，則其指數形式為 $a^y = x$。使用隱函數微分法對 $x$ 微分：
      - $$\frac{d}{dx}(a^y) = \frac{d}{dx}(x)$$
      - $$a^y (\ln a) \frac{dy}{dx} = 1$$
      - $$\frac{dy}{dx} = \frac{1}{a^y \ln a} = \frac{1}{x \ln a}$$

3.  **對數微分法步驟**:
    1.  給定函數 $y = f(x)$
    2.  等號兩邊取自然對數：$\ln y = \ln(f(x))$
    3.  利用對數律簡化右式
    4.  使用隱函數微分法對兩邊進行微分：$\frac{1}{y} \frac{dy}{dx} = \dots$
    5.  解出 $\frac{dy}{dx}$，並將 $y$ 換回 $f(x)$：$\frac{dy}{dx} = y \cdot (\dots)$

- special: $\frac{d}{dx}\ln|x|= \frac{1}{x}$
