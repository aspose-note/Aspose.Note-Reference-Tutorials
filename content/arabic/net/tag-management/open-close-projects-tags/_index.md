---
title: فتح وإغلاق المشاريع باستخدام العلامات في Aspose.Note
linktitle: فتح وإغلاق المشاريع باستخدام العلامات في Aspose.Note
second_title: Aspose.Note .NET API
description: تعرف على كيفية التعامل مع ملفات Microsoft OneNote برمجياً باستخدام Aspose.Note لـ .NET. فتح وإغلاق المشاريع باستخدام العلامات بكفاءة.
type: docs
weight: 15
url: /ar/net/tag-management/open-close-projects-tags/
---
## مقدمة

في هذا البرنامج التعليمي، سوف نتعلم كيفية استخدام Aspose.Note لـ .NET لفتح وإغلاق المشاريع ذات العلامات. Aspose.Note عبارة عن واجهة برمجة تطبيقات قوية تتيح للمطورين العمل مع ملفات Microsoft OneNote برمجيًا، مما يتيح مهام مثل معالجة النصوص والصور والعلامات داخل المستندات.

## المتطلبات الأساسية

قبل أن نبدأ، تأكد من إعداد المتطلبات الأساسية التالية:

## استيراد مساحات الأسماء

```csharp
using System.IO;
using System.Linq;
```

الآن دعونا نقسم كل مثال إلى خطوات متعددة:

## الخطوة 1: قم بتحميل المستند

أولاً، نحتاج إلى تحميل المستند إلى Aspose.Note.

```csharp
string dataDir = "Your Document Directory";
var oneFile = new Document(Path.Combine(dataDir, "ProjectNotes.one"));
```

## الخطوة 2: أغلق عناصر المشروع C

الآن، دعونا نغلق جميع عناصر مربع الاختيار المتعلقة بـ "المشروع C".

```csharp
foreach (var node in oneFile.GetChildNodes<ITaggable>())
{
    foreach (var checkBox in node.Tags.OfType<CheckBox>())
    {
        if (checkBox.Label.Contains("Project C") && !checkBox.Checked)
        {
            checkBox.SetCompleted();
        }
    }
}
```

## الخطوة 3: احفظ ملاحظات المشروع المغلق C

احفظ المستند المعدل بعناصر "المشروع C" المغلقة.

```csharp
oneFile.Save("Path to save the closed Project C notes");
```

## الخطوة 4: افتح عناصر المشروع C

بعد ذلك، دعونا نفتح جميع عناصر مربع الاختيار المتعلقة بـ "المشروع C".

```csharp
var oneFile = new Document("Path to the closed Project C notes");

foreach (var node in oneFile.GetChildNodes<ITaggable>())
{
    foreach (var checkBox in node.Tags.OfType<CheckBox>())
    {
        if (checkBox.Label.Contains("Project C") && checkBox.Checked)
        {
            checkBox.SetOpen();
        }
    }
}
```

## الخطوة 5: احفظ ملاحظات المشروع المفتوح

احفظ المستند المعدل مع عناصر "المشروع C" المفتوحة.

```csharp
oneFile.Save(Path.Combine(dataDir, "ProjectNoteWithOpenProjectC.one"));
```

لقد تعلمت الآن كيفية فتح وإغلاق المشاريع ذات العلامات في Aspose.Note باستخدام .NET.

## خاتمة

يوفر Aspose.Note for .NET طريقة مناسبة لمعالجة مستندات OneNote برمجيًا. باتباع هذا البرنامج التعليمي، يمكنك إدارة مشاريعك بكفاءة عن طريق فتح العناصر وإغلاقها باستخدام العلامات.

## الأسئلة الشائعة

### س1: هل Aspose.Note متوافق مع كافة إصدارات OneNote؟

ج1: يدعم Aspose.Note Microsoft OneNote 2010 والإصدارات الأحدث.

### س2: هل يمكنني استخدام Aspose.Note للمشاريع التجارية؟

 ج2: نعم، يمكنك استخدام Aspose.Note لكل من المشاريع الشخصية والتجارية. يزور[هنا](https://purchase.aspose.com/buy) لشراء ترخيص.

### س3: هل يقدم Aspose.Note نسخة تجريبية مجانية؟

ج3: نعم، يمكنك الحصول على نسخة تجريبية مجانية[هنا](https://releases.aspose.com/).

### س4: أين يمكنني العثور على وثائق Aspose.Note؟

 ج4: يمكنك العثور على الوثائق[هنا](https://reference.aspose.com/note/net/).

### س5: أين يمكنني الحصول على الدعم لـ Aspose.Note؟

ج5: للحصول على الدعم، يمكنك زيارة Aspose.Note[المنتدى](https://forum.aspose.com/c/note/28).