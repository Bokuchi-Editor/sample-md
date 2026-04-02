# Mermaid 圖表範例

用於驗證 Bokuchi 中 Mermaid 圖表渲染效果的範例集。

## 流程圖

```mermaid
graph TD
    A[開始] --> B{正常運作嗎？}
    B -- 是 --> C[太好了！]
    B -- 否 --> D[除錯]
    D --> B
    C --> E[上線部署]
```

## 時序圖

```mermaid
sequenceDiagram
    participant 使用者
    participant 前端
    participant 後端
    participant 資料庫

    使用者->>前端: 點擊「儲存」
    前端->>後端: POST /api/save
    後端->>資料庫: INSERT INTO documents
    資料庫-->>後端: OK
    後端-->>前端: 200 成功
    前端-->>使用者: 顯示通知
```

## 甘特圖

```mermaid
gantt
    title 專案時程表
    dateFormat  YYYY-MM-DD
    section 規劃
    需求分析        :done,    req, 2025-01-01, 14d
    設計            :done,    des, after req, 10d
    section 開發
    前端開發        :active,  fe,  after des, 30d
    後端開發        :         be,  after des, 25d
    section 測試
    整合測試        :         test, after fe, 14d
    上線            :milestone, rel, after test, 0d
```

## 類別圖

```mermaid
classDiagram
    class Editor {
        -content: string
        -theme: string
        +onChange(content)
        +setTheme(theme)
    }
    class Preview {
        -markdown: string
        +render()
    }
    class Tab {
        -id: string
        -title: string
        -isModified: boolean
        +save()
        +close()
    }
    Editor --> Preview : 渲染
    Tab --> Editor : 包含
```

## 狀態圖

```mermaid
stateDiagram-v2
    [*] --> 空白
    空白 --> 編輯中 : 新增檔案 / 開啟檔案
    編輯中 --> 已修改 : 內容變更
    已修改 --> 已儲存 : 儲存 (Ctrl+S)
    已儲存 --> 已修改 : 內容變更
    已修改 --> 已關閉 : 未儲存即關閉
    已儲存 --> 已關閉 : 關閉
    已關閉 --> 空白 : 最後一個分頁已關閉
    空白 --> [*]
```

## 圓餅圖

```mermaid
pie title 支援的語言
    "英文" : 1
    "日文" : 1
    "簡體中文" : 1
    "繁體中文" : 1
    "韓文" : 1
    "西班牙文" : 1
    "法文" : 1
    "德文" : 1
    "葡萄牙文（巴西）" : 1
    "俄文" : 1
    "印地文" : 1
    "阿拉伯文" : 1
    "印尼文" : 1
    "越南文" : 1
```

## 錯誤處理測試

以下區塊包含故意的語法錯誤，用於驗證錯誤訊息的顯示：

```mermaid
invalid diagram syntax !!!
this should show an error message
```
