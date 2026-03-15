---
aliases:
  - 瑕積分
  - Improper Integral
tags:
  - Math
up: "[[definite integral|定積分]]"
related:
  - "[[數列與級數]]"
  - "[[正項級數]]"
  - "[[羅必達法則]]"
annotation: 處理無窮區間或無界函數的積分擴充
---

# 概要 (Overview)
**瑕積分 (Improper Integrals)** 透過 **極限 (Limit)** 處理不滿足黎曼積分前提（區間閉且函數有界）的情況。

1. **第一型 (Type I)**：積分區間無窮（如 $[a, \infty)$）。
2. **第二型 (Type II)**：函數在區間內存在奇點（Singularity）。

# 核心概念 (Core Concepts)
- **收斂 (Convergent)**：極限存在且有限。
- **發散 (Divergent)**：極限趨向 $\pm\infty$ 或不存在。
- **比較法 (Comparison Tests)**：利用已知基準（如 p-test）判定未知函數。

# 結構/要素 (Structure/Elements)

### 積分 p-測試 (p-Test for Integrals)
| 形式                                                    | 收斂條件           | 證明簡述 (Integral Test)                               |
| :---------------------------------------------------- | :------------- | :------------------------------------------------- |
| **標準型**：$\int_{1}^{\infty} \frac{1}{x^p} dx$          | **$p > 1$** 收斂 | $[\frac{x^{1-p}}{1-p}]_{1}^{\infty}$ 在 $p>1$ 時有界   |
| **對數分子型**：$\int_{e}^{\infty} \frac{\ln x}{x^p} dx$    | **$p > 1$** 收斂 | $\ln x \ll x^\epsilon$，利用比較法轉化為標準型                 |
| **對數分母型**：$\int_{e}^{\infty} \frac{1}{x(\ln x)^p} dx$ | **$p > 1$** 收斂 | 令 $u = \ln x$，轉化為 $\int_1^\infty \frac{1}{u^p} du$ |

> [!IMPORTANT] 級數連結
> 以上積分形式分別對應級數 $\sum \frac{1}{n^p}$, $\sum \frac{\ln n}{n^p}$, $\sum \frac{1}{n(\ln n)^p}$。透過**積分審斂法**，級數與對應積分具有相同斂散性。

# 原理/推導 (Principles/Derivation)

### 1. 積分審斂法證明 p-Test
對於 $f(x) \ge 0$ 且單調遞減，$\sum_{n=k}^\infty f(n)$ 與 $\int_k^\infty f(x)dx$ 同斂散。

- **針對 $\frac{1}{x^p}$**：
  $\int_1^\infty x^{-p} dx = \lim_{t \to \infty} \left[ \frac{x^{-p+1}}{-p+1} \right]_1^t$ (當 $p \ne 1$)。
  若 $1-p < 0 \implies p > 1$，極限為 $\frac{1}{p-1}$ (收斂)；若 $p < 1$，極限為 $\infty$ (發散)。
  若 $p=1$，$\int_1^\infty \frac{1}{x} dx = \ln x |_1^\infty = \infty$ (發散)。

- **針對 $\frac{\ln x}{x^p}$**：

  **Case 1：$p = 1$**
  利用變數變換，令 $u = \ln x, du = \frac{1}{x} dx$：
  $$\int_{e}^{\infty} \frac{\ln x}{x} dx = \left. \frac{1}{2}(\ln x)^2 \right|_{e}^{\infty} = \infty \text{ (發散)}$$

  **Case 2：$p \neq 1$**
  使用分部積分法 (Integration by Parts)：
  令 $u = \ln x \implies du = \frac{1}{x} dx$
  令 $dv = x^{-p} dx \implies v = \frac{x^{1-p}}{1-p}$

  $$\int \frac{\ln x}{x^p} dx = \frac{x^{1-p} \ln x}{1-p} - \int \frac{x^{1-p}}{1-p} \cdot \frac{1}{x} dx$$
  $$= \frac{\ln x}{(1-p)x^{p-1}} - \frac{1}{1-p} \int x^{-p} dx$$
  $$= \frac{\ln x}{(1-p)x^{p-1}} - \frac{1}{(1-p)^2 x^{p-1}} + C$$

  分析極限 ($x \to \infty$)：
  1. 若 **$p > 1$**：
     則 $p-1 > 0$，由羅必達法則知 $\lim_{x \to \infty} \frac{\ln x}{x^{p-1}} = 0$。
     且 $\lim_{x \to \infty} \frac{1}{x^{p-1}} = 0$。
     故積分收斂於 $\frac{1}{(p-1)^2}$。
  2. 若 **$p < 1$**：
     則 $1-p > 0$，分母趨向 $0$ 或分子 $x^{1-p}$ 趨向 $\infty$。
     故積分發散。

  **結論**：此形式收斂 $\iff p > 1$。

- **針對 $\frac{1}{x(\ln x)^p}$**：
  令 $u = \ln x \implies du = \frac{1}{x} dx$。
  $\int_e^\infty \frac{1}{x(\ln x)^p} dx = \int_1^\infty \frac{1}{u^p} du$。
  此即回歸標準型 $p$-test，當 $p > 1$ 時收斂。

### 2. 比較等級
增長速率：$\ln x \ll x^p \ll e^x$。此等級關係決定了分子分母對決時的斂散方向。
