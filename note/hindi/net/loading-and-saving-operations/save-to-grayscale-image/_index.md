---
title: Aspose.Note में ग्रेस्केल छवि में सहेजें
linktitle: Aspose.Note में ग्रेस्केल छवि में सहेजें
second_title: Aspose.Note .NET API
description: .NET के लिए Aspose.Note का उपयोग करके OneNote दस्तावेज़ों को ग्रेस्केल छवियों के रूप में सहेजना सीखें। कुशल दस्तावेज़ प्रसंस्करण के लिए इस व्यापक ट्यूटोरियल का पालन करें।
weight: 24
url: /hi/net/loading-and-saving-operations/save-to-grayscale-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note में ग्रेस्केल छवि में सहेजें

## परिचय

इस ट्यूटोरियल में, हम यह पता लगाएंगे कि किसी दस्तावेज़ को ग्रेस्केल छवि के रूप में सहेजने के लिए .NET के लिए Aspose.Note का उपयोग कैसे करें। Aspose.Note एक शक्तिशाली लाइब्रेरी है जो डेवलपर्स को कार्यात्मकताओं की एक विस्तृत श्रृंखला प्रदान करते हुए, Microsoft OneNote फ़ाइलों के साथ प्रोग्रामेटिक रूप से काम करने की अनुमति देती है।

## आवश्यक शर्तें

आगे बढ़ने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित शर्तें हैं:

- C# प्रोग्रामिंग भाषा की बुनियादी समझ।
- आपके सिस्टम पर विज़ुअल स्टूडियो स्थापित है।
-  .NET लाइब्रेरी के लिए Aspose.Note स्थापित किया गया। आप इसे डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/note/net/).
- .NET का उपयोग करके फ़ाइलों तक पहुँचने और उनमें हेरफेर करने से परिचित होना।

## नामस्थान आयात करें

आइए आवश्यक नामस्थान आयात करके प्रारंभ करें:

```csharp
using System;

using Aspose.Note.Saving;

```

## चरण 1: दस्तावेज़ लोड करें

सबसे पहले, दस्तावेज़ को Aspose.Note में लोड करें। 

```csharp
string dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## चरण 2: ग्रेस्केल छवि के रूप में सहेजें

इसके बाद, ग्रेस्केल छवि को सहेजने के लिए पथ निर्दिष्ट करें और तदनुसार दस्तावेज़ को सहेजें।

```csharp
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
oneFile.Save(dataDir, new ImageSaveOptions(SaveFormat.Png)
					  {
						  ColorMode = ColorMode.GrayScale
					  });
```

## चरण 3: सत्यापित करें और परिणाम प्रदर्शित करें

अंत में, फ़ाइल पथ के साथ सफल रूपांतरण संदेश को सत्यापित और प्रदर्शित करें।

```csharp
Console.WriteLine("\nOneNote document converted successfully to grayscale image.\nFile saved at " + dataDir);
```

## निष्कर्ष

इस ट्यूटोरियल में, हमने सीखा कि किसी दस्तावेज़ को ग्रेस्केल छवि में बदलने के लिए .NET के लिए Aspose.Note का उपयोग कैसे करें। इन सरल चरणों का पालन करके, डेवलपर्स अपनी दस्तावेज़ प्रसंस्करण क्षमताओं को बढ़ाते हुए, इस कार्यक्षमता को अपने अनुप्रयोगों में कुशलतापूर्वक शामिल कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Aspose.Note जटिल OneNote फ़ाइलों को संभाल सकता है?

A1: हां, Aspose.Note जटिल OneNote फ़ाइलों को कुशलतापूर्वक संभाल सकता है, दस्तावेज़ हेरफेर के लिए मजबूत कार्यक्षमता प्रदान कर सकता है।

### Q2: क्या Aspose.Note विभिन्न फ़ाइल स्वरूपों के साथ संगत है?

A2: बिल्कुल, Aspose.Note दस्तावेज़ प्रसंस्करण में लचीलापन सुनिश्चित करते हुए, विभिन्न फ़ाइल स्वरूपों का समर्थन करता है।

### Q3: क्या Aspose.Note डेवलपर्स के लिए समर्थन प्रदान करता है?

उ3: हाँ, डेवलपर्स एस्पोज़ फ़ोरम और दस्तावेज़ीकरण के माध्यम से व्यापक समर्थन प्राप्त कर सकते हैं।

### Q4: क्या मैं खरीदने से पहले Aspose.Note आज़मा सकता हूँ?

A4: हाँ, आप Aspose.Note को उनकी वेबसाइट पर उपलब्ध निःशुल्क परीक्षण के माध्यम से एक्सप्लोर कर सकते हैं।

### Q5: मैं Aspose.Note के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?

A5: आप दिए गए लिंक पर जाकर और निर्देशों का पालन करके Aspose.Note के लिए एक अस्थायी लाइसेंस प्राप्त कर सकते हैं।
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
