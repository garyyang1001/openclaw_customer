# OpenClaw AI 助理 — 使用教學

歡迎使用 OpenClaw AI 助理！

OpenClaw 是你的**個人 AI 助理**，可以透過 Telegram 或網頁與你對話。它不只是聊天機器人——它能幫你搜尋資料、分析圖片、處理長文件、排程提醒，甚至瀏覽網頁。

---

## 開始使用

### 方法一：Telegram 對話（推薦）

1. 點擊我們提供的 **Bot 連結**
2. 按下 **Start** 或傳送任何訊息
3. 直接打字就能跟 AI 對話了！

```
你：今天台北天氣如何？
Bot：[AI 回答]

你：幫我翻譯這段英文：Hello, how are you?
Bot：你好，你好嗎？
```

### 方法二：網頁版對話（WebChat）

1. 打開瀏覽器，前往我們提供的 **WebChat 網址**
2. 直接在網頁上對話，不需要安裝任何東西

### 管理介面（Control UI）

前往我們提供的**管理介面網址**，用 Gateway Token 登入，可以：

- 查看所有對話紀錄
- 管理 AI 設定
- 查看系統狀態與日誌

---

## 常用指令

在 Telegram 對話中輸入以下指令：

| 指令 | 功能 |
|------|------|
| `/status` | 查看 Bot 目前狀態 |
| `/reset` | 清除對話紀錄，重新開始 |
| `/model` | 查看目前使用的 AI 模型 |
| `/model list` | 列出所有可用的 AI 模型 |
| `/model [編號]` | 切換到指定的 AI 模型 |
| `/help` | 顯示幫助資訊 |

### 切換 AI 模型

如果你有多個 AI 模型可用，可以隨時切換：

```
/model list
→ 1. kimi-coding/k2p5 (目前使用)
→ 2. anthropic/claude-sonnet-4-5
→ 3. openai/gpt-4o

/model 2
→ 已切換至 anthropic/claude-sonnet-4-5
```

---

## AI 能幫你做什麼

### 日常對話
回答問題、翻譯、寫作、腦力激盪，直接打字就好。

### 圖片分析
傳送圖片給 Bot，它可以：
- 描述圖片內容
- 分析圖表數據
- 辨識文字（OCR）
- 回答關於圖片的問題

```
[傳送一張菜單照片]
你：這個菜單上最貴的菜是什麼？
Bot：根據菜單，最貴的是...
```

### 長文件處理
AI 支援超長上下文（最高 256K token），你可以：
- 貼上長篇文章請它摘要
- 傳送文件請它分析
- 持續多輪對話，AI 會記住前面的內容

### 排程提醒
請 AI 設定定時提醒或任務：

```
你：每天早上 9 點提醒我喝水
Bot：已設定每日 09:00 提醒
```

### 網路搜尋
AI 可以幫你搜尋最新資訊（需額外設定 Brave Search API）：

```
你：幫我查一下 2026 年台灣的最低工資是多少
Bot：[搜尋結果 + AI 整理的答案]
```

### 網頁瀏覽
AI 可以自動瀏覽網頁、截圖、填寫表單、擷取內容並整理重點。

```
你：幫我打開 apple.com 看看最新的 iPhone 多少錢
Bot：[自動瀏覽網頁後回覆結果]
```

### 程式碼執行
AI 可以在安全的沙箱環境中執行程式碼，幫你：
- 做數學計算
- 處理資料分析
- 產生圖表
- 測試程式片段

```
你：幫我算 1 到 100 的質數有哪些
Bot：[執行程式碼後回覆結果]
```

### 檔案操作
AI 可以在伺服器上讀寫檔案，例如：
- 產生文件並提供下載
- 處理你上傳的檔案
- 整理資料輸出為特定格式

### 媒體處理
除了圖片，Bot 還支援：
- **音訊訊息** — 傳送語音訊息，AI 能理解並回覆
- **影片** — 傳送影片，AI 能分析內容
- **文件檔案** — 傳送 PDF、文字檔等文件

### 語音模式（選配）
如果已設定語音服務（ElevenLabs），AI 可以用語音回覆你的訊息。需額外設定，請聯繫我們。

### Canvas 畫布（進階）
AI 可以產生互動式的視覺內容，例如圖表、流程圖等，透過 WebChat 介面查看。

---

## 群組使用

如果需要在群組中使用 Bot：

1. 將 Bot 加入 Telegram 群組
2. 在群組中使用 **@你的Bot名稱** 提及 Bot 才會回應
3. Bot 不會回應群組中所有訊息，只會回應被 @ 的訊息

```
@BotName 幫我摘要今天的討論重點
@BotName 翻譯上面那段話成英文
```

---

## 支援的 AI 模型

| 模型 | 特色 | 適合場景 |
|------|------|----------|
| **Kimi K2.5**（預設） | 256K 超長上下文、速度快 | 長文件分析、日常對話 |
| Claude Sonnet 4.5 | 速度與品質平衡 | 一般對話、工作協助 |
| Claude Opus 4.6 | 最強綜合能力 | 複雜推理、創意寫作 |
| GPT-4o | 多模態能力強 | 圖片分析、通用對話 |
| Gemini 2.5 Pro | Google 最新模型 | 多模態、長上下文 |

> 可用的模型取決於部署時的設定。用 `/model list` 查看你目前有哪些模型可用。

---

## 使用注意事項與限制

### 回應速度
- AI 回應通常需要 **5-30 秒**，複雜問題可能更久
- 使用思考模式（reasoning）的模型會需要更長時間
- 如果超過 1 分鐘沒回應，請用 `/status` 確認 Bot 是否在線

### 對話上下文
- AI 會記住同一段對話的前後文，但**不會跨對話記憶**
- 用 `/reset` 可以清除上下文，重新開始
- 單次對話的上下文有長度限制，超過會自動截斷較早的內容

### AI 的限制
- AI 的回答**不一定正確**，重要資訊請自行驗證
- AI **無法主動發起對話**（只能回應你的訊息，排程提醒除外）
- AI **無法存取你的本機檔案或系統**（只能處理伺服器上的檔案和你傳送的檔案）
- AI **無法進行語音/視訊通話**（只支援文字和語音訊息）
- 每次對話的回應長度有上限，過長的回答會被自動分段傳送
- AI 的使用受 API 配額限制，大量使用可能產生額外費用
- AI **不會自動備份對話紀錄**，如有需要請自行從管理介面匯出

### 費用說明
- AI 的使用會產生 API 費用，費用由你的 AI API Key 對應的帳號承擔
- **用越多，費用越高** — 長對話、複雜任務、使用更強的模型都會增加費用
- 建議定期在 AI 供應商的後台查看用量和費用
- 如果擔心超支，可以在 AI 供應商後台設定費用上限

---

## 安全架構說明

我們為你設計了 **五層安全防護架構**，以下是每一層的說明：

```
第 1 層：網路安全
  ✅ HTTPS 加密傳輸（Zeabur 自動提供 SSL 憑證）
  ✅ 專用伺服器（獨立 IP，不與其他用戶共享）
  ✅ 伺服器層級防火牆

第 2 層：Gateway 認證
  ✅ Gateway Token 驗證（40 字元隨機密碼）
  ✅ 管理介面需要 Token 才能登入

第 3 層：頻道存取控制
  ✅ Telegram 採用 allowlist 機制 — 只有你的帳號能與 Bot 對話
  ✅ 群組中 Bot 只回應被 @ 提及的訊息

第 4 層：工具權限控制
  ✅ AI 執行的程式碼在沙箱中隔離運行
  ✅ 檔案系統存取受限
  ✅ 可針對不同功能設定允許/拒絕清單

第 5 層：模型安全
  ✅ 提示注入防護
  ✅ AI 推理過程內容隱藏
  ✅ 日誌中的敏感資料（API Key、密碼等）自動遮蔽
```

### 你的資料歸屬與控制權

| 項目 | 說明 |
|------|------|
| **資料存放位置** | 所有資料存在你自己的 Zeabur 帳號、你自己的專用伺服器上 |
| **對話紀錄** | 只有你能透過管理介面查看，每個人的對話完全隔離 |
| **我們能存取嗎？** | **不能。** 部署完成後，除非你再次提供 Zeabur Token，否則我們無法存取你的服務和資料 |
| **你能收回控制權嗎？** | **可以。** 你隨時可以在 Zeabur 後台撤銷 API Token，立即切斷所有外部存取 |
| **獨立隔離** | 每個客戶的 OpenClaw 實例完全獨立，互不影響 |
| **檔案權限** | 伺服器上的設定檔和對話紀錄僅擁有者可讀寫 |

### 已啟用的安全設定

| 設定項目 | 目前狀態 | 說明 |
|----------|----------|------|
| HTTPS 加密 | ✅ 已啟用 | Zeabur 自動提供 SSL |
| Gateway Token | ✅ 已設定（40 字元） | 管理介面登入密碼 |
| Telegram 存取控制 | ✅ allowlist | 只有你的帳號能私訊 Bot |
| 群組存取控制 | ✅ 提及閘門 | 群組中需 @ Bot 才會回應 |
| 沙箱隔離 | ✅ 已啟用 | 程式碼在隔離環境執行 |
| 敏感資料遮蔽 | ✅ 已啟用 | 日誌自動遮蔽 API Key 等資訊 |

### 安全限制（請知悉）

以下是目前系統**不支援**的安全功能，請了解：

| 限制 | 說明 | 影響 |
|------|------|------|
| **沒有端對端加密（E2E）** | 通訊加密依賴 Telegram 和 HTTPS，OpenClaw 本身不提供 E2E 加密 | 不要傳送高度機密的資訊 |
| **管理介面沒有多因素認證（MFA）** | 只有 Gateway Token 一層驗證 | 請務必保管好 Token |
| **沒有 IP 白名單** | 任何知道網址和 Token 的人都能登入管理介面 | 不要洩漏管理介面網址和 Token |
| **沒有自動威脅偵測** | 無入侵偵測系統（IDS/IPS） | 如發現異常請立即聯繫我們 |
| **對話紀錄不會自動刪除** | 對話會持續保存，直到手動清除 | 定期用 `/reset` 清除不需要的對話 |
| **沒有內建合規審計** | 無自動化的合規檢查報告 | 如有合規需求請聯繫我們 |

---

## 安全性提醒

### 請勿做以下事情

- **不要傳送密碼、信用卡號、身分證號等個人敏感資訊**
  AI 對話紀錄會保存在伺服器上，敏感資料可能被記錄

- **不要分享你的 Gateway Token 給他人**
  Gateway Token 是管理介面的登入密碼，洩漏會讓他人存取你的對話紀錄和設定

- **不要公開你的管理介面網址**
  管理介面網址 + Gateway Token = 完整的管理權限，兩者都要保密

- **不要將 Bot 轉發或分享給未經授權的人**
  Bot 已設定為只有你的帳號能使用（allowlist 機制），其他人無法使用

- **不要嘗試讓 AI 繞過安全限制**
  AI 有內建的安全過濾機制，請勿嘗試用提示注入等方式繞過

- **不要用 AI 生成違法、有害或不當的內容**
  請遵守使用規範

### 建議的安全習慣

- **定期檢查管理介面** — 確認對話紀錄中沒有異常活動
- **不要在公共場所登入管理介面** — 避免 Gateway Token 被旁人看到
- **定期清除不需要的對話** — 用 `/reset` 清除對話，或在管理介面中清理
- **如果懷疑 Token 洩漏** — 立即聯繫我們更換 Gateway Token
- **留意 AI 費用** — 定期在 AI 供應商後台查看用量，異常增長可能代表安全問題

### 如果你發現異常

如果發現以下情況，**請立即聯繫我們**：
- Bot 回應了不是你發送的訊息
- 管理介面出現你不認識的對話紀錄
- 收到可疑的系統訊息
- Gateway Token 疑似洩漏
- AI 費用異常增長

---

## 使用建議

### 讓 AI 回答更好的技巧
- **問題越具體，回答越好** — 「幫我寫一封請假信」比「幫我寫信」效果好很多
- **提供背景資訊** — 告訴 AI 你的角色和情境，例如「我是一個行銷人員，幫我...」
- **分步驟提問** — 複雜任務拆成幾個小問題，比一次問完效果更好
- **善用 `/reset`** — 如果 AI 開始答非所問，清除上下文重新開始通常能解決

### 節省費用的建議
- **日常問題用預設模型（Kimi K2.5）** — 速度快、費用低，大部分情境夠用
- **只在需要時切換到更強的模型** — Claude Opus、GPT-5 費用較高，複雜問題才用
- **避免重複提問相同問題** — AI 會記住對話上下文，不需要每次都重新描述
- **長文件先摘要再深入** — 先請 AI 摘要重點，再針對感興趣的部分追問

### 不適合使用 AI 的情境
- **需要 100% 正確的場景** — 法律條文、醫療診斷、財務報表等，AI 可能出錯
- **即時性要求極高的場景** — AI 回應需要數秒到數十秒
- **高度機密的資訊處理** — 對話紀錄會保存在伺服器上，不適合處理最高機密資料

---

## 常見問題

### Bot 沒有回應？
1. 傳送 `/status` 確認 Bot 是否在線
2. 等待 1-2 分鐘後再試
3. 如果在群組中，確認是否有用 `@` 提及 Bot
4. 聯繫我們確認服務是否正常

### 回應速度很慢？
- AI 處理複雜問題通常需要 5-30 秒
- 使用思考模式的模型會更慢
- 可以用 `/model list` 切換到更快的模型

### 回答不準確？
- 用 `/reset` 清除對話，重新開始
- 試著把問題描述得更具體
- 切換到更強的模型（如 Claude Opus）

### 怎麼查看使用量？
- 在管理介面（Control UI）中可以查看使用統計
- AI API 費用請到你的 AI 供應商後台查看（例如 Kimi、OpenAI 的帳單頁面）

### AI 的回答可以信任嗎？
- AI 可能會產生看起來正確但實際上錯誤的資訊（稱為「幻覺」）
- **重要決策、法律、醫療、財務相關問題，請務必自行驗證**
- AI 適合作為輔助工具，不適合作為唯一的資訊來源

### 想要新增功能或其他 AI 模型？
- 聯繫我們，我們可以幫你調整設定
- 可新增的項目包括：更多 AI 模型、網路搜尋、語音模式、更多通訊平台（WhatsApp、Discord、LINE 等）

---

## 客戶部署與除錯 SOP（標準版）

以下是跨客戶都一致的標準設定，請勿任意變更：

| 類別 | 標準設定 |
|------|----------|
| Gateway Port | `OPENCLAW_GATEWAY_PORT=3000` |
| Gateway Bind | 啟動必帶 `--bind lan` |
| Gateway Token | `OPENCLAW_GATEWAY_TOKEN` 至少 32 字元 |
| Telegram DM 策略 | `allowlist`（不使用 `open`） |
| Allowlist ID | `TELEGRAM_USER_ID` 必須是客戶本人數字 ID |
| Telegram 啟動 Token | 優先使用 `${OPENCLAW_TELEGRAM_BOT_TOKEN:-$TELEGRAM_BOT_TOKEN}` |

### 快速健康檢查（客戶反映「Bot 不回應」時）

1. 檢查 Telegram Token 是否有效（`getMe`）。
2. 檢查 webhook 狀態（`getWebhookInfo`，若採 long polling，`url` 應為空）。
3. 檢查 OpenClaw logs 是否出現：
   - `[telegram] [default] starting provider`
   - `[gateway] listening on ws://0.0.0.0:3000`
4. 若 logs 出現 `Telegram configured, not enabled yet` 或 `botToken: No such file or directory`：
   - 重新套用部署（更新 env + 更新 start command + restart）
   - `channels add` 使用 env token，不要依賴 `cat .../botToken`
5. 若 logs 出現 `getUpdates conflict (409)`：
   - 先 `deleteWebhook(drop_pending_updates=true)`，再重啟服務

### Zeabur API 端點規則（重要）

- 優先：`https://api.zeabur.com/graphql`
- 若回 `403` 且含 `error code: 1010`：改用 `https://api.zeabur.cn/graphql`

### Service ID 格式規則（重要）

- Zeabur UI 常見 `service-xxxxxxxx` 格式
- GraphQL `service(_id: "...")` 需要 raw `_id`（去掉 `service-` 前綴）

---

## 進階：透過 CLI 或 AI 工具管理你的服務

如果你有使用 CLI 終端機、或 AI 編程工具（如 Cursor、Windsurf 等），可以直接透過 Zeabur API 管理你的 OpenClaw 服務。

### 前置準備

1. **取得你的 Zeabur API Token**
   - 前往 [zeabur.com](https://zeabur.com) → Settings → API Token
   - 產生一組 Token（格式為 `sk-xxxxx`）
   - 這個 Token 可以讓你透過 API 管理你的所有 Zeabur 服務

2. **安裝 Zeabur CLI**（可選）
   ```bash
   npm install -g zeabur
   ```

### 使用 Zeabur GraphQL API

所有操作都透過 Zeabur 的 GraphQL API 進行：

**API 端點：** `https://api.zeabur.com/graphql`
（若遇到 `403 error code: 1010`，改用 `https://api.zeabur.cn/graphql`）

**認證方式：** 在 HTTP Header 加入 `Authorization: Bearer <你的 Zeabur Token>`

#### 查看服務狀態

```bash
curl -s -X POST https://api.zeabur.com/graphql \
  -H "Authorization: Bearer <你的TOKEN>" \
  -H "Content-Type: application/json" \
  -d '{"query":"query{projects{edges{node{_id name services{_id name status}}}}}"}'
```

#### 查看服務日誌

```bash
curl -s -X POST https://api.zeabur.com/graphql \
  -H "Authorization: Bearer <你的TOKEN>" \
  -H "Content-Type: application/json" \
  -d '{"query":"query{runtimeLogs(projectID:\"<PROJECT_ID>\",serviceID:\"<SERVICE_ID>\",environmentID:\"<ENV_ID>\"){message timestamp}}"}'
```

#### 重啟服務

```bash
curl -s -X POST https://api.zeabur.com/graphql \
  -H "Authorization: Bearer <你的TOKEN>" \
  -H "Content-Type: application/json" \
  -d '{"query":"mutation{restartService(serviceID:\"<SERVICE_ID>\",environmentID:\"<ENV_ID>\")}"}'
```

#### 更新環境變數

```bash
curl -s -X POST https://api.zeabur.com/graphql \
  -H "Authorization: Bearer <你的TOKEN>" \
  -H "Content-Type: application/json" \
  -d '{"query":"mutation($data: Map!){updateEnvironmentVariable(serviceID:\"<SERVICE_ID>\",environmentID:\"<ENV_ID>\",data:$data)}","variables":{"data":{"KEY_NAME":"NEW_VALUE"}}}'
```

### 常用 API 操作速查表

| 操作 | 用途 |
|------|------|
| 列出專案 | 查看你所有的 Zeabur 專案和服務 |
| 查看服務狀態 | 確認 OpenClaw 是否正常運行 |
| 查看日誌 | 排查問題、確認 Bot 是否連線 |
| 重啟服務 | 服務異常時重啟 |
| 更新環境變數 | 更換 AI API Key、更新 Token 等 |

### 在 Cursor / Windsurf 中使用

如果你使用 AI 編程工具，可以把以下資訊提供給你的 AI 助手，讓它幫你操作：

```
Zeabur API 端點：https://api.zeabur.com/graphql
認證方式：Bearer Token
Token：<你的 Zeabur API Token>

常用 GraphQL 操作：
- 列出專案：query{projects{edges{node{_id name services{_id name status}}}}}
- 查看服務狀態：query{service(_id:"<SERVICE_ID>"){name status}}
- 查看日誌：query{runtimeLogs(projectID:"<PID>",serviceID:"<SID>",environmentID:"<EID>"){message timestamp}}
- 重啟服務：mutation{restartService(serviceID:"<SID>",environmentID:"<EID>")}
- 更新環境變數：mutation($data: Map!){updateEnvironmentVariable(serviceID:"<SID>",environmentID:"<EID>",data:$data)}
```

> **安全提醒：** Zeabur API Token 擁有你帳號的完整管理權限。請勿將 Token 分享給不信任的人或工具。如果你懷疑 Token 洩漏，請立即到 Zeabur 後台撤銷並重新產生。
> **ID 提醒：** 若你拿到的是 `service-xxxx`，請先轉為 raw `_id` 再做 `service(_id:...)` 查詢。

### 服務成功運行的判斷標準

查看日誌時，出現以下訊息代表服務正常：
- `[gateway] listening on ws://0.0.0.0:3000` — Gateway 已啟動
- `[gateway] agent model: kimi-coding/k2p5` — AI 模型已載入
- `[telegram] [default] starting provider` — Telegram Bot 已連線

---

## 聯繫支援

如有任何問題，請聯繫：
- Threads：@881freelancer
- 服務網站：ohya.co/easyclaw
