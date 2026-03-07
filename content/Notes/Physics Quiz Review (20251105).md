--- 
tags:
#QuizReview #Physics 

---
START
7Qs
title: Physics Quiz Review (20251105)
content:
轉動慣量、力學

Q1: Find the rotational inertia of a hollow cylinder with mass M, inner and outer radius a and b. (15%)
A1:
**核心觀念:**
- 轉動慣量 (Rotational Inertia)
- 體密度 (Volume Density)

**解題關鍵:**
1.  將空心圓柱體視為許多無限薄的圓環組成。
2.  寫出微小質量元素 `dm` 的表示式。
3.  對半徑 `r` 從 `a` 到 `b` 積分 `r²dm`。
4.  利用總質量 `M` 與密度 `ρ` 的關係式代換，化簡結果。

**解題思路:**
1.  **建立積分:** 轉動慣量公式為 $I = \int r^2 dm$。
2.  **質量元素 dm:** 考慮一個半徑為 `r`、厚度為 `dr` 的薄圓環，其體積為 $dV = (2\pi r dr)h$，質量為 $dm = \rho dV = \rho (2\pi rh dr)$，其中 $\rho$ 是密度，h 是高度。
3.  **積分計算:**
    $I = \int_a^b r^2 (\rho 2\pi rh dr) = 2\pi\rho h \int_a^b r^3 dr = 2\pi\rho h [\frac{1}{4}r^4]_a^b = \frac{1}{2}\pi\rho h (b^4 - a^4)$。
4.  **密度代換:** 總質量 $M = \rho V = \rho (\pi b^2 h - \pi a^2 h) = \rho \pi h (b^2 - a^2)$。因此，$
ho = \frac{M}{\pi h (b^2 - a^2)}$。
5.  **化簡:** 將 $
ho$ 代入 I 的表達式:
    $I = \frac{1}{2}\pi h ( \frac{M}{\pi h (b^2 - a^2)} ) (b^4 - a^4) = \frac{1}{2}M \frac{(b^2-a^2)(b^2+a^2)}{b^2-a^2} = \frac{1}{2}M(a^2+b^2)$。

---

Q2: Prove that the rotational inertia of a uniform thin rod of mass M and length L about an axis through its center and perpendicular to the rod is (1/12)ML². From the result of (a), use parallel-axis theorem to find the rotational inertia about a new axis in the edge. (10%)
A2:
**核心觀念:**
- 轉動慣量 (Rotational Inertia)
- 線密度 (Linear Density)
- 平行軸定理 (Parallel-Axis Theorem)

**解題關鍵:**
1.  (a) 對於細桿，使用線密度 $\lambda = M/L$。積分範圍為從 -L/2 到 L/2。
2.  (b) 平行軸定理: $I = I_{cm} + Md^2$，其中 d 是新軸到質心軸的距離。

**解題思路:**
(a) **質心轉動慣量 $I_{cm}$**
- **線密度:** $\lambda = M/L$。在位置 x 處取一小段 dx，其質量 $dm = \lambda dx$。
- **積分:** $I_{cm} = \int r^2 dm = \int_{-L/2}^{L/2} x^2 (\lambda dx) = \lambda [\frac{1}{3}x^3]_{-L/2}^{L/2}$
- **計算:** $I_{cm} = \frac{\lambda}{3} [(\frac{L}{2})^3 - (-\frac{L}{2})^3] = \frac{\lambda}{3} [\frac{L^3}{8} + \frac{L^3}{8}] = \frac{\lambda}{3} \frac{L^3}{4} = \frac{M/L}{3} \frac{L^3}{4} = \frac{1}{12}ML^2$。

(b) **平行軸定理**
- **轉軸距離:** 新軸在邊緣，質心在中央，所以兩軸距離 $d = L/2$。
- **計算:** $I_{edge} = I_{cm} + Md^2 = \frac{1}{12}ML^2 + M(\frac{L}{2})^2 = \frac{1}{12}ML^2 + \frac{1}{4}ML^2 = (\frac{1}{12} + \frac{3}{12})ML^2 = \frac{4}{12}ML^2 = \frac{1}{3}ML^2$。

---

Q3: A particle of mass m₁ makes a one-dimensional elastic collision with a particle of mass m₂ initially at rest. What percentage of the initial kinetic energy of m₁ is transferred to m₂ if (a) m₂=2m₁; (b) m₂=0.5m₁? (15%)
A3:
**核心觀念:**
- 一維彈性碰撞 (1D Elastic Collision)
- 動量守恆 (Conservation of Momentum)
- 動能守恆 (Conservation of Kinetic Energy)

**解題關鍵:**
1.  寫出一維彈性碰撞的速度公式: $v_{2f} = \frac{2m_1}{m_1+m_2}v_{1i}$。
2.  計算能量轉移百分比: $\frac{K_{2f}}{K_{1i}} = \frac{\frac{1}{2}m_2 v_{2f}^2}{\frac{1}{2}m_1 v_{1i}^2}$。
3.  將 $v_{2f}$ 代入並化簡，再分別代入(a)和(b)的條件。

**解題思路:**
1.  **能量轉移比例:**
    $\% \text{Transfer} = \frac{K_{2f}}{K_{1i}} = \frac{m_2 v_{2f}^2}{m_1 v_{1i}^2}$
2.  **代入速度公式:**
    $\% \text{Transfer} = \frac{m_2}{m_1} ( \frac{2m_1}{m_1+m_2} )^2 = \frac{m_2}{m_1} \frac{4m_1^2}{(m_1+m_2)^2} = \frac{4m_1 m_2}{(m_1+m_2)^2}$
3.  **(a) m₂ = 2m₁:**
    $\% \text{Transfer} = \frac{4m_1 (2m_1)}{(m_1+2m_1)^2} = \frac{8m_1^2}{(3m_1)^2} = \frac{8}{9} \approx 88.9\%$
4.  **(b) m₂ = 0.5m₁:**
    $\% \text{Transfer} = \frac{4m_1 (0.5m_1)}{(m_1+0.5m_1)^2} = \frac{2m_1^2}{(1.5m_1)^2} = \frac{2}{2.25} = \frac{8}{9} \approx 88.9\%$
    *(Note: The handwritten solution for (b) seems to have a calculation error, it should be 8/9 as well)*

---

Q4: Use integration to locate the CM of the triangular plate of base b and height h shown in the figure below. The plate has a uniform areal mass density σ (kg/m²). (10%)
A4:
**核心觀念:**
- 質心 (Center of Mass, CM)
- 面密度 (Areal Density)

**解題關鍵:**
1.  質心 y 座標公式: $Y_{cm} = \frac{1}{M} \int y \, dm$。
2.  將三角形看作是由許多無限窄的水平長條所組成。
3.  找出在高度 y 處的長條質量 `dm` 的表達式。

**解題思路:**
1.  **建立座標:** 以底邊為 x 軸，頂點在 (0, h)。
2.  **相似三角形:** 在任意高度 y 處，水平長條的寬度 x' 與高度 (h-y) 的關係，可由相似三角形得到: $\frac{x'}{b} = \frac{h-y}{h}$，所以 $x' = \frac{b}{h}(h-y)$。
3.  **質量元素 dm:** 在高度 y 處，厚度為 dy 的長條，其面積 $dA = x' dy = \frac{b}{h}(h-y)dy$。其質量 $dm = \sigma dA = \sigma \frac{b}{h}(h-y)dy$。
4.  **總質量 M:** $M = \int dm = \int_0^h \sigma \frac{b}{h}(h-y)dy = \frac{\sigma b}{h} [hy - \frac{1}{2}y^2]_0^h = \frac{\sigma b}{h} (h^2 - \frac{1}{2}h^2) = \frac{1}{2}\sigma bh$。 (符合三角形面積公式)
5.  **計算 Ycm:**
    $Y_{cm} = \frac{1}{M} \int y \, dm = \frac{1}{\frac{1}{2}\sigma bh} \int_0^h y ( \sigma \frac{b}{h}(h-y) dy )$
    $Y_{cm} = \frac{2}{h} \int_0^h (hy - y^2) dy = \frac{2}{h} [\frac{1}{2}hy^2 - \frac{1}{3}y^3]_0^h$
    $Y_{cm} = \frac{2}{h} (\frac{1}{2}h^3 - \frac{1}{3}h^3) = \frac{2}{h} (\frac{1}{6}h^3) = \frac{1}{3}h$。
    質心在離底邊 h/3 的高度。

---

Q5: At time t=0, a 2150 kg rocket in outer space fires an engine that exerts an increasing force on it in the +x-direction. This force obeys the equation, Fₓ = At², where t is time, and has a magnitude of 781.25 N when t=1.25 s. (a) Find the impulse the engine exerts on the rocket during the 1.5 s interval starting 2 s after the engine is fired. (15%) (b) How much work is done by the engine on the rocket during this interval?
A5:
**核心觀念:**
- 衝量 (Impulse)
- 功 (Work)
- 牛頓第二定律 (F=ma)

**解題關鍵:**
1.  (a) 衝量是力對時間的積分: $J = \int F(t) dt$。
2.  (b) 功是力對位移的積分: $W = \int F(x) dx$。需要先找出速度 v(t) 和位移 x(t) 的函數。

**解題思路:**
1.  **求常數 A:**
    $F_x = At^2 \implies 781.25 = A(1.25)^2 \implies A = \frac{781.25}{1.5625} = 500 \text{ N/s}^2$。
    所以 $F_x(t) = 500t^2$。
2.  **(a) 計算衝量 J:**
    $J = \int_{2.0s}^{3.5s} F_x(t) dt = \int_{2.0}^{3.5} 500t^2 dt = 500 [\frac{1}{3}t^3]_{2.0}^{3.5}$
    $J = \frac{500}{3} (3.5^3 - 2.0^3) = \frac{500}{3} (42.875 - 8) = \frac{500}{3} (34.875) = 5812.5 \text{ N·s}$。
3.  **(b) 計算功 W:**
    - **加速度 a(t):** $a(t) = \frac{F_x(t)}{m} = \frac{500t^2}{2150} = \frac{10}{43}t^2$。
    - **速度 v(t):** $v(t) = v_0 + \int_0^t a(t') dt' = 0 + \int_0^t \frac{10}{43}t'^2 dt' = \frac{10}{129}t^3$。
    - **功的計算:** $W = \Delta K = K_f - K_i = \frac{1}{2}m[v(3.5)^2 - v(2.0)^2]$
      $v(3.5) = \frac{10}{129}(3.5)^3 \approx 3.324 \text{ m/s}$
      $v(2.0) = \frac{10}{129}(2.0)^3 \approx 0.620 \text{ m/s}$
      $W = \frac{1}{2}(2150)[(3.324)^2 - (0.620)^2] = 1075 [11.049 - 0.384] \approx 11464 \text{ J}$。

---

Q6: In an experiment, one of the forces exerted on a proton is F = -αx² i where α = 12 N/m². How much work does F do when the proton moves along the straight-line path from the point (0.1m, 0) to the point (0.3m, 0.4m)? If F is conservative, what is the potential energy function U(x) corresponding to this conservative force? Let U=0 when x=0. (15%)
A6:
**核心觀念:**
- 功 (Work)
- 保守力 (Conservative Force)
- 位能 (Potential Energy)

**解題關鍵:**
1.  功的定義: $W = \int \vec{F} \cdot d\vec{l}$。對於保守力，功只與起點和終點有關，與路徑無關。
2.  位能的定義: $U(x) = -\int_0^x F(x') dx'$。

**解題思路:**
1.  **計算功 W:**
    - 力 $\vec{F}$ 只有 x 分量，所以 $d\vec{l} = dx \hat{i} + dy \hat{j}$ 的點積只剩下 x 部分。
    - $W = \int \vec{F} \cdot d\vec{l} = \int_{x_i}^{x_f} F_x dx = \int_{0.1}^{0.3} -\alpha x^2 dx$
    - $W = -\alpha [\frac{1}{3}x^3]_{0.1}^{0.3} = -12 \times \frac{1}{3} (0.3^3 - 0.1^3)$
    - $W = -4 (0.027 - 0.001) = -4 (0.026) = -0.104 \text{ J}$。
    *(Note: The proton also moves in y, but the force has no y-component, so that part of the path does no work)*
2.  **計算位能 U(x):**
    - $U(x) - U(0) = -\int_0^x F_x(x') dx' = -\int_0^x -\alpha x'^2 dx' = \alpha \int_0^x x'^2 dx'$
    - $U(x) - 0 = \alpha [\frac{1}{3}x'^3]_0^x = \frac{\alpha}{3}x^3$
    - $U(x) = \frac{12}{3}x^3 = 4x^3$。

---

Q7: The potential energy of two atoms in a diatomic molecule is approximated by U(r) = a/r¹² - b/r⁶, where r is the spacing between atoms and a and b are positive constants. (a) Find the force F(r) on one atom as a function of r. (b) Find the equilibrium distance between the two atoms. (20%)
A7:
**核心觀念:**
- 力與位能的關係 (Force and Potential Energy)
- 平衡位置 (Equilibrium Position)

**解題關鍵:**
1.  (a) 力是位能對距離的負導數: $F(r) = -\frac{dU(r)}{dr}$。
2.  (b) 平衡位置發生在淨力為零的地方，即 $F(r)=0$。

**解題思路:**
1.  **(a) 計算力 F(r):**
    $F(r) = -\frac{d}{dr} (ar^{-12} - br^{-6})$
    $F(r) = -[a(-12r^{-13}) - b(-6r^{-7})]$
    $F(r) = -[-12ar^{-13} + 6br^{-7}] = 12ar^{-13} - 6br^{-7}$
2.  **(b) 找平衡距離 r₀:**
    - 令 $F(r_0) = 0$:
      $12ar_0^{-13} - 6br_0^{-7} = 0$
    - $12ar_0^{-13} = 6br_0^{-7}$
    - $\frac{12a}{6b} = \frac{r_0^{13}}{r_0^7} = r_0^6$
    - $r_0^6 = \frac{2a}{b}$
    - $r_0 = (\frac{2a}{b})^{1/6}$