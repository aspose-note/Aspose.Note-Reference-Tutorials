---
date: 2026-03-05
description: تعلم تنسيق جداول OneNote باستخدام Aspose.Note للغة Java. يوضح هذا الدليل
  كيفية تعيين لون خلفية الخلية، وتطبيق خلفية الخلية، وتغيير لون خلية OneNote بسهولة.
linktitle: 'Onenote Table Formatting: Setting Cell Background Color with Aspose.Note'
second_title: Aspose.Note Java API
title: 'تنسيق جدول OneNote: تعيين لون خلفية الخلية باستخدام Aspose.Note'
url: /ar/java/onenote-table-manipulation/setting-cell-background-color/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تنسيق جدول OneNote: تعيين لون خلفية الخلية

## المقدمة
في هذا البرنامج التعليمي ستكتشف كيفية تنفيذ **تنسيق جدول OneNote** عن طريق تعيين لون خلفية الخلية باستخدام Aspose.Note for Java. سواءً كنت تبني تقريرًا، دليلًا دراسيًا، أو دفتر ملاحظات تعاوني، فإن تخصيص ألوان الخلايا يساعدك على إبراز البيانات الرئيسية وتحسين قابلية القراءة. لنستعرض الخطوات معًا.

## إجابات سريعة
- **ما المكتبة المطلوبة؟** Aspose.Note for Java.  
- **أي طريقة تغير اللون؟** `setBackgroundColor(Color)` على كائن `TableCell`.  
- **هل يمكن تطبيق اللون على عدة خلايا؟** نعم – عبر حلقة تمر على الصفوف والخلايا.  
- **هل أحتاج إلى ترخيص للإنتاج؟** يلزم وجود ترخيص Aspose صالح؛ يتوفر إصدار تجريبي مجاني.  
- **ما نسخة Java المدعومة؟** Java 8+ (أو أحدث) تعمل مع أحدث إصدار من Aspose.Note.

## ما هو تنسيق جدول OneNote؟
يشير تنسيق جدول OneNote إلى مجموعة خيارات التنسيق—مثل الحدود، والمحاذاة، وألوان الخلفية—التي يمكنك تطبيقها على الجداول داخل صفحات OneNote. تعديل ألوان خلفية الخلايا طريقة شائعة لجذب الانتباه إلى المعلومات الهامة.

## لماذا تعيين لون خلفية الخلية في OneNote؟
- **التسلسل البصري:** إبراز الإجماليات، التحذيرات، أو عناوين الأقسام.  
- **اتساق العلامة التجارية:** مطابقة ألوان الشركة عبر الوثائق.  
- **قابلية القراءة:** جعل الجداول الكثيفة أسهل للعين، خاصةً على الشاشات الكبيرة.  

## المتطلبات المسبقة
قبل أن نبدأ، تأكد من توفر المتطلبات التالية:
1. مكتبة Aspose.Note for Java: حمّلها وثبّتها من [هنا](https://releases.aspose.com/note/java/).  
2. بيئة تطوير Java: قم بإعداد بيئة تطوير Java الخاصة بك.  
3. دليل المستندات: احرص على وجود دليل يحتوي على مستند OneNote الخاص بك.  

الآن، دعنا نغوص في البرنامج التعليمي!

## استيراد الحزم
أولاً، استورد الحزم اللازمة إلى مشروع Java الخاص بك:
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.OutlineElement;
import com.aspose.note.RichText;
import com.aspose.note.TableCell;
import com.aspose.note.TableRow;
import com.aspose.note.ParagraphStyle;
```

## كيفية تعيين لون خلفية الخلية في جداول OneNote؟
### الخطوة 1: إعداد مشروعك
تأكد من جاهزية بيئة تطوير Java، وأنك قد دمجت Aspose.Note for Java في مشروعك.

### الخطوة 2: تحميل مستند OneNote الخاص بك
```java
Document doc = new Document();
```

### الخطوة 3: تهيئة كائن TableRow
أنشئ كائن `TableRow` لتمثيل صف في جدول OneNote الخاص بك:
```java
TableRow row1 = new TableRow();
```

### الخطوة 4: تهيئة كائن TableCell
تهيئ كائن `TableCell` داخل الصف وضع المحتوى النصي المطلوب:
```java
TableCell cell11 = new TableCell();
cell11.appendChildLast(GetOutlineElementWithText("Small text"));
```

### الخطوة 5: تعيين لون خلفية الخلية
استخدم طريقة `setBackgroundColor` لتخصيص لون خلفية الخلية (في هذا المثال، تم تعيينه إلى الأسود):
```java
cell11.setBackgroundColor(Color.BLACK);
```

### الخطوة 6: حفظ المستند الخاص بك
لا تنس حفظ مستند OneNote المعدل بعد إجراء التغييرات اللازمة.

> **نصيحة احترافية:** إذا أردت تطبيق نفس الخلفية على عمود كامل، كرّر الحلقة عبر كل صف واستدعِ `setBackgroundColor` على الخلية المقابلة.

## كيفية تطبيق لون خلفية الخلية على خلايا متعددة؟
يمكنك المرور عبر صفوف الجدول وخلاياه، وتطبيق نفس استدعاء `setBackgroundColor` حيثما تحتاج. هذه الطريقة فعّالة عندما يكون لديك جداول كبيرة أو تريد تلوين أقسام كاملة.

## كيفية تغيير لون خلية OneNote برمجياً؟
إلى جانب الألوان الصلبة، يدعم Aspose.Note قيم RGB مخصصة. استبدل `Color.BLACK` بـ `new Color(r, g, b)` لتطابق أي لوحة ألوان للعلامة التجارية.

## المشكلات الشائعة والحلول
- **NullPointerException عند الوصول إلى خلية:** تأكد من إضافة الخلية إلى صف قبل تعيين خلفيتها.  
- **اللون لا يظهر بعد الحفظ:** تحقق من أنك تحفظ المستند باستخدام `doc.save("output.one")` وأن نسخة OneNote المستهدفة تدعم تنسيق الجداول.  
- **أخطاء الترخيص:** النسخة التجريبية تكفي للتقييم، لكن الترخيص الكامل مطلوب للنشر في بيئات الإنتاج.

## الأسئلة المتكررة

**س: هل يمكنني تطبيق هذه الطريقة على عدة خلايا في آن واحد؟**  
ج: نعم، يمكنك المرور عبر صفوف الجدول وخلاياه لتطبيق لون الخلفية على عدة خلايا simultaneouly.

**س: هل هناك ألوان مسبقة التعريف يمكنني استخدامها؟**  
ج: يدعم Aspose.Note مجموعة واسعة من الألوان، بما في ذلك الثوابت المسبقة مثل `Color.BLACK`. راجع الوثائق [هنا](https://reference.aspose.com/note/java/) للقائمة الكاملة.

**س: هل يتوفر إصدار تجريبي؟**  
ج: نعم، يمكنك الحصول على نسخة تجريبية مجانية [هنا](https://releases.aspose.com/).

**س: كيف يمكنني الحصول على الدعم إذا واجهت مشاكل؟**  
ج: زر منتدى الدعم [هنا](https://forum.aspose.com/c/note/28) للحصول على مساعدة من مجتمع Aspose.

**س: أين يمكنني شراء Aspose.Note for Java؟**  
ج: يمكنك شراء المكتبة [هنا](https://purchase.aspose.com/buy).

## الخاتمة
تهانينا! لقد تعلمت بنجاح كيفية تنفيذ **تنسيق جدول OneNote** عن طريق تعيين ألوان خلفية الخلايا في OneNote باستخدام Aspose.Note for Java. جرّب ألوانًا مختلفة، وطبق التقنية على صفوف أو أعمدة كاملة، ودمجها في خطوط تقاريرك الآلية للحصول على مظهر مصقول واحترافي.

---

**آخر تحديث:** 2026-03-05  
**تم الاختبار مع:** Aspose.Note for Java 24.11 (أحدث نسخة وقت الكتابة)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}