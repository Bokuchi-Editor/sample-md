# GFM Alerts Checklist

A catalog of GitHub alerts (also called callouts or admonitions) for checking how the Bokuchi preview renders them. Alerts are a GitHub feature built on blockquote syntax; they are not part of the GFM spec.

```markdown
> [!NOTE]
> Alert body goes here.
```

On GitHub, an alert is a blockquote whose **first line is only the marker** `[!TYPE]`. There are five types.

| Type | Marker | Purpose | Color on GitHub |
|------|--------|---------|-----------------|
| Note | `[!NOTE]` | Information users should know, even when skimming | Blue |
| Tip | `[!TIP]` | Advice for doing things better or more easily | Green |
| Important | `[!IMPORTANT]` | Key information needed to achieve a goal | Purple |
| Warning | `[!WARNING]` | Urgent information that needs immediate attention | Yellow |
| Caution | `[!CAUTION]` | Risks or negative outcomes of an action | Red |

---

## 1. The five alert types

> [!NOTE]
> Useful information that users should know, even when skimming content.

> [!TIP]
> Helpful advice for doing things better or more easily.

> [!IMPORTANT]
> Key information users need to know to achieve their goal.

> [!WARNING]
> Urgent info that needs immediate user attention to avoid problems.

> [!CAUTION]
> Advises about risks or negative outcomes of certain actions.

---

## 2. Regular blockquote for comparison

> A plain blockquote without a marker. It must look different from the alerts above.

---

## 3. Body content

### Multiple lines and paragraphs

> [!NOTE]
> First line of the first paragraph,
> continued on a second source line.
>
> A second paragraph in the same alert.
>
> A third paragraph in the same alert.

### Inline formatting

> [!TIP]
> **Bold**, *italic*, ***bold italic***, ~~strikethrough~~, `inline code`, a [link](https://github.com/Bokuchi-Editor/bokuchi), an autolink https://github.com, and <kbd>Ctrl</kbd> + <kbd>S</kbd>.

### Lists

> [!IMPORTANT]
> Before releasing:
>
> - Run the tests
> - Update the changelog
>   - Nested item
>   - Another nested item
>
> 1. First step
> 2. Second step
>
> - [x] Checked task
> - [ ] Unchecked task

### Code block

> [!WARNING]
> This command deletes files without confirmation:
>
> ```bash
> rm -rf ./dist
> ```
>
> Make sure you are in the right directory.

### Table

> [!NOTE]
> | Key | Value |
> |-----|-------|
> | one | 1 |
> | two | 2 |

### Heading

> [!CAUTION]
> ### Heading inside an alert
>
> Text under the heading.

### Image

> [!TIP]
> ![Bokuchi icon](../images/bokuchi-icon.png)

### Hard line breaks

> [!NOTE]
> Line one with two trailing spaces  
> Line two with a backslash\
> Line three

### Long text

> [!WARNING]
> Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

### Non-Latin text

> [!NOTE]
> 日本語の本文です。アラートの中でも正しく折り返されることを確認します。

> [!NOTE]
> مرحبا بالعالم. هذا نص عربي داخل تنبيه.

---

## 4. Placement

### Consecutive alerts

> [!NOTE]
> First alert.

> [!WARNING]
> Second alert, separated by a blank line.

### Alert directly after a paragraph

A paragraph immediately followed by an alert, with no blank line between them.
> [!TIP]
> Alert after a paragraph.

### Alert and plain blockquote back to back

> [!NOTE]
> An alert.

> A plain blockquote right after it.

### Lazy continuation line

> [!NOTE]
> The next source line has no `>` marker
but still belongs to the alert.

---

## 5. Marker variations

GitHub's behavior is noted for each case; other renderers differ, so these show where Bokuchi stands.

### Lowercase marker — GitHub renders an alert

> [!note]
> Lowercase marker.

### Mixed-case marker — GitHub renders an alert

> [!Warning]
> Mixed-case marker.

### Marker only, no body — GitHub renders a plain blockquote

> [!NOTE]

### Text on the marker line — GitHub renders a plain blockquote

> [!NOTE] Text on the same line as the marker.

### Custom title on the marker line — GitHub renders a plain blockquote

> [!TIP] Custom title
> Body under a custom title.

### Unknown type — plain blockquote

> [!INFO]
> `INFO` is not one of the five types.

> [!DANGER]
> `DANGER` is not one of the five types.

### Space inside the marker — plain blockquote

> [! NOTE]
> A space after the exclamation mark.

### Missing exclamation mark — plain blockquote

> [NOTE]
> No exclamation mark.

### Escaped marker — plain blockquote with literal text

> \[!NOTE]
> The bracket is escaped.

### Marker not on the first line — plain blockquote

> Some text first.
> [!NOTE]
> The marker is on the second line.

### Marker in inline code — plain blockquote

> `[!NOTE]`
> The marker is inside a code span.

### Blank quote line between marker and body — GitHub renders an alert

> [!NOTE]
>
> Body after an empty quote line.

### No space after `>` — GitHub renders an alert

>[!NOTE]
>No space after the quote marker.

### Marker outside a blockquote — literal text

[!NOTE]
Not inside a blockquote.

---

## 6. Nesting

GitHub does not render alerts nested inside other elements; they fall back to plain blockquotes.

### Alert inside a list item

- List item

  > [!NOTE]
  > Alert inside a list item.

### Alert inside a blockquote

> Outer blockquote.
>
> > [!WARNING]
> > Alert nested in a blockquote.

### Alert inside an alert

> [!NOTE]
> Outer alert.
>
> > [!TIP]
> > Inner alert.

### Blockquote inside an alert

> [!NOTE]
> Alert body.
>
> > A plain quote nested inside the alert.

### Alert inside a details block

<details>
<summary>Click to expand</summary>

> [!IMPORTANT]
> Alert inside a details block.

</details>

---

## 7. Themes and export

- Switch between light and dark themes: each of the five types stays distinguishable and readable.
- Run **Export → HTML** and **Export → PDF**: alerts look the same as in the preview.
