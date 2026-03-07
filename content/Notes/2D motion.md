---
tags:
  - Physics
up:
related:
  - "[[有阻力之自由落體速度推導]]"
  - "[[拋射體運動實驗報告]]"
anntation:
aliases:
---
# Projectile
** 拋體運動**
- 若為長地表拋射，g為非垂直$\to$誤差

## X-axis(軸)
$v_{x}=v\cos \theta$，constant
$a_{x}=0$
$x=v\cos \theta \cdot t$
## Y-axis
$$\displaylines{
v_{y_{0}}=v\sin \theta
\a_{y}=-g
\y=v\sin \theta \cdot t-\frac{1}{2}gt^{2}
\v_{y}=v\sin \theta-gt
}$$
## summary
1. max height$$\displaylines{
y_{max}=\frac{v^{2}\sin^{2}\theta}{2g}}
$$ 
2. time of flight
$$ 
t=\frac{2v\sin \theta}{g}
$$ 
3. traveling distance
$$ 
 R=\frac{v^{2}\sin 2\theta}{g}
$$ 

---
# 2D 運動公式推導摘要

此摘要提供二維運動中關鍵公式的簡易推導，以鞏固核心觀念。所有推導均基於基礎的微積分及向量概念。

這些二維向量的分析，皆是建立在以 [[Units#Unit Vector|單位向量]] 標示方向的基礎之上。

## 拋體運動 (Projectile Motion) 推導

從已知的運動方程式出發，可推導軌跡、飛行時間、最大高度與射程。

**初始條件:**
- 初始速度: $\vec{v}_0 = (v_0\cos\theta)\hat{i} + (v_0\sin\theta)\hat{j}$
- 加速度: $\vec{a} = -g\hat{j}$
- 初始位置: $\vec{r}_0 = 0$ (從原點發射)

**運動方程式:**
- $x(t) = (v_0\cos\theta)t$
- $y(t) = (v_0\sin\theta)t - \frac{1}{2}gt^2$

### 1. 軌跡方程式 (Trajectory Equation)
此方程式描述 y 隨 x 變化的路徑，與時間 t 無關。
1.  從 x 方向的運動方程式解出 t：
    $$ t = \frac{x}{v_0\cos\theta} $$
2.  將 t 代入 y 方向的運動方程式：
    $$ y(x) = (v_0\sin\theta)\left(\frac{x}{v_0\cos\theta}\right) - \frac{1}{2}g\left(\frac{x}{v_0\cos\theta}\right)^2 $$
3.  化簡後可得拋物線方程式：
    $$ y(x) = (\tan\theta)x - \left(\frac{g}{2v_0^2\cos^2\theta}\right)x^2 $$

### 2. 飛行時間 (Time of Flight)
飛行時間是物體從發射到返回初始高度 (y=0) 所需的時間。
1.  令 $y(t) = 0$：
    $$ (v_0\sin\theta)t - \frac{1}{2}gt^2 = 0 $$
2.  提出 t：
    $$ t\left(v_0\sin\theta - \frac{1}{2}gt\right) = 0 $$
3.  此方程式有兩個解：$t=0$ (發射瞬間) 和 $v_0\sin\theta - \frac{1}{2}gt = 0$。取後者：
    $$ t_{flight} = \frac{2v_0\sin\theta}{g} $$

### 3. 最大高度 (Max Height)
在最高點時，y 方向的瞬時速度 $v_y$ 為 0。
1.  從 $v_y(t) = v_0\sin\theta - gt$ 出發，令 $v_y = 0$：
    $$ 0 = v_0\sin\theta - gt_{peak} \implies t_{peak} = \frac{v_0\sin\theta}{g} $$
    (即上升到最高點的時間是總飛行時間的一半)
2.  將 $t_{peak}$ 代入 y(t) 方程式：
    $$ y_{max} = (v_0\sin\theta)\left(\frac{v_0\sin\theta}{g}\right) - \frac{1}{2}g\left(\frac{v_0\sin\theta}{g}\right)^2 $$
3.  化簡可得：
    $$ y_{max} = \frac{v_0^2\sin^2\theta}{g} - \frac{1}{2}\frac{v_0^2\sin^2\theta}{g} = \frac{v_0^2\sin^2\theta}{2g} $$

### 4. 水平射程 (Traveling Distance)
將總飛行時間 $t_{flight}$ 代入 x 方向的運動方程式。
1.  $R = x(t_{flight}) = (v_0\cos\theta) \cdot t_{flight}$
2.  代入 $t_{flight}$：
    $$ R = (v_0\cos\theta)\left(\frac{2v_0\sin\theta}{g}\right) = \frac{v_0^2(2\sin\theta\cos\theta)}{g} $$
3.  使用三角函數的倍角公式 $2\sin\theta\cos\theta = \sin(2\theta)$：
    $$ R = \frac{v_0^2\sin(2\theta)}{g} $$
