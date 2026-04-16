---
title: "企業與個人的 AI 智慧夥伴：打造本地化知識管理系統"
source: "https://hsuanwei.notion.site/AI-19fde4d95a6780088945ed0a46252014#19fde4d95a678064832cd51118bf7737"
author:
published:
created: 2026-04-13
description: "A collaborative AI workspace, built on your company context. Build and orchestrate agents right alongside your team's projects, meetings, and connected apps."
tags:
  - "clippings"
---
在 AI 技術蓬勃發展的當下，開源資源與工具已為我們帶來建立本地端 AI 知識庫的嶄新可能。本文將介紹如何透過 [Ollama](https://ollama.com/) 在本地設備建立大型語言模型 (LLMs)，並結合 [Dify](https://dify.ai/zh) 打造企業與個人專屬的智慧知識庫系統。

![](https://hsuanwei.notion.site/image/attachment%3Ae9b1e54a-bb72-48e3-bef8-f4c5d994bec8%3AFireShot_Capture_092_-_%E5%B7%A5%E4%BD%9C%E5%AE%A4_-_Dify_-_192.168.68.117.png?table=block&id=19fde4d9-5a67-80e1-beba-c7f59414f6d9&spaceId=62bf69dc-979d-461b-823d-65a21abb9647&width=1410&userId=&cache=v2)

### 知識庫的進化：從傳統到 AI 時代

知識庫作為企業與個人的重要資產，涵蓋了教育訓練資料、專業知識累積、技術文件等多元內容，與我們的工作和生活密不可分。傳統知識庫通常結合檔案管理、郵件系統及搜尋功能，讓使用者透過關鍵字尋找資訊。

然而，生成式語言模型的出現徹底改變了知識管理方式。透過 AI 代理 (AI Agent)，我們不僅能進行傳統的關鍵字搜尋，更能獲得資訊的綜合整理與輸出。不同於傳統搜尋引擎需要逐一點擊結果查看內容，AI 驅動的知識庫結合了 RAG 技術 (檢索增強生成，Retrieval-Augmented Generation) 與 LLM 的組織能力，讓我們能以自然對話方式直接獲取精煉後的答案。

Dify 搭配 Ollama 正是實現這種本地端進階知識庫與 AI 問答應用的理想組合。這套解決方案不僅可作為知識庫應用，還能擴展為 AI 客服系統及自動化工作流程的基礎架構。

![](https://hsuanwei.notion.site/image/attachment%3A5d16ee0d-0da2-434e-a2c7-b8fd2839a3e6%3AMacmini%E5%9F%B7%E8%A1%8C%E6%88%AA%E5%9C%96_2025-02-14_%E6%99%9A%E4%B8%8A11.04.23.png?table=block&id=19fde4d9-5a67-8084-b420-c65688a0ddbe&spaceId=62bf69dc-979d-461b-823d-65a21abb9647&width=1410&userId=&cache=v2)

### 我的知識庫建構經驗

經過兩週時間，我利用手邊設備成功建立了個人知識庫系統。將常用參考資料依主題分類，建構了一系列專業知識庫：

「相機說明書」知識庫：匯集個人攝影器材的說明文件

「攝影觀念」知識庫：整合攝影理論書籍與自出版的相關著作

「資訊規劃與開發」知識庫：收錄資訊專業工具書

「收益管理」知識庫：彙整旅宿業收益管理的電子書與資料

「AI 專案」知識庫：包含工作專案的歷史紀錄、會議摘要及教育訓練文件

![](https://hsuanwei.notion.site/image/attachment%3A4e5b2c11-a80f-44cb-a3dd-ba7fc896f18b%3A%E7%9F%A5%E8%AD%98%E5%BA%ABFireShot_Capture_094_-_%E7%9B%B8%E6%A9%9F%E8%AA%AA%E6%98%8E%E6%9B%B8_-_Dify_-_192.168.68.117.png?table=block&id=19fde4d9-5a67-8050-9355-f55e3e672974&spaceId=62bf69dc-979d-461b-823d-65a21abb9647&width=1410&userId=&cache=v2) ![](https://hsuanwei.notion.site/image/attachment%3Ad24b8eca-6bf5-42f8-97ac-8877fbd2ef5f%3A%E7%9F%A5%E8%AD%98%E5%BA%AB%E8%A8%AD%E5%AE%9AFireShot_Capture_098_-_Dify_-_192.168.68.117.png?table=block&id=19fde4d9-5a67-80cf-b7b2-ebf187920537&spaceId=62bf69dc-979d-461b-823d-65a21abb9647&width=1410&userId=&cache=v2)

Dify 會對每個上傳文件進行預處理與索引，支援權限設定及多種索引模式，甚至可使用自定義的嵌入模型進行知識處理。這些內容結合 Ollama 的本地 LLM 模型，實現了在特定知識領域內的 AI 智慧對答功能。

### 實際應用場景與優勢

這種知識庫應用帶來了意想不到的效益，同時節省了大量時間與成本。以工作專案為例，傳統方式需要我們搜尋關鍵字、篩選文件、逐一開啟查看、再次搜尋、自行整理後總結。現在，LLM 可協助執行這些繁瑣工作，快速提供結構化輸出。

雖然雲端也有類似服務，如 OpenAI 的 [ChatGPT](https://chatgpt.com/) 文件問答或 Google 的 [NotebookLM](https://notebooklm.google.com/) ，但 Dify 搭配 Ollama 的最大優勢在於：所有資料保留在本地端，無需上傳至外部平台。即使各 AI 服務提供商都宣稱不會利用客戶資料訓練模型，對於商業機密與敏感資訊，本地化解決方案仍能更有效地防止 Know-How 與隱私外洩風險。

![](https://hsuanwei.notion.site/image/attachment%3A161efa53-7570-4bfe-99ba-c881f81519e9%3A%E4%B8%8D%E5%90%8C%E6%A8%A1%E5%9E%8B%E6%B8%AC%E8%A9%A6476883248_17898313356109194_6948120094965975175_n.jpg?table=block&id=19fde4d9-5a67-80bf-bf2c-e2d37519a74e&spaceId=62bf69dc-979d-461b-823d-65a21abb9647&width=1410&userId=&cache=v2)

### 應用效果與實測比較

我以「攝影觀念」知識庫為例進行測試，上傳了自己出版的電子書《 [簡單構圖與基礎攝影](https://app.duncan.tw/book/menu.html) 》與多本原文攝影書籍，串接 [Mistral](https://mistral.ai/en) 7B 模型進行問答評估。

針對「照片的景深跟拍攝時的哪些設定有關係？」等三個問題，我比較了本地端 Mistral 7B、Deepseek 8B 與雲端 ChatGPT 4o 的回答。結果顯示：

Mistral 7B 回答較為精簡

[Deepseek](https://www.deepseek.com/) 8B 表現接近 ChatGPT 4o，且能精確對應知識庫內容

當在「相機說明書」知識庫中提問同樣問題時，回答明顯不同，證明 AI 確實以指定的知識範疇作答

模型確實遵循了設定的 Prompt 指令，以知識庫資料為主要回答依據

![](https://hsuanwei.notion.site/image/attachment%3Aa1a8f220-7b84-42fd-841a-5c0368d47d67%3A%E7%9F%A5%E8%AD%98%E5%BA%AB%E8%A1%A8%E7%8F%BE3%E6%88%AA%E5%9C%96_2025-02-19_%E4%B8%8A%E5%8D%8810.12.57.png?table=block&id=19fde4d9-5a67-809d-a337-fc0280aab91f&spaceId=62bf69dc-979d-461b-823d-65a21abb9647&width=1410&userId=&cache=v2)

透過測試發現，當地端模型表現效能越高時，AI 知識庫的回應質量也相應提升。即使只使用 7B 和 8B 的基本模型，已能獲得相當不錯的效果。對於查詢特定領域知識或企業內部封閉式內容，這種本地化解決方案提供了雲端 LLM 無法企及的優勢。

![](https://hsuanwei.notion.site/image/attachment%3Aba130d51-5c8b-4316-b4f6-d508aaadbd39%3AFireShot_Capture_089_-_%E6%94%9D%E5%BD%B1%E6%A6%82%E5%BF%B5_-_Dify_-_192.168.68.117.png?table=block&id=19fde4d9-5a67-8097-a9e1-e41a913ab2f1&spaceId=62bf69dc-979d-461b-823d-65a21abb9647&width=1410&userId=&cache=v2)

### 導入挑戰與 AI 課程的思考

Dify 功能強大，但設定與使用門檻不低，這也是個人或企業導入 AI 工具時普遍面臨的困境。成功應用需要對 AI、LLM 等領域有充分理解的人才能進行安裝設定、場景應用推廣，與教育訓練。這也解釋了為何現在坊間推出了大量 AI 代理應用課程。

許多人會疑惑：「如果我不知道可以應用在工作跟生活的哪些區塊，那麼我該去上這樣的課嗎？」這個問題非常關鍵，反映了 AI 學習與實際應用之間的鴻溝。

這讓我想起前公司與外部廠商合作的 AI 客服系統開發的經驗。該項目原定目標是緩解線上與電話客服的負載，藉由使用 LLM 解析查詢、將問題解析轉換為 API 呼叫，並提供訂房、改期、取消等服務。一般已熟悉線上訂房系統的旅客，透過人工客服尋求協助通常是因為面臨系統無法執行的複雜問題。

例如，查詢連續假期多種房型的可用性，傳統訂房系統需要逐一輸入確切日期才能獲得結果。而 LLM 能一次提供多種彈性搜尋結果，甚至在熱門日期無房時推薦附近其他同集團的旅店住宿選擇。這類複雜條件篩選，正是 AI 客服的優勢所在，更不用說回答停車位、周邊景點、入住退房時間等常見問題的效率提升。

原本這個應用是我們單位先提出發想，但當時我們部門正在執行另一個更大的 [AI 商業策略平台的開發](https://www.mastrirms.com/) ，為了保持時效性公司最後決定委外來開發。然而這個專案最終陷入停滯，已開發近兩年卻遲遲無法上線，主要原因在於：

負責人員對 AI 技術應用場景缺乏理解

外廠商忽略了資料預處理的重要性，未能將問題適當解析為 API 查詢，並將回覆重新包裝回饋給使用者訂房的建議

![](https://hsuanwei.notion.site/image/attachment%3Ae05f46ef-4db8-41ed-92e8-31210c425372%3AFireShot_Capture_091_-_%E6%94%B6%E7%9B%8A%E7%AE%A1%E7%90%86_-_Dify_-_192.168.68.117.png?table=block&id=19fde4d9-5a67-80e0-8738-e56e19de640f&spaceId=62bf69dc-979d-461b-823d-65a21abb9647&width=1410&userId=&cache=v2)

### 從知識庫開始的 AI 旅程

我認為無論企業或個人，AI 應用最佳切入點應從知識庫管理與應用開始。這是最容易上手也最具延展性的應用模式，畢竟我們一直以來都有使用文件的相關經驗。

對缺乏底層 AI 技術開發能力的組織而言，直接大筆投資 AI 工具風險較高。相較之下，從具備系統安裝設定能力的資訊人員入手，以知識庫作為實驗項目，能更穩健地探索 AI 導入方向，循序漸進地推動技術轉型。

隨著 AI 技術的不斷進步，這類知識庫應用必將更加普及，為企業和個人知識管理帶來革命性變革。

![](https://hsuanwei.notion.site/image/attachment%3A690d4fd8-6c47-4a23-a5bd-25658aeeffa5%3AMBP%E5%9F%B7%E8%A1%8C-477752877_17898384357109194_8434975798012939795_n.jpg?table=block&id=19fde4d9-5a67-80bb-844d-fa17add2a48c&spaceId=62bf69dc-979d-461b-823d-65a21abb9647&width=1410&userId=&cache=v2)

### Dify 與 Ollama 安裝流程指南

#### 1\. 設備環境概述

本次安裝測試分別於以下設備進行：

Synology DiskStation DS918+（Intel Celeron J3455、4GB）

Mac mini M1 2020（16GB）

MacBook Pro M3 2023（18GB）

由於 NAS 記憶體不足，無法有效運行 LLM，因此後續主要使用 Mac 進行安裝測試。結果顯示，MacBook Pro M3 的執行效率最佳，而 Mac mini M1 亦能運作，但 LLM 回應稍慢且偶爾會中斷。

#### 2\. 選擇的開源 LLM 模型

在 16GB 記憶體環境下，可執行以下開源模型，並獲得可接受的運行效能：

Deepseek LLM (deepseek-r1:8b)：80 億參數，適用於程式碼輔助、問答與一般對話，推理效率佳。

[Qwen](https://chat.qwenlm.ai/) (qwen:latest)：阿里巴巴開發，支援多語言，特別適用於中文處理。

Mistral (mistral:latest)：7B 參數，針對開源社群優化，效能接近 LLaMA 13B。

#### 3\. 安裝流程概述

安裝順序：

Ollama（本機安裝）

Dify（透過 Docker 安裝）

[Portainer](https://www.portainer.io/) （Web 管理工具，非必要）

建議在安裝過程中，可搭配免費或付費的線上 LLM，如 ChatGPT，輔助安裝與設定。

#### 4\. 安裝 Ollama

4.1 安裝 Homebrew（若尚未安裝）

/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

4.2 安裝 Ollama

brew install ollama

4.3 安裝 LLM 模型（以 Mistral 為例）

ollama run mistral

4.4 確認已安裝的模型

ollama list

4.5 測試模型

ollama run mistral

可輸入問題，如「你是什麼？」進行測試。

![](https://hsuanwei.notion.site/image/attachment%3A0a94e04c-43ae-4f64-b261-d6e7a8242640%3AMBP%E5%9F%B7%E8%A1%8C-%E6%96%87%E7%AB%A0%E6%94%B9%E5%AF%AB%E6%87%89%E7%94%A8479497902_17898264078109194_568243443601461049_n.jpg?table=block&id=19fde4d9-5a67-804e-8814-dea71099ca63&spaceId=62bf69dc-979d-461b-823d-65a21abb9647&width=1410&userId=&cache=v2)

4.6 測試 REST API

curl http://127.0.0.1:11434/api/tags

若正常，應返回類似：

{"models":\["mistral","deepseek-r1","qwen"\]}

![](https://hsuanwei.notion.site/image/attachment%3A8ba09e20-82cf-4f4e-ad8e-da6da1137468%3AiShot_2025-02-11_23.10.11.png?table=block&id=19fde4d9-5a67-80d2-b9f7-e30c17d95fa0&spaceId=62bf69dc-979d-461b-823d-65a21abb9647&width=1410&userId=&cache=v2)

#### 5\. 安裝 Dify

5.1 安裝 Docker 及相關工具

brew install docker brew install docker-compose brew install git

5.2 下載 Dify

git clone https://github.com/langgenius/dify.git cd dify/docker

5.3 設定環境變數（.env）

cp.env.example.env

開啟

.env

進行編輯，關鍵參數：

CONSOLE\_API\_URL=http://127.0.0.1:5001 SERVICE\_API\_URL=http://127.0.0.1:5001 OLLAMA\_BASE\_URL=http://host.docker.internal:11434

若需區網連線，可將

127.0.0.1

改為設備的內網 IP。 ![](https://hsuanwei.notion.site/image/attachment%3A7d5f10c5-35d4-40da-9efc-585cb3eee14e%3AiShot_2025-02-19_16.05.34.png?table=block&id=19fde4d9-5a67-8049-9b18-ff988179496d&spaceId=62bf69dc-979d-461b-823d-65a21abb9647&width=1410&userId=&cache=v2)

#### 5.4 設定 docker-compose.yaml

5.4.1 使用

docker-compose-template.yaml

生成正式配置檔案

./generate\_docker\_compose

5.4.2 重要設定修改

確保 API 容器正確設定映像檔

image: langgenius/dify-api:latest

開放 API 端口

ports: - "5001:5001"

調整 Nginx 上傳限制（可至 300MB）

NGINX\_CLIENT\_MAX\_BODY\_SIZE: ${NGINX\_CLIENT\_MAX\_BODY\_SIZE:-300M}

![](https://hsuanwei.notion.site/image/attachment%3A09f4891a-9355-4974-b5e5-ba2fa6398bed%3AiShot_2025-02-19_16.07.21.png?table=block&id=19fde4d9-5a67-80ae-8a65-f599ebe3ddc1&spaceId=62bf69dc-979d-461b-823d-65a21abb9647&width=1410&userId=&cache=v2)

#### 5.5 產生 HTTPS 憑證（可選）

5.5.1 安裝

mkcert

brew install mkcert

5.5.2 建立憑證

mkcert -install mkcert -cert-file dify.crt -key-file dify.key localhost 127.0.0.1::1

5.5.3 移動憑證至適當位置

mv dify.crt dify.key /Users/duncan/dify/docker/nginx/ssl/

![](https://hsuanwei.notion.site/image/attachment%3A3da5b80b-af70-44ef-a3de-3a5da855386c%3AHTTPS%E6%86%91%E8%AD%89iShot_2025-02-14_16.34.57.png?table=block&id=19fde4d9-5a67-80e9-91a0-e885cc090667&spaceId=62bf69dc-979d-461b-823d-65a21abb9647&width=1410&userId=&cache=v2)

#### 6\. 啟動 Dify 服務

6.1 啟動 Dify 容器

docker-compose up -d

成功啟動後，透過瀏覽器開啟

https://127.0.0.1

進行首次設定。

6.2 若啟動失敗，執行 Debug

docker-compose down

可檢查

.env

和

docker-compose.yaml

，以及查看 Docker 日誌進行錯誤排除。 ![](https://hsuanwei.notion.site/image/attachment%3A150bac2b-f3ed-4c26-843d-33f8869b7359%3AiShot_2025-02-19_16.08.38.png?table=block&id=19fde4d9-5a67-8098-b0cd-f14ce037412f&spaceId=62bf69dc-979d-461b-823d-65a21abb9647&width=1410&userId=&cache=v2)

#### 7\. Dify 設定與使用

7.1 設定 Ollama 模型

進入 個人帳戶 > 模型供應商設定，填寫：

Model Name：

deepseek-r1:8b

Base URL：

http://192.168.1.100:11434

（或本機 IP）

7.2 建立知識庫

可上傳說明書、電子書、計劃書等文件。 推薦參數：

最大段落長度：4000 tokens

段落重疊長度：200 tokens

Top K：5

7.3 建立 AI 代理工具

可從應用模版中選擇，或自行建立。

![](https://hsuanwei.notion.site/image/attachment%3Aa33034fd-3b69-461c-be9f-3ad5d97f871e%3A%E6%A8%A1%E5%9E%8B%E5%BB%BA%E7%AB%8BFireShot_Capture_096_-_%E7%9B%B8%E6%A9%9F%E8%AA%AA%E6%98%8E%E6%9B%B8_-_Dify_-_192.168.68.117.png?table=block&id=19fde4d9-5a67-8022-9b14-d6913847c14f&spaceId=62bf69dc-979d-461b-823d-65a21abb9647&width=1410&userId=&cache=v2) ![](https://hsuanwei.notion.site/image/attachment%3A793d05a8-862a-4a77-8459-88d02dceecac%3A%E6%A8%A1%E5%9E%8B%E4%BE%9B%E6%87%89%E5%95%86FireShot_Capture_097_-_%E7%9B%B8%E6%A9%9F%E8%AA%AA%E6%98%8E%E6%9B%B8_-_Dify_-_192.168.68.117.png?table=block&id=19fde4d9-5a67-802a-aefb-d139b6ae0fe9&spaceId=62bf69dc-979d-461b-823d-65a21abb9647&width=1410&userId=&cache=v2)

#### 8\. 總結與注意事項

8.1 LLM 輔助安裝建議僅供參考

AI 無法準確掌握每台設備環境，可能提供無法執行的建議。（ [GPT 在 Dify + Ollama 安裝與錯誤排查過程中的局限與挑戰分析](https://hsuanwei.notion.site/197de4d95a6780b58b72d46ba1a9bf5d?pvs=25) ）

排錯時需依據實際狀況進行調整。

8.2 容器配置影響系統穩定性

金鑰變更、固定 IP、端口設定等，都可能導致容器無法啟動。

啟動失敗時，請回頭檢查

.env

及

docker-compose.yaml

。

8.3 測試與調整參數

測試不同 LLM 的回應時間與準確度，根據需求選擇合適的模型。

![](https://hsuanwei.notion.site/image/attachment%3Ad5d03e10-023c-4268-a813-4d5b3bbd903e%3ALLM%E8%BC%94%E5%8A%A9%E5%AE%89%E8%A3%9D%E6%88%AA%E5%9C%962-iShot_2025-02-10_16.52.37.png?table=block&id=19fde4d9-5a67-8005-a4e8-de4429543152&spaceId=62bf69dc-979d-461b-823d-65a21abb9647&width=1410&userId=&cache=v2) ![](https://hsuanwei.notion.site/image/attachment%3A29cc7f41-7214-4f20-a952-e60f543fc9f7%3ALLM%E8%BC%94%E5%8A%A9%E5%AE%89%E8%A3%9D%E6%88%AA%E5%9C%96_1-2025-02-11_%E4%B8%8A%E5%8D%8810.25.15.png?table=block&id=19fde4d9-5a67-803d-88d8-c3eb4b15891d&spaceId=62bf69dc-979d-461b-823d-65a21abb9647&width=1410&userId=&cache=v2)

設定完知識庫，可以建立空白的應用，或是從應用模版裡來建立，這樣就可以有自己的 AI 代理工具與知識庫可以使用了。而建立應用時可以選擇最多四個模型來測試不同 LLM 的輸出結果，這部份可以自行實驗，最終選一個表現較好的模型來提供服務。這裡需注意 DeepSeek 會產生思考用的 Token，因此它的輸出效率會比其他模型要慢一點。

### 延伸閱讀

這邊補充 Dify 除了知識庫之外的延伸應用，例如客服系統，或者是搭配 make 還可以串接到像是 Line 跟 Google 文件，進行便當的訂購。這是一些 No Code 的應用，目前使用上雖然不用寫程式，但還是需要進行許多節點的設置，因此操作上還是需要有基礎的系統概念與流程的判斷邏輯，以下是其他人製作的影片，有更好的補充資訊。

#### Dify 完整安裝教學

![](https://www.youtube.com/watch?v=kTpC6MtYuKc)

#### 學習 Agent 從 dify 開始

![](https://www.youtube.com/watch?v=n6x77rT6MEw)

#### make 自動化串接教學 - LINE 官方帳號串接 Dify 建立 AI Agent

![](https://www.youtube.com/watch?v=CaA8cj1B6FI)

#### 使用 Dify 工作流 | 10 分鐘打造高效 AI 客服系統

![](https://www.youtube.com/watch?v=ZeBMzx4y8l0)

#### 提升 Dify 效率的必學祕技！自定義工具全攻略大揭密｜串接 Fish Audio API 配音教學｜No Code 快速上手

![](https://www.youtube.com/watch?v=az1QtVZblW4)

[回首頁](https://hsuanwei.notion.site/13dde4d95a6780959dfbfa2db0aa2a29?pvs=25)