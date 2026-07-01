---
tags:
  - Math
up:
  - "[[limit and continuty]]"
related:
  - "[[均值定理|The Mean Value Theorem]]"
aliases:
  - 中間值定理
annotation:
---
if f is continuous on a closed interval^[極小的區間] [a, b], $y_{0}$ is every value between $f(a), f(b)$, 
then
$$
\exists c \in [a, b], y_{0}=f(c)
$$
>$\exists$: exists

ex1 **勘根**
*Show there is a root of $x^{3}-x-1=0$ between 1 & 2*
sol.
$f(x)=x^{3}-x-1$
$f(1)=-1,f(2)=5$
$0\in[-1,5]$
**by intermediate value theorm**, $\exists c \in [1, 2]$, s.t.^[subject to 使滿足] $f(c)=0$
$f(c)=c^{3}-c-1=0$, c is a root _#

ex2
$f(x)= \frac{\sin(x)}{x},x\ne 0$
$f(x)= 1,x = 0$
>第二式補上第一式未連續之點(x = 0)

