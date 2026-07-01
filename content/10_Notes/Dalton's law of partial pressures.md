---
tags:
  - Chemistry
  - Physics
up:
  - "[[理想氣體方程式]]"
related:
annotation:
aliases:
  - Dalton's Law
  - Partial Pressures
  - 分壓定律
---
# 概要
道爾頓分壓定律 (Dalton's Law of Partial Pressures) 指出，在一個由多種互不反應的氣體組成的混合氣體中，其 **總壓力 (total pressure)** 等於各個氣體 **分壓 (partial pressure)** 的總和。

**分壓** 的定義是：在相同溫度下，該氣體單獨佔據整個容器體積時所產生的壓力。

# 理論

## 理論基礎：氣體動力論 (KMT)
道爾頓分壓定律的成立，源於理想氣體的假設：
1.  **粒子體積可忽略**：氣體粒子本身不佔體積。
2.  **無分子間作用力**：氣體粒子之間互不影響，彼此獨立。

基於這些假設，每種氣體的粒子對容器壁的碰撞所貢獻的壓力，與其他種類的氣體無關。因此，總壓力就是所有氣體粒子碰撞效應的簡單疊加。

## 分壓與莫耳分率 (Partial Pressure and Mole Fraction)
計算分壓最實用的方法是使用 **莫耳分率 (Mole Fraction, $\chi$)**。

對於混合氣體中的某個氣體 A，其莫耳分率 $\chi_A$ 定義為：
$$ \chi_A = \frac{n_A}{n_{\text{total}}} = \frac{\text{氣體 A 的莫耳數}}{\text{總莫耳數}} $$

根據理想氣體方程式 $PV=nRT$，氣體 A 的分壓為 $P_A = \frac{n_A RT}{V}$，總壓力為 $P_{\text{total}} = \frac{n_{\text{total}} RT}{V}$。將兩式相除可得：
$$ \frac{P_A}{P_{\text{total}}} = \frac{n_A}{n_{\text{total}}} = \chi_A $$

由此得到分壓的核心計算關係：
$$ P_A = \chi_A \cdot P_{\text{total}} $$

## 應用：排水集氣法 (Collecting Gas Over Water)
在實驗室中，常使用排水集氣法來收集難溶於水的氣體。這樣收集到的氣體，實際上是目標氣體與 **水蒸氣 (water vapor)** 的混合物。

此時，收集瓶內的總壓力等於目標氣體的分壓與水蒸氣的分壓（即水的 **飽和蒸氣壓**）之和：
$$ P_{\text{total}} = P_{\text{gas}} + P_{\text{water vapor}} $$

水的飽和蒸氣壓只與溫度有關，可以從文獻中查得。因此，要計算乾燥的目標氣體的壓力，必須扣除水的蒸氣壓：
$$ P_{\text{gas}} = P_{\text{total}} - P_{\text{water vapor}} $$

# 公式

## 道爾頓分壓定律
混合氣體的總壓力等於各氣體分壓之和：
$$ P_{\text{total}} = P_1 + P_2 + P_3 + \dots = \sum_{i} P_i $$

## 分壓計算
特定氣體 A 的分壓，等於其莫耳分率乘以總壓力：
$$ P_A = \chi_A \cdot P_{\text{total}} $$
其中，莫耳分率 $\chi_A$ 為：
$$ \chi_A = \frac{n_A}{n_{\text{total}}} = \frac{n_A}{n_A + n_B + \dots} $$

## 排水集氣法
$$ P_{\text{gas}} = P_{\text{total}} - P_{\text{water vapor}} $$

