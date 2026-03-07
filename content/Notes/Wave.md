---
aliases:
  - Wave
  - 波
tags:
  - Physics
up:
  - "[[periodic motion]]"
related:
  - "[[Simple Harmonic Motion]]"
  - "[[機械波]]"
  - "[[波的疊加原理]]"
---

# 概要

**波 (Wave)** 是一種在空間中傳播**能量**與**動量**的**擾動 (Disturbance)**。它在空間中前進，但組成介質的粒子通常僅在平衡位置附近振盪，不隨波進行長距離遷移。波是理解從[[機械波]]到電磁波等廣泛物理現象的核心。

# 核心概念

### 1. 波的分類
- **根據介質需求**:
    1.  **[[機械波]] (Mechanical Wave)**: 必須依賴介質傳播。
    2.  **電磁波 (Electromagnetic Wave)**: 不需介質，可在真空中傳播。
- **根據振盪方向**:
    1.  **橫波 (Transverse Wave)**: 質點振盪方向與波的傳播方向**垂直** (e.g., 繩波, 光)。
    2.  **縱波 (Longitudinal Wave)**: 質點振盪方向與波的傳播方向**平行** (e.g., 聲波)。

### 2. 描述波的物理量
- **振幅 (Amplitude, A)**: 質點偏離平衡位置的最大位移。
- **波長 (Wavelength, $\lambda$)**: 波形上兩個連續同相點之間的距離。
- **週期 (Period, T)**: 介質質點完成一次完整振盪的時間。
- **頻率 (Frequency, f)**: $f = 1/T$。
- **波速 (Wave Speed, v)**: $v = f\lambda$，由介質性質決定。
- **角頻率 (Angular Frequency, $\omega$)**: $\omega = 2\pi f$。
- **波數 (Wave Number, k)**: $k = 2\pi/\lambda$。

---

# 結構/要素: 關鍵現象

波的行為引發了多種重要物理現象：
- **[[波的疊加原理|疊加與干涉 (Superposition & Interference)]]**: 多個波相遇時，其位移向量和，產生建設性或破壞性干涉。
- **[[Standing Wave|駐波 (Standing Waves)]]**: 兩列反向行進的相同波疊加後，產生波形不前進的共振現象。
- **反射 (Reflection)**: 波在介質邊界返回。固定端反射有 180° 相位反轉，自由端則無。
- **繞射 (Diffraction)**: 波繞過障礙物或通過孔隙時的擴散現象。
- **都卜勒效應 (Doppler Effect)**: 波源與觀察者相對運動導致的頻率變化。

---

# 原理/推導: 基礎方程式

### 1. 波動方程式 (Wave Equation)
描述波在時空中的行為的基礎是一個二階偏微分方程。其一維形式為：
$$ \frac{\partial^2 y}{\partial t^2} = v^2 \frac{\partial^2 y}{\partial x^2} $$
- **波速 $v$**: 完全由介質的物理性質決定。例如，對於弦波，$v = \sqrt{T/\mu}$。其詳細推導見[[機械波]]。

### 2. 波函數 (Wave Function)
波動方程式的通解為 $y(x,t) = f(x \mp vt)$。一個重要的特解是正弦波：
$$ y(x, t) = A\sin(kx - \omega t + \phi) $$
考察固定位置 ($x=x_0$) 的質點，其運動 $y(t)$ 是一種[[Simple Harmonic Motion|簡諧運動]]，證明了波與簡諧運動的深刻聯繫。
