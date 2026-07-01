---
aliases:
  - 無滑動滾動
tags:
  - Physics
up:
  - "[[Rotaional energy]]"
related:
annotation:
---
# 概要
無滑動滾動 (Rolling without slipping) 是一種常見的物理運動，物體同時進行**平移 (translation)** 與**轉動 (rotation)**，且兩者之間存在一個完美的約束關係。

在這種理想情況下，物體與接觸面在接觸點上沒有相對滑動。這意味著物體的質心速度 $v_{cm}$、角速度 $\omega$ 和半徑 $R$ 之間存在一個固定關係：$v_{cm} = R\omega$。

# 理論
### 1. 運動學條件 (Kinematic Condition)
我們可以從接觸點的速度來理解無滑動的條件。
- 相對於質心，接觸點的切線速度方向向後，大小為 $R\omega$。
- 同時，整個物體（包括接觸點）以質心速度 $v_{cm}$ 向前平移。

在接觸點 B，這兩個速度向量相加：$\vec{v}_B = \vec{v}_{cm} + \vec{v}_{rot}$。
為了使接觸點相對於地面的速度為零（即不滑動），必須滿足：
$$ v_{cm} - R\omega = 0 \implies v_{cm} = R\omega $$
- 若 $v_{cm} > R\omega$，物體滑動 (sliding)。
- 若 $v_{cm} < R\omega$，物體打滑 (spinning)。

### 2. 滾動動能 (Kinetic Energy of Rolling)
滾動中的物體同時具有平移動能和轉動動能。其總動能可以從兩個角度計算：

**a) 以質心為參考點:**
總動能是平移動能和繞質心轉動的動能之和。
$$ K_{total} = K_{trans} + K_{rot} = \frac{1}{2}Mv_{cm}^2 + \frac{1}{2}I_{cm}\omega^2 $$

**b) 以接觸點為瞬時轉軸 (Instantaneous Axis of Rotation):**
在無滑動滾動的瞬間，接觸點 B 可視為瞬時轉軸。整個物體繞此點轉動，總動能即為繞 B 點的轉動動能。
$$ K_{total} = \frac{1}{2}I_B\omega^2 $$
根據[[Parallel-axis theorem|平行軸定理]]，$I_B = I_{cm} + MR^2$。代入上式：
$$ K_{total} = \frac{1}{2}(I_{cm} + MR^2)\omega^2 = \frac{1}{2}I_{cm}\omega^2 + \frac{1}{2}M(R\omega)^2 $$
因為 $v_{cm} = R\omega$，上式等於 $\frac{1}{2}I_{cm}\omega^2 + \frac{1}{2}Mv_{cm}^2$，與 a) 的結果完全相同。

### 3. 靜摩擦力的角色
要使物體產生角加速度（開始滾動或改變滾動速度），必須有力矩作用。
在水平面上滾動的物體，此力矩通常由**靜摩擦力**提供。
靜摩擦力作用在接觸點上，確保 $a_{cm} = R\alpha$ 的關係成立，但**靜摩擦力本身不作功**，因為其作用點的瞬時速度為零。

# 公式
- **無滑動條件**: $v_{cm} = R\omega$
- **無滑動加速度條件**: $a_{cm} = R\alpha$
- **總動能**: $K_{total} = \frac{1}{2}Mv_{cm}^2 + \frac{1}{2}I_{cm}\omega^2$

