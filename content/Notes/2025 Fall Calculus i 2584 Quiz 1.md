---
tags:
  - QuizReview
  - Math
---

9Qs
title: 大一上第一次微積分小考
content:
2-d,4,5-c,6,7-a
反函數，三角函數及其極限，夾擠，漸進，極限，微分定義

Q1: 
Evaluate $\cos\left( \frac{3\pi}{2}-x \right)$，express the given quantities in terms of $\sin x$ and $\cos x$.
A1: 
**核心觀念:**
和差角公式

**解題關鍵:**
1. 套用 $\cos(A-B) = \cos A \cos B + \sin A \sin B$
2. 代入 $A = \frac{3\pi}{2}, B = x$
3. 利用 $\cos(\frac{3\pi}{2})=0$ 和 $\sin(\frac{3\pi}{2})=-1$ 化簡

**最終答案:**
$-\sin x$

Q2: 
Let $f(x)=x^{2}-2x,x \le 1$. Find the range of f(x) and the inverse function $f^{-1}(x)$.
A2: 
**核心觀念:**
配方法求值域、反函數求解

**解題關鍵:**
1. 將 $f(x)$ 配方為 $(x-1)^2 - 1$
2. 根據定義域 $x \le 1$ 確定值域
3. 令 $y = f(x)$，解出 $x$
4. 交換 $x, y$ 得反函數

**最終答案:**
Range: $[-1, \infty)$, $f^{-1}(x) = 1 - \sqrt{x+1}$

Q3: 
Evaluate $\lim_{ \theta \to 0 } \frac{{\sin \theta}}{\sin 3\theta}$.
A3: 
**核心觀念:**
基本三角極限

**解題關鍵:**
1. 運用 $\lim_{u \to 0} \frac{\sin u}{u} = 1$
2. 將原式變形為 $\frac{\sin \theta}{\theta} \cdot \frac{3\theta}{\sin 3\theta} \cdot \frac{1}{3}$
3. 分別取極限後合併

**最終答案:**
$\frac{1}{3}$

Q4: 
Find the vertical and horizontal asymptotes of $y= \frac{x-1}{x+1}$.
A4: 
**核心觀念:**
漸近線定義

**解題關鍵:**
1. **水平漸近線:** 計算 $\lim_{x \to \pm\infty} f(x)$
2. **垂直漸近線:** 令分母為零

**最終答案:**
Horizontal: $y=1$, Vertical: $x=-1$

Q5: 
Find the derivative of $\sqrt{ x }$ by definition which is a limit. 
A5: 
**核心觀念:**
導數的極限定義

**解題關鍵:**
1. 套用 $f'(x) = \lim_{h \to 0} \frac{\sqrt{x+h} - \sqrt{x}}{h}$
2. 分子分母同乘共軛根式
3. 化簡後求極限

**最終答案:**
$\frac{1}{2\sqrt{x}}$


TARGET DECK: MathQ

source url: 

END
