---
aliases:
  - 駐波
tags:
  - Physics
up:
  - "[[波的疊加原理]]"
related:
  - "[[Wave]]"
  - "[[Simple Harmonic Motion]]"
---

# 概要

**駐波 (Standing Wave)** 是一種波形不向前傳播的波，由兩列振幅、波長、頻率皆相同但行進方向相反的波疊加而成。駐波中的能量被局限在特定區域內振盪，而不像行進波那樣將能量從一處傳播到另一處。

# 核心概念

- **節點 (Node)**: 駐波上振幅恆為零的點。在這些點，兩列波總是產生完全的破壞性干涉。相鄰節點之間的距離為半個波長 ($\lambda/2$)。
- **腹點 (Antinode)**: 駐波上振幅達到最大值（$2A$）的點。在這些點，兩列波總是產生完全的建設性干涉。相鄰腹點之間的距離也是半個波長 ($\lambda/2$)。

# 結構/要素

駐波的數學形式可以從兩列反向行進的正弦波疊加得到：
$$ y_{total} = y_1 + y_2 = A\sin(kx - \omega t) + A\sin(kx + \omega t) $$
使用和差化積公式，可得駐波方程式：
$$ y_{total}(x, t) = [2A\sin(kx)] \cos(\omega t) $$
- **振幅項**: $[2A\sin(kx)]$，是一個只與位置 $x$ 有關的振幅函數。
- **振盪項**: $\cos(\omega t)$，表示所有非節點的粒子都以相同的頻率和相位（或反相）進行[[Simple Harmonic Motion|簡諧運動]]。

# 原理/推導: 共振頻率與波長

駐波的形成與邊界條件密切相關。只有當系統的長度 L 能夠容納特定波長的波時，才能形成穩定的駐波，這種現象稱為**共振 (Resonance)**。

### 1. 兩端固定的弦 (String Fixed at Both Ends)
- **邊界條件**: 弦的兩端 ($x=0$ 和 $x=L$) 必須是**節點**。
  $$ y(0, t) = 0 \quad \text{and} \quad y(L, t) = 0 $$
- **推導**:
  - $y(0,t) = [2A\sin(k \cdot 0)]\cos(\omega t) = 0$，此條件自動滿足。
  - $y(L,t) = [2A\sin(kL)]\cos(\omega t) = 0$，此要求 $\sin(kL) = 0$。
  - 因此，$kL$ 必須是 $\pi$ 的整數倍：$k_n L = n\pi$，其中 $n = 1, 2, 3, ...$
- **結果**:
  - **允許的波長**: $\lambda_n = \frac{2\pi}{k_n} = \frac{2L}{n}$
  - **允許的頻率 (Harmonics)**: $f_n = \frac{v}{\lambda_n} = n \left(\frac{v}{2L}\right) = n f_1$
    - **基頻 (Fundamental Frequency, n=1)**: $f_1 = v/2L$
    - **泛音 (Overtones)**: $f_2, f_3, ...$ (等於 2, 3, ... 倍的基頻)

### 2. 兩端開放的氣柱 (Air Column Open at Both Ends)
- **邊界條件**: 開放端空氣可自由移動，壓力恆等於大氣壓力，因此兩端 ($x=0$ 和 $x=L$) 都是**腹點 (Antinode)**。
- **推導**: 這等效於要求位移在兩端為最大值，其數學條件與兩端固定的弦完全相同。
- **結果**:
  - **允許的波長**: $\lambda_n = \frac{2L}{n}$
  - **允許的頻率**: $f_n = n \left(\frac{v}{2L}\right) \quad (n = 1, 2, 3, ...)$

### 3. 一端封閉的氣柱 (Air Column Closed at One End)
- **邊界條件**: 封閉端 ($x=0$) 空氣無法移動，是**節點**。開放端 ($x=L$) 是**腹點**。
  $$ y(0, t) = 0 \quad \text{and} \quad y(L, t) \text{ is an antinode} $$
- **推導**:
  - $y(0,t)$ 為節點，要求駐波形式為 $y(x,t) = [2A\sin(kx)]\cos(\omega t)$。
  - $y(L,t)$ 為腹點，要求 $|\sin(kL)|=1$。
  - 因此，$kL$ 必須是 $\pi/2$ 的奇數倍：$k_n L = (n + \frac{1}{2})\pi = \frac{(2n+1)\pi}{2}$。更常用的形式是 $k_n L = m\frac{\pi}{2}$，其中 $m$ 為奇數。
    $$ k_n L = m \frac{\pi}{2}, \quad m = 1, 3, 5, ... $$
- **結果**:
  - **允許的波長**: $\lambda_m = \frac{2\pi}{k_m} = \frac{4L}{m}$
  - **允許的頻率**: $f_m = \frac{v}{\lambda_m} = m \left(\frac{v}{4L}\right) = m f_1$
    - **基頻 (m=1)**: $f_1 = v/4L$
    - **泛音**: 只存在**奇數倍**的泛音 ($f_3, f_5, ...$)。