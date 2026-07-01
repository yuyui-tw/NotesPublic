---
aliases:
  - Euler's formula
tags:
  - Math
up:
  - "[[泰勒級數]]"
related:
annotation:
---
# 概要 (Overview)
**歐拉公式 (Euler's formula)** 是複分析中連結三角函數與指數函數的橋樑，表達式為：
$$e^{ix} = \cos x + i \sin x$$
當 $x = \pi$ 時，可導出著名的歐拉恆等式 $e^{i\pi} + 1 = 0$。

# 核心概念 (Core Concepts)
- **複數指數函數 (Complex Exponential)**：將指數的概念從實數域擴展至複數平面。
- **單位圓關係**：在複數平面上，$e^{ix}$ 代表一個位於單位圓上、輻角為 $x$ 的點。

# 結構/要素 (Structure / Elements)
- **實部與虛部**：
	- $\text{Re}(e^{ix}) = \cos x$
	- $\text{Im}(e^{ix}) = \sin x$
- **三角函數的指數表示**：
	- $\cos x = \frac{e^{ix} + e^{-ix}}{2}$
	- $\sin x = \frac{e^{ix} - e^{-ix}}{2i}$

# 原理/推導 (Principles / Derivation)
利用 **[[泰勒級數]]** 在 $x=0$ 的展開（馬克勞林級數）進行證明：
1. 已知 $e^z = 1 + z + \frac{z^2}{2!} + \frac{z^3}{3!} + \frac{z^4}{4!} + \dots$
2. 代入 $z = ix$：
   $$e^{ix} = 1 + ix + \frac{(ix)^2}{2!} + \frac{(ix)^3}{3!} + \frac{(ix)^4}{4!} + \dots$$
   $$e^{ix} = 1 + ix - \frac{x^2}{2!} - i\frac{x^3}{3!} + \frac{x^4}{4!} + \dots$$
3. 將實部與虛部分開組合：
   $$e^{ix} = \left( 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \dots \right) + i \left( x - \frac{x^3}{3!} + \frac{x^5}{5!} - \dots \right)$$
4. 對照 **[[常見函數的泰勒級數]]**，括號內分別為 $\cos x$ 與 $\sin x$ 的級數，故得證。
