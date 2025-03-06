---
title: Aspose.Note में पथ द्वारा फ़ाइल संलग्न करें
linktitle: Aspose.Note में पथ द्वारा फ़ाइल संलग्न करें
second_title: Aspose.Note .NET API
description: जानें कि .NET के लिए Aspose.Note का उपयोग करके प्रोग्रामेटिक रूप से Microsoft OneNote दस्तावेज़ों में फ़ाइलें कैसे संलग्न करें। इस व्यापक ट्यूटोरियल के साथ अपनी विकास प्रक्रिया को सरल बनाएं।
weight: 11
url: /hi/net/attachments/attach-file-by-path/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note में पथ द्वारा फ़ाइल संलग्न करें

## परिचय

.NET के लिए Aspose.Note एक शक्तिशाली लाइब्रेरी है जो डेवलपर्स को Microsoft OneNote फ़ाइलों के साथ प्रोग्रामेटिक रूप से काम करने में सक्षम बनाती है। चाहे आप OneNote दस्तावेज़ बनाना, संपादित करना, परिवर्तित करना या उनमें हेरफेर करना चाहते हों, .NET के लिए Aspose.Note आपकी विकास प्रक्रिया को सुव्यवस्थित करने के लिए व्यापक कार्यक्षमता प्रदान करता है।

## आवश्यक शर्तें

.NET के लिए Aspose.Note का उपयोग करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ हैं:

1. विकास वातावरण: आपको .NET फ्रेमवर्क स्थापित एक कंप्यूटर और विजुअल स्टूडियो जैसे उपयुक्त विकास वातावरण की आवश्यकता है।

2.  .NET के लिए Aspose.Note: .NET के लिए Aspose.Note को डाउनलोड और इंस्टॉल करें[लिंक को डाउनलोड करें](https://releases.aspose.com/note/net/).

3. C# का ज्ञान: C# प्रोग्रामिंग भाषा से खुद को परिचित करें क्योंकि .NET के लिए Aspose.Note का उपयोग मुख्य रूप से C# के साथ किया जाता है।

4. OneNote की बुनियादी समझ: हालांकि अनिवार्य नहीं है, OneNote संरचना और अवधारणाओं की बुनियादी समझ होना फायदेमंद होगा।

## नामस्थान आयात करें

अपने प्रोजेक्ट में .NET के लिए Aspose.Note का उपयोग करने के लिए, आपको आवश्यक नेमस्पेस आयात करने की आवश्यकता है। यहां बताया गया है कि आप यह कैसे कर सकते हैं:

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using System.Drawing;
```

## Aspose.Note में पथ द्वारा फ़ाइल संलग्न करें

.NET के लिए Aspose.Note का उपयोग करके OneNote दस्तावेज़ में फ़ाइलें संलग्न करना एक सीधी प्रक्रिया है। आइए इसे कई चरणों में विभाजित करें:

### चरण 1: दस्तावेज़ ऑब्जेक्ट को आरंभ करें

```csharp
// दस्तावेज़ निर्देशिका का पथ.
string dataDir = RunExamples.GetDataDir_Attachments();
Document doc = new Document();
```

 यह का एक नया उदाहरण प्रारंभ करता है`Document` वर्ग, जो OneNote दस्तावेज़ का प्रतिनिधित्व करता है।

### चरण 2: पेज ऑब्जेक्ट को आरंभ करें

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

 यहां, हम इसका एक नया उदाहरण बनाते हैं`Page` वर्ग, जो दस्तावेज़ के भीतर एक पृष्ठ का प्रतिनिधित्व करता है।

### चरण 3: आउटलाइन ऑब्जेक्ट को आरंभ करें

```csharp
Outline outline = new Outline(doc);
```

 एक`Outline` ऑब्जेक्ट पृष्ठ के भीतर सामग्री को व्यवस्थित करने के लिए बनाया गया है।

### चरण 4: आउटलाइनएलिमेंट ऑब्जेक्ट को आरंभ करें

```csharp
OutlineElement outlineElem = new OutlineElement(doc);
```

`OutlineElement` रूपरेखा संरचना के भीतर एक तत्व का प्रतिनिधित्व करता है।

### चरण 5: अटैच्डफ़ाइल ऑब्जेक्ट को आरंभ करें

```csharp
AttachedFile attachedFile = new AttachedFile(doc,  dataDir + "attachment.txt");
```

 यहां, हम इसका एक उदाहरण बनाते हैं`AttachedFile`, उस फ़ाइल का पथ निर्दिष्ट करना जिसे हम संलग्न करना चाहते हैं।

### चरण 6: संलग्न फ़ाइल संलग्न करें

```csharp
outlineElem.AppendChildLast(attachedFile);
```

संलग्न फ़ाइल रूपरेखा तत्व से जुड़ी हुई है।

### चरण 7: रूपरेखा तत्व जोड़ें

```csharp
outline.AppendChildLast(outlineElem);
```

रूपरेखा तत्व को रूपरेखा से जोड़ा गया है।

### चरण 8: रूपरेखा जोड़ें

```csharp
page.AppendChildLast(outline);
```

रूपरेखा पृष्ठ पर संलग्न है।

### चरण 9: पृष्ठ जोड़ें

```csharp
doc.AppendChildLast(page);
```

अंत में, पृष्ठ को दस्तावेज़ में जोड़ दिया जाता है।

### चरण 10: दस्तावेज़ सहेजें

```csharp
dataDir = dataDir + "AttachFileByPath_out.one";
doc.Save(dataDir);
```

दस्तावेज़ सहेजा गया है, और फ़ाइल सफलतापूर्वक संलग्न की गई है।

## निष्कर्ष

.NET के लिए Aspose.Note, OneNote दस्तावेज़ों के साथ प्रोग्रामेटिक रूप से काम करने की प्रक्रिया को सरल बनाता है। ऊपर बताए गए चरणों का पालन करके, आप .NET के लिए Aspose.Note का उपयोग करके अपने OneNote दस्तावेज़ों में फ़ाइलें आसानी से संलग्न कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या .NET के लिए Aspose.Note OneNote के सभी संस्करणों के साथ संगत है?

A1: .NET के लिए Aspose.Note OneNote के विभिन्न संस्करणों का समर्थन करता है, जिसमें OneNote 2010, 2013, 2016 और Windows 10 के लिए नवीनतम OneNote शामिल है।

### Q2: क्या मैं .NET के लिए Aspose.Note का उपयोग करके मौजूदा OneNote फ़ाइलों में हेरफेर कर सकता हूँ?

उ2: हां, आप .NET के लिए Aspose.Note का उपयोग करके मौजूदा OneNote फ़ाइलों को प्रोग्रामेटिक रूप से संपादित, संशोधित और हेरफेर कर सकते हैं।

### Q3: क्या .NET के लिए Aspose.Note को व्यावसायिक उपयोग के लिए लाइसेंस की आवश्यकता है?

उ3: हां, आपको .NET के लिए Aspose.Note के व्यावसायिक उपयोग के लिए लाइसेंस प्राप्त करने की आवश्यकता है। आप से लाइसेंस प्राप्त कर सकते हैं[खरीद पृष्ठ](https://purchase.aspose.com/buy).

### Q4: क्या .NET के लिए Aspose.Note का निःशुल्क परीक्षण उपलब्ध है?

 A4: हाँ, आप .NET के लिए Aspose.Note के निःशुल्क परीक्षण का लाभ उठा सकते हैं[परीक्षण पृष्ठ](https://releases.aspose.com/).

### Q5: मैं .NET के लिए Aspose.Note के लिए समर्थन कहाँ से प्राप्त कर सकता हूँ?

 A5: आप Aspose.Note सामुदायिक मंचों से समर्थन प्राप्त कर सकते हैं[यहाँ](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
