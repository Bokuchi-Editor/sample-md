# Mermaid Diagram Samples

A collection of Mermaid diagrams to verify rendering in Bokuchi.

## Flowchart

```mermaid
graph TD
    A[Start] --> B{Is it working?}
    B -- Yes --> C[Great!]
    B -- No --> D[Debug]
    D --> B
    C --> E[Ship it]
```

## Sequence Diagram

```mermaid
sequenceDiagram
    participant User
    participant Frontend
    participant Backend
    participant DB

    User->>Frontend: Click "Save"
    Frontend->>Backend: POST /api/save
    Backend->>DB: INSERT INTO documents
    DB-->>Backend: OK
    Backend-->>Frontend: 200 Success
    Frontend-->>User: Show notification
```

## Gantt Chart

```mermaid
gantt
    title Project Timeline
    dateFormat  YYYY-MM-DD
    section Planning
    Requirements     :done,    req, 2025-01-01, 14d
    Design           :done,    des, after req, 10d
    section Development
    Frontend         :active,  fe,  after des, 30d
    Backend          :         be,  after des, 25d
    section Testing
    Integration Test :         test, after fe, 14d
    Release          :milestone, rel, after test, 0d
```

## Class Diagram

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
    Editor --> Preview : renders
    Tab --> Editor : contains
```

## State Diagram

```mermaid
stateDiagram-v2
    [*] --> Empty
    Empty --> Editing : New File / Open File
    Editing --> Modified : Content Changed
    Modified --> Saved : Save (Ctrl+S)
    Saved --> Modified : Content Changed
    Modified --> Closed : Close without saving
    Saved --> Closed : Close
    Closed --> Empty : Last tab closed
    Empty --> [*]
```

## Pie Chart

```mermaid
pie title Supported Languages
    "English" : 1
    "Japanese" : 1
    "Chinese (Simplified)" : 1
    "Chinese (Traditional)" : 1
    "Korean" : 1
    "Spanish" : 1
    "French" : 1
    "German" : 1
    "Portuguese (BR)" : 1
    "Russian" : 1
    "Hindi" : 1
    "Arabic" : 1
    "Indonesian" : 1
    "Vietnamese" : 1
```

## Error Handling Test

The following block contains intentional syntax errors to verify error display:

```mermaid
invalid diagram syntax !!!
this should show an error message
```
