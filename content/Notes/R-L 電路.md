---
aliases:
  - RL Circuit
  - RL 電路
tags:
  - Physics
up:
  - "[[電感器]]"
related:
  - "[[克希荷夫法則]]"
  - "[[RC電路分析]]"
  - "[[磁場]]"
annotation: 探討電阻與電感串聯之電路動態行為，包含充電與放電方程式之推導、時間常數之定義以及磁能之儲存。
---

# 1. 導論 (Introduction & Background)

**R-L 電路 (RL Circuit)** 是由 **電阻器 (Resistor)** 與 **電感器 (Inductor)** 串聯而成的基本電路。在直流電路中，由於電感器具有「自感現象」，當電路接通或切斷時，電流不會瞬間達到峰值或歸零，而是呈現指數型的過渡過程。

研究 R-L 電路的動態行為對於理解磁能儲存、電流緩衝以及過渡響應具有重要意義，是電子濾波器與電力保護裝置的物理基礎。
![[RL Circuit.png]]
# 2. 核心 (Core Framework)

### 2.1 充電過程 (Charging/Energizing)
![[RL Circuit 充電圖.png]]
當電路接通電動勢 $\mathcal{E}$ 時，電流 $i(t)$ 隨時間變化的方程式為：
$$i(t) = \frac{\mathcal{E}}{R} \left( 1 - e^{-t/\tau} \right)$$
- **初始狀態 ($t=0$)**：$i=0$，電感產生最大反電動勢 $\varepsilon_L = \mathcal{E}$。
- **穩定狀態 ($t \to \infty$)**：$i = \mathcal{E}/R$，電感視為短路（理想導線，==若有電阻並聯要注意電流走向==）。

### 2.2 放電過程 (Discharging/De-energizing)
當移除電源並將電感與電阻閉合時，儲存於電感中的磁能釋放：
$$i(t) = I_0 e^{-t/\tau}$$
其中 $I_0$ 為初始穩定電流。

### 2.3 時間常數 (Time Constant)
==對突發變化作出反應速度的特徵參數==。代表系統狀態（如電壓、電流或溫度）按指數規律衰減或增長至特定比例所需的時間，數值越小代表系統反應越快。
定義 **時間常數 (Time Constant)** $\tau$ 為：
$$\tau = \frac{L}{R}$$
- 當 $t = \tau$ 時，充電電流達到最大值的 $63.2\%$；放電電流下降至初始值的 $36.8\%$。

### 2.4 電感中的儲能 (Energy Storage)
電感器儲存的磁能 $U_L$ 為：
$$U_L = \frac{1}{2} L I^2$$

# 3. 邏輯 (Operational Logic)

### 3.1 充電方程式推導
根據 [[克希荷夫法則#克希荷夫迴路法則 (Kirchhoff's Voltage Law, KVL)]]，迴路總電壓為零：
$$\mathcal{E} - iR - L \frac{di}{dt} = 0$$
整理成一階線性微分方程：
$$L \frac{di}{dt} = \mathcal{E} - iR \implies \int_0^i \frac{di}{\mathcal{E} - iR} = \int_0^t \frac{1}{L} dt$$
積分後可得：
$$-\frac{1}{R} \ln\left( \frac{\mathcal{E} - iR}{\mathcal{E}} \right) = \frac{t}{L} \implies i(t) = \frac{\mathcal{E}}{R} \left( 1 - e^{-\frac{R}{L}t} \right)$$

### 3.2 能量守恆分析
將 KVL 方程式 $\mathcal{E} = iR + L \frac{di}{dt}$ 同乘以電流 $i$：
$$\mathcal{E}i = i^2R + Li \frac{di}{dt}$$
- $\mathcal{E}i$：電源提供的總功率。
- $i^2R$：電阻器消耗的熱能功率。
- $Li \frac{di}{dt} = \frac{d}{dt} \left( \frac{1}{2}LI^2 \right)$：電感磁場能量的增加率。
這表明電源提供的能量，一部分轉化為熱能，另一部分以磁能形式儲存於電感中。

### 3.3 磁能密度 (Magnetic Energy Density)
以長度 $l$、截面積 $A$、匝數 $N$ 的理想螺線管為例：
$$U_L = \frac{1}{2} L I^2 = \frac{1}{2} \left( \frac{\mu_0 N^2 A}{l} \right) \left( \frac{Bl}{\mu_0 N} \right)^2 = \frac{B^2}{2\mu_0} (Al)$$
定義 **磁能密度 (Magnetic Energy Density)** $u_B$（每單位體積之磁能）：
$$u_B = \frac{B^2}{2\mu_0}$$
此公式可推廣至任何形式之磁場。

# 4. 應用與脈絡 (Application & Context)

- **電流緩衝**：利用電感反抗電流突變的特性，防止電路開關瞬間產生過大電流損壞元件。
- **過電壓保護**：切斷電感電路時產生的自感電動勢可能極大，需配合二極體（飛輪二極體）路徑釋放能量。
- **相關連結**：
    - [[電感器]]：理解 $L$ 的物理定義與構造。
    - [[RC電路分析]]：對比電容與電感的對偶特性（電容儲能於電場，電感儲能於磁場）。
    - [[磁場]]：磁能密度公式中的底層場論背景。
