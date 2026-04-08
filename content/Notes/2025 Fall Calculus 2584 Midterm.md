---
tags:
  - QuizReview
---
START
9Qs
title: 2025 Fall Calculus 2584 Midterm
content: 
不定型微分，[[Inverse Trigonometric function|反三角函數]]極限與微分，二階微分，[[均值定理|The Mean Value Theorem]]與其表示法

Q1: 
Evaluate $$
\lim_{ x \to 0 } \frac{x}{\arcsin x}$$
A1: 
令 $\theta=\arcsin x$, 則 $x=\sin \theta$。
當 $x \to 0$ 時，$\theta \to 0$。
因此，極限變為：
$$
\lim_{ \theta \to 0 } \frac{\sin \theta}{\theta} = 1
$$
此為標準的三角函數極限。
Q2: 
Evaluate $$
\lim_{ \theta \to \frac{\pi}{2}^{+} } \sec x$$
A2: 
假設題目應為 $\sec \theta$ 以符合極限變數：
$$
\lim_{ \theta \to \frac{\pi}{2}^{+} } \sec \theta = \lim_{ \theta \to \frac{\pi}{2}^{+} } \frac{1}{\cos \theta}
$$
當 $\theta$ 從比 $\frac{\pi}{2}$ 大的方向趨近時（即從右側趨近），$\cos \theta$ 會從負的方向趨近於 $0$（記為 $0^{-}$）。
因此，
$$
\lim_{ \theta \to \frac{\pi}{2}^{+} } \frac{1}{\cos \theta} = -\infty
$$

Q3: 
evaluate$$
\lim_{ x \to \infty } (\sin \sqrt{ x^{2}+2 }-\sin x)$$
A3:
使用和差化積公式：$\sin A - \sin B = 2 \cos \left( \frac{A+B}{2} \right) \sin \left( \frac{A-B}{2} \right)$。
令 $A = \sqrt{x^2+2}$ 且 $B = x$。

首先，計算 $\lim_{x \to \infty} (A-B)$：
$$
\lim_{x \to \infty} (\sqrt{x^2+2} - x) = \lim_{x \to \infty} \frac{(\sqrt{x^2+2} - x)(\sqrt{x^2+2} + x)}{\sqrt{x^2+2} + x} \\
= \lim_{x \to \infty} \frac{x^2+2 - x^2}{\sqrt{x^2+2} + x} = \lim_{x \to \infty} \frac{2}{\sqrt{x^2+2} + x} = 0
$$
因此，$\lim_{x \to \infty} \frac{A-B}{2} = 0$。

現在考慮原式：
$$
\lim_{ x \to \infty } 2 \cos \left( \frac{\sqrt{x^{2}+2}+x}{2} \right) \sin \left( \frac{\sqrt{x^{2}+2}-x}{2} \right)
$$
當 $x \to \infty$ 時，$\frac{\sqrt{x^{2}+2}-x}{2} \to 0$。我們可以使用小角度近似 $\sin u \approx u$。
所以，$\sin \left( \frac{\sqrt{x^{2}+2}-x}{2} \right) \approx \frac{\sqrt{x^{2}+2}-x}{2} = \frac{1}{\sqrt{x^{2}+2}+x}$。

極限變為：
$$
\lim_{ x \to \infty } 2 \cos \left( \frac{\sqrt{x^{2}+2}+x}{2} \right) \cdot \frac{1}{\sqrt{x^{2}+2}+x}
$$
當 $x \to \infty$ 時，$\frac{\sqrt{x^{2}+2}+x}{2} \to \infty$。$\cos \left( \frac{\sqrt{x^{2}+2}+x}{2} \right)$ 項會在 -1 和 1 之間震盪（有界函數）。
而 $\frac{1}{\sqrt{x^{2}+2}+x}$ 項會趨近於 $0$。
根據夾擠定理，一個有界函數乘以一個趨近於零的函數，其極限為零。
$$
= 0
$$

Q4:
evaluate$$
\lim_{ x \to -\infty } \frac{{3x^{3}-1}}{x^{2}+2x+1}$$
A4:
計算當 $x \to -\infty$ 時的極限，我們將分子和分母同除以分母的最高次項 $x^2$：
$$
\lim_{ x \to -\infty } \frac{{3x^{3}-1}}{x^{2}+2x+1} = \lim_{ x \to -\infty } \frac{\frac{3x^{3}}{x^2}-\frac{1}{x^2}}{\frac{x^{2}}{x^2}+\frac{2x}{x^2}+\frac{1}{x^2}} \\
= \lim_{ x \to -\infty } \frac{3x-\frac{1}{x^2}}{1+\frac{2}{x}+\frac{1}{x^2}}
$$
當 $x \to -\infty$ 時：
$3x \to -\infty$
$\frac{1}{x^2} \to 0$
$\frac{2}{x} \to 0$
因此，極限為：
$$
= \frac{-\infty - 0}{1+0+0} = -\infty
$$

Q5: 
Let $f(x)=x^{3}-2x^{2}+2,x\ge 2$. Find $\frac{df^{-1}}{dx}$ at $x=11=f(3)$
A5: 
我們要求在 $x=11$ 時的反函數微分值 $\frac{df^{-1}}{dx}$。
反函數的微分公式為：$\frac{df^{-1}}{dx}(a) = \frac{1}{f'(f^{-1}(a))}$。
給定 $f(x)=x^{3}-2x^{2}+2$。
題目給出 $f(3)=11$，因此 $f^{-1}(11) = 3$。

首先，計算 $f(x)$ 的微分：
$f'(x) = 3x^2 - 4x$。

接著，計算在 $x=3$ 時的微分值：
$f'(3) = 3(3)^2 - 4(3) = 3(9) - 12 = 27 - 12 = 15$。

最後，代入反函數微分公式：
$$
\frac{df^{-1}}{dx}(11) = \frac{1}{f'(f^{-1}(11))} = \frac{1}{f'(3)} = \frac{1}{15}
$$

Q6: 
Find derivative of $$
y= \frac{\sec(\ln x)}{x}$$
A6: 
為了求 $y= \frac{\sec(\ln x)}{x}$ 的微分，我們使用除法規則：$\left( \frac{u}{v} \right)' = \frac{u'v - uv'}{v^2}$。
令 $u = \sec(\ln x)$ 且 $v = x$。

首先，計算 $u'$：
使用連鎖律，$\frac{d}{dx}(\sec(\ln x)) = \sec(\ln x) \tan(\ln x) \cdot \frac{d}{dx}(\ln x) = \sec(\ln x) \tan(\ln x) \cdot \frac{1}{x}$。
所以，$u' = \frac{\sec(\ln x) \tan(\ln x)}{x}$。

接著，計算 $v'$：
$v' = \frac{d}{dx}(x) = 1$。

現在，應用除法規則：
$$
\frac{dy}{dx} = \frac{\left( \frac{\sec(\ln x) \tan(\ln x)}{x} \right) \cdot x - \sec(\ln x) \cdot 1}{x^2} \\
= \frac{\sec(\ln x) \tan(\ln x) - \sec(\ln x)}{x^2} \\
= \frac{\sec(\ln x) (\tan(\ln x) - 1)}{x^2}
$$

Q7: 
Given the curve $xy+y^{3}=2$, use implicit differentiation to find $\frac{dy}{dx}, \frac{d^{2}y}{dx^{2}}$, and tangent line at (1, 1).
A7: 
給定曲線 $xy+y^{3}=2$。

**1. 使用隱微分計算 $\frac{dy}{dx}$：**
將方程式兩邊對 $x$ 進行微分：
$$
\frac{d}{dx}(xy) + \frac{d}{dx}(y^3) = \frac{d}{dx}(2)
$$
對 $xy$ 使用乘法規則，對 $y^3$ 使用連鎖律：
$$
(1 \cdot y + x \cdot \frac{dy}{dx}) + (3y^2 \cdot \frac{dy}{dx}) = 0 \\
y + x \frac{dy}{dx} + 3y^2 \frac{dy}{dx} = 0
$$
提出 $\frac{dy}{dx}$：
$$
(x + 3y^2) \frac{dy}{dx} = -y \\
\frac{dy}{dx} = \frac{-y}{x + 3y^2}
$$
在點 $(1, 1)$ 的微分值：
$$
\frac{dy}{dx} \Big|_{(1,1)} = \frac{-1}{1 + 3(1)^2} = \frac{-1}{1+3} = \frac{-1}{4}
$$

**2. 使用隱微分計算 $\frac{d^{2}y}{dx^{2}}$：**
將 $\frac{dy}{dx} = \frac{-y}{x + 3y^2}$ 再次對 $x$ 進行微分，使用除法規則。
令 $u = -y$ 且 $v = x + 3y^2$。
$u' = -\frac{dy}{dx}$。
$v' = 1 + 6y \frac{dy}{dx}$。

$$
\frac{d^{2}y}{dx^{2}} = \frac{u'v - uv'}{v^2} = \frac{(-\frac{dy}{dx})(x + 3y^2) - (-y)(1 + 6y \frac{dy}{dx})}{(x + 3y^2)^2}
$$
代入 $\frac{dy}{dx} = \frac{-y}{x + 3y^2}$：
$$
\frac{d^{2}y}{dx^{2}} = \frac{(-\frac{-y}{x + 3y^2})(x + 3y^2) - (-y)(1 + 6y (\frac{-y}{x + 3y^2}))}{(x + 3y^2)^2} \\
= \frac{y - (-y)(1 - \frac{6y^2}{x + 3y^2})}{(x + 3y^2)^2} \\
= \frac{y + y - \frac{6y^3}{x + 3y^2}}{(x + 3y^2)^2} \\
= \frac{2y - \frac{6y^3}{x + 3y^2}}{(x + 3y^2)^2}
$$
為了簡化，將分子和分母同乘以 $(x + 3y^2)$：
$$
\frac{d^{2}y}{dx^{2}} = \frac{2y(x + 3y^2) - 6y^3}{(x + 3y^2)^3} \\
= \frac{2xy + 6y^3 - 6y^3}{(x + 3y^2)^3} \\
= \frac{2xy}{(x + 3y^2)^3}
$$
在點 $(1, 1)$ 的二階微分值：
$$
\frac{d^{2}y}{dx^{2}} \Big|_{(1,1)} = \frac{2(1)(1)}{(1 + 3(1)^2)^3} = \frac{2}{(1+3)^3} = \frac{2}{4^3} = \frac{2}{64} = \frac{1}{32}
$$

**3. 計算在點 (1, 1) 的切線方程式：**
切線方程式的形式為 $y - y_1 = m(x - x_1)$。
我們有 $(x_1, y_1) = (1, 1)$ 且斜率 $m = \frac{dy}{dx} \Big|_{(1,1)} = -\frac{1}{4}$。
$$
y - 1 = -\frac{1}{4}(x - 1) \\
4(y - 1) = -(x - 1) \\
4y - 4 = -x + 1 \\
x + 4y - 5 = 0
$$


TARGET DECK: 

source url: 

END