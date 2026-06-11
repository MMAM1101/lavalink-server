# Lavalink Server — Railway Deployment

## كيف تنشره على Railway

1. ارفع هذا المجلد على GitHub (مجلد `lavalink-server` فقط)
2. أنشئ **New Service** في Railway واربطه بالـ Repository
3. أضف متغير البيئة:
   - `LAVALINK_PASSWORD` — كلمة سر تختارها (مثلاً: `MySuperSecret123`)
4. Railway سيبني الـ Docker image تلقائياً
5. بعد النشر، احفظ الـ **Private Domain** من Railway لاستخدامه في البوت

## متغيرات البيئة في البوت

بعد نشر Lavalink، أضف في سيرفر البوت:
- `LAVALINK_HOST` — Private Domain من Railway (مثلاً: `lavalink.railway.internal`)
- `LAVALINK_PORT` — `2333`
- `LAVALINK_PASSWORD` — نفس الكلمة السرية اللي اخترتها
- `LAVALINK_SSL` — `false` (للـ Private Domain) أو `true` (للـ Public Domain)
