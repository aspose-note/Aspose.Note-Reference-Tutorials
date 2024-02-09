---
title: Aspose.Note में छवियों की जानकारी प्राप्त करें
linktitle: Aspose.Note में छवियों की जानकारी प्राप्त करें
second_title: Aspose.Note .NET API
description: .NET के लिए Aspose.Note का उपयोग करके Microsoft OneNote फ़ाइलों से छवि जानकारी निकालने का तरीका जानें। कुशल विकास के लिए हमारे चरण-दर-चरण मार्गदर्शिका का पालन करें।
type: docs
weight: 13
url: /hi/net/images/get-info-of-images/
---
## परिचय

.NET विकास की दुनिया में, Aspose.Note Microsoft OneNote फ़ाइलों के साथ काम करने के लिए उपकरणों का एक शक्तिशाली सेट प्रदान करता है। डेवलपर्स द्वारा अक्सर सामना किया जाने वाला एक सामान्य कार्य इन नोटों के भीतर एम्बेडेड छवियों से जानकारी निकालना है। चाहे वह आयाम, फ़ाइल नाम, या संशोधन समय प्राप्त करना हो, Aspose.Note इस प्रक्रिया को सरल बनाता है।

## आवश्यक शर्तें

इससे पहले कि हम Aspose.Note के साथ छवि जानकारी निकालना शुरू करें, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

1. C# का बुनियादी ज्ञान: कोड उदाहरणों को समझने के लिए C# प्रोग्रामिंग भाषा से परिचित होना आवश्यक है।
2.  .NET के लिए Aspose.Note स्थापित: सुनिश्चित करें कि आपके पास अपने विकास परिवेश में Aspose.Note लाइब्रेरी स्थापित है। आप इसे डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/note/net/).

## नामस्थान आयात करें

शुरू करने से पहले, आइए आवश्यक नामस्थान आयात करें:

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System;
```

## चरण 1: दस्तावेज़ लोड करें

सबसे पहले, लक्ष्य OneNote दस्तावेज़ को Aspose.Note में लोड करें:

```csharp
// दस्तावेज़ निर्देशिका का पथ.
string dataDir = "Your Document Directory";

// दस्तावेज़ को Aspose.Note में लोड करें।
Document oneFile = new Document(dataDir + "Aspose.one");
```

 प्रतिस्थापित करें`"Your Document Directory"` आपकी OneNote फ़ाइल के पथ के साथ।

## चरण 2: छवि जानकारी पुनः प्राप्त करें

इसके बाद, दस्तावेज़ से सभी छवि नोड्स पुनर्प्राप्त करें:

```csharp
// सभी छवि नोड प्राप्त करें
IList<Aspose.Note.Image> images = oneFile.GetChildNodes<Aspose.Note.Image>();
```

यह कोड स्निपेट लोड किए गए OneNote दस्तावेज़ के भीतर सभी छवि नोड्स को लाता है।

## चरण 3: छवियों के माध्यम से पुनरावृति करें

अब, आइए प्रत्येक छवि नोड के माध्यम से उसका मेटाडेटा निकालने के लिए पुनरावृति करें:

```csharp
foreach (Aspose.Note.Image image in images)
{
    Console.WriteLine("Width: {0}", image.Width);
    Console.WriteLine("Height: {0}", image.Height);
    Console.WriteLine("OriginalWidth: {0}", image.OriginalWidth);
    Console.WriteLine("OriginalHeight: {0}", image.OriginalHeight);
    Console.WriteLine("FileName: {0}", image.FileName);
    Console.WriteLine("LastModifiedTime: {0}", image.LastModifiedTime);
    Console.WriteLine();
}
```

यह लूप प्रत्येक छवि की विभिन्न विशेषताओं को प्रिंट करता है, जैसे चौड़ाई, ऊंचाई, मूल आयाम, फ़ाइल नाम और अंतिम संशोधित समय।

## निष्कर्ष

.NET के लिए Aspose.Note के साथ, OneNote दस्तावेज़ों से छवि जानकारी निकालना एक सहज प्रक्रिया बन जाती है। इस ट्यूटोरियल में बताए गए चरणों का पालन करके, डेवलपर्स एम्बेडेड छवियों से मेटाडेटा को कुशलतापूर्वक पुनर्प्राप्त कर सकते हैं, जिससे उन्हें मजबूत एप्लिकेशन बनाने में सशक्त बनाया जा सकता है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Aspose.Note Microsoft OneNote के सभी संस्करणों के साथ संगत है?

A1: Aspose.Note .one, .onepkg, और .onetoc2 सहित OneNote फ़ाइलों के विभिन्न स्वरूपों का समर्थन करता है, जो विभिन्न संस्करणों में अनुकूलता सुनिश्चित करता है।

### Q2: क्या मैं Aspose.Note का उपयोग करके छवि गुणों को संशोधित कर सकता हूँ?

A2: हां, Aspose.Note आपको छवि गुणों जैसे आयाम, फ़ाइल नाम और संशोधन समय को प्रोग्रामेटिक रूप से हेरफेर करने की अनुमति देता है।

### Q3: क्या Aspose.Note .NET कोर के लिए समर्थन प्रदान करता है?

A3: हाँ, Aspose.Note .NET कोर के लिए समर्थन प्रदान करता है, जो आपके अनुप्रयोगों के लिए क्रॉस-प्लेटफ़ॉर्म विकास को सक्षम करता है।

### Q4: क्या Aspose.Note के लिए कोई निःशुल्क परीक्षण उपलब्ध है?

उ4: हाँ, आप खरीदारी करने से पहले इसकी विशेषताओं का पता लगाने के लिए Aspose.Note का निःशुल्क परीक्षण प्राप्त कर सकते हैं।

### Q5: मुझे Aspose.Note के साथ अतिरिक्त सहायता या सहायता कहां मिल सकती है?

 A5: किसी भी पूछताछ या सहायता के लिए, आप Aspose.Note फोरम पर जा सकते हैं[यहाँ](https://forum.aspose.com/c/note/28).