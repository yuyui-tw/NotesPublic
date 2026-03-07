---
tags:
  - Chemistry
  - Physics
up:
  - "[[理想氣體方程式]]"
related:
  - "[[理想氣體方程式]]"
annotation:
aliases:
  - Kinetic Molecular Theory
  - KMT
  - 氣體動力論
---
# 概要
氣體動力論 (The Kinetic Molecular Theory of Gases, KMT) 是一個理論模型，旨在從微觀層面解釋氣體的宏觀行為（如壓力、溫度、體積）。它將氣體視為由大量處於持續、隨機運動中的粒子所組成，並為理想氣體方程式等氣體定律提供了理論基礎。

# 理論

## 氣體動力論的五個基本假設 (Postulates)
此理論建立在以下五個基本假設之上：

1.  **粒子性與隨機運動 (Particles and Random Motion)**
    氣體由大量微小粒子（原子或分子）組成，這些粒子處於永不停止的、快速的、隨機的直線運動中。

2.  **粒子體積可忽略 (Negligible Particle Volume)**
    與氣體佔據的容器體積相比，氣體粒子本身的體積小到可以忽略不計。

3.  **無分子間作用力 (No Intermolecular Forces)**
    氣體粒子之間不存在相互吸引或排斥的作用力。它們僅在碰撞時才會相互影響。

4.  **彈性碰撞 (Elastic Collisions)**
    氣體粒子之間以及粒子與容器壁之間的碰撞均為 **完全彈性碰撞**。在碰撞過程中，動能可以在粒子間轉移，但系統的總動能（在溫度恆定時）保持不變。

5.  **動能與溫度的關係 (Kinetic Energy and Temperature)**
    氣體粒子的 **平均動能 (average kinetic energy)** 與氣體的 **絕對溫度 (absolute temperature, K)** 成正比。這是連結微觀運動與宏觀溫度的核心假設。

## KMT 如何解釋氣體行為
- **壓力 (Pressure)**: 壓力源於大量氣體粒子對容器壁的持續碰撞所產生的累積作用力。
- **溫度 (Temperature)**: 溫度是衡量氣體粒子平均動能的宏觀指標。溫度越高，粒子的平均運動速率越快。
- **波以耳定律 ($V \propto 1/P$)**: 體積減小時，粒子碰撞容器壁的頻率增加，從而導致壓力升高。
- **查理定律 ($V \propto T$)**: 溫度升高時，粒子平均動能和速率增加。為維持壓力不變（即碰撞頻率和強度不變），氣體體積必須膨脹。

## 分子速率分佈 (Distribution of Molecular Speeds)
在特定溫度下，氣體中的所有粒子並非以相同速率運動。它們的速率分佈遵循 **麥克斯韋-波茲曼分佈 (Maxwell-Boltzmann distribution)**。

- **方均根速率 ($u_{rms}$)**: 與氣體總動能直接相關的速率統計量。
- **平均速率 ($ar{u}$)**: 所有粒子速率的算術平均值。
- **最可幾速率 ($u_{mp}$)**: 分佈曲線峰值對應的速率，即擁有該速率的粒子數最多。

## 方均根速率的推導 (Derivation of $u_{rms}$)
方均根速率的公式可以通過結合 KMT 的微觀壓力模型與宏觀的理想氣體方程式來推導。

1.  **從微觀壓力出發**: 考慮一個邊長為 $L$ 的立方體容器，內有 $N$ 個質量均為 $m$ 的氣體粒子。壓力 $P$ 來自粒子對容器壁的碰撞力 $F$ 除以壁面積 $A$。
    $$ P = \frac{F}{A} $$

2.  **單一粒子的貢獻**: 考慮一個粒子沿 x 軸方向的運動，其速度分量為 $u_x$。它與一側牆壁碰撞後，動量變化為 $\Delta p = m u_x - (-m u_x) = 2m u_x$。來回一次與同一牆壁碰撞所需時間為 $\Delta t = \frac{2L}{u_x}$。因此，該粒子對牆壁施加的平均力為：
    $$ F_x = \frac{\Delta p}{\Delta t} = \frac{2m u_x}{2L/u_x} = \frac{m u_x^2}{L} $$

3.  **總壓力的計算**: 所有 $N$ 個粒子的總作用力為 $F_{\text{total}} = \sum_{i=1}^{N} \frac{m u_{xi}^2}{L} = \frac{Nm\overline{u_x^2}}{L}$，其中 $\overline{u_x^2}$ 是 x 方向速度平方的平均值。壓力為：
    $$ P = \frac{F_{\text{total}}}{A} = \frac{Nm\overline{u_x^2}}{L \cdot L^2} = \frac{Nm\overline{u_x^2}}{V} $$
    ($V=L^3$ 是體積)

4.  **三維速度的關聯**: 粒子的運動是隨機的，因此在各方向上的平均速度平方相等：$\overline{u_x^2} = \overline{u_y^2} = \overline{u_z^2}$。總速度的平方平均值 $\overline{u^2} = \overline{u_x^2} + \overline{u_y^2} + \overline{u_z^2} = 3\overline{u_x^2}$。因此，$\overline{u_x^2} = \frac{1}{3}\overline{u^2}$。

5.  **KMT 的壓力方程式**: 將上式代入壓力表達式，得到 KMT 的核心成果之一：
    $$ P = \frac{Nm(\frac{1}{3}\overline{u^2})}{V} \implies PV = \frac{1}{3}Nm\overline{u^2} $$

6.  **結合理想氣體方程式**: 我們現在有兩個關於 $PV$ 的表達式：
    - KMT: $PV = \frac{1}{3}Nm\overline{u^2}$
    - 理想氣體定律: $PV = nRT$

7.  **推導 $u_{rms}$**: 令兩式相等：
    $$ \frac{1}{3}Nm\overline{u^2} = nRT $$
    我們知道粒子總數 $N = n N_A$ (莫耳數 $\times$ 亞佛加厥常數)，且莫耳質量 $M = m N_A$ (單一粒子質量 $\times$ 亞佛加厥常數)。代入上式：
    $$ \frac{1}{3}(nN_A)m\overline{u^2} = nRT \implies \frac{1}{3}n(mN_A)\overline{u^2} = nRT \implies \frac{1}{3}nM\overline{u^2} = nRT $$ 
    消去 $n$，整理可得：
    $$ \overline{u^2} = \frac{3RT}{M} $$ 
    方均根速率 $u_{rms}$ 定義為 $\sqrt{\overline{u^2}}$，因此：
    $$ u_{rms} = \sqrt{\frac{3RT}{M}} $$ 

# 公式

## 平均動能與溫度
對於 1 莫耳的氣體，其粒子的平均動能與絕對溫度 T 的關係為：
$$ \text{KE}_{\text{avg}} = \frac{3}{2}RT $$ 
- $\text{KE}_{\text{avg}}$: 平均動能 (J/mol)
- $R$: 氣體常數，此處必須使用 $8.314 \frac{J}{mol \cdot K}$
- $T$: 絕對溫度 (K)

## 方均根速率 (Root-Mean-Square Speed)
方均根速率是描述氣體粒子運動速率的重要物理量，其計算公式為：
$$ u_{rms} = \sqrt{\frac{3RT}{M}} $$ 
- $u_{rms}$: 方均根速率 (m/s)
- $R$: 氣體常數 ($8.314 \frac{J}{mol \cdot K}$)
- $T$: 絕對溫度 (K)
- $M$: **莫耳質量 (Molar Mass)**，此處單位必須為 **公斤/莫耳 (kg/mol)**
