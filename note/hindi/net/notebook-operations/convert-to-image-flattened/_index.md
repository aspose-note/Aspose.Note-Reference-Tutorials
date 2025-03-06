---
title: Aspose Note .NET में नोटबुक को छवि (चपटा) में बदलें
linktitle: Aspose Note .NET में नोटबुक को छवि (चपटा) में बदलें
second_title: Aspose.Note .NET API
description: .NET के लिए Aspose.Note का उपयोग करके OneNote नोटबुक को चपटी छवियों में परिवर्तित करने का तरीका जानें। निर्बाध एकीकरण के लिए चरण-दर-चरण मार्गदर्शिका।
weight: 12
url: /hi/net/notebook-operations/convert-to-image-flattened/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose Note .NET में नोटबुक को छवि (चपटा) में बदलें

## परिचय

इस ट्यूटोरियल में, हम सीखेंगे कि नोटबुक को चपटी छवियों में बदलने के लिए .NET के लिए Aspose.Note का उपयोग कैसे करें। इसे समझने और इसे प्रभावी ढंग से लागू करने में आपकी सहायता के लिए हम इस प्रक्रिया को सरल चरणों में विभाजित करेंगे।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

1.  .NET के लिए Aspose.Note: यदि आपने पहले से नहीं किया है, तो .NET के लिए Aspose.Note को डाउनलोड और इंस्टॉल करें।[यहाँ](https://releases.aspose.com/note/net/).
2. विकास वातावरण: सुनिश्चित करें कि आपके पास .NET विकास के लिए एक उपयुक्त विकास वातावरण स्थापित है।
3. OneNote नोटबुक: वह OneNote नोटबुक तैयार करें जिसे आप एक छवि में कनवर्ट करना चाहते हैं।

## नामस्थान आयात करें

रूपांतरण प्रक्रिया शुरू करने से पहले, आपको अपने कोड में आवश्यक नामस्थान आयात करने होंगे:

```csharp
using Aspose.Note.Saving;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

अब, आइए .NET के लिए Aspose.Note का उपयोग करके नोटबुक को चपटी छवियों में परिवर्तित करने के लिए चरण-दर-चरण मार्गदर्शिका देखें।

## चरण 1: नोटबुक लोड करें

सबसे पहले, उस OneNote नोटबुक को लोड करें जिसे आप अपने एप्लिकेशन में कनवर्ट करना चाहते हैं।

```csharp
// दस्तावेज़ निर्देशिका का पथ.
string dataDir = "Your Document Directory";

// OneNote नोटबुक लोड करें
var notebook = new Notebook(dataDir + "Notizbuch öffnen.onetoc2");
```

## चरण 2: सहेजें विकल्प सेट करें

छवि प्रारूप और रिज़ॉल्यूशन सहित नोटबुक के लिए सहेजें विकल्पों को परिभाषित करें।

```csharp
var notebookSaveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
var documentSaveOptions = notebookSaveOptions.DocumentSaveOptions;

documentSaveOptions.Resolution = 400;
notebookSaveOptions.Flatten = true;
```

## चरण 3: नोटबुक को छवि के रूप में सहेजें

अब, परिभाषित सेव विकल्पों का उपयोग करके नोटबुक को एक चपटी छवि के रूप में सहेजें।

```csharp
dataDir = dataDir + "ConvertToImageAsFlattenedNotebook_out.png";

// नोटबुक सहेजें
notebook.Save(dataDir, notebookSaveOptions);
```

## निष्कर्ष

इस ट्यूटोरियल में, हमने सीखा कि .NET के लिए Aspose.Note का उपयोग करके नोटबुक को चपटी छवियों में कैसे परिवर्तित किया जाए। चरण-दर-चरण मार्गदर्शिका का पालन करके, आप इस कार्यक्षमता को अपने .NET अनुप्रयोगों में निर्बाध रूप से एकीकृत कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या .NET के लिए Aspose.Note जटिल नोटबुक्स को संभाल सकता है?

A1: हाँ, .NET के लिए Aspose.Note जटिल नोटबुक्स को कुशलतापूर्वक संभालने में सक्षम है।

### Q2: क्या .NET के लिए Aspose.Note का निःशुल्क परीक्षण उपलब्ध है?

 उ2: हाँ, आप नि:शुल्क परीक्षण डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/).

### Q3: क्या Aspose अपने उत्पादों के लिए सहायता प्रदान करता है?

 उ3: हां, आप एस्पोज़ समुदाय से समर्थन प्राप्त कर सकते हैं[यहाँ](https://forum.aspose.com/c/note/28).

### Q4: क्या मैं .NET के लिए Aspose.Note के लिए एक अस्थायी लाइसेंस खरीद सकता हूँ?

 उ4: हाँ, आप एक अस्थायी लाइसेंस खरीद सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/).

### Q5: मुझे .NET के लिए Aspose.Note के लिए दस्तावेज़ कहां मिल सकते हैं?

 A5: आप दस्तावेज़ पा सकते हैं[यहाँ](https://reference.aspose.com/note/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
