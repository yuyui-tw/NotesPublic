---
aliases:
  - 三角換元法
  - Trigonometric Substitution
  - 三角代換法
tags:
  - Math
up: "[[Integral]]"
related: "[[Trigonometric Integral]]"
---

# 概要 (Summary)
三角換元法 (Trigonometric Substitution) 是一種特殊的積分換元技巧，專門用於處理含有特定形式根號的被積函數。其核心思想是，通過引入一個三角函數作為新的變數，利用畢氏恆等式來**消去根號**，從而將一個看似複雜的代數函數積分轉化為一個 [[Trigonometric Integral|三角函數積分]]。

# 核心概念 (The Substitutions)
本方法主要針對以下三種含有根號的表達式。每種形式都有其對應的換元策略和參考三角形。

| 根號形式 (Expression) | 換元 (Substitution) | 使用的恆等式 (Identity) | 角度範圍 (Range) |
| :--- | :--- | :--- | :--- |
| $\sqrt{a^2 - x^2}$ | $x = a \sin\theta$ | $a^2 - a^2\sin^2\theta = a^2\cos^2\theta$ | $-\frac{\pi}{2} \le \theta \le \frac{\pi}{2}$ |
| $\sqrt{a^2 + x^2}$ | $x = a \tan\theta$ | $a^2 + a^2\tan^2\theta = a^2\sec^2\theta$ | $-\frac{\pi}{2} < \theta < \frac{\pi}{2}$ |
| $\sqrt{x^2 - a^2}$ | $x = a \sec\theta$ | $a^2\sec^2\theta - a^2 = a^2\tan^2\theta$ | $0 \le \theta < \frac{\pi}{2}$ 或 $\pi \le \theta < \frac{3\pi}{2}$ |

# 結構/要素 (The Process)
1.  **識別形式與換元:** 根據積分式中的根號，從上表中選擇合適的換元 $x=f(\theta)$。同時計算出 $dx = f'(\theta) d\theta$。
2.  **執行換元:** 將原積分中的 $x$, $dx$ 以及根號部分完全用 $\theta$ 的表達式替換。利用恆等式消去根號。
3.  **計算三角積分:** 求解換元後得到的三角函數積分。這可能需要用到 [[Trigonometric Integral]] 中的技巧。
4.  **換回原變數:** 根據初始的換元關係，畫出**參考三角形**，將積分結果中的三角函數表達式重新換回成關於原變數 $x$ 的代數式。

# 原理/推導 (Reference Triangles)
參考三角形是從換元關係推導出來的，用於在積分完成後將 $\theta$ 換回 $x$。
- **For $x = a \sin\theta$ ($\sin\theta = x/a$):**
  - 斜邊 (Hypotenuse): $a$
  - 對邊 (Opposite): $x$
  - 鄰邊 (Adjacent): $\sqrt{a^2 - x^2}$

>$\int \frac{1}{\sqrt{\mathbf{a^2 - u^2}}} du=\arcsin\left(\frac{u}{a}\right) + C$
- **For $x = a \tan\theta$ ($\tan\theta = x/a$):**
  - 鄰邊: $a$
  - 對邊: $x$
  - 斜邊: $\sqrt{a^2 + x^2}$

>$$\int \frac{du}{\sqrt{u^2+a^2}} = \ln |u + \sqrt{u^2+a^2}|$$
- **For $x = a \sec\theta$ ($\sec\theta = x/a$):**
  - 鄰邊: $a$
  - 斜邊: $x$
  - 對邊: $\sqrt{x^2 - a^2}$

>$\int \frac{1}{\sqrt{\mathbf{u^2 - a^2}}} du=\ln u + \sqrt{u^2 - a^2}$
# 範例 (Example)
**計算積分 $\int \frac{1}{x^2 \sqrt{4-x^2}} \,dx$**

1.  **識別形式與換元:**
    - 形式為 $\sqrt{a^2 - x^2}$，其中 $a=2$。
    - 換元: $x = 2\sin\theta$
    - 微分: $dx = 2\cos\theta \,d\theta$
    - 根號: $\sqrt{4-x^2} = \sqrt{4-4\sin^2\theta} = \sqrt{4\cos^2\theta} = 2\cos\theta$

2.  **執行換元:**
    $$ \int \frac{1}{(2\sin\theta)^2 (2\cos\theta)} (2\cos\theta \,d\theta) $$
    $$ = \int \frac{1}{4\sin^2\theta} \,d\theta = \frac{1}{4} \int \csc^2\theta \,d\theta $$

3.  **計算三角積分:**
    $$ \frac{1}{4} (-\cot\theta) + C = -\frac{1}{4}\cot\theta + C $$

4.  **換回原變數:**
    - 從 $x = 2\sin\theta$ 可知 $\sin\theta = x/2$。
    - 畫參考三角形：斜邊為 2，對邊為 $x$，則鄰邊為 $\sqrt{4-x^2}$。
    - 從三角形可知: $\cot\theta = \frac{\text{Adjacent}}{\text{Opposite}} = \frac{\sqrt{4-x^2}}{x}$。
    - 代回結果:
      $$ -\frac{1}{4} \frac{\sqrt{4-x^2}}{x} + C $$