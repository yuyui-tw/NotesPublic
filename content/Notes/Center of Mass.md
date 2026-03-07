---
tags:
  - Physics
up:
  - "[[MOMENTUM, IMPULSE, AND COLLISIONS]]"
related:
  - "[[Momentum]]"
annotation:
aliases:
  - 質心
---
# 概要
質心 (Center of Mass) 是系統質量的加權平均位置。

此概念可簡化複雜系統的運動分析：系統的整體運動，可視為所有質量集中於質心，並僅受淨外力影響的運動。

# 理論
質心的運動只受系統所受的**淨外力**決定，與內力無關。

- **質心速度與總動量**: 系統總動量等於其總質量乘以質心速度。
  $$ \vec{P}_{total} = M_{total} \vec{V}_{cm} $$

- **質心加速度與淨外力**: 作用於系統的淨外力，等於系統總質量乘以其質心加速度。
  $$ \vec{F}_{net, ext} = M_{total} \vec{A}_{cm} $$
  若淨外力為零，系統質心保持靜止或等速直線運動。

# 公式
### 離散系統 (Discrete System)
$$ \vec{R}_{cm} = \frac{1}{M_{total}} \sum_{i} m_i \vec{r}_i $$

### 連續系統 (Continuous System)
$$ \vec{r}_{cm} = \frac{1}{M} \int \vec{r} dm $$

# 公式推導
質心運動定律可由其定義及牛頓第二定律推導。
1.  **質心位置**: $\vec{R}_{cm} = \frac{1}{M} \sum m_i \vec{r}_i$
2.  **對時間微分一次 (速度)**:
    $M \frac{d\vec{R}_{cm}}{dt} = \sum m_i \frac{d\vec{r}_i}{dt}$
    $\implies M \vec{V}_{cm} = \sum m_i \vec{v}_i = \vec{P}_{total}$
3.  **對時間微分兩次 (加速度)**:
    $M \frac{d\vec{V}_{cm}}{dt} = \frac{d\vec{P}_{total}}{dt}$
    $\implies M \vec{A}_{cm} = \frac{d\vec{P}_{total}}{dt}$
4.  **代入牛頓第二定律**: 根據牛頓第二定律，系統總動量的時變率等於作用在系統上的淨外力 ($\frac{d\vec{P}_{total}}{dt} = \sum \vec{F}_{ext}$)。
	內力成對出現且互相抵銷，不影響總動量。
    $$ \implies M_{total} \vec{A}_{cm} = \sum \vec{F}_{ext} $$
