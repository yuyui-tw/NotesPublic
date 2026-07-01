---
tags:
  - Math
up:
  - "[[微積分]]"
related:
annotation:
aliases:
  - 導數
---

# Definition

> derivative: result of calculating a derivative (導數)
> differentiation: process (微分)

**Derivative of f(x) at $x_{0}$**
$$ 
\lim_{ h \to 0 } \frac{f(x_{0}+h)-f(x_{0})}{h} 
$$ 
This represents:
1.  instantaneous rate of change
2.  slope of the tangent line

**Alternative Formula**
$$ 
f'(x)=\lim_{ z \to x } \frac{f(z)-f(x)}{z-x} \quad (z=x+h) 
$$ 

**Notations**
$$ 
\displaylines{ 
f'(x)=y'= \frac{dy}{dx}= \frac{df}{dx} =\frac{d}{dx}f(x) \ 
=D(f)(x)=D_{x}f(x) 
}
$$ 
$$ 
\displaylines{ 
f'(a) = \frac{dy}{dx}|_{x=a} = \frac{df}{dx}|_{x=a} = \frac{d}{dx}f(x)|_{x=a} 
}
$$ 
> $\frac{d}{dx}$ can more clearly identify what is being differentiated

# Differentiability and Continuity

**Theorem**
If $f'(c)$ exists, then $f$ is differentiable at $x=c$
This also implies $f$ is [[limit and continuty#Continuty|continuous]] at $x=c$

**Proof**
If $\lim_{ h \to 0} \frac{f(c+h)-f(c)}{h}$ exists, then the numerator must approach zero
$\lim_{h \to 0} [f(c+h)-f(c)] = 0$
$\lim_{h \to 0} f(c+h) = f(c)$
Let $x = c+h$, then as $h \to 0$, $x \to c$
$\lim_{x \to c} f(x) = f(c)$, which is the definition of continuity at c, Q.E.D.

# Differentiation Rules

1.  **Constant Rule**
    $\frac{d}{dx}(c)=0$

2.  **Power Rule**
    $\frac{d}{dx}x^{n}=nx^{n-1}$

3.  **Constant Multiple Rule**
    $\frac{d}{dx}(cu)=c \frac{du}{dx}$

4.  **Sum Rule**
    $\frac{d}{dx}(u+v)= \frac{du}{dx}+ \frac{dv}{dx}$

5.  **Product Rule**
    $\frac{d}{dx}(uv)=u \frac{dv}{dx}+ v \frac{du}{dx}$

6.  **Quotient Rule**
    $\frac{d}{dx}\left( \frac{u}{v} \right)=\frac{v \frac{du}{dx} - u \frac{dv}{dx}}{v^{2}}$
    (Simplify the fraction first if possible)

7.  **Exponential Rule of [[Natural log]]**
    $\frac{d}{dx}(e^x) = e^x$

---

# Proofs

### Power Rule
$$ 
\displaylines{ 
\frac{d}{dx}x^{n}=\lim_{ z \to x } \frac{z^{n}-x^{n}}{z-x} \ 
= \lim_{ z \to x } (z^{n-1}+z^{n-2}x+\dots+x^{n-1}) \ 
=nx^{n-1} 
}
$$ 

### Product Rule
$$ 
\begin{aligned} 
(f(x)g(x))' &= \lim_{\Delta x \to 0} \frac{f(x+\Delta x)g(x+\Delta x) - f(x)g(x)}{\Delta x} \ 
&= \lim_{\Delta x \to 0} \frac{f(x+\Delta x)g(x+\Delta x) - f(x)g(x+\Delta x) + f(x)g(x+\Delta x) - f(x)g(x)}{\Delta x} \ 
&= \lim_{\Delta x \to 0} \left[ \frac{f(x+\Delta x) - f(x)}{\Delta x} \cdot g(x+\Delta x) + f(x) \cdot \frac{g(x+\Delta x) - g(x)}{\Delta x} \right] \ 
&= f'(x)g(x) + f(x)g'(x) 
\end{aligned} 
$$ 

### Quotient Rule
$$ 
\begin{aligned} 
\left( \frac{f(x)}{g(x)} \right)' &= \lim_{\Delta x \to 0} \frac{\frac{f(x+\Delta x)}{g(x+\Delta x)} - \frac{f(x)}{g(x)}}{\Delta x} \ 
&= \lim_{\Delta x \to 0} \frac{f(x+\Delta x)g(x) - f(x)g(x+\Delta x)}{\Delta x g(x)g(x+\Delta x)} \ 
&= \lim_{\Delta x \to 0} \frac{f(x+\Delta x)g(x) - f(x)g(x) + f(x)g(x) - f(x)g(x+\Delta x)}{\Delta x g(x)g(x+\Delta x)} \ 
&= \lim_{\Delta x \to 0} \frac{1}{g(x)g(x+\Delta x)} \left[ \frac{f(x+\Delta x) - f(x)}{\Delta x} g(x) - f(x) \frac{g(x+\Delta x) - g(x)}{\Delta x} \right] \ 
&= \frac{f'(x)g(x) - f(x)g'(x)}{[g(x)]^2} 
\end{aligned} 
$$ 

### Exponential Function ($e^x$)
Based on the limit definition $\lim_{h \to 0} \frac{e^h - 1}{h} = 1$
$$ 
\begin{aligned} 
\frac{d}{dx}(e^x) &= \lim_{h \to 0} \frac{e^{x+h} - e^x}{h} \ 
&= \lim_{h \to 0} \frac{e^x e^h - e^x}{h} \ 
&= \lim_{h \to 0} \frac{e^x(e^h - 1)}{h} \ 
&= e^x \left( \lim_{h \to 0} \frac{e^h - 1}{h} \right) \ 
&= e^x \cdot 1 \ 
&= e^x 
\end{aligned} 
$$ 
> $a=e^{h}-1, e^{h}=a+1\Rightarrow h=\ln(a+1), h\to 0\Rightarrow a\to 0$
> 1. $\lim_{ h \to 0 } \frac{h}{e^{h}-1}=\lim_{ a \to 0 } \frac{\ln(a+1)}{a}=\lim_{ a \to 0 }{(a+1)}^{\frac 1a}$
> 2. $e=\lim_{ n \to \infty }\left( 1+ \frac{1}{n} \right)^{n}\Rightarrow \lim_{ x \to 0^{+} }{(1+x)}^{\frac 1x}$
> 
> $\Rightarrow \ln(\lim_{ a \to 0 }(a+1^{\frac 1a}))=\ln e=1$
> $e^{x}\lim_{ h \to 0 } \frac{{e^{h}-1}}{h}=e^{x}$

# higher-order derivatives
$$ 
y^{(n)}= \frac{d}{dx}y^{(n-1)}= \frac{d^{n}y}{dx^{n}}=D^{n}y 
$$ 

# The Derivative as a Rate Change
- position (on the line) $x=f(t)$
- displacement $s=f(t+\Delta t)-f(t)=\Delta x$
- velocity $\frac{ds}{dt}$
- speed $|v(t)|=|\frac{ds}{dt}|$
- acceleration $a=a(t)=\frac{dv}{dt}= \frac{d^{2}s}{dt^{2}}$
- jerk $\frac{da}{dt}= \frac{d^{3}s}{dt^{3}}$

# Derivatives of Trigonometric functions
$$ 
\frac{d}{dx}\sin x=\cos x 
$$ 
pf.
$$ 
\frac{d}{dx}\sin x= \lim_{ h \to 0 } \frac{\sin(x+h)-\sin x}{h}
=\lim_{ h \to 0 } \frac{1}{h}(\sin x\cos(h-1)+\sin h \cos x)
=\cos x 
$$ 
---
$$ 
\frac{d}{dx}\cos x=-\sin x 
$$ 

推:
$\tan'x= \left( \frac{\sin x}{\cos x} \right)'$
$\frac{d}{dx}\sec x= \left( \frac {1}{\cos x} \right)'$
...


> [!NOTE] 實用(?)公式
> 1. $\lim_{ x \to 0 } \frac{\sin x}x =1$
> 2. $\lim_{ x \to 0 }\frac{1-\cos x}x =0$
> 3. $\lim_{ x \to 0 }\frac{1-\cos x}{x^{2}}=\frac{1}{2}$

# The [[Chain Rule]]
連鎖律
$$ 
f\circ g=f(g(x)) 
$$ 
$$\frac{d}{dx}f(g(x))=f'(g(x))\cdot g'(x)$$ 