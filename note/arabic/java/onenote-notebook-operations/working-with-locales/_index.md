---
date: 2026-01-05
description: تعلم كيفية تعيين اللغة الافتراضية، تحميل مستند OneNote، تعيين ترخيص Aspose،
  تحويل OneNote إلى PNG وحفظ OneNote كصورة باستخدام Aspose.Note للغة Java.
linktitle: Working with Locales in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: تعيين اللغة الافتراضية في OneNote – Aspose.Note Java
url: /ar/java/onenote-notebook-operations/working-with-locales/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تعيين اللغة الافتراضية في OneNote – Aspose.Note Java

## المقدمة

إذا كنت بحاجة إلى **تعيين اللغة الافتراضية** أثناء معالجة ملفات OneNote، فإن Aspose.Note for Java يجعل ذلك سهلًا للغاية. في هذا البرنامج التعليمي سنستعرض كل ما تحتاجه — من ترخيص المنتج إلى تحميل مستند OneNote، تغيير اللغة، وأخيرًا تحويل الملف إلى صورة PNG. في النهاية، ستكون قادرًا على تخصيص إعدادات اللغة وإنشاء مخرجات مخصصة للغة المحددة ببضع أسطر من الشيفرة فقط.

## إجابات سريعة
- **ماذا يفعل “تعيين اللغة الافتراضية”؟** يحدد اللغة وتنسيق المنطقة التي يستخدمها Aspose.Note عند قراءة أو كتابة ملفات OneNote.  
- **هل أحتاج إلى ترخيص؟** نعم — قم بتعيين ترخيص Aspose لفتح جميع الوظائف.  
- **ما نسخة Java المطلوبة؟** أي JDK 8+ مدعومة.  
- **هل يمكنني تحويل OneNote إلى PNG؟** بالتأكيد؛ تتيح لك الـ API حفظ الصفحات كصور.  
- **هل العملية آمنة في بيئة متعددة الخيوط؟** تعيين اللغة الافتراضية هو إعداد عالمي، لذا يتم تكوينه مرة واحدة عند بدء تشغيل التطبيق.

## ما هو “set default locale” في Aspose.Note؟
تعيين اللغة الافتراضية يخبر Aspose.Note أي لغة وعادات ثقافية يجب تطبيقها عند تحليل التواريخ والأرقام والنصوص. هذا أمر أساسي للتطبيقات متعددة المناطق التي تحتاج إلى تنسيق ثابت عبر لغات المستخدمين المختلفة.

## لماذا تعيين اللغة الافتراضية عند العمل مع OneNote؟
- **تمثيل البيانات بدقة:** تظهر التواريخ والأرقام بشكل صحيح للجمهور المستهدف.  
- **ثبات سلاسل واجهة المستخدم:** النص المستخرج من OneNote يحترم إعدادات اللغة.  
- **تبسيط التحويل:** عندما تقوم لاحقًا بتحويل ملف OneNote إلى PNG أو صيغ أخرى، يتطابق التخطيط البصري مع اللغة المتوقعة.

## المتطلبات المسبقة

- **بيئة تطوير Java:** تثبيت JDK وتكوين المتغير `JAVA_HOME`.  
- **مكتبة Aspose.Note:** تحميل أحدث ملف JAR من [رابط التحميل](https://releases.aspose.com/note/java/).  
- **ملف ترخيص Aspose صالح** (الإصدار التجريبي المجاني يكفي للاختبار).

## استيراد الحزم

قبل كتابة أي شفرة، استورد الفئات التي توفر الوظائف المطلوبة.

```java
import java.io.IOException;
import java.nio.file.Path;
import java.util.Locale;
import com.aspose.note.Document;
import com.aspose.note.License;
import com.aspose.note.LocaleOptions;
```

## الخطوة 1: تعيين ترخيص Aspose

```java
License license = new License();
license.setLicense("licenseFile");
```

تعيين ترخيص Aspose يفتح جميع الميزات، بما في ذلك معالجة اللغة وتحويل الصور.

## الخطوة 2: تعيين اللغة الافتراضية

```java
java.util.Locale.setDefault(new java.util.Locale("en", "rs"));
```

هنا نقوم **بتعيين اللغة الافتراضية** إلى الإنجليزية (`en`) مع رمز الدولة `rs`. عدل رموز اللغة والدولة لتتناسب مع المنطقة المستهدفة لديك.

## الخطوة 3: تحميل مستند OneNote

```java
String inputFile = "Sample1.one";
Path inputPath = Paths.get(inputFile);

Document oneFile = new Document(inputPath.toString());
```

هذه الخطوة **تحمّل مستند OneNote** إلى كائن `Document` حتى تتمكن من التعامل مع محتوياته.

## الخطوة 4: تحويل OneNote إلى PNG (تحويل ملف OneNote)

```java
oneFile.save("sample.png");
```

طريقة `save` تقوم بـ **تحويل ملف OneNote**، وتصدّر دفتر الملاحظات (أو صفحة محددة) كصورة PNG — أي **تحويل OneNote إلى PNG** و**حفظ OneNote كصورة**.

## المشكلات الشائعة والنصائح

- **الترخيص غير موجود:** تأكد من صحة المسار إلى `licenseFile` وأن الملف يمتلك صلاحيات القراءة.  
- **اللغة غير مطبقة:** استدعِ `Locale.setDefault` **قبل** تحميل المستند.  
- **عدم وجود صورة ناتجة:** تحقق من أن ملف OneNote يحتوي فعليًا على صفحات قابلة للعرض؛ دفاتر الملاحظات الفارغة ستنتج PNG فارغًا.

## الأسئلة المتكررة

**س: هل Aspose.Note متوافق مع إصدارات Java المختلفة؟**  
ج: نعم، يدعم Aspose.Note Java 8 وما بعده، مما يضمن توافقًا واسعًا عبر بيئات التطوير.

**س: هل يمكنني دمج Aspose.Note مع مكتبات Java أخرى؟**  
ج: بالتأكيد. تعمل الـ API بسلاسة مع مكتبات شائعة مثل Apache POI وJackson وSpring.

**س: هل يقدم Aspose.Note دعمًا لصيغ ملفات مختلفة؟**  
ج: رغم أن تركيزه الأساسي هو ملفات OneNote، إلا أن المكتبة يمكنها التصدير إلى PNG وJPEG وPDF وصيغ صور أخرى.

**س: هل هناك منتدى مجتمع لمستخدمي Aspose.Note للحصول على المساعدة ومشاركة المعرفة؟**  
ج: نعم، يوفر منتدى مجتمع Aspose منصة للمستخدمين للتواصل مع الخبراء، طرح الأسئلة، والتعاون على حلول. زر [منتدى الدعم](https://forum.aspose.com/c/note/28) للحصول على المساعدة.

**س: هل يمكنني تجربة Aspose.Note قبل الشراء؟**  
ج: بالطبع، يمكنك استكشاف قدرات Aspose.Note من خلال النسخة التجريبية المجانية المتاحة على الموقع.

## الخلاصة

باتباع هذه الخطوات تعلمت كيفية **تعيين اللغة الافتراضية**، **تحميل مستند OneNote**، **تعيين ترخيص Aspose**، و**تحويل OneNote إلى PNG** باستخدام Aspose.Note for Java. هذه العملية تمكنك من إنشاء تقارير وصور حساسة للغة تلبي احتياجات الجمهور العالمي.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-05  
**Tested With:** Aspose.Note 24.11 for Java  
**Author:** Aspose