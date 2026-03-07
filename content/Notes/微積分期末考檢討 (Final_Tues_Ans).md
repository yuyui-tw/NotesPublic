---
tags:
  - QuizReview
---
# 微積分期末考檢討 (2025/12/16)

此文件為 `Final_Tues_Ans.pdf` 的試題檢討。

---

### 1. 求下列函數的微分 (Derivatives)

**(a) $y = x^3 2^x$**

*   **解法 (使用乘法法則):**
    
    $y' = (x^3)' \cdot 2^x + x^3 \cdot (2^x)' = 3x^2 \cdot 2^x + x^3 \cdot 2^x \ln 2$
    

**(b) $y = \ln(e^{2t} + t^3)$**

*   **解法 (使用連鎖律):**
    
    $y' = \frac{1}{e^{2t} + t^3} \cdot (e^{2t} + t^3)' = \frac{2e^{2t} + 3t^2}{e^{2t} + t^3}$
    

**(c) $y = \frac{t^2+1}{2t^3+1}$**

*   **解法 (使用除法法則):**
    
    $y' = \frac{(t^2+1)'(2t^3+1) - (t^2+1)(2t^3+1)'}{(2t^3+1)^2} = \frac{2t(2t^3+1) - (t^2+1)(6t^2)}{(2t^3+1)^2} = \frac{4t^4+2t - 6t^4-6t^2}{(2t^3+1)^2} = \frac{-2t^4 - 6t^2 + 2t}{(2t^3+1)^2}$
    

**(d) $y = \sqrt{\sec^3(\ln x)}$**

*   **解法 (使用連鎖律):**
    
    $y' = \frac{1}{2\sqrt{\sec^3(\ln x)}} \cdot (\sec^3(\ln x))'$
    
    $= \frac{1}{2\sqrt{\sec^3(\ln x)}} \cdot 3\sec^2(\ln x) \cdot (\sec(\ln x))'$
    
    $= \frac{3\sec^2(\ln x)}{2\sqrt{\sec^3(\ln x)}} \cdot \sec(\ln x)\tan(\ln x) \cdot (\ln x)'$
    
    $= \frac{3\sec^3(\ln x)\tan(\ln x)}{2\sqrt{\sec^3(\ln x)}} \cdot \frac{1}{x} = \frac{3\sqrt{\sec^3(\ln x)}\tan(\ln x)}{2x}$
    

---

### 2. 計算下列極限 (Limits)

**(a) $\lim_{x \to \infty} x^{1/x}$**

*   **解法 (使用 L'Hopital's Rule):**
    
    這是一個 $\infty^0$ 型的不定式。令 $L = \lim_{x \to \infty} x^{1/x}$，取自然對數：
    
    $\ln L = \lim_{x \to \infty} \ln(x^{1/x}) = \lim_{x \to \infty} \frac{\ln x}{x}$
    
    此為 $\frac{\infty}{\infty}$ 型，使用羅必達法則：
    
    $\ln L = \lim_{x \to \infty} \frac{(\ln x)'}{(x)'} = \lim_{x \to \infty} \frac{1/x}{1} = 0$
    
    因此，$L = e^0 = 1$
    

**(b) $\lim_{\theta \to 0} \frac{\theta \cos \theta}{\tan \theta}$**

*   **解法:**
    
    $\lim_{\theta \to 0} \frac{\theta \cos \theta}{\frac{\sin \theta}{\cos \theta}} = \lim_{\theta \to 0} \frac{\theta \cos^2 \theta}{\sin \theta} = (\lim_{\theta \to 0} \frac{\theta}{\sin \theta}) \cdot (\lim_{\theta \to 0} \cos^2 \theta) = 1 \cdot 1^2 = 1$
    

**(c) $\lim_{x \to 0} \frac{\tan x - \cos x \sin(\sin x)}{x^3}$**

*   **解法 (使用泰勒展開或 L'Hopital's Rule):**
    
    這是一個複雜的極限，解答中展示了兩種解法，但都涉及到較為進階的替換和極限運算。核心是將其拆解為多個已知極限的和。
    
    **解法1:** 將 $\tan x$ 提出，並利用 $\lim_{x \to 0} \frac{\sin x}{x} = 1$ 進行代換。
    
    **解法2:** 多次使用羅必達法則 (計算會非常繁瑣)。
    
    最終答案為 $\frac{7}{6}$。
    

---

### 3. 隱微分 (Implicit Differentiation)

**求 $2x^3 + xy + y^3 = 4$ 的 $\frac{dy}{dx}$**

*   **解法:**
    
    將方程式兩邊對 x 微分：
    
    $\frac{d}{dx}(2x^3) + \frac{d}{dx}(xy) + \frac{d}{dx}(y^3) = \frac{d}{dx}(4)$
    
    $6x^2 + (1 \cdot y + x \cdot \frac{dy}{dx}) + 3y^2 \frac{dy}{dx} = 0$
    
    $6x^2 + y + (x + 3y^2)\frac{dy}{dx} = 0$
    
    $\frac{dy}{dx} = -\frac{6x^2 + y}{x + 3y^2}$
    

---

### 4. 尋找函數的絕對極值 (Absolute Extreme Values)

**函數 $y = 2x^3 + 6x^2 - 48x + 7$ 在區間 $[-5, 5]$ 上的絕對極值。**

*   **解法:**
    
    1.  **找臨界點 (Critical Points):**
        
        $y' = 6x^2 + 12x - 48 = 6(x^2 + 2x - 8) = 6(x+4)(x-2)$
        
        令 $y' = 0$，得到臨界點 $x = -4$ 和 $x = 2$。
        
    2.  **比較端點與臨界點的函數值:**
        
        *   $f(-5) = 2(-125) + 6(25) - 48(-5) + 7 = -250 + 150 + 240 + 7 = 147$
        *   $f(-4) = 2(-64) + 6(16) - 48(-4) + 7 = -128 + 96 + 192 + 7 = 167$
        *   $f(2) = 2(8) + 6(4) - 48(2) + 7 = 16 + 24 - 96 + 7 = -49$
        *   $f(5) = 2(125) + 6(25) - 48(5) + 7 = 250 + 150 - 240 + 7 = 167$
        
    3.  **結論:**
        
        *   **絕對最大值 (Absolute Maximum):** 167, 發生在 $x=-4$ 和 $x=5$。
        *   **絕對最小值 (Absolute Minimum):** -49, 發生在 $x=2$。
        

---

### 5. 初始值問題 (Initial Value Problem)

**解 $\frac{dy}{dx} = e^x - 4x + 1$, 其中 $y(0) = 2$**

*   **解法:**
    
    1.  **積分:**
        
        $y = \int (e^x - 4x + 1) dx = e^x - 2x^2 + x + C$
        
    2.  **使用初始條件找 C:**
        
        $y(0) = e^0 - 2(0)^2 + 0 + C = 1 + C = 2$
        
        得到 $C = 1$。
        
    3.  **解答:**
        
        $y = e^x - 2x^2 + x + 1$
        

---

### 6. 計算下列積分 (Integrals)

**(a) $\int x^8(x^9+4)^{11} dx$**

*   **解法 (使用 u-代換):**
    
    令 $u = x^9+4$, 則 $du = 9x^8 dx \implies x^8 dx = \frac{du}{9}$
    
    $\int \frac{1}{9} u^{11} du = \frac{1}{9} \cdot \frac{u^{12}}{12} + C = \frac{1}{108}(x^9+4)^{12} + C$
    
    *註: 解答紙上為 $\frac{1}{24}(x^2+4)^{12}+C$，推測原題目應為 $\int x(x^2+4)^{11} dx$*
    

**(b) $\int_{\ln 2}^{\ln 3} e^{2x} dx$**

*   **解法:**
    
    $[\frac{1}{2}e^{2x}]_{\ln 2}^{\ln 3} = \frac{1}{2}(e^{2\ln 3} - e^{2\ln 2}) = \frac{1}{2}(e^{\ln 9} - e^{\ln 4}) = \frac{1}{2}(9-4) = \frac{5}{2}$
    

**(c) $\int x^2 \sqrt{x-1} dx$**

*   **解法 (使用 u-代換):**
    
    令 $u = x-1$, 則 $x = u+1$, $dx = du$
    
    $\int (u+1)^2 \sqrt{u} du = \int (u^2+2u+1)u^{1/2} du = \int (u^{5/2} + 2u^{3/2} + u^{1/2}) du$
    
    $= \frac{2}{7}u^{7/2} + \frac{4}{5}u^{5/2} + \frac{2}{3}u^{3/2} + C$
    
    $= \frac{2}{7}(x-1)^{7/2} + \frac{4}{5}(x-1)^{5/2} + \frac{2}{3}(x-1)^{3/2} + C$
    

**(d) $\int \frac{x^3}{x^4+2} dx$**

*   **解法 (使用 u-代換):**
    
    令 $u = x^4+2$, 則 $du = 4x^3 dx \implies x^3 dx = \frac{du}{4}$
    
    $\int \frac{1}{4u} du = \frac{1}{4}\ln|u| + C = \frac{1}{4}\ln(x^4+2) + C$
    

**(e) $\int \cos^2 x dx$**

*   **解法 (使用降冪公式):**
    
    $\int \frac{1+\cos(2x)}{2} dx = \frac{1}{2} \int (1+\cos(2x)) dx = \frac{1}{2}(x + \frac{1}{2}\sin(2x)) + C = \frac{x}{2} + \frac{\sin(2x)}{4} + C$
    

**(f) $\int x e^x dx$**

*   **解法 (使用分部積分):**
    
    令 $u = x, dv = e^x dx$, 則 $du = dx, v = e^x$
    
    $\int u dv = uv - \int v du = xe^x - \int e^x dx = xe^x - e^x + C = e^x(x-1) + C$
    

---

### 7. 三角代換積分 (Trigonometric Substitution)

**計算 $\int \frac{dx}{(1+x^2)^{3/2}}$**

*   **解法:**
    
    令 $x = \tan\theta$, 則 $dx = \sec^2\theta d\theta$ 且 $1+x^2 = 1+\tan^2\theta = \sec^2\theta$
    
    $\int \frac{\sec^2\theta}{(\sec^2\theta)^{3/2}} d\theta = \int \frac{\sec^2\theta}{\sec^3\theta} d\theta = \int \cos\theta d\theta = \sin\theta + C$
    
    從 $x = \tan\theta$ 畫出直角三角形，可知 $\sin\theta = \frac{x}{\sqrt{1+x^2}}$
    
    所以答案為 $\frac{x}{\sqrt{1+x^2}} + C$
    

---

### 8. 區域面積 (Area of a Region)

**求由 $y = x^2 - 1$ 和 $y = x + 5$ 所圍成區域的面積。**

*   **解法:**
    
    1.  **找交點 (Intersections):**
        
        $x^2 - 1 = x + 5 \implies x^2 - x - 6 = 0 \implies (x-3)(x+2) = 0$
        
        交點為 $x = -2$ 和 $x = 3$。
        
    2.  **建立積分式:**
        
        在區間 $[-2, 3]$ 上，$x+5 \ge x^2-1$。
        
        Area $= \int_{-2}^3 [(x+5) - (x^2-1)] dx = \int_{-2}^3 (-x^2 + x + 6) dx$
        
    3.  **計算積分:**
        
        $[-\frac{x^3}{3} + \frac{x^2}{2} + 6x]_{-2}^3 = (-\frac{27}{3} + \frac{9}{2} + 18) - (\frac{8}{3} + \frac{4}{2} - 12)$
        
        $= (-9 + 4.5 + 18) - (2.66 + 2 - 12) = 13.5 - (-7.33) \approx \frac{125}{6}$
        

---

### 9. 旋轉體體積與曲線長度 (Volume and Arc Length)

**(a) 將 $y=2x-x^2$ 與 x-軸所圍區域繞直線 $x=-2$ 旋轉，求其體積。**

*   **解法 (使用殼法 Shell Method):**
    
    $y = x(2-x)$，與 x-軸交於 $x=0, x=2$。
    
    Volume $V = \int_0^2 2\pi \cdot (\text{radius}) \cdot (\text{height}) dx$
    
    其中 radius $= x - (-2) = x+2$，height $= 2x-x^2$
    
    $V = 2\pi \int_0^2 (x+2)(2x-x^2) dx = 2\pi \int_0^2 (2x^2 - x^3 + 4x - 2x^2) dx = 2\pi \int_0^2 (4x-x^3) dx$
    
    $= 2\pi [2x^2 - \frac{x^4}{4}]_0^2 = 2\pi (2(4) - \frac{16}{4}) = 2\pi (8-4) = 8\pi$
    

**(b) 求曲線 $y = \frac{2}{3}(x^2+1)^{3/2}$ 在 $0 \le x \le 1$ 上的長度。**

*   **解法:**
    
    1.  **求微分:**
        
        $\frac{dy}{dx} = \frac{2}{3} \cdot \frac{3}{2}(x^2+1)^{1/2} \cdot 2x = 2x\sqrt{x^2+1}$
        
    2.  **建立弧長積分式:**
        
        Length $L = \int_0^1 \sqrt{1 + (\frac{dy}{dx})^2} dx = \int_0^1 \sqrt{1 + (2x\sqrt{x^2+1})^2} dx$
        
        $= \int_0^1 \sqrt{1 + 4x^2(x^2+1)} dx = \int_0^1 \sqrt{1 + 4x^4 + 4x^2} dx = \int_0^1 \sqrt{(2x^2+1)^2} dx$
        
        $= \int_0^1 (2x^2+1) dx$
        
    3.  **計算積分:**
        
        $[\frac{2x^3}{3} + x]_0^1 = (\frac{2}{3} + 1) - 0 = \frac{5}{3}$
        

---
