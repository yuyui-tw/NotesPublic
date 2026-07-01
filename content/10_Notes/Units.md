---
tags:
  - Physics
up:
related:
aliases:
---
# 7 basic SI units

| physical quantity         | unit         |
| ------------------------- | ------------ |
| *length*                  | m(meter)     |
| *mass*                    | kg(kilogram) |
| *time*                    | s(second)    |
| *temp*                    | K(kelvin)    |
| *electric current*        | A(ampere)    |
| *luminosity*              | Cd(candela)  |
| num of atom<br>(Avogadro) | mol(mole)    |
>光/照/亮度 定義上不同，但都是對於光強度的描寫


# derivde units
- area $m^{2}$
- volume $m^{3}$
- density $kg/m^{3},g/cm^{3}$
- velocity $m/s$
- acceleration $m/s^{2}$
- frequency $s^{-1}\equiv Hz$
- force $kg\cdot m/s^{2}\equiv N$
- presure $N/m^{2}=\frac{kg\cdot m/s^{2}}{m^2}=\frac{kg}{s^{2}\cdot m}\equiv pa$
- energy/heat/work $N\cdot m=kg\cdot m^{2}/s^{2}\equiv J$
- power $J/s=Kg\cdot \frac{m^{2}}{s^{2}}\equiv W$
- charge $C\equiv A\cdot s$
- momentum(動量) $kg\cdot m/s$

>[!NOTES] 物理量分類
>Vector 向量: magnitude(量值) + direction
>Scalar 純量: a numerical value(magnitude only)
>Tensor 張量

# metric prefix 公制前綴

### Submultiples (小於 1 的前綴)
| Prefix | Symbol | Factor |
| --- | :---: | --- |
| deci | d | $10^{-1}$ |
| centi | c | $10^{-2}$ |
| milli | m | $10^{-3}$ |
| micro | $\mu$ | $10^{-6}$ |
| nano | n | $10^{-9}$ |
| pico | p | $10^{-12}$ |
| femto | f | $10^{-15}$ |
| atto | a | $10^{-18}$ |

> [!NOTE] Angstrom
> 埃 (Angstrom, $\mathring{A}$) 是一個特殊的長度單位，定義為 $1\mathring{A} = 10^{-10}$ m。它**不是**一個公制前綴。

### Multiples (大於 1 的前綴)
| Prefix | Symbol | Factor |
| --- | :---: | --- |
| deca | da | $10^{1}$ |
| hecto | h | $10^{2}$ |
| kilo | k | $10^{3}$ |
| mega | M | $10^{6}$ |
| giga | G | $10^{9}$ |
| tera | T | $10^{12}$ |
| peta | P | $10^{15}$ |
| exa | E | $10^{18}$ |

# Unit Vector
單位向量是一個長度(量值)為 1 的向量。它的唯一目的就是用來指向一個特定的方向。

### 定義與特性
- **定義**: 對於任意向量 $\vec{v}$，其對應的單位向量 $\hat{v}$ 可表示為：
  $$ \hat{v} = \frac{\vec{v}}{||\vec{v}||} $$
  其中 $||\vec{v}||$ 是向量 $\vec{v}$ 的長度。
- **特性**:
    - 量值為 1：$||\hat{v}|| = 1$。
    - 無單位：單位向量是純粹的方向指標，不帶有原始向量的物理單位。
    - **標準單位向量**: 在直角座標系 (Cartesian coordinate system) 中，我們常用 $\hat{i}, \hat{j}, \hat{k}$ 來分別代表 x, y, z 軸的正方向。任何向量都可以用它們的線性組合來表示，例如 $\vec{v} = v_x\hat{i} + v_y\hat{j} + v_z\hat{k}$。

### 座標系的選擇與計算簡化
在處理物理問題時，**明智地選擇座標系**是簡化計算的關鍵技巧。

一個好的座標系通常會將其一個或多個軸與問題中的關鍵方向對齊，例如：
- 物體的運動方向
- 主要作用力的方向
- 對稱軸的方向

**好處**:
透過使座標軸與向量平行，可以讓該向量在其他軸上的分量變為零。

**範例**:
假設一個物體在一個斜面上滑下。
- **糟糕的選擇**: 將 x-y 軸設為水平和垂直。這樣重力向量 $\vec{g}$ 很簡單 (只有 y 分量)，但法向力 $\vec{N}$ 和摩擦力 $\vec{f}$ 都會有 x 和 y 兩個分量，運動加速度 $\vec{a}$ 也會有兩個分量，計算會變得很複雜。
- **明智的選擇**: 將 x 軸設為沿斜面向下，y 軸設為垂直於斜面。這樣法向力 $\vec{N}$ 和加速度 $\vec{a}$ 都只剩下單一分量 ($\vec{N}=N\hat{j}$, $\vec{a}=a\hat{i}$)，只有重力 $\vec{g}$ 需要被分解。這會讓整個系統的方程式變得極為簡潔，大幅降低計算複雜性。
