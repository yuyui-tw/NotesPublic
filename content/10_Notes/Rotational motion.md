---
aliases:
  - 轉動
tags:
  - Physics
up:
related:
  - "[[Moment of inertia]]"
annotation:
---
# 概要
轉動 (Rotational motion) 描述物體繞固定軸的圓周運動。

描述轉動的物理量為**角位置** ($\phi$)、**角速度** ($\omega$)、及**角加速度** ($\alpha$)，分別對應於直線運動中的位移、速度和加速度。

# 理論
### 轉動運動學 (Rotational Kinematics)
等角加速度運動的公式與等加速度直線運動公式完全對應：

| 直線運動 (Linear) | 轉動 (Rotational) |
| :--- | :--- |
| $v = v_0 + at$ | $\omega = \omega_0 + \alpha t$ |
| $x = x_0 + v_0t + \frac{1}{2}at^2$ | $\phi = \phi_0 + \omega_0t + \frac{1}{2}\alpha t^2$ |
| $v^2 = v_0^2 + 2a\Delta x$ | $\omega^2 = \omega_0^2 + 2\alpha\Delta\phi$ |

### 轉動動力學 (Rotational Dynamics)
- **Torque|力矩 ($\vec{\tau}$)**: 造成轉動狀態改變的原因，是轉動中的「力」。
  $$ \vec{\tau} = \vec{r} \times \vec{F} $$
- **Moment of inertia|轉動慣量 ($I$)**: 物體抵抗轉動狀態改變的量度，是轉動中的「質量」。
  $$ I = \sum m_i r_i^2 $$
- **轉動的牛頓第二定律**: 淨外力矩等於轉動慣量乘以角加速度。
  $$ \sum \vec{\tau}_{ext} = I \vec{\alpha} $$

# 公式推導 (牛頓第二定律)
1.  **單質點**: 考慮一個質量為 $m$ 的質點，受力 $F$ 作用，繞半徑為 $r$ 的圓周運動。
    - 切線力 $F_t = ma_t$。
    - 切線加速度 $a_t = r\alpha$。
    - 力矩 $\tau = r F_t = r(ma_t) = r(mr\alpha) = (mr^2)\alpha$。
2.  **剛體**: 將剛體視為無數質點的集合，將所有質點的力矩加總：
    $$ \sum \tau_i = \sum (m_i r_i^2) \alpha $$
    因為角加速度 $\alpha$ 對剛體上所有點皆相同，可提出：
    $$ \sum \tau_i = (\sum m_i r_i^2) \alpha $$
    其中 $\sum \tau_i$ 是作用在剛體上的淨力矩 $\sum \tau$，而 $\sum m_i r_i^2$ 就是剛體的轉動慣量 $I$。
    $$ \implies \sum \tau = I \alpha $$

# 公式總覽
### 角量與線量關係
- 切線速度: $v_t = r\omega$
- 切線加速度: $a_t = r\alpha$
- 向心加速度: $a_r = \omega^{2}r$
>related: [[Uniform Circular Motion|UCM]]
### 動力學
- 力矩: $\vec{\tau} = \vec{r} \times \vec{F}$
- 轉動動能: $K_{rot} = \frac{1}{2}I\omega^2$
- 牛頓第二定律: $\sum \tau = I\alpha$
