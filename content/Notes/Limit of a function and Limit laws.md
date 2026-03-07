---
tags:
  - Math
up: "[[limit and continuty]]"
related:
aliases:
  - 極限與其規則
annotation:
---
# Limit
ex.
$$
f(x)=\frac{x^{2}-1}{x-1}
$$
1. 直接帶入 $x\to c$
2. 檢查內容的性質: 根號、平方、正負、分母不為0

- polynomial 多項式
$$\begin{align} \\
 & p(x) = a_{n}x^{n}+a_{n-1}x^{n-1}+\dots a_{n}x^{n}+a_{0}\\
 & q(x)
          \end{align}$$
則
  $$
\lim_{ x \to c }\frac{p(x)}{q(x)}=\frac{p(c)}{q(c)},q(c)\ne 0
$$
- $\lim_{ x \to -1 }\frac{1}{x+1}$ ==do not exist==
- 當遇到不定型函數(*indeterminate form*)，試用有理化處理
	1. 分母為0
	2. 根號相加減且無法運算
	
	ex. $$\displaylines{
\lim_{ x \to 0 }\frac{\sqrt{ x^{2}+100 }-10}{x^{2}}\\
=\lim_{ x \to 0 }\frac{\sqrt{ x^{2}+100 }-10}{x^{2}}\times\frac{\sqrt{ x^{2}+100 }+10}{\sqrt{ x^{2}+100 }+10}\\
=\frac{x^{2}+100-100}{(\sqrt{ x^{2}+100 }+10)x^{2}}  
}$$

# Laws of limit
- 加減分離律
- 乘除分離律(常數係數也可)
- $\lim f(x)^{n}=(\lim(f(x))^{n}$,radical(根式)也適用
- [[夾擠定理]]

# The Precise Definition of a limit
>極限的嚴格定義

$\lim_{ x \to a }f(x)=L\Leftrightarrow$ $\forall\varepsilon>0,\exists \delta>0,s.t.$
$0<|x-a|<\delta \Rightarrow |f(x)-L|<\varepsilon$
![[2-4.pdf#page=1&rect=151,450,374,593|2-4, p.1]]

ex.
$\lim_{ x \to \infty }a_{n}=a$
$\lim_{ x \to \infty }\frac{a_{1}+\dots+a_{n}}{n}$
**確保極限的理論誤差與解之間能夠被解釋**


> [!NOTE] such that
> 在數學與微積分的語境中，「**such that**」是一個極為關鍵的邏輯連接詞，在中文講義中常被翻譯為「**使得**」，並且經常縮寫為「**s.t.**」。
 **1. 函數的基本定義**
 **2. 極限與連續性的精確定義**
 **3. 存在性定理中的應用**
 **4. 數學常數的定義**
總結來說，**「such that」在數學上扮演著「條件限定」的角色**，它跟在「存在性（there exists）」陳述之後，用來明確指出所尋找的對象必須具備的特徵或滿足的方程式。

