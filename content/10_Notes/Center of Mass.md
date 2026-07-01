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
質心的運動只受系統所受的**淨外力**決定，與內力無關。這意味著無論系統內部的組成部分如何運動，質心的運動軌跡就像是一個質量為 $M_{total}$ 的質點在淨外力作用下的運動。

- **質心速度與總動量**: 系統總動量等於其總質量乘以質心速度。
  $$ \vec{P}_{total} = \sum m_i \vec{v}_i = M_{total} \vec{V}_{cm} $$
  這表示系統的整體平移運動可以用質心的運動來描述。

- **質心加速度與淨外力**: 作用於系統的淨外力，等於系統總質量乘以其質心加速度。
  $$ \vec{F}_{net, ext} = \frac{d\vec{P}_{total}}{dt} = M_{total} \vec{A}_{cm} $$
  若淨外力為零，系統總動量守恆，質心保持靜止或做等速直線運動（[[Momentum|動量守恆定律]]）。

# 公式
### 離散系統 (Discrete System)
對於由數個質點組成的系統，其質心座標為各質點位置的質量加權平均：
$$ \vec{R}_{cm} = \frac{\sum m_i \vec{r}_i}{\sum m_i} = \frac{1}{M_{total}} \sum_{i} m_i \vec{r}_i $$
在分量形式下：
$$ \bar{x} = \frac{\sum m_i x_i}{M}, \quad \bar{y} = \frac{\sum m_i y_i}{M}, \quad \bar{z} = \frac{\sum m_i z_i}{M} $$

### 連續系統 (Continuous System)
對於質量連續分布(函數)的物體，使用積分代替加總：
$$ \vec{r}_{cm} = \frac{1}{M} \int \vec{r} dm $$
其中 $dm$ 是微小質量單元，可表示為 $\rho dV$（體積）、$\sigma dA$（面積）或 $\lambda ds$（長度）。

# 質心計算 (Calculations)
質心位置在本質上可以看作是 **力矩和 / 質量和**（在重力場均勻的情況下，力矩與質量成正比）。

### 1. 質量曲線 (Massive Curve)
若有一曲線 $C$，其密度函數為 $\rho(x,y)$，則總質量 $M = \int_C \rho(x,y) ds$。
- **對 $y$ 軸力矩** ($M_y$): $M_y = \int_C x \rho(x,y) ds$
- **對 $x$ 軸力矩** ($M_x$): $M_x = \int_C y \rho(x,y) ds$
- **質心座標**: $\bar{x} = \frac{M_y}{M}, \bar{y} = \frac{M_x}{M}$

### 2. 平面區域 (Planar Region)
當平面區域 $R$ 由 $y=f(x)$、 $y=g(x)$ 與 $x=a$、$x=b$ 包圍，且密度 $\rho$ 為常數時：
- 此時質心僅由幾何形狀決定，稱為 **形心 (Centroid)**。
- 若 $g(x)=0$（即曲線與 x 軸之間），則：
  $$ \bar{x} = \frac{1}{A} \int_a^b x f(x) dx, \quad \bar{y} = \frac{1}{A} \int_a^b \frac{1}{2}[f(x)]^2 dx $$
  *註：此公式意義在於將二維積分轉化為一維積分（左右切齊型）。*

### 3. 立體區域 (Solid Region)
對於體積 $V$，質心座標為：
$$ \bar{x} = \frac{1}{M} \iiint_V x \rho dV, \quad \bar{y} = \frac{1}{M} \iiint_V y \rho dV, \quad \bar{z} = \frac{1}{M} \iiint_V z \rho dV $$

# 補充與關聯
- **質心 vs. 形心**: 
    - **質心 (Center of Mass)**: 考慮質量分布（密度可能不均）。
    - **形心 (Centroid)**: 僅考慮幾何形狀（假設密度為常數）。當物體密度均勻時，兩者重合。
- **[[Pappus Theorem|帕普斯定理 (Pappus Theorem)]]**: 利用形心位置與旋轉路徑計算旋轉體的表面積或體積。
- **[[Moment of inertia|轉動慣量]]**: 描述物體繞軸旋轉的難易程度，與質心位置及質量分布密切相關。

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