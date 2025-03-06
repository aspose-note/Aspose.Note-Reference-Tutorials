---
title: Aspose.Note का उपयोग करके रूट और उप-पृष्ठों के साथ दस्तावेज़ बनाएं
linktitle: Aspose.Note का उपयोग करके रूट और उप-पृष्ठों के साथ दस्तावेज़ बनाएं
second_title: Aspose.Note .NET API
description: पदानुक्रमित संरचनाओं के साथ गतिशील OneNote दस्तावेज़ बनाने के लिए .NET के लिए Aspose.Note का उपयोग करना सीखें।
weight: 11
url: /hi/net/note-manipulation/create-documents-root-sub-pages/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note का उपयोग करके रूट और उप-पृष्ठों के साथ दस्तावेज़ बनाएं

## परिचय

.NET के लिए Aspose.Note का उपयोग करके रूट और उप-पृष्ठों के साथ दस्तावेज़ बनाने पर हमारे ट्यूटोरियल में आपका स्वागत है! Aspose.Note एक शक्तिशाली लाइब्रेरी है जो डेवलपर्स को Microsoft OneNote फ़ाइलों के साथ प्रोग्रामेटिक रूप से काम करने में सक्षम बनाती है, जिससे OneNote दस्तावेज़ों के निर्माण, हेरफेर और रूपांतरण की अनुमति मिलती है।

इस ट्यूटोरियल में, हम आपको चरण दर चरण रूट और उप-पृष्ठों के साथ OneNote दस्तावेज़ बनाने की प्रक्रिया के बारे में बताएंगे। हम .NET के लिए Aspose.Note का उपयोग करके विस्तृत स्पष्टीकरण और कोड स्निपेट प्रदान करेंगे, जिससे आपके लिए इसे अपनाना और अपनी परियोजनाओं में लागू करना आसान हो जाएगा।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित शर्तें हैं:

1. विजुअल स्टूडियो: .NET कोड लिखने और संकलित करने के लिए आपको अपने सिस्टम पर विजुअल स्टूडियो स्थापित करना होगा।
2.  .NET के लिए Aspose.Note: .NET के लिए Aspose.Note को डाउनलोड और इंस्टॉल करें[डाउनलोड पेज](https://releases.aspose.com/note/net/).
3. बुनियादी सी# ज्ञान: कोड उदाहरणों को समझने और लागू करने के लिए सी# प्रोग्रामिंग भाषा से परिचित होना आवश्यक है।

अब जब आपने सब कुछ सेट कर लिया है, तो आइए ट्यूटोरियल पर ध्यान दें!

## नामस्थान आयात करें

सबसे पहले, आइए अपने प्रोजेक्ट में आवश्यक नामस्थान आयात करें:

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using System.Drawing;
```

## चरण 1: दस्तावेज़ ऑब्जेक्ट को आरंभ करें

```csharp
//दस्तावेज़ वर्ग का एक ऑब्जेक्ट बनाएं
Document doc = new Document();
```

## चरण 2: रूट पेज और सब-पेज बनाएं

```csharp
// पेज क्लास ऑब्जेक्ट को आरंभ करें और उनके स्तर निर्धारित करें
Page page1 = new Page(doc) { Level = 1 };
Page page2 = new Page(doc) { Level = 2 };
Page page3 = new Page(doc) { Level = 1 };
```

### पेज 1 के लिए:

```csharp
Outline outline1 = new Outline(doc);
OutlineElement outlineElem1 = new OutlineElement(doc);
ParagraphStyle textStyle1 = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text1 = new RichText(doc) { Text = "First page.", ParagraphStyle = textStyle1 };
outlineElem1.AppendChildLast(text1);
outline1.AppendChildLast(outlineElem1);
page1.AppendChildLast(outline1);
```

### पेज 2 के लिए:

```csharp
Outline outline2 = new Outline(doc);
OutlineElement outlineElem2 = new OutlineElement(doc);
ParagraphStyle textStyle2 = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text2 = new RichText(doc) { Text = "Second page.", ParagraphStyle = textStyle2 };
outlineElem2.AppendChildLast(text2);
outline2.AppendChildLast(outlineElem2);
page2.AppendChildLast(outline2);
```

### पेज 3 के लिए:

```csharp
Outline outline3 = new Outline(doc);
OutlineElement outlineElem3 = new OutlineElement(doc);
ParagraphStyle textStyle3 = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text3 = new RichText(doc) { Text = "Third page.", ParagraphStyle = textStyle3 };
outlineElem3.AppendChildLast(text3);
outline3.AppendChildLast(outlineElem3);
page3.AppendChildLast(outline3);
```

## चरण 4: दस्तावेज़ में पेज जोड़ें

```csharp
// OneNote दस्तावेज़ में पृष्ठ जोड़ें
doc.AppendChildLast(page1);
doc.AppendChildLast(page2);
doc.AppendChildLast(page3);
```

## चरण 5: दस्तावेज़ सहेजें

```csharp
// OneNote दस्तावेज़ सहेजें
string dataDir = "Your Document Directory";
dataDir = dataDir + "CreateDocWithRootAndSubPages_out.one";
doc.Save(dataDir);
```

## निष्कर्ष

बधाई हो! आपने .NET के लिए Aspose.Note का उपयोग करके रूट और उप-पृष्ठों के साथ दस्तावेज़ बनाना सफलतापूर्वक सीख लिया है। अब आप इस ज्ञान का उपयोग अपने अनुप्रयोगों में जटिल OneNote दस्तावेज़ों को गतिशील रूप से उत्पन्न करने के लिए कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Aspose.Note बड़े OneNote दस्तावेज़ों को संभाल सकता है?

A1: हाँ, Aspose.Note को प्रदर्शन से समझौता किए बिना बड़े OneNote दस्तावेज़ों को कुशलतापूर्वक संभालने के लिए डिज़ाइन किया गया है।

### Q2: क्या Aspose.Note .NET कोर के साथ संगत है?

A2: हां, Aspose.Note पारंपरिक .NET फ्रेमवर्क के साथ-साथ .NET कोर का भी समर्थन करता है।

### Q3: क्या मैं Aspose.Note का उपयोग करके OneNote दस्तावेज़ों को अन्य प्रारूपों में परिवर्तित कर सकता हूँ?

A3: बिल्कुल, Aspose.Note PDF, DOCX, HTML और अन्य सहित विभिन्न प्रारूपों में रूपांतरण क्षमताएं प्रदान करता है।

### Q4: क्या Aspose.Note क्लाउड एकीकरण की पेशकश करता है?

A4: Aspose.Note मुख्य रूप से ऑन-प्रिमाइसेस विकास पर केंद्रित है, लेकिन आप इसे उचित सेटअप के साथ क्लाउड वातावरण में उपयोग कर सकते हैं।

### Q5: क्या Aspose.Note के लिए तकनीकी सहायता उपलब्ध है?

A5: हाँ, Aspose अपने फ़ोरम के माध्यम से समर्पित तकनीकी सहायता प्रदान करता है जहाँ आप प्रश्न पूछ सकते हैं और सहायता प्राप्त कर सकते हैं।
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
