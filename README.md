# k4_call


# Virtual Terminal Flask App with Twilio Integration

## المتطلبات

- Python 3.7 أو أحدث
- حساب Twilio
- ملف MP3 على الإنترنت لتشغيله أثناء المكالمة

## تثبيت الحزم

أولاً، قم بتثبيت الحزم المطلوبة باستخدام pip:

```bash
pip install flask twilio
```

## إعداد المتغيرات

يُفضل عدم وضع بيانات الدخول مباشرة داخل الكود. يمكنك استخدام المتغيرات البيئية بدلاً من ذلك. لإنشاءها مؤقتًا في نفس الجلسة:

```bash
export TWILIO_ACCOUNT_SID="معرف الحساب الخاص بك"
export TWILIO_AUTH_TOKEN="رمز الدخول الخاص بك"
export TWILIO_PHONE_NUMBER="+213XXXXXXXXX"
```

## تشغيل التطبيق

شغل التطبيق باستخدام:

```bash
python virtual_terminal_app.py
```

ثم افتح المتصفح وتوجه إلى:

```
http://localhost:5000
```

## إرسال طلب اتصال

يمكنك إرسال طلب POST إلى المسار `/call` باستخدام أداة مثل Postman أو curl:

```bash
curl -X POST http://localhost:5000/call -H "Content-Type: application/json" -d '{"to": "+213XXXXXXXXX"}'
```

تأكد من تعديل رابط الصوت داخل الكود إلى رابط MP3 فعّال.

## ملاحظة أمنية

**لا تنشر بيانات Twilio الحساسة على الإنترنت أو في مستودعات عامة.**
