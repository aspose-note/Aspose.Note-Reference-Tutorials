---
date: 2026-01-12
description: تعلم كيفية التراجع عن صفحات OneNote واستعادة النسخة السابقة من OneNote
  باستخدام Aspose.Note للغة Java. اتبع هذا الدليل خطوة بخطوة لإدارة مستندات فعّالة.
linktitle: How to Roll Back OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: كيفية التراجع عن OneNote - Aspose.Note
url: /ar/java/onenote-page-manipulation/roll-back-to-previous-page-version/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية التراجع عن OneNote - Aspose.Note

## مقدمة

إذا كنت تبحث عن طريقة تصفية برمجية **كيفية استرجاع OneNote** للصفحات عندما يحدث خطأ، مطلوب في المكان الصحيح. في هذا الدرس سنستعرض كيفية استخدام Aspose.Note for Java لإرجاع صفحة OneNote إلى حالة سابقة. سواءً كنت تبدأ أداة إدارة التعليقات بطريقة ميكانيكية أو تحتاج إلى شبكة أمان للأفكار التشاركية، فإن الحكمة عن صفحة تساعدك في الحفاظ على محتوى دقيق وموثوقًا.

## إجابات سريعة
- **ما معنى “التراجع” في OneNote؟** استعادة الصفحة إلى نسخة سابقة محفوظة في تاريخها.
- **أي API يشير إلى السماء؟** فئة `PageHistory` في Aspose.Note لـ Java.
- **هل أحتاج إلى ترخيص؟** يلزم الحاجة إلى ترخيص لـ Aspose.Note للاستخدام في بيئة الإنتاج.
- **هل يمكنني اختيار أي نسخة سابقة؟** نعم – يمكنك اختيار أي كتاب من قائمة تاريخ القائمة.
- **هل هذه الطريقة الآمنة للملاحظات الجديدة؟** تأكيد؛ تعمل على تصفيات دون تحميل الدفتر بالكامل في الذاكرة.

## كيفية استرجاع إصدار صفحة OneNote
باختصار، يوضح الدليل بالتفصيل كيفية تنفيذ الهدف بالضبط. كل ما تتضمنه شرحًا موجزًا ​​لفهم *لماذا* الكتاب المقدس، وليس فقط *ماذا* نكتب.

## المتطلبات الأساسية

قبل الغوص في الشيفرة، تأكد من جاهزية ما يلي:

### إعداد بيئة تطوير جافا
1. **تثبيت مجموعة تطوير جافا (JDK):** احصل على أحدث JDK من موقع Oracle أو من مدير الحزم المفضل لديك.
2. **تكوين متغيرات البيئة:** عيّن `JAVA_HOME` مشاركًا في `PATH` بحيث تكون أوامر `java` و `javac` من سطر المفيد.
3. **إضافة Aspose.Note for Java:** شبكة البنوك من [الموقع](https://purchase.aspose.com/buy) وأضف ملف JAR إلى مسار الفئة (classpath) في مشروعك.

## استيراد الحزم

للتفاعل مع ملفات OneNote، استورد الفئات الأساسية من Aspose.Note:

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## الخطوة 1: تحميل مستند OneNote
```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
```
نحدد أولاً المجلد الذي يحتوي على ملف `.one` ونحمّله إلى كائن `Document`.

## الخطوة 2: الحصول على سجل الصفحات
```java
Page page = document.getFirstChild();
PageHistory pageHistory = document.getPageHistory(page);
```
توفر لك `PageHistory` إمكانية الوصول إلى كل نسخة محفوظة من الصفحة المحددة، مما يتيح قدرة **restore previous onenote version**.

## الخطوة 3: حذف الصفحة الحالية
```java
document.removeChild(page);
```
بإزالة الصفحة الحالية نُفسح المجال للنسخة التي نريد إعادتها.

## الخطوة 4: إضافة نسخة الصفحة السابقة
```java
document.appendChildLast(pageHistory.get_Item(pageHistory.size() - 1));
```
هنا نختار أحدث إدخال تاريخي (يمكنك تعديل الفهرس لاستهداف أي نسخة أقدم) ونضيفه مرة أخرى إلى المستند.

## الخطوة 5: حفظ المستند
```java
document.save(dataDir + "RollBackToPreviousPageVersion_out.one");
```
أخيرًا، احفظ الدفتر المعدل. الآن يحتوي ملف الإخراج على الصفحة التي تم التراجع عنها.

## استعادة إصدار OneNote السابق
تجمع استخدام `PageHistory` مع `appendChildLast` المتنوعة لتتمكن من **استعادة نسخة onenote السابقة** ببضع أسطر من شيفرة فقط. هذا مفيد جدًا في سير العمل حيث لا يكون رسم يدوي ممكنًا.

## المشكلات والنصائح الشائعة
- **السجل الفارغ:** إذا النسخة `pageHistory.size()` القيمة 0، وهذا يعني أن الصفحة لا تملكها محفوظة — تأكد من تفعيل النسخ الاحتياطي في OneNote.
- **الفهرس خارج الحدود:** تذكر أن قائمة التاريخ تبدأ من الصفر. تعديل الفهرس (`size() - 1`) لاستهداف النسخة الدقيقة التي تحتاجها.
- **الأداء:** العمل على صفحة واحدة يتجنب تحميل الدفتر بالكامل في الذاكرة، مما يحافظ على السرعة الصحيحة حتى مع الملفات الكبيرة.

## خاتمة

أصبح لديك الآن طريقة كاملة وجاهزة للإنتاج **كيفية استرجاع Onenote** باستخدام Aspose.Note لـ Java. من خلال التسجيل من `PageHistory`، يمكنك استعادة أي حالة سابقة لصفحة الدفتر بأمان، مما يضمن سلامة البيانات ويمنح المستخدمين الثقة ببيئات التعاون.

## الأسئلة المتداولة

**س1: هل يمكنني أن أرغب في الحصول على عدة نسخ من الصفحة؟**
ج: نعم، يمكنك الوصول إلى تاريخ الصفحة بالكامل والرجوع إلى أي نسخة سابقة حسب الحاجة.

**س2: هل يدعم Aspose.Note لغات برمجة أخرى غير Java؟**
ج: نعم، يوفر Aspose.Note مكاتبات عديدة لغات برمجة، بما في ذلك .NET و C++ و Python.

**Q3: هل Aspose.Note متوافق مع جميع إصدارات OneNote؟**
ج: يدعم Aspose.Note صيغ OneNote المتنوعة، مما يضمن التوافق مع معظم إصدارات المستندات.

**Q4: هل يمكنني تخصيص مهام أخرى في OneNote باستخدام Aspose.Note؟**
ج: بالتأكيد، أرسل Aspose.Note للتعديل الشامل وحذف وتعديل المحتوى برمجيًا.

**Q5: هل هناك منتدى مجتمع أو دعم خيارات لـ Aspose.Note؟**
ج: نعم، يمكنك زيارة [منتدى Aspose.Note](https://forum.aspose.com/c/note/28) للحصول على دعم المجتمع أو التواصل مع عملاء Aspose للمساعدة.

---

**آخر تحديث:** 12-01-2026
**تم الاختبار باستخدام:** Aspose.Note لـ Java (أحدث إصدار)
**المؤلف:** اطرح 

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}