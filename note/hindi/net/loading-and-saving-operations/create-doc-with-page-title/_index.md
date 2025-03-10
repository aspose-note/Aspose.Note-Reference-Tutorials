---
title: Aspose.Note में पृष्ठ शीर्षक के साथ दस्तावेज़ बनाएँ
linktitle: Aspose.Note में पृष्ठ शीर्षक के साथ दस्तावेज़ बनाएँ
second_title: Aspose.Note .NET API
description: .NET के लिए Aspose.Note का उपयोग करके शीर्षक वाले पृष्ठों वाले दस्तावेज़ बनाना सीखें। निर्बाध एकीकरण के लिए हमारी चरण-दर-चरण मार्गदर्शिका का पालन करें।
weight: 13
url: /hi/net/loading-and-saving-operations/create-doc-with-page-title/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note में पृष्ठ शीर्षक के साथ दस्तावेज़ बनाएँ

## परिचय

इस ट्यूटोरियल में, हम .NET के लिए Aspose.Note का उपयोग करके शीर्षक वाले पृष्ठ के साथ एक दस्तावेज़ बनाने की प्रक्रिया में आपका मार्गदर्शन करेंगे। Aspose.Note एक शक्तिशाली API है जो डेवलपर्स को Microsoft OneNote फ़ाइलों के साथ प्रोग्रामेटिक रूप से काम करने की अनुमति देता है।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ स्थापित और सेटअप हैं:

### विजुअल स्टूडियो इंस्टालेशन

1. विज़ुअल स्टूडियो डाउनलोड करें: यदि आपने पहले से नहीं किया है, तो Microsoft वेबसाइट से विज़ुअल स्टूडियो डाउनलोड और इंस्टॉल करें।

2. .NET डेवलपमेंट वर्कलोड इंस्टॉल करें: इंस्टॉलेशन प्रक्रिया के दौरान, यह सुनिश्चित करने के लिए कि आपके पास .NET डेवलपमेंट के लिए सभी आवश्यक घटक हैं, ".NET डेस्कटॉप डेवलपमेंट" वर्कलोड का चयन करना सुनिश्चित करें।

3. एक नया प्रोजेक्ट बनाएं: विज़ुअल स्टूडियो खोलें और एक नया प्रोजेक्ट बनाएं (कंसोल एप्लिकेशन या कोई अन्य प्रकार जिसे आप पसंद करते हैं)।

### Aspose.नोट स्थापना

1.  Aspose.Note प्राप्त करें: .NET लाइब्रेरी के लिए Aspose.Note डाउनलोड करें[वेबसाइट](https://releases.aspose.com/note/net/).

2. NuGet के माध्यम से Aspose.Note इंस्टॉल करें: वैकल्पिक रूप से, आप विजुअल स्टूडियो में NuGet पैकेज मैनेजर के माध्यम से .NET के लिए Aspose.Note इंस्टॉल कर सकते हैं। बस "Aspose.Note" खोजें और नवीनतम संस्करण इंस्टॉल करें।

## नामस्थान आयात करना

सबसे पहले, आपको अपने प्रोजेक्ट में Aspose.Note का उपयोग करने के लिए आवश्यक नामस्थान आयात करने की आवश्यकता है।

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Drawing;
using System.Globalization;
```

अब, आइए पृष्ठ शीर्षक के साथ दस्तावेज़ बनाने की प्रक्रिया को कई चरणों में विभाजित करें:

## चरण 1: एक दस्तावेज़ ऑब्जेक्ट बनाएँ

```csharp
//दस्तावेज़ वर्ग का एक ऑब्जेक्ट बनाएं
Document doc = new Aspose.Note.Document();
```

## चरण 2: पेज क्लास ऑब्जेक्ट को आरंभ करें

```csharp
// पेज क्लास ऑब्जेक्ट को इनिशियलाइज़ करें
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## चरण 3: टेक्स्ट के लिए डिफ़ॉल्ट शैली सेट करें

```csharp
// दस्तावेज़ में सभी टेक्स्ट के लिए डिफ़ॉल्ट शैली.
ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```

## चरण 4: पृष्ठ शीर्षक गुण सेट करें

```csharp
// पृष्ठ शीर्षक गुण सेट करें
page.Title = new Title(doc)
{
    TitleText = new RichText(doc) { Text = "Title text.", ParagraphStyle = textStyle },
    TitleDate = new RichText(doc) { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
    TitleTime = new RichText(doc) { Text = "12:34", ParagraphStyle = textStyle }
};
```

## चरण 5: दस्तावेज़ में पेज नोड जोड़ें

```csharp
// दस्तावेज़ में पेज नोड जोड़ें
doc.AppendChildLast(page);
```

## चरण 6: OneNote दस्तावेज़ सहेजें

```csharp
// OneNote दस्तावेज़ सहेजें
string dataDir = "Your Document Directory";
dataDir = dataDir + "CreateDocWithPageTitle_out.one";
doc.Save(dataDir);
```

## निष्कर्ष

बधाई हो! आपने .NET के लिए Aspose.Note का उपयोग करके शीर्षक वाले पृष्ठ के साथ सफलतापूर्वक एक दस्तावेज़ बनाया है। यह ट्यूटोरियल आपको OneNote फ़ाइलों को प्रोग्रामेटिक रूप से प्रबंधित करने के लिए Aspose.Note को अपने .NET अनुप्रयोगों में एकीकृत करने में मदद करने के लिए चरण-दर-चरण मार्गदर्शिका प्रदान करता है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं शीर्षक पाठ शैली को अनुकूलित कर सकता हूँ?

A1: हाँ, आप अपनी आवश्यकताओं के अनुसार शीर्षक पाठ के फ़ॉन्ट रंग, फ़ॉन्ट नाम और फ़ॉन्ट आकार को अनुकूलित कर सकते हैं।

### Q2: क्या Aspose.Note .NET कोर के साथ संगत है?

A2: हां, Aspose.Note .NET कोर का समर्थन करता है, जिससे आप क्रॉस-प्लेटफ़ॉर्म एप्लिकेशन विकसित कर सकते हैं।

### Q3: क्या मैं दस्तावेज़ में चित्र और अनुलग्नक जोड़ सकता हूँ?

उ3: बिल्कुल! Aspose.Note आपके OneNote दस्तावेज़ों में छवियाँ, अनुलग्नक और अन्य तत्व निर्बाध रूप से जोड़ने के लिए API प्रदान करता है।

### Q4: क्या Aspose.Note मौजूदा OneNote फ़ाइलों को पढ़ने का समर्थन करता है?

A4: हां, आप मौजूदा OneNote फ़ाइलों को आसानी से पढ़ने, संशोधित करने और हेरफेर करने के लिए Aspose.Note का उपयोग कर सकते हैं।

### Q5: यदि मुझे कोई समस्या आती है तो मुझे सहायता कहां मिल सकती है?

 A5: आप इस पर समर्थन और सहायता पा सकते हैं[Aspose.नोट फोरम](https://forum.aspose.com/c/note/28), जहां विशेषज्ञ और समुदाय के सदस्य आपके प्रश्नों में आपकी सहायता कर सकते हैं।
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
