---
tags:
  - Physics
up:
  - "[[2D motion]]"
  - 圓周運動
  - 向心力
related:
annotation:
aliases:
  - UCM
---
# 等速率圓周運動 (Uniform Circular Motion)
>in inertial reference frame

1.  frequency (Hz)
    $f = \text{revolutions/sec}$
2.  period
    $T=f^{-1}$
3.  velocity
    $V= \frac{2\pi R}{T}=2\pi Rf=\omega \cdot R$
4.  angular velocity
    $\omega= 2\pi f=\frac{2\pi}{T}$
5.  [[#向心加速度 (Centripetal Acceleration) 推導|radial/centripetal acceleration]]
    $a_{c}=\frac{V^{2}}{R}=\omega^{2}R$
6.  tangential acceleration
    $a_{T}=0$

## 向心加速度 (Centripetal Acceleration) 推導

此處推導向心加速度公式 $a_c = v^2/R$。

1.  **位置向量**: 一個在半徑為 R 的圓上以角速度 $\omega$ 運動的質點，其位置可表示為：
    $$ \vec{r}(t) = R\cos(\omega t)\hat{i} + R\sin(\omega t)\hat{j} $$ 
2.  **速度向量**: 將位置對時間微分一次 (其中 $v = \omega R$)：
    $$ \vec{v}(t) = \frac{d\vec{r}}{dt} = -R\omega\sin(\omega t)\hat{i} + R\omega\cos(\omega t)\hat{j} $$ 
    速度量值 $\lVert\vec{v}\rVert = \sqrt{(-R\omega\sin(\omega t))^2 + (R\omega\cos(\omega t))^2} = R\omega = v$ (定值)。
3.  **加速度向量**: 將速度對時間再微分一次：
    $$ \vec{a}(t) = \frac{d\vec{v}}{dt} = -R\omega^2\cos(\omega t)\hat{i} - R\omega^2\sin(\omega t)\hat{j} $$ 
4.  **結果分析**:
    - 將 $-\omega^2$ 提出：
      $$ \vec{a}(t) = -\omega^2 \underbrace{(R\cos(\omega t)\hat{i} + R\sin(\omega t)\hat{j})}_{\vec{r}(t)} = -\omega^2\vec{r}(t) $$ 
      此結果表示加速度向量的方向永遠與位置向量**相反**，即永遠指向圓心。
    - 計算加速度量值：
      $$ \lVert\vec{a}\rVert = |-\omega^2| \cdot \lVert\vec{r}\rVert = \omega^2 R $$ 
    - 用 $v=R\omega \implies \omega = v/R$ 代換 $\omega$：
      $$ a_c = \lVert\vec{a}\rVert = \left(\frac{v}{R}\right)^2 R = \frac{v^2}{R} $$ 

## 向心力 (Centripetal Force)
- 根據牛頓第二運動定律
> $F=ma$
- 使物體進行圓周運動的合力,稱為向心力
- 其方向恆指向圓心,與向心加速度相同
> $F_c = m a_c$
- 代入向心加速度的公式可得
> $F_c = m \frac{v^2}{R} = m \omega^2 R$
