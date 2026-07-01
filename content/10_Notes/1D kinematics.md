---
tags:
  - Physics
up:
related:
aliases:
  - 一維運動
---

# Summary
一維運動學(1D kinematics)
研究如何描述物體的運動,而不探討運動發生的原因

## 基本概念
- **參考系(Reference Frame)**
  - 描述運動所需的人為座標系統
  - 例如,車站與行駛中的火車為不同參考系
- **位置(Position, x)**
  - 物體相對於參考系原點的所在之處
- **路徑長(Distance)**
  - 物體運動軌跡的總長度,是純量
- **位移(Displacement, Δx)**
  - 位置的變化量, $\Delta x = x_f - x_i$
  - 是向量,具有方向性
- **平均速率(Average Speed)**
  - 總路徑長 / 總時間, 是純量
- **平均速度(Average Velocity, $\bar{v}$)**
  - $\bar{v} = \frac{\Delta x}{\Delta t} = \frac{x_f - x_i}{t_f - t_i}$
  - 是向量,方向與位移相同
- **瞬時速度(Instantaneous Velocity, v)**
  - $v = \lim_{\Delta t \to 0} \frac{\Delta x}{\Delta t} = \frac{dx}{dt}$
  - 速度是位置對時間的一次微分
- **平均加速度(Average Acceleration, $\bar{a}$)**
  - $\bar{a} = \frac{\Delta v}{\Delta t} = \frac{v_f - v_i}{t_f - t_i}$
- **瞬時加速度(Instantaneous Acceleration, a)**
  - $a = \lim_{\Delta t \to 0} \frac{\Delta v}{\Delta t} = \frac{dv}{dt} = \frac{d^2x}{dt^2}$
  - 加速度是速度對時間的一次微分

## 圖形分析 (Graphical Analysis)
- **位置-時間圖 (x-t graph)**
  - 斜率代表瞬時速度 ($v = \frac{dx}{dt}$)
  - 割線斜率則為平均速度
- **速度-時間圖 (v-t graph)**
  - 斜率代表瞬時加速度 ($a = \frac{dv}{dt}$)
  - 曲線下的面積代表位移 ($\Delta x = \int v(t) dt$)
- **加速度-時間圖 (a-t graph)**
  - 曲線下的面積代表速度變化量 ($\Delta v = \int a(t) dt$)

# 等加速度直線運動 (Constant Acceleration Motion)
假設物體在直線上以固定加速度 `a` 運動
- 初始條件 (Initial conditions):
  - $t_0 = 0$
  - 初始位置 $x_0$
  - 初始速度 $v_0$

## 運動學三大公式推導
1.  **V(t)推導**
    > $a = \frac{dv}{dt} \implies dv = a dt$
    $$ \int_{v_0}^{v(t)} dv = \int_{0}^{t} a dt $$
    $$ v(t) - v_0 = at $$
    $$ v(t) = v_0 + at $$

2.  **x(t)推導**
    > $v = \frac{dx}{dt} \implies dx = v dt$
    $$ \int_{x_0}^{x(t)} dx = \int_{0}^{t} v(t) dt = \int_{0}^{t} (v_0 + at) dt $$
    $$ x(t) - x_0 = [v_0t + \frac{1}{2}at^2]_0^t $$
    $$ x(t) = x_0 + v_0t + \frac{1}{2}at^2 $$

3.  **v²-v₀² 推導 (不含時間t)**
    > 使用連鎖律: $a = \frac{dv}{dt} = \frac{dv}{dx} \frac{dx}{dt} = v \frac{dv}{dx}$
    $$ a dx = v dv $$
    $$ \int_{x_0}^{x} a dx = \int_{v_0}^{v} v dv $$
    $$ a(x - x_0) = \frac{1}{2}(v^2 - v_0^2) $$
    $$ v^2 = v_0^2 + 2a(x - x_0) $$

# 自由落體 (Free Fall)
自由落體是等加速度運動的特例,加速度為重力加速度 `g`
- 環境假設:
  - 物體在地表附近下落
  - 忽略空氣阻力 (air resistance)
  - 因此,物體的加速度與其形狀,大小,質量無關
  - $g \approx 9.8 \, m/s^2$ (方向通常取向下為負)

- **自由落體公式** (設向上為正, $a = -g$):
  1. $v(t) = v_0 - gt$
  2. $y(t) = y_0 + v_0t - \frac{1}{2}gt^2$
  3. $v^2 = v_0^2 - 2g(y - y_0)$

---
*Footnotes:*
[^1]: Air drag force is proportional to velocity, avoiding terminal velocity considerations.
