---
title: Aspose.Note में टैग के साथ तालिका नोड जोड़ें
linktitle: Aspose.Note में टैग के साथ तालिका नोड जोड़ें
second_title: Aspose.Note .NET API
description: जानें कि .NET के लिए Aspose.Note में टैग के साथ तालिकाएँ कैसे जोड़ें। अपने दस्तावेज़ हेरफेर कौशल को प्रोग्रामेटिक रूप से बढ़ाएं।
type: docs
weight: 11
url: /hi/net/tag-management/add-table-node-tag/
---
## परिचय

इस ट्यूटोरियल में, हम .NET के लिए Aspose.Note का उपयोग करके एक टैग के साथ तालिका नोड जोड़ने की प्रक्रिया में आपका मार्गदर्शन करेंगे। इसे प्राप्त करने के लिए नीचे दिए गए चरणों का पालन करें।

## नामस्थान आयात करें

आरंभ करने से पहले, Aspose.Note के साथ काम करने के लिए आवश्यक नामस्थान आयात करना सुनिश्चित करें:

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using Aspose.Note.Examples.CSharp.Tables;
```

## आवश्यक शर्तें

सुनिश्चित करें कि आगे बढ़ने से पहले आपके पास निम्नलिखित आवश्यक शर्तें हों:

1.  इंस्टालेशन: .NET लाइब्रेरी के लिए Aspose.Note को डाउनलोड और इंस्टॉल करें[यहाँ](https://releases.aspose.com/note/net/).
2.  लाइसेंस: लाइसेंस प्राप्त करें या इसका उपयोग करें[अस्थायी लाइसेंस](https://purchase.aspose.com/temporary-license/) पुस्तकालय का उपयोग करने के लिए.
3. विकास परिवेश: एक संगत विकास परिवेश स्थापित करें, जैसे विज़ुअल स्टूडियो।

## चरण 1: दस्तावेज़ और पृष्ठ ऑब्जेक्ट प्रारंभ करें

 का एक उदाहरण बनाकर प्रारंभ करें`Document` कक्षा और आरंभीकरण a`Page` वस्तु:

```csharp
Document doc = new Document();
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## चरण 2: तालिका, पंक्ति और सेल ऑब्जेक्ट बनाएं

 को आरंभ करें`Table`, `TableRow` , और`TableCell` वस्तुएं:

```csharp
TableRow row = new TableRow(doc);
TableCell cell = new TableCell(doc);
```

## चरण 3: सेल में सामग्री डालें

 का उपयोग करके सेल में सामग्री जोड़ें`AppendChildLast` तरीका:

```csharp
cell.AppendChildLast(InsertTable.GetOutlineElementWithText(doc, "Single cell."));
```

## चरण 4: तालिका नोड प्रारंभ करें

 को आरंभ करें`Table` निर्दिष्ट गुणों वाली वस्तु:

```csharp
Table table = new Table(doc)
{
    IsBordersVisible = true,
    Columns = { new TableColumn { Width = 70 } }
};
```

## चरण 5: पंक्ति को तालिका में जोड़ें

तालिका में पंक्ति नोड जोड़ें:

```csharp
table.AppendChildLast(row);
```

## चरण 6: टेबल नोड में टैग जोड़ें

तालिका नोड के लिए एक टैग शामिल करें:

```csharp
table.Tags.Add(NoteTag.CreateQuestionMark());
```

## चरण 7: आउटलाइन एलिमेंट में टेबल नोड जोड़ें

 एक बनाएं`Outline` और`OutlineElement` तालिका नोड जोड़ने के लिए:

```csharp
Outline outline = new Outline(doc);
OutlineElement outlineElem = new OutlineElement(doc);
outlineElem.AppendChildLast(table);
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## चरण 8: दस्तावेज़ सहेजें

OneNote दस्तावेज़ सहेजें:

```csharp
string dataDir = "Your Document Directory";
dataDir = dataDir + "AddTableNodeWithTag_out.one";
doc.Save(dataDir);
Console.WriteLine("\nTable node with tag added successfully.\nFile saved at " + dataDir);
```

इन चरणों का पालन करने के बाद, आपको .NET के लिए Aspose.Note का उपयोग करके एक टैग के साथ एक तालिका नोड को सफलतापूर्वक जोड़ना चाहिए।

## निष्कर्ष

इस ट्यूटोरियल में, हमने .NET के लिए Aspose.Note में एक टैग के साथ टेबल नोड जोड़ने की प्रक्रिया को कवर किया है। इन चरणों का पालन करके, आप अपनी दस्तावेज़ प्रबंधन क्षमताओं को बढ़ाते हुए OneNote दस्तावेज़ों को प्रोग्रामेटिक रूप से कुशलतापूर्वक प्रबंधित कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Aspose.Note .NET के सभी संस्करणों के साथ संगत है?

A1: .NET के लिए Aspose.Note .NET कोर और .NET मानक सहित .NET फ्रेमवर्क संस्करण 2.0 और उससे ऊपर का समर्थन करता है।

### Q2: क्या मैं लाइसेंस खरीदने से पहले Aspose.Note आज़मा सकता हूँ?

 उ2: हाँ, आप Aspose.Note का निःशुल्क परीक्षण प्राप्त कर सकते हैं[यहाँ](https://releases.aspose.com/).

### Q3: मैं Aspose.Note के लिए अस्थायी लाइसेंस कैसे प्राप्त करूं?

 A3: आप यहां से अस्थायी लाइसेंस प्राप्त कर सकते हैं[इस लिंक](https://purchase.aspose.com/temporary-license/), जो 30 दिनों के लिए वैध है।

### Q4: क्या Aspose.Note दस्तावेज़ एन्क्रिप्शन का समर्थन करता है?

A4: हाँ, Aspose.Note डेटा सुरक्षा सुनिश्चित करने के लिए OneNote दस्तावेज़ों को एन्क्रिप्ट करने के लिए समर्थन प्रदान करता है।

### Q5: क्या Aspose.Note उपयोगकर्ताओं के लिए तकनीकी सहायता उपलब्ध है?

 A5: हां, Aspose मंचों के माध्यम से तकनीकी सहायता प्रदान की जाती है[यहाँ](https://forum.aspose.com/c/note/28), जहां आप विशेषज्ञों से सहायता ले सकते हैं।