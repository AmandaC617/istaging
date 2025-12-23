# iStaging 專案管理系統

一個整合式的專案管理平台，包含工作流程管理、市場情資分析、Google Ads 文案生成和媒體提案生成功能。

## 🚀 功能特色

### 📋 工作流程管理 (Workflow)
- 專案建立與管理
- 自動生成專案 ID
- 多步驟工作流程追蹤
- 檔案版本管理
- 團隊協作功能

### 🔍 市場情資分析 (Intelligence)
- AI 驅動的競爭對手分析
- 關鍵字建議與搜尋量分析
- SEO 策略優化建議
- 搜索意圖分析
- 自動化 Google Drive 整合
- 集中化資料夾管理

### 📝 Google Ads 文案生成器 (Ads Copy Generator)
- 智能關鍵字文案生成
- 支援 40字元標題和 90字元描述
- 整合 Intelligence 模組 SEO 分析
- 根據商業模式和搜索意圖優化文案
- 一鍵套用智能建議
- 文案複製、下載、儲存功能

### 📊 媒體提案引擎 (Media Plan) - v2.10.0
- 🤖 **Gemini 2.0 Flash** 最新AI模型驅動
- 🧠 **12個專業分析模組** 深度市場洞察
- 🏢 **30+產業類別** 特別強化B2B支援
- 📋 **37個詳細欄位** 完整客戶資料收集
- 🎯 **複雜B2B產品分析** 支援多競爭對手、產品線、行業認證
- 🌍 **13個國際市場** 跨國策略分析
- 📊 **智能媒體組合** 預算分配與ROI最佳化
- 🎨 **創意策略規劃** 品牌定位與執行方案
- 📈 **10章節專業報告** 結構化策略建議
- 🔍 **關鍵字SEO整合** 中英文關鍵字策略
- SEO 與內容策略分析

### 🔑 關鍵字建議工具 (Keyword Suggestions)
- 智能關鍵字生成
- 搜尋量分析
- 競爭度評估
- 長尾關鍵字建議

## 🏗️ 系統架構

```
iStaging_專案管理/
├── [PROJECT_ID]_專案資料/
│   ├── 01_市場情資分析/
│   ├── 02_媒體提案/
│   ├── 03_Google_Ads_文案/
│   ├── 04_關鍵字建議/
│   └── 05_工作流程文件/
```

## 🛠️ 技術棧

- **前端**: HTML5, CSS3, JavaScript (ES6+)
- **UI 框架**: Tailwind CSS
- **後端**: Firebase (Firestore, Authentication)
- **AI 服務**: Google Gemini API
- **雲端儲存**: Google Drive API
- **搜尋引擎**: Google Custom Search API

## 📦 安裝與部署

### 本地開發
```bash
# 克隆專案
git clone https://github.com/AmandaC617/istaging.git
cd istaging

# 啟動本地伺服器
python3 -m http.server 8000

# 開啟瀏覽器
open http://localhost:8000
```

### 生產環境部署
1. 將檔案上傳到您的 Web 伺服器
2. 確保 HTTPS 支援（Google API 要求）
3. 設定 Firebase 專案
4. 配置 Google API 金鑰

## 🔧 設定說明

### Firebase 設定
1. 建立 Firebase 專案
2. 啟用 Firestore 資料庫
3. 設定 Google 登入認證
4. 更新各模組中的 Firebase 配置

### Google API 設定
1. 建立 Google Cloud 專案
2. 啟用以下 API：
   - Gemini API
   - Google Drive API
   - Custom Search API
3. 建立 API 金鑰
4. 設定 OAuth 2.0 憑證

## 📖 使用指南

### 1. 建立專案
1. 開啟 `workflow.html`
2. 點擊「新增專案」
3. 填寫專案資訊
4. 系統自動生成專案 ID

### 2. 市場情資分析
1. 在專案詳情頁面點擊「市場情資分析」
2. 輸入專案 ID（自動填入）
3. 設定分析參數
4. 執行分析並儲存結果

### 3. Google Ads 文案生成
1. 在專案詳情頁面點擊「Google Ads 文案生成器」
2. 輸入專案 ID（自動填入）
3. 選擇商業模式和字元限制
4. 輸入產品關鍵字和購買關鍵字
5. 系統自動整合 Intelligence 分析結果
6. 生成優化的廣告文案

### 4. 媒體提案生成
1. 在專案詳情頁面點擊「媒體提案引擎」
2. 輸入專案 ID（自動填入）
3. 填寫品牌與競爭對手資訊
4. 生成 AI 分析報告

### 5. 關鍵字建議
1. 開啟 `kw.html`
2. 輸入專案 ID
3. 設定關鍵字參數
4. 生成關鍵字建議

### 6. 檔案管理
- 所有檔案自動儲存到 Google Drive
- 按專案 ID 分類管理
- 支援版本控制
- 團隊協作功能

## 🔐 安全性

- 使用 Firebase Authentication 進行身份驗證
- API 金鑰安全儲存
- HTTPS 加密傳輸
- 資料存取權限控制

## 🐛 故障排除

### 常見問題

1. **JavaScript 錯誤 "Cannot read properties of null"**
   - 已修復：添加了完整的 null 檢查
   - 解決方案：重新整理頁面

2. **API 金鑰錯誤**
   - 檢查 API 金鑰是否正確
   - 確認 API 服務已啟用
   - 檢查配額限制

3. **Firebase 連線問題**
   - 檢查網路連線
   - 確認 Firebase 專案設定
   - 檢查瀏覽器快取

## 🤝 貢獻指南

1. Fork 專案
2. 建立功能分支 (`git checkout -b feature/AmazingFeature`)
3. 提交變更 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 開啟 Pull Request

## 📄 授權

本專案採用 MIT 授權條款 - 詳見 [LICENSE](LICENSE) 檔案

## 📞 聯絡資訊

- 專案維護者: Amanda Chien
- Email: amanda.chien@timelimited.com.tw
- GitHub: [@AmandaC617](https://github.com/AmandaC617)

## 🆕 更新日誌

### v2.10.0 (2024-12-23) - B2B複雜產品分析專業版
- ⚙️ 新增複雜B2B產品專用分析模組 (analyzeComplexB2BProducts)
- 🏭 支援多競爭對手分析 (如: 3M, PIP, Ansell, Drager等)
- 📦 新增產品子分類/產品線管理功能
- 🔍 整合關鍵字與行業認證標準分析 (Z87, EN166等)
- 🌐 強化B2B貿易渠道策略分析
- 🎯 完美支援Kitchen Blockers類型的複雜B2B產品

### v2.9.0 (2024-12-03) - 產業類別與產品描述強化版
- 🏢 B2B產業類別從1個擴展至18個專業類別
- 📋 總產業分類從8個擴展至30+詳細分類
- 📝 新增產品/服務詳細描述大型文本欄位
- 🏷️ 新增產品類型和發展階段分類
- 🔧 AI分析整合產品詳細資訊

### v2.8.0 (2024-12-02) - 完整客戶資料洞察版
- 📊 客戶資料欄位從8個擴展至31個
- 🏢 新增品牌現狀與市場定位分析
- 👥 新增客戶洞察與消費行為分析
- 📈 新增行銷背景與歷史績效分析
- 🎯 新增績效指標與目標設定

### v2.7.0 (2024-12-01) - 深度洞察與創意策略版
- 🧠 新增深度市場洞察分析模組
- 🎯 新增媒體組合策略分析模組
- 🎨 新增創意策略分析模組
- 📊 報告結構升級至10個專業章節

### v2.6.0 (2024-11-30) - Gemini 2.0 Flash版
- 🚀 升級至Gemini 2.0 Flash Experimental最新模型
- ⚡ 2倍更快的回應速度
- 🔧 改善JSON格式輸出準確性
- 🇹🇼 更好的中文語言處理

### v2.1.0 (2024-12-07)
- 🐛 修復 Mediaplan 模組 JavaScript 錯誤
- 🔧 添加完整的 null 檢查和錯誤處理
- 📝 新增 Google Ads 文案生成器
- 🔗 整合 Intelligence 模組 SEO 分析
- 🎯 改善使用者體驗和穩定性
- 📚 更新文件和使用指南

### v2.0.0 (2024-12-01)
- ✨ 新增集中化資料夾管理系統
- 🔗 實作 project ID 統一管理
- 📁 自動化 Google Drive 資料夾結構
- 🔄 系統間無縫整合
- 🎯 改善使用者體驗

### v1.0.0 (2024-11-01)
- 🎉 初始版本發布
- 📋 基本工作流程管理
- 🔍 市場情資分析功能
- 📊 媒體提案生成