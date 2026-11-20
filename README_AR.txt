NEXORA SND — Professional Cloud Edition
========================================

محتويات المشروع
- index.html / style.css / app.js: واجهة الموقع الاحترافية.
- netlify/functions/measure.mjs: وظيفة قياس HTTP تعمل على Netlify.
- netlify.toml: إعدادات النشر.

النشر من GitHub إلى Netlify
1) أنشئ مستودع GitHub جديداً.
2) ارفع محتويات هذا المجلد إلى جذر المستودع (وليس ملف ZIP).
3) في Netlify اختر Add new project ثم Import an existing project.
4) اختر مستودع GitHub هذا.
5) اترك Build command فارغاً، وPublish directory = .
6) انشر الموقع. يجب أن يرفع Netlify وظيفة netlify/functions/measure.mjs أيضاً.

مهم جداً عن القياسات
هذه نسخة Cloud Edition. وظيفة القياس تنفذ طلبات HTTP من بيئة Netlify إلى ثلاثة مواقع عامة، وتحسب متوسط زمن الاستجابة وتغيره ونسبة فشل طلبات HTTP. هذه ليست ICMP ping ولا packet loss، ولا تقيس شبكة المنزل أو الراوتر أو Wi-Fi. لقياس الشبكة المحلية يلزم Raspberry Pi أو جهاز قياس داخل الشبكة.

سجل الاختبارات يُحفظ في localStorage داخل المتصفح فقط، وليس قاعدة بيانات سحابية مشتركة. لا توجد مفاتيح API مطلوبة.

نسخة Raspberry Pi منفصلة ويمكن إضافتها لاحقاً؛ هذا الأرشيف مخصص للنشر السحابي على Netlify.
