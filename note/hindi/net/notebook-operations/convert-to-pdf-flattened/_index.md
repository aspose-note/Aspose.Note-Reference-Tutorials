---
title: Aspose Note .NET में नोटबुक को पीडीएफ (चपटा) में बदलें
linktitle: Aspose Note .NET में नोटबुक को पीडीएफ (चपटा) में बदलें
second_title: Aspose.Note .NET API
description: .NET के लिए Aspose.Note का उपयोग करके OneNote नोटबुक को आसानी से फ़्लैट किए गए PDF में परिवर्तित करना सीखें। अपनी सामग्री को निर्बाध रूप से सुरक्षित रखें.
weight: 15
url: /hi/net/notebook-operations/convert-to-pdf-flattened/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose Note .NET में नोटबुक को पीडीएफ (चपटा) में बदलें

## परिचय

क्या आप Aspose Note .NET का उपयोग करके अपनी OneNote नोटबुक को चपटी PDF में परिवर्तित करना चाह रहे हैं? आप सही जगह पर हैं! इस ट्यूटोरियल में, हम चरण दर चरण प्रक्रिया से गुजरेंगे।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

1.  .NET के लिए Aspose.Note: सुनिश्चित करें कि आपने .NET के लिए Aspose.Note को डाउनलोड और इंस्टॉल कर लिया है। यदि नहीं, तो आप इसे प्राप्त कर सकते हैं[यहाँ](https://releases.aspose.com/note/net/).
2. विज़ुअल स्टूडियो: कोडिंग और संकलन के लिए आपको अपने सिस्टम पर विज़ुअल स्टूडियो स्थापित करना होगा।
3. वननोट नोटबुक: एक वननोट नोटबुक तैयार रखें जिसे आप पीडीएफ में बदलना चाहते हैं।

## नामस्थान आयात करें

आइए आपके C# कोड में आवश्यक नामस्थान आयात करके प्रारंभ करें:

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Collections.Generic;
```

## चरण 1: OneNote नोटबुक लोड करें

```csharp
// दस्तावेज़ निर्देशिका का पथ.
string dataDir = "Your Document Directory";

// OneNote नोटबुक लोड करें
var notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

 इस चरण में, हम OneNote नोटबुक का उपयोग करके लोड करते हैं`Notebook` Aspose.Note द्वारा प्रदान की गई कक्षा।

## चरण 2: फ़्लैटनिंग के साथ पीडीएफ में कनवर्ट करें

```csharp
// नोटबुक को फ़्लैटिंग के साथ पीडीएफ के रूप में सहेजें
dataDir = dataDir + "ConvertToPDFAsFlattened_out.pdf";
notebook.Save(
    dataDir,
    new NotebookPdfSaveOptions
    {
        Flatten = true
    }); 
```

 यहां, हम भरी हुई नोटबुक को पीडीएफ के रूप में सहेजते हैं`Flatten` संपत्ति के लिए सेट`true`. यह प्रॉपर्टी एनोटेशन और छवियों सहित सभी सामग्री को पीडीएफ में समतल कर देती है।

## चरण 3: सफलता संदेश प्रिंट करें

```csharp
Console.WriteLine("\nNoteBook document converted to PDF as flattened successfully.\nFile saved at " + dataDir);
```

अंत में, हम उस पथ के साथ एक सफलता संदेश प्रिंट करते हैं जहां पीडीएफ सहेजा गया है।

## निष्कर्ष

बधाई हो! आपने .NET के लिए Aspose.Note का उपयोग करके अपने OneNote नोटबुक को एक चपटा PDF में सफलतापूर्वक परिवर्तित कर लिया है। यह प्रक्रिया सुनिश्चित करती है कि आपकी सभी सामग्री पीडीएफ प्रारूप में सटीक रूप से संरक्षित है, जिससे साझा करना और वितरित करना आसान हो जाता है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं पीडीएफ में इंटरैक्टिव तत्वों को संरक्षित कर सकता हूं?

A1: Aspose.Note चेकबॉक्स या फॉर्म फ़ील्ड जैसे इंटरैक्टिव तत्वों सहित सामग्री को पीडीएफ में समतल कर देता है, जिससे वे स्थिर हो जाते हैं।

### Q2: क्या Aspose.Note नोटबुक को अन्य प्रारूपों में परिवर्तित करने का समर्थन करता है?

A2: हां, Aspose.Note नोटबुक को पीडीएफ, HTML, इमेज और अन्य जैसे विभिन्न प्रारूपों में परिवर्तित करने का समर्थन करता है।

### Q3: क्या मैं रूपांतरण विकल्पों को अनुकूलित कर सकता हूँ?

उ3: बिल्कुल! Aspose.Note रूपांतरण प्रक्रिया के दौरान अनुकूलन के लिए व्यापक विकल्प प्रदान करता है, जिससे आप अपनी आवश्यकताओं के अनुसार आउटपुट को तैयार कर सकते हैं।

### Q4: क्या कोई परीक्षण संस्करण उपलब्ध है?

 A4: हाँ, आप Aspose.Note का निःशुल्क परीक्षण प्राप्त कर सकते हैं[यहाँ](https://releases.aspose.com/).

### Q5: यदि मुझे कोई समस्या आती है तो मुझे कहां से सहायता मिल सकती है?

 A5: आप Aspose समुदाय से समर्थन प्राप्त कर सकते हैं[Aspose.नोट फ़ोरम](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
