---
tags:
  - computer-science
up: 
related: 
aliases: 
Chapter:
  - "[[完全圖解人工智慧#第二章 AI的基礎知識]]"
---

# CNN
>圖像辨識經常使用**卷積神經網路(convolutional neural network，CNN)**

- 用(圖像像素)整體的傾向來辨識資料

![[CNN 流程圖.png]]

# RNN
>處理時序資料經常使用**循環神經網路(Recurrent neural network，RNN)**

- 非單向神經網路，具有回饋循環(feedback loop)來考慮資料優先級或前後關係
e.g. 輸入*appl*，令AI思考下一個字母，很大的機率為*e*

![[RNN 架構示意圖.png|800]]

# [[BERT]]
>處理自然語言資料經常使用**基於變換器的雙向編碼器表示技術(Bidirectional Encoder Representations from Transformers，BERT)**，一種普及於實務方面的標準化方法

- 辨識前後關係與文法上的依賴結構
e.g. 輸入*豚骨*、*以外的*、*拉麵*
傳統模型:輸出豚骨拉麵相關內容
具BERT演算法的模型:輸出除了豚骨口味的拉麵以外的相關內容
- 基於轉換器的生成式預訓練模型(generative pre-trained transformers，GPT)為其在自然語言處理方面上的延伸

# 決策樹
>列表資料常用如 *XGBoost、LightGBM* 等運用決策樹的演算法，或著 *TabNet* 等神經網路算法

![[XGBoost & LightGBM 示意圖.png|500]]
- 處裡列表資料的深度學習模型發展較慢(以~2022來說)
