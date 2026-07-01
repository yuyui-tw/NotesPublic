---
aliases:
  - 陀螺儀進動
tags:
  - Physics
up:
  - "[[Angular momentum|角動量]]"
related:
annotation:
---
# 概要
陀螺儀進動是旋轉物體的轉軸，在受外力矩作用時，其轉軸方向垂直於力矩方向進行圓周運動的現象。

# 核心概念
進動源於角動量守恆。當外力矩 $\vec{\tau}$ 施加於一具有角動量 $\vec{L}$ 的旋轉物體時，此力矩會導致角動量產生變化 ($d\vec{L} = \vec{\tau} dt$)。
若力矩方向垂直於角動量，則角動量的 *方向* 將隨時間改變，而非其大小，從而使自旋軸繞著一個固定軸穩定轉動。

# 結構/要素
- **角動量 ([[Angular momentum]]), $\vec{L}$**: $L = I\omega$，其中 $I$ 為轉動慣量，$\omega$ 為自旋角速度。
- **外力矩 (Torque), $\vec{\tau}$**: $\vec{\tau} = \vec{r} \times \vec{F}$，是造成進動的原因。例如，重力產生的力矩 $\tau = mgr$。
- **進動角速度 (Precession Angular Velocity), $\Omega$**: 描述自旋軸轉動快慢的物理量。

# 原理/推導
根據牛頓第二定律的轉動形式，力矩等於角動量的時變率：
$$ \vec{\tau} = \frac{d\vec{L}}{dt} $$
在時間 $dt$ 內，角動量向量的變化量為 $d\vec{L} = \vec{\tau} dt$。

從俯視角觀察，角動量向量 $\vec{L}$ 的末端在 $dt$ 時間內移動的弧長為 $|d\vec{L}| = L \sin\phi \cdot d\theta$，其中 $\phi$ 是 $\vec{L}$ 與固定軸的夾角，而 $d\theta$ 是進動掃過的角度。

進動角速度 $\Omega$ 定義為 $\Omega = \frac{d\theta}{dt}$。結合以上各式可得：
$$ \Omega = \frac{d\theta}{dt} = \frac{|d\vec{L}|/dt}{L\sin\phi} = \frac{\tau}{L\sin\phi} $$

**特例：水平進動**
當陀螺儀的自旋軸接近水平時，$\phi \approx 90^\circ$，$\sin\phi \approx 1$。
此時，若力矩由重力產生 ($\tau = mgr$)，且角動量為 $L=I\omega$，則公式可簡化為：
$$ \Omega = \frac{mgr}{I\omega} $$
此結果顯示，自旋速度 $\omega$ 越快，進動速度 $\Omega$ 越慢。
