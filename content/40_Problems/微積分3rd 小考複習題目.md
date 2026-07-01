---
tags:
  - QuizReview
  - Math
---

# 微積分3rd 小考複習題目

**Related Topics:**
- [[Monotonic functions & the first derivative test]]
- [[Concavity & curve sketching]]
- [[羅必達法則]]
- [[Antiderivative]]
- [[Integral]]
- [[Inverse Trigonometric function]], [[Derivative of inverse function & Logarithms]]
- [[Implicit Differentiation]]
- [[Extrem Values of Functions on closed Intervals]]、[[均值定理|The Mean Value Theorem]]

---

## Q1
$$
f'(x)=(\sin x-1)(2\cos x + 1), 0\le x\le 2\pi
$$
a. What are the critical points of f?
b. On what open intervals is f increasing or decreasing?
c. At what points, if any, does f assume local maximum or minimum values?

### A1
**a. 臨界點 (Critical points):**
臨界點發生在 $f'(x) = 0$ 的地方。
- $\sin(x) - 1 = 0 \implies \sin(x) = 1 \implies x = \pi/2$
- $2\cos(x) + 1 = 0 \implies \cos(x) = -1/2 \implies x = 2\pi/3$ 和 $x = 4\pi/3$

所以臨界點為 $x = \pi/2, 2\pi/3, 4\pi/3$。

**b. 遞增/遞減區間 (Increasing/decreasing intervals):**
我們需要分析 $f'(x)$ 的正負。
- $(\sin(x) - 1)$ 這一項，在 $0 \le x \le 2\pi$ 的範圍內，除了 $x = \pi/2$ 時等於0，其餘時候恆為負。
- 因此，$f'(x)$ 的正負由 $(2\cos(x) + 1)$ 決定。
- **遞增 (f increasing, $f'(x) > 0$):** 當 $2\cos(x) + 1 < 0$，即 $\cos(x) < -1/2$。這發生在區間 $(2\pi/3, 4\pi/3)$。
- **遞減 (f decreasing, $f'(x) < 0$):** 當 $2\cos(x) + 1 > 0$，即 $\cos(x) > -1/2$。這發生在區間 $(0, 2\pi/3)$ 和 $(4\pi/3, 2\pi)$。

**c. 局部極大/極小值 (Local maximum/minimum):**
- 在 $x = 2\pi/3$，$f'(x)$ 由負轉正，故 $f$ 在此處有局部極小值。
- 在 $x = 4\pi/3$，$f'(x)$ 由正轉負，故 $f$ 在此處有局部極大值。
- 在 $x = \pi/2$，$f'(x)$ 未變號（左右皆為負），故此處不是局部極值點，而是一個水平切線點。

---

## Q2
a. Find the open intervals on which the function is increasing and those on which it is decreasing.
b. Identify the function's local extreme values, if any, saying where they occur.

1.  **$h(x)=x^{1/3}(x^{2}-4)$**
2.  **$f(x)=e^{2x}+e^{-x}$**

### A2
**1. $h(x) = x^{7/3} - 4x^{1/3}$**

*   **a. 遞增/遞減區間:**
    - 微分: $h'(x) = \frac{7}{3}x^{4/3} - \frac{4}{3}x^{-2/3} = \frac{1}{3}x^{-2/3}(7x^2 - 4)$
    - 臨界點: $h'(x) = 0$ 發生在 $7x^2 - 4 = 0$，即 $x = \pm 2/\sqrt{7}$。$h'(x)$ 在 $x = 0$ 未定義。
    - $x^{-2/3}$ 恆為正，所以 $h'(x)$ 的符號由 $(7x^2 - 4)$ 決定。
    - **遞增 ($h'(x) > 0$):** $x^2 > 4/7 \implies (-\infty, -2/\sqrt{7})$ 和 $(2/\sqrt{7}, \infty)$。
    - **遞減 ($h'(x) < 0$):** $x^2 < 4/7 \implies (-2/\sqrt{7}, 0)$ 和 $(0, 2/\sqrt{7})$。

*   **b. 局部極值:**
    - 在 $x = -2/\sqrt{7}$，$h'(x)$ 由正轉負，有局部極大值。
    - 在 $x = 2/\sqrt{7}$，$h'(x)$ 由負轉正，有局部極小值。
    - 在 $x = 0$，導數未定義，但函數在該點兩側皆為遞減，故不是極值點（是一個垂直切線點）。

**2. $f(x) = e^{2x} + e^{-x}$**

*   **a. 遞增/遞減區間:**
    - 微分: $f'(x) = 2e^{2x} - e^{-x}$
    - 臨界點: $f'(x) = 0 \implies 2e^{2x} = e^{-x} \implies 2 = e^{-3x} \implies \ln(2) = -3x \implies x = -\ln(2)/3$。
    - **遞減 ($f'(x) < 0$):** 當 $x < -\ln(2)/3$，區間為 $(-\infty, -\ln(2)/3)$。
    - **遞增 ($f'(x) > 0$):** 當 $x > -\ln(2)/3$，區間為 $(-\ln(2)/3, \infty)$。

*   **b. 局部極值:**
    - 在 $x = -\ln(2)/3$，$f'(x)$ 由負轉正，有局部極小值。此函數沒有局部極大值。

---

## Q3
Identify the function's local extreme values in the given domain, and say where they occur. Then Graph the function over given domain. Which of the extreme values, if any, are absolute?
$$ h(x)=\frac{x^{3}}{3}-2x^{2}+4x, 0\le x < \infty $$

### A3
- **求導:** $h'(x) = x^2 - 4x + 4 = (x - 2)^2$
- **臨界點:** $h'(x) = 0$ 發生在 $x = 2$。
- **單調性分析:** 
    - 因為 $h'(x) = (x - 2)^2 \ge 0$，所以函數 $h(x)$ 在其定義域 $[0, \infty)$ 上是嚴格遞增的。
    - 在 $x = 2$ 是一個水平切線的拐點，但不是局部極值點。
- **極值分析:** 
    - **局部極值:** 無。
    - **絕對極值:** 
        - 因為函數在 $[0, \infty)$ 上嚴格遞增，最小值必定發生在區間的起點。
        - **絕對極小值** 發生在 $x = 0$，$h(0) = 0$。
        - 因為函數趨近於無窮大，所以**沒有絕對極大值**。
- **圖形描述:** 
    - 函數圖形從原點 $(0, 0)$ 開始。
    - 隨著 $x$ 增加，圖形一直向上攀升。
    - 在 $x = 2$ 的地方，切線斜率為0，圖形暫時變平，形成一個拐點，然後繼續向上攀升。

---

## Q4
Find the local extrema of each function on the given interval, and say where they occur. Then Graph the function and its derivative together. Comment on the behavior of f in relation to the signs and values of f'.
$$ f(x)=\sqrt{ 3 }\cos x+\sin x, 0\le x\le 2\pi $$

### A4
- **函數疊合(函數視為極座標系統):**
    - 使用 R-form，$f(x) = R\sin(x + \alpha)$。$R = \sqrt{(\sqrt{3})^2 + 1^2} = 2$。
    - $f(x) = 2( \frac{\sqrt{3}}{2}\cos(x) + \frac{1}{2}\sin(x) ) = 2( \sin(\pi/3)\cos(x) + \cos(\pi/3)\sin(x) ) = 2\sin(x + \pi/3)$。
    - **其結果可幫助繪圖**
- **求導:**
    - $f'(x) = -\sqrt{3} \sin(x) + \cos(x)$。
- **臨界點:**
    - $f'(x) = 0 \implies \cos(x) = \sqrt{3} \sin(x) \implies \tan(x) = 1/\sqrt{3}$。
    - 在 $[0, 2\pi]$ 中，解得 $x = \pi/6$ 和 $x = 7\pi/6$。
- **極值分析 (使用二階導數):**
    - $f''(x) = -\sqrt{3} \cos(x) - \sin(x) = -f(x)$。
    - $f''(\pi/6) = -f(\pi/6) = -2\sin(\pi/6 + \pi/3) = -2\sin(\pi/2) = -2 < 0$。故在 $x = \pi/6$ 有**局部極大值**，$f(\pi/6) = 2$。
    - $f''(7\pi/6) = -f(7\pi/6) = -2\sin(7\pi/6 + \pi/3) = -2\sin(3\pi/2) = 2 > 0$。故在 $x = 7\pi/6$ 有**局部極小值**，$f(7\pi/6) = -2$。
- **圖形與關係:**
    - $f(x)$ 的圖形是一個振幅為2、向左平移 $\pi/3$ 的正弦波。
    - $f'(x)$ 的圖形是一個餘弦波。
    - **關係:**
        - 當 $f'(x) > 0$ (導數為正) 時，$f(x)$ 的圖形是遞增的。
        - 當 $f'(x) < 0$ (導數為負) 時，$f(x)$ 的圖形是遞減的。
        - 當 $f'(x) = 0$ (導數為零) 時，$f(x)$ 達到局部極值點（極大值或極小值）。

---

## Q5
Use the function below to explain how to graph by useing approprite methods.
1.  $y=\frac{x^{2}}{x+1}$
2.  $y= x+\sin x, 0\le x\le 2\pi$
3.  $y=\ln(3-x^{2})$

### A5
**1. $y = x^2 / (x+1)$**
1.  **定義域:** $x \neq -1$。
2.  **對稱性:** 無。
3.  **截距:** $(0, 0)$ 是唯一的 x 截距和 y 截距。
4.  **漸近線:**
    - **垂直漸近線:** $x = -1$。
    - **斜漸近線:** 使用長除法 $x^2 / (x+1) = (x-1) + 1/(x+1)$，所以斜漸近線是 $y = x-1$。
5.  **一階導數分析 (單調性 & 極值):**
    - $y' = \frac{x(x+2)}{(x+1)^2}$。
    - 臨界點: $x = 0, -2$。
    - 遞增區間: $(-\infty, -2)$ 和 $(0, \infty)$。
    - 遞減區間: $(-2, -1)$ 和 $(-1, 0)$。
    - 局部極大值: $(-2, -4)$。
    - 局部極小值: $(0, 0)$。
6.  **二階導數分析 (凹性 & 拐點):**
    - $y'' = 2 / (x+1)^3$。
    - $y''$ 永不為0，無拐點。
    - 凹向上區間 ($y'' > 0$): $x > -1$，即 $(-1, \infty)$。
    - 凹向下區間 ($y'' < 0$): $x < -1$，即 $(-\infty, -1)$。
7.  **繪圖:** 結合以上資訊，先畫出漸近線和關鍵點，再根據單調性和凹性連接曲線。

**2. $y = x + \sin(x), 0 \le x \le 2\pi$**
1.  **定義域:** $[0, 2\pi]$。
2.  **一階導數分析:**
    - $y' = 1 + \cos(x)$。
    - 因為 $\cos(x) \ge -1$，所以 $y' \ge 0$ 恆成立。函數總是遞增的。
    - 臨界點: $y' = 0$ 發生在 $\cos(x) = -1$，即 $x = \pi$。此處為水平切線。
3.  **二階導數分析:**
    - $y'' = -\sin(x)$。
    - $y'' = 0$ 發生在 $x = 0, \pi, 2\pi$。
    - 凹向下 ($y'' < 0$): $\sin(x) > 0$，在 $(0, \pi)$。
    - 凹向上 ($y'' > 0$): $\sin(x) < 0$，在 $(\pi, 2\pi)$。
    - 拐點: $(\pi, \pi)$。
4.  **繪圖:** 圖形類似於直線 $y=x$，但在 $(0, \pi)$ 區間稍微向下彎曲，在 $(\pi, 2\pi)$ 區間向上彎曲。它從 $(0,0)$ 開始，單調遞增至 $(2\pi, 2\pi)$，並在 $(\pi, \pi)$ 處有水平拐點。

**3. $y = \ln(3 - x^2)$**
1.  **定義域:** $3 - x^2 > 0 \implies x^2 < 3 \implies (-\sqrt{3}, \sqrt{3})$。
2.  **對稱性:** $y(-x) = y(x)$，為偶函數，圖形對稱於 y 軸。
3.  **漸近線:** **垂直漸近線**在 $x = \sqrt{3}$ 和 $x = -\sqrt{3}$。
4.  **一階導數分析:**
    - $y' = -2x / (3 - x^2)$。
    - 臨界點: $x = 0$。
    - 遞增區間 ($y' > 0$): $(-\sqrt{3}, 0)$。
    - 遞減區間 ($y' < 0$): $(0, \sqrt{3})$。
    - 局部極大值 (也是絕對極大值): $(0, \ln(3))$。
5.  **二階導數分析:**
    - $y'' = -(2x^2 + 6) / (3 - x^2)^2$。
    - 在定義域內，分子恆負，分母恆正，所以 $y'' < 0$。
    - 圖形總是**凹向下**，無拐點。
6.  **繪圖:** 圖形是一個對稱於 y 軸的鐘形曲線，頂點在 $(0, \ln(3))$，並在 $x = \pm\sqrt{3}$ 處趨近於負無窮。

---

## Q6
Use L'Hôpital's rule to find the limits.
1.  $\lim_{ x \to \infty } (\ln 2x-\ln(x+1))$
2.  $\lim_{ x \to 0^{+} } \frac{(\ln x)^{2}}{\ln(\sin x)}$
3.  $\lim_{ x \to 1^{+} } \left( \frac{1}{x-1}- \frac{1}{\ln x} \right)$

### A6
**1. $\lim_{x\to\infty} (\ln(2x) - \ln(x+1))$**
- **形式:** $\infty - \infty$ (不定型)。
- **步驟:**
  1. 合併對數: $\lim_{x\to\infty} \ln(\frac{2x}{x+1})$
  2. 利用對數函數的連續性: $\ln( \lim_{x\to\infty} \frac{2x}{x+1} )$
  3. 計算內部極限 (分子分母同除以x): $\lim_{x\to\infty} \frac{2}{1 + 1/x} = \frac{2}{1 + 0} = 2$
  4. **答案:** $\ln(2)$

**2. $\lim_{x\to 0^+} \frac{(\ln x)^2}{\ln(\sin x)}$**
- **形式:** $\infty / - \infty$ (不定型)。
- **步驟:**
  1. 使用羅必達法則:
     $$ \lim_{x\to 0^+} \frac{2(\ln x) \cdot \frac{1}{x}}{\frac{1}{\sin x} \cdot \cos x} = \lim_{x\to 0^+} \frac{2\ln x}{x \cot x} $$
     這比較複雜。我們換個思路。
  2. 代換: $\ln(\sin x) = \ln(x \cdot \frac{\sin x}{x}) = \ln(x) + \ln(\frac{\sin x}{x})$。
  3. 原式變為: $\lim_{x\to 0^+} \frac{(\ln x)^2}{\ln(x) + \ln(\frac{\sin x}{x})}$
  4. 分子分母同除以 $\ln(x)$: $\lim_{x\to 0^+} \frac{\ln x}{1 + \frac{\ln(\sin x/x)}{\ln x}}$
  5. 當 $x\to 0^+$ 時, $\sin(x)/x \to 1$，所以 $\ln(\sin x/x) \to \ln(1) = 0$。
  6. 分母部分 $\frac{\ln(\sin x/x)}{\ln x} \to \frac{0}{-\infty} = 0$。
  7. 極限變為: $\lim_{x\to 0^+} \frac{\ln x}{1 + 0} = \lim_{x\to 0^+} \ln x$
>自然對數圖形參考[[graph of natural logarithms.png]]

  8. **答案:** $-\infty$

**3. $\lim_{x\to 1^+} ( \frac{1}{x-1} - \frac{1}{\ln x} )$**
- **形式:** $\infty - \infty$ (不定型)。
- **步驟:**
  1. 通分: $\lim_{x\to 1^+} \frac{\ln(x) - (x-1)}{(x-1)\ln(x)}$。此時為 $0/0$ 形式。
  2. **應用羅必達法則:**
     - 分子微分: $\frac{d}{dx}(\ln(x) - x + 1) = \frac{1}{x} - 1$
     - 分母微分: $\frac{d}{dx}((x-1)\ln(x)) = 1 \cdot \ln(x) + (x-1) \cdot \frac{1}{x} = \ln(x) + 1 - \frac{1}{x}$
  3. 新的極限: $\lim_{x\to 1^+} \frac{1/x - 1}{\ln(x) + 1 - 1/x}$。仍然是 $0/0$ 形式。
  4. **再次應用羅必達法則:**
     - 分子微分: $\frac{d}{dx}(\frac{1}{x} - 1) = -\frac{1}{x^2}$
     - 分母微分: $\frac{d}{dx}(\ln(x) + 1 - \frac{1}{x}) = \frac{1}{x} + \frac{1}{x^2}$
  5. 代入 $x=1$: $\frac{-1/1^2}{1/1 + 1/1^2} = \frac{-1}{1+1}$
  6. **答案:** $-1/2$

---

## Q7
Find the limit of
$$ \lim_{ x \to 0^{+} } x^{x} $$

### A7
- **形式:** $0^0$ (不定型)。
- **步驟:**
  1. 設 $y = x^x$，取自然對數: $\ln(y) = \ln(x^x) = x \ln(x)$。
  2. 計算 $\ln(y)$ 的極限: $\lim_{x\to 0^+} x \ln(x)$。此為 $0 \cdot (-\infty)$ 形式。
  3. 轉換形式以便使用羅必達法則: $\lim_{x\to 0^+} \frac{\ln(x)}{1/x}$。此為 $-\infty / \infty$ 形式。
  4. **應用羅必達法則:**
     - 分子微分: $\frac{d}{dx}(\ln x) = 1/x$
     - 分母微分: $\frac{d}{dx}(1/x) = -1/x^2$
  5. 新的極限: $\lim_{x\to 0^+} \frac{1/x}{-1/x^2} = \lim_{x\to 0^+} -x = 0$。
  6. 我們得到 $\lim_{x\to 0^+} \ln(y) = 0$。
  7. 因此, $\lim_{x\to 0^+} y = e^0$。
  8. **答案:** $1$

---

## Q8
L'Hôpital's rule does not help with the limits , may keep on cycling. Find the limits some other way.
$$ \lim_{ x \to \infty } \frac{e^{x^{2}}}{xe^{x}} $$

### A8
- **分析:** 雖然羅必達法則可用，但比較函數的增長率更為直觀。
- **步驟:**
  1. **化簡表達式:** $\lim_{x\to\infty} \frac{1}{x} \cdot e^{x^2 - x}$。
  2. **比較增長率:**
     - 指數部分 $x^2 - x$當 $x\to\infty$ 時，趨近於 $\infty$。
     - 指數函數 $e^{x^2 - x}$ 的增長速度遠遠快於任何多項式函數，包括 $x$。
     - 雖然 $1/x$ 趨近於 0，但 $e^{x^2 - x}$ 趨近於 $\infty$ 的速度是壓倒性的。
  3. **結論:** 整個表達式 $\frac{e^{x^2-x}}{x}$ 會因為分子爆炸性的增長而趨近於無窮大。
  4. **答案:** $\infty$

---

## Q9
Find the most general antiderivative of indefinite integral. You may need to try a solution and then adjust your guess. Check your answers by differentiation.
1.  $\int\left( \frac{1}{x^{2}}-x^{2}- \frac{1}{3} \right)dx$
2.  $\int \cos \theta(\tan \theta+\sec \theta)d\theta$

### A9
**1. $\int( \frac{1}{x^2} - x^2 - \frac{1}{3} ) dx$**
- **步驟:**
  1. 將表達式改寫為冪函數形式: $\int(x^{-2} - x^2 - \frac{1}{3}) dx$
  2. 使用==冪函數積分法則==^[寫這個對於計算積分好像蠻有幫助的] $\int x^n dx = \frac{x^{n+1}}{n+1}$:
     - $\int x^{-2} dx = \frac{x^{-1}}{-1} = -1/x$
     - $\int -x^2 dx = -\frac{x^3}{3}$
     - $\int -\frac{1}{3} dx = -\frac{1}{3}x$
  3. 合併結果並加上常數 $C$。
- **答案:** $-\frac{1}{x} - \frac{x^3}{3} - \frac{x}{3} + C$

**2. $\int \cos\theta(\tan\theta + \sec\theta) d\theta$**
- **步驟:**
  1. 化簡被積函數: $\cos\theta \cdot (\frac{\sin\theta}{\cos\theta} + \frac{1}{\cos\theta})$
  2. $\cos\theta \cdot (\frac{\sin\theta}{\cos\theta}) + \cos\theta \cdot (\frac{1}{\cos\theta}) = \sin\theta + 1$
  3. 積分: $\int(\sin\theta + 1) d\theta$
     - $\int \sin\theta d\theta = -\cos\theta$
     - $\int 1 d\theta = \theta$
  4. 合併結果並加上常數 $C$。
- **答案:** $-\cos\theta + \theta + C$

---

## Q10
Solve the initial value problems.
$$ \frac{dv}{dt}= \frac{3}{t\sqrt{ t^{2}-1 }},\ t >1 ,\ v(2)=0 $$

### A10
- **分析:** 被積函數的形式 $\frac{1}{t\sqrt{t^2-1}}$ 是 $\text{arcsec}(t)$ 的導數。
- **步驟:**
  1. **求不定積分:**
     - $v(t) = \int \frac{3}{t\sqrt{t^2-1}} dt$
     - $v(t) = 3 \int \frac{1}{t\sqrt{t^2-1}} dt$
     - $v(t) = 3 \text{arcsec}(t) + C$ (因為 $t>1$，所以 $|t|=t$)
  2. **使用初始值求解 C:**
     - $v(2) = 0 \implies 3 \text{arcsec}(2) + C = 0$
     - $\text{arcsec}(2)$ 是 $\sec(\theta) = 2$ 的角度 $\theta$，即 $\cos(\theta) = 1/2$。在 $\text{arcsec}$ 的值域 $[0, \pi/2) \cup (\pi/2, \pi]$ 中，$\theta = \pi/3$。
     - $3 \cdot (\pi/3) + C = 0$
     - $\pi + C = 0 \implies C = -\pi$
- **答案:** $v(t) = 3\text{arcsec}(t) - \pi$

END
