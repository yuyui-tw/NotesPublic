---
aliases:
  - 應力與應變
tags:
  - Physics
up:
related:
annotation:
---
# 概要
應力 (Stress) 為物體單位面積所受的力，描述引發變形的原因；應變 (Strain) 則是物體因應力而產生的相對變形量。
兩者關係揭示了材料的彈性 (Elasticity) 與塑性 (Plasticity) 特性。

# 核心概念
1.  **應力 (Stress, $\sigma$)**: 單位面積所受的力，用以量化造成物體變形的外力。單位為帕斯卡 (Pa)。
    -   **正向應力 (Normal Stress)**: 作用力垂直於橫截面。
        -   **拉伸應力 (Tensile Stress)**: $\sigma = \frac{F_{\perp}}{A}$，物體被拉伸。
        -   **壓縮應力 (Compressive Stress)**: $\sigma = \frac{F_{\perp}}{A}$，物體被壓縮。
    -   **剪應力 (Shear Stress, $\tau$)**: $\tau = \frac{F_{\parallel}}{A}$，作用力平行於橫截面。
2.  **應變 (Strain, $\epsilon$)**: 物體變形的相對程度，為無因次量。
    -   **正向應變 (Normal Strain)**:
        -   **拉伸/壓縮應變**: $\epsilon = \frac{\Delta l}{l_0}$，長度變化量與原始長度之比。
    -   **剪應變 (Shear Strain, $\gamma$)**: $\gamma = \frac{x}{h} = \tan\theta$，物體側面相對位移與兩面間距之比。
    -   **體積應變 (Volume Strain)**: $\epsilon_V = \frac{\Delta V}{V_0}$，體積變化量與原始體積之比。

# 結構/要素
**虎克定律 (Hooke's Law)**
在彈性限度內，應力與應變成正比，其比例常數稱為**彈性模數 (Elastic Modulus)**。
$$ \text{應力} = \text{彈性模數} \times \text{應變} $$
-   **楊氏模數 (Young's Modulus, Y)**: 描述材料抵抗拉伸或壓縮變形的能力。
$$ Y = \frac{\text{正向應力}}{\text{正向應變}} = \frac{\sigma}{\epsilon} = \frac{F_{\perp}/A}{\Delta l/l_0} $$
-   **剪切模數 (Shear Modulus, S)**: 描述材料抵抗剪切變形的能力。
$$ S = \frac{\text{剪應力}}{\text{剪應變}} = \frac{\tau}{\gamma} = \frac{F_{\parallel}/A}{x/h} $$
-   **體積模數 (Bulk Modulus, B)**: 描述材料抵抗體積變形的能力。
$$ B = \frac{-\Delta P}{\Delta V/V_0} $$
負號表示壓力增加時，體積減小。

**可壓縮性 (Compressibility, k)**
可壓縮性是體積模數的倒數，表示材料每單位壓力下的體積相對變化率。
$$ k = \frac{1}{B} = -\frac{1}{V_0}\frac{\Delta V}{\Delta P} $$

**應力-應變曲線 (Stress-Strain Curve)**
![[Stress-Strain Curve.png|450]]
該曲線描述材料從彈性變形到塑性變形，最終斷裂的過程。
- **彈性區 (Elastic Region)**: 應力移除後，物體可恢復原狀。遵循虎克定律的區域為此區的線性部分。
- **塑性區 (Plastic Region)**: 超過彈性極限後，產生永久變形。
- **斷裂點 (Fracture Point)**: 材料發生斷裂的位置。

# 原理/推導
應力與應變的關係主要基於實驗觀察與定義。
虎克定律即為一個基於實驗結果的經驗定律，描述了多數材料在小變形下的線性彈性行為。
