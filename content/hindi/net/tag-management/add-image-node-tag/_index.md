---
title: Aspose.Note में टैग के साथ छवि नोड जोड़ें
linktitle: Aspose.Note में टैग के साथ छवि नोड जोड़ें
second_title: Aspose.Note .NET API
description: जानें कि .NET के लिए Aspose.Note का उपयोग करके कस्टम टैग के साथ छवियां जोड़कर अपने OneNote दस्तावेज़ों को कैसे बढ़ाया जाए।
type: docs
weight: 10
url: /hi/net/tag-management/add-image-node-tag/
---
## परिचय

इस ट्यूटोरियल में, हम जानेंगे कि .NET के लिए Aspose.Note का उपयोग करके टैग के साथ एक छवि नोड कैसे जोड़ा जाए। यह सुविधा आपको कस्टम टैग के साथ छवियां जोड़कर अपने OneNote दस्तावेज़ों को बेहतर बनाने की अनुमति देती है।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

1. विजुअल स्टूडियो: अपने सिस्टम पर विजुअल स्टूडियो आईडीई स्थापित करें।
2.  .NET के लिए Aspose.Note: .NET लाइब्रेरी के लिए Aspose.Note को डाउनलोड और इंस्टॉल करें।[लिंक को डाउनलोड करें](https://releases.aspose.com/note/net/).
3. बुनियादी ज्ञान: C# प्रोग्रामिंग भाषा और .NET फ्रेमवर्क से खुद को परिचित करें।

## नामस्थान आयात करें

सबसे पहले, अपने C# कोड में आवश्यक नामस्थान शामिल करना सुनिश्चित करें:

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

## चरण 1: दस्तावेज़ और पृष्ठ ऑब्जेक्ट प्रारंभ करें

 का एक उदाहरण बनाकर शुरुआत करें`Document` कक्षा और ए`Page` वस्तु:

```csharp
Document doc = new Document();
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## चरण 2: आउटलाइन और आउटलाइनएलिमेंट ऑब्जेक्ट को आरंभ करें

 अगला, आरंभ करें`Outline` और`OutlineElement` वस्तुएं:

```csharp
Outline outline = new Outline(doc);
OutlineElement outlineElem = new OutlineElement(doc);
```

## चरण 3: छवि लोड करें और डालें

वांछित छवि लोड करें और इसे दस्तावेज़ नोड में डालें:

```csharp
Aspose.Note.Image image = new Aspose.Note.Image(doc, "path_to_your_image.jpg");
outlineElem.AppendChildLast(image);
```

## चरण 4: छवि में टैग जोड़ें

छवि में एक कस्टम टैग जोड़ें:

```csharp
image.Tags.Add(NoteTag.CreateYellowStar());
```

## चरण 5: रूपरेखा तत्व और पृष्ठ नोड्स जोड़ें

पृष्ठ पर रूपरेखा तत्व और रूपरेखा नोड्स जोड़ें:

```csharp
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
```

## चरण 6: दस्तावेज़ सहेजें

संशोधित OneNote दस्तावेज़ सहेजें:

```csharp
doc.AppendChildLast(page);
string outputFilePath = "output_path/AddImageNodeWithTag_out.one";
doc.Save(outputFilePath);
```

## निष्कर्ष

इन चरणों का पालन करके, आप .NET के लिए Aspose.Note का उपयोग करके कस्टम टैग के साथ एक छवि नोड को सहजता से जोड़ सकते हैं, अपने OneNote दस्तावेज़ों को व्यक्तिगत दृश्यों के साथ समृद्ध कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं Aspose.Note का उपयोग करके एक ही दस्तावेज़ में अलग-अलग टैग के साथ कई छवियां जोड़ सकता हूं?

A1: हां, आप प्रत्येक छवि के लिए समान चरणों का पालन करके विभिन्न टैग के साथ कई छवियां जोड़ सकते हैं।

### Q2: क्या Aspose.Note OneNote के सभी संस्करणों के साथ संगत है?

A2: Aspose.Note विभिन्न परिवेशों में अनुकूलता सुनिश्चित करते हुए, OneNote के विभिन्न संस्करणों का समर्थन करता है।

### Q3: क्या मैं छवि में जोड़े गए टैग के स्वरूप को अनुकूलित कर सकता हूँ?

A3: हां, Aspose.Note आपकी प्राथमिकताओं के अनुरूप टैग उपस्थिति को अनुकूलित करने में लचीलापन प्रदान करता है।

### Q4: क्या Aspose.Note यूआरएल से छवियां जोड़ने के लिए समर्थन प्रदान करता है?

A4: Aspose.Note मुख्य रूप से स्थानीय निर्देशिकाओं से छवियों को जोड़ने का समर्थन करता है, लेकिन आप बाहरी छवियों को पहले स्थानीय रूप से डाउनलोड करके शामिल कर सकते हैं।

### Q5: क्या जोड़ी जा सकने वाली छवियों के आकार या प्रारूप पर कोई सीमाएँ हैं?

A5: Aspose.Note छवि प्रारूपों की एक विस्तृत श्रृंखला का समर्थन करता है और छवि आकार पर कोई सख्त सीमा नहीं लगाता है, जिससे आप अपने दस्तावेज़ों में विविध दृश्यों को शामिल कर सकते हैं।