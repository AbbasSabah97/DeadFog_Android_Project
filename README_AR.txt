Dead Fog - مشروع Android Studio (WebView)
=======================================
المتطلبات: Android Studio (Hedgehog أو أحدث) مع JDK 17 المرفق به، واتصال بالإنترنت أول مرة لتنزيل Gradle.

1) افتح Android Studio ثم File > Open واختر هذا المجلد (الذي فيه settings.gradle).
2) انتظر انتهاء Gradle Sync.
3) لتجربة اللعبة: وصّل هاتفك (تفعيل USB debugging) واضغط Run.
4) لملف APK: Build > Build Bundle(s) / APK(s) > Build APK(s).
   للنشر في متجر Google Play: Build > Generate Signed Bundle / APK ثم اختر Android App Bundle (AAB) ووقّعه بمفتاحك.

ملاحظات:
- اللعبة كلها (HTML + المكتبات + الأصول) داخل app/src/main/assets ولا تحتاج إنترنت أثناء اللعب.
- لتغيير الأيقونة: أضف ic_launcher في res/mipmap-* وحدّث android:icon في AndroidManifest.xml.
- هذا المشروع لم يُبنَ ولم يُجرَّب على هاتف حقيقي في بيئة إعداده.

بناء APK عبر GitHub (بدون Android Studio)
-----------------------------------------
1) أنشئ مستودعاً جديداً على github.com وارفع محتويات هذا المجلد في جذر المستودع (يجب أن يكون settings.gradle في الجذر، ومعه المجلد المخفي .github).
2) افتح تبويب Actions، سيبدأ البناء تلقائياً (أو اضغط Run workflow على Build APK).
3) بعد نجاحه (حوالي 5 إلى 10 دقائق) افتح التشغيل وحمّل DeadFog-debug-apk من قسم Artifacts، وفيه app-debug.apk.
4) انقل الملف إلى هاتفك وثبّته (يلزم السماح بالتثبيت من مصدر غير معروف). هذا ملف تجريبي (debug).
للنشر على Google Play يلزم بناء AAB موقَّع بمفتاحك.
