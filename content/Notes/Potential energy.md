---
tags:
  - Physics
up:
related:
  - "[[kinetic energy]]"
annotation:
aliases:
  - 位能
  - Gravitational force
  - P.E.
---
# 概要
位能 (Potential Energy) 是物體因其在力場中的位置或組態而儲存的能量。
它與保守力相關聯，且其數值取決於所選的參考點。

# 理論
- **定義**
位能是物體因其相對於其他物體的位置或其內部組態而儲存的能量。只有當作用力是[[Conservative force|保守力]]時，才能定義位能。
- **參考點**
位能的絕對值沒有物理意義，只有位能的變化量才具有物理意義。
因此，在計算位能時，需要選擇一個參考點（或零位面），在此參考點處位能被定義為零。
- **重力位能 (Gravitational Potential Energy)**:
    - **一般情況 (General Case)**: 適用於萬有引力，通常將無窮遠處的位能定義為零。
    - **近地表 (Near Earth Surface)**: 在地球表面附近，重力可視為定力，位能與高度成正比。
- **彈性位能 (Elastic Potential Energy)**: 儲存在被壓縮或拉伸的彈性物體（如彈簧）中的能量。
- **電位能 (Electric Potential Energy)**: 儲存在電荷系統中的能量，由於電荷間的靜電力作用。
- **藍納-瓊斯位能 (Lennard-Jones Potential)**: 一種用於描述中性原子或分子間交互作用的經驗模型，包含短距離排斥和長距離吸引。

# 公式
- **重力位能 (General Case)**:
    $$ U_{g}=- \frac{GMm}{r} $$
    - $G$: 萬有引力常數
    - $M, m$: 兩個物體的質量
    - $r$: 兩物體間的距離
    - 參考點: $U_{g}(r \to \infty) \equiv 0$
- **重力位能 (Near Earth Surface)**:
    $$ U_{g}=mgy $$
    - $m$: 物體質量
    - $g$: 重力加速度
    - $y$: 物體相對於參考零位面的高度
    - 參考點: $U_{g}(y=0) \equiv 0$ (通常選擇地面)
- **彈性位能 (Elastic Potential Energy)**:
    $$ U_{s}(x)=\frac{1}{2}kx^{2} $$
    - $k$: 彈簧常數
    - $x$: 彈簧的形變量（壓縮或拉伸的長度）
    - 參考點: $U_{s}(x=0) \equiv 0$ (彈簧處於自然長度時)
- **電位能 (Electric Potential Energy)**:
    $$ U_e = k \frac{q_1 q_2}{r} $$
    - $k$: 庫倫常數
    - $q_1, q_2$: 兩個點電荷的電量
    - $r$: 兩電荷間的距離
    - 參考點: 無窮遠處的位能定義為零
- **藍納-瓊斯位能 (Lennard-Jones Potential)**:
    $$ U(r) = 4\epsilon \left[ \left( \frac{\sigma}{r} \right)^{12} - \left( \frac{\sigma}{r} \right)^{6} \right] $$
    - $r$: 兩粒子間的距離
    - $\epsilon$: 位能井的深度
    - $\sigma$: 位能為零時的粒子間距
    - **排斥項**: $\left( \frac{\sigma}{r} \right)^{12}$ (短距離鮑利斥力)
    - **吸引項**: $-\left( \frac{\sigma}{r} \right)^{6}$ (長距離凡德瓦力)
