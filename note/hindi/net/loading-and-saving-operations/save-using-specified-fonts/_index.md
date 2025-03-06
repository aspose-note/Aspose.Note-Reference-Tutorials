---
title: Aspose.Note में निर्दिष्ट फ़ॉन्ट का उपयोग करके सहेजें
linktitle: Aspose.Note में निर्दिष्ट फ़ॉन्ट का उपयोग करके सहेजें
second_title: Aspose.Note .NET API
description: .NET के लिए Aspose.Note में निर्दिष्ट फ़ॉन्ट के साथ दस्तावेज़ों को सहेजना सीखें। लगातार दस्तावेज़ फ़ॉर्मेटिंग के लिए फ़ॉन्ट सेटिंग्स को आसानी से अनुकूलित करें।
weight: 28
url: /hi/net/loading-and-saving-operations/save-using-specified-fonts/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note में निर्दिष्ट फ़ॉन्ट का उपयोग करके सहेजें

## परिचय

इस ट्यूटोरियल में, हम सीखेंगे कि .NET के लिए Aspose.Note में निर्दिष्ट फ़ॉन्ट का उपयोग करके दस्तावेज़ों को कैसे सहेजा जाए। हम इसे प्राप्त करने के लिए चरण दर चरण विभिन्न तरीकों का पता लगाएंगे।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

1.  .NET के लिए Aspose.Note: सुनिश्चित करें कि आपने .NET के लिए Aspose.Note इंस्टॉल कर लिया है। आप इसे यहां से डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/note/net/).

2. विकास परिवेश: आपको .NET विकास के लिए एक विकास परिवेश स्थापित करने की आवश्यकता है।

## नामस्थान आयात करें

सबसे पहले, आइए आवश्यक नामस्थान आयात करें:

```csharp
using System;
using System.IO;

using Aspose.Note.Fonts;
using Aspose.Note.Saving;

```

## चरण 1: डिफ़ॉल्ट फ़ॉन्ट नाम के साथ सहेजा जा रहा है

इस चरण में, हम एक निर्दिष्ट डिफ़ॉल्ट फ़ॉन्ट नाम का उपयोग करके एक दस्तावेज़ सहेजेंगे।

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName()
{
    // दस्तावेज़ निर्देशिका का पथ.
    string dataDir = "Your Document Directory";

    // दस्तावेज़ को Aspose.Note में लोड करें।
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // निर्दिष्ट डिफ़ॉल्ट फ़ॉन्ट के साथ दस्तावेज़ को पीडीएफ के रूप में सहेजें।
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFont("Times New Roman")
                          });
}
```

## चरण 2: फ़ाइल से डिफ़ॉल्ट फ़ॉन्ट के साथ सहेजना

इसके बाद, आइए किसी फ़ाइल से लोड किए गए डिफ़ॉल्ट फ़ॉन्ट का उपयोग करके दस्तावेज़ को सहेजें।

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile()
{
    // दस्तावेज़ निर्देशिका का पथ.
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    // दस्तावेज़ को Aspose.Note में लोड करें।
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // दस्तावेज़ को फ़ाइल से लोड किए गए डिफ़ॉल्ट फ़ॉन्ट के साथ पीडीएफ के रूप में सहेजें।
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromFile(fontFile)
                          });
}
```

## चरण 3: स्ट्रीम से डिफ़ॉल्ट फ़ॉन्ट के साथ सहेजा जा रहा है

अंत में, आइए स्ट्रीम से लोड किए गए डिफ़ॉल्ट फ़ॉन्ट का उपयोग करके दस्तावेज़ को सहेजें।

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream()
{
    // दस्तावेज़ निर्देशिका का पथ.
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    // दस्तावेज़ को Aspose.Note में लोड करें।
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // स्ट्रीम से लोड किए गए डिफ़ॉल्ट फ़ॉन्ट के साथ दस्तावेज़ को पीडीएफ के रूप में सहेजें।
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf";

    using (var stream = File.Open(fontFile, FileMode.Open, FileAccess.Read, FileShare.Read))
    {
        oneFile.Save(dataDir, new PdfSaveOptions()
                              {
                                  FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromStream(stream)
                              });
    }
}
```

## निष्कर्ष

इस ट्यूटोरियल में, हमने पता लगाया कि .NET के लिए Aspose.Note में निर्दिष्ट फ़ॉन्ट का उपयोग करके दस्तावेज़ों को कैसे सहेजा जाए। इन चरणों का पालन करके, आप अपनी आवश्यकताओं के अनुसार फ़ॉन्ट सेटिंग्स को अनुकूलित कर सकते हैं, यह सुनिश्चित करते हुए कि आपके दस्तावेज़ इच्छानुसार प्रारूपित हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं Aspose.Note में दस्तावेज़ों को सहेजने के लिए किसी फ़ॉन्ट का उपयोग कर सकता हूँ?

A1: हाँ, आप दस्तावेज़ों को सहेजने के लिए कोई भी फ़ॉन्ट निर्दिष्ट कर सकते हैं। बस सुनिश्चित करें कि फ़ॉन्ट फ़ाइल पहुंच योग्य है और सही ढंग से लोड की गई है।

### Q2: क्या Aspose.Note विभिन्न दस्तावेज़ प्रारूपों के साथ संगत है?

A2: Aspose.Note मुख्य रूप से OneNote दस्तावेज़ों के साथ काम करता है लेकिन PDF सहित विभिन्न स्वरूपों में सहेजने के विकल्प प्रदान करता है।

### Q3: दस्तावेज़ सहेजते समय मैं गुम फ़ॉन्ट को कैसे संभाल सकता हूँ?

A3: Aspose.Note निर्दिष्ट फ़ॉन्ट गुम होने की स्थिति में डिफ़ॉल्ट फ़ॉन्ट का उपयोग करने के विकल्प प्रदान करता है, जिससे लगातार दस्तावेज़ स्वरूपण सुनिश्चित होता है।

### Q4: क्या Aspose.Note आउटपुट दस्तावेज़ों में फ़ॉन्ट एम्बेडिंग का समर्थन करता है?

A4: हां, Aspose.Note विभिन्न प्लेटफार्मों पर दस्तावेज़ पोर्टेबिलिटी और लगातार रेंडरिंग सुनिश्चित करने के लिए फ़ॉन्ट एम्बेड करने की अनुमति देता है।

### Q5: Aspose.Note के साथ मुझे और सहायता कहां मिल सकती है?

 A5: अधिक सहायता या तकनीकी सहायता के लिए, आप यहां जा सकते हैं[Aspose.नोट फोरम](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
