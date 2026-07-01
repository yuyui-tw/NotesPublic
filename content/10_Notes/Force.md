---
tags:
  - Physics
up:
related: "[[2D motion]]"
aliases: 力
annotation: 作用於質點之力
---

# 力的基本概念 (Force)

在物理學中，力是一種導致物體運動狀態發生改變的交互作用
簡而言之，力可以使有質量的物體加速
力是一個向量，同時具有量值和方向

- **單位**
  在國際單位制(SI)中，力的單位是牛頓(Newton, N)
  其定義為使一公斤(kg)的物體，產生 1 $m/s^2$ 加速度所需的力
  ($1 N = 1 kg \cdot m/s^2$)
  相關單位可參考 [[Units]]

## 牛頓運動定律 (Newton's Laws of Motion)

牛頓的三大運動定律是古典力學的基石，描述了力與運動之間的關係

### 第一定律：慣性定律 (Law of Inertia)
> "An object at rest stays at rest and an object in motion stays in motion with the same speed and in the same direction unless acted upon by an unbalanced force."

若一個物體未受任何外力，或所受外力之向量合為零，則其將保持靜止或等速直線運動
這即是物體的**慣性**

### 第二定律：加速度定律 (Law of Acceleration)
> "The net force on an object is equal to the mass of the object multiplied by its acceleration."

物體所受的**淨力** ($\vec{F}_{net}$)，等於其質量(m)與加速度($\vec{a}$)的乘積
$$ \vec{F}_{net} = m\vec{a} $$
- **淨力 (Net Force)**
  是作用在單一物體上所有力的向量總和，也稱為合力(Resultant Force)
  力的疊加符合向量加法，即 $\vec{F}_{net} = \sum \vec{F}_i$
- 此定律是連結力(原因)，與運動狀態改變(結果)的核心

### 第三定律：作用與反作用定律 (Law of Action and Reaction)
> "For every action, there is an equal and opposite reaction."

當兩個物體交互作用時，彼此施加於對方的力，量值相等，方向相反，且作用在同一直線上

- **重要特性**
  作用力與反作用力，分別作用在**不同**的物體上，因此**不可互相抵銷**
- **範例**
  當你的手推牆壁時(作用力)，牆壁也同時以等大反向的力，推你的手(反作用力)

## 自由體圖 (Free-Body Diagram)

自由體圖是解決力學問題時一個極為重要的工具
它將所關注的單一物體分離出來，並以向量箭頭畫出所有作用在**該物體**上的外力

- **目的**
  視覺化所有力的分佈，以利正確應用牛頓第二定律($\sum \vec{F} = m\vec{a}$)
- **繪製原則**
  只畫作用在該物體上的力，不畫該物體施加給其他物體的力

## 常見力的類型

### 非接觸力 (Non-contact Forces) / 場力 (Field Forces)
物體無需接觸即可感受到的力，通常透過「場」來傳遞，這主要對應到宇宙中的四種基本力

- **重力 (Gravity)**
  具質量的物體之間的吸引力，在地球表面附近，其近似值為 $\vec{F}_g = m\vec{g}$
- **電磁力 (Electromagnetic Force)**
  帶電粒子之間的力，包括靜電力和磁力
- **弱核力 (Weak Nuclear Force)**
  是引起放射性衰變(如 β衰變)的力，作用尺度極短
- **強核力 (Strong Nuclear Force)**
  能將夸克結合為質子和中子，並將質子和中子束縛在原子核內，是四種力中最強的(作用尺度大於弱核力)

### 接觸力 (Contact Forces)
需要透過物體表面，直接接觸才能產生的力

- **正向力 (Normal Force, $\vec{N}$)**
  是接觸面為防止物體穿透，而施加的**垂直於接觸面**的支持力
  其量值不一定等於物體的重量，而是取決於具體的運動情況
- **摩擦力 (Friction, $\vec{f}$)**
  平行於接觸面，抵抗物體相對運動，或相對運動趨勢的力
    - **靜摩擦力 ($f_s$)**
      是物體靜止時的摩擦力，其量值會隨外力變化，但有一最大值：$f_{s,max} = \mu_s N$，其中 $\mu_s$ 為靜摩擦係數
    - **動摩擦力 ($f_k$)**
      是物體運動時的摩擦力，其量值通常為一定值，$f_k = \mu_k N$，其中 $\mu_k$ 為動摩擦係數，一般而言 $\mu_k \le \mu_s$
- **張力 (Tension, $\vec{T}$)**
  是透過繩索、纜線等傳遞的拉力，繩索中每一點的張力，被假設為大小相等
- **彈簧力 (Spring Force, $\vec{F}_s$)**
  是彈簧因形變而產生的力，在理想彈性限度內，其大小遵循**虎克定律(Hooke's Law)**
  $$ \vec{F}_s = -k\vec{x} $$
  其中 k 是彈簧常數，$\vec{x}$ 是彈簧相對於其平衡位置的位移，負號表示回復力的方向永遠與位移方向相反
