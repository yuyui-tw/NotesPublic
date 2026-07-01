---
tags:
  - Physics
up:
  - "[[2D motion]]"
related:
aliases:
  - 衛星運動
annotation:
---
# 參數
1. r: 軌道半徑 (orbital radius) = $r_{E}+H\dots(m)$
2. v: 軌道速度 (orbital velocity)
3. T: 軌道週期 (orbital period)
4. M: 地球質量 (mass of Earth)
5. m: 衛星質量 (mass of satellite)
6. G: 萬有引力常數 $6.67\times 10^{-11}\dots\left( \frac{{N\cdot m^{2}}}{kg^{2}} \right)$
7. $r_E$: 地球半徑 (radius of Earth)

# 圓形軌道力學 (Circular Orbit Mechanics)
- 向心力由萬有引力提供
- Centripetal Force = Gravitational Force

$$ 
\frac{GMm}{r^{2}} = m \frac{v^{2}}{r} 
$$ 

- 從上式可導出軌道速度
$$ v=\sqrt{ \frac{GM}{r} } $$ 

# 軌道週期 (Orbital Period)
- 週期為衛星繞行一圈所需時間
$$ v = \frac{2\pi r}{T} $$ 
- 將速度公式代入,可得週期
$$ \sqrt{ \frac{GM}{r} } = \frac{2\pi r}{T} $$ 
$$ T^2 = \frac{4\pi^2 r^3}{GM} $$ 
- 此為克卜勒第三定律於圓形軌道的特例

# 軌道能量 (Orbital Energy)
- 衛星的總機械能 = 動能 + 位能
- $E = K + U$

## 位能 (Potential Energy)
- 無窮遠處定義為位能零點
$$ U = -\frac{GMm}{r} $$ 

## 動能 (Kinetic Energy)
$$ K = \frac{1}{2}mv^2 $$ 
- 將軌道速度 $v^2 = \frac{GM}{r}$ 代入
$$ K = \frac{1}{2}m(\frac{GM}{r}) = \frac{GMm}{2r} $$ 

## 總能量 (Total Mechanical Energy)
$$ E = K + U = \frac{GMm}{2r} + (-\frac{GMm}{r}) $$ 
$$ E = -\frac{GMm}{2r} $$ 
- 總能量為負值,代表衛星被引力束縛
- $E = -K = \frac{1}{2}U$

# 脫離速度 (Escape Velocity)
- 脫離速度是物體能完全擺脫星球引力,所需的最小初始速度
- 此時總機械能需大於等於零
- $E = K + U \ge 0$
$$ \frac{1}{2}mv_{esc}^2 - \frac{GMm}{R} \ge 0 $$ 
- R 為星球半徑
$$ v_{esc} = \sqrt{\frac{2GM}{R}} $$ 
- $v_{esc} = \sqrt{2} \cdot v_{orbit}$ (在同一半徑R下)

# 同步衛星 (Geostationary Satellite)
- 軌道週期與地球自轉週期相同的衛星
- $T = 24 \text{ hours}$ 
$$ \frac{GMm}{r^{2}}=m \frac{v^{2}}{r}= m \frac{(\omega r)^{2}}{r}=m \omega^2 r = m(\frac{2\pi}{T})^2 r $$ 
$$ r = {\left( \frac{GMT^2}{4\pi^{2}} \right)^{1/3}}\approx 42,241 \text{ km} $$ 