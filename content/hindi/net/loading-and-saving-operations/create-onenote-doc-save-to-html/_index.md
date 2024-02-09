---
title: OneNote दस्तावेज़ बनाएं और Aspose.Note में HTML में सहेजें
linktitle: OneNote दस्तावेज़ बनाएं और Aspose.Note में HTML में सहेजें
second_title: Aspose.Note .NET API
description: Aspose.Note API का उपयोग करके .NET अनुप्रयोगों में Microsoft OneNote दस्तावेज़ों को HTML प्रारूप में बनाने और सहेजने का तरीका जानें। चरण-दर-चरण उदाहरणों के साथ हमारे व्यापक ट्यूटोरियल का अनुसरण करें।
type: docs
weight: 14
url: /hi/net/loading-and-saving-operations/create-onenote-doc-save-to-html/
---
## परिचय

.NET के लिए Aspose.Note एक शक्तिशाली API है जो डेवलपर्स को उनके .NET अनुप्रयोगों में Microsoft OneNote दस्तावेज़ों के साथ प्रोग्रामेटिक रूप से काम करने की अनुमति देता है। Aspose.Note के साथ, आप OneNote फ़ाइलों को आसानी से बना सकते हैं, हेरफेर कर सकते हैं और परिवर्तित कर सकते हैं। इस ट्यूटोरियल में, हम जानेंगे कि OneNote दस्तावेज़ कैसे बनाएं और .NET API के लिए Aspose.Note द्वारा प्रदान किए गए विभिन्न विकल्पों का उपयोग करके इसे HTML प्रारूप में कैसे सहेजें।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यकताएँ हैं:

- C# प्रोग्रामिंग भाषा का बुनियादी ज्ञान।
- आपके सिस्टम पर विज़ुअल स्टूडियो स्थापित है।
-  आपके प्रोजेक्ट में स्थापित .NET API के लिए Aspose.Note। आप इसे यहां से डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/note/net/).
- Microsoft OneNote दस्तावेज़ों की संरचना से परिचित होना।

## नामस्थान आयात करें

इससे पहले कि हम कोडिंग भाग में उतरें, आइए आवश्यक नामस्थान आयात करें:

```csharp
using System;
using System.Drawing;
using System.Globalization;
using System.IO;

using Aspose.Note.Saving;
using Aspose.Note.Saving.Html;

```

अब, आइए प्रत्येक उदाहरण को कई चरणों में विभाजित करें और देखें कि OneNote दस्तावेज़ कैसे बनाएं और इसे .NET के लिए Aspose.Note का उपयोग करके HTML प्रारूप में कैसे सहेजें।

## चरण 1: डिफ़ॉल्ट विकल्पों के साथ एक OneNote दस्तावेज़ बनाएँ

```csharp
public static void CreateAndSaveToHTMLUsingDefaultOptions()
{
    // OneNote दस्तावेज़ प्रारंभ करें
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    // दस्तावेज़ में सभी टेक्स्ट के लिए डिफ़ॉल्ट शैली.
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    // HTML प्रारूप में सहेजें
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateOneNoteDocAndSaveToHTML_out.html");
    doc.Save(outputPath);

    Console.WriteLine("\nOneNote document created successfully.\nFile saved at " + outputPath);
}
```

इस चरण में, हम एक नया OneNote दस्तावेज़ प्रारंभ करते हैं, शीर्षक के साथ एक पृष्ठ जोड़ते हैं, और डिफ़ॉल्ट विकल्पों का उपयोग करके इसे HTML प्रारूप में सहेजते हैं।

## चरण 2: HTML में एक विशिष्ट पेज रेंज बनाएं और सहेजें

```csharp
public static void CreateAndSavePageRange()
{
    // OneNote दस्तावेज़ प्रारंभ करें
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    // दस्तावेज़ में सभी टेक्स्ट के लिए डिफ़ॉल्ट शैली.
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    // HTML प्रारूप में सहेजें
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateAndSavePageRange_out.html");
    doc.Save(outputPath, new HtmlSaveOptions { PageCount = 1, PageIndex = 0 });

    Console.WriteLine("\nOneNote document created successfully and saved as page range.\nFile saved at " + outputPath);
}
```

यहां, हम प्रदर्शित करते हैं कि दस्तावेज़ कैसे बनाएं और एक विशिष्ट पृष्ठ श्रेणी को HTML प्रारूप में कैसे सहेजें।

## चरण 3: एम्बेडेड संसाधनों के साथ मेमोरी स्ट्रीम में HTML के रूप में सहेजें

```csharp
public static void SaveAsHTMLToMemoryStreamWithEmbeddedResources()
{
    // OneNote दस्तावेज़ लोड करें
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // HTML बचत विकल्प निर्दिष्ट करें
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportEmbedded,
        ExportFonts = ResourceExportType.ExportEmbedded,
        ExportImages = ResourceExportType.ExportEmbedded,
        FontFaceTypes = FontFaceType.Ttf
    };

    // दस्तावेज़ को मेमोरी स्ट्रीम में सहेजें
    var memoryStream = new MemoryStream();
    document.Save(memoryStream, options);
}
```

यह चरण दिखाता है कि OneNote दस्तावेज़ को एम्बेडेड संसाधनों (CSS, फ़ॉन्ट और छवियों) के साथ HTML प्रारूप में मेमोरी स्ट्रीम में कैसे सहेजा जाए।

## चरण 4: अलग-अलग फ़ाइलों में संसाधनों के साथ फ़ाइल को HTML के रूप में सहेजें

```csharp
public static void SaveAsHTMLToFileWithResourcesInSeparateFiles()
{
    // OneNote दस्तावेज़ लोड करें
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // HTML बचत विकल्प निर्दिष्ट करें
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportAsStream,
        ExportFonts = ResourceExportType.ExportAsStream,
        ExportImages = ResourceExportType.ExportAsStream,
        FontFaceTypes = FontFaceType.Ttf
    };

    //दस्तावेज़ को अलग-अलग फ़ाइलों में संग्रहीत संसाधनों के साथ HTML फ़ाइल में सहेजें
    document.Save(Path.Combine(dataDir, "document_out.html"), options);
}
```

इस चरण में, हम एक OneNote दस्तावेज़ को अलग-अलग फ़ाइलों में संग्रहीत सभी संसाधनों (CSS, फ़ॉन्ट और छवियों) के साथ HTML प्रारूप में सहेजते हैं।

## चरण 5: संसाधनों को बचाने के लिए कॉलबैक के साथ मेमोरी स्ट्रीम में HTML के रूप में सहेजें

```csharp
public static void SaveAsHTMLToMemoryStreamWithCallBacksToSaveResources()
{
    // सेविंग कॉलबैक कॉन्फ़िगरेशन निर्दिष्ट करें
    var savingCallbacks = new UserSavingCallbacks()
    {
        RootFolder = "documentFolder",
        CssFolder = "css",
        KeepCssStreamOpened = true,
        ImagesFolder = "images",
        FontsFolder = "fonts"
    };

    // HTML बचत विकल्प निर्दिष्ट करें
    var options = new HtmlSaveOptions
    {
        FontFaceTypes = FontFaceType.Ttf,
        CssSavingCallback = savingCallbacks,
        FontSavingCallback = savingCallbacks,
        ImageSavingCallback = savingCallbacks
    };

    // OneNote दस्तावेज़ लोड करें
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // उपयोगकर्ता-परिभाषित कॉलबैक द्वारा प्रबंधित संसाधनों के साथ दस्तावेज़ को HTML प्रारूप में सहेजें
    using (var stream = File.Create(Path.Combine(savingCallbacks.RootFolder, "document.html")))
    {
        document.Save(stream, options);
    }

    // सीएसएस स्ट्रीम में डेटा को मैन्युअल रूप से जोड़ें
    using (var writer = new StreamWriter(savingCallbacks.CssStream))
    {
        writer.WriteLine();
        writer.WriteLine("/* This line is appended to stream manually by user */");
    }
}
```

यहां, हम प्रदर्शित करते हैं कि उपयोगकर्ता-परिभाषित कॉलबैक द्वारा प्रबंधित संसाधनों के साथ OneNote दस्तावेज़ को HTML प्रारूप में कैसे सहेजा जाए।

## निष्कर्ष

इस लेख में, हमने पता लगाया है कि OneNote दस्तावेज़ों के साथ कैसे काम करें और उन्हें .NET के लिए Aspose.Note का उपयोग करके HTML प्रारूप में सहेजें। चरण-दर-चरण मार्गदर्शिका का पालन करके, आप आसानी से कर सकते हैं

 इस कार्यक्षमता को अपने .NET अनुप्रयोगों में एकीकृत करें, जिससे आप OneNote फ़ाइलों में कुशलतापूर्वक हेरफेर कर सकेंगे।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं सहेजी गई HTML फ़ाइल के स्वरूप को अनुकूलित कर सकता हूँ?

A1: हां, आप रूपांतरण प्रक्रिया के दौरान उत्पन्न सीएसएस स्टाइलशीट को संशोधित करके उपस्थिति को अनुकूलित कर सकते हैं।

### Q2: क्या Aspose.Note HTML के अलावा अन्य प्रारूपों में रूपांतरण का समर्थन करता है?

A2: हां, Aspose.Note पीडीएफ, छवियों और माइक्रोसॉफ्ट वर्ड दस्तावेजों जैसे विभिन्न प्रारूपों में रूपांतरण का समर्थन करता है।

### Q3: क्या Aspose.Note .NET कोर अनुप्रयोगों के साथ संगत है?

A3: हाँ, Aspose.Note .NET Framework और .NET Core अनुप्रयोगों दोनों के साथ संगत है।

### Q4: क्या मैं Aspose.Note का उपयोग करके OneNote दस्तावेज़ों से पाठ और छवियाँ निकाल सकता हूँ?

A4: हाँ, आप Aspose.Note API का उपयोग करके टेक्स्ट और छवियों को निकालने के साथ-साथ विभिन्न अन्य जोड़-तोड़ भी कर सकते हैं।

### Q5: क्या Aspose.Note सुविधाओं के परीक्षण के लिए कोई परीक्षण संस्करण उपलब्ध है?

 A5: हां, आप यहां से निःशुल्क परीक्षण संस्करण डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/).