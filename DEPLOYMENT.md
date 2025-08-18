# 🚀 部署說明 - GitHub Pages

## 📋 部署方式

本項目使用 **GitHub Pages** 進行自動部署，無需 Netlify 或其他第三方服務。

## 🔧 自動部署設置

### 1. GitHub Pages 啟用
1. 前往您的 GitHub 倉庫設置
2. 點擊 "Pages" 選項
3. 在 "Source" 部分選擇 "GitHub Actions"
4. 保存設置

### 2. 自動部署工作流程
項目已配置 GitHub Actions 工作流程 (`.github/workflows/static.yml`)：
- 當您推送代碼到 `main` 分支時自動觸發
- 自動構建和部署到 GitHub Pages
- 無需手動操作

## 🌐 訪問您的網站

部署完成後，您的網站將可以通過以下 URL 訪問：
```
https://[您的GitHub用戶名].github.io/[倉庫名稱]
```

例如：`https://amandac617.github.io/istaging`

## 📁 部署的文件

GitHub Pages 將部署以下文件：
- `index.html` - 主頁
- `mediaplan.html` - 媒體計劃工具（包含德國市場分析）
- `workflow.html` - 工作流程管理
- `ads-copy-generator.html` - 廣告文案生成器
- `intelligence.html` - 智能分析工具
- `kw.html` - 關鍵字建議工具
- 其他 HTML 和資源文件

## 🔄 更新部署

### 自動更新
1. 修改代碼後提交到 GitHub
2. 推送到 `main` 分支
3. GitHub Actions 自動觸發部署
4. 幾分鐘後網站自動更新

### 手動觸發部署
如果需要手動觸發部署：
1. 前往 GitHub 倉庫的 "Actions" 標籤
2. 選擇 "Deploy Static Site to Pages" 工作流程
3. 點擊 "Run workflow" 按鈕

## 🛠️ 故障排除

### 部署失敗
1. 檢查 GitHub Actions 日誌
2. 確認代碼沒有語法錯誤
3. 檢查文件權限設置

### 網站無法訪問
1. 確認 GitHub Pages 已啟用
2. 檢查部署狀態
3. 等待幾分鐘讓 DNS 傳播

## 📊 部署狀態檢查

您可以在以下位置檢查部署狀態：
- **GitHub 倉庫**: Actions 標籤
- **GitHub Pages 設置**: Settings > Pages
- **網站狀態**: 直接訪問網站 URL

## 🎯 優勢

使用 GitHub Pages 的優勢：
- ✅ 完全免費
- ✅ 自動部署
- ✅ 無需配置
- ✅ 與 GitHub 完美整合
- ✅ 無 API 限制
- ✅ 可靠的 CDN 服務

## 📞 需要幫助？

如果遇到部署問題：
1. 檢查 GitHub Actions 日誌
2. 查看 GitHub Pages 設置
3. 確認代碼提交成功
4. 等待自動部署完成

---

**注意**: 首次部署可能需要 5-10 分鐘完成。後續更新通常只需要 2-3 分鐘。
