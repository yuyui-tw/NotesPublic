---
aliases:
  - Stirling's Formula
tags:
  - Math
up: "[[數列與級數]]"
related:
  - "[[正項級數]]"
  - "[[冪級數]]"
annotation: 階乘在大 n 時的漸近估計公式
---

# 概要 (Overview)
**斯特林近似 (Stirling's Approximation / Stirling's Formula)** 是一個用於估計階乘 $n!$ 在 $n \to \infty$ 時行為的公式。它將離散的階乘運算轉化為連續函數的指數與乘冪運算，是分析級數斂散性（特別是包含 $n!$ 的項）的重要工具。

# 核心概念 (Core Concepts)
- **漸近等價 (Asymptotic Equivalence)**：當 $n$ 極大時：
  $$n! \sim \sqrt{2\pi n} \left( \frac{n}{e} \right)^n$$
  意即 $\lim_{n \to \infty} \frac{n!}{\sqrt{2\pi n} (n/e)^n} = 1$。
- **誤差趨勢**：相對誤差隨 $n$ 增加而縮小，約為 $O(1/n)$。

# 結構/要素 (Structure/Elements)
### 1. 斯特林公式主體
- $\sqrt{2\pi n}$：修正項（來自高斯積分）。
- $(n/e)^n$：主增長項，反映了 $n!$ 的指數級增長速度。

### 2. 常用對數形式 (Logarithmic Form)
在統計力學與大數據計算中更常用：
$$\ln(n!) \approx n \ln n - n$$
（這是公式的粗略一階近似，來自 $\int_1^n \ln x \, dx$）。

# 原理/推導 (Principles/Derivation)
### 1. 積分逼近法
利用 $\ln(n!) = \sum_{k=1}^n \ln k$，將求和看作 $\int_1^n \ln x \, dx$ 的梯形近似。
透過積分計算：$\int \ln x \, dx = x \ln x - x + C$，可導出 $\ln(n!)$ 的基本增長級。

### 2. 應用場景：冪級數收斂分析
當遇到級數如 $\sum \frac{n!}{(n^n)} x^n$ 時，直接使用比值法（Ratio Test）可能較複雜，若利用斯特林公式：
$$\frac{n!}{n^n} \sim \frac{\sqrt{2\pi n} (n/e)^n}{n^n} = \sqrt{2\pi n} \cdot e^{-n}$$
可更直觀看出其衰減速度，進而判斷其 **[[正項級數]]** 的斂散性。

> [!TIP] 連結
> 在探討 **[[冪級數]]** 的收斂半徑時，若係數包含階乘，斯特林近似常能幫助化簡極限運算。
