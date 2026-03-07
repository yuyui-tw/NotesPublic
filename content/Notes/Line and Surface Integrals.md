---
aliases:
  - 線積分與面積分
tags:
  - Physics
up:
  - "[[Integral]]"
related:
  - "[[梯度、散度、旋度]]"
annotation:
---
# 概要

線積分 (Line Integral) 與面積分 (Surface Integral) 是將 [[Integral|定積分]] 從一維的直線區間，推廣到更高維度幾何結構（**曲線**與**曲面**）上的積分方法。

它們是物理學和工程學中不可或缺的工具，用於計算沿著彎曲路徑的功、穿過一個曲面的流體通量等複雜問題。本筆記旨在定義這兩種積分，並為理解向量微積分三大定理奠定基礎。

# 核心概念

### 1. 線積分 (Line Integral)
線積分是在一條**曲線 $C$** 上對一個場（純量或向量）進行的積分。

- **純量線積分 $\int_C f\,ds$**
  - **定義**：將一個**純量函數 $f$** 沿著曲線 $C$ 的**弧長 $s$** 進行積分。
  - **直觀意義**：若 $f$ 代表在曲線路徑 $C$ 上方一個「圍籬」的高度，則此積分計算的是該**圍籬的總面積**。若 $f=1$，則結果為曲線 $C$ 的總長度。

- **向量線積分 $\int_C \mathbf{F} \cdot d\mathbf{r}$**
  - **定義**：將一個**向量場 $\mathbf{F}$** 的**切向分量**沿著曲線 $C$ 進行積分。
  - **直觀意義**：若 $\mathbf{F}$ 代表一個力場，則此積分計算的是力場推動一個物體沿路徑 $C$ 移動所做的**總功 (Work)**。若 $C$ 為封閉曲線，則稱為**環流量 (Circulation)**。

### 2. 面積分 (Surface Integral)
面積分是在一個**曲面 $\Sigma$** 上對一個場（純量或向量）進行的積分。

- **純量面積分 $\iint_\Sigma f\,dS$**
  - **定義**：將一個**純量函數 $f$** 在曲面 $\Sigma$ 的**面積 $S$** 上進行積分。
  - **直觀意義**：若 $f$ 代表一個薄殼曲面 $\Sigma$ 的**密度**，則此積分計算的是該**薄殼的總質量**。若 $f=1$，則結果為曲面 $\Sigma$ 的總面積。

- **向量面積分 (通量, Flux) $\iint_\Sigma \mathbf{F} \cdot d\mathbf{S}$**
  - **定義**：將一個**向量場 $\mathbf{F}$** 的**法向分量**在曲面 $\Sigma$ 上進行積分。這類積分常表示為 $\int \mathbf{F} \cdot d\mathbf{a}$ 或 $\int \mathbf{F} \cdot d\mathbf{S}$，其中 $d\mathbf{a}$ ($d\mathbf{S}$) 為**微分面積向量**，其方向為曲面的法線方向。
  - **範例**: 對於一個與 xz 平面平行，且法向量指向 $y$ 軸正向的微小面積元素，其微分面積向量可表示為 $d\mathbf{a} = dx\,dz\,\hat{j}$。
  - **直觀意義**：若 $\mathbf{F}$ 代表流體的向量速度場，則此積分計算的是單位時間內流體穿過曲面 $\Sigma$ 的**總通量 (Flux)**。可以將 $\int \mathbf{F} \cdot d\mathbf{a}$ 理解為流體通過該「單面」的淨流量。

# 結構/要素

下表總結了線積分與面積分在結構上的核心差異：

| 特性 | 線積分 (Line Integral) | 面積分 (Surface Integral) |
| :--- | :--- | :--- |
| **積分域** | 空間中的**曲線** $C$ (一維) | 空間中的**曲面** $\Sigma$ (二維) |
| **被積函數** | 純量函數 $f$ 或向量場 $\mathbf{F}$ | 純量函數 $f$ 或向量場 $\mathbf{F}$ |
| **積分微元** | `ds` (弧長微元) 或 `dr` (向量位移微元) | `dS` (面積微元) 或 `dS` (向量面積微元) |
| **計算轉換** | 轉換為對**單一參數 $t$** 的定積分 | 轉換為對**兩個參數 $(u, v)$** 的二重積分 |

# 計算方法

要實際計算線積分與面積分，核心步驟是將它們轉換為我們熟悉的**[[Integral|定積分]]**。這需要「參數化」曲線或曲面。

### 1. 純量線積分 (Scalar Line Integral)
**目標**：計算 $\int_C f\,ds$。

1.  **參數化曲線 $C$**：
    - 找到一個向量函數 $\mathbf{r}(t) = \langle x(t), y(t), z(t) \rangle$ 來描述這條曲線，其中參數 $t$ 在一個區間 $[a, b]$ 內變動。
    - 例如，一個在 xy 平面上、半徑為 $R$ 的圓，可以參數化為 $\mathbf{r}(t) = \langle R\cos(t), R\sin(t), 0 \rangle$，其中 $t \in [0, 2\pi]$。

2.  **計算弧長微元 $ds$**：
    - 首先計算 $\mathbf{r}(t)$ 的一階導數 $\mathbf{r}'(t) = \langle x'(t), y'(t), z'(t) \rangle$。
    - 然後計算其大小（速率）：$|\mathbf{r}'(t)| = \sqrt{(x'(t))^2 + (y'(t))^2 + (z'(t))^2}$。
    - 弧長微元 $ds$ 就是速率乘上時間微元：$ds = |\mathbf{r}'(t)|\,dt$。

3.  **轉換為定積分**：
    - 將 $f$ 中的 $x, y, z$ 替換為 $\mathbf{r}(t)$ 的分量 $x(t), y(t), z(t)$。
    - 將 $ds$ 替換為 $|\mathbf{r}'(t)|\,dt$。
    - 最終得到一個關於單一變數 $t$ 的[[Integral|定積分]]：
      $$ \int_C f(x,y,z)\,ds = \int_a^b f(x(t), y(t), z(t)) |\mathbf{r}'(t)|\,dt $$

### 2. 向量線積分 (Vector Line Integral)
**目標**：計算 $\int_C \mathbf{F} \cdot d\mathbf{r}$。

1.  **參數化曲線 $C$**：
    - 與純量線積分相同，用 $\mathbf{r}(t)$ 描述曲線，其中 $t \in [a, b]$。

2.  **計算位移向量微元 $d\mathbf{r}$**：
    - $d\mathbf{r}$ 代表沿曲線的無窮小位移向量。它等於切線向量 $\mathbf{r}'(t)$ 乘上時間微元 $dt$：
      $$ d\mathbf{r} = \mathbf{r}'(t)\,dt = \langle x'(t), y'(t), z'(t) \rangle\,dt $$

3.  **轉換為定積分**：
    - 將向量場 $\mathbf{F}$ 中的 $x, y, z$ 替換為 $\mathbf{r}(t)$ 的分量。
    - 計算 $\mathbf{F}(\mathbf{r}(t))$ 與 $\mathbf{r}'(t)$ 的點積。
    - 最終得到一個關於 $t$ 的[[Integral|定積分]]：
      $$ \int_C \mathbf{F} \cdot d\mathbf{r} = \int_a^b \mathbf{F}(\mathbf{r}(t)) \cdot \mathbf{r}'(t)\,dt $$

### 3. 純量面積分 (Scalar Surface Integral)
**目標**：計算 $\iint_\Sigma f\,dS$。這需要將其轉為**二重積分**，也就是對兩個變數的**迭代[[Integral|積分]]**。

1.  **參數化曲面 $\Sigma$**：
    - 找到一個使用兩個參數 $(u, v)$ 的向量函數 $\mathbf{r}(u,v) = \langle x(u,v), y(u,v), z(u,v) \rangle$ 來描述曲面。這兩個參數在某個二維區域 $D$ 內變動。
    - 例如，一個半徑為 $R$ 的球面，可參數化為 $\mathbf{r}(\phi, \theta) = \langle R\sin\phi\cos\theta, R\sin\phi\sin\theta, R\cos\phi \rangle$，其中 $(\phi, \theta)$ 在區域 $D = [0, \pi] \times [0, 2\pi]$ 內。

2.  **計算面積微元 $dS$**：
    - 計算 $\mathbf{r}(u,v)$ 對 $u$ 和 $v$ 的偏導數：$\mathbf{r}_u$ 和 $\mathbf{r}_v$。
    - 計算這兩個向量的叉積 $\mathbf{r}_u \times \mathbf{r}_v$，這個新向量垂直於曲面。
    - 計算叉積的大小 $|\mathbf{r}_u \times \mathbf{r}_v|$。
    - 面積微元 $dS$ 就是這個大小乘上 $u,v$ 平面上的微小面積 $dA$：$dS = |\mathbf{r}_u \times \mathbf{r}_v|\,dA$。

3.  **轉換為二重積分**：
    - 將 $f$ 中的 $x, y, z$ 替換為 $\mathbf{r}(u,v)$ 的分量。
    - 最終得到一個在區域 $D$ 上對 $u,v$ 的二重積分：
      $$ \iint_\Sigma f\,dS = \iint_D f(\mathbf{r}(u,v)) |\mathbf{r}_u \times \mathbf{r}_v|\,dA $$
    - 這個二重積分通過**迭代積分**來計算，例如 $\int_c^d \int_a^b g(u,v)\,du\,dv$，代表先對 $u$ 積分，再將結果對 $v$ 積分。

### 4. 向量面積分 (Vector Surface Integral)
**目標**：計算通量 $\iint_\Sigma \mathbf{F} \cdot d\mathbf{S}$。

1.  **參數化曲面 $\Sigma$**：
    - 與純量面積分相同，用 $\mathbf{r}(u,v)$ 描述曲面。

2.  **計算有向面積微元 $d\mathbf{S}$**：
    - $d\mathbf{S}$ 是一個向量，其方向是曲面的法線方向，大小是面積微元。
    - 它等於叉積向量 $\mathbf{r}_u \times \mathbf{r}_v$ 乘上 $dA$：
      $$ d\mathbf{S} = (\mathbf{r}_u \times \mathbf{r}_v)\,dA $$
    - **重要**：叉積的順序 $(\mathbf{r}_u \times \mathbf{r}_v)$ 或 $(\mathbf{r}_v \times \mathbf{r}_u)$ 決定了法向量的方向（例如「向外」或「向內」）。必須根據題目要求選擇正確的方向。

3.  **轉換為二重積分**：
    - 將向量場 $\mathbf{F}$ 中的 $x, y, z$ 替換為 $\mathbf{r}(u,v)$ 的分量。
    - 計算 $\mathbf{F}(\mathbf{r}(u,v))$ 與 $(\mathbf{r}_u \times \mathbf{r}_v)$ 的點積。
    - 最終得到一個在區域 $D$ 上的二重積分：
      $$ \iint_\Sigma \mathbf{F} \cdot d\mathbf{S} = \iint_D \mathbf{F}(\mathbf{r}(u,v)) \cdot (\mathbf{r}_u \times \mathbf{r}_v)\,dA $$

# 原理/推導

### 性質與關鍵差異

1.  **線性性質**：兩者都滿足線性性質，即 $\int (a\mathbf{F} + b\mathbf{G}) = a\int\mathbf{F} + b\int\mathbf{G}$。

2.  **方向依賴性 (Orientation Dependence)**：這是兩者最重要的差異之一。
    - **向量積分**（功、環流量、通量）的結果**強烈依賴方向**。
        - 線積分：反轉路徑 $C$ 的方向，結果會變號。$\int_{-C}\mathbf{F}\cdot d\mathbf{r} = -\int_{C}\mathbf{F}\cdot d\mathbf{r}$。
        - 面積分：必須為曲面 $\Sigma$ 指定一個法向量方向（如「外側」或「內側」），選擇相反的法向量會使結果變號。
    - **純量積分**（弧長、圍籬面積、曲面質量）的結果**與方向無關**。

3.  **路徑獨立性 (Path Independence)**：
    - 僅適用於**向量線積分**。若向量場 $\mathbf{F}$ 為**保守場**（即 $\mathbf{F} = \nabla f$），則其線積分與路徑無關，僅取決於起點和終點。在這種情況下，沿任何封閉曲線的線積分（環流量）恆為零。

### 與三大積分定理的聯繫
線積分與面積分並非孤立，它們是更高維度積分定理的基石。這些定理揭示了 [[梯度、散度、旋度]] 中討論的微分算子（散度、旋度）與積分之間的深刻聯繫，共同構成了向量微積分的統一理論框架：

- **[[格林定理]]**：在**平面**上，將**封閉線積分**（環流量）與其圍成**區域**的**二重積分**聯繫起來。
- **[[斯托克斯定理]]**：在**三維空間**中，將**封閉線積分**（環流量）與其跨過的**曲面**上**旋度的面積分**聯繫起來。
- **[[散度定理]]**：在**三維空間**中，將**封閉面積分**（通量）與其圍成**體積**的**三重積分**聯繫起來。

這些定理本質上都是廣義斯托克斯定理的不同表現形式，體現了微積分基本定理在高維空間的推廣。
