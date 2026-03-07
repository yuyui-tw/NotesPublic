---
aliases:
  - 轉動動能
tags:
  - Physics
up:
  - "[[Rotational motion]]"
related:
  - "[[kinetic energy]]"
  - "[[Work-energy theorem]]"
annotation:
---
# 概要
轉動動能 (Rotational Kinetic Energy) 是物體因繞軸轉動而具有的能量。它與物體的**轉動慣量** ($I$) 和**角速度** ($\omega$) 的平方成正比，是線性動能 ($\frac{1}{2}mv^2$) 在轉動系統中的對應概念。

# 理論
### 轉動動能的推導
一個繞固定軸轉動的剛體，可以看作是無數個質點的集合。每個質點 $m_i$ 的切線速率為 $v_i = r_i\omega$。
系統的總動能是所有質點動能的總和：
$$ K_{total} = \sum \frac{1}{2}m_i v_i^2 = \sum \frac{1}{2}m_i (r_i\omega)^2 $$
由於角速度 $\omega$ 對於剛體上的每一個點都是相同的，可以提出：
$$ K_{total} = \frac{1}{2} (\sum m_i r_i^2) \omega^2 $$
括號中的項正是物體的轉動慣量 $I = \sum m_i r_i^2$。因此，轉動動能的公式為：
$$ K_{rot} = \frac{1}{2}I\omega^2 $$

### 力矩作功與轉動能量定理 (Work and Energy in Rotation)
力矩 ($\tau$) 對一個轉動的物體作功，會改變其轉動動能。
力矩作功的公式為：
$$ W = \int_{\phi_1}^{\phi_2} \tau d\phi $$
這引出了轉動版本的功-能定理：
$$ W_{net} = \Delta K_{rot} = \frac{1}{2}I\omega_f^2 - \frac{1}{2}I\omega_i^2 $$
淨力矩所作的功，等於物體轉動動能的變化量。

### 功率 (Power)
力矩作功的瞬時功率，等於力矩與角速度的乘積：
$$ P = \frac{dW}{dt} = \tau \omega $$

# 公式
### 轉動動能 (Rotational Kinetic Energy)
$$ K_{rot} = \frac{1}{2}I\omega^2 $$

### 滾動動能 (Rolling Kinetic Energy)
對於同時進行平移和轉動的物體（如滾動的輪子），其總動能為平移動能與轉動動能之和。
$$ K_{total} = K_{trans} + K_{rot} = \frac{1}{2}Mv_{cm}^2 + \frac{1}{2}I_{cm}\omega^2 $$

### 功與功率 (Work and Power)
- **力矩作功**: $W = \int \tau d\phi$
- **功率**: $P = \tau \omega$
- **轉動能量定理**: $W_{net} = \Delta K_{rot}$

