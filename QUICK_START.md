# 🚀 دليل التشغيل السريع - منصة ربح

## تم إصلاح جميع الأخطاء! ✅

تم إصلاح المشاكل التالية:
- ✅ خطأ 500 في API Categories
- ✅ أخطاء Socket.io 404
- ✅ إضافة API endpoints للحذف والتحديث
- ✅ تحسين NotificationProvider
- ✅ إنشاء Custom Server للـ Socket.io
- ✅ إعداد ملف البيئة

## 📋 متطلبات التشغيل

1. **Node.js 18+**
2. **MongoDB 6+** (محلي أو MongoDB Atlas)
3. **حساب Cloudinary** (لرفع الصور)

## ⚡ التشغيل السريع

### 1. إعداد ملف البيئة
```bash
# انسخ ملف البيئة المثال
cp .env.local.example .env.local
```

### 2. تحديث ملف `.env.local`
```env
# قاعدة البيانات - مطلوب
MONGODB_URI=mongodb://localhost:27017/ribh-ecommerce

# JWT السر - مطلوب
JWT_SECRET=ribh-super-secret-jwt-key-change-in-production-2024

# Cloudinary - مطلوب لرفع الصور
CLOUDINARY_CLOUD_NAME=your-cloudinary-cloud-name
CLOUDINARY_API_KEY=your-cloudinary-api-key
CLOUDINARY_API_SECRET=your-cloudinary-api-secret

# الموقع الأساسي - مطلوب
NEXT_PUBLIC_APP_URL=http://localhost:3000
```

### 3. تثبيت التبعيات
```bash
npm install
```

### 4. تشغيل المشروع
```bash
# تشغيل مع Custom Server (موصى به)
npm run dev

# أو تشغيل Next.js العادي (بدون Socket.io)
npm run dev:next
```

### 5. إنشاء مستخدم إداري
```bash
# إنشاء مستخدم إداري سريع
npm run simple-admin
```

## 🔧 إعدادات Cloudinary

1. سجل في [Cloudinary](https://cloudinary.com)
2. احصل على:
   - Cloud Name
   - API Key  
   - API Secret
3. ضعها في ملف `.env.local`

## 🗄️ إعداد قاعدة البيانات

### MongoDB محلي:
```bash
# تشغيل MongoDB
mongod

# إنشاء قاعدة البيانات
mongo
use ribh-ecommerce
```

### MongoDB Atlas:
1. إنشاء حساب في [MongoDB Atlas](https://cloud.mongodb.com)
2. إنشاء cluster
3. نسخ connection string
4. وضعه في `MONGODB_URI`

## 📱 الوصول للمنصة

### صفحات المستخدمين:
- **الرئيسية**: http://localhost:3000
- **تسجيل الدخول**: http://localhost:3000/auth/login
- **التسجيل**: http://localhost:3000/auth/register

### لوحة التحكم:
- **لوحة التحكم**: http://localhost:3000/dashboard
- **إدارة الفئات**: http://localhost:3000/dashboard/admin/categories
- **إدارة المستخدمين**: http://localhost:3000/dashboard/admin/users

## 🛡️ أدوار المستخدمين

### 1. الإدارة (admin)
- إدارة جميع جوانب المنصة
- اعتماد المنتجات والموردين
- إدارة الفئات والإعدادات
- عرض التحليلات والتقارير

### 2. المورد (supplier)
- إضافة وإدارة المنتجات
- عرض الطلبات والأرباح
- طلبات التخزين في المستودع
- إدارة المحفظة الإلكترونية

### 3. المسوق (marketer)
- تصفح المنتجات المعتمدة
- طلب المنتجات للعملاء
- إدارة المفضلة
- عرض العمولات والأرباح

### 4. تاجر الجملة (wholesaler)
- شراء بأسعار الجملة
- طلب كميات كبيرة
- أرباح أعلى من المسوقين
- تكاملات مع المتاجر الخارجية

## 🔍 الميزات المتاحة

### ✅ مكتمل
- نظام المصادقة الكامل
- إدارة الفئات (إضافة، تعديل، حذف)
- إدارة المستخدمين
- رفع الصور عبر Cloudinary
- Socket.io للإشعارات الفورية
- الوضع المظلم الشامل
- دعم RTL كامل للعربية
- نظام المحافظ الإلكترونية
- إدارة الطلبات
- التحليلات والتقارير

### 🚧 قيد التطوير
- تكاملات المتاجر الخارجية
- نظام الدردشة المباشر
- تكاملات الشحن
- تطبيق الهاتف المحمول

## 🐛 استكشاف الأخطاء

### مشكلة اتصال قاعدة البيانات:
```bash
# تحقق من تشغيل MongoDB
mongod --version

# تحقق من connection string
echo $MONGODB_URI
```

### مشكلة Socket.io:
```bash
# تأكد من استخدام Custom Server
npm run dev

# تحقق من console logs
```

### مشكلة رفع الصور:
```bash
# تحقق من إعدادات Cloudinary في .env.local
# تأكد من صحة المفاتيح
```

## 📚 موارد إضافية

- [توثيق Next.js](https://nextjs.org/docs)
- [توثيق MongoDB](https://docs.mongodb.com)
- [توثيق Cloudinary](https://cloudinary.com/documentation)
- [توثيق Socket.io](https://socket.io/docs)

## 💬 الدعم

إذا واجهت أي مشاكل:
1. تحقق من console logs
2. تأكد من ملف `.env.local`
3. تحقق من تشغيل MongoDB
4. راجع هذا الدليل

---
**منصة ربح** - نظام التجارة الإلكترونية الذكي 🏪 