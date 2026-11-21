# نور القرآن — NoorQuran (Android)

تطبيق أندرويد لقراءة القرآن الكريم والاستماع إليه، مع التفاسير والترجمات والأذكار وأدعية المسلم.

## التنزيل

أحدث إصدار:

https://github.com/Abdelrahmanatta22/NoorQuran/releases/latest

رابط مباشر ثابت لأحدث APK:

https://github.com/Abdelrahmanatta22/NoorQuran/releases/latest/download/NoorQuran.apk

## طريقة إصدار نسخة جديدة

1. ارفع رقم `versionCode` و`versionName` في `app/build.gradle`، ثم ابنِ:

   ```
   gradlew assembleRelease
   ```

2. من صفحة المستودع: **Releases → Draft a new release**.
3. اختر Tag جديدًا مثل `v18.12`، واكتب عنوان الإصدار وملاحظات «ما الجديد».
4. أرفق الملف `app/build/outputs/apk/release/app-release.apk` باسمه الثابت
   **`NoorQuran.apk`** (الاسم مهم: الرابط المباشر يعتمد عليه).
5. انشر الإصدار.
6. حدّث ملف `update.json` في الفرع `main` بالقيم الجديدة (`versionCode`، `versionName`، `notes`).
   التطبيق يقرأ هذا الملف عند الفتح ويقارن رقمه برقم النسخة المثبتة.

## تنبيهات

- لا ترفع مفتاح التوقيع `keystore/noorquran.jks` ولا كلمات سره إلى المستودع.
  فقدان المفتاح يمنع إصدار تحديثات لمن ثبّت التطبيق، وتسريبه يسمح بتوقيع نسخ مزيّفة.
- التحديث يُثبّت فوق النسخة القديمة فقط إذا كان موقّعًا بالمفتاح نفسه وبـ`versionCode` أعلى.
- بيانات الأذكار مأخوذة من مشروع حصن المسلم مفتوح المصدر (GPL-3.0)؛ راجع الترخيص قبل أي نشر واسع.
