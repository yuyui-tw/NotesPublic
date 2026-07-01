---
aliases:
  - 反三角函數
tags:
  - Math
up:
  - "[[Implicit Differentiation]]"
related:
  - "[[三角函數]]"
annotation:
---
# 概要
反三角函數是三角函數的反函數，用於根據給定的三角函數值求得對應的角度。
![[graph of inverse trigonometric functions.png]]
# 理論
為了定義反三角函數，我們需要將三角函數的定義域限制在一個使它們成為一對一函數的區間上。

- $\sin^{-1}x = \arcsin x = \theta \iff \sin \theta = x$
	- Domain: $x \in [-1, 1]$
	- Range: $\theta \in \left[ -\frac{\pi}{2}, \frac{\pi}{2} \right]$

- $\cos^{-1}x = \arccos x = \theta \iff \cos \theta = x$
	- Domain: $x \in [-1, 1]$
	- Range: $\theta \in [0, \pi]$

- $\tan^{-1}x = \arctan x = \theta \iff \tan \theta = x$
	- Domain: $x \in (-\infty, \infty)$
	- Range: $\theta \in \left( -\frac{\pi}{2}, \frac{\pi}{2} \right)$

- $\csc^{-1}x  = \theta \iff \csc \theta = x$
	- Domain: $x \in (-\infty, -1] \cup [1, \infty)$
	- Range: $\theta \in \left[ -\frac{\pi}{2}, 0 \right) \cup \left( 0, \frac{\pi}{2} \right]$

- $\sec^{-1}x = \operatorname{arcsec} x = \theta \iff \sec \theta = x$
	- Domain: $x \in (-\infty, -1] \cup [1, \infty)$
	- Range: $\theta \in \left[ 0, \frac{\pi}{2} \right) \cup \left( \frac{\pi}{2}, \pi \right]$

- $\cot^{-1}x = \operatorname{arccot} x = \theta \iff \cot \theta = x$
	- Domain: $x \in (-\infty, \infty)$
	- Range: $\theta \in (0, \pi)$

> [!NOTE] 奇、偶函數
> - **奇函數 (Odd Functions):** $\sin^{-1}(-x) = -\sin^{-1}(x)$, $\tan^{-1}(-x) = -\tan^{-1}(x)$, $\csc^{-1}(-x) = -\csc^{-1}(x)$
> - **偶函數 (Even Functions):** N/A (在標準定義範圍內，反餘弦、反餘割、反餘切均不為嚴格的奇函數或偶函數，但有恆等式如 $\cos^{-1}(-x) = \pi - \cos^{-1}(x)$)

^6c25bc

# 公式
## Derivatives of Inverse Trigonometric Functions
- $\frac{d}{dx}(\sin^{-1}x) = \frac{1}{\sqrt{1-x^2}}$
- $\frac{d}{dx}(\cos^{-1}x) = -\frac{1}{\sqrt{1-x^2}}$
- $\frac{d}{dx}(\tan^{-1}x) = \frac{1}{1+x^2}$
$$\int \frac{1}{a^2 + x^2} dx = \frac{1}{a} \arctan\left(\frac{x}{a}\right) + C$$
- $\frac{d}{dx}(\csc^{-1}x) = -\frac{1}{x\sqrt{x^2-1}}$
- $\frac{d}{dx}(\sec^{-1}x) = \frac{1}{x\sqrt{x^2-1}}$
- $\frac{d}{dx}(\cot^{-1}x) = -\frac{1}{1+x^2}$

### 證明 (Proof)
我們以 $\frac{d}{dx}(\sin^{-1}x)$ 為例，使用隱微分法進行證明：
1.  令 $y = \sin^{-1}x$。根據定義，這等價於 $\sin y = x$，其中 $y \in \left[ -\frac{\pi}{2}, \frac{\pi}{2} \right]$。
2.  對 $\sin y = x$ 兩邊同時對 $x$ 進行微分：
    $$ \frac{d}{dx}(\sin y) = \frac{d}{dx}(x) $$
    $$ (\cos y) \cdot \frac{dy}{dx} = 1 $$
3.  求解 $\frac{dy}{dx}$：
    $$ \frac{dy}{dx} = \frac{1}{\cos y} $$
4.  現在需要將 $\cos y$ 用 $x$ 來表示。我們使用三角恆等式 $\sin^2 y + \cos^2 y = 1$，得到 $\cos^2 y = 1 - \sin^2 y$。
5.  因為 $y \in \left[ -\frac{\pi}{2}, \frac{\pi}{2} \right]$，在這個區間內 $\cos y \ge 0$。因此，我們可以取正平方根：
    $$ \cos y = \sqrt{1 - \sin^2 y} $$
6.  將 $\sin y = x$ 代入上式：
    $$ \cos y = \sqrt{1 - x^2} $$
7.  最後，將此結果代回步驟 3 的式子中，即得證：
    $$ \frac{dy}{dx} = \frac{d}{dx}(\sin^{-1}x) = \frac{1}{\sqrt{1-x^2}} $$

#### 推導至其他公式
其他反三角函數的微分公式皆可透過類似的隱微分法推得。例如，對於 $y = \cos^{-1}x$，可從 $\cos y = x$ 開始。另外，也可以利用餘角恆等式，例如：
$$ \sin^{-1}x + \cos^{-1}x = \frac{\pi}{2} $$
對兩邊同時微分：
$$ \frac{d}{dx}(\sin^{-1}x) + \frac{d}{dx}(\cos^{-1}x) = 0 $$
$$ \frac{1}{\sqrt{1-x^2}} + \frac{d}{dx}(\cos^{-1}x) = 0 $$
$$ \frac{d}{dx}(\cos^{-1}x) = -\frac{1}{\sqrt{1-x^2}} $$

## 餘角恆等式 (Cofunction Identities)
- $\sin^{-1}x + \cos^{-1}x = \frac{\pi}{2}$
- $\tan^{-1}x + \cot^{-1}x = \frac{\pi}{2}$
- $\sec^{-1}x + \csc^{-1}x = \frac{\pi}{2}$
