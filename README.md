# Tensor Frontend

## 📌 專案目的
Tensor Frontend 是一個基於 **Next.js、TailwindCSS** 和 **shadcn/ui** 開發的 AI 研究平台前端專案。本專案主要目標是提供 **直觀且高效的使用者介面**，使研究人員能夠輕鬆管理 AI 模型、數據集以及查看儀表板數據。

本專案的核心功能包括：
- 🚀 **Dashboard**：可視化 AI 研究數據
- 🧠 **模型管理**：上傳、更新和管理機器學習模型
- 📊 **數據集管理**：數據上傳與篩選
- 🔗 **API 整合**：與 Firebase Firestore 後端進行數據交互

## 🛠️ 技術棧
本專案使用 **最新技術** 來確保高效能與可維護性：

| 技術 | 版本 | 用途 |
|------|------|------|
| **Next.js** | 14.x | React 應用框架 (App Router) |
| **React** | 18.x | 前端 UI 庫 |
| **TypeScript** | 5.x | 型別安全的 JavaScript |
| **TailwindCSS** | 3.x | CSS 框架，提供高效樣式設計 |
| **shadcn/ui** | 最新版 | UI 元件庫，基於 Radix UI |
| **Zustand** | 最新版 | 前端狀態管理 |
| **Firebase Firestore** | 最新版 | 雲端資料庫，用於儲存數據 |
| **Vercel** | 最新版 | 部署平台 |

## 📂 目錄結構

```
/your-project
├── /app                     # Next.js 應用程式的根目錄
│   ├── /dashboard           # 儀表板
│   ├── /models              # 模型管理
│   ├── /datasets            # 數據集管理
│   ├── /auth                # 身分驗證（登入/註冊）
│   ├── /settings            # 設定頁面
│   ├── /api                 # API 端點（用於與 Firestore 交互）
│   ├── layout.tsx           # 頂級佈局（Header / Sidebar）
│   ├── page.tsx             # 首頁
│   ├── loading.tsx          # 全局 Skeleton UI
│   ├── error.tsx            # 全局錯誤處理頁面
│
├── /components              # 可重用 UI 元件
│   ├── /ui                  # shadcn/ui 封裝
│   │   ├── Button.tsx       # 按鈕組件
│   │   ├── Input.tsx        # 輸入框
│   │   ├── Modal.tsx        # 模態視窗
│   │   ├── Table.tsx        # 表格組件
│   │   ├── Select.tsx       # 下拉選單
│   │   ├── Toast.tsx        # 提示通知
│   ├── /layout              # 佈局相關元件（Header、Sidebar）
│
├── /hooks                   # 自定義 Hook
│   ├── useFetch.ts          # API 資料請求 Hook
│   ├── useAuth.ts           # 身分驗證 Hook
│   ├── useLocalStorage.ts   # 快取 Hook
│
├── /lib                     # 工具函式庫
│   ├── api.ts               # API 請求封裝
│   ├── utils.ts             # 常用函式
│   ├── firebase.ts          # Firestore 設定
│
├── /store                   # Zustand 狀態管理
│   ├── useUserStore.ts      # 用戶狀態
│   ├── useModelStore.ts     # 模型管理狀態
│   ├── useDatasetStore.ts   # 數據管理狀態
│
├── /styles                  # TailwindCSS 設定
│   ├── globals.css          # 全域樣式
│   ├── tailwind.config.ts   # Tailwind 設定
│
├── /public                  # 靜態資源（圖片、icons）
│
├── .env.local                # 環境變數 (請確保未被提交到 Git)
├── .gitignore                # Git 忽略檔案
├── next.config.js            # Next.js 設定
├── package.json              # 套件管理
├── tsconfig.json             # TypeScript 設定
└── README.md                 # 本文件
```

## 🚀 如何開始開發
### 1️⃣ 安裝依賴
```
npm install
```

### 2️⃣ 啟動開發伺服器
```
npm run dev
```
📌 本機預覽：`http://localhost:3000`

## 🧪 如何進行測試
### **運行 Lint 檢查**
```
npm run lint
```

### **執行單元測試（如果有 Jest）**
```
npm run test
```

### **端對端測試（如果有 Playwright / Cypress）**
```
npm run test:e2e
```

## 🌍 如何部署到 Vercel
### 1️⃣ 安裝 Vercel CLI
```
npm i -g vercel
```

### 2️⃣ 登入並部署
```
vercel login
vercel --prod
```
📌 部署成功後，你將獲得一個 `https://your-project.vercel.app` 網址。

## 📝 開發者須知
- **請勿將 `.env.local` 上傳至 GitHub**，以保護 API 金鑰等敏感資訊。
- **請確保分支管理規範**，所有新功能請從 `feature/your-feature-name` 分支開發。
- **請在提交 PR 前執行 `npm run lint`**，確保代碼符合格式規範。

---
✍ **作者**: Tensor Frontend 開發團隊 🚀