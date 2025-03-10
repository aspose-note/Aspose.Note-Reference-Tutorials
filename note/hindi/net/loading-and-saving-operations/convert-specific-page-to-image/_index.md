---
title: Aspose.Note में विशिष्ट पृष्ठ को छवि में बदलें
linktitle: Aspose.Note में विशिष्ट पृष्ठ को छवि में बदलें
second_title: Aspose.Note .NET API
description: जानें कि .NET के लिए Aspose.Note का उपयोग करके Microsoft OneNote दस्तावेज़ों के विशिष्ट पृष्ठों को प्रोग्रामेटिक रूप से छवियों में कैसे परिवर्तित किया जाए।
weight: 11
url: /hi/net/loading-and-saving-operations/convert-specific-page-to-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note में विशिष्ट पृष्ठ को छवि में बदलें

## परिचय

.NET के लिए Aspose.Note एक शक्तिशाली एपीआई है जो डेवलपर्स को Microsoft OneNote दस्तावेज़ों के साथ प्रोग्रामेटिक रूप से काम करने में सक्षम बनाता है। चाहे आपको सामग्री निकालने, दस्तावेज़ों को अन्य प्रारूपों में परिवर्तित करने, या OneNote फ़ाइल के भीतर तत्वों में हेरफेर करने की आवश्यकता हो, .NET के लिए Aspose.Note आपके कार्यों को सुव्यवस्थित करने के लिए व्यापक कार्यक्षमता प्रदान करता है। इस ट्यूटोरियल में, हम जानेंगे कि OneNote दस्तावेज़ के विशिष्ट पृष्ठों को छवियों में बदलने के लिए .NET के लिए Aspose.Note का उपयोग कैसे करें। हम पूर्वापेक्षाएँ कवर करेंगे, नामस्थान आयात करेंगे, और रूपांतरण प्रक्रिया को लागू करने पर चरण-दर-चरण मार्गदर्शन प्रदान करेंगे।

## आवश्यक शर्तें

OneNote पृष्ठों को छवियों में बदलने के लिए .NET के लिए Aspose.Note का उपयोग करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

- विजुअल स्टूडियो: सुनिश्चित करें कि आपके सिस्टम पर विजुअल स्टूडियो स्थापित है।
-  .NET के लिए Aspose.Note: .NET के लिए Aspose.Note को डाउनलोड और इंस्टॉल करें[यहाँ](https://releases.aspose.com/note/net/).
- Microsoft OneNote: OneNote दस्तावेज़ बनाने या प्राप्त करने के लिए आपको अपने सिस्टम पर OneNote स्थापित करना होगा।

## नामस्थान आयात करें

अपने C# प्रोजेक्ट में, .NET कक्षाओं और विधियों के लिए Aspose.Note तक पहुँचने के लिए आवश्यक नामस्थान आयात करें।

```csharp
using System;
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
```

## विशिष्ट पृष्ठ को छवि में बदलें

आइए अब .NET के लिए Aspose.Note का उपयोग करके OneNote दस्तावेज़ के एक विशिष्ट पृष्ठ को एक छवि में परिवर्तित करने की प्रक्रिया पर चलते हैं।

### चरण 1: दस्तावेज़ लोड करें

```csharp
string dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

### चरण 2: ImageSaveOptions को आरंभ करें

```csharp
ImageSaveOptions opts = new ImageSaveOptions(SaveFormat.Png)
{
    PageIndex = 1 // कनवर्ट करने के लिए पेज इंडेक्स सेट करें
};
```

### चरण 3: दस्तावेज़ को पीएनजी के रूप में सहेजें

```csharp
dataDir = dataDir + "ConvertSpecificPageToImage_out.png";
oneFile.Save(dataDir, opts);
```

## आउटपुट छवि रिज़ॉल्यूशन सेट करें

दस्तावेज़ को छवि के रूप में सहेजते समय आप आउटपुट छवि रिज़ॉल्यूशन भी सेट कर सकते हैं।

### चरण 1: दस्तावेज़ लोड करें

```csharp
string dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Aspose.one");
```

### चरण 2: आउटपुट छवि रिज़ॉल्यूशन सेट करें

```csharp
dataDir = dataDir + "SetOutputImageResolution_out.jpg";
doc.Save(dataDir, new ImageSaveOptions(SaveFormat.Jpeg) { Resolution = 220 });
```

## निष्कर्ष

.NET के लिए Aspose.Note OneNote दस्तावेज़ों के विशिष्ट पृष्ठों को प्रोग्रामेटिक रूप से छवियों में परिवर्तित करने के कार्य को सरल बनाता है। इस ट्यूटोरियल में बताए गए चरणों का पालन करके, आप इस कार्यक्षमता को अपने .NET अनुप्रयोगों में कुशलतापूर्वक एकीकृत कर सकते हैं, उत्पादकता बढ़ा सकते हैं और OneNote फ़ाइलों के साथ अपनी क्षमताओं का विस्तार कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं .NET के लिए Aspose.Note का उपयोग करके एक साथ कई पेज परिवर्तित कर सकता हूँ?

A1: हाँ, आप पृष्ठों को लूप कर सकते हैं और उन्हें व्यक्तिगत या सामूहिक रूप से परिवर्तित कर सकते हैं।

### Q2: क्या .NET के लिए Aspose.Note PNG और JPEG के अलावा अन्य आउटपुट स्वरूपों का समर्थन करता है?

A2: हाँ, .NET के लिए Aspose.Note छवि रूपांतरण के लिए विभिन्न आउटपुट स्वरूपों का समर्थन करता है।

### Q3: क्या .NET के लिए Aspose.Note का कोई परीक्षण संस्करण उपलब्ध है?

 उ3: हाँ, आप नि:शुल्क परीक्षण प्राप्त कर सकते हैं[यहाँ](https://releases.aspose.com/).

### Q4: क्या मैं JPEG में परिवर्तित करते समय छवि गुणवत्ता को समायोजित कर सकता हूँ?

A4: हाँ, आप अपनी आवश्यकताओं के अनुसार छवि गुणवत्ता निर्धारित कर सकते हैं।

### Q5: मुझे .NET के लिए Aspose.Note के लिए समर्थन कहाँ से मिल सकता है?

 A5: आप .NET समुदाय के लिए Aspose.Note से समर्थन प्राप्त कर सकते हैं[मंच](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
