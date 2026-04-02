# Mermaid 图表示例

用于验证 Bokuchi 中 Mermaid 图表渲染效果的示例集合。

## 流程图

```mermaid
graph TD
    A[开始] --> B{是否正常工作？}
    B -- 是 --> C[太好了！]
    B -- 否 --> D[调试]
    D --> B
    C --> E[发布上线]
```

## 时序图

```mermaid
sequenceDiagram
    participant User as 用户
    participant Frontend as 前端
    participant Backend as 后端
    participant DB as 数据库

    User->>Frontend: 点击"保存"
    Frontend->>Backend: POST /api/save
    Backend->>DB: INSERT INTO documents
    DB-->>Backend: OK
    Backend-->>Frontend: 200 成功
    Frontend-->>User: 显示通知
```

## 甘特图

```mermaid
gantt
    title 项目时间线
    dateFormat  YYYY-MM-DD
    section 规划
    需求分析         :done,    req, 2025-01-01, 14d
    设计             :done,    des, after req, 10d
    section 开发
    前端             :active,  fe,  after des, 30d
    后端             :         be,  after des, 25d
    section 测试
    集成测试         :         test, after fe, 14d
    发布             :milestone, rel, after test, 0d
```

## 类图

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

## 状态图

```mermaid
stateDiagram-v2
    [*] --> 空白
    空白 --> 编辑中 : 新建文件 / 打开文件
    编辑中 --> 已修改 : 内容变更
    已修改 --> 已保存 : 保存 (Ctrl+S)
    已保存 --> 已修改 : 内容变更
    已修改 --> 已关闭 : 未保存直接关闭
    已保存 --> 已关闭 : 关闭
    已关闭 --> 空白 : 关闭最后一个标签页
    空白 --> [*]
```

## 饼图

```mermaid
pie title 支持的语言
    "英语" : 1
    "日语" : 1
    "简体中文" : 1
    "繁体中文" : 1
    "韩语" : 1
    "西班牙语" : 1
    "法语" : 1
    "德语" : 1
    "葡萄牙语（巴西）" : 1
    "俄语" : 1
    "印地语" : 1
    "阿拉伯语" : 1
    "印度尼西亚语" : 1
    "越南语" : 1
```

## 错误处理测试

以下代码块包含故意的语法错误，用于验证错误显示效果：

```mermaid
invalid diagram syntax !!!
this should show an error message
```
