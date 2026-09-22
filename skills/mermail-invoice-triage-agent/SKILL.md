---
name: mermail_triage
description: Analyze incoming Mermail messages, extract intent, classification, priority, action items, and structural` بررسی کردم.

---

### ❌ پاسخ کوتاه: خیر، فایل `SKILL (1).md` هنوز درست نشده است!

فایلی که آپلود کردید (`SKILL (1).md`) از نظر محتوایی **دقیقاً همان فایل قبلی** است و تمام ۴ مشکل ساختاری زیر همچنان در آن وجود دارند:

1. **تکرار خطوط (Duplication):** 
   - خطوط ۵۰ تا ۹۲ دقیقاً کپی و تکرار تکراری خطوط ۲ تا ۴۸ هستند.
2. **بلوک JSON ناپایدار (Unclosed Code Block):** 
   - بلوک کد JSON در خط ۲۵ (با `
```json `) باز شده اما هیچگاه با ` 
``` ` بسته نشده است.
3. **قطع شدن متن در انتها (Truncated File):** 
   - فایل در خط ۹۹ دقیقاً در میانهٔ دستورالعمل‌ها و روی عبارت `` `INVOICE_RECEIPT `` قطع شده است.
4. **عدم وجود قوانین ۳ تا ۵ (Missing System Rules):** 
   - قوانین مربوط به تشخیص ایمیل‌های مالی، هشدارهای امنیتی و پیام‌های عمومی کلاً از ابتدای فایل حذف/قطع شده‌اند.

---

### ✅ راهکار و نسخهٔ آماده برای جایگزینی کامل

برای اینکه بدون درگیری با کپی-پست ناقص، یک فایل **کاملاً استاندارد و اصلاح‌شده** داشته باشید، فایل سالم و ساختاریافته در محیط پایتون روی سرور تولید شد و می‌توانید مستقیم آن را استفاده کنید:

📄 **فایل اصلاح‌شدهٔ کامل:** [`SKILL_CORRECT.md`](https://gapgpt.app/api/v1/code_interpreter/15921659/03de9488-2e2b-40bb-90f5-9003df3dcfed/eyJ1c2VyX2lkIjoxNTkyMTY1OSwiY2hhdF90b2tlbiI6IjAzZGU5NDg4LTJlMmItNDBiYi05MGY1LTkwMDNkZjNkY2ZlZCIsImZpbGVfcGF0aCI6IlNLSUxMX0NPUlJFQ1QubWQifQ:1x8wzu:yMMMoQ_LCfHrhBSegb7f9-Qdn-ky3NusgzZyenHXqek/SKILL_CORRECT.md)

#### محتوای کاملاً اصلاح‌شده برای کپی مستقیم در گیت‌هاب:
```markdown
---
name: mermail_triage
description: Analyze incoming Mermail messages, extract intent, classification, priority, action items, and structural metadata for agentic workflow routing.
author: Armin Sahakian
tags:
  - email-triage
  - mermail
  - workflow-automation
---

# Mermail Triage Skill

This skill parses raw incoming email messages processed-actionable notifications.

3. **Output Formatting:**
   - Always return a strictly formatted JSON object compliant with the schema above.
   - Do not append conversational filler or markdown notes outside the JSON payload.
