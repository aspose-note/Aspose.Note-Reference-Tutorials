---
title: Aspose.Note में टैग के साथ टेक्स्ट नोड जोड़ें
linktitle: Aspose.Note में टैग के साथ टेक्स्ट नोड जोड़ें
second_title: Aspose.Note .NET API
description: .NET के लिए Aspose.Note का उपयोग करके OneNote दस्तावेज़ों में टैग के साथ टेक्स्ट नोड्स जोड़ने का तरीका जानें।
type: docs
weight: 12
url: /hi/net/tag-management/add-text-node-tag/
---
## परिचय

.NET के लिए Aspose.Note एक शक्तिशाली लाइब्रेरी है जो डेवलपर्स को .NET फ्रेमवर्क का उपयोग करके Microsoft OneNote फ़ाइलों को प्रोग्रामेटिक रूप से बनाने, हेरफेर करने और परिवर्तित करने में सक्षम बनाता है। इस ट्यूटोरियल में, हम यह पता लगाएंगे कि .NET के लिए Aspose.Note का उपयोग करके OneNote दस्तावेज़ में टैग के साथ टेक्स्ट नोड कैसे जोड़ा जाए।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित शर्तें हैं:

1. विजुअल स्टूडियो: सुनिश्चित करें कि आपके सिस्टम पर विजुअल स्टूडियो स्थापित है।
2.  .NET के लिए Aspose.Note: .NET के लिए Aspose.Note को डाउनलोड और इंस्टॉल करें[वेबसाइट](https://releases.aspose.com/note/net/).
3. C# का बुनियादी ज्ञान: C# प्रोग्रामिंग भाषा की बुनियादी बातों से खुद को परिचित करें।

## नामस्थान आयात करें

सबसे पहले, आपको .NET के लिए Aspose.Note के साथ काम करने के लिए आवश्यक कक्षाओं और विधियों तक पहुंचने के लिए आवश्यक नामस्थान आयात करने की आवश्यकता है।

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

## चरण 1: एक दस्तावेज़ ऑब्जेक्ट बनाएँ

OneNote दस्तावेज़ के साथ काम शुरू करने के लिए दस्तावेज़ ऑब्जेक्ट को प्रारंभ करें।

```csharp
// दस्तावेज़ निर्देशिका का पथ.
string dataDir = "Your Document Directory";
Document doc = new Document();
```

## चरण 2: पृष्ठ प्रारंभ करें और ऑब्जेक्ट की रूपरेखा बनाएं

OneNote दस्तावेज़ की सामग्री को संरचित करने के लिए पेज और आउटलाइन ऑब्जेक्ट बनाएं।

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
Outline outline = new Outline(doc);
```

## चरण 3: टैग के साथ टेक्स्ट नोड जोड़ें

वांछित टेक्स्ट और शैली के साथ एक रिचटेक्स्ट ऑब्जेक्ट बनाएं, और फिर इसे आउटलाइनएलिमेंट में जोड़ें।

```csharp
OutlineElement outlineElem = new OutlineElement(doc);
ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text = new RichText(doc) { Text = "OneNote text.", ParagraphStyle = textStyle };
text.Tags.Add(NoteTag.CreateYellowStar());
outlineElem.AppendChildLast(text);
```

## चरण 4: रूपरेखा तत्व और पृष्ठ नोड्स जोड़ें

आउटलाइनएलिमेंट को आउटलाइन में जोड़ें, और फिर आउटलाइन को पेज पर जोड़ें। अंत में, पेज को दस्तावेज़ में जोड़ें।

```csharp
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## चरण 5: दस्तावेज़ सहेजें

संशोधित OneNote दस्तावेज़ को निर्दिष्ट स्थान पर सहेजें।

```csharp
string dataDir = "Your Document Directory";
string outputPath = Path.Combine(dataDir, "AddTextNodeWithTag_out.one");
doc.Save(outputPath);
```

## निष्कर्ष

बधाई हो! आपने .NET के लिए Aspose.Note का उपयोग करके OneNote दस्तावेज़ में टैग के साथ टेक्स्ट नोड जोड़ने का तरीका सफलतापूर्वक सीख लिया है। इस ज्ञान के साथ, अब आप अपनी OneNote फ़ाइलों को प्रोग्रामेटिक रूप से अनुकूलित और बढ़ा सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं एक ही दस्तावेज़ में विभिन्न टैग के साथ एकाधिक टेक्स्ट नोड जोड़ सकता हूँ?

A1: हां, आप प्रत्येक नोड के लिए समान प्रक्रिया का पालन करके विभिन्न टैग के साथ एकाधिक टेक्स्ट नोड जोड़ सकते हैं।

### Q2: क्या .NET के लिए Aspose.Note OneNote के सभी संस्करणों के साथ संगत है?

A2: .NET के लिए Aspose.Note 2010, 2013, 2016 और इसके बाद के संस्करण सहित OneNote के विभिन्न संस्करणों का समर्थन करता है।

### Q3: क्या मैं टैग रंग और शैलियाँ अनुकूलित कर सकता हूँ?

A3: हां, आप अपनी आवश्यकताओं के अनुसार टैग रंग और शैलियों को अनुकूलित कर सकते हैं।

### Q4: क्या .NET के लिए Aspose.Note दस्तावेज़ एन्क्रिप्शन का समर्थन करता है?

A4: हां, .NET के लिए Aspose.Note डेटा सुरक्षा सुनिश्चित करने के लिए दस्तावेज़ एन्क्रिप्शन का समर्थन करता है।

### Q5: मुझे .NET के लिए Aspose.Note के लिए अधिक संसाधन और समर्थन कहां मिल सकता है?

 A5: आप इसका पता लगा सकते हैं[.NET दस्तावेज़ीकरण के लिए Aspose.Note](https://reference.aspose.com/note/net/) और से सहायता मांगें[Aspose.नोट फोरम](https://forum.aspose.com/c/note/28).