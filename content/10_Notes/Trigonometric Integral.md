---
aliases:
  - 三角函數積分
tags:
  - Math
up:
  - "[[Integral]]"
related:
  - "[[Trigonometric Substitution]]"
  - "[[三角函數|Trigonometric Functions]]"
---

# 概要 (Summary)
三角函數積分 (Trigonometric Integrals) 是指被積函數包含三角函數的積分。求解這類積分的核心策略是巧妙地運用**三角恆等式 (Trigonometric Identities)**，將複雜的被積函數轉換為可以使用 [[Integration by Parts|換元積分法]] 或其他基本方法求解的形式。

# 核心恆等式 (Core Identities)
1.  **畢氏恆等式 (Pythagorean Identities):**
    - $\sin^2 x + \cos^2 x = 1$
    - ==$\tan^2 x + 1 = \sec^2 x$==
    - $1 + \cot^2 x = \csc^2 x$
2.  **半角/倍角公式 (Half-Angle/Double-Angle Formulas):** (常用於降冪)
    - ==$\sin^2 x = \frac{1 - \cos(2x)}{2}$==
    - ==$\cos^2 x = \frac{1 + \cos(2x)}{2}$==
    - ==$\sin(2x) = 2 \sin x \cos x$==

- $\int \sec\theta d\theta$
計算 $\int \sec \theta \, d\theta$ 的方法與 $\csc x$ 的邏輯非常相似，都需要用到一個特殊的「技巧」來構造 $u$-代換（$u$-substitution）。
$$\int \sec \theta \, d\theta = \int \sec \theta \cdot \frac{\sec \theta + \tan \theta}{\sec \theta + \tan \theta} \, d\theta$$
$$\int \frac{\sec^2 \theta + \sec \theta \tan \theta}{\sec \theta + \tan \theta} \, d\theta$$
	- $\frac{d}{d\theta}(\sec \theta) = \sec \theta \tan \theta$
	- $\frac{d}{d\theta}(\tan \theta) = \sec^2 \theta$
$$du = (\sec \theta \tan \theta + \sec^2 \theta) \, d\theta$$
$$\int \frac{1}{u} \, du = \ln|u| + C$$
$$\int \sec \theta \, d\theta = \ln|\sec \theta + \tan \theta| + C$$

# 結構/要素 (Strategies)
## 類型 1: $\int \sin^m x \cos^n x \,dx$
- **策略 1: $\cos$ 的次方 $n$ 為奇數**
  1.  分離出一個 $\cos x$。
  2.  使用 $\cos^2 x = 1 - \sin^2 x$ 將剩餘的 $\cos$ 全部轉換為 $\sin$。
  3.  進行換元，令 $u = \sin x$，則 $du = \cos x \,dx$。
- **策略 2: $\sin$ 的次方 $m$ 為奇數**
  1.  分離出一個 $\sin x$。
  2.  使用 $\sin^2 x = 1 - \cos^2 x$ 將剩餘的 $\sin$ 全部轉換為 $\cos$。
  3.  進行換元，令 $u = \cos x$，則 $du = -\sin x \,dx$。
- **策略 3: $m$ 和 $n$皆為偶數**
  1.  使用半角公式 $\sin^2 x = \frac{1 - \cos(2x)}{2}$ 和 $\cos^2 x = \frac{1 + \cos(2x)}{2}$ 來降冪。
  2.  展開並重複此過程，直到可以積分。

## 類型 2: $\int \tan^m x \sec^n x \,dx$
- **策略 1: $\sec$ 的次方 $n$ 為偶數**
  1.  分離出一個 $\sec^2 x$。
  2.  使用 $\sec^2 x = 1 + \tan^2 x$ 將剩餘的 $\sec$ 全部轉換為 $\tan$。
  3.  進行換元，令 $u = \tan x$，則 $du = \sec^2 x \,dx$。
- **策略 2: $\tan$ 的次方 $m$ 為奇數 (且 $n \ge 1$)**
  1.  分離出一個 $\sec x \tan x$。
  2.  使用 $\tan^2 x = \sec^2 x - 1$ 將剩餘的 $\tan$ 全部轉換為 $\sec$。
  3.  進行換元，令 $u = \sec x$，則 $du = \sec x \tan x \,dx$。

# 原理/推導 (Other Cases and Reductions)
- **$\\cot$ 與 $\\csc$ 的積分:** 積分 $\int \cot^m x \csc^n x \,dx$ 的策略與 $\tan / \sec$ 組合非常相似，主要利用恆等式 $1 + \cot^2 x = \csc^2 x$。
- **遞推公式 (Reduction Formulas):** 對於某些情況 (如 $\int \sec^3 x \,dx$)，可能無法直接套用上述策略，此時需要使用[[Integration by Parts|分部積分法]]來推導出遞推公式，逐步降低冪次。

# 範例 (Examples)
## 範例 1: Sin 的奇次冪
計算 $\int \sin^3 x \,dx$。
1.  **分離 $\sin x$:** $\int \sin^2 x \sin x \,dx$
2.  **轉換為 $\cos x$:** $\int (1 - \cos^2 x) \sin x \,dx$
3.  **換元 ($u = \cos x, du = -\sin x \,dx$):**
    $$ \int (1 - u^2) (-du) = \int (u^2 - 1) \,du $$
    $$ = \frac{1}{3}u^3 - u + C $$
4.  **代回 $x$:**
    $$ \frac{1}{3}\cos^3 x - \cos x + C $$

## 範例 2: Cos 的偶次冪
計算 $\int \cos^2 x \,dx$。
1.  **使用半角公式:**
    $$ \int \frac{1 + \cos(2x)}{2} \,dx = \frac{1}{2} \int (1 + \cos(2x)) \,dx $$
2.  **積分:**
    $$ \frac{1}{2} \left( x + \frac{1}{2}\sin(2x) \right) + C = \frac{1}{2}x + \frac{1}{4}\sin(2x) + C $$