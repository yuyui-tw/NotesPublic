---
aliases:
  - SHM
  - 簡諧運動
tags:
  - Physics
up:
  - "[[periodic motion]]"
related:
  - "[[Wave]]"
annotation:
---

# 概要

**簡諧運動 (Simple Harmonic Motion, SHM)** 是[[periodic motion|週期性運動]]中最基本的一種振盪形式。其定義核心為：系統受到的**回復力 (Restoring Force)** 與其偏離平衡點的**位移 (Displacement)** 成正比且方向相反。從數學上講，它是由二階常微分方程 $\frac{d^2x}{dt^2} +  \omega^2 x = 0$ 所描述的運動。

SHM 是理解更複雜振盪現象（如阻尼、共振）和[[Wave|波]]的基礎。介質中單一質點在[[機械波]]通過時的運動，通常就可近似為簡諧運動。

---

# 原理/推導: 從微分方程到運動解

### 1. 理想簡諧運動 (Ideal SHM)
- **運動方程式 (Equation of Motion)**: 根據牛頓第二定律與虎克定律 $F=-kx$ 推導：
  $$ m\frac{d^2x}{dt^2} = -kx \Rightarrow \frac{d^2x}{dt^2} +  \omega^2 x = 0 $$
  其中，自然角頻率 $\omega =  \sqrt{(k/m)}$。這是一個二階線性齊次常微分方程。
- **通解 (General Solution)**: 此方程的通解形式為：
  $$ x(t) = C_1 \cos(\omega t) + C_2 \sin(\omega t) $$
  其中 $C_1$ 和 $C_2$ 是由初始條件決定的常數。此解也可寫成更符合物理直觀的**相-幅形式**:
  $$ x(t) = A \cos(\omega t + \phi) $$
  - **振幅 (A)**: $A = \sqrt{C_1^2 + C_2^2}$，表示最大位移。
  - **相位常數 ($\phi$)**: $\phi = \arctan(-C_2/C_1)$，表示 $t=0$ 時的初始相位。
- **運動學量的微分關係**:
  - **速度**: $v(t) = \frac{dx}{dt} = -A \omega \sin(\omega t + \phi)$
  - **加速度**: $a(t) = \frac{dv}{dt} = -A \omega^2 \cos(\omega t + \phi) = - \omega^2x(t)$

### 2. 簡諧運動的能量守恆
系統總機械能 $E = K + U = \frac{1}{2}mv^2 + \frac{1}{2}kx^2$。其對時間的導數為：
$$ \frac{dE}{dt} = \frac{d}{dt} 
\left( \frac{1}{2}m v^2 + \frac{1}{2}k x^2 
\right) = mv\frac{dv}{dt} + kx\frac{dx}{dt} $$
將 $v = dx/dt$ 和 $a = dv/dt = - (k/m)x$ 代入：
$$ \frac{dE}{dt} = m v (-\frac{k}{m}x) + kxv = -kvx + kxv = 0 $$
$dE/dt = 0$ 證明了在理想SHM中，總機械能是守恆的。將 $x(t)$ 和 $v(t)$ 的解代入能量表達式，可得總能量 $E = \frac{1}{2}kA^2$。

---

# 延伸: 阻尼與強制振盪

### 1. 阻尼振盪 (Damped Oscillation)
- **運動方程式**: 引入與速度成正比的阻尼力 $F_d = -bv$：
  $$ m\frac{d^2x}{dt^2} + b\frac{dx}{dt} + kx = 0 $$
- **特徵方程式與解**: 這是一個具有常數係數的二階齊次微分方程。我們假設解的形式為 $x(t)=e^{\lambda t}$，代入後得到特徵方程式：
  $$ m \lambda^2 + b \lambda + k = 0 $$
  其解為 $\lambda = \frac{-b \pm \sqrt{b^2 - 4mk}}{2m}$。解的形式由判別式 $b^2 - 4mk$ 的符號決定。
  1.  **欠阻尼 (Underdamped)**: $b^2 < 4mk$。根為一對共軛複數。解的形式為振幅呈指數衰減的振盪。
      $$ x(t) = A_0 e^{-\frac{b}{2m}t} \cos(\omega' t + \phi) $$
      其中阻尼角頻率 $\omega' = \sqrt{\frac{k}{m} - (\frac{b}{2m})^2} = \sqrt{\omega^2 - (\frac{b}{2m})^2}$。
  2.  **臨界阻尼 (Critically Damped)**: $b^2 = 4mk$。根為一個重根。系統不振盪，並以最快速度回到平衡。
      $$ x(t) = (C_1 + C_2 t)e^{-\frac{b}{2m}t} $$
  3.  **過阻尼 (Overdamped)**: $b^2 > 4mk$。根為兩個不等的負實根。系統不振盪，緩慢地回到平衡。
      $$ x(t) = C_1 e^{\lambda_1 t} + C_2 e^{\lambda_2 t} $$

### 2. 強制阻尼振盪 (Forced Damped Oscillation)
- **運動方程式**: 在阻尼系統上施加週期性驅動力 $F(t) = F_0 \cos(\omega_d t)$：
  $$ m\frac{d^2x}{dt^2} + b\frac{dx}{dt} + kx = F_0 \cos(\omega_d t) $$
- **通解結構**: 作為一個二階線性**非齊次**微分方程，其通解 $x(t)$ 是**齊次解** $x_h(t)$ 與**特解** $x_p(t)$ 的和。
  $$ x(t) = x_h(t) + x_p(t) $$
  1.  **暫態解 (Transient Solution, $x_h(t)$)**:
      這就是前述的阻尼振盪解。由於指數衰減項 $e^{-\frac{b}{2m}t}$ 的存在，該部分隨時間推移而消失。
      $$ x_h(t) = C e^{-\frac{b}{2m}t} \cos(\omega' t + \phi) $$
  2.  **穩態解 (Steady-State Solution, $x_p(t)$)**:
      當暫態解消失後，系統以驅動頻率 $\omega_d$ 進行穩態振盪。這是方程的一個特解，形式為：
      $$ x_p(t) = A(\omega_d) \cos(\omega_d t - \delta) $$
      - **穩態振幅 $A( \omega_d)$**: 振幅大小依賴於驅動頻率 $\omega_d$。
        $$ A(\omega_d) = \frac{F_0/m}{\sqrt{(\omega_d^2 - \omega^2)^2 + (b\omega_d/m)^2}} $$
      - **相位差 $ ext{δ}$**: 穩態振盪的位移落後於驅動力的相位。
        $$ \tan\delta = \frac{b\omega_d/m}{\omega_d^2 - \omega^2} $$
- **共振 (Resonance)**: 當穩態振幅 $A( \omega_d)$ 達到最大值時，即為共振。這發生在驅動頻率 $\omega_d$ 約等於系統的自然頻率 $\omega$ 時。嚴格來說，振幅共振頻率為 $\omega_R = \sqrt{\omega^2 - b^2/2m^2}$，只有在阻尼 $b$ 極小時才約等於 $\omega$。

---
# 相關系統範例

- **彈簧振子**: 質量為 $m$ 的物塊連接勁度係數為 $k$ 的理想彈簧，角頻率 $\omega = \sqrt{k/m}$。勁度係數 $k$ 取決於材料的楊氏模數與幾何形狀。
- **單擺 (Simple Pendulum)**: 在小角度近似 ($\sin\theta \approx \theta$) 下，運動方程簡化為 $L\ddot{\theta} + g\theta = 0$，成為 SHM，角頻率 $\omega = \sqrt{g/L}$。
- **物理擺 (Physical Pendulum)**: 任何繞固定軸擺動的剛體，小角度振盪的角頻率為 $\omega = \sqrt{mgd/I}$，其中 $d$ 為質心與轉軸距離，$I$ 為轉動慣量。
- **LC電路**: 電感 $L$ 和電容 $C$ 組成的電路中，電荷 $Q$ 的振盪方程為 $L\frac{d^2Q}{dt^2} + \frac{1}{C}Q = 0$，這也是 SHM，角頻率 $\omega = \sqrt{1/LC}$。

---

# 應用與工程考量
### 1. 共振的利用與避免
共振現象在工程設計中是雙面刃，既要避免其破壞性，也要利用其放大效應。
- **避免共振 (災害防制)**:
  - **橋梁與建築設計**: 工程师必須計算結構（如橋梁、高樓）的自然頻率，並確保該頻率遠離常見的外部驅動力頻率（如強風、地震波、人流步伐）。著名的 **塔科馬海峽吊橋 (Tacoma Narrows Bridge)** 崩塌事件，就是因為橋梁的自然頻率與風所造成的渦流頻率發生共振，導致振幅過大而崩毀。
  - **機械與引擎**: 旋轉機械（如引擎、馬達）的設計需要避開其操作轉速範圍內的共振頻率，以防止劇烈振動損壞零件。
- **利用共振 (儀器設計)**:
  - **樂器**: 弦樂器（如吉他）或管樂器（如長笛）的設計，就是為了在特定頻率（基頻與泛音）產生共振，從而發出清晰、響亮的樂音。
  - **無線電與通訊**: 早期的收音機通過調整 LC 振盪電路的電容或電感，使其自然頻率與目標電台的無線電波頻率相匹配（共振），從而放大特定頻率的信號，實現頻道選擇。
  - **掃描探針顯微鏡 (SPM)**: 例如原子力顯微鏡 (AFM)，其探針懸臂會以極高的共振頻率振盪。當探針接近樣品表面時，原子間作用力會改變其共振頻率，通過測量此頻率的微小變化，可以反推出樣品表面的形貌。

### 2. 阻尼的應用
- **避震器 (Shock Absorber)**: 汽車的懸吊系統是**臨界阻尼**或**微欠阻尼**的經典應用。當車輪遇到顛簸時，避震器能迅速吸收衝擊能量，讓車身快速穩定下來，而不會持續上下晃動（欠阻尼）或反應遲鈍（過阻尼）。
- **地震儀 (Seismometer)**: 地震儀內部有一個擺錘系統。為了準確記錄地面運動，而不是讓擺錘自身的振盪影響讀數，系統通常設計有適當的阻尼，使其能夠忠實地跟隨並記錄地震波的動態。
- **儀表指針**: 傳統的指針式儀表（如電壓表、壓力錶）的指針機構也利用阻尼，使其在讀數變化時能快速穩定指向新值，而不會來回擺動。
