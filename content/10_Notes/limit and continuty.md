---
tags:
  - Math
up:
related:
aliases:
  - 極限與連續性
---

# 動機
一個函數 f(t) 代表在時間 t 的移動距離
則在 [t₁, t₂] 區間內的平均速度為
$$ 
\frac{f(t_{2})-f(t_{1})}{t_{2}-t_{1}} 
$$ 
若時間區間縮小為 [t₀, t₀+h]
$$ 
\frac{f(t_{0}+h)-f(t_{0})}{h} 
$$ 
此即為在 t₀ 的瞬時速度，也是微分概念的基礎

# 極限的觀念
## 單邊極限 (One-Sided Limits)
考慮一個函數
$$ 
f(x) = 
\begin{cases}
1, & x > 0 \\
-1, & x < 0
\end{cases}
$$ 
![[非連續極限 示意圖.png|200]]
從右邊趨近 0 時，極限為 1
$$ 
\lim_{ x \to 0^{+} }f(x)=1 
$$ 
從左邊趨近 0 時，極限為 -1
$$ 
\lim_{ x \to 0^{-} }f(x)=-1 
$$ 
由於左右極限不相等，因此 $x \to 0$ 的雙邊極限不存在
$$ 
\lim_{ x \to 0 }f(x) \text{ does not exist} 
$$ 

## 極限不存在的情況
極限不存在主要有三種情況
1.  左右極限不相等，如上述例子
2.  函數在趨近點附近無限震盪
    例如 $f(x) = \sin(\frac{1}{x})$
    當 x 趨近 0 時，其值在 -1 和 1 之間震盪
    $$ 
    \lim_{ x \to 0 } \sin \frac{1}{x} \text{ does not exist} 
    $$ 
3.  函數值趨近於無限大或無限小
    $$ 
    \lim_{ x \to 0^{+} } \frac{1}{x} = \infty 
    $$ 
    $$ 
    \lim_{ x \to 0^{-} } \frac{1}{x} = -\infty 
    $$ 

# 極限的計算
## 無窮遠處的極限與漸近線
- 水平漸近線 (Horizontal Asymptote)
若 $\lim_{ x \to \infty }f(x) = L$ 或 $\lim_{ x \to -\infty }f(x) = L$，
則 y=L 為一條水平漸近線
一個基本例子: 
$$ 
\lim_{ x \to \infty } \frac{1}{x}= 0 
$$ 
- 垂直漸近線 (Vertical Asymptote)
若 $\lim_{ x \to a }f(x) = \pm \infty$，則 x=a 為一條垂直漸近線

## 不定型與有理化
形如 $\frac{0}{0}$ 或 $\frac{\infty}{\infty}$ 的極限被稱為不定型 *indeterminate*
計算這類極限時，一個常用技巧是有理化，通常是除以分子或分母中影響最大的項

# 重要極限的證明
## 標準極限: $\lim_{ \theta \to 0 } \frac{\sin\theta}{\theta}=1$
此證明主要使用 [[夾擠定理]]

### 1. 幾何面積比較
在單位圓中，比較三個區域的面積
假設 $\theta$ 為一個很小的正角
1.  小三角形 $\triangle OAP$
2.  扇形 $OAP$
3.  大三角形 $\triangle OAR$

- 面積大小關係為:
面積(小三角形) < 面積(扇形) < 面積(大三角形)

### 2. 計算各區域面積
- $\triangle OAP$ 面積
  $\frac{1}{2} \cdot \text{底} \cdot \text{高} = \frac{1}{2} \cdot 1 \cdot \sin\theta = \frac{\sin\theta}{2}$
- 扇形 $OAP$ 面積
  $\frac{1}{2} r^2 \theta = \frac{1}{2} (1)^2 \theta = \frac{\theta}{2}$
- $\triangle OAR$ 面積
  $\frac{1}{2} \cdot \text{底} \cdot \text{高} = \frac{1}{2} \cdot 1 \cdot \tan\theta = \frac{\tan\theta}{2}$

### 3. 建立不等式
將面積代入關係式
$\frac{\sin\theta}{2} < \frac{\theta}{2} < \frac{\tan\theta}{2}$

同乘以 2
$\sin\theta < \theta < \tan\theta$

因 $0 < \theta < \frac{\pi}{2}$， $\sin\theta > 0$
同除以 $\sin\theta$
$1 < \frac{\theta}{\sin\theta} < \frac{1}{\cos\theta}$

將不等式全部倒數, 並反轉不等號
$\cos\theta < \frac{\sin\theta}{\theta} < 1$

### 4. 使用夾擠定理
計算不等式兩側函數在 $\theta \to 0^{+}$ 時的極限
$\lim_{\theta \to 0^{+}} \cos\theta = \cos(0) = 1$
$\lim_{\theta \to 0^{+}} 1 = 1$

根據 [[夾擠定理]]，
被夾在中間的函數極限也必然是 1
$\lim_{\theta \to 0^{+}} \frac{\sin\theta}{\theta} = 1$

### 5. 考慮左極限
令 $\theta = -y$，其中 $y > 0$

當 $\theta \to 0^{-}$ 時, $y \to 0^{+}$，
$\frac{\sin\theta}{\theta} = \frac{\sin(-y)}{-y} = \frac{-\sin y}{-y} = \frac{\sin y}{y}$
因此左極限也為 1
$\lim_{\theta \to 0^{-}} \frac{\sin\theta}{\theta} = \lim_{y \to 0^{+}} \frac{\sin y}{y} = 1$

### 結論
左右極限均存在且相等，故 $\lim_{\theta \to 0} \frac{\sin\theta}{\theta} = 1$ 成立

# 連續性 (Continuity)
## 連續性的定義
一個函數 f(x) 在 c 點是連續的，若且唯若滿足以下三個條件
1.  $f(c)$ 有定義
2.  $\lim_{ x \to c }f(x)$ 存在
3.  $\lim_{ x \to c }f(x) = f(c)$
注意: c 點必須在函數的定義域*(domain)*內

## 連續函數的性質
若 f 和 g 兩個函數在 c 點皆連續，
則以下組合構成的函數在 c 點也連續
1.  $f \pm g$
2.  $k \cdot f$
3.  $f \cdot g$
4.  $f/g$ (要求 $g(c) \ne 0$)
5.  $f^n$
6.  $\sqrt[n]{f}$
7.  複合函數 $g \circ f$， (要求 g 在 $f(c)$ 連續)

## 中間值定理 (Intermediate Value Theorem)
[[Intermediate Value Theorem]]
