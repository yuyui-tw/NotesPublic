---
aliases:
  - Calculus II Midterm Review
  - 微積分二期中檢討
tags:
  - Math
  - QuizReview
annotation: 2026 Spring Calculus II 期中考題目深度檢討與概念解析。
---

# 2026 Spring Calculus II (1303) Midterm 題目檢討

這份檢討報告旨在透過「第一性原理 (`First-principles thinking`)」拆解核心概念，並利用「逆向思考 (`Inversion`)」預防常見錯誤。

---

## 1. 不定積分：$\int \ln x \, dx$

### 核心概念 (Core Framework)
*   **分部積分法 (Integration by Parts)**：源於乘法的微分法則 $\frac{d}{dx}(uv) = u\frac{dv}{dx} + v\frac{du}{dx}$。
*   **公式**：$\int u \, dv = uv - \int v \, du$。

### 邏輯 (Operational Logic)
1.  **選擇變數**：令 $u = \ln x$，則 $dv = dx$。
2.  **求微分與積分**：$du = \frac{1}{x} dx$，$v = x$。
3.  **代入公式**：
    $$\int \ln x \, dx = x \ln x - \int x \cdot \frac{1}{x} \, dx = x \ln x - \int 1 \, dx$$
4.  **結果**：$x \ln x - x + C$。

### 陷阱與檢討 (Inversion & Pitfalls)
*   **常見錯誤**：忘記最後的常數 $C$，或是在選擇 $u$ 與 $dv$ 時順序顛倒（通常遵循 LIATE 準則，對數函數優先作為 $u$）。
*   **檢驗**：對結果求導 $\frac{d}{dx}(x \ln x - x) = (1 \cdot \ln x + x \cdot \frac{1}{x}) - 1 = \ln x + 1 - 1 = \ln x$，回歸原題，證明正確。

---

## 2. 不定積分：$\int \frac{1}{\cos^2 x + 4 \sin^2 x} \, dx$

### 核心概念
*   **等價轉換 (Equivalence)**：處理三角函數分式積分時，常見技巧是將其轉換為 $\tan x$ 與 $\sec^2 x$ 的形式。

### 邏輯
1.  **同除 $\cos^2 x$**：將分子分母同時除以 $\cos^2 x$。
    $$\int \frac{\sec^2 x}{1 + 4 \tan^2 x} \, dx$$
2.  **變數變換 (Substitution)**：令 $u = \tan x$，則 $du = \sec^2 x \, dx$。
3.  **轉換形式**：原式變為 $\int \frac{1}{1 + 4u^2} \, du$。
4.  **積分公式**：利用 $\int \frac{1}{1 + a^2 u^2} \, du = \frac{1}{a} \arctan(au) + C$。這裡 $a=2$。
5.  **結果**：$\frac{1}{2} \arctan(2u) + C = \frac{1}{2} \arctan(2 \tan x) + C$。

### 陷阱與檢討
*   **技巧點**：若不熟悉同除 $\cos^2 x$ 的技巧，可能會卡在倍角公式或複雜的三角代換中。記住：看到 $\sin^2$ 與 $\cos^2$ 的組合出現在分母，優先考慮 $\tan$ 轉換。

---

## 3. 瑕積分：$\int_0^\infty \frac{e^{-x}}{1+e^{-x}} \, dx$

### 核心概念
*   **瑕積分 (Improper Integral)**：上限為無限大，需考慮極限。
*   **對數積分**：觀察分子是否為分母的導數（或其倍數）。

### 邏輯
1.  **觀察結構**：分母為 $1+e^{-x}$，其導數為 $-e^{-x}$，與分子高度相關。
2.  **變數變換**：令 $u = 1 + e^{-x}$，則 $du = -e^{-x} \, dx$。
3.  **更換上下限**：
    *   當 $x = 0$，$u = 1 + e^0 = 2$。
    *   當 $x \to \infty$，$u \to 1 + 0 = 1$。
4.  **積分過程**：
    $$\int_2^1 \frac{-1}{u} \, du = \int_1^2 \frac{1}{u} \, du = [\ln |u|]_1^2$$
5.  **結果**：$\ln 2 - \ln 1 = \ln 2$。

### 陷阱與檢討
*   **符號與上下限**：在變數變換時，務必注意 $du$ 的負號與上下限的對應關係。
*   **直觀理解**：$e^{-x}$ 在無限遠處趨近於 0，這保證了積分的收斂性。

---

## 4. 參數式曲線圍成的面積：$x = t+t^3, y = t+t^5$，圍繞 y 軸與 $y=2$

### 核心概念
*   **參數式積分面積**：$A = \int x \, dy = \int_{t_1}^{t_2} x(t) \cdot y'(t) \, dt$。

### 邏輯
1.  **尋找 $t$ 的邊界**：
    *   y 軸代表 $x=0 \implies t+t^3 = 0 \implies t=0$。
    *   $y=2 \implies t+t^5 = 2 \implies t=1$ (觀察法，且函數單調遞增)。
2.  **求導**：$dy = (1 + 5t^4) \, dt$。
3.  **列式計算**：
    $$A = \int_0^1 (t+t^3)(1+5t^4) \, dt = \int_0^1 (t + 5t^5 + t^3 + 5t^7) \, dt$$
4.  **逐項積分**：
    $$A = [\frac{1}{2}t^2 + \frac{5}{6}t^6 + \frac{1}{4}t^4 + \frac{5}{8}t^8]_0^1 = \frac{1}{2} + \frac{5}{6} + \frac{1}{4} + \frac{5}{8}$$
5.  **結果**：$\frac{12 + 20 + 6 + 15}{24} = \frac{53}{24}$。

### 陷阱與檢討
*   **概念模糊**：容易誤用 $A = \int y \, dx$，需根據題目要求（y 軸與 $y=2$ 圍成）判斷應對 $y$ 進行積分。

---

## 5. 向量值函數初值問題 (IVP)：$\frac{dr}{dt} = t^2 \mathbf{i} - \sin t \mathbf{j} - \mathbf{k}, \mathbf{r}(0) = \mathbf{i} + \mathbf{k}$

### 核心概念
*   **分量積分**：對每個向量分量分別進行不定積分，並利用初值確定常數。

### 邏輯
1.  **不定積分**：
    $\mathbf{r}(t) = \int (t^2 \mathbf{i} - \sin t \mathbf{j} - \mathbf{k}) \, dt = (\frac{1}{3}t^3 + C_1)\mathbf{i} + (\cos t + C_2)\mathbf{j} + (-t + C_3)\mathbf{k}$
2.  **代入初值 $t=0$**：
    $\mathbf{r}(0) = (0 + C_1)\mathbf{i} + (1 + C_2)\mathbf{j} + (0 + C_3)\mathbf{k} = 1\mathbf{i} + 0\mathbf{j} + 1\mathbf{k}$
3.  **解常數**：$C_1 = 1, C_2 = -1, C_3 = 1$。
4.  **結果**：$\mathbf{r}(t) = (\frac{1}{3}t^3 + 1)\mathbf{i} + (\cos t - 1)\mathbf{j} + (1-t)\mathbf{k}$。

### 陷阱與檢討
*   **常數誤差**：最常見的錯誤是忽略了 $\cos 0 = 1$，導致 $C_2$ 計算錯誤。務必代入具體數值檢驗。

---

## 6. 空間曲線性質：$\mathbf{r}(t) = (4 \cos t)\mathbf{i} + (4 \sin t)\mathbf{j} + 3t\mathbf{k}$

### 核心概念
*   **單位切向量 ($\mathbf{T}$)**：$\mathbf{v}/|\mathbf{v}|$。
*   **曲率 ($\kappa$)**：$|d\mathbf{T}/dt| / |\mathbf{v}|$。
*   **單位法向量 ($\mathbf{N}$)**：$(d\mathbf{T}/dt) / |d\mathbf{T}/dt|$。

### 邏輯
1.  **求速度與速率**：
    $\mathbf{v}(t) = -4 \sin t \mathbf{i} + 4 \cos t \mathbf{j} + 3\mathbf{k} \implies |\mathbf{v}| = \sqrt{16+9} = 5$。
2.  **求 $\mathbf{T}$**：$\mathbf{T}(t) = -\frac{4}{5} \sin t \mathbf{i} + \frac{4}{5} \cos t \mathbf{j} + \frac{3}{5} \mathbf{k}$。
3.  **求 $\mathbf{T}'(t)$**：$\mathbf{T}'(t) = -\frac{4}{5} \cos t \mathbf{i} - \frac{4}{5} \sin t \mathbf{j} \implies |\mathbf{T}'(t)| = \frac{4}{5}$。
4.  **計算曲率**：$\kappa = \frac{4/5}{5} = \frac{4}{25}$。
5.  **求 $\mathbf{N}$**：$\mathbf{N} = \frac{\mathbf{T}'(t)}{|\mathbf{T}'(t)|} = -\cos t \mathbf{i} - \sin t \mathbf{j}$。

### 陷阱與檢討
*   **計算量**：此題為典型的螺線 (Helix)。特點是速率 $|\mathbf{v}|$ 與曲率 $\kappa$ 均為常數。若計算出 $\kappa$ 含有 $t$，則需重新檢查計算過程。
