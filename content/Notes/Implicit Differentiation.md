---
tags:
  - Math
up:
  - "[[Derivative]]"
related:
  - "[[Chain Rule]]"
  - "[[多變數隱函數]]"
aliases:
  - 隱函數微分
---

# 隱函數微分 (Implicit Differentiation)

### 1. 概要 (Overview)
在微積分中，大多數函數是以 **顯函數 (Explicit Function)** 的形式給出，例如 $y = f(x)$。然而，有些變數間的關係是以方程式 **隱函數 (Implicit Function)** 的形式存在，例如圓的方程式 $x^2 + y^2 = 25$。

**隱函數微分法**讓我們不需要先將 $y$ 解出來（有時甚至無法解出），就能直接對方程式兩邊關於 $x$ 微分，求得導數 $\frac{dy}{dx}$。

### 2. 核心概念 (Core Concepts)
*   **連鎖律的應用**: 隱微分的核心在於 [[Chain Rule|連鎖律]]。當我們對包含 $y$ 的項（如 $y^2, \sin(y)$）關於 $x$ 微分時，必須記得 $y$ 是 $x$ 的函數，因此：
    $$\frac{d}{dx}(g(y)) = g'(y) \cdot \frac{dy}{dx}$$
*   **思維轉換**: 將 $y$ 看作一個被隱藏起來的 $f(x)$，每當微分到 $y$ 時，後面都要補上一個 $\frac{dy}{dx}$。

### 3. 操作步驟 (Steps & Example)
#### 標準步驟：
1.  **兩邊微分**: 對方程式的等號兩邊同時關於 $x$ 進行微分。
2.  **套用規則**: 遇到 $y$ 的項時，使用連鎖律產生 $\frac{dy}{dx}$。
3.  **整理項**: 將所有包含 $\frac{dy}{dx}$ 的項移到等號左邊，其餘移到右邊。
4.  **提出求解**: 提出 $\frac{dy}{dx}$ 並解出其表達式。

#### 範例：求 $x^3 + y^3 = 6xy$ 在 $(x, y)$ 的導數
1.  $\frac{d}{dx}(x^3 + y^3) = \frac{d}{dx}(6xy)$
2.  $3x^2 + 3y^2 \frac{dy}{dx} = 6(y + x \frac{dy}{dx})$ (右邊使用了 [[Derivative#Differentiation Rules|乘法法則]])
3.  $3x^2 + 3y^2 y' = 6y + 6xy'$
4.  $(3y^2 - 6x)y' = 6y - 3x^2$
5.  $y' = \frac{6y - 3x^2}{3y^2 - 6x} = \frac{2y - x^2}{y^2 - 2x}$

### 4. 圖形意義 (Geometric Meaning)
*   **切線斜率**: $\frac{dy}{dx}$ 代表曲線 $F(x, y) = 0$ 在特定點 $(x, y)$ 的切線斜率。
*   **垂直切線 (Vertical Tangents)**: 當分母為 0（例如上述範例中的 $y^2 - 2x = 0$）時，該處可能存在垂直切線。
*   **法線 (Normal Line)**: 若切線斜率為 $m$，則法線斜率為 $-1/m$。

### 5. 進階：多變數觀點 (Advanced Perspective)
根據 [[多變數隱函數]] 的全微分原理，若定義 $F(x, y) = 0$，則可以使用偏導數公式快速求解：
$$\frac{dy}{dx} = -\frac{F_x}{F_y} = -\frac{\partial F / \partial x}{\partial F / \partial y}$$
這在驗證複雜的隱微分結果時非常有用。

### 6. 常見技巧 (Tips)
*   **二階導數**: 求 $\frac{d^2y}{dx^2}$ 時，對一階導數的結果再次進行隱微分，並在最後將原本求得的 $\frac{dy}{dx}$ 代回消去。
*   **簡化計算**: 在求特定點的斜率時，通常在微分完後直接代入數值 $(x_0, y_0)$，而非先解出抽象的 $\frac{dy}{dx}$ 公式，這樣計算會簡單許多。
