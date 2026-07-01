---
aliases:
  - 衝量
tags:
  - Physics
up:
  - "[[MOMENTUM, IMPULSE, AND COLLISIONS]]"
related:
  - "[[Momentum]]"
annotation:
---
# 概要
衝量 (Impulse) 是一個描述**力**在**時間**上累積效應的物理量。當一個力作用在物體上一段時間，它便對物體施加了一個衝量。

衝量的核心價值在於它與動量之間的直接關係，即**衝量-動量定理**。
這個定理表明，施加於物體的淨衝量，等於該物體動量的變化量。這在分析碰撞、打擊等瞬時作用力問題時特別有用。

# 理論
### 衝量-動量定理 (Impulse-Momentum Theorem)
此定理可以直接從牛頓第二定律的動量形式推導出來。
1.  從牛頓第二定律出發：
    $$ \vec{F} = \frac{d\vec{p}}{dt} $$
2.  將 $dt$ 移項，得到動量的微小變化 $d\vec{p}$：
    $$ d\vec{p} = \vec{F} dt $$
3.  將等號兩邊從初始時間 $t_i$ 到末了時間 $t_f$ 進行積分：
    $$ \int_{\vec{p}_i}^{\vec{p}_f} d\vec{p} = \int_{t_i}^{t_f} \vec{F}(t) dt $$
4.  左邊的積分結果是動量的總變化 $\Delta\vec{p}$，而右邊的積分就是衝量 $\vec{J}$ 的定義：
    $$ \Delta\vec{p} = \vec{J} $$

### 平均力 (Average Force)
在很多碰撞問題中，作用力 $\vec{F}(t)$ 的函數形式非常複雜且短暫，難以測量。但我們可以透過測量動量的總變化（即總衝量）來計算一個等效的**平均力** $\vec{F}_{avg}$。
$$ \vec{F}_{avg} = \frac{\vec{J}}{\Delta t} = \frac{\Delta\vec{p}}{\Delta t} $$
平均力的物理意義是：在相同的時間間隔 $\Delta t$ 內，一個恆定的力 $\vec{F}_{avg}$ 所產生的衝量，與變動力 $\vec{F}(t)$ 所產生的總衝量相同。

# 公式
### 衝量 (Impulse)
$$ \vec{J} = \int_{t_i}^{t_f} \vec{F}(t) dt $$
- $\vec{J}$: 衝量 (N·s 或 kg·m/s)
- $\vec{F}(t)$: 隨時間變化的力 (N)

### 衝量-動量定理
$$ \vec{J} = \Delta\vec{p} = \vec{p}_f - \vec{p}_i $$

### 平均力
$$ \vec{F}_{avg} = \frac{\vec{J}}{\Delta t} $$

