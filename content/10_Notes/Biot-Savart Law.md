---
aliases:
  - Biot-Savart Law
  - 必歐-沙伐定律
tags:
  - Physics
up:
  - "[[磁場]]"
related:
  - "[[安培定律]]"
  - "[[電流]]"
annotation: 介紹計算電流產生磁場的基本定律，提供微元電流源與空間磁場點的數學關係，是分析複雜幾何形狀電流磁場的基礎。
---

# 必歐-沙伐定律 (Biot-Savart Law)

**必歐-沙伐定律** 是靜磁學中的基本定律，描述了穩恆電流產生的磁場強度與電流元之間的定量關係。它在磁學中的地位相當於電學中的 [[庫倫定律]]。

---

## 1. 基本定義 (Fundamental Formula)

考慮一條載有電流 $I$ 的導線，其中的一個微小長度元（電流元）為 $d\mathbf{l}$。在距離該電流元為 $\mathbf{r}$ 的空間某點產生的微元磁場 $d\mathbf{B}$ 為：
$$d\mathbf{B} = \frac{\mu_0}{4\pi} \frac{I d\mathbf{l} \times \hat{\mathbf{r}}}{r^2}$$
其中：
- $\mu_0 = 4\pi \times 10^{-7} \text{ T}\cdot\text{m/A}$ 為 **真空磁導率**。
- $\hat{\mathbf{r}}$ 是從電流元指向觀察點的單位向量。
- 方向遵循向量外積的 **右手定則**。

若要求整條導線產生的總磁場，則需進行向量積分：
$$\mathbf{B} = \int d\mathbf{B} = \frac{\mu_0 I}{4\pi} \int \frac{d\mathbf{l} \times \hat{\mathbf{r}}}{r^2}$$

---

## 2. 典型幾何形狀的應用

### (1) 長直導線 (Straight Wire)
對於一條有限長的載流導線，在距離為 $R$ 的點產生的磁場大小為：
$$B = \frac{\mu_0 I}{4\pi R} (\sin\theta_1 + \sin\theta_2)$$
- **無限長導線極限**：當導線趨向無限長時（$\theta_1, \theta_2 \to \pi/2$）：
  $$B = \frac{\mu_0 I}{2\pi R}$$
  *此結果亦可利用 [[安培定律]] 快速求得。*

### (2) 圓弧形與圓環導線 (Circular Loop)
考慮半徑為 $R$ 的圓弧導線，在圓心處產生的磁場：
- **圓弧 (角度 $\phi$)**：由於 $d\mathbf{l} \perp \mathbf{r}$，積分簡化為：
  $$B = \frac{\mu_0 I \phi}{4\pi R}$$
- **完整圓環 ($\phi = 2\pi$)**：
  $$B = \frac{\mu_0 I}{2 R}$$

---

## 3. 與安培定律的對比

| 特性 | 必歐-沙伐定律 | [[安培定律]] |
| :--- | :--- | :--- |
| **數學形式** | 微分/積分式 | 線積分式 (環路積分) |
| **適用範圍** | 任何穩恆電流分布 | 具備高對稱性的電流分布 |
| **物理意象** | 「點源」疊加而成 | 場的「環流量」與淨電流關係 |
# 荷姆霍茲雙線圈（Helmholtz Coil）$d=R$ 條件與中心磁場推導

>[[實驗報告-電腦化賀姆霍茲線圈磁場實驗]]

## 一、 單個圓形線圈的軸向磁場

根據**畢奧-沙伐定律（Biot-Savart Law）**，一個半徑為 $R$、通有電流 $I$、總匝數為 $N$ 的圓形線圈，在其中心軸（設為 $z$ 軸）上距離線圈圓心 $z'$ 處所產生的磁場 $B$ 為：

$$B(z') = \frac{\mu_0 N I R^2}{2(z'^2 + R^2)^{3/2}}$$

其中 $\mu_0$ 為真空磁導率。

---

## 二、 雙線圈系統的磁場疊加

將兩個完全相同的線圈平行放置，並使它們的中心軸重合。
設系統的幾何中心點為座標原點 $z = 0$，兩個線圈之間的距離為 $d$。
* **線圈 1** 位於 $z = -\frac{d}{2}$
* **線圈 2** 位於 $z = +\frac{d}{2}$

在軸線上任意一點 $z$ 的總磁場 $B_{\text{total}}(z)$ 為兩線圈產生磁場的代數和：

$$B_{\text{total}}(z) = \frac{\mu_0 N I R^2}{2} \left[ \frac{1}{\left( (z + \frac{d}{2})^2 + R^2 \right)^{3/2}} + \frac{1}{\left( (z - \frac{d}{2})^2 + R^2 \right)^{3/2}} \right]$$

為了簡化數學表達式，定義常數 $C = \frac{\mu_0 N I R^2}{2}$：

$$B_{\text{total}}(z) = C \left[ \left( \left(z + \frac{d}{2}\right)^2 + R^2 \right)^{-3/2} + \left( \left(z - \frac{d}{2}\right)^2 + R^2 \right)^{-3/2} \right]$$

---

## 三、 泰勒展開與磁場均勻化條件

為了讓中心點（$z=0$）附近的磁場儘可能均勻，我們將總磁場函數 $B_{\text{total}}(z)$ 在 $z=0$ 處進行**泰勒級數展開（Taylor Series Expansion）**：

$$B_{\text{total}}(z) = B(0) + \left.\frac{dB}{dz}\right|_{z=0} z + \frac{1}{2!}\left.\frac{d^2B}{dz^2}\right|_{z=0} z^2 + \frac{1}{3!}\left.\frac{d^3B}{dz^3}\right|_{z=0} z^3 + \frac{1}{4!}\left.\frac{d^4B}{dz^4}\right|_{z=0} z^4 + \dots$$

### 1. 對稱性消去奇數階導數
由於雙線圈系統在 $z=0$ 兩側具有完全的對稱性，磁場函數 $B_{\text{total}}(z)$ 是一個**偶函數**（即 $B(z) = B(-z)$）。因此，所有在 $z=0$ 處的**奇數階導數必定為零**：
$$\left.\frac{dB}{dz}\right|_{z=0} = 0, \quad \left.\frac{d^3B}{dz^3}\right|_{z=0} = 0$$

### 2. 令二階導數為零（尋求極致均勻度）
要使 $z=0$ 周圍的磁場變化最平緩，我們必須消除最低階的非零變動項，即**令二階導數為零**：
$$\left.\frac{d^2B_{\text{total}}}{dz^2}\right|_{z=0} = 0$$

對 $B_{\text{total}}(z)$ 求一階與二階導數：

* **一階導數：**
  $$\frac{dB_{\text{total}}}{dz} = C \left( -\frac{3}{2} \right) \left[ \frac{2(z + \frac{d}{2})}{\left((z + \frac{d}{2})^2 + R^2\right)^{5/2}} + \frac{2(z - \frac{d}{2})}{\left((z - \frac{d}{2})^2 + R^2\right)^{5/2}} \right]$$

* **二階導數：**
  再對其求導，並將 $z=0$ 代入（此時兩項項相同，合併乘以 2）：
  $$\left.\frac{d^2B_{\text{total}}}{dz^2}\right|_{z=0} = -3C \left[ \frac{1}{\left((\frac{d}{2})^2 + R^2\right)^{5/2}} - \frac{5\left(\frac{d}{2}\right)^2}{\left((\frac{d}{2})^2 + R^2\right)^{7/2}} \right] \times 2$$

為了讓二階導數為 0，括號內部的分子與分母關係必須滿足：
$$1 - \frac{5\left(\frac{d}{2}\right)^2}{(\frac{d}{2})^2 + R^2} = 0$$

解此方程式：
$$\left(\frac{d}{2}\right)^2 + R^2 = 5\left(\frac{d}{2}\right)^2$$
$$R^2 = 4\left(\frac{d}{2}\right)^2$$
$$R^2 = d^2 \implies d = R$$

**結論：當線圈間距 $d$ 等於線圈半徑 $R$ 時，磁場的二階導數為零。此時中心點附近的磁場最為均勻。**

---

## 四、 中心點的最終磁場計算

將最優條件 $d = R$ 以及中心點 $z = 0$ 代入總磁場公式中：

$$B_{\text{center}} = B_{\text{total}}(0) = \frac{\mu_0 N I R^2}{2} \left[ \frac{1}{\left( (\frac{R}{2})^2 + R^2 \right)^{3/2}} + \frac{1}{\left( (-\frac{R}{2})^2 + R^2 \right)^{3/2}} \right]$$

$$B_{\text{center}} = \frac{\mu_0 N I R^2}{2} \cdot 2 \cdot \left( \frac{5}{4}R^2 \right)^{-3/2}$$

$$B_{\text{center}} = \mu_0 N I R^2 \cdot \left( \frac{4}{5R^2} \right)^{3/2}$$

$$B_{\text{center}} = \mu_0 N I R^2 \cdot \frac{8}{5\sqrt{5} R^3}$$

$$B_{\text{center}} = \left( \frac{4}{5} \right)^{3/2} \frac{\mu_0 N I}{R} = \frac{8}{5\sqrt{5}} \frac{\mu_0 N I}{R}$$

### 數值近似值
$$\frac{8}{5\sqrt{5}} \approx \frac{8}{5 \times 2.236} \approx 0.7155$$

$$B_{\text{center}} \approx 0.716 \frac{\mu_0 N I}{R}$$
