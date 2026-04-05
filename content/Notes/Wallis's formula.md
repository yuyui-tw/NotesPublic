---
aliases:
  - Wallis Formula
  - Wallis Product
  - 華里士公式
  - 華里士乘積
tags:
  - Math
up:
  - "[[definite integral|定積分]]"
related:
  - "[[Trigonometric Integral|三角函數積分]]"
annotation: 一個用於計算圓周率或特定三角函數定積分的公式，通常表示為無限乘積。
---

# 華里士公式 (Wallis's Formula)

## 1. 導論 (Introduction & Background)
華里士公式 (Wallis's Formula)，亦稱華里士乘積 (Wallis Product)，是微積分 (Calculus) 領域中一個著名的數學結果。它提供了一種以無限乘積 (infinite product) 形式表達圓周率 (pi, $\pi$) 的方法。此外，此公式與特定形式的三角函數 (trigonometric functions) 定積分 (definite integral) 計算有密切關聯，尤其在處理 $\sin^n x$ 或 $\cos^n x$ 在區間 $[0, \frac{\pi}{2}]$ 上的積分時極為關鍵。華里士公式在數學分析 (mathematical analysis) 和理論物理學 (theoretical physics) 中均有重要應用。

>不論n為奇數或偶數，一律先寫分母，分子插空隙。

## 2. 核心 (Core Framework)
華里士公式主要呈現為兩種相互關聯的形式：

### 圓周率的無限乘積形式
這個表達式直接給出了 $\frac{\pi}{2}$ 的無限乘積：
$$ \frac{\pi}{2} = \prod_{n=1}^{\infty} \frac{(2n)^2}{(2n-1)(2n+1)} = \frac{2 \cdot 2}{1 \cdot 3} \cdot \frac{4 \cdot 4}{3 \cdot 5} \cdot \frac{6 \cdot 6}{5 \cdot 7} \cdots $$

### 廣義華里士積分 (Wallis Integrals)
華里士公式通常是透過對以下形式的定積分 $I_n$ 或 $J_n$ 進行分析而導出的：
$$ I_n = \int_0^{\frac{\pi}{2}} \sin^n x \, dx $$
或
$$ J_n = \int_0^{\frac{\pi}{2}} \cos^n x \, dx $$
其中 $n$ 是一個非負整數 (non-negative integer)。由於三角恆等式 $\sin(\frac{\pi}{2}-x) = \cos x$，因此 $I_n = J_n$。

對於 $n \ge 2$，這些積分滿足一個遞迴關係 (recurrence relation)：
$$ I_n = \frac{n-1}{n} I_{n-2} $$

根據 $n$ 的奇偶性，其積分值可以明確表示：
-   若 $n$ 為偶數 (even)，$n=2k$：
    $$ I_{2k} = \int_0^{\frac{\pi}{2}} \sin^{2k} x \, dx = \frac{2k-1}{2k} \cdot \frac{2k-3}{2k-2} \cdots \frac{1}{2} \cdot \frac{\pi}{2} $$
-   若 $n$ 為奇數 (odd)，$n=2k+1$：
    $$ I_{2k+1} = \int_0^{\frac{\pi}{2}} \sin^{2k+1} x \, dx = \frac{2k}{2k+1} \cdot \frac{2k-2}{2k-1} \cdots \frac{2}{3} \cdot 1 $$

## 3. 邏輯 (Operational Logic)
華里士積分的遞迴關係是利用分部積分法 (integration by parts) 導出的。以 $I_n = \int_0^{\frac{\pi}{2}} \sin^n x \, dx$ 為例：
1.  將被積分函數分解為 $\sin^n x = \sin^{n-1} x \cdot \sin x$。
2.  應用分部積分公式 $\int u \, dv = uv - \int v \, du$，其中設 $u = \sin^{n-1} x$ 且 $dv = \sin x \, dx$。則 $du = (n-1)\sin^{n-2} x \cos x \, dx$ 且 $v = -\cos x$。
3.  代入公式後，邊界項 $[uv]_0^{\frac{\pi}{2}} = [-\sin^{n-1} x \cos x]_0^{\frac{\pi}{2}}$ 等於 $0$ (對於 $n \ge 1$)。積分部分變為：
    $$ I_n = -\int_0^{\frac{\pi}{2}} (- \cos x)(n-1)\sin^{n-2} x \cos x \, dx = (n-1) \int_0^{\frac{\pi}{2}} \sin^{n-2} x \cos^2 x \, dx $$
4.  使用三角恆等式 $\cos^2 x = 1 - \sin^2 x$ 進行替換：
    $$ I_n = (n-1) \int_0^{\frac{\pi}{2}} \sin^{n-2} x (1 - \sin^2 x) \, dx $$
    $$ I_n = (n-1) \left( \int_0^{\frac{\pi}{2}} \sin^{n-2} x \, dx - \int_0^{\frac{\pi}{2}} \sin^n x \, dx 
\right) $$
    $$ I_n = (n-1) (I_{n-2} - I_n) $$
5.  重新整理此等式，即可得到遞迴關係：
    $$ n I_n = (n-1)I_{n-2} \implies I_n = \frac{n-1}{n} I_{n-2} $$
這個遞迴關係是推導出圓周率無限乘積形式的基礎。透過分析 $I_n$ 和 $I_{n-1}$ 在 $n 	o \infty$ 時的比值，並結合夾擠定理 (Squeeze Theorem) 和廣義華里士積分的行為，最終可以導出華里士公式的無限乘積形式。

## 4. 應用與脈絡 (Application & Context)
華里士公式及其相關積分在多個數學及科學領域中均有重要應用：
-   **斯特林近似 (Stirling's Approximation)**：華里士公式是推導階乘函數 (factorial function) 大數近似，即斯特林近似公式的關鍵步驟之一。
-   **量子力學 (Quantum Mechanics)**：在量子力學中，華里士積分可用於計算某些波函數 (wave function) 的正交性 (orthogonality) 和歸一化 (normalization) 積分。
-   **概率論 (Probability Theory)**：在計算一些概率分佈 (probability distributions) 的常數項時，尤其涉及正弦或餘弦函數的冪次時，華里士積分會自然出現。
-   **歷史意義 (Historical Significance)**：約翰·華里士 (John Wallis) 於1655年首次發表此公式，是微積分早期發展中的重要成果。它展現了當時數學家在缺乏現代微積分形式化工具下解決複雜問題的卓越能力，也為後來艾薩克·牛頓 (Isaac Newton) 和戈特弗里德·萊布尼茲 (Gottfried Leibniz) 的微積分奠基工作提供了重要的啟發。
