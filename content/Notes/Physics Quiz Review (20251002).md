---
tags:
  - QuizReview
  - Physics
---
START
9Qs
title: Physics Quiz Review (20251002)
content:
垂直上拋、拋射、衛星運動、終端速度

Q1: 
You throw a ball vertically from the roof of a tower building of height 300 m, with an upward speed of 15 m/s. 
The ball is in free fall. 
Find (a) the ball's velocity when it is 5 m above the railing; (b) the ball's acceleration when it is at its maximum height. (15%)
A1:
**核心觀念:** 垂直拋體運動。
**解題關鍵:**
1. (a) 使用不含時間的運動學公式 $v^2 = v_0^2 + 2a\Delta y$。注意 $\Delta y$ 為正，加速度 $a$ 為負 (-g)。速度 $v$ 有正負兩個解，分別代表上升與下降經過該點。
2. (b) 在最高點，瞬時速度為 0，但加速度恆為重力加速度 $g$，方向向下。

---
**核心觀念:**
- 垂直拋體運動
- 自由落體加速度恆為定值
- 運動學公式: $v^2 = v_0^2 + 2a\Delta y$

**解題思路:**
(a)
- **設定座標:** 以拋出點為 y=0，向上為正。
- **已知條件:** 初始速度 $v_0 = +15$ m/s，加速度 $a = -g = -9.8$ m/s²，位移 $\Delta y = +5$ m。
- **計算:**
  - $v^2 = v_0^2 + 2a\Delta y = 15^2 + 2(-9.8)(5) = 225 - 98 = 127$
  - $v = \pm\sqrt{127} \approx \pm 11.27$ m/s。
- **解釋:** 正值代表上升時經過該點的速度，負值代表下降時經過該點的速度。題目未指明，兩個都是可能的答案。

(b)
- **觀念:** 在最高點，物體的瞬時速度為 0，但它仍然在地球的重力場中。
- **結論:** 加速度始終是重力加速度 $g$，方向向下。因此，$a = -9.8$ m/s²。

Q2: 
A projectile is fired with initial speed $v_0$ at angle $\theta$ above the horizontal from a point at height h. 
Show that (證明) the horizontal range(水平距離) is:
$$ R = \frac{v_0^2 \sin 2\theta}{2g} \left( 1 + \sqrt{1 + \frac{2gh}{v_0^2 \sin^2\theta}} \right) $$
(20%)
A2:
**核心觀念:** 
- 拋體運動
- 拋體運動的獨立性 (水平與垂直)
- 二次方程式求解

**解題關鍵:**
1. 寫出垂直位置函數 $y(t) = h + (v_0 \sin\theta)t - \frac{1}{2}gt^2$。
2. 令 $y(t)=0$ (落地)，使用二次公式解出飛行時間 $t$。
3. 將飛行時間 $t$ 代入水平位置函數 $R = (v_0 \cos\theta)t$。
4. 透過三角函數恆等式 ($2\sin\theta\cos\theta = \sin 2\theta$) 化簡即可得證。

**解題思路:**
1.  **垂直運動:** 寫出垂直位置函數 $y(t) = h + (v_0 \sin\theta)t - \frac{1}{2}gt^2$。令 $y(t)=0$ (落地) 得到關於飛行時間 t 的二次方程式: $\frac{1}{2}gt^2 - (v_0 \sin\theta)t - h = 0$。
2.  **求解飛行時間 t:** 使用二次公式 $t = \frac{-b \pm \sqrt{b^2-4ac}}{2a}$，代入 $a = g/2, b = -v_0 \sin\theta, c = -h$。取正根可得 $t = \frac{v_0 \sin\theta + \sqrt{v_0^2 \sin^2\theta + 2gh}}{g}$。
3.  **水平運動:** 水平射程 $R = (v_0 \cos\theta)t$。將 t 代入得 $R = \frac{v_0 \cos\theta}{g} (v_0 \sin\theta + \sqrt{v_0^2 \sin^2\theta + 2gh})$。
4.  **化簡:** 將 $v_0 \sin\theta$ 提出根號外，需要平方後再開方。$R = \frac{v_0^2 \sin\theta\cos\theta}{g} \left(1 + \frac{\sqrt{v_0^2 \sin^2\theta + 2gh}}{v_0 \sin\theta}\right) = \frac{v_0^2 (2\sin\theta\cos\theta)}{2g} \left(1 + \sqrt{1 + \frac{2gh}{v_0^2 \sin^2\theta}}\right)$。利用 $2\sin\theta\cos\theta = \sin 2\theta$ 即得證。

Q3: 
A geosynchronous satellite orbits (地球同步衛星) at an altitude of 35,800 km above the earth's surface. 
What is its centripetal acceleration? [radius of Earth = 6371 km] (15%)
A3:
**核心觀念:**
- 同步衛星的定義
- 向心加速度公式: $a_c = \omega^2 r$

**解題關鍵:**
1. 同步衛星的週期 $T$ 等於地球自轉週期 (24 小時)。
2. 軌道半徑 $r$ 是地球半徑 $R_E$ 加上軌道高度 $h$。
3. 由週期算出角速度 $\omega = \frac{2\pi}{T}$。
4. 代入向心加速度公式 $a_c = \omega^2 r$ 求解。

**解題思路:**
1.  **週期 (T):** ==同步衛星的週期與地球自轉相同==，T = 24 hours = 86400 s。
2.  **軌道半徑 (r):** $r = R_E + h = 6371 \text{ km} + 35800 \text{ km} = 42171 \text{ km} = 4.2171 \times 10^7 \text{ m}$。
3.  **角速度 ($\omega$):** $\omega = \frac{2\pi}{T} = \frac{2\pi}{86400 \text{ s}} \approx 7.272 \times 10^{-5} \text{ rad/s}$。
4.  **向心加速度 ($a_c$):** $a_c = \omega^2 r = (7.272 \times 10^{-5})^2 \times (4.2171 \times 10^7) \approx 0.223 \text{ m/s}^2$。

Q4: 
A satellite in circular orbit has an orbital speed of 7.8 km/s. 
What is the period of the orbit? (15%)
A4:
**核心觀念:**
- 萬有引力提供向心力
- 圓周運動週期與速度的關係

**解題關鍵:**
1. 建立力平衡關係式: 萬有引力 = 向心力，即 $\frac{G M_E m}{r^2} = \frac{m v^2}{r}$。
2. 從上式解出軌道半徑 $r = \frac{G M_E}{v^2}$。
3. 將半徑 $r$ 代入週期公式 $T = \frac{2\pi r}{v}$ 求解。

**解題思路:**
1.  **力平衡:** 萬有引力 = 向心力, $\frac{G M_E m}{r^2} = \frac{m v^2}{r}$。
2.  **求解軌道半徑 (r):** $r = \frac{G M_E}{v^2} = \frac{(6.67\times10^{-11})(5.97\times10^{24})}{(7.8 \times 10^3)^2} \approx \frac{3.982\times10^{14}}{6.084\times10^7} \approx 6.545 \times 10^6 \text{ m}$。
3.  **計算週期 (T):** $T = \frac{2\pi r}{v} = \frac{2\pi (6.545 \times 10^6)}{7.8 \times 10^3} \approx 5266 \text{ s}$ (約 87.8 分鐘)。

Q5: 
In a conical pendulum, a bob with constant speed 1.21 m/s moves in a horizontal circle. 
The string is 1.2 m long and makes an angle of 20° with the vertical. 
Find the acceleration of the bob. (10%)
A5:
**核心觀念:** 
- 圓錐擺為水平圓周運動，加速度即為向心加速度。
- 向心加速度: $a_c = v^2/r$

**解題關鍵:**
1. 圓錐擺的運動是水平圓周運動，其加速度即為向心加速度 $a_c$。
2. 圓周半徑 $r$ 可由繩長 $L$ 和角度 $\theta$ 算出: $r = L \sin\theta$。
3. 將 $v$ 和 $r$ 代入公式 $a_c = v^2/r$ 求解。

**解題思路:**
1.  **計算圓周半徑 (r):** 從幾何關係，$r = L \sin\theta = 1.2 \times \sin(20°) \approx 1.2 \times 0.342 = 0.4104 \text{ m}$。
2.  **計算向心加速度 ($a_c$):** $a_c = \frac{v^2}{r} = \frac{1.21^2}{0.4104} = \frac{1.4641}{0.4104} \approx 3.567 \text{ m/s}^2$。

Q6: 
A roller coaster at its highest point has a radius of curvature of 6.5 m. 
(a) What is the minimum speed to not lose contact? 
(b) If the actual speed is 9.5 m/s, what is the apparent weight of a 40-kg child? (10%)
A6:
**核心觀念:** 
- 圓周運動的向心力由重力和正向力提供。
- 視重 (Apparent weight) 等於正向力 (Normal force, N)。

**解題關鍵:**
1. 在最高點，向心力由「重力」與「正向力」共同提供: $N + mg = \frac{mv^2}{r}$。
2. (a) 最小速度(不脫離軌道)的臨界條件是正向力 $N=0$，此時 $mg = \frac{mv_{min}^2}{r}$。
3. (b) 視重即為正向力 $N$。由第一步的公式移項可得 $N = m(\frac{v^2}{r} - g)$。

**解題思路:**
1.  **最高點受力:** 重力(mg)和正向力(N)都指向圓心，合力提供向心力: $N + mg = \frac{mv^2}{r}$。
2.  **(a) 最小速度:** =="不脫離軌道" 的臨界條件是正向力 N=0(正向力是接觸力。當兩個物體即將分離、失去接觸的那一瞬間，它們之間的接觸力正好變為零。)==。此時 $mg = \frac{mv_{min}^2}{r}$，解得 $v_{min} = \sqrt{gr} = \sqrt{9.8 \times 6.5} = \sqrt{63.7} \approx 7.98 \text{ m/s}$。
>「不脫離軌道」的臨界條件，就是指剛好要接觸，又剛好要分開的那個瞬間。在這個瞬間，接觸力 N 恰好為零。如果速度再慢一點點，mg 將會大於所需的向心力mv²/r，這時沒有任何力可以抵銷多餘的重力，車子將會脫離圓形軌道，開始做拋體運動掉下來。
3.  **(b) 視重:** 視重即正向力 N。由第一步公式移項得 $N = \frac{mv^2}{r} - mg = m(\frac{v^2}{r} - g)$。代入數值: $N = 40 \times (\frac{9.5^2}{6.5} - 9.8) = 40 \times (13.88 - 9.8) = 40 \times 4.08 = 163.2 \text{ N}$。(==注意單位==)

Q7: 
A 9-kg object starting from rest falls through a viscous medium with $F_{drag} \propto v$. 
It reaches half its terminal speed $v_T$ in 5.54s. 
(a) Determine $v_T$. 
(b) How far has it traveled in the first 5.54s? (20%)
A7:
**核心觀念:**
- 黏性介質是==由於層間內部摩擦而阻礙流動的流體==，這種特性被稱為黏度。 這種內部摩擦力衡量的是流體的「黏性」及其運動阻力。
- 牛頓第二定律含阻力項: $m\frac{dv}{dt} = mg - bv$。
- 終端速度發生在加速度為0時。

**解題關鍵:**
1. 寫出含阻力的牛頓第二定律: $m\frac{dv}{dt} = mg - bv$。
2. 解此微分方程可得速度函數 $v(t) = v_T(1 - e^{-\frac{b}{m}t})$，其中終端速度 $v_T = \frac{mg}{b}$。
3. 利用 $v(5.54) = v_T / 2$ 的條件，可以解出阻力係數 $b$。
4. 將 $b$ 代入即可求得 $v_T$。
5. 對 $v(t)$ 積分可得位移函數 $x(t)$，代入時間即可求解。

**解題思路:**
1.  **速度函數:** 解微分方程可得 $v(t) = v_T(1 - e^{-\frac{b}{m}t})$。
2.  **求阻力係數 (b):** 由 $v(5.54) = v_T / 2$ 可知 $0.5 = 1 - e^{-\frac{b}{9}(5.54)}$，解得 $e^{-\frac{5.54b}{9}} = 0.5$。取自然對數 $\frac{5.54b}{9} = \ln(2)$，所以 $b = \frac{9 \ln(2)}{5.54} \approx \frac{9 \times 0.693}{5.54} \approx 1.125 \text{ kg/s}$。
3.  **求終端速度 ($v_T$):** $v_T = \frac{mg}{b} = \frac{9 \times 9.8}{1.125} = 78.4 \text{ m/s}$。
4.  **求位移 x(t):** 對 $v(t)$ 積分: $x(t) = \int_0^t v_T(1 - e^{-\frac{b}{m}t}) dt = v_T[t + \frac{m}{b}e^{-\frac{b}{m}t}]_0^t$。代入 t=5.54s: $x(5.54) = v_T[(5.54 + \frac{m}{b}e^{-\frac{b}{m}(5.54)}) - (0 + \frac{m}{b}e^0)] = v_T[5.54 + \frac{m}{b}(0.5) - \frac{m}{b}] = v_T[5.54 - 0.5\frac{m}{b}]$。代入數值: $x(5.54) = 78.4[5.54 - 0.5(\frac{9}{1.125})] = 78.4[5.54 - 4] = 120.736 \text{ m}$。

TARGET DECK: PhysicQ

source url: 

END
