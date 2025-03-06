---
title: Aspose.Note दस्तावेज़ों में पृष्ठ संशोधनों का अन्वेषण करें
linktitle: Aspose.Note दस्तावेज़ों में पृष्ठ संशोधनों का अन्वेषण करें
second_title: Aspose.Note .NET API
description: चरण-दर-चरण मार्गदर्शन के साथ .NET फ्रेमवर्क का उपयोग करके Aspose.Note दस्तावेज़ों में पृष्ठ संशोधनों का पता लगाना सीखें।
weight: 14
url: /hi/net/note-manipulation/page-revisions-exploration/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note दस्तावेज़ों में पृष्ठ संशोधनों का अन्वेषण करें

## परिचय

इस ट्यूटोरियल में, हम .NET फ्रेमवर्क का उपयोग करके Aspose.Note दस्तावेज़ों में पेज संशोधनों की खोज करेंगे। Aspose.Note एक शक्तिशाली लाइब्रेरी है जो डेवलपर्स को Microsoft OneNote फ़ाइलों के साथ प्रोग्रामेटिक रूप से काम करने में सक्षम बनाती है, और इन फ़ाइलों से डेटा में हेरफेर करने और निकालने के लिए विभिन्न सुविधाएँ प्रदान करती है।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ स्थापित हैं:

### 1. .NET के लिए Aspose.Note डाउनलोड और इंस्टॉल करें

 दौरा करना[डाउनलोड पेज](https://releases.aspose.com/note/net/) और .NET लाइब्रेरी के लिए Aspose.Note डाउनलोड करें। अपने विकास परिवेश में लाइब्रेरी स्थापित करने के लिए दिए गए इंस्टॉलेशन निर्देशों का पालन करें।

### 2. आवश्यक नामस्थान लोड करें

Aspose.Note कार्यात्मकताओं तक निर्बाध रूप से पहुंचने के लिए अपने .NET प्रोजेक्ट में आवश्यक नेमस्पेस आयात करना सुनिश्चित करें।

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

अब, आइए पृष्ठ संशोधनों की खोज की प्रक्रिया को चरण-दर-चरण निर्देशों में विभाजित करें:

## चरण 1: दस्तावेज़ लोड करें

सबसे पहले, हमें Aspose.Note दस्तावेज़ को लोड करना होगा, जिससे दस्तावेज़ इतिहास की लोडिंग सक्षम हो सके।

```csharp
string dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Aspose.one", new LoadOptions { LoadHistory = true });
```

## चरण 2: पृष्ठ संशोधन पुनः प्राप्त करें

एक बार दस्तावेज़ लोड हो जाने पर, हम किसी विशिष्ट पृष्ठ के लिए संशोधन पुनः प्राप्त कर सकते हैं। इस उदाहरण में, हमें पहले पृष्ठ के लिए संशोधन मिलेंगे।

```csharp
Page firstPage = document.FirstChild;
foreach (Page pageRevision in document.GetPageHistory(firstPage))
{
    /*Use pageRevision like a regular page.*/
    Console.WriteLine("LastModifiedTime: {0}", pageRevision.LastModifiedTime);
    Console.WriteLine("CreationTime: {0}", pageRevision.CreationTime);
    Console.WriteLine("Title: {0}", pageRevision.Title);
    Console.WriteLine("Level: {0}", pageRevision.Level);
    Console.WriteLine("Author: {0}", pageRevision.Author);
    Console.WriteLine();
}
```

## चरण 3: संशोधनों के माध्यम से पुनरावृति करें

लूप के भीतर, पृष्ठ के प्रत्येक संशोधन के माध्यम से पुनरावृति करें और इसके गुणों जैसे अंतिम संशोधित समय, निर्माण समय, शीर्षक, स्तर और लेखक तक पहुंचें।

## निष्कर्ष

.NET का उपयोग करके Aspose.Note दस्तावेज़ों में पृष्ठ संशोधन की खोज करना एक सीधी प्रक्रिया है। इस ट्यूटोरियल में उल्लिखित चरणों का पालन करके, आप प्रोग्रामेटिक रूप से अपनी OneNote फ़ाइलों के संशोधन इतिहास को प्रभावी ढंग से पुनर्प्राप्त और विश्लेषण कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं नए OneNote दस्तावेज़ बनाने के लिए .NET के लिए Aspose.Note का उपयोग कर सकता हूँ?

A1: हाँ, .NET के लिए Aspose.Note आपको OneNote दस्तावेज़ों को प्रोग्रामेटिक रूप से बनाने, संपादित करने और हेरफेर करने की अनुमति देता है।

### Q2: क्या Aspose.Note सभी प्रकार की OneNote फ़ाइलों के लिए लोडिंग इतिहास का समर्थन करता है?

A2: Aspose.Note .one और .onepkg दोनों फ़ाइल स्वरूपों के लिए लोडिंग इतिहास का समर्थन करता है।

### Q3: क्या .NET के लिए Aspose.Note का निःशुल्क परीक्षण उपलब्ध है?

उ3: हाँ, आप .NET के लिए Aspose.Note का निःशुल्क परीक्षण डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/).

### Q4: मैं .NET के लिए Aspose.Note के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?

 उ4: आप यहां से अस्थायी लाइसेंस का अनुरोध कर सकते हैं[इस लिंक](https://purchase.aspose.com/temporary-license/).

### Q5: मुझे .NET के लिए Aspose.Note के लिए समर्थन कहां मिल सकता है?

 A5: आप यहां सहायता और संसाधन पा सकते हैं[Aspose.नोट फोरम](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
