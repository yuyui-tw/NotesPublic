---
aliases:
  - 轉動慣量
tags:
  - Physics
up:
  - "[[Rotational motion]]"
related:
  - "[[Parallel-axis theorem]]"
annotation:
---
# 概要
轉動慣量 (Moment of Inertia, $I$) 是物體對轉動狀態改變的阻力，為轉動版本的「質量」。
它取決於物體的總質量與**質量相對於轉軸的分佈**。質量離轉軸越遠，轉動慣量越大。
![[University Physics with Modern Physics 15th Edition By Hugh D. Young_compressed.pdf#page=305&rect=71,386,620,724|University Physics with Modern Physics 15th Edition By Hugh D. Young_compressed, p.cccvii|600]]

# 核心概念
轉動慣量 $I$ 是連結力矩 $\tau$ 與角加速度 $\alpha$ 的比例常數，定義於轉動的牛頓第二定律中：
$$ \tau = I\alpha $$
其物理意義可從單質點的力矩推得：
$\tau = r F_t = r(ma_t) = r(mr\alpha) = (mr^2)\alpha$
由此可見，質點的轉動慣量為 $I = mr^2$。

# 結構/要素
### 基本定義
- **離散系統 (Discrete System)**:
  $$ I = \sum_{i} m_i r_i^2 $$
  ($r_i$ 為質點 $m_i$ 到轉軸的垂直距離)

- **連續系統 (Continuous Body)**:
  $$ I = \int r^2 dm $$
  ($r$ 為質量微元 $dm$ 到轉軸的距離)

### 平行軸定理 (Parallel-Axis Theorem)
平行軸定理是一個重要的計算工具，它建立了物體繞質心軸的轉動慣量 $I_{cm}$ 與繞任一平行軸的轉動慣量 $I$ 之間的關係。

其公式為：
$$ I = I_{cm} + Md^2 $$
- $M$: 物體總質量
- $d$: 兩平行軸之間的距離

此定理的詳細推導、使用條件與應用，請參見 [[Parallel-axis theorem]]。

# 原理/推導
連續體的轉動慣量是透過積分 $I = \int r^2 dm$ 計算的，其中 $r$ 是質量微元 $dm$ 到轉軸的垂直距離。
若密度 $\rho$ 均勻，可寫為 $I = \rho \int r^2 dV$。

### 1. 中空圓柱體 (Hollow Cylinder)
- **方法**: 將圓柱體視為由許多半徑為 $r$、厚度為 $dr$ 的薄圓柱殼組成。
- **質量微元**:
    - 考慮一個半徑為 $r$、厚度為 $dr$、長度為 $L$ 的薄圓柱殼。
    - 體積微元 $dV = (2\pi r dr) L$
    - 質量微元 $dm = \rho dV = \rho (2\pi rL dr)$
- **積分**:
    - 轉動慣量 $I = \int r^2 dm = \int_{R_1}^{R_2} r^2 [\rho (2\pi rL dr)]$
    - $I = 2\pi \rho L \int_{R_1}^{R_2} r^3 dr = 2\pi \rho L \left[ \frac{r^4}{4} \right]_{R_1}^{R_2} = \frac{\pi \rho L}{2} (R_2^4 - R_1^4)$
- **與總質量 M 連結**:
    - 總質量 $M = \int dm = \int_{R_1}^{R_2} \rho (2\pi rL dr) = 2\pi \rho L \int_{R_1}^{R_2} r dr = \pi \rho L (R_2^2 - R_1^2)$
    - 因此，密度 $\rho = \frac{M}{\pi L (R_2^2 - R_1^2)}$
- **最終結果**:
    - 將 $\rho$ 代入 $I$ 的表達式：
    - $I = \frac{\pi L}{2} \frac{M}{\pi L (R_2^2 - R_1^2)} (R_2^4 - R_1^4)$
    - $I = \frac{M}{2} \frac{(R_2^2 - R_1^2)(R_2^2 + R_1^2)}{R_2^2 - R_1^2} = \frac{1}{2} M(R_1^2 + R_2^2)$
- **特例**:
    - **實心圓柱 (Solid Cylinder)**: $R_1=0 \implies I = \frac{1}{2} M R^2$
    - **薄壁圓柱 (Thin-walled Cylinder)**: $R_1 \approx R_2 = R \implies I = M R^2$

### 2. 均勻實心球體 (Uniform Solid Sphere)
- **方法**: 將球體切割成許多軸線與旋轉軸重合的薄實心圓盤。
- **圓盤慣量**: 圓盤半徑為 $r = \sqrt{R^2 - x^2}$，其轉動慣量為 $dI = \frac{1}{2} r^2 dm$。
- **積分**: 對 $x$ 從 $-R$ 到 $R$ 積分 $dI$。
- **結果**: $I = \frac{2}{5} M R^2$

### 3. 非均勻物體
若物體密度不均，例如細長桿的線密度 $\frac{dm}{dx} = \gamma x$，則需將此關係代入 $I = \int r^2 dm$ 進行積分。

