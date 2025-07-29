# Admin Scripts Documentation

## 📋 نظرة عامة

هذا المجلد يحتوي على scripts لإنشاء وإدارة مستخدمي الإدارة في منصة ربح.

## 🚀 Scripts المتاحة

### 1. `simple-admin.js` - إنشاء مدير بسيط
```bash
npm run simple-admin
# أو
node scripts/simple-admin.js
```

**الميزات:**
- إنشاء مدير جديد بسرعة
- حذف المدير السابق (إن وجد)
- إنشاء محفظة تلقائياً
- كلمة مرور: `Admin123!`

### 2. `check-admin.js` - فحص المدير
```bash
npm run check-admin
# أو
node scripts/check-admin.js
```

**الميزات:**
- فحص وجود المدير
- اختبار كلمة المرور
- عرض معلومات المدير
- فحص المحفظة

### 3. `create-admin.js` - إنشاء مدير متقدم
```bash
npm run create-admin
# أو
node scripts/create-admin.js
```

**الميزات:**
- إنشاء مدير مع خيارات متقدمة
- دعم المعاملات
- validation للبيانات
- رسائل تفصيلية

## 🔐 بيانات تسجيل الدخول الافتراضية

```
البريد الإلكتروني: admin@ribh.com
كلمة المرور: Admin123!
```

## 📝 كيفية الاستخدام

### إنشاء مدير جديد:
```bash
# الطريقة السريعة (مُوصى بها)
npm run simple-admin

# الطريقة المتقدمة
npm run create-admin
```

### فحص المدير:
```bash
npm run check-admin
```

### إنشاء مدير مخصص:
```bash
node scripts/create-admin.js "اسم المدير" "admin@example.com" "01234567890" "كلمة_المرور"
```

## ⚠️ ملاحظات مهمة

1. **تأكد من تشغيل التطبيق أولاً:**
   ```bash
   npm run dev
   ```

2. **تأكد من وجود ملف `.env.local`:**
   ```env
   MONGODB_URI=mongodb+srv://...
   JWT_SECRET=your-secret
   ```

3. **في حالة وجود مشاكل:**
   - استخدم `npm run check-admin` للفحص
   - تأكد من صحة بيانات الاتصال بقاعدة البيانات

## 🔧 استكشاف الأخطاء

### مشكلة: "البريد الإلكتروني أو كلمة المرور غير صحيحة"
**الحل:**
```bash
npm run simple-admin
npm run check-admin
```

### مشكلة: "لا يمكن الاتصال بقاعدة البيانات"
**الحل:**
- تأكد من صحة `MONGODB_URI` في `.env.local`
- تأكد من أن قاعدة البيانات متاحة

### مشكلة: "المدير غير موجود"
**الحل:**
```bash
npm run simple-admin
```

## 📞 الدعم

في حالة وجود أي مشاكل، تأكد من:
1. تشغيل التطبيق: `npm run dev`
2. فحص المدير: `npm run check-admin`
3. إنشاء مدير جديد: `npm run simple-admin` 