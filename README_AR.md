# Custom Gameplay & World Dynamics — Forge 1.20.1

## المتطلبات
- Java JDK 17
- Minecraft Forge 1.20.1
- IntelliJ IDEA أو Eclipse مع دعم Gradle

## البناء
1. افتح المجلد كمشروع Gradle.
2. نفّذ `gradlew build` (على Windows: `gradlew.bat build`).
3. ضع الملف الناتج من `build/libs/` داخل مجلد `mods` في نسخة Minecraft Forge 1.20.1.

## الأصوات
ضع ملفات OGG التالية هنا:
`src/main/resources/assets/customgameplay/sounds/`
- `diamond_found.ogg`
- `netherite_found.ogg`
- `iron_found.ogg`
- `gold_found.ogg`
- `nether_entered.ogg`

أسماء الملفات يجب أن تطابق الأسماء في `sounds.json`.

## الموجود حاليًا
- تسجيل 20 كتلة زخرفية مع Blockstates / models / item models.
- تسجيل 5 أحداث صوتية.
- إشعارات استخراج الدايموند والنذررايت، وأول حديد/ذهب لكل لاعب باستخدام Persistent Data.
- إشعار دخول النذر.
- كيان Bandit مع مستويات تجهيز أولية ومدى متابعة يصل إلى 100 عند تفعيل وضع القناص.
- Renderer أساسي يحتاج texture في `assets/customgameplay/textures/entity/bandit.png`.

## حدود مهمة
هذه نسخة أساس قابلة للتطوير وليست تنفيذًا نهائيًا لكل المواصفات. القناص حاليًا يملك قوسًا ومدى متابعة 100، لكن منطق إطلاق سهام دقيق حتى 100 بلوك غير مكتمل. كما أن القواعد/الحصون/المتاهات، تضاريس الأنهار، ونشر الصخور تلقائيًا في العالم تحتاج تنفيذ worldgen وقوالب NBT إضافية. لا تستخدمها على عالم أساسي قبل اختبارها على عالم تجريبي.
