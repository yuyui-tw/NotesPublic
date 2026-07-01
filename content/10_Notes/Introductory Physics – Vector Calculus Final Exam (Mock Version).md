---
tags:
  - QuizReview
---
title: Introductory Physics – Vector Calculus Final Exam Review
content:

TARGET DECK: Physics::Vector Calculus

source url: 

---

# Q1: **Problem 1: Physical Meaning**

Clearly explain the physical meaning of the following vector operations:
(a) Gradient
(b) Divergence
(c) Curl
A1: 
(a) **梯度 (Gradient)**:
純量場中，梯度指向數值上升最快的方向。
其大小代表該方向的變化率，方向與等位面垂直。

(b) **散度 (Divergence)**:
描述向量場在某點的發散或收斂程度。
若散度 > 0，代表該點為「源」(source)，有淨流出。
若散度 < 0，代表該點為「匯」(sink)，有淨流入。
若散度 = 0，代表此場為不可壓縮場 (incompressible)。

(c) **旋度 (Curl)**:
描述向量場在某點的旋轉趨勢與強度。
旋度向量的方向為旋轉軸，可由右手定則判斷。
若旋度 = 0，代表此場為無旋場 (irrotational)。

---

# Q2: **Problem 2: Gradient**

Given the scalar field $φ(x, y, z) = x²y + yz³ – 4xz$, compute the gradient $\nabla φ$.
A2: 
計算 $φ$ 對 $x, y, z$ 的偏導數：
$$ \frac{\partial φ}{\partial x} = 2xy - 4z $$
$$ \frac{\partial φ}{\partial y} = x^2 + z^3 $$
$$ \frac{\partial φ}{\partial z} = 3yz^2 - 4x $$

梯度 $\nabla φ$ 即為上述偏導數組成的向量：
$$ \nabla φ = (2xy - 4z, x^2 + z^3, 3yz^2 - 4x) $$

---

# Q3: **Problem 3: Divergence**

Given the vector field $\vec{F}(x, y, z) = (xy²)\hat{i} + (z² – x)\hat{j} + (e^{xy})\hat{k}$, compute the divergence $\nabla \cdot \vec{F}$.
A3: 
散度是將向量場各分量對其對應變數做偏導後相加：
$$ \nabla \cdot \vec{F} = \frac{\partial(xy²)}{\partial x} + \frac{\partial(z²–x)}{\partial y} + \frac{\partial(e^{xy})}{\partial z} $$

分別計算每一項：
$$ = y^2 + 0 + 0 $$
$$ = y^2 $$

---

# Q4: **Problem 4: Curl**

Given the vector field $\vec{A}(x, y, z) = (x² - y)\hat{i} + (3z + xy)\hat{j} + (y²)\hat{k}$, compute the curl $\nabla \times \vec{A}$.
A4: 
使用旋度的行列式公式計算：
$$ \nabla \times \vec{A} = \begin{vmatrix} \hat{i} & \hat{j} & \hat{k} \\ \frac{\partial}{\partial x} & \frac{\partial}{\partial y} & \frac{\partial}{\partial z} \\ x^2-y & 3z+xy & y^2 \end{vmatrix} $$

x-分量: $\frac{\partial(y^2)}{\partial y} - \frac{\partial(3z+xy)}{\partial z} = 2y - 3$
y-分量: $\frac{\partial(x^2-y)}{\partial z} - \frac{\partial(y^2)}{\partial x} = 0 - 0 = 0$
z-分量: $\frac{\partial(3z+xy)}{\partial x} - \frac{\partial(x^2-y)}{\partial y} = y - (-1) = y + 1$

組合後可得旋度 $\nabla \times \vec{A}$：
$$ \nabla \times \vec{A} = (2y - 3, 0, y + 1) $$

---

# Q5: **Problem 5: Vector Orthogonality**

Let $\vec{a}=(2,-1,4)$, $\vec{b}=(1,0,-2)$, $\vec{c}=(3,1,k)$.
(a) Determine whether $\vec{a}$ and $\vec{b}$ are orthogonal.
(b) Find the value of $k$ such that $\vec{c}$ is orthogonal to both $\vec{a}$ and $\vec{b}$.
A5: 
(a) 計算向量 $\vec{a}$ 與 $\vec{b}$ 的內積：
$$ \vec{a} \cdot \vec{b} = (2)(1) + (-1)(0) + (4)(-2) = 2 - 8 = -6 $$
因為內積不為 0，所以兩向量不互相垂直。

(b) 若 $\vec{c}$ 同時垂直於 $\vec{a}$ 和 $\vec{b}$，則需滿足 $\vec{c} \cdot \vec{a}=0$與 $\vec{c} \cdot \vec{b}=0$。
$$ \vec{c} \cdot \vec{a} = (3)(2) + (1)(-1) + (k)(4) = 5 + 4k = 0 \implies k = -\frac{5}{4} $$
$$ \vec{c} \cdot \vec{b} = (3)(1) + (1)(0) + (k)(-2) = 3 - 2k = 0 \implies k = \frac{3}{2} $$
$k$ 值無法同時滿足兩個條件，因此不存在這樣的 $k$ 值。

---

# Q6: **Problem 6: Gauss' Divergence Theorem**

Consider $\vec{F}=(x,y,z)$ and a sphere of radius $R$ centered at the origin. Verify Gauss' Divergence Theorem $\oint \vec{F}\cdot d\vec{S} = \iiint (\nabla\cdot \vec{F})dV$.
A6: 
**體積分 (Volume Integral)**:
1. 計算 $\vec{F}$ 的散度:
   $$ \nabla \cdot \vec{F} = \frac{\partial x}{\partial x} + \frac{\partial y}{\partial y} + \frac{\partial z}{\partial z} = 3 $$
2. 對球體體積 $V$ 積分:
   $$ \iiint_V (\nabla \cdot \vec{F}) dV = \iiint_V 3 dV = 3 \times (\frac{4}{3}\pi R^3) = 4\pi R^3 $$

**面積分 (Surface Integral)**:
1. 在球面上, $\vec{F}$與面法向量 $\vec{n}$皆沿徑向，兩者平行。
2. 計算 $\vec{F} \cdot \vec{n}$：
   $$ \vec{F} \cdot \vec{n} = |\vec{F}| = \sqrt{x^2+y^2+z^2} = R $$
3. 對球面面積 $S$ 積分:
   $$ \oint_S (\vec{F} \cdot \vec{n}) dS = \oint_S R dS = R \times (4\pi R^2) = 4\pi R^3 $$

兩邊結果均為 $4\pi R^3$，高斯散度定理成立。

---

# Q7: **Problem 7: Stokes' Theorem**

Let $\vec{F}=(-y,x,0)$ and $C$ be a circle of radius $a$ in the xy-plane. Verify Stokes' Theorem $\oint_C \vec{F}\cdot d\vec{r} = \iint_S (\nabla\times\vec{F})\cdot d\vec{S}$.
A7: 
**線積分 (Line Integral)**:
1. 將路徑 $C$ 參數化: $\vec{r}(t) = (a \cos(t), a \sin(t), 0)$，則 $d\vec{r} = (-a \sin(t), a \cos(t), 0) dt$。
2. $\vec{F}$ 在路徑 $C$ 上為 $(-a \sin(t), a \cos(t), 0)$。
3. 計算內積 $\vec{F} \cdot d\vec{r}$: $a^2\sin^2(t) + a^2\cos^2(t) = a^2$。
4. 沿路徑積分: 
   $$ \oint_C \vec{F} \cdot d\vec{r} = \int_{0}^{2\pi} a^2 dt = 2\pi a^2 $$

**面積分 (Surface Integral)**:
1. 計算 $\vec{F}$ 的旋度: 
   $$ \nabla \times \vec{F} = (0, 0, \frac{\partial x}{\partial x} - \frac{\partial(-y)}{\partial y}) = (0, 0, 2) $$
2. 曲面 $S$ 是 xy 平面上的圓盤，其法向量 $d\vec{S} = (0,0,1)dA$。
3. 計算內積 $(\nabla \times \vec{F}) \cdot d\vec{S}$: $(0,0,2) \cdot (0,0,1)dA = 2dA$。
4. 積分: 
   $$ \iint_S (\nabla \times \vec{F}) \cdot d\vec{S} = \iint_S 2dA = 2 \times (\pi a^2) = 2\pi a^2 $$

兩邊結果均為 $2\pi a^2$，斯托克斯定理成立。

---

# Q8: **Problem 8: Force from a Potential**

Given potential $φ = x²+2y²+3z²-xy+yz$, find the force $\vec{F}=-\nabla φ$ and evaluate it at $P(1,-1,2)$. Find its magnitude and direction.
A8: 
1. 計算 $φ$ 的梯度 $\nabla φ$:
   $$ \nabla φ = (\frac{\partial φ}{\partial x}, \frac{\partial φ}{\partial y}, \frac{\partial φ}{\partial z}) = (2x-y, 4y-x+z, 6z+y) $$
2. 計算力場 $\vec{F} = -\nabla φ$:
   $$ \vec{F} = (-2x+y, -4y+x-z, -6z-y) $$
3. 將點 $P(1,-1,2)$ 代入:
   $$ \vec{F} = (-2(1)+(-1), -4(-1)+1-2, -6(2)-(-1)) = (-3, 3, -11) $$
4. 計算大小 (magnitude):
   $$ |\vec{F}| = \sqrt{(-3)^2+3^2+(-11)^2} = \sqrt{9+9+121} = \sqrt{139} $$
5. 計算方向 (unit vector):
   $$ \frac{1}{\sqrt{139}}(-3, 3, -11) $$

---

# Q9: **Problem 9: Electric Flux and Gauss' Law**

Consider $\vec{E} = k\frac{\vec{r}}{r^3}$. Let $S$ be a sphere of radius $R$. Compute the electric flux $\oint_S \vec{E}\cdot d\vec{S}$ and relate the result to Gauss' Law.
A9: 
1. 在半徑為 $R$ 的球面上，電場 $\vec{E}$ 為 $\vec{E} = \frac{k}{R^2} \hat{r}$ (其中 $\hat{r}$ 是徑向單位向量^[描述物體相對於某中心點（原點）**徑向（由中心向外）方向上的單位長度向量**])。
2. 球面上的面積元 $d\vec{S}$ 可寫為 $\hat{r} dS$。
3. 計算 $\vec{E} \cdot d\vec{S}$: 
   $$ \vec{E} \cdot d\vec{S} = (\frac{k}{R^2} \hat{r}) \cdot (\hat{r} dS) = \frac{k}{R^2} dS $$
4. 計算總電通量 $\Phi$ (對整個球面積分):
   $$ \Phi = \oint_S \frac{k}{R^2} dS = \frac{k}{R^2} \times (4\pi R^2) = 4\pi k $$

根據高斯定律^[高斯定律是物理學中描述電場與電荷關係的基本定律，核心概念是：穿越任何一個閉合曲面（稱為高斯曲面）的電場總通量，等於該曲面所包圍的淨電荷量除以真空介電常數$\epsilon_0$]，電通量 $\Phi = \frac{Q_{enclosed}}{\epsilon_0}$。
比較兩式可得 $4\pi k = \frac{Q_{enclosed}}{\epsilon_0}$，因此 $k = \frac{Q_{enclosed}}{4\pi\epsilon_0}$。此結果將常數 $k$ 與源電荷 $Q_{enclosed}$ 連結起來。

---

# Q10: **Problem 10: Velocity Field Analysis**

Given $\vec{v} = (xz)\hat{i} + (3y²)\hat{j} + (x+y)\hat{k}$ and $T = x² + yz$.
(a) Compute $|v|$
(b) Compute $\nabla\cdot\vec{v}$
(c) Compute $\nabla\times\vec{v}$
(d) Compute $\nabla T$
A10: 
(a) **速度大小**:
$$ |\vec{v}| = \sqrt{(xz)^2 + (3y^2)^2 + (x+y)^2} = \sqrt{x^2z^2 + 9y^4 + (x+y)^2} $$

(b) **散度**:
$$ \nabla \cdot \vec{v} = \frac{\partial(xz)}{\partial x} + \frac{\partial(3y^2)}{\partial y} + \frac{\partial(x+y)}{\partial z} = z + 6y $$

(c) **旋度**:
$$ \nabla \times \vec{v} = (\frac{\partial(x+y)}{\partial y} - \frac{\partial(3y^2)}{\partial z}, \frac{\partial(xz)}{\partial z} - \frac{\partial(x+y)}{\partial x}, \frac{\partial(3y^2)}{\partial x} - \frac{\partial(xz)}{\partial y}) $$
$$ = (1-0, x-1, 0-0) = (1, x-1, 0) $$
**注意**: 此計算結果與參考答案的 $(-1,0,x)$ 不同。

(d) **溫度梯度**:
$$ \nabla T = (\frac{\partial T}{\partial x}, \frac{\partial T}{\partial y}, \frac{\partial T}{\partial z}) = (2x, z, y) $$
