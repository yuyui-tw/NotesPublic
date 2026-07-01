---
tags:
  - computer-science
up:
  - "[[甚麼是自然語言處理(NLP)]]"
related: 
aliases: 
Chapter:
  - "[[完全圖解人工智慧#第三章 自然語言處理的方法和模型]]"
---

# 執行NLP特有的難題
- 詞彙與句子沒有統一定義，可以有多種詮釋

>e.g. 命令: 請把資料蓋成**更好理解**的形式
畫圖?表格?條列重點?

# NLP的重點與技術
- 多義詞

>e.g. **I bought a picture.**
**picture**: 畫? 照片?

- 語素分析 *morphological analysis*
e.g. 像是中文、日文的詞語之間不會有空格，難以分析哪些文字屬於同一單詞

- 子句的從屬關係
	- 樹狀結構 *tree structure*
	- 語法分析 *parsing, syntactic analysis*

>e.g. **我拍了一張很大的狗和貓的照片**
很大的狗 + 貓 ? 很大的狗 + 很大的貓?

- 代詞解析
	- 指代解消 *anaphora resolution* : 辨識代詞與其先行詞的技術
		- 回指關係 *anaphor relation* ^80d868
		- 先行詞 *antecedent* : 代詞所指之事物
		- 零回指 *zero anaphora* : 主語被省略

>e.g. **它很好用**
**它** 是指誰?

- 情緒分析 *sentiment analysis*

>e.g. **你真的好棒喔~**
>真的在稱讚? 還是在陰陽怪氣?

# NLP的事前準備
- 資料集
	- NLP的資料集為**文本資料**，稱為==語料庫== *corpus*
		- [[甚麼是監督式學習|監督式學習]]帶有標註的語料庫稱為==註解語料庫== *annotated corpus*
		- 只有文本、沒有註解的語料庫為==生語料庫== *raw corpus*
	- e.g. 社群網站、網路評價、契約書、論文、健康紀錄、維基百科...或著青空文庫這類開放公眾使用的語料庫(已過著作權保護期之作品)
