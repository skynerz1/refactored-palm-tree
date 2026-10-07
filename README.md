# عُقدة سحب — sa1

حزمة **جاهزة ومجهّزة بالكامل** لهذا المزوّد: **cloudflare**.
العُقدة تسرّع السحب التلقائي عبر موازاة العمل مع السيرفر الأصلي
— **بدون** تخزين أي بيانات قاعدة هنا.

- رابط اللوحة: `https://tv-api.verx1.xyz/0000`
- التوكن: `nd_ضع-توكن-العقدة-هنا`
- نطاق العمل: كل المواقع

## النشر على Cloudflare Workers

1. `npm i -g wrangler` ثم `wrangler login`.
2. من داخل المجلد: `wrangler deploy`.
3. رابط العُقدة: `https://<name>.<account>.workers.dev`.
بعد أول `wrangler deploy` اضبط المتغيّرات من لوحة Cloudflare
(Workers ← worker ← Settings ← Variables) أو بالأسطر:

```bash
wrangler secret put NODE_TOKEN
wrangler secret put NODE_PANEL_URL
```

4. الكرون (`* * * * *`) مضبوط في `wrangler.toml` ويعمل تلقائيا.

## التأكد من الاتصال

بعد النشر افتح رابط العُقدة — يجب أن يظهر: `{"ok":true,"node":"sa1"}`

بعدها ارجع للوحة ← «عُقد السحب» واضغط **فحص الاتصال**. لما تصير خضراء يبدأ التوزيع تلقائيا.
