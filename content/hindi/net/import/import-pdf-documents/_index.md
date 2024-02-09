---
title: Aspose.Note में PDF दस्तावेज़ आयात करें
linktitle: Aspose.Note में PDF दस्तावेज़ आयात करें
second_title: Aspose.Note .NET API
description: सहज एकीकरण के लिए विभिन्न मर्ज विकल्पों का उपयोग करके आसानी से .NET के लिए Aspose.Note में PDF दस्तावेज़ आयात करना सीखें।
type: docs
weight: 10
url: /hi/net/import/import-pdf-documents/
---
## परिचय

आज बड़ी मात्रा में उपलब्ध डिजिटल सामग्री के साथ, पीडीएफ दस्तावेज़ों को अपनी परियोजनाओं में सहजता से एकीकृत करना महत्वपूर्ण है। .NET के लिए Aspose.Note पीडीएफ दस्तावेजों को कुशलतापूर्वक आयात करने के लिए शक्तिशाली कार्यक्षमता प्रदान करता है। इस ट्यूटोरियल में, हम जानेंगे कि .NET के लिए Aspose.Note का उपयोग करके चरण दर चरण पीडीएफ दस्तावेज़ कैसे आयात करें।

## आवश्यक शर्तें

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

1.  .NET के लिए Aspose.Note: यहां से लाइब्रेरी डाउनलोड और इंस्टॉल करें[यहाँ](https://releases.aspose.com/note/net/).
2. C# और .NET फ्रेमवर्क का बुनियादी ज्ञान: C# प्रोग्रामिंग भाषा और .NET फ्रेमवर्क की समझ फायदेमंद होगी।

## नामस्थान आयात करें

पीडीएफ आयात कार्यक्षमता के लिए आवश्यक कक्षाओं और विधियों तक पहुंचने के लिए आवश्यक नामस्थान आयात करना सुनिश्चित करें:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;

using Aspose.Note.Importing;

```

## चरण 1: सिंपल मर्ज का उपयोग करके पीडीएफ दस्तावेज़ आयात करें

सिंपल मर्ज दृष्टिकोण कई पीडीएफ दस्तावेज़ों से सभी पेजों को पेज दर पेज आयात करने की अनुमति देता है:

```csharp
public static void ImportSetOfFiles_SimpleMerge()
{
    string dataDir = "Your Document Directory";

    var d = new Document();

    d.Import(Path.Combine(dataDir, "sampleText.pdf"))
     .Import(Path.Combine(dataDir, "sampleImage.pdf"))
     .Import(Path.Combine(dataDir, "sampleTable.pdf"));

    d.Save(Path.Combine(dataDir, "sample_SimpleMerge.one"));

    Console.WriteLine("\nThe PDF documents are imported successfully.");
}
```

## चरण 2: स्ट्रक्चर्ड मर्ज का उपयोग करके पीडीएफ दस्तावेज़ आयात करें

संरचित मर्ज पीडीएफ दस्तावेज़ों से सभी पृष्ठों को आयात करता है जबकि प्रत्येक दस्तावेज़ से पृष्ठों को शीर्ष-स्तरीय OneNote पृष्ठ के बच्चों के रूप में सम्मिलित करता है:

```csharp
public static void ImportSetOfFiles_StructuredMerge()
{
    string dataDir = "Your Document Directory";

    var d = new Document();

    foreach (var file in new[] { "sampleText.pdf", "sampleImage.pdf", "sampleTable.pdf" })
    {
        d.AppendChildLast(new Page()).Title = new Title() { TitleText = new RichText() { ParagraphStyle = ParagraphStyle.Default }.Append(file) };
        d.Import(Path.Combine(dataDir, file), new PdfImportOptions(), new MergeOptions() { InsertAt = int.MaxValue, InsertAsChild = true });
    }

    d.Save(Path.Combine(dataDir, "sample_StructuredMerge.one"));

    Console.WriteLine("\nThe PDF documents are imported successfully.");
}
```

## चरण 3: सिंगल पेज मर्ज का उपयोग करके पीडीएफ दस्तावेज़ आयात करें

सिंगल पेज मर्ज कई पीडीएफ दस्तावेज़ों की सामग्री को एक OneNote पेज पर मर्ज करता है:

```csharp
public static void ImportSetOfFiles_SinglePageMerge()
{
    string dataDir = "Your Document Directory";

    var d = new Document();

    var importOptions = new PdfImportOptions();
    var mergeOptions = new MergeOptions() { ImportAsSinglePage = true, PageSpacing = 100 };

    d.Import(Path.Combine(dataDir, "sampleText.pdf"), importOptions, mergeOptions)
     .Import(Path.Combine(dataDir, "sampleImage.pdf"), importOptions, mergeOptions)
     .Import(Path.Combine(dataDir, "sampleTable.pdf"), importOptions, mergeOptions);

    d.Save(Path.Combine(dataDir, "sample_SinglePageMerge.one"));

    Console.WriteLine("\nThe PDF documents are imported successfully.");
}
```

## चरण 4: कस्टम मर्ज का उपयोग करके पीडीएफ दस्तावेज़ आयात करें

कस्टम मर्ज कस्टम मानदंडों के आधार पर PDF दस्तावेज़ों के पृष्ठों को एकल OneNote पृष्ठों में समूहित करने की अनुमति देता है:

```csharp
public static void ImportSetOfFiles_CustomMerge()
{
    string dataDir = "Your Document Directory";

    var d = new Document();

    var mergeOptions = new MergeOptions() { ImportAsSinglePage = true, PageSpacing = 100 };

    IEnumerable<Page> pages = PdfImporter.Import(Path.Combine(dataDir, "SampleGrouping.pdf"));
    while (pages.Any())
    {
        d.Merge(pages.Take(5), mergeOptions);
        pages = pages.Skip(5);
    }

    d.Save(Path.Combine(dataDir, "sample_CustomMerge.one"));

    Console.WriteLine("\nThe PDF documents are imported successfully.");
}
```

## निष्कर्ष

Aspose.Note के साथ अपने .NET अनुप्रयोगों में PDF दस्तावेज़ों को एकीकृत करना एक सीधी प्रक्रिया है, जो आपके प्रोजेक्ट की आवश्यकताओं के अनुरूप विभिन्न मर्ज विकल्प प्रदान करती है। चाहे आपको कई पृष्ठों को आयात करने या सामग्री को पदानुक्रम से व्यवस्थित करने की आवश्यकता हो, Aspose.Note निर्बाध एकीकरण के लिए आवश्यक उपकरण प्रदान करता है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं एन्क्रिप्टेड पीडीएफ दस्तावेज़ आयात कर सकता हूँ?

A1: हां, Aspose.Note एन्क्रिप्टेड पीडीएफ दस्तावेजों को आयात करने का समर्थन करता है। सुनिश्चित करें कि आप आवश्यक डिक्रिप्शन क्रेडेंशियल प्रदान करें।

### Q2: क्या आयात के लिए पीडीएफ फ़ाइल आकार पर कोई सीमाएँ हैं?

A2: Aspose.Note में आयात के लिए पीडीएफ फ़ाइल आकार पर कोई अंतर्निहित सीमा नहीं है। हालाँकि, बड़ी पीडीएफ फाइलों के लिए सिस्टम संसाधनों और प्रदर्शन निहितार्थों पर विचार करें।

### Q3: क्या मैं आयातित पीडीएफ सामग्री के स्वरूप को अनुकूलित कर सकता हूँ?

A3: हां, आप Aspose.Note द्वारा प्रदान किए गए विभिन्न विकल्पों, जैसे फ़ॉन्ट शैली, रंग और लेआउट समायोजन का उपयोग करके आयातित पीडीएफ सामग्री की उपस्थिति को अनुकूलित कर सकते हैं।

### Q4: क्या Aspose.Note .NET कोर के साथ संगत है?

A4: हाँ, Aspose.Note .NET कोर के साथ संगत है, जो आपको क्रॉस-प्लेटफ़ॉर्म अनुप्रयोगों में पीडीएफ आयात कार्यक्षमता को एकीकृत करने की अनुमति देता है।

### Q5: मुझे अतिरिक्त सहायता या संसाधन कहां मिल सकते हैं?

 A5: अतिरिक्त सहायता, दस्तावेज़ीकरण, या सामुदायिक सहायता के लिए, पर जाएँ[Aspose.नोट फोरम](https://forum.aspose.com/c/note/28).