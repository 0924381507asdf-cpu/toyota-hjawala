# TOYOTA HJAWALA — corrected asset build

## الملفات المطلوبة
- `index.html` في جذر المشروع (اسم الملف يجب أن يبقى كما هو).
- `assets/toyota_hilux.glb`
- `assets/american_road.glb`

## النشر على Vercel
1. ارفع الملفات الثلاثة/المجلدات إلى جذر مستودع GitHub.
2. تأكد أن `index.html` ليس باسم `index(2).html`.
3. تأكد أن أسماء مجسمات GLB مطابقة تماماً للأسماء أعلاه.
4. في Vercel افتح المشروع ثم Deployments وأعد النشر بعد رفع التعديلات.
5. إعدادات المشروع لموقع HTML ثابت:
   - Framework Preset: Other
   - Build Command: اتركه فارغاً
   - Output Directory: `.` أو اتركه فارغاً حسب إعداد Vercel
   - Root Directory: `./`

## التحكم
- أزرار الشاشة: يمين، يسار، بنزين، فرامل، هاند بريك.
- الكمبيوتر: الأسهم أو WASD، والمسافة للهاند بريك.
- إعادة السيارة: زر إعادة السيارة.
- تغيير زاوية الكاميرا: زر تغيير الكاميرا.

## تصحيحات هذه النسخة
- تصحيح اسم ملف الطريق ليتطابق مع مسار التحميل.
- تثبيت اسم الصفحة الرئيسية `index.html`.
- إزالة تدوير 90 درجة غير الصحيح؛ ملفات GLB بوضعية Y-up.
- وضع المجسمين على مستوى الأرض مع توسيطهما.
- إضافة مجموعة Pivot للسيارة حتى تدور حول مركزها أثناء القيادة.

## متطلبات التشغيل
يحتاج المتصفح إلى اتصال بالإنترنت لتحميل Three.js من jsDelivr.

## إسناد المجسمات (CC BY 4.0)
- Toyota Hilux 2007 — David_Holiday: https://sketchfab.com/3d-models/toyota-hilux-2007-0234ebed01ee4b87affed0e58673247e
- American Road — jimbogies: https://sketchfab.com/3d-models/american-road-179a1e6a0a154031a60f300fc73d9dd8

## إصلاح Import Map
تم تعريف `three` و`three/addons/` باستخدام Import Map قبل سكربت اللعبة، حتى يتمكن المتصفح من حل الاستيرادات الداخلية في GLTFLoader.
