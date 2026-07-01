---
source: https://hackmd.io/@96PkR44hSsyH3YyL-33BYA/BkYH6NfgY
tags:
  - clippings
---
# 概要
Node Wrangler 是 Blender 內附的一個 Shading （著色）節點加強工具，在 Youtube平台上面很多著色節點材質的教學都會使用到這個 Addon，但可能因為初階教程都會告知要啟用它，以致於後面的教學影片上就沒有提到，所以看材質教學時講師有些熱鍵操作自己跟得做卻沒動靜時，那大概可以推測講師使用了 Node Wrangler 魔法。

Node Wrangler 因為已經附在 Blender 中，因此只要到 Addons 中找到並啟用它即可。

---

# 一. 滑鼠操作簡表

| 操作簡表 | 意義 |
| --- | --- |
| MMB | 滑鼠中鍵 |
| LMB | 滑鼠左鍵 |
| RMB | 滑鼠右鍵 |
| Mouse Wheel | 滑鼠滾輪 |
| Click | 單擊 |
| Drag | 拖拉 |

---

# 二. Node Wrangler 常用的懶人操作

下列操作說明的動畫必要時可使用滑鼠右鍵選「在新分頁開啟影像」，以觀看比較詳細的操作畫面。

## 1. 懶人連接

| 操作方式                  | 操作說明                                                                                                                                                                                                                              |
| --------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| SHIFT+CTRL+LMB\_Click | 懶人連接，Shader （著色器）分類的節點（例如 Principled BSDF、Emission）則會直接連到Material Output（材質輸出）。   Shading（著色）模式 ![](https://i.imgur.com/r9PzlcU.gif) 此快捷鍵在 Compositing（合成）模式下則是將當前滑鼠治標下的節點連到 Viewer （預覽輸出）節點。![](https://i.imgur.com/ZSM4aI8.gif) |

---

## 2. 懶人混合

| 操作方式 | 操作說明 |
| --- | --- |
| SHIFT+CTR+RMB\_Drag | 懶人混合，選其中一個節點按著不放拖到另一節點，用在兩個材質混合，會增加一個 Mix RGB（混合RGB）![](https://i.imgur.com/n4tOKYM.gif) |

---

## 3. 懶人接合

| 操作方式 | 操作說明 |
| --- | --- |
| ALT+RMB\_Drag | 懶人接合，用在兩個節點間可匹配的連接，例如COLOR連到COLOR![](https://i.imgur.com/hcOj5DJ.gif) |

---

## 4. 交換節點類型

| 操作方式 | 操作說明 |
| --- | --- |
| SHIFT+S | 交換節點類型，選一個要交換的節點按組合鍵，會出現節點選單![](https://i.imgur.com/3hkFj2b.gif) |

---

## 5. 添加控制座標

| 操作方式 | 操作說明 |
| --- | --- |
| CTRL+T | 為節點添加控制座標，先選取一個紋理節點然後按組合鍵![](https://i.imgur.com/r3ZhLsS.gif) |

---

## 6. 交換輸出連接

| 操作方式 | 操作說明 |
| --- | --- |
| ALT+S | 選取節點以交換輸出連接![](https://i.imgur.com/4r5iGie.gif) |

---

## 7. 自動連結影像紋理

| 操作方式 | 操作說明 |
| --- | --- |
| SHIFT+CTRL+T | 自動添加具有控制座標節點的PBR影像紋理。   先選取Principled BSDF 後按下SHIFT+CTRL+T組合鍵會出現檔案瀏覽器，瀏覽到材質之後選取需連進來的材質影像，它會自動把該有的節點都連接好。![](https://i.imgur.com/CTqKMEz.gif)自動連接的材質影像，檔按格式則可使用PNG、JPG、TIFF…任何Blender可支援的格式，但檔案名稱必須有以下命名規則所包含的名稱：![](https://i.imgur.com/FiuNCkI.png) |

>Node Wrangler檔案名稱規則所列應該符合大多數PBR材質通用的命名原則。
>但必要時也可點擊上方「Edit tags for auto texture detection in Principled BSDF setup」自己新增，但必須符合用途類型，例如 Normal 用途的類型不應增加至 Base Color 的類型，反之亦然，其他類型也一樣需按用途類型去增加以免因此造成自己困擾。

---

## 8. 將節點包進框架

| 操作方式 | 操作說明 |
| --- | --- |
| SHIFT+P | 將節點包進框架，先選取鎖要包進框架的節點後按組合鍵。![](https://i.imgur.com/7eieqbz.gif) |

---

## 9. 刪除對結果無關的節點

| 操作方式 | 操作說明 |
| --- | --- |
| ALT+X | 刪除所有對材質結果無關的節點，只需在Shading 編輯視窗中按下組合鍵即可。![](https://i.imgur.com/T2RtDcQ.gif) |

---

## 10. 插入 Math（數學）節點

| 操作方式 | 操作說明 |
| --- | --- |
| CTRL ＋、－、＊、/ | 插入ADD（加）、Subtract（減）、Multiply（乘）、Divide （除） 的 Math（數學）節點 ![](https://i.imgur.com/zP6w9pQ.gif) |

---

## 11. 懶人插座選單連結

| 操作方式 | 操作說明 |
| --- | --- |
| ALT+SHIFT+RMB | 懶人插座，連結時會出現選單以選取兩端的插座。在兩個節點距離太遠插座本身變小就很難選的狀況下，這功能會變得很方便。![](https://i.imgur.com/IeetMMK.gif) |

---

## 12. 懶人插座切換開關

| 操作方式 | 操作說明 |
| --- | --- |
| ALT+S | 懶人切換，使用這一組快捷鍵可以快速切換插座，每按一次就會切換到下一個。![](https://i.imgur.com/zRPmI5l.gif) |
|  |  |

# 三. Blender 內建 Shading 著色器的節點操作

---

## 1. 增加路由

| 操作方式 | 操作說明 |
| --- | --- |
| SHIFT+RMB | 增加路由點，在連接線增加路由。   按 SHIFT 後按滑鼠右鍵劃過連接線，在有多個節點需要連接時，可用路由的方式在路由點牽出連接線接到不同節點!![](https://i.imgur.com/YGux6wY.gif) |

## 2. 刪除路由

| 操作方式 | 操作說明 |
| --- | --- |
| CTRL+X | 刪除路由點，要刪除路由點只需要選取路由點後按Ctrl+X組合鍵![](https://i.imgur.com/X6KiBWA.gif) |

## 3. 移動路由

| 操作方式 | 操作說明 |
| --- | --- |
| G | 移動路由點，選取路由點後按G即可移動。![](https://i.imgur.com/DPjPKBa.gif) |

## 4. 中斷連接

| 操作方式 | 操作說明 |
| --- | --- |
| CTRL+RMB | 將連接節點的線切除，   按 CTRL 後按滑鼠右鍵劃過連接線即可移除兩節點間的連接。![](https://i.imgur.com/GnJgxbz.gif) |

## 5. 對齊節點

| 操作方式                          | 操作說明                                                                                                    |
| ----------------------------- | ------------------------------------------------------------------------------------------------------- |
| S+X0水平對齊   S+Y0垂直對齊   S +移動縮放 | 將所選取的多個節點對齊   按 S 後按X0可做水平向左對齊   按 S 後按Y0可做垂直向上對齊   按 S 後移動滑鼠則可縮放距離![](https://i.imgur.com/qtHp8E7.gif) |
|                               |                                                                                                         |
|                               |                                                                                                         |