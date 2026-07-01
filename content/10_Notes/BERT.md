---
tags:
  - computer-science
Chapter:
  - "[[完全圖解人工智慧#第三章 自然語言處理的方法和模型]]"
up: 
related: []
aliases:
---
>基於變換器的雙向編碼器表示技術
>*Bidirectional Encoder Representations from Transformers，BERT*
>由Google發明，運用預訓練以及微調來提升模型精度的技術

減少需準備的標註語料庫數量並縮短特定任務的學習時間
- 預訓練 *pre-training* : 先用大型的(通用)語料庫進行[[#雙向性|雙向預測訓練]]
- 微調 *fine-tuning* : 在預訓練後，使用特定任務的標記語料庫調整模型參數

# 高精度性
- 應用案例
	- 科學、法律、生物醫學、醫療
	- Google 搜尋引擎 : 提高介系詞的分辨精度，更加準確的理解文句脈絡
	- Hugging Face 之 Transformer
	- Facebook Meta AI 之 RoBERTa
- BERT最高精度任務例
	- GLUE: *General Language Understanding Evaluation*，自然語言模型的綜合評價標準
	- 在[[標註語料庫與雙語語料庫#^b57d5b|NER]]展現高精度
	- 在SQuAD(*Stanford Question Answering Dataset*)v1.1超越人類平均正確率

| 基準         | 語料庫   | 概要                |
| ---------- | ----- | ----------------- |
| GLUE       | MNLI  | 判斷兩篇文章的涵義、中立性、矛盾性 |
| $\uparrow$ | QQP   | 判斷兩個問句的意義是否等價     |
| $\uparrow$ | QNLI  | 判斷敘述是否回答到問句       |
| $\uparrow$ | SST-2 | 情緒分析              |
| $\uparrow$ | CoLA  | 文法查錯              |
| $\uparrow$ | STS-B | 判斷兩則新聞標題的涵義是否等價   |
| $\uparrow$ | MRPC  | 判斷兩篇新聞文章的涵義是否等價   |
| $\uparrow$ | RTE   | 判斷兩篇文章的涵義         |

| 語料庫        | 概要            |
| ---------- | ------------- |
| SQuAD v1.1 | 詢答            |
| SQuAD v2.0 | v1.1 的擴充版本    |
| SWAG       | 從四個候選中選出文章的後續 |

# 雙向性
- BERT 結構
	- 在神經網路的內部(Trm)堆疊多層的[[Transformer]]，以[[Transformer#自注意力機制|自注意力機制]]的多層堆疊掌握相距遙遠的單詞關係並強化表達能力
- 雙向 *bidirectional* : 根據 前/後 單詞預測 後/前 單詞
- 雙向的預測訓練
	- 單詞填空(遮罩)問題 *Masked Language Model*
	- 下一句預測問題 *Next Sentence Prediction, NSP*

![[BERT 結構圖.png|600]]

