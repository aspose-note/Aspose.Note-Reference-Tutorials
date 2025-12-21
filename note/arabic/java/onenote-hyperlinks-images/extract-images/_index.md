---
date: 2025-12-21
description: تعلم كيفية استخراج الصور من مستندات OneNote باستخدام Java مع Aspose.Note.
  يوضح هذا الدليل خطوة بخطوة كيفية استخراج الصور بسرعة وموثوقية.
linktitle: How to Extract Images from OneNote Document using Java
second_title: Aspose.Note Java API
title: كيفية استخراج الصور من مستند OneNote باستخدام Java
url: /ar/java/onenote-hyperlinks-images/extract-images/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية استخراج الصور من مستند OneNote باستخدام Java

## المقدمة

في هذا الدرس، سنرشدك إلى **كيفية استخراج الصور** من مستند OneNote باستخدام Java بمساعدة مكتبة Aspose.Note. سواء كنت تحتاج الصور للتقارير أو الأرشفة أو المعالجة الإضافية، سيوضح لك هذا الدليل سير العمل بالكامل.

## إجابات سريعة
- **ما المكتبة الموصى بها؟** Aspose.Note for Java  
- **هل يمكن استخراج الصور من دفتر ملاحظات محمي بكلمة مرور؟** نعم، تدعم Aspose.Note ذلك.  
- **هل أحتاج إلى ترخيص للتطوير؟** النسخة التجريبية المجانية تكفي للاختبار؛ الترخيص مطلوب للإنتاج.  
- **ما إصدارات Java المدعومة؟** Java 8 وأحدث (بما في ذلك Java 15).  
- **كم يستغرق استخراج الصور؟** عادةً بضع ثوانٍ لدفتر ملاحظات قياسي.

## ما هو استخراج الصور من OneNote؟
يعني استخراج الصور تحديد كل صورة مدمجة في ملف OneNote (.one) برمجيًا وحفظ كل واحدة كملف صورة منفصل على القرص. هذا مفيد عندما تريد إعادة استخدام الرسومات خارج بيئة دفتر الملاحظات.

## لماذا استخراج الصور من OneNote باستخدام Java؟
- **الأتمتة:** معالجة دفاتر ملاحظات متعددة دفعة واحدة دون جهد يدوي.  
- **الاتساق:** يضمن نفس منطق الاستخراج عبر جميع الملفات.  
- **التكامل:** يمكن دمجه بسهولة مع سير عمل Java آخر (مثل OCR أو تحليل الصور).  

## المتطلبات المسبقة

قبل البدء، تأكد من توفر ما يلي:

1. **Java Development Kit (JDK)** – تأكد من تثبيت Java على نظامك. يمكنك تنزيله وتثبيته من [الموقع الإلكتروني](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).

2. **Aspose.Note Library** – قم بتنزيل مكتبة Aspose.Note وأدرجها في مشروع Java الخاص بك. يمكنك الحصول عليها من [رابط التنزيل](https://releases.aspose.com/note/java/).

## استيراد الحزم

لبدء، استورد الحزم اللازمة:

```java
import java.io.IOException;
import java.nio.file.Files;
import java.nio.file.Paths;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.Image;
```

## الخطوة 1: تحميل المستند

أولاً، حمّل مستند OneNote باستخدام Aspose.Note:

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```

## الخطوة 2: الحصول على جميع الصور

بعد ذلك، استرجع جميع الصور من المستند:

```java
List<Image> list = doc.getChildNodes(Image.class);
System.out.printf("Total Images: %s\n\n", list.size());
```

## الخطوة 3: استخراج الصور

تكرار عبر قائمة الصور وحفظ كل صورة في ملف:

```java
for (int i = 0; i < list.size(); i++) {
    Image image = list.get(i);
    String outputFile = "ExtractImages_out" + i + "_" + image.getFileName();
    byte[] buffer = image.getBytes();
    Files.write(Paths.get(dataDir + outputFile), buffer);
    System.out.printf("File saved: %s\n", dataDir);
}
```

## المشكلات الشائعة والحلول
- **لم يتم العثور على صور:** تأكد من أن ملف `.one` المصدر يحتوي فعليًا على صور مدمجة.  
- **أخطاء أذونات الملف:** تحقق من أن مسار `dataDir` قابل للكتابة.  
- **تنسيقات صور غير مدعومة:** تدعم Aspose.Note معظم التنسيقات الشائعة (PNG، JPEG، GIF). إذا كان هناك تنسيق غير مدعوم، فكر في تحويل دفتر الملاحظات في OneNote أولاً.

## الخلاصة

باتباع الخطوات أعلاه، أصبحت الآن تعرف **كيفية استخراج الصور** من مستند OneNote باستخدام Java ومكتبة Aspose.Note. يمكنك دمج هذه المنطق في تطبيقات أكبر، أتمتة المعالجة الدفعة، أو ببساطة استرجاع الرسومات لإعادة استخدامها.

## الأسئلة المتكررة

**س: هل يمكن استخراج الصور من مستندات OneNote المحمية بكلمة مرور؟**  
ج: نعم، تدعم Aspose.Note استخراج الصور من دفاتر ملاحظات محمية.

**س: هل Aspose.Note متوافق مع إصدارات Java المختلفة؟**  
ج: تعمل Aspose.Note مع Java 8 وأحدث، مما يمنحك مرونة عبر البيئات.

**س: هل يمكن استخراج الصور من عدة مستندات OneNote في تنفيذ واحد؟**  
ج: بالتأكيد. يمكنك تكرار قائمة مسارات الملفات وتطبيق نفس منطق الاستخراج على كل مستند.

**س: هل هناك أي قيود على حجم مستندات OneNote؟**  
ج: تدير Aspose.Note دفاتر ملاحظات كبيرة بكفاءة؛ لا يوجد حد ثابت لحجم استخراج الصور.

**س: هل تدعم Aspose.Note استخراج أنواع محتوى أخرى غير الصور؟**  
ج: نعم، يمكنك أيضًا استخراج النص، المرفقات، والكائنات المدمجة الأخرى.

---

**آخر تحديث:** 2025-12-21  
**تم الاختبار مع:** Aspose.Note for Java 24.12  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}