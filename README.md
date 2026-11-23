# 413631382_StudentHub

1. [GitHub 倉庫：413631382_StudentHub](https://github.com/leo20060526/413631382_StudentHub)
2. Postman 測試截圖
   - [findAll（200 OK）](screenshots/findAll/413631382.jpg)
   - [insertOne（200 OK）](screenshots/insertOne/413631382.jpg)
3. [Postman Collection](postman/413631382_StudentHub.postman_collection.json)

- 學號：413631382
- 姓名：陳品翰

學生資料管理系統（StudentHub），後端使用 Node.js + TypeScript + Express，資料庫使用 MongoDB（Docker）。

## 專案結構

- `BackEndExample/`：後端 API
- `FrontEndExample/`：前端（React + Vite）
- `studentslist.csv`：學生範例資料，匯入 MongoDB `studenthub.students`

## API

| 方法 | 網址 | 說明 |
|---|---|---|
| GET | `http://localhost:8877/api/v1/user/findAll` | 取得所有學生 |
| POST | `http://localhost:8877/api/v1/user/insertOne` | 新增一位學生（Body 為 JSON） |

## 啟動

```bash
cd BackEndExample
npm install
npm run dev
```

需先在 `BackEndExample` 建立 `.env`（參考 `.env.example`）。

## 修改說明

後端原本固定使用 `authSource=admin` 連線，改為預設使用 `DBNAME` 作為認證資料庫，也可在 `.env` 設定 `DBAUTHSOURCE` 指定。
