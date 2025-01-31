# [Chat Chat](https://chat.okisdev.com)

> Chat Chat，解鎖你的下一級 AI 對話體驗。你可以使用 OpenAI、微軟 Azure、Claude、Cohere、Hugging Face 等多個 API，讓你的 AI 對話體驗更加豐富。

[![LICENSE](https://img.shields.io/github/license/okisdev/ChatChat?style=flat-square)](https://github.com/okisdev/ChatChat/blob/master/LICENSE) [![Twitter](https://img.shields.io/twitter/follow/okisdev)](https://twitter.com/okisdev) [![Telegram](https://img.shields.io/badge/Telegram-Chat%20Chat-blue?style=flat-square&logo=telegram)](https://t.me/+uWx9qtafv-BiNGVk)

<p align='center'>
    <a href='README.md'>English</a> | <a>繁體中文</a> | <a href='README.zh_CN.md'>簡體中文</a> | <a href='README.JA.md'>日本語</a>
</p>

<p align='center'>
    <a href='https://docs.okis.dev/chat' target='_blank'>
        文檔
    </a>
    | <a href='https://github.com/okisdev/ChatChat/issues/3'>常見問題</a>
</p>

## 重要提示

-   部分 API 為付費 API，使用前請確保你已經閱讀並同意了相關服務條款。
-   本項目會在一定範圍內獲取到用戶部分數據，請確保你已經閱讀並同意了隱私政策。
-   部分功能還在開發中，歡迎提交 PR 或者 Issue。
-   AI 可能會生成令人反感的內容，請謹慎使用。

## 預覽

### 界面

![UI](https://cdn.harrly.com/project/GitHub/Chat-Chat/img/UI-1.png)

![Dashboard](https://cdn.harrly.com/project/GitHub/Chat-Chat/img/Dashboard-1.png)

### 功能演示

https://user-images.githubusercontent.com/66008528/235539101-562afbc8-cb62-41cc-84d9-1ea8ed83d435.mp4

https://user-images.githubusercontent.com/66008528/235539163-35f7ee91-e357-453a-ae8b-998018e003a7.mp4

## 功能

-   [x] TTS
-   [x] 暗色模式
-   [x] 與文件聊天
-   [x] 多語言支持
-   [x] 支持分享對話
-   [x] 支持流信息（SSE）
-   [x] Markdown 格式化
-   [x] 支持消息代碼語法高亮
-   [x] 支持 System Prompt
-   [x] 快捷菜單（command + k）
-   [x] 聊天記錄（本地和雲端同步）
-   [x] 封裝的 API（不再需要代理）
-   [x] 支持插件功能（`/search`, `/fetch`）
-   [x] 支持 OpenAI, Microsoft Azure, Claude, Cohere, Hugging Face

## Roadmap

請查看 https://github.com/users/okisdev/projects/7

## 使用

### 前提條件

-   來自 OpenAI、Microsoft Azure、Claude、Cohere、Hugging Face 的任何 API 密鑰

### 環境變量

| 變量名稱          | 描述                  | 默認 | 是否強制需要 | 提示                                                                                                |
| ----------------- | --------------------- | ---- | ------------ | --------------------------------------------------------------------------------------------------- |
| `DATABASE_URL`    | Postgresql 數據庫地址 |      | **Yes**      | 以 `postgresql://` 開頭 （如果不需要，請填寫 `postgresql://user:password@example.com:port/dbname`） |
| `NEXTAUTH_URL`    | 您的網站 URL          |      | **Yes**      | （帶前綴）                                                                                          |
| `NEXTAUTH_SECRET` | NextAuth Secret       |      | **Yes**      | 隨機哈希數值（16 位最佳）                                                                           |
| `EMAIL_HOST`      | SMTP Host             |      | No           |                                                                                                     |
| `EMAIL_PORT`      | SMTP Port             | 587  | No           |                                                                                                     |
| `EMAIL_USERNAME`  | SMTP username         |      | No           |                                                                                                     |
| `EMAIL_PASSWORD`  | SMTP password         |      | No           |                                                                                                     |
| `EMAIL_FROM`      | SMTP 發送地址         |      | No           |                                                                                                     |

### 部署

> 請在部署前更改環境變量，如需更詳細的部署流程請看 https://docs.okis.dev/chat/deployment/

#### 本地部署

```bash
git clone https://github.com/okisdev/ChatChat.git
cd ChatChat
cp .env.example .env
pnpm i
pnpm dev
```

#### Vercel

[![部署在 Vercel](https://vercel.com/button)](https://vercel.com/import/project?template=https://github.com/okisdev/ChatChat)

#### Zeabur

訪問 [Zeabur](https://zeabur.com) 來部署

#### Railway

[![部署在 Railway](https://railway.app/button.svg)](https://railway.app/template/-WWW5r)

#### Docker

```bash
docker build -t chatchat .
docker run -p 3000:3000 chatchat -e DATABASE_URL="" -e NEXTAUTH_URL="" -e NEXTAUTH_SECRET="" -e EMAIL_HOST="" -e EMAIL_PORT="" -e EMAIL_USERNAME="" -e EMAIL_PASSWORD="" -e EMAIL_FROM=""
```

或者

```bash
docker run -p 3000:3000 -e DATABASE_URL="" -e NEXTAUTH_URL="" -e NEXTAUTH_SECRET="" -e EMAIL_HOST="" -e EMAIL_PORT="" -e EMAIL_USERNAME="" -e EMAIL_PASSWORD="" -e EMAIL_FROM="" ghcr.io/okisdev/chatchat:latest
```

## LICENSE

[AGPL-3.0](./LICENSE)

## 支持我

[![Buy Me A Coffee](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://www.buymeacoffee.com/okisdev)

## 技術棧

nextjs / tailwindcss / shadcn UI
