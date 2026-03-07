---
aliases:
  - 瑕積分
tags:
  - Math
up:
  - "[[definite integral|定積分]]"
related:
  - "[[羅必達法則]]"
  - "[[limit and continuty]]"
annotation: 處理無窮區間或無界函數的積分擴充
---

# 概要 (Overview)
**瑕積分 (Improper Integrals)** 是定積分概念的延伸。主要處理傳統定積分定義（在有限區間內積分連續函數）無法直接應用的情況，核心在於將 **極限 (Limit)** 引入積分運算中，用來處理邊界或函數值趨向無窮大的特殊情況。

主要分為兩類：
1. **第一型瑕積分 (Type I)**：積分區間為無窮大（無窮區間 Infinite Intervals）。
2. **第二型瑕積分 (Type II)**：函數在積分區間內不連續（無界函數 Discontinuous Integrands），通常存在垂直漸近線 (Vertical Asymptote)。

# 核心概念 (Core Concepts)

### 1. 第一型：無窮區間 (Infinite Intervals)
當上限或下限包含 $\pm\infty$ 時，將該端點替換為變數並取極限：
- $\int_{a}^{\infty} f(x) \, dx = \lim_{b \to \infty} \int_{a}^{b} f(x) \, dx$
- $\int_{-\infty}^{b} f(x) \, dx = \lim_{a \to -\infty} \int_{a}^{b} f(x) \, dx$
- $\int_{-\infty}^{\infty} f(x) \, dx = \int_{-\infty}^{c} f(x) \, dx + \int_{c}^{\infty} f(x) \, dx$ （需兩者皆收斂才算收斂）

### 2. 第二型：無界函數 (Discontinuous Integrands)
當函數在點 $c$ 處不連續（奇點 Singularity）時：
- 若在左端點 $a$：$\int_{a}^{b} f(x) \, dx = \lim_{t \to a^+} \int_{t}^{b} f(x) \, dx$
- 若在右端點 $b$：$\int_{a}^{b} f(x) \, dx = \lim_{t \to b^-} \int_{a}^{t} f(x) \, dx$
- 若在區間內一點 $c$：$\int_{a}^{b} f(x) \, dx = \int_{a}^{c} f(x) \, dx + \int_{c}^{b} f(x) \, dx$

# 結構/要素 (Structure/Elements)

### 1. 收斂與發散 (Convergence and Divergence)
- **收斂 (Convergent)**：極限存在且為一有限數值。代表區域無界但其面積有限。
- **發散 (Divergent)**：極限不存在或趨向 $\pm\infty$。

### 2. 判定法則 (Tests for Convergence)
- **p-級數測試 (p-Test for Integrals)**：
  - $\int_{1}^{\infty} \frac{1}{x^p} \, dx$：當 $p > 1$ 時收斂，當 $p \le 1$ 時發散。
  - $\int_{0}^{1} \frac{1}{x^p} \, dx$：當 $p < 1$ 時收斂，當 $p \ge 1$ 時發散。
- **比較判別法 (Comparison Test)**：
  - 設 $f(x) \ge g(x) \ge 0$。
  - 較大函數積分收斂，較小函數積分必收斂：$\int f(x) \, dx$ 收斂 $\implies \int g(x) \, dx$ 收斂。
  - 較小函數積分發散，較大函數積分必發散：$\int g(x) \, dx$ 發散 $\implies \int f(x) \, dx$ 發散。
- **極限比較判別法 (Limit Comparison Test)**：
  - 若 $\lim_{x \to \infty} \frac{f(x)}{g(x)} = L$ ($0 < L < \infty$)，則兩者同時收斂或發散。

# 原理/推導 (Principles/Derivation)
瑕積分的本質是利用 **微積分基本定理 (Fundamental Theorem of Calculus)** 與 **極限論** 的結合。

### 推導範例：p-級數 (Type I)
考慮 $I = \int_{1}^{\infty} \frac{1}{x^p} \, dx$：
1. 若 $p \ne 1$：
   $\lim_{b \to \infty} \int_{1}^{b} x^{-p} \, dx = \lim_{b \to \infty} \left[ \frac{x^{-p+1}}{-p+1} \right]_1^b = \lim_{b \to \infty} \left( \frac{b^{1-p}}{1-p} - \frac{1}{1-p} \right)$
   - 當 $1-p < 0$ (即 $p>1$)， $b^{1-p} \to 0$，結果為 $\frac{1}{p-1}$ (收斂)。
   - 當 $1-p > 0$ (即 $p<1$)， $b^{1-p} \to \infty$ (發散)。
2. 若 $p = 1$：
   $\lim_{b \to \infty} [\ln|x|]_1^b = \lim_{b \to \infty} \ln b = \infty$ (發散)。
