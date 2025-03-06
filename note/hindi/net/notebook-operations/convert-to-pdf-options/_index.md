---
title: Aspose Note .NET में विकल्पों के साथ नोटबुक को पीडीएफ में बदलें
linktitle: Aspose Note .NET में विकल्पों के साथ नोटबुक को पीडीएफ में बदलें
second_title: Aspose.Note .NET API
description: अनुकूलन योग्य विकल्पों के साथ .NET लाइब्रेरी के लिए Aspose.Note का उपयोग करके Microsoft OneNote नोटबुक को PDF प्रारूप में परिवर्तित करने का तरीका जानें।
weight: 16
url: /hi/net/notebook-operations/convert-to-pdf-options/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose Note .NET में विकल्पों के साथ नोटबुक को पीडीएफ में बदलें

## परिचय

इस ट्यूटोरियल में, हम .NET लाइब्रेरी के लिए Aspose.Note का उपयोग करके नोटबुक को पीडीएफ प्रारूप में परिवर्तित करने की प्रक्रिया के बारे में जानेंगे। .NET के लिए Aspose.Note Microsoft OneNote फ़ाइलों के साथ प्रोग्रामेटिक रूप से काम करने के लिए सुविधाओं का एक शक्तिशाली सेट प्रदान करता है।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यकताएँ हैं:

### 1. .NET लाइब्रेरी के लिए Aspose.Note
 सुनिश्चित करें कि आपने .NET लाइब्रेरी के लिए Aspose.Note डाउनलोड और इंस्टॉल कर लिया है। आप इसे यहां से डाउनलोड कर सकते हैं[वेबसाइट](https://releases.aspose.com/note/net/).

### 2. विकास का वातावरण
आपके पास आवश्यक .NET फ्रेमवर्क स्थापित होने के साथ विजुअल स्टूडियो जैसा एक विकास वातावरण स्थापित होना चाहिए।

## नामस्थान आयात करें

इससे पहले कि हम अपने प्रोजेक्ट में .NET के लिए Aspose.Note का उपयोग शुरू करें, आइए आवश्यक नेमस्पेस आयात करें:

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Collections.Generic;
```

अब, आइए विकल्पों के साथ नोटबुक को पीडीएफ में परिवर्तित करने की प्रक्रिया को कई चरणों में विभाजित करें:

## चरण 1: नोटबुक लोड करें

सबसे पहले, हमें OneNote नोटबुक को लोड करना होगा जिसे हम एक पीडीएफ फाइल में बदलना चाहते हैं।

```csharp
// दस्तावेज़ निर्देशिका का पथ.
string dataDir = "Your Document Directory";

// OneNote नोटबुक लोड करें
var notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## चरण 2: पीडीएफ सेव विकल्प निर्दिष्ट करें

इसके बाद, हम नोटबुक को पीडीएफ फ़ाइल के रूप में सहेजने के विकल्प निर्दिष्ट करेंगे। हम विभिन्न सेटिंग्स जैसे पेज स्प्लिटिंग एल्गोरिदम, मार्जिन और पेज आकार को अनुकूलित कर सकते हैं।

```csharp
var notebookSaveOptions = new NotebookPdfSaveOptions();
var documentSaveOptions = notebookSaveOptions.DocumentSaveOptions;

documentSaveOptions.PageSplittingAlgorithm = new KeepSolidObjectsAlgorithm();
```

## चरण 3: नोटबुक को पीडीएफ के रूप में सहेजें

अब, हम निर्दिष्ट विकल्पों का उपयोग करके नोटबुक को पीडीएफ फ़ाइल के रूप में सहेजेंगे।

```csharp
dataDir = dataDir + "ConvertToPDF_out.pdf";

// नोटबुक सहेजें
notebook.Save(dataDir, notebookSaveOptions);
```

## चरण 4: रूपांतरण सत्यापित करें

अंत में, आइए सत्यापित करें कि रूपांतरण सफल रहा और उस स्थान को प्रिंट करें जहां पीडीएफ फ़ाइल सहेजी गई है।

```csharp
Console.WriteLine("\nNoteBook document converted to pdf successfully with save options.\nFile saved at " + dataDir);
```

## निष्कर्ष

इस ट्यूटोरियल में, हमने सीखा है कि .NET लाइब्रेरी के लिए Aspose.Note का उपयोग करके OneNote नोटबुक को पीडीएफ प्रारूप में कैसे परिवर्तित किया जाए। ऊपर बताए गए चरणों का पालन करके, आप इस कार्यक्षमता को अपने .NET अनुप्रयोगों में आसानी से एकीकृत कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या .NET के लिए Aspose.Note Microsoft OneNote के सभी संस्करणों के साथ संगत है?

A1: हाँ, .NET के लिए Aspose.Note Microsoft OneNote के विभिन्न संस्करणों का समर्थन करता है, जिसमें .one और .onetoc2 प्रारूप शामिल हैं।

### Q2: क्या मैं पीडीएफ आउटपुट के स्वरूप को अनुकूलित कर सकता हूँ?

उ2: हां, आप पीडीएफ आउटपुट की उपस्थिति को अनुकूलित करने के लिए पेज आकार, मार्जिन और पेज स्प्लिटिंग एल्गोरिदम जैसे विभिन्न विकल्प निर्दिष्ट कर सकते हैं।

### Q3: क्या .NET के लिए Aspose.Note अन्य फ़ाइल स्वरूपों के लिए समर्थन प्रदान करता है?

A3: हाँ, .NET के लिए Aspose.Note छवियों, HTML और Microsoft Word दस्तावेज़ों जैसे विभिन्न अन्य प्रारूपों में रूपांतरण का समर्थन करता है।

### Q4: क्या .NET के लिए Aspose.Note का निःशुल्क परीक्षण उपलब्ध है?

A4: हाँ, आप खरीदारी करने से पहले इसकी विशेषताओं का मूल्यांकन करने के लिए वेबसाइट से .NET के लिए Aspose.Note का निःशुल्क परीक्षण डाउनलोड कर सकते हैं।

### Q5: मैं .NET के लिए Aspose.Note के लिए तकनीकी सहायता कैसे प्राप्त कर सकता हूं?

 A5: आप पर जाकर .NET के लिए Aspose.Note के लिए तकनीकी सहायता प्राप्त कर सकते हैं[Aspose.नोट फोरम](https://forum.aspose.com/c/note/28) या Aspose सहायता टीम से सीधे संपर्क करना।
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
