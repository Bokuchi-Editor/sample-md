# Mermaid ダイアグラムサンプル

Bokuchi でのレンダリングを確認するための Mermaid ダイアグラム集です。

## フローチャート

```mermaid
graph TD
    A[開始] --> B{動いてる？}
    B -- はい --> C[すばらしい！]
    B -- いいえ --> D[デバッグ]
    D --> B
    C --> E[リリース]
```

## シーケンス図

```mermaid
sequenceDiagram
    participant ユーザー
    participant フロントエンド
    participant バックエンド
    participant DB

    ユーザー->>フロントエンド: 「保存」をクリック
    フロントエンド->>バックエンド: POST /api/save
    バックエンド->>DB: INSERT INTO documents
    DB-->>バックエンド: OK
    バックエンド-->>フロントエンド: 200 成功
    フロントエンド-->>ユーザー: 通知を表示
```

## ガントチャート

```mermaid
gantt
    title プロジェクトスケジュール
    dateFormat  YYYY-MM-DD
    section 企画
    要件定義         :done,    req, 2025-01-01, 14d
    設計             :done,    des, after req, 10d
    section 開発
    フロントエンド    :active,  fe,  after des, 30d
    バックエンド      :         be,  after des, 25d
    section テスト
    結合テスト        :         test, after fe, 14d
    リリース          :milestone, rel, after test, 0d
```

## クラス図

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
    Editor --> Preview : レンダリング
    Tab --> Editor : 含む
```

## 状態遷移図

```mermaid
stateDiagram-v2
    [*] --> 空
    空 --> 編集中 : 新規作成 / ファイルを開く
    編集中 --> 変更あり : 内容を変更
    変更あり --> 保存済み : 保存 (Ctrl+S)
    保存済み --> 変更あり : 内容を変更
    変更あり --> 閉じた : 保存せずに閉じる
    保存済み --> 閉じた : 閉じる
    閉じた --> 空 : 最後のタブを閉じた
    空 --> [*]
```

## 円グラフ

```mermaid
pie title 対応言語
    "英語" : 1
    "日本語" : 1
    "中国語（簡体字）" : 1
    "中国語（繁体字）" : 1
    "韓国語" : 1
    "スペイン語" : 1
    "フランス語" : 1
    "ドイツ語" : 1
    "ポルトガル語（BR）" : 1
    "ロシア語" : 1
    "ヒンディー語" : 1
    "アラビア語" : 1
    "インドネシア語" : 1
    "ベトナム語" : 1
```

## エラーハンドリングテスト

以下のブロックにはエラー表示を確認するための不正な構文が含まれています:

```mermaid
invalid diagram syntax !!!
this should show an error message
```
