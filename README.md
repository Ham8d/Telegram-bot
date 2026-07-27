# 🤖 بوت تليغرام — النسخة المعدّلة v2.1

## ✅ الجديد في هذه النسخة
- **زر الرابط 🔗**: عند إضافة زر اختر نوع "رابط" وأدخل الرابط مباشرةً
- **تعديل الرابط**: من لوحة الأدمن → الأزرار → ✏️ تعديل الرابط
- **لوحة الويب** `/admin`: تعديل روابط الأزرار مباشرةً من الجدول

## 🚀 الرفع على Vercel

### الخطوة 1 — رفع على GitHub
1. اذهب إلى github.com وسجّل دخول
2. اضغط **New repository**
3. اسمه مثلاً: `telegram-bot`
4. اضغط **Create repository**
5. ارفع الملفات الثلاثة: `api/bot.js` و `package.json` و `vercel.json`
   - اضغط **uploading an existing file**
   - اسحب الملفات أو اختارها
   - اضغط **Commit changes**

### الخطوة 2 — ربط Vercel
1. اذهب إلى vercel.com وسجّل دخول بحساب GitHub
2. اضغط **Add New → Project**
3. اختر الـ repository اللي أنشأته
4. اضغط **Deploy** (بدون تغيير أي إعداد)

### الخطوة 3 — إعداد المتغيرات
بعد ما يكمل الـ Deploy:
1. اذهب إلى **Settings → Environment Variables**
2. أضف هذه المتغيرات:

| الاسم | القيمة |
|-------|--------|
| `BOT_TOKEN` | توكن البوت من @BotFather |
| `ADMIN_ID` | رقم ID الخاص بك (من @userinfobot) |
| `ADMIN_PASS` | كلمة مرور قوية لـ /admin |
| `JSONBIN_KEY` | مفتاح API من jsonbin.io |

3. اضغط **Redeploy** بعد إضافة المتغيرات

### الخطوة 4 — إعداد JSONBin
1. اذهب إلى jsonbin.io وسجّل حساب مجاني
2. اذهب إلى **API Keys** وأنشئ مفتاح جديد
3. انسخ المفتاح وضعه في `JSONBIN_KEY` في Vercel
4. بعد Redeploy، افتح: `https://your-domain.vercel.app/api/bot?setup=1`
5. انسخ الـ `JSONBIN_ID` من الرد وأضفه في Vercel
6. **Redeploy** مرة أخيرة

### الخطوة 5 — تفعيل البوت
افتح البوت في تيلغرام واكتب `/start`

## 📋 ملاحظات مهمة
- **BOT_TOKEN**: احصل عليه من @BotFather في تيلغرام
- **ADMIN_ID**: احصل عليه من @userinfobot في تيلغرام  
- البوت يجب أن يكون مشرفاً في القنوات لفحص الاشتراك
