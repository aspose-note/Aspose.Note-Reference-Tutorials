---
date: 2026-03-19
description: تعلم كيفية استخراج صور OneNote باستخدام Java ومكتبة Aspose.Note. يوضح
  هذا الدليل خطوة بخطوة كيفية استخراج الصور من ملفات .one بسرعة وموثوقية.
linktitle: extract onenote images java – Extract Images from OneNote
second_title: Aspose.Note Java API
title: استخراج صور OneNote بجافا – استخراج الصور من OneNote
url: /ar/java/onenote-hyperlinks-images/extract-images/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# استخراج صور OneNote باستخدام Java – كيفية استخراج الصور من مستند OneNote باستخدام Java

## المقدمة

في هذا الدرس ستكتشف **كيفية استخراج صور OneNote باستخدام Java** باستخدام مكتبة Aspose.Note for Java. سواء كنت تحتاج الصور للتقارير أو الأرشفة أو لإدخالها في خط أنابيب OCR، سنرشدك خلال سير العمل بالكامل — من تحميل دفتر ملاحظات `.one` إلى حفظ كل صورة كملف منفصل على القرص.

## إجابات سريعة
- **ما المكتبة الموصى بها؟** Aspose.Note for Java  
- **هل يمكنني استخراج الصور من دفتر ملاحظات محمي بكلمة مرور؟** نعم، يدعم Aspose.Note ذلك.  
- **هل أحتاج إلى ترخيص للتطوير؟** النسخة التجريبية المجانية تعمل للاختبار؛ الترخيص مطلوب للإنتاج.  
- **ما إصدارات Java المدعومة؟** Java 8 وأحدث (بما في ذلك Java 15).  
- **كم يستغرق استخراج الصور؟** عادةً بضع ثوانٍ لدفتر ملاحظات قياسي.  

## ما هو **استخراج الصور من .one**؟

استخراج الصور من ملف OneNote يعني تحديد كل صورة مدمجة في دفتر ملاحظات `.one` برمجيًا وكتابة كل واحدة كملف صورة منفصل (PNG، JPEG، GIF، إلخ). هذا مفيد عندما تريد إعادة استخدام الرسومات خارج بيئة OneNote.

## لماذا استخراج صور OneNote باستخدام Java؟

- **الأتمتة:** معالجة العشرات أو المئات من دفاتر الملاحظات دون نقرات يدوية.  
- **الاتساق:** يضمن منطق استخراج متطابق عبر جميع الملفات.  
- **التكامل:** ربط الناتج بسهولة مع سير عمل آخر مبني على Java مثل OCR، تحليل الصور، أو أنظمة إدارة المحتوى.  

## المتطلبات المسبقة

قبل البدء، تأكد من أن لديك العناصر التالية جاهزة:

1. **Java Development Kit (JDK)** – قم بتثبيت Java 8 أو أحدث. يمكنك تنزيله من [الموقع الإلكتروني](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).  
2. **Aspose.Note Library** – قم بتنزيل أحدث حزمة Aspose.Note for Java وأضفها إلى مسار الفئات (classpath) في مشروعك. احصل عليها من [رابط التحميل](https://releases.aspose.com/note/java/).  

## استيراد الحزم

لبدء العمل، استورد الفئات Java اللازمة:

```java
import java.io.IOException;
import java.nio.file.Files;
import java.nio.file.Paths;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.Image;
```

## الخطوة 1: تحميل مستند OneNote

أولاً، وجه الـ API إلى المجلد الذي يحتوي على ملف `.one` الخاص بك وحمّل دفتر الملاحظات:

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```

## الخطوة 2: استرجاع جميع الصور

اطلب من Aspose.Note كل عقدة `Image` داخل المستند. هذا هو جوهر عملية **استخراج صور OneNote باستخدام Java**:

```java
List<Image> list = doc.getChildNodes(Image.class);
System.out.printf("Total Images: %s\n\n", list.size());
```

## الخطوة 3: حفظ كل صورة على القرص

قم بالتكرار عبر المجموعة، استخرج البايتات الخام، واكتب كل صورة إلى ملف باسم فريد:

```java
for (int i = 0; i < list.size(); i++) {
    Image image = list.get(i);
    String outputFile = "ExtractImages_out" + i + "_" + image.getFileName();
    byte[] buffer = image.getBytes();
    Files.write(Paths.get(dataDir + outputFile), buffer);
    System.out.printf("File saved: %s\n", dataDir);
}
```

### ما الذي يحدث خلف الكواليس؟

- `image.getBytes()` تُعيد بيانات الصورة الأصلية (PNG، JPEG، GIF، إلخ).  
- `image.getFileName()` يحافظ على الاسم الأصلي، مما يسهل تتبع المصدر.  

## المشكلات الشائعة والحلول
- **لم يتم العثور على صور:** تحقق من أن ملف `.one` المصدر يحتوي فعليًا على صور مدمجة.  
- **أخطاء أذونات الملف:** تأكد من أن مجلد `dataDir` قابل للكتابة من قبل عملية Java.  
- **تنسيقات صور غير مدعومة:** يدعم Aspose.Note PNG، JPEG، GIF، BMP، وTIFF. بالنسبة للتنسيقات الغريبة، فكر في تحويل دفتر الملاحظات في OneNote أولاً.  

## الأسئلة المتكررة

**س: هل يمكنني استخراج الصور من مستندات OneNote المحمية بكلمة مرور؟**  
ج: نعم، يدعم Aspose.Note فتح دفاتر الملاحظات المشفرة واستخراج صورها.

**س: هل Aspose.Note متوافق مع إصدارات Java المختلفة؟**  
ج: المكتبة تعمل مع Java 8 وأحدث، لذا يمكنك تشغيلها على Java 11، Java 15، أو الإصدارات الأحدث.

**س: هل يمكنني استخراج الصور من عدة ملفات OneNote في تشغيل واحد؟**  
ج: بالتأكيد. فقط ضع منطق الاستخراج داخل حلقة تتكرر على قائمة مسارات ملفات `.one`.

**س: هل هناك حدود لحجم دفاتر الملاحظات التي يمكنني معالجتها؟**  
ج: يتعامل Aspose.Note بفعالية مع دفاتر ملاحظات كبيرة؛ لا يوجد حد ثابت لحجم استخراج الصور.

**س: هل يسمح Aspose.Note باستخراج أنواع محتوى أخرى؟**  
ج: نعم، يمكنك أيضًا استخراج النصوص، الجداول، الملفات المدمجة، وغيرها من الكائنات باستخدام واجهات برمجة تطبيقات مماثلة.

---

**آخر تحديث:** 2026-03-19  
**تم الاختبار مع:** Aspose.Note for Java 24.12  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}