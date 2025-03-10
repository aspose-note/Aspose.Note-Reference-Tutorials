---
title: Aspose.Note दस्तावेज़ों में छवियाँ सम्मिलित करें
linktitle: Aspose.Note दस्तावेज़ों में छवियाँ सम्मिलित करें
second_title: Aspose.Note .NET API
description: उन्नत दृश्य सामग्री के लिए .NET का उपयोग करके Aspose.Note दस्तावेज़ों में छवियों को निर्बाध रूप से सम्मिलित करना सीखें। आसान एकीकरण के लिए हमारी चरण-दर-चरण मार्गदर्शिका का पालन करें।
weight: 16
url: /hi/net/images/insert-images/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note दस्तावेज़ों में छवियाँ सम्मिलित करें

## परिचय

अपने Aspose.Note दस्तावेज़ों में छवियां जोड़ने से उनकी दृश्य अपील और उपयोगिता में काफी वृद्धि हो सकती है। चाहे आप नोट्स, प्रेजेंटेशन या कोई अन्य दस्तावेज़ बना रहे हों, छवियों को एकीकृत करने से आपकी सामग्री को संदर्भ और स्पष्टता मिल सकती है। इस ट्यूटोरियल में, हम .NET का उपयोग करके आपके Aspose.Note दस्तावेज़ों में छवियां सम्मिलित करने की प्रक्रिया में आपका मार्गदर्शन करेंगे।

## आवश्यक शर्तें

आरंभ करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

1.  .NET के लिए Aspose.Note: .NET के लिए Aspose.Note को डाउनलोड और इंस्टॉल करें[यहाँ](https://releases.aspose.com/note/net/).
   
2. छवि फ़ाइलें: वे छवि फ़ाइलें तैयार करें जिन्हें आप अपने Aspose.Note दस्तावेज़ों में सम्मिलित करना चाहते हैं।

## नामस्थान आयात करें

सबसे पहले, आपको अपने .NET प्रोजेक्ट में Aspose.Note के साथ काम करने के लिए आवश्यक नेमस्पेस आयात करने की आवश्यकता है। यहां बताया गया है कि आप यह कैसे कर सकते हैं:

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System.Drawing;
using System;
```

## चरण 1: दस्तावेज़ लोड करें और पृष्ठ प्राप्त करें

अपने मौजूदा Aspose.Note दस्तावेज़ को लोड करके और वांछित पृष्ठ तक पहुँचकर शुरुआत करें जहाँ आप छवि सम्मिलित करना चाहते हैं।

```csharp
string dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "YourDocument.one");
Aspose.Note.Page page = doc.FirstChild;
```

## चरण 2: छवि लोड करें और गुण सेट करें

इसके बाद, उस छवि को लोड करें जिसे आप सम्मिलित करना चाहते हैं और अपनी आवश्यकताओं के अनुसार उसके गुणों जैसे चौड़ाई, ऊंचाई, ऑफसेट और संरेखण को निर्दिष्ट करें।

```csharp
Aspose.Note.Image image = new Aspose.Note.Image(doc, dataDir + "image.jpg")
{
    Width = 100,                // छवि की चौड़ाई निर्धारित करें
    Height = 100,               // छवि ऊंचाई सेट करें
    HorizontalOffset = 100,     // क्षैतिज ऑफसेट सेट करें
    VerticalOffset = 400,       // लंबवत ऑफसेट सेट करें
    Alignment = HorizontalAlignment.Right  // छवि संरेखण सेट करें
};
```

## चरण 3: पेज पर छवि जोड़ें

एक बार जब आप छवि गुणों को कॉन्फ़िगर कर लें, तो छवि को अपने Aspose.Note दस्तावेज़ के वांछित पृष्ठ पर जोड़ें।

```csharp
page.AppendChildLast(image);
```

## निष्कर्ष

बधाई हो! आपने .NET का उपयोग करके अपने Aspose.Note दस्तावेज़ में एक छवि सफलतापूर्वक सम्मिलित कर ली है। छवियाँ आपके दस्तावेज़ों के दृश्य प्रतिनिधित्व में उल्लेखनीय रूप से सुधार कर सकती हैं, जिससे वे अधिक आकर्षक और जानकारीपूर्ण बन सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं Aspose.Note दस्तावेज़ों में किसी भी प्रारूप की छवियां सम्मिलित कर सकता हूं?

A1: हाँ, Aspose.Note JPG, PNG, BMP, GIF, आदि सहित विभिन्न छवि प्रारूपों का समर्थन करता है।

### Q2: क्या सम्मिलित छवियों का प्रोग्रामेटिक रूप से आकार बदलना संभव है?

ए2: बिल्कुल! आप सम्मिलन के दौरान अपनी प्राथमिकताओं के अनुसार छवियों की चौड़ाई और ऊंचाई को समायोजित कर सकते हैं।

### Q3: क्या Aspose.Note छवि संरेखण को संशोधित करने के लिए विकल्प प्रदान करता है?

उ3: हाँ, आप छवियों को अपने दस्तावेज़ पृष्ठों के भीतर बाएँ, दाएँ या केंद्र में संरेखित कर सकते हैं।

### Q4: क्या मैं अपने दस्तावेज़ के एक पृष्ठ में एकाधिक छवियाँ सम्मिलित कर सकता हूँ?

ए4: निश्चित रूप से! Aspose.Note का उपयोग करके आप एक पृष्ठ पर जितनी चाहें उतनी छवियां सम्मिलित कर सकते हैं।

### Q5: क्या सम्मिलित की जा सकने वाली छवियों के फ़ाइल आकार की कोई सीमा है?

A5: Aspose.Note छवि फ़ाइल आकार पर सख्त सीमाएं नहीं लगाता है, लेकिन बेहतर प्रदर्शन के लिए छवियों को अनुकूलित करने की अनुशंसा की जाती है।
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
