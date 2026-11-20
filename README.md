# 我的電影俱樂部 ♡
紫色簡約風格的電影／影集收藏網站，支援個人片單、共享片單、邀請碼、TMDB 搜尋與觀影紀錄。

## 本機啟動
1. 安裝 Node.js（建議 LTS）。
2. 解壓縮後，在專案資料夾執行 `npm install`。
3. 複製 `.env.example` 並改名為 `.env.local`。
4. 填入 Supabase URL、Supabase anon key、TMDB Read Access Token。
5. 在 Supabase SQL Editor 執行 `supabase/schema.sql`。
6. 執行 `npm run dev`，開啟終端機顯示的網址。

## 服務設定
- Supabase：建立專案後，從 Project Settings > API 取得 Project URL 和 anon/public key。
- TMDB：在 themoviedb.org 建立帳號並申請 API Read Access Token。
- `.env.local` 範例：
  VITE_SUPABASE_URL=https://xxxx.supabase.co
  VITE_SUPABASE_ANON_KEY=你的anon-key
  VITE_TMDB_READ_TOKEN=你的TMDB-read-token

## 目前功能
- 搜尋真實電影與影集，帶入 TMDB 海報、中文簡介及年份。
- 個人清單與好友共享清單。
- 邀請碼加入共享清單（預設 7 天有效）。
- 狀態：想看、觀看中、已看完、已棄劇。
- 影集觀看進度、個人評分、心得、最愛標記。
- 響應式紫色簡約介面。

## 注意
- 未設定雲端服務時，可按「先試用展示模式」體驗介面；展示模式資料只存在目前頁面記憶體，重新整理會重置。
- 目前清單內每筆作品的評分／心得欄位為共用欄位；若要讓每位成員對同一作品各自評分與寫心得，下一版應新增 `item_reviews` 個人紀錄表。
- TMDB 資料使用需遵守 TMDB 的 API 條款及 attribution 規範。此專案非 TMDB 官方產品。
