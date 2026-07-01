---
tags:
  - Physics
up:
  - "[[Work]]"
  - "[[kinetic energy]]"
related:
  - "[[Law of Conservation of mechanical energy]]"
aliases:
  - 功能定理
annotation:
---
# 功能定理 (Work-Energy Theorem)
> 合力 (Net Force) 對一個質點所作的功 (Net Work), 等於該質點動能 (Kinetic Energy) 的變化量
$$
W_{net} = \Delta K = K_f - K_i
$$
- 這是一個從牛頓第二定律直接導出的普遍定理
- 它建立了「功」與「動能變化」之間的直接聯繫, 為動力學問題提供了另一種分析視角

## 一般推導 (General Derivation)
- 從功的積分定律與牛頓第二定律出發
$$
W_{net} = \int_{x_i}^{x_f} F_{net} \,dx = \int_{x_i}^{x_f} m a \,dx
$$
- 運用連鎖律 (Chain Rule) 變換積分變數
> $a = \frac{dv}{dt} = \frac{dv}{dx}\frac{dx}{dt} = v\frac{dv}{dx} \implies a\,dx = v\,dv$
$$
W_{net} = \int_{v_i}^{v_f} m v \,dv
$$
- 對速度積分即得
$$
W_{net} = \left[ \frac{1}{2}mv^2 \right]_{v_i}^{v_f} = \frac{1}{2}mv_f^2 - \frac{1}{2}mv_i^2 = \Delta K
$$

## 與機械能守恆的關係
功能定理是比 [[Law of Conservation of mechanical energy|機械能守恆定律]] 更廣義的定理
將總功 $W_{net}$ 分解為保守力作功 $W_c$ 與非保守力作功 $W_{nc}$
$$
W_{net} = W_c + W_{nc}
$$
根據 [[Conservative force|保守力]] 與位能的關係, $W_c = -\Delta U$
代入功能定理 $W_{net} = \Delta K$
$$
W_c + W_{nc} = \Delta K
$$
$$
-\Delta U + W_{nc} = \Delta K
$$
移項可得
$$
W_{nc} = \Delta K + \Delta U = \Delta E_{mech}
$$
- 此式表明, **非保守力所作的功等於總機械能的變化量**
- 當 $W_{nc} = 0$ 時, $\Delta E_{mech} = 0$, 這就是機械能守恆定律

## 常見運用
- 當不關心過程時間, 只關心初末狀態的速度與受力作功時, 功能定理特別有用
- 尤其適用於計算變力作功所造成的速度變化