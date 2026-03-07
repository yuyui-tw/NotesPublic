# 題目 1
#Physics #QuizReview 
**Question:** 
1. Some people are able to spin a basketball on the tip of a finger. It is often done by balancing the ball on the tip of the finger and brushing the other hand along the side of the ball to cause it to rotate. Suppose the ball begins from rest and reaches a final angular speed of 18.65 rad/s in 1.10 s.
(a) Assuming the ball is subject to a constant angular acceleration, what is the magnitude of the constant acceleration? (10%)
(b) Through how many revolutions does the ball rotate during the 1.10 s? (10%)

**解題過程：**

**(a) 角加速度 ($\alpha$):**
- 使用公式：$\omega_f = \omega_i + \alpha t$
- 已知：
    - $\omega_i$ (初角速度) = $0 \text{ rad/s}$ (從靜止開始)
    - $\omega_f$ (末角速度) = $18.65 \text{ rad/s}$
    - $t$ (時間) = $1.10 \text{ s}$
- 計算：
    - $18.65 = 0 + \alpha \cdot 1.10$
    - $\alpha = 18.65 / 1.10 \approx 16.95 \text{ rad/s}^2$

**(b) 總轉動圈數：**
- 使用公式：$\Delta\theta = \omega_i t + \frac{1}{2}\alpha t^2$
- 計算角位移 $\Delta\theta$：
    - $\Delta\theta = 0 \cdot 1.10 + \frac{1}{2} \cdot 16.95 \cdot (1.10)^2$
    - $\Delta\theta \approx 0.5 \cdot 16.95 \cdot 1.21 \approx 10.25 \text{ rad}$ 
- 將角位移從弧度轉換為圈數：
    - $1 \text{ 圈} = 2\pi \text{ rad}$
    - $\text{圈數} = \Delta\theta / (2\pi) \approx 10.25 / (2 \cdot 3.14159) \approx 1.63 \text{ 圈}$

---

# 題目 2

**Question:**
2. A solid sphere of mass M and radius R is rotating around an axis that is tangent to the sphere. What is the rotational inertia of the sphere in this scenario in terms of M and R? (10%)

**解題過程：**
- **平行軸定理：** $I = I_{cm} + Md^2$
- 已知：
    - $I_{cm}$ (繞質心轉動的轉動慣量，對於實心球體) = $\frac{2}{5}MR^2$
    - $d$ (旋轉軸到質心的距離) = $R$ (因為軸與球體相切)
- 計算：
    - $I = \frac{2}{5}MR^2 + MR^2$
    - $I = \frac{7}{5}MR^2$

---

# 題目 3

**Question:**
3. (a) Prove that the rotational inertia of a uniform, long thin rod of mass M and length L about an axis through its center and perpendicular to the rod is (1/12)ML². (10%)
(b) Use parallel-axis theorem to find the rotational inertia about a new axis in the edge (see right figure). (10%)

**解題過程：**

**(a) 證明 $I_{cm} = \frac{1}{12}ML^2$:**
- **定義：** 轉動慣量 $I = \int r^2 dm$
- 設定：
    - 線密度 $\lambda = M/L$，所以 $dm = \lambda dx$
    - 桿的範圍從 $x = -L/2$ 到 $x = +L/2$，旋轉軸在 $x = 0$。
- 積分：
    - $I = \int_{-L/2}^{L/2} x^2 (\lambda dx)$
    - $I = \lambda \int_{-L/2}^{L/2} x^2 dx$
    - $I = \lambda [\frac{x^3}{3}] \Big|_{-L/2}^{L/2}$
    - $I = (M/L) \cdot [ (\frac{L^3}{24}) - (-\frac{L^3}{24}) ]$
    - $I = (M/L) \cdot (\frac{2L^3}{24}) = (M/L) \cdot (\frac{L^3}{12})$
    - $I = \frac{1}{12}ML^2$

**(b) 繞一端的轉動慣量:**
- **平行軸定理：** $I = I_{cm} + Md^2$
- 已知：
    - $I_{cm}$ = $\frac{1}{12}ML^2$ (從 a 部分得知)
    - $d$ (新軸到質心的距離) = $\frac{L}{2}$
- 計算：
    - $I = \frac{1}{12}ML^2 + M(\frac{L}{2})^2$
    - $I = \frac{1}{12}ML^2 + \frac{1}{4}ML^2$
    - $I = (\frac{1}{12} + \frac{3}{12})ML^2 = (\frac{4}{12})ML^2$
    - $I = \frac{1}{3}ML^2$

---

# 題目 4

**Question:**
4. A particle moving at 20 m/s collides elastically with an identical particle at rest. The incoming particle moves off at 30° to the original direction. What is the final speed of each particle? (20%)

**解題過程：**
- **基本守恆定律：**
    1.  動量守恆 (x 和 y 分量)
    2.  動能守恆 (因為是彈性碰撞)
- 設定：
    - $m_1 = m_2 = m$
    - $v_{1i}$ (粒子1初速度) = $20 \text{ m/s}$ (沿 x 軸)
    - $v_{2i}$ (粒子2初速度) = $0 \text{ m/s}$
    - $v_{1f}$ (粒子1末速度) 的角度 $\theta_1 = 30°$
    - $v_{2f}$ (粒子2末速度) 的角度 $\theta_2$
- **動量守恆：**
    - x-分量: $m v_{1i} = m v_{1f} \cos(30°) + m v_{2f} \cos(\theta_2)$
      $20 = v_{1f} (\frac{\sqrt{3}}{2}) + v_{2f} \cos(\theta_2)$  (式1)
    - y-分量: $0 = m v_{1f} \sin(30°) + m v_{2f} \sin(\theta_2)$
      $0 = v_{1f} (\frac{1}{2}) + v_{2f} \sin(\theta_2)$  (式2)
- **動能守恆：**
    - $\frac{1}{2}m v_{1i}^2 = \frac{1}{2}m v_{1f}^2 + \frac{1}{2}m v_{2f}^2$
    - $20^2 = v_{1f}^2 + v_{2f}^2$
    - $400 = v_{1f}^2 + v_{2f}^2$ (式3)
- **求解：**
    - (一個技巧：質量相等的彈性碰撞，若一粒子初速為零，則碰撞後夾角為$90°$，因此 $\theta_2 = -60°$)
    - 將 $\theta_2 = -60°$ 代入 (式1) 和 (式2):
    - 從 (式2): $0 = v_{1f} (\frac{1}{2}) + v_{2f} \sin(-60°)$
      $0 = v_{1f} (\frac{1}{2}) - v_{2f} (\frac{\sqrt{3}}{2})$
      $v_{1f} = v_{2f} \sqrt{3}$ (式2')
    - 將 (式2') 代入 (式1):
      $20 = (v_{2f} \sqrt{3}) (\frac{\sqrt{3}}{2}) + v_{2f} \cos(-60°)$
      $20 = \frac{3}{2} v_{2f} + v_{2f} (\frac{1}{2})$
      $20 = \frac{4}{2} v_{2f} = 2 v_{2f}$
      $v_{2f} = 10 \text{ m/s}$
    - 代入 (式2'): $v_{1f} = 10 \sqrt{3} \approx 17.32 \text{ m/s}$

**最終速度：**
- 入射粒子: $v_{1f} = 10 \sqrt{3} \approx 17.32 \text{ m/s}$
- 靜止粒子: $v_{2f} = 10 \text{ m/s}$

# 題目 5

**Question:**
5. Canadian nuclear reactors use heavy water moderators in which elastic collisions occur between the neutrons and deuterons of mass 2u. 
(a) What is the speed of a neutron, expressed as a fraction of its original speed, after a head-on, elastic collision with a deuteron that is initially at rest? 
(b) What is its kinetic energy, expressed as a fraction of its original kinetic energy?
(c) How many such successive collisions will reduce the speed of a neutron to 1/59000 of its original value? (20%)

**解題過程：**

- **設定：**
    - $m_1$ (中子質量) $\approx u$
    - $m_2$ (氘核質量) $= 2u$
    - $v_{1i}$ (中子初速度)
    - $v_{2i}$ (氘核初速度) $= 0$ (靜止)

**(a) 碰撞後中子速度 $v_{1f}$：**
- **一維彈性碰撞公式：** $v_{1f} = \left(\frac{m_1 - m_2}{m_1 + m_2}\right) v_{1i}$
- 計算：
    - $v_{1f} = \left(\frac{u - 2u}{u + 2u}\right) v_{1i}$
    - $v_{1f} = \left(\frac{-u}{3u}\right) v_{1i}$
    - $v_{1f} = \left(-\frac{1}{3}\right) v_{1i}$
- **答案：** 碰撞後速度是初始速度的 **-1/3** 倍。速率的比例為 **1/3**。

**(b) 碰撞後動能 $K_{1f}$：**
- **動能公式：** $K = \frac{1}{2}mv^2$
- $K_{1i} = \frac{1}{2}m_1 v_{1i}^2$
- $K_{1f} = \frac{1}{2}m_1 v_{1f}^2 = \frac{1}{2}m_1 \left(-\frac{1}{3} v_{1i}\right)^2 = \frac{1}{2}m_1 \left(\frac{1}{9} v_{1i}^2\right)$
- $K_{1f} = \frac{1}{9} K_{1i}$
- **答案：** 碰撞後動能是初始動能的 **1/9**。

**(c) 連續碰撞次數 $N$：**
- 每次碰撞，速度大小變為原來的 $\frac{1}{3}$。
- 經過 $N$ 次碰撞後的速度為 $v_f = \left(\frac{1}{3}\right)^N v_i$。
- 我們要找 $N$ 使得$\frac{v_f}{v_i} = \frac{1}{59000}$。
- $\left(\frac{1}{3}\right)^N = \frac{1}{59000}$
- $3^N = 59000$
- 取對數：$N \log(3) = \log(59000)$
- $N = \frac{\log(59000)}{\log(3)}$
- $N \approx \frac{4.7709}{0.4771} \approx 10$
- **答案：** 大約需要 **10** 次碰撞。

---

# 題目 6

**Question:**
6. Use integration to locate the CM of the triangular plate of base b and height h shown in the figure below. The plate has a uniform areal mass density $\sigma$ (kg/m²). (10%)

**解題過程：**
- **質心公式 (y分量)：** $y_{cm} = \frac{1}{M} \int y \, dm$
- **設定：**
    - 總質量 $M = \sigma A = \sigma \left(\frac{1}{2}\right)bh$
    - 我們取一個在高度 $y$ 處的水平薄片，其厚度為 $dy$。
    - 該薄片的長度為 $x$。由相似三角形可知：$\frac{x}{b} = \frac{h-y}{h} \implies x = \frac{b}{h}(h-y)$
    - 薄片的面積 $dA = x \, dy = \frac{b}{h}(h-y) \, dy$
    - 薄片的質量 $dm = \sigma \, dA = \sigma \frac{b}{h}(h-y) \, dy$
- **積分：**
    - $y_{cm} = \frac{1}{\sigma \frac{bh}{2}} \int_{0}^{h} y \left[\sigma \frac{b}{h}(h-y)\right] \, dy$
    - $y_{cm} = \frac{2}{bh} \frac{b}{h} \int_{0}^{h} (hy - y^2) \, dy$
    - $y_{cm} = \frac{2}{h^2} \left[ \frac{h y^2}{2} - \frac{y^3}{3} \right] \Big|_{0}^{h}$
    - $y_{cm} = \frac{2}{h^2} \left[ \left(\\rac{h^3}{2} - \frac{h^3}{3}\right) - 0 \right]$
    - $y_{cm} = \frac{2}{h^2} \left[ \left(\frac{3h^3 - 2h^3}{6}\right) \right]$
    - $y_{cm} = \frac{2}{h^2} \cdot \frac{h^3}{6}$
    - $y_{cm} = \frac{h}{3}$
- **答案：** 質心位於從底部算起 $\frac{h}{3}$ 的高度。

---

# 題目 7

**Question:**
7. A uniform hoop and a uniform solid disk are released from rest from a height h on an incline and roll without slipping.
(a) Which object reaches the bottom of the incline first? Explain your reasoning. (5%)
(b) Find expressions for the speed with which each object reaches the bottom of the incline. (5%)

**解題過程：**
- **能量守恆：** 初始位能 $U_i$ = 末動能 $K_f$ (包含平動和轉動)
    - $Mgh = \frac{1}{2}Mv^2 + \frac{1}{2}I\omega^2$
- **無滑動條件：** $v = R\omega \implies \omega = \frac{v}{R}$
- **轉動慣量 $I$：**
    - 圓環 (Hoop): $I_h = MR^2$
    - 實心圓盤 (Disk): $I_d = \frac{1}{2}MR^2$

**(b) 計算末速度 $v$：**
- **通用公式：**
    - $Mgh = \frac{1}{2}Mv^2 + \frac{1}{2}I(\frac{v}{R})^2$
    - $Mgh = \frac{1}{2}Mv^2 + \frac{I}{2R^2}v^2$
    - $gh = \frac{1}{2}v^2 + \frac{I}{2MR^2}v^2 = v^2 (\frac{1}{2} + \frac{I}{2MR^2})$
    - $v^2 = \frac{2gh}{1 + \frac{I}{MR^2}}$
    - $v = \sqrt{\frac{2gh}{1 + \frac{I}{MR^2}}}$

- **圓環 (Hoop):**
    - $v_h = \sqrt{\frac{2gh}{1+\frac{MR^2}{MR^2}}} = \sqrt{\frac{2gh}{2}} = \sqrt{gh}$

- **實心圓盤 (Disk):**
    - $v_d = \sqrt{\frac{2gh}{1 +\frac{\frac{1}{2}MR^2}{MR^2}}} = \sqrt{\frac{2gh}{1 + \frac{1}{2}}} = \sqrt{\frac{2gh}{\frac{3}{2}}} = \sqrt{\frac{4gh}{3}}$

**(a) 誰先到達？**
- 從 (b) 的結果可知, $v_d = \sqrt{\frac{4}{3} gh} \approx 1.15 \sqrt{gh}$，而 $v_h = \sqrt{gh}$。
- $v_d > v_h$，**實心圓盤** 的末速度較快，因此它會先到達底部。
- **理由：** 根據能量守恆，初始位能 $Mgh$ 轉化為平動動能和轉動動能。實心圓盤的轉動慣量 $\frac{1}{2}MR^2$ 小於圓環的 $MR^2$。這意味著在相同的位能轉換下，圓盤分配給轉動的能量較少，因此有更多的能量分配給平動，導致其平動速度更快。
