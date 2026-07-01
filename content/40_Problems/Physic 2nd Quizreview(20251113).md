---
tags:
  - QuizReview
---
START
9Qs
title: Physic 2nd Quizreview(20251113)
content:


Q1: Some people are able to spin a basketball on the tip of a finger. 
It is often done by balancing the ball on the tip of the finger and brushing the other hand along the side of the ball to cause it to rotate. 
Suppose the ball begins from rest and reaches a final angular speed of 18.65 rad/s in 1.10 s.
(a) Assuming the ball is subject to a constant angular acceleration, what is the magnitude of the constant acceleration?
(b) Through how many revolutions does the ball rotate during the 1.10 s?
A1:
1.  **核心觀念:** 此問題屬於**等角加速度運動學**。當角加速度 $\alpha$ 為常數時，角速度 $\omega$ 和角位移 $\theta$ 的變化遵循特定的運動學公式。
2.  **思路解析 (a):**
    *   題目給定了初角速度 ($\omega_0 = 0$)、末角速度 ($\omega$) 和時間 ($t$)。
    *   要找到角加速度 $\alpha$，應選用直接關聯這四個物理量的公式：
        $$\omega = \omega_0 + \alpha t$$
    *   將已知值代入即可解出 $\alpha$。
3.  **思路解析 (b):**
    *   要計算轉動的「圈數」，首先需要求出總**角位移** $\Delta\theta$ (單位為弧度)。
    *   可以使用公式 $\Delta\theta = \omega_0 t + \frac{1}{2}\alpha t^2$，因為 $\alpha$ 在 (a) 中已經成為已知。
    *   計算出 $\Delta\theta$ (弧度) 後，利用換算關係 1 圈 = $2\pi$ 弧度，將其單位轉換為「圈」。

Q2: 
A copper rod with length 1.4 m and cross-sectional area 2 cm² is fastened to a steel rod of length Ls and cross-sectional area 1 cm². 
The compound structure is pulled on each side by two forces of equal magnitude 6 × 10⁴ N. 
Find the length of the steel rod if the elongations ($\Delta L$) of the two rods are equal. 
(Use Young's constants E_steel & E_cu)
A2:
1.  **核心觀念:** **楊氏模數 (Young's Modulus)** 描述了材料在受力時抵抗形變的能力，其定義為應力 (Stress, $F/A$) 與應變 (Strain, $\Delta L/L_0$) 的比值。公式為：
    $$\Delta L = \frac{F L_0}{E A}$$
2.  **思路解析:**
    *   **關鍵條件分析:** 
        1.  兩根桿串聯並在兩端受力，代表它們承受的**內部張力 $F$ 是相同的**。
        2.  題目明確指出，兩根桿的**伸長量 $\Delta L$ 是相等的**。
    *   **解題策略:** 
        *   分別寫出銅桿和鋼桿的伸長量表達式：$\Delta L_{cu}$ 和 $\Delta L_{steel}$。
        *   根據關鍵條件 $\Delta L_{cu} = \Delta L_{steel}$，建立一個等式。
        *   由於兩邊的 $F$ 和 $\Delta L$ 都相等，這個等式會將兩根桿的 $L_0$、$E$ 和 $A$ 關聯起來。
        *   將所有已知數值代入，即可解出未知的鋼桿長度 $L_{steel}$。

Q3: 
(a) Prove that the rotational inertia of a uniform, long thin rod of mass M and length L about an axis through its center and perpendicular to the rod is (1/12)ML².
(b) Use parallel-axis theorem to find the rotational inertia about a new axis in the edge.
A3:
1.  **核心觀念 (a):** **轉動慣量 (Rotational Inertia)** 是物體對轉動慣性的度量。對於連續分佈的質量，它需要通過積分計算：
    $$I = \int r^2 dm$$ 
    其中 $r$ 是質量元素 $dm$ 到轉軸的距離。
2.  **思路解析 (a):**
    *   **建立積分:** 
        *   首先，定義**線密度** $\lambda = M/L$。
        *   取一小段長度為 $dr$ 的質量元素 $dm$，其質量為 $dm = \lambda dr$。
        *   將坐標原點設在桿的中心，積分範圍為 $-L/2$ 到 $L/2$。
        *   將 $dm$ 代入轉動慣量公式進行積分，即可證明。
3.  **核心觀念 (b):** **平行軸定理 (Parallel-Axis Theorem)** 提供了一個捷徑，當我們已知繞質心軸的轉動慣量 $I_{cm}$ 時，可以快速求出繞任何平行軸的轉動慣量 $I$。公式為：
    $$I = I_{cm} + Md^2$$
4.  **思路解析 (b):**
    *   $I_{cm}$ 即為 (a) 中證明的 $\frac{1}{12}ML^2$。
    *   $d$ 是新軸（在桿的邊緣）到質心軸（在中心）的距離，在此例中 $d = L/2$。
    *   直接將 $I_{cm}$ 和 $d$ 代入平行軸定理公式即可得到結果，無需再次積分。

Q4: 
Canadian nuclear reactors use heavy water moderators in which elastic collisions occur between the neutrons and deuterons of mass 2u.
(a) What is the speed of a neutron, expressed as a fraction of its original speed, after a head-on, elastic collision with a deuteron that is initially at rest?
(b) What is the kinetic energy of a neutron, expressed as a fraction of its original kinetic energy...?
(c) How many such successive collisions will reduce the speed of a neutron to 1/59000 of its original value?
A4:
1.  **核心觀念:** **彈性碰撞 (Elastic Collision)** 的特點是系統的**總動量守恆**與**總動能守恆**。
2.  **思路解析 (a):**
    *   對於一維彈性碰撞，且目標物體B初速為零的特殊情況，有一個簡化的末速公式：
        $$v_{A2} = \left( \frac{m_A - m_B}{m_A + m_B} \right) v_{A1}$$
    *   將中子視為 $m_A$，氘核視為 $m_B$，代入各自的質量即可求出速度變化的比例。
3.  **思路解析 (b):**
    *   動能的表達式為 $K = \frac{1}{2}mv^2$。
    *   末動能與初動能的比值 $K_2/K_1$ 可以通過速度的比值 $v_2/v_1$ 來計算：$(v_2/v_1)^2$。
4.  **思路解析 (c):**
    *   這是一個等比級數問題。每次碰撞，速度都會乘以一個固定的比例 $f$（在 (a) 中已求出）。
    *   $n$ 次碰撞後，末速度將是初速度的 $f^n$ 倍。
    *   設定 $f^n = 1/59000$，然後使用對數 ($\\log$) 來解出 $n$。

Q5: 
Use integration to locate the CM of the triangular plate of base b and height h shown in the figure below. 
The plate has a uniform areal mass density $\sigma$ (kg/m²).
A5:
1.  **核心觀念:** 連續物體的**質心 (Center of Mass)** 位置是各質量元素的加權平均位置，需要通過積分計算：
    $$x_{cm} = \frac{1}{M} \int x dm \quad \text{和} \quad y_{cm} = \frac{1}{M} \int y dm$$
2.  **思路解析:**
    *   **“切片”策略:** 將三角形切成許多無限薄的細條來進行積分。可以選擇水平切或垂直切。
    *   **以水平切片為例 (求 $y_{cm}$):**
        *   在任意高度 $y$ 處，取一個厚度為 $dy$ 的水平細條。
        *   首先，需要用**相似三角形**原理，找出在 $y$ 高度處細條的寬度 $w$ 與 $y$ 的關係。
        *   該細條的質量 $dm$ 等於其面積 ($w \cdot dy$) 乘以面密度 $\sigma$。
        *   將 $dm$ 的表達式代入 $y_{cm}$ 的積分公式中，積分範圍為 $0$ 到 $h$。
        *   總質量 $M$ 也是通過對 $dm$ 積分得到。
    *   $x_{cm}$ 的計算與 $y_{cm}$ 類似，但通常改用垂直切片會更直觀。

Q6: 
A uniform hoop and a uniform solid disk are released from rest from a height h on an incline and roll without slipping.
(a) Which object reaches the bottom of the incline first? Explain your reasoning.
(b) Find expressions for the speed with which each object reaches the bottom of the incline.
A6:
1.  **核心觀念:** **能量守恆**。物體初始的重力位能 $U = Mgh$ 會轉化為到達底部時的動能。
2.  **關鍵區別:** 對於滾動物體，其動能包含**平動動能** ($K_{trans} = \frac{1}{2}Mv^2$) 和**轉動動能** ($K_{rot} = \frac{1}{2}I\omega^2$) 兩部分。
3.  **重要條件:** **無滑動 (no slipping)** 滾動意味著 $v = R\omega$，這個關係可以將平動與轉動聯繫起來。
4.  **思路解析:**
    *   建立能量守恆方程：$Mgh = \frac{1}{2}Mv^2 + \frac{1}{2}I\omega^2$。
    *   使用 $\omega = v/R$ 替換 $\omega$，使方程中只剩下一個未知速度 $v$。
    *   代數運算，整理出 $v$ 的通用表達式，例如：
        $$v^2 = \frac{2gh}{1 + I/(MR^2)}$$
    *   分別代入圓環 ($I = MR^2$) 和實心圓盤 ($I = \frac{1}{2}MR^2$) 的轉動慣量，求出它們各自到達底部的速度。
    *   **比較與解釋:** 速度較大者先到達。從公式可以看出，$I$ 越小的物體，$v$ 越大。這是因為更少的能量被分配到「轉動」上，從而有更多的能量用於「平動」。

Q7: 
Calculate the moment of inertia of a uniform solid cone about an axis through its center. 
The cone has mass M and altitude h. 
The radius of its circular base is R. 
(Hint: Break the cone into small disks and integrate over those disks).
A7:
1.  **核心觀念:** 再次使用**積分法**來求解複雜形狀的轉動慣量：
    $$I = \int dI$$
2.  **“切片”策略:** 按照提示，將圓錐體沿其對稱軸切成一系列無限薄的**圓盤 (disk)**。
3.  **思路解析:**
    *   **單個薄盤的轉動慣量 ($dI$):** 我們已知一個實心圓盤繞中心軸的轉動慣量是 $\frac{1}{2} \cdot (\text{質量}) \cdot (\text{半徑})^2$。因此，一個薄盤的轉動慣量為 $dI = \frac{1}{2} (dm) r^2$。
    *   **建立變數關係:** 
        *   在距離頂點 $x$ 處取一個厚度為 $dx$ 的薄盤。
        *   它的半徑 $r$ 和質量 $dm$ 都會隨 $x$ 變化。
        *   利用**相似三角形**，找出 $r$ 與 $x$ 的關係 ($r/x = R/h$)。
        *   利用圓錐的**體密度** $\rho$，找出 $dm$ 與 $x$ 的關係 ($dm = \rho \cdot dV = \rho \cdot (\pi r^2) \cdot dx$)。
    *   **建立積分:** 
        *   將 $r$ 和 $dm$ 的表達式（全部用 $x$ 表示）代入 $dI$ 的表達式中。
        *   你將得到一個只含 $x$ 和一堆常數的 $dI$ 表達式。
        *   最後，從頂點 ($x=0$) 到錐底 ($x=h$) 對 $dI$ 進行積分，即可得到整個圓錐的總轉動慣量 $I$。

TARGET DECK:

source url:

END