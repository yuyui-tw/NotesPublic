---
aliases:
  - 分部積分
tags:
  - Math
up: "[[Integral]]"
related:
---

# 概要 (Summary)
分部積分法 (Integration by Parts) 是一種重要的積分技巧，其本質是**乘積求導法則 (Product Rule for Differentiation) 的逆運算**。它主要用於計算兩個函數乘積的積分，目標是將一個複雜的積分轉化為一個更容易計算的積分。

# 核心概念 (Core Concepts)
分部積分的公式源於對乘積法則 $d(uv) = u \,dv + v \,du$ 進行積分。整理後可得：
$$ \int u \,dv = uv - \int v \,du $$
- **$u$**: 我們選擇的、準備對其進行**微分**的函數部分。
- **$dv$**: 我們選擇的、準備對其進行**積分**的函數部分 (包含 $dx$)。

**成功的關鍵**在於謹慎選擇 $u$ 和 $dv$，使得新的積分 $\int v \,du$ 比原來的積分 $\int u \,dv$ 更簡單。

# 結構/要素 (Method and Strategy)
## 如何選擇 u：LIATE 原則
選擇 $u$ 的一個實用經驗法則是遵循 **LIATE** 的優先順序。排在越前面的函數類型，越適合被選為 $u$：
1.  **L** - **對數函數 (Logarithmic functions):** 如 $\ln x, \log_b x$
2.  **I** - **反三角函數 (Inverse trigonometric functions):** 如 $\arcsin x, \arctan x$
3.  **A** - **代數函數 (Algebraic functions):** 如 $x^2, 3x^5$
4.  **T** - **三角函數 (Trigonometric functions):** 如 $\sin x, \cos x$
5.  **E** - **指數函數 (Exponential functions):** 如 $e^x, 2^x$

**理由:** 這個順序通常能確保 $du$ 比 $u$ 更簡單，而 $v$ (即 $dv$ 的積分) 不會變得過於複雜。

## 定積分的分部積分
對於定積分，公式變為：
$$ \int_a^b u \,dv = \left[uv\right]_a^b - \int_a^b v \,du $$

# 原理/推導 (Derivation)
分部積分公式可以直接從乘積求導法則推導出來：
1.  從乘積法則開始:
    $$ \frac{d}{dx}(uv) = u \frac{dv}{dx} + v \frac{du}{dx} $$
2.  對兩邊同時進行關於 $x$ 的不定積分:
    $$ \int \frac{d}{dx}(uv) \,dx = \int \left( u \frac{dv}{dx} + v \frac{du}{dx} \right) \,dx $$
3.  左邊的積分和微分互為逆運算，消去後得到 $uv$ (省略常數 C，最後統一加上):
    $$ uv = \int u \,dv + \int v \,du $$
4.  移項整理，即得分部積分公式:
    $$ \int u \,dv = uv - \int v \,du $$

# 範例 (Examples)
## 範例 1: 基本應用
計算 $\int x \cos x \,dx$。
- **選擇 u 和 dv:**
  - 根據 LIATE 原則，代數函數 $x$ (A) 優先於三角函數 $\cos x$ (T)。
  - 令 $u = x \implies du = dx$
  - 令 $dv = \cos x \,dx \implies v = \sin x$
- **套用公式:**
  $$ \int x \cos x \,dx = x \sin x - \int \sin x \,dx $$
  $$ = x \sin x - (-\cos x) + C = x \sin x + \cos x + C $$

## 範例 2: 多次應用
計算 $\int x^2 e^x \,dx$。
- **第一次:**
  - $u = x^2 \implies du = 2x \,dx$
  - $dv = e^x \,dx \implies v = e^x$
  - $\int x^2 e^x \,dx = x^2 e^x - \int 2x e^x \,dx = x^2 e^x - 2 \int x e^x \,dx$
- **第二次 (對 $\int x e^x \,dx$):**
  - $u = x \implies du = dx$
  - $dv = e^x \,dx \implies v = e^x$
  - $\int x e^x \,dx = x e^x - \int e^x \,dx = x e^x - e^x$
- **組合結果:**
  $$ \int x^2 e^x \,dx = x^2 e^x - 2(x e^x - e^x) + C = e^x(x^2 - 2x + 2) + C $$

## 範例 3: 循環積分 (Boomerang)
計算 $\int e^x \cos x \,dx$。
- **第一次:**
  - $u = \cos x \implies du = -\sin x \,dx$
  - $dv = e^x \,dx \implies v = e^x$
  - $I = \int e^x \cos x \,dx = e^x \cos x - \int e^x (-\sin x) \,dx = e^x \cos x + \int e^x \sin x \,dx$
- **第二次 (對 $\int e^x \sin x \,dx$):**
  - $u = \sin x \implies du = \cos x \,dx$
  - $dv = e^x \,dx \implies v = e^x$
  - $\int e^x \sin x \,dx = e^x \sin x - \int e^x \cos x \,dx$
- **組合並求解:**
  $$ I = e^x \cos x + (e^x \sin x - I) $$
  $$ 2I = e^x (\cos x + \sin x) $$
  $$ I = \frac{e^x (\cos x + \sin x)}{2} + C $$