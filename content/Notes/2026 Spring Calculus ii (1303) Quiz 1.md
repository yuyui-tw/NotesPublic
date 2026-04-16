---
tags:
  - QuizReview
related:
  - "[[Trigonometric Substitution]]"
  - "[[正項級數]]"
  - "[[Improper Integrals|瑕積分]]"
---
# 2026 Spring Calculus II (1303) Quiz 1 錯題檢討

## 1. Find derivative (微分計算)
**題目：** $y = x \ln(\sec 2x)$

### 解法：
使用 **乘法律 (Product Rule)** 與 **連鎖律 (Chain Rule)**：
$$
\begin{aligned}
y' &= \frac{d}{dx}(x) \cdot \ln(\sec 2x) + x \cdot \frac{d}{dx}(\ln(\sec 2x)) \\
&= 1 \cdot \ln(\sec 2x) + x \cdot \frac{1}{\sec 2x} \cdot (\sec 2x \tan 2x \cdot 2) \\
&= \ln(\sec 2x) + 2x \tan 2x
\end{aligned}
$$

**關鍵點：** $\frac{d}{dx}(\sec 2x) = 2 \sec 2x \tan 2x$，不要漏掉係數 $2$。

---

## 2. Evaluate integrals (積分計算)

### (1) $\int \sin^{3}x dx$
**技巧：** 奇數次方正弦。
$$
\begin{aligned}
\int \sin^{3}x dx &= \int \sin^{2}x \sin x dx \\
&= \int (1 - \cos^{2}x) \sin x dx \\
&\text{Let } u = \cos x, du = -\sin x dx \\
&= -\int (1 - u^{2}) du = \int (u^{2} - 1) du \\
&= \frac{1}{3}u^{3} - u + C = \frac{1}{3}\cos^{3}x - \cos x + C
\end{aligned}
$$

### (2) $\int \sqrt{ \frac{x^{3}-1}{x^{11}} } dx$
**技巧：** 提取公因式簡化根號。
$$
\begin{aligned}
\int \sqrt{ \frac{x^{3}-1}{x^{11}} } dx &= \int \frac{(x^{3}-1)^{1/2}}{x^{11/2}} dx = \int \frac{[x^3(1-x^{-3})]^{1/2}}{x^{11/2}} dx \\
&= \int \frac{x^{3/2}(1-x^{-3})^{1/2}}{x^{11/2}} dx = \int \frac{(1-x^{-3})^{1/2}}{x^{4}} dx \\
&\text{Let } u = 1 - x^{-3}, du = 3x^{-4} dx \implies \frac{1}{x^4} dx = \frac{1}{3} du \\
&= \frac{1}{3} \int u^{1/2} du = \frac{1}{3} \cdot \frac{2}{3} u^{3/2} + C \\
&= \frac{2}{9}(1-x^{-3})^{3/2} + C
\end{aligned}
$$

### (3) $\int \sqrt{ 4-x^{2} }dx$
**技巧：** 三角代換法 ($x = 2\sin\theta$)。
$$
\begin{aligned}
&\text{Let } x = 2\sin\theta, dx = 2\cos\theta d\theta \\
\int \sqrt{ 4-4\sin^{2}\theta } \cdot 2\cos\theta d\theta &= \int 2\cos\theta \cdot 2\cos\theta d\theta = 4 \int \cos^{2}\theta d\theta \\
&= 4 \int \frac{1+\cos 2\theta}{2} d\theta = 2 \int (1+\cos 2\theta) d\theta \\
&= 2\theta + \sin 2\theta + C = 2\theta + 2\sin\theta\cos\theta + C \\
&= 2\arcsin(\frac{x}{2}) + \frac{x\sqrt{4-x^2}}{2} + C
\end{aligned}
$$

### (4) $\int^{\infty}_{1} \frac{1}{x^{3}}dx$
**技巧：** 瑕積分。
$$
\lim_{b \to \infty} \int^{b}_{1} x^{-3} dx = \lim_{b \to \infty} \left[ -\frac{1}{2x^2} \right]^b_1 = \lim_{b \to \infty} \left( -\frac{1}{2b^2} + \frac{1}{2} \right) = \frac{1}{2}
$$

---

## 3. Test the integral for convergence (斂散性測試)
**題目：** $\int_{2}^{\infty} \frac{1}{x^{5}-1}dx$

### 解法：
使用 **極限比較測試法 (Limit Comparison Test, LCT)**：
1. 選擇比較對象：$g(x) = \frac{1}{x^5}$。
2. 已知 $\int_{2}^{\infty} \frac{1}{x^5} dx$ 收斂（$p$-test, $p=5>1$）。
3. 計算極限：
   $$ \lim_{x \to \infty} \frac{1/(x^5-1)}{1/x^5} = \lim_{x \to \infty} \frac{x^5}{x^5-1} = 1 > 0 $$
4. 結論：因為極限為正整數且比較對象收斂，故原積分 **收斂 (Convergent)**。

---
**複習重點：**
- 代換積分時要觀察 $du$ 是否存在。
- 三角代換後通常需要用到倍角公式或半角公式。
- 瑕積分的收斂判斷首選 LCT 或 $p$-test。
