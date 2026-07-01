---
aliases:
  - 角動量
tags:
  - Physics
up:
  - "[[Rotational motion]]"
related:
  - "[[Momentum]]"
annotation:
---
# 概要
角動量 (Angular Momentum, $\vec{L}$) 是描述物體轉動狀態的物理量，可視為轉動版本的「動量」。它是一個向量，方向由右手定則決定。

對於一個繞固定軸轉動的剛體，角動量可以簡單地表示為其**轉動慣量** ($I$) 與**角速度** ($\vec{\omega}$) 的乘積。

# 理論
### 單一質點的角動量 (Angular Momentum of a Single Particle)
對於一個質量為 $m$，位置向量為 $\vec{r}$，動量為 $\vec{p} = m\vec{v}$ 的質點，其角動量 $\vec{L}$ 定義為：
$$ \vec{L} = \vec{r} \times \vec{p} $$
其大小為 $L = rp\sin\theta = rmv\sin\theta$，方向垂直於由 $\vec{r}$ 和 $\vec{p}$ 構成的平面。

### 剛體的角動量 (Angular Momentum of a Rigid Body)
對於繞固定軸轉動的剛體，其總角動量是所有質點角動量的向量和。對於對稱剛體，可以證明其總角動量與角速度方向相同，大小為：
$$ L = I\omega $$
寫成向量形式為：
$$ \vec{L} = I\vec{\omega} $$

### 力矩與角動量變化 (Torque and Change in Angular Momentum)
角動量的時變率等於作用在物體上的淨外力矩。這是牛頓第二定律的轉動形式。
$$ \sum \vec{\tau}_{ext} = \frac{d\vec{L}}{dt} $$
- 若淨外力矩為零，則系統的總角動量守恆。

### 角動量守恆 (Conservation of Angular Momentum)
**若一個系統所受的淨外力矩為零，則該系統的總角動量保持不變。**
$$ \text{If } \sum \vec{\tau}_{ext} = 0, \text{ then } \vec{L}_{total} = \text{constant} $$
$$ \implies I_i \omega_i = I_f \omega_f $$
這是物理學中最基本的守恆定律之一。一個常見的例子是，滑冰選手在旋轉時收縮手臂（減小轉動慣量 $I$），其轉速 ($\omega$) 會因此增加，以保持角動量 $L$ 守恆。

# 公式
- **單一質點**: $\vec{L} = \vec{r} \times \vec{p}$
- **剛體繞固定軸**: $\vec{L} = I\vec{\omega}$
- **力矩與角動量關係**: $\sum \vec{\tau}_{ext} = \frac{d\vec{L}}{dt}$
- **角動量守恆**: 若 $\sum \vec{\tau}_{ext} = 0$，則 $I_i \omega_i = I_f \omega_f$
