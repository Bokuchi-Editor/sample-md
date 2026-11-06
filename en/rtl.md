# Preview Text Direction (RTL) Sample

This file demonstrates the **Text Direction** setting of the Bokuchi preview, which lets Arabic, Hebrew, Persian and other right-to-left (RTL) scripts render correctly.

> Setting location: the **direction icon in the preview header** (left of Export), or **Settings → Editor**

Switch between the three modes while previewing this file:

| Mode | Behavior |
|------|----------|
| Auto | Follows the first strongly-directional character of the document |
| Left to Right | Forces the whole preview to flow left-to-right |
| Right to Left | Forces the whole preview to flow right-to-left |

This file **starts with an English heading**, so **Auto renders it left-to-right** even though RTL text follows below. For a document that Auto renders right-to-left, open `rtl-arabic.md` in the same folder.

The direction applies to the preview and to HTML/PDF export. The editor pane itself always stays left-to-right.

---

## Example 1: Paragraphs in RTL scripts

**Arabic**

مرحبًا بكم في محرر بوكوتشي. هذا محرر ماركداون خفيف وسريع يعمل على ويندوز وماك ولينكس، ويدعم المعاينة الفورية أثناء الكتابة.

**Hebrew**

ברוכים הבאים לעורך בוקוצ'י. זהו עורך Markdown קל ומהיר שפועל ב-Windows, ב-macOS וב-Linux, ותומך בתצוגה מקדימה בזמן אמת.

**Persian**

به ویرایشگر بوکوچی خوش آمدید. این یک ویرایشگر سبک و سریع مارک‌داون است که روی ویندوز، مک و لینوکس اجرا می‌شود.

With **Right to Left**, these paragraphs are right-aligned and read naturally from the right edge.

---

## Example 2: Mixed RTL and LTR text in one sentence

تم إصدار النسخة 1.2.0 من Bokuchi Editor في عام 2026، وهي تدعم 14 لغة.

يمكنك زيارة [صفحة المشروع على GitHub](https://github.com/Bokuchi-Editor/bokuchi) لمعرفة المزيد.

Latin words, numbers and the link stay readable left-to-right inside the right-to-left sentence.

---

## Example 3: Inline code inside an RTL sentence

لتشغيل التطبيق استخدم الأمر `npm run tauri:dev`، ثم افتح الملف `README.md`: سيظهر المحتوى في المعاينة.

The inline code is not reordered by the surrounding text, and the punctuation next to it (`،` and `:`) does not flip to the wrong side.

---

## Example 4: Code blocks always stay left-to-right

```javascript
function greet(name) {
  // التعليقات العربية تبقى داخل كتلة الشيفرة
  if (name) {
    return `Hello, ${name}!`;
  }
  return "مرحبا";
}
```

```bash
if [ -d "$HOME/workspace" ]; then
  echo "indentation, brackets and operators keep their order"
fi
```

Even with **Right to Left**, code blocks stay left-aligned and keep their indentation and bracket order.

---

## Example 5: Tables follow the document direction

| الاسم | الدور | المدينة |
|-------|-------|---------|
| أحمد | مطوّر | القاهرة |
| سارة | مصمّمة | دبي |
| يوسف | مدير المشروع | الرياض |

| First | Second | Third |
|-------|--------|-------|
| one | two | three |

With **Right to Left**, both tables flip: the first Markdown column ("الاسم" / "First") appears on the right.

---

## Example 6: Lists

- العنصر الأول
- العنصر الثاني
  - عنصر متداخل
  - عنصر متداخل آخر
- العنصر الثالث

1. الخطوة الأولى: افتح الملف
2. الخطوة الثانية: اختر اتجاه النص
3. الخطوة الثالثة: صدّر المستند

- [x] مهمة مكتملة
- [ ] مهمة لم تكتمل بعد

With **Right to Left**, bullets, numbers and checkboxes sit on the right, and nested items indent from the right.

---

## Example 7: Headings and blockquotes

### عنوان فرعي باللغة العربية

> المعرفة كنز لا يفنى.
>
> هذا اقتباس متعدد الأسطر للتحقق من موضع شريط الاقتباس.

With **Right to Left**, the heading is right-aligned and the quote bar moves to the right side.

---

## Example 8: Export

Set the direction to **Right to Left**, then run **Export → HTML** and **Export → PDF**.
The exported files match the preview: text flows right-to-left, tables flip, and code blocks stay left-to-right.
