# GitHub 上傳教學

## 方法一：使用 GitHub 網頁介面（最簡單）

### 步驟 1：創建 GitHub 帳號
1. 前往 https://github.com
2. 點擊右上角「Sign up」註冊
3. 驗證 Email

### 步驟 2：創建新的 Repository（儲存庫）
1. 登入 GitHub
2. 點擊右上角「+」→「New repository」
3. 填寫資訊：
   - **Repository name**: `BRM411-Calculator`（或你想要的名稱）
   - **Description**: `BRM411 臨床試驗訪視計算器`
   - 選擇「Public」（公開）或「Private」（私人）
   - ✅ 勾選「Add a README file」
4. 點擊「Create repository」

### 步驟 3：上傳檔案
1. 在新創建的 Repository 頁面，點擊「Add file」→「Upload files」
2. 將以下檔案拖曳到上傳區：
   - `BRM411_Calculator_Final.html`
   - `README.md`
3. 在下方「Commit changes」填寫：
   - Commit message: `Initial commit - BRM411 Calculator`
4. 點擊「Commit changes」

### 步驟 4：啟用 GitHub Pages（讓網頁可以直接瀏覽）
1. 在 Repository 頁面，點擊「Settings」
2. 左側選單找到「Pages」
3. 在「Branch」下：
   - Source: 選擇「main」
   - Folder: 選擇「/ (root)」
4. 點擊「Save」
5. 等待 1-2 分鐘，頁面會顯示網址：
   ```
   https://[你的用戶名].github.io/BRM411-Calculator/BRM411_Calculator_Final.html
   ```

### 步驟 5：重命名檔案（可選）
如果想要更簡潔的網址，可以：
1. 在 Repository 頁面找到 `BRM411_Calculator_Final.html`
2. 點擊檔案名稱旁的「⋯」→「Rename」
3. 改名為 `index.html`
4. Commit changes
5. 現在網址變成：
   ```
   https://[你的用戶名].github.io/BRM411-Calculator/
   ```

---

## 方法二：使用 Git 命令列（適合開發者）

### 前置要求
- 安裝 Git：https://git-scm.com/downloads
- GitHub 帳號

### 步驟 1：在 GitHub 創建 Repository
（同方法一的步驟 1-2，但不要勾選「Add a README file」）

### 步驟 2：本地初始化和上傳
打開終端機（Terminal），執行以下命令：

```bash
# 進入檔案所在目錄
cd /path/to/your/files

# 初始化 Git
git init

# 添加檔案
git add BRM411_Calculator_Final.html
git add README.md

# 提交變更
git commit -m "Initial commit - BRM411 Calculator"

# 設定遠端儲存庫（替換成你的用戶名和 repo 名稱）
git remote add origin https://github.com/[你的用戶名]/BRM411-Calculator.git

# 推送到 GitHub
git branch -M main
git push -u origin main
```

### 步驟 3：啟用 GitHub Pages
（同方法一的步驟 4）

---

## 方法三：使用 GitHub Desktop（圖形界面）

### 步驟 1：安裝 GitHub Desktop
1. 前往 https://desktop.github.com
2. 下載並安裝
3. 登入 GitHub 帳號

### 步驟 2：創建 Repository
1. 點擊「File」→「New repository」
2. 填寫：
   - Name: `BRM411-Calculator`
   - Local path: 選擇檔案存放位置
3. 點擊「Create repository」

### 步驟 3：添加檔案
1. 將 `BRM411_Calculator_Final.html` 和 `README.md` 複製到 Repository 資料夾
2. GitHub Desktop 會自動偵測到新檔案
3. 在左下角填寫 Commit message: `Initial commit`
4. 點擊「Commit to main」

### 步驟 4：發布到 GitHub
1. 點擊右上角「Publish repository」
2. 選擇「Public」或「Private」
3. 點擊「Publish repository」

### 步驟 5：啟用 GitHub Pages
（同方法一的步驟 4）

---

## 更新檔案的方法

### 網頁介面更新
1. 在 GitHub Repository 頁面找到要更新的檔案
2. 點擊檔案名稱 → 右上角鉛筆圖示「Edit」
3. 修改內容
4. 點擊「Commit changes」

### Git 命令列更新
```bash
# 修改檔案後

# 添加變更
git add .

# 提交變更
git commit -m "Update: 說明更新內容"

# 推送到 GitHub
git push
```

### GitHub Desktop 更新
1. 修改本地檔案
2. GitHub Desktop 會自動顯示變更
3. 填寫 Commit message
4. 點擊「Commit to main」
5. 點擊右上角「Push origin」

---

## 常見問題

### Q1: 我的網頁顯示 404 Not Found
**A**: 等待 2-5 分鐘讓 GitHub Pages 部署完成，或檢查：
- Settings → Pages 是否已啟用
- Branch 是否選擇正確
- 檔案名稱是否正確

### Q2: 更新後網頁沒有變化
**A**: 
- 清除瀏覽器快取（Ctrl+F5 或 Cmd+Shift+R）
- 等待幾分鐘讓 GitHub Pages 更新

### Q3: 如何刪除 Repository
**A**:
1. Repository 頁面 → Settings
2. 滾動到最下方「Danger Zone」
3. 點擊「Delete this repository」
4. 按照指示確認

### Q4: 如何設為私人 Repository
**A**:
1. Repository 頁面 → Settings
2. 滾動到最下方「Danger Zone」
3. 點擊「Change visibility」→「Make private」
4. 注意：私人 Repository 的 GitHub Pages 需要付費方案

---

## 分享網址

完成後，你可以分享以下網址：

**Repository 網址**（查看原始碼）:
```
https://github.com/[你的用戶名]/BRM411-Calculator
```

**GitHub Pages 網址**（直接使用）:
```
https://[你的用戶名].github.io/BRM411-Calculator/BRM411_Calculator_Final.html
```

或者如果改名為 `index.html`:
```
https://[你的用戶名].github.io/BRM411-Calculator/
```

---

## 建議

✅ **檔案命名建議**
- 將 `BRM411_Calculator_Final.html` 重命名為 `index.html`
- 這樣網址更簡潔好記

✅ **版本控制建議**
- 每次更新都寫清楚 commit message
- 例如："Fix: 修正假期資料"、"Add: 新增 2028 年假期"

✅ **備份建議**
- 定期下載本地備份
- 可以用 Git clone 到不同位置

---

需要更多幫助？
- GitHub 官方文件：https://docs.github.com
- GitHub Pages 文件：https://pages.github.com
