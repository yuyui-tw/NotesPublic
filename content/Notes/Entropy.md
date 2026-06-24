---
aliases:
  - Entropy
  - 熵
  - 熵變
  - 熱力學第三定律
  - Third Law of Thermodynamics
tags:
  - Physics
  - Chemistry
up:
  - "[[熱力學第二定律]]"
related:
  - "[[狀態函數]]"
  - "[[卡諾熱機]]"
  - "[[熱容量]]"
  - "[[理想氣體方程式]]"
annotation: 介紹熵的熱力學定義、熱力學第三定律、絕對零度，推導理想氣體及一般物質的熵變計算公式，並以 T-S 圖分析卡諾循環。
---

# 1. 導論 (Introduction & Background)

**熵 (Entropy, $S$)** 是一個用來量度系統無序程度或能量退化程度的**[[狀態函數]]**。該物理量由魯道夫·克勞修斯 (Rudolf Clausius) 於 1865 年首次提出，用以定量描述**[[熱力學第二定律]]**中的不可逆性。

在宏觀熱力學中，熵的定義是基於可逆過程的熱量與溫度的比值。而在微觀統計力學中，熵則被定義為系統微觀狀態數的對數度量。熵的計算能夠預測自發過程的方向以及系統對外作功的最大能力限制。

# 2. 核心 (Core Framework)

### 熵的熱力學定義
對於一個經歷無限小變化的過程，系統熵的變量 $dS$ 定義為：
$$ dS = \frac{dq_{\text{rev}}}{T} $$
- $dq_{\text{rev}}$ 是系統在**可逆過程 (Reversible Process)** 中吸收的微小熱量。
- $T$ 是發生熱交換時的絕對溫度。
- 若要計算系統從狀態 $A$ 變到狀態 $B$ 的熵變 $\Delta S$，必須在 $A$ 與 $B$ 之間人為選擇一條可逆路徑進行積分：
  $$ \Delta S = S_B - S_A = \int_{A}^{B} \frac{dq_{\text{rev}}}{T} $$

### 熱力學第三定律 (Third Law of Thermodynamics)
- **表述**：當絕對溫度趨近於絕對零度 ($0 \text{ K}$) 時，純物質完美晶體的熵值趨近於零：
  $$ \lim_{T \to 0} S = 0 $$
- **絕對零度 (Absolute Zero)**：即 $0 \text{ K}$ ($-273.15^\circ\text{C}$)，是物質分子熱運動動能達到最低的極限狀態。根據此定律，可以定義物質在特定溫度下的**絕對熵 (Absolute Entropy)**。

# 3. 邏輯 (Operational Logic)

### 常用系統的熵變計算
1. **理想氣體 (Ideal Gas) 的熵變**：
   - 根據**[[熱力學第一定律]]**，$dq = dU - dw = n C_v dT + P dV$。
   - 除以 $T$，並代入**[[理想氣體方程式]]** $P = nRT/V$：
     $$ dS = \frac{dq_{\text{rev}}}{T} = n C_v \frac{dT}{T} + n R \frac{dV}{V} $$
   - 積分後得到理想氣體熵變公式：
     $$ \Delta S = n C_v \ln\left(\frac{T_f}{T_i}\right) + n R \ln\left(\frac{V_f}{V_i}\right) $$
   - 若以壓力 $P$ 表示，可推導為（利用 $C_p = C_v + R$）：
     $$ \Delta S = n C_p \ln\left(\frac{T_f}{T_i}\right) - n R \ln\left(\frac{P_f}{P_i}\right) $$

2. **一般物質的等壓變溫過程**：
   - 在無相變且恆壓（例如 $\Delta P = 0$）的條件下，微小熱量為 $dq_{\text{rev}} = n C_p dT$（參見**[[熱容量]]**）。
   - 熵變計算式：
     $$ \Delta S = \int_{T_i}^{T_f} \frac{n C_p}{T} \,dT $$
   - 若 $C_p$ 在該溫區內為常數，則：$\Delta S = n C_p \ln\left(\frac{T_f}{T_i}\right)$。

3. **一般物質的相變過程 (Phase Transition)**：
   - 相變發生於恆溫恆壓下，其吸收或釋放的熱量即為相變焓 $\Delta H_{\text{phase}}$（如熔化熱、汽化熱）。
   - 熵變公式：
     $$ \Delta S_{\text{phase}} = \frac{\Delta H_{\text{phase}}}{T_{\text{phase}}} $$

### 卡諾循環的溫-熵圖 (T-S Diagram)

![[T-S Diagram of Carnot Cycle.png]]

在溫-熵圖上，卡諾循環的軌跡為一矩形，能直觀地展示熱與功的關係：
- **等溫膨脹 ($T_H$)**：水平線向右，$S$ 增加，吸熱 $Q_H = T_H (S_2 - S_1)$。
- **絕熱膨脹**：垂直線向下，$S$ 不變（等熵過程，Isentropic Process），溫度降至 $T_C$。
- **等溫壓縮 ($T_C$)**：水平線向左，$S$ 減少，放熱 $Q_C = T_C (S_2 - S_1)$。
- **絕熱壓縮**：垂直線向上，$S$ 不變，溫度升回 $T_H$。
- 矩形所包圍的面積即為熱機所做的淨功：$W_{\text{net}} = (T_H - T_C)(S_2 - S_1)$。

# 4. 應用與脈絡 (Application & Context)

### 孤立系統的自發不可逆過程
- **不可逆過程與熵增**：對於孤立系統，任何實際的自發過程皆為不可逆過程，必然導致系統總熵增加。例如：
  - **熱傳導**：熱量從 $T_H$ 傳導至 $T_C$，其熵變 $\Delta S = -\frac{Q}{T_H} + \frac{Q}{T_C} = Q\left(\frac{1}{T_C} - \frac{1}{T_H}\right) > 0$。
  - **氣體自由膨脹**：不作功也不交換熱量，但氣體體積增大，微觀狀態數增加，故 $\Delta S > 0$。
- **熵的系統思維**：熵可視為能量退化的測度。能量的總量不變（第一定律），但有用的能量（做功能力）在每一次自發過程中都無可挽回地耗散。
- **相關連結**：
  - 了解不同狀態量之區分，參見 **[[狀態函數]]**。
  - 了解卡諾循環對熱機效率的物理極限，參見 **[[卡諾熱機]]**。
  - 熱量傳遞的自發方向限制，參見 **[[熱力學第二定律]]**。