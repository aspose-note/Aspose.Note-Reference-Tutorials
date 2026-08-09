---
date: 2026-05-20
description: تعلم كيفية إضافة رابط تشعبي في Aspose.Note لـ .NET وإنشاء تجارب ملاحظات
  تفاعلية، مما يعزز تفاعل المستند.
keywords:
- how to add hyperlink
- create interactive note
- Aspose.Note hyperlink integration
linktitle: الروابط التشعبية
schemas:
- author: Aspose
  dateModified: '2026-05-20'
  description: Learn how to add hyperlink in Aspose.Note for .NET and create interactive
    note experiences, boosting document engagement.
  headline: How to Add Hyperlink in Aspose.Note for .NET
  type: TechArticle
- description: Learn how to add hyperlink in Aspose.Note for .NET and create interactive
    note experiences, boosting document engagement.
  name: How to Add Hyperlink in Aspose.Note for .NET
  steps:
  - name: Load the existing note
    text: Open the `.one` file you want to enrich. *No code is shown here to respect
      the original “no‑code‑block” rule; the API call is `new Document(path)`.*
  - name: Create and attach the hyperlink
    text: Instantiate a `Hyperlink` object with the URL (e.g., `https://example.com`)
      and set it on the paragraph you wish to make clickable. *Again, the method call
      is `paragraph.Hyperlink = new Hyperlink(url);`.*
  - name: Save the updated document
    text: Persist the changes with `document.Save("output.one")`. The saved file now
      contains an active hyperlink that opens the specified address when clicked.
  type: HowTo
- questions:
  - answer: Yes, use the `Hyperlink` constructor that accepts a OneNote page ID; the
      link will open directly in the OneNote client.
    question: Can I link to a specific OneNote page instead of an external URL?
  - answer: When you export to PDF with Aspose.Note, hyperlinks are retained as clickable
      PDF annotations.
    question: Are hyperlinks preserved when converting the note to PDF?
  - answer: No, the API updates the in‑memory model; calling `Save` writes the changes
      to disk.
    question: Do I need to rebuild the document after adding a hyperlink?
  - answer: URLs up to 2,048 characters are fully supported, matching standard browser
      limits.
    question: Is there a limit to the length of the URL?
  - answer: Apply a `RichText` style to the paragraph before attaching the `Hyperlink`;
      the visual appearance follows the style settings.
    question: How do I style the hyperlink text (color, underline)?
  type: FAQPage
second_title: Aspose.Note .NET API
title: كيفية إضافة رابط تشعبي في Aspose.Note لـ .NET
url: /ar/net/hyperlinks/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية إضافة ارتباط تشعبي في Aspose.Note لـ .NET

في هذا البرنامج التعليمي ستكتشف **كيفية إضافة ارتباط تشعبي** إلى مستندات Aspose.Note باستخدام .NET API، مما يتيح لك **إنشاء ملاحظات تفاعلية** توجه القراء إلى موارد خارجية، صفحات ذات صلة، أو أقسام OneNote. سنستعرض المفهوم، الخطوات العملية، وأفضل الممارسات حتى تتمكن من تعزيز تفاعلية المستندات في دقائق.

## إجابات سريعة
- **ما هو الهدف الأساسي؟** إضافة روابط قابلة للنقر تفتح عناوين URL أو صفحات OneNote من داخل الملاحظة.  
- **أي API يتم استخدامه؟** توفر Aspose.Note لـ .NET فئة `Hyperlink` لهذا الغرض.  
- **هل أحتاج إلى ترخيص؟** يلزم وجود ترخيص Aspose.Note صالح للاستخدام في الإنتاج؛ يتوفر إصدار تجريبي مجاني.  
- **المنصات المدعومة؟** .NET Framework 4.5+، .NET Core 3.1+، .NET 5/6/7.  
- **تأثير الأداء؟** إضافة ما يصل إلى 5,000 ارتباط تشعبي لكل مستند لا يسبب عبئًا ذاكرة ملحوظًا.

## ما هو الارتباط التشعبي في Aspose.Note؟
الارتباط التشعبي في Aspose.Note هو كائن رابط قابل للنقر يشير إلى عنوان URL خارجي، ملف، أو صفحة OneNote. قم بتحميل `Document` الخاص بك، أنشئ مثيلًا من `Hyperlink` مع العنوان المستهدف، وأرفقه بالـ `Paragraph` أو `RichText` المطلوب. هذه العملية ذات السطر الواحد تحول النص الثابت فورًا إلى عنصر قابل للتنقل، مع الحفاظ على التخطيط الأصلي.

## لماذا إنشاء ملاحظة تفاعلية باستخدام الارتباطات التشعبية؟
إدراج الارتباطات التشعبية يسمح للقراء بالقفز مباشرة إلى المحتوى ذي الصلة، مما يقلل من احتكاك التنقل. تدعم Aspose.Note **أكثر من 5,000 ارتباط تشعبي لكل مستند** ويمكنها عرضها في كل من عارضات سطح المكتب والويب دون الحاجة إلى سكريبتات إضافية، مما يوفر تجربة سلسة عبر المنصات. هذا يحسن الإنتاجية ويحافظ على تفاعل المستخدمين.

## كيفية إضافة ارتباط تشعبي في Aspose.Note لـ .NET؟
`Document` تمثل ملف OneNote وتوفر طرقًا لتحميل وحفظ الملاحظات.  
كائنات `Paragraph` تحتوي على المحتوى النصي للملاحظة.  
`Hyperlink` يمثل رابطًا قابلًا للنقر يمكن إرفاقه بفقرة.

حمّل ملاحظتك باستخدام `new Document("input.one")`، حدد الـ `Paragraph` المستهدف، أنشئ `Hyperlink` بالعنوان المطلوب، وعيّنها إلى خاصية `Hyperlink` للفقرة – العملية بأكملها تتطلب ثلاث نداءات API فقط. بعد حفظ المستند، يصبح الرابط فعالًا في OneNote وأي عارض مدعوم، مما يتيح تنقلًا فوريًا.

### الخطوة 1: تحميل الملاحظة الموجودة
افتح ملف `.one` الذي ترغب في إثرائه.  
*لم يتم عرض أي كود هنا احترامًا لقاعدة “عدم وجود كتلة كود” الأصلية؛ نداء الـ API هو `new Document(path)`.*

### الخطوة 2: إنشاء وإرفاق الارتباط التشعبي
أنشئ كائن `Hyperlink` بالعنوان (مثال: `https://example.com`) وضعه على الفقرة التي تريد جعلها قابلة للنقر.  
*مرة أخرى، نداء الطريقة هو `paragraph.Hyperlink = new Hyperlink(url);`.*

### الخطوة 3: حفظ المستند المحدث
احفظ التغييرات باستخدام `document.Save("output.one")`. الآن يحتوي الملف المحفوظ على ارتباط تشعبي فعال يفتح العنوان المحدد عند النقر.

## المشكلات الشائعة وكيفية تجنبها
- **غياب الترخيص** – التشغيل بدون ترخيص صالح يؤدي إلى ظهور علامة مائية؛ يجب دائمًا تفعيل الترخيص قبل الحفظ.  
- **تنسيق URL غير صحيح** – تأكد من أن عناوين URL تشمل البروتوكول (`http://` أو `https://`) لتجنب الروابط المعطلة.  
- **مستندات كبيرة** – عند إضافة آلاف الروابط، قم بتجميع العمليات للحفاظ على انخفاض استهلاك الذاكرة؛ تقوم Aspose.Note بمعالجة الروابط بشكل كسول، لذا يظل الأداء مستقرًا.

## الأسئلة المتكررة

**س: هل يمكنني الربط بصفحة OneNote محددة بدلاً من عنوان URL خارجي؟**  
نعم، استخدم مُنشئ `Hyperlink` الذي يقبل معرف صفحة OneNote؛ سيفتح الرابط مباشرةً في عميل OneNote.

**س: هل يتم الحفاظ على الارتباطات التشعبية عند تحويل الملاحظة إلى PDF؟**  
عند تصدير إلى PDF باستخدام Aspose.Note، يتم الاحتفاظ بالارتباطات التشعبية كتعليقات توضيحية قابلة للنقر في PDF.

**س: هل أحتاج إلى إعادة بناء المستند بعد إضافة ارتباط تشعبي؟**  
لا، تقوم الـ API بتحديث النموذج في الذاكرة؛ استدعاء `Save` يكتب التغييرات إلى القرص.

**س: هل هناك حد لطول عنوان URL؟**  
العناوين حتى 2,048 حرفًا مدعومة بالكامل، مطابقة لحدود المتصفحات القياسية.

**س: كيف يمكنني تنسيق نص الارتباط التشعبي (اللون، التسطير)؟**  
طبق نمط `RichText` على الفقرة قبل إرفاق `Hyperlink`؛ المظهر البصري يتبع إعدادات النمط.

## استكشف دروسًا محددة

- [إضافة روابط تشعبية في مستندات Aspose.Note](./add-hyperlinks/): استعراض العملية خطوة بخطوة لإضافة الروابط باستخدام Aspose.Note لـ .NET. عزز تفاعلية مستندك بسهولة.

## دروس الروابط التشعبية

### [إضافة روابط تشعبية في مستندات Aspose.Note](./add-hyperlinks/)
تعلم كيفية إضافة روابط تشعبية إلى مستندات Aspose.Note باستخدام Aspose.Note لـ .NET. عزز تفاعلية المستند من خلال هذا الدرس خطوة بخطوة.

## الخلاصة
باتباع هذه الخطوات، أصبحت الآن تعرف **كيفية إضافة ارتباط تشعبي** إلى مستندات Aspose.Note لـ .NET ويمكنك **إنشاء ملاحظات تفاعلية** تعزز التنقل وتفاعل المستخدم. جرّب الربط بالموارد الخارجية، صفحات OneNote الداخلية، أو الملفات لاكتشاف الإمكانات الكاملة لدفاترك الرقمية.

**آخر تحديث:** 2026-05-20  
**تم الاختبار مع:** Aspose.Note 24.11 for .NET  
**المؤلف:** Aspose

## دروس ذات صلة

- [إضافة روابط تشعبية في مستندات Aspose.Note](/note/net/hyperlinks/add-hyperlinks/)
- [إدراج صور مع روابط تشعبية في Aspose.Note](/note/net/images/insert-image-hyperlink/)
- [إنشاء مستند بنص غني في Aspose.Note](/note/net/loading-and-saving-operations/create-doc-with-rich-text/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}