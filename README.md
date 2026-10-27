# Medoz TV

مشروع مستقل لتطبيق تلفزيون ذكي باسم **Medoz**، يستهدف شاشات Samsung Tizen، مع تطبيق موبايل للتحكم والتثبيت عند دعم المنصة.

## حالة المشروع
مرحلة تحليل المتطلبات والتصميم — **لم تبدأ البرمجة بعد**.

## مبادئ المشروع
- مجاني بالكامل: دون اشتراكات أو مشتريات داخل التطبيق.
- تصميم واجهة جديد مستقل.
- دعم العربية واتجاه RTL.
- العمل دون إنترنت في الوظائف التي يمكن تشغيلها محليًا.
- اختبار التوافق الفعلي مع إصدارات Samsung Tizen قبل إعلان الدعم.

## المكونات المخططة
- `apps/mobile/`: تطبيق الموبايل للاتصال والتحكم والتثبيت المدعوم.
- `apps/tizen-tv/`: تطبيق التلفزيون المتوافق مع Tizen.
- `docs/`: وثائق المتطلبات والتصميم والاختبارات.
- `assets/`: الأيقونات والخلفيات والأصول المرخصة.

## الوظائف المخططة
- واجهة رئيسية وثيمات قابلة للتخصيص.
- اكتشاف التلفزيون والاتصال به.
- ريموت موبايل ضمن صلاحيات المنصة.
- اختصارات التطبيقات.
- مواقيت الصلاة والأذان.
- راديو وقرآن ورقية شرعية من ملفات محلية وروابط بث.
- ساعة وطقس.
- IPTV لمصادر قانونية متوافقة.
- بروفايلات عائلية وحماية داخل التطبيق.
- إرسال وسائط للأجهزة المتوافقة.

## ملاحظات
- اسم المستودع المقترح: `Medoz-TV`.
- لا يحتوي هذا المستودع التمهيدي على كود Morph TV أو ملفات APK الخاصة به.
- لا تُعتبر أي ميزة متوافقة مع جميع الشاشات قبل اختبارها.

## Documentation map
- `docs/DESIGN-PROPOSAL.md` — visual direction.
- `docs/FINAL-DESIGN-SPEC.md` — dashboard and identity specification.
- `docs/REMOTE-AND-NAVIGATION.md` — TV remote behavior.
- `docs/MOBILE-COMPANION.md` — mobile companion scope and limitations.
- `docs/PRAYER-LOCATION-WEATHER.md` — time, prayer, location, and weather rules.
- `docs/AUDIO-AND-PLAYBACK.md` — audio and radio playback.
- `docs/HOME-SCREEN-AND-THEMES.md` — dashboard and theme requirements.
- `docs/IPTV-CASTING-AND-APP-SHORTCUTS.md` — optional integrations.
- `docs/OFFLINE-PRIVACY-SECURITY.md` — offline and privacy rules.
- `docs/COMPATIBILITY-AND-TEST-PLAN.md` — device validation plan.
- `docs/IMPLEMENTATION-ROADMAP.md` — phased delivery plan.
- `docs/OPEN-DECISIONS.md` — unresolved decisions.
- `docs/RELEASE-CHECKLIST.md` — release gate.

**Important:** This repository is a requirements and planning package. It does not yet contain a working Tizen or Android implementation.
