---
tags:
  - computer-science
Chapter:
  - "[[完全圖解人工智慧#第三章 自然語言處理的方法和模型]]"
up: 
related: 
aliases:
---

# GPT-3的三種學習方法
- 易於處理特定任務
- 解決[[BERT]]準備調用的資料集成本過高的問題
- 不須更新參數，只需說明任務和給予舉例

1. zero-shot learning : 只說明任務
2. one-shot learning : 說明任務和一個例題
3. few-shot learning : 說明任務和10~100個例題

# 特徵
- 龐大的參數數量
透過增加[[Transformer]]層數和預訓練
GPT-3的Transformer有96層，導致神經網路中的參數數量急速膨脹
- 生成非常自然的文章
根據某判斷實驗，數百人類辨別一個文章是否為GPT-3生成的準確率為52%，與隨機選擇率50%相差無幾

# 面臨的問題
- 缺乏常識
在物理常識詢答(*Physical Interaction: Question Answering，PIQA*)答對率仍不夠高
人類為94.9%，GPT-3為82.8%
例如:起司放進冰箱會融化嗎?(蛤
- 運算量龐大
保守估計，建立GPT-3所需的計算量為3640 petaflops/s-day
Flops為一秒鐘浮動小數點的運算次數，peta為$10^{15}$，也就是一千兆(矮噁
- 無法辨識到矛盾
*NLI，Natural Language Inference*為判斷兩張文章關係為矛盾、一致或中立，其表現不如其他先進模型
- 訓練資料偏差造成有偏見的答案
深度學習的模型幾乎都因為資料收集自網路而有[[AI系統的開發流#^ffe71b|資料偏差問題]]，包括性別、種族、宗教
e.g. 要求產出跟男/女性相關的職業，則輸出結果男性輸出結果較多且多為教育程度高或重度勞動的職業，不符合性別平等的宗旨
- 模型非開源

# 未來趨勢
- 改進文字
- 圖像輸入

用文章和圖片的配對進行預訓練
zero-shot e.g. 
- CLIP，Contrastive Language Image Pre-training : 輸入圖片後分類
- DALL.E/.E2 : 輸入文章後生成圖片
