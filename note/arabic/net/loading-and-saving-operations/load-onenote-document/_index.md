---
title: قم بتحميل مستند OneNote في Aspose.Note
linktitle: قم بتحميل مستند OneNote في Aspose.Note
second_title: Aspose.Note .NET API
description: تعرف على كيفية تحميل مستندات OneNote وتشفيرها وفك تشفيرها برمجيًا في .NET باستخدام Aspose.Note.
type: docs
weight: 16
url: /ar/net/loading-and-saving-operations/load-onenote-document/
---
## مقدمة

Aspose.Note for .NET عبارة عن واجهة برمجة تطبيقات قوية تتيح للمطورين العمل مع ملفات Microsoft OneNote برمجيًا في تطبيقات .NET الخاصة بهم. سواء كنت بحاجة إلى تحميل مستندات OneNote أو معالجتها أو تحويلها، فإن Aspose.Note for .NET يوفر وظائف شاملة لتبسيط سير عملك.

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من أن لديك المتطلبات الأساسية التالية:

1. Visual Studio: قم بتثبيت Visual Studio، وهو بيئة تطوير متكاملة وشاملة (IDE) لتطوير .NET.
2.  Aspose.Note لـ .NET: قم بتنزيل Aspose.Note لـ .NET وتثبيته من[صفحة التحميل](https://releases.aspose.com/note/net/).
3. المعرفة الأساسية لـ C#: يعد الإلمام بأساسيات لغة البرمجة C# ضروريًا لفهم الأمثلة المقدمة في هذا البرنامج التعليمي وتنفيذها.

## استيراد مساحات الأسماء

قبل البدء في العمل مع Aspose.Note لـ .NET، تأكد من استيراد مساحات الأسماء المطلوبة إلى مشروع C# الخاص بك:

```csharp
using System;
using System.IO;
```

دعنا نقسم كل مثال إلى خطوات متعددة:

## قم بتحميل مستند OneNote في Aspose.Note

### الخطوة 1: تحميل دفتر ملاحظات بسيط:
   -  ابدأ بإنشاء مثيل جديد لـ`Notebook` فئة، وتمرير المسار إلى مستند OneNote.
   - قم بالتكرار عبر العقد الفرعية لدفتر الملاحظات باستخدام حلقة foreach.
   - عرض اسم العرض لكل عقدة فرعية.
   - قم بتنفيذ إجراءات محددة بناءً على ما إذا كانت العقدة الفرعية عبارة عن مستند أو دفتر ملاحظات آخر.

```csharp
public static void SimpleLoadNotebook()
{
    // المسار إلى دليل المستندات.
    string dataDir = "Your Document Directory";
    string fileName = "Open Notebook.onetoc2";
    try
    {
        var notebook = new Notebook(Path.Combine(dataDir, fileName));
        foreach (var notebookChildNode in notebook)
        {
            Console.WriteLine(notebookChildNode.DisplayName);
            if (notebookChildNode is Document)
            {
                // افعل شيئًا باستخدام مستند الطفل
            }
            else if (notebookChildNode is Notebook)
            {
                // افعل شيئًا باستخدام دفتر ملاحظات الطفل
            }
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine(ex.Message);
    }
}
```

### الخطوة 2: التحقق مما إذا كان المستند مشفرًا وقم بتحميله:
   -  تحقق مما إذا كان مستند OneNote مشفرًا عن طريق الاتصال بـ`Document.IsEncrypted` طريقة تمرير اسم الملف.
   - إذا لم تكن مشفرة، تابع معالجة المستندات.
   - إذا كانت مشفرة، فاطلب من المستخدم تقديم كلمة مرور لفك التشفير.

```csharp
public static void Document_CheckIfEncryptedAndLoad()
{
    // المسار إلى دليل المستندات.
    string dataDir = "Your Document Directory";
    string fileName = Path.Combine(dataDir, "Aspose.one");

    Document document;
    if (!Document.IsEncrypted(fileName, out document))
    {
        Console.WriteLine("The document is loaded and ready to be processed.");
    }
    else
    {
        Console.WriteLine("The document is encrypted. Provide a password.");
    }
}
```

### الخطوة 3: التحقق مما إذا كان المستند مشفرًا بكلمة مرور ثم قم بتحميله:
   - كما هو الحال في الخطوة السابقة، تحقق مما إذا كان المستند مشفرًا بكلمة مرور محددة.
   - إذا كانت مشفرة وتم توفير كلمة المرور الصحيحة، فتابع معالجة المستند.
   - إذا كانت مشفرة ولكن تم توفير كلمة مرور غير صحيحة، فاطلب من المستخدم معرفة كلمة المرور غير الصالحة.

```csharp
public static void Document_CheckIfEncryptedByPasswordAndLoad()
{
    // المسار إلى دليل المستندات.
    string dataDir = "Your Document Directory";
    string fileName = Path.Combine(dataDir, "Aspose.one");

    Document document;
    if (Document.IsEncrypted(fileName, "VerySecretPassword", out document))
    {
        if (document != null)
        {
            Console.WriteLine("The document is decrypted. It is loaded and ready to be processed.");
        }
        else
        {
            Console.WriteLine("The document is encrypted. Invalid password was provided.");
        }
    }
    else
    {
        Console.WriteLine("The document is NOT encrypted. It is loaded and ready to be processed.");
    }
}
```

### الخطوة 4: التعامل مع تنسيق OneNote 2007 غير المدعوم:
   - حاول تحميل مستند OneNote بتنسيق 2007.
   -  إذا كان التنسيق غير مدعوم، فالتقط ملف`UnsupportedFileFormatException`والتعامل معها بشكل مناسب، وإعلام المستخدم بالتنسيق غير المدعوم.

```csharp
public static void Document_OneNote2007_Is_NotSupported()
{
    // المسار إلى دليل المستندات.
    string dataDir = "Your Document Directory";
    string fileName = Path.Combine(dataDir, "OneNote2007.one");

    try
    {
        new Document(fileName);
    }
    catch (UnsupportedFileFormatException e)
    {
        if (e.FileFormat == FileFormat.OneNote2007)
        {
            Console.WriteLine("It looks like the provided file is in OneNote 2007 format that is not supported.");
        }
        else
            throw;
    }
}
```

## خاتمة

في هذا البرنامج التعليمي، اكتشفنا كيفية تحميل مستندات OneNote في Aspose.Note لـ .NET باستخدام طرق مختلفة. باتباع هذه الإرشادات خطوة بخطوة، يمكنك دمج إمكانات معالجة مستندات OneNote بسلاسة في تطبيقات .NET الخاصة بك.

## الأسئلة الشائعة

### س1: هل يتوافق Aspose.Note for .NET مع كافة إصدارات Microsoft OneNote؟

A1: يدعم Aspose.Note for .NET إصدارات مختلفة من OneNote. ومع ذلك، قد تكون هناك قيود في التنسيقات الأقدم مثل OneNote 2007.

### س٢: هل يمكنني تشفير مستندات OneNote وفك تشفيرها برمجيًا باستخدام Aspose.Note لـ .NET؟

ج2: نعم، يمكنك التحقق من تشفير المستند وفك تشفيره باستخدام Aspose.Note لـ .NET.

### س3: أين يمكنني العثور على المزيد من الموارد والدعم لـ Aspose.Note لـ .NET؟

 ج3: يمكنك زيارة[Aspose.Note لوثائق .NET](https://reference.aspose.com/note/net/) للحصول على أدلة وأمثلة شاملة. بالإضافة إلى ذلك، يمكنك طلب المساعدة من[Aspose.Note لمنتدى .NET](https://forum.aspose.com/c/note/28).

### س4: هل تتوفر نسخة تجريبية مجانية من Aspose.Note لـ .NET؟

 ج4: نعم، يمكنك تنزيل نسخة تجريبية مجانية من[موقع أسبوز](https://releases.aspose.com/).

### س5: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.Note لـ .NET؟

 ج5: يمكنك طلب ترخيص مؤقت من[Aspose صفحة الشراء](https://purchase.aspose.com/temporary-license/).