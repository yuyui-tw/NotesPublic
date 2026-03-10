---
aliases:
  - Flight Path Optimization
  - TSP Python
tags:
  - Math
  - computer-science
up:
related:
annotation:
---
# 專案目標：飛機最短路徑計算方案

本專案旨在解決一個帶有**不對稱權重**的**旅行推銷員問題 (TSP)**。
已知多個機場的經緯度座標，計算從某一啟始點出發，遍歷所有城市後回到原點的最短飛行時間（考慮地球自轉對航速的影響）。

## 1. 數學原理

### A. 大圓距離：Haversine 公式
由於地球是球體，地表兩點間的最短路徑並非直線，而是「大圓距離」。
使用 **[[半正矢公式|Haversine 公式]]** 來計算：

$$d = 2R \cdot \arcsin\left(\sqrt{\sin^2\left(\frac{\Delta\phi}{2}\right) + \cos\phi_1\cos\phi_2\sin^2\left(\frac{\Delta\lambda}{2}\right)}\right)$$

其中：
- $\phi_1, \phi_2$：兩點的緯度（弧度）。
- $\Delta\phi, \Delta\lambda$：緯度差與經度差（弧度）。
- $R$：地球平均半徑（約 $6371$ km）。

### B. 考慮自轉的有效速度 (Effective Speed)
程式模擬了地球自轉（噴流）對飛行速度的影響，設定了「向東快、向西慢」的模型：
- **向東飛行 (Eastbound)**：有效速度 $V_{east} = V_{air} \times 1.1$
- **向西飛行 (Westbound)**：有效速度 $V_{west} = V_{air} \times (1 / 1.1)$
- **飛行時間計算**：$T_{i \to j} = \text{Distance}(i, j) / V_{effective}$

> [!NOTE] 
> 由於 $T_{i \to j} \neq T_{j \to i}$，這是一個**不對稱 TSP (Asymmetric TSP)**，路徑的方向性對結果有顯著影響。

## 2. 核心程式碼實現

### 距離計算函數
```python
def haversine(lat1, lon1, lat2, lon2):
    R = 6371  # 地球半徑 (km)
    dlat = radians(lat2 - lat1)
    dlon = radians(lon2 - lon1)
    # Haversine 核心公式
    a = sin(dlat / 2) ** 2 + cos(radians(lat1)) * cos(radians(lat2)) * sin(dlon / 2) ** 2
    c = 2 * atan2(sqrt(a), sqrt(1 - a))
    return R * c
```

### 時間矩陣與方向判斷
建立一個 $n \times n$ 的矩陣，預存所有城市間的飛行時間：
```python
# 判斷方向並計算時間
if lon2 > lon1:
    effective_speed = aircraft_speed * east_multiplier # 向東
else:
    effective_speed = aircraft_speed * west_multiplier # 向西
time_matrix[i][j] = dist / effective_speed
```

### TSP 暴力破解算法 (Brute Force)
使用 `itertools.permutations` 遍歷所有可能的路徑組合。
- **時間複雜度**：$O(n! \cdot n)$
- **適用範圍**：城市數量 $n \le 10$。

```python
for perm in itertools.permutations(others):
    path = [start] + list(perm) + [start]
    # 加總路徑上每一段的時間
    cost = sum(time_matrix[path[k]][path[k + 1]] for k in range(len(path) - 1))
    if cost < min_cost:
        min_cost = cost
        best_path = path
```



## 3. 使用與輸出範例

### 執行方式
支援檔案輸入或手動輸入（以 `Ctrl+Z` 結束）：
`type input.txt | python 飛行路徑計算.py`

### 範例輸出
```text
程式假設數據:
飛機速度: 800 km/hr
向東飛行速度倍數: 1.1 (有效速度: 880.0 km/hr)
向西飛行速度倍數: 0.909 (有效速度: 727.3 km/hr)
地球半徑: 6371 km

最短路徑為(Taipei -> Tokyo -> Canberra -> Santiago -> NewYork -> London -> NewDelhi -> HongKong -> Taipei)
總飛行時間: 57.48 小時
```



## 4. 未來改進方向
1. **處理 180 度經線問題**：目前 `lon2 > lon1` 的判斷在跨越國際日期變更線時會失效。
2. **算法優化**：引入 **動態規劃 (Held-Karp)** 算法將複雜度降至 $O(2^n \cdot n^2)$，以處理更多城市。
3. **動態風速**：結合 API 獲取真實的高空噴流數據，提升預測準確度。
