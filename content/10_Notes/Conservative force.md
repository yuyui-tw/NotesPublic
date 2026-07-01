---
tags:
  - Physics
up:
  - "[[Force]]"
related:
  - "[[Potential energy]]"
  - "[[Law of Conservation of mechanical energy]]"
annotation:
aliases:
  - 保守力
  - c.f.
---
# 主要定義 (Key Definitions)
保守力 (Conservative Force) 是指一種力,其所作的功只與物體的初末位置有關,而與其運動的路徑無關
這等價於以下兩種陳述:

1. **路徑無關性 (Path Independence)**
> 保守力沿任意兩點間作的功,其值與路徑無關
> $$ W_{A \to B} = \int_{A}^{B} \vec{F} \cdot d\vec{l} \text{ is independent of the path} $$

2. **封閉路徑功為零 (Zero Work over a Closed Loop)**
> 保守力沿任何封閉路徑 (起點與終點相同) 所作的總功為零
> $$ \oint \vec{F} \cdot d\vec{l} = 0 $$

# 位能與保守力 (Potential Energy & C.F.)
對於任何一個保守力,我們都可以定義一個與其對應的位能函數 (Potential Energy Function), $U$
保守力所作的功,等於其對應位能的**負**變化量
$$ W_c = -\Delta U = -(U_f - U_i) $$

反過來,保守力可以表示為其位能函數的負梯度 (negative gradient)
$$ \vec{F} = -\vec{\nabla}U $$
- 在一維情況下,可簡化為:
$$ F_x = -\frac{dU}{dx} $$
- 梯度 (Gradient, $\nabla$) 是一個指向函數變化率最大方向的向量算子

# 機械能守恆 (Conservation of Mechanical Energy)
當系統中只有保守力作功時,其總機械能將會守恆,這是保守力最重要的特性之一
更詳細的內容與推導,請見 [[Law of Conservation of mechanical energy]]

# 判斷方式 (Tests for a Conservative Force)
一個力場 $\vec{F}$ 是否為保守力,可以透過數學方式檢驗:
> **旋度為零 (Zero Curl)**
> 如果一個力場的旋度 (Curl) 處處為零,則該力場為保守力
> $$ \vec{\nabla} \times \vec{F} = 0 $$
- 旋度 (Curl, $\vec{\nabla} \times$) 是描述向量場在某點周圍旋轉趨勢的向量

# 範例 (Examples)
## 保守力 (Conservative Forces)
- **重力 (Gravitational Force)**
- **彈性力 (Elastic Spring Force)**, 遵循虎克定律
- **靜電力 (Electrostatic Force)**, 遵循庫倫定律

## 非保守力 (Non-conservative Forces)
- **摩擦力 (Friction)**
- **空氣阻力 (Air Resistance / Drag)**
- **繩子張力 (Tension)**
- 這些力作的功與路徑有關,且通常會將機械能轉換為熱能