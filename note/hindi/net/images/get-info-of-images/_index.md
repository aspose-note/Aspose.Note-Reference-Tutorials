---
date: 2026-04-09
description: Aspose.Note for .NET के साथ OneNote फ़ाइलों से इमेज मेटाडेटा निकालना
  और इमेज के आयाम प्राप्त करना सीखें। C# डेवलपर्स के लिए चरण‑दर‑चरण गाइड।
keywords:
- extract image metadata
- how to extract images
- get image dimensions
- load onenote document
- c# get image properties
linktitle: Aspose.Note का उपयोग करके OneNote से इमेज मेटाडेटा कैसे निकालें
second_title: Aspose.Note .NET API
title: Aspose.Note का उपयोग करके OneNote से इमेज मेटाडाटा कैसे निकालें
url: /hi/net/images/get-info-of-images/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note for .NET के साथ इमेज मेटाडाटा निकालें

इस व्यावहारिक ट्यूटोरियल में आप **इमेज मेटाडाटा कैसे निकालें** सीखेंगे—जिसमें चौड़ाई, ऊँचाई, मूल आकार, फ़ाइल नाम, और संशोधन समय शामिल हैं—Microsoft OneNote फ़ाइलों से Aspose.Note लाइब्रेरी का उपयोग करके C# में। चाहे आपको इमेज थंबनेल दिखाने हों, इमेज आकार की वैधता जाँचनी हो, या एम्बेडेड एसेट्स का कैटलॉग बनाना हो, इस जानकारी को प्रोग्रामेटिकली निकालने से अनगिनत मैन्युअल कदम बचते हैं।

## त्वरित उत्तर
- **“इमेज मेटाडाटा निकालना” का क्या अर्थ है?** OneNote दस्तावेज़ के भीतर संग्रहीत इमेजों से आयाम, फ़ाइल नाम, और टाइमस्टैम्प जैसी प्रॉपर्टीज़ प्राप्त करना।  
- **कौन सी लाइब्रेरी इसे संभालती है?** Aspose.Note for .NET।  
- **क्या लाइसेंस की जरूरत है?** विकास के लिए फ्री ट्रायल काम करता है; प्रोडक्शन के लिए कमर्शियल लाइसेंस आवश्यक है।  
- **समर्थित प्लेटफ़ॉर्म?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6+।  
- **सामान्य रनटाइम?** एक मानक .one फ़ाइल के लिए एक सेकंड से कम।

## इमेज मेटाडाटा निकालना क्या है?
इमेज मेटाडाटा निकालना मतलब प्रोग्रामेटिकली प्रत्येक इमेज ऑब्जेक्ट के साथ जुड़े वर्णनात्मक गुण (चौड़ाई, ऊँचाई, मूल आयाम, फ़ाइल नाम, अंतिम‑संशोधित समय आदि) पढ़ना। यह डेटा वैधता, रिपोर्टिंग, या आगे की इमेज प्रोसेसिंग के लिए उपयोगी है।

## OneNote से इमेज मेटाडाटा क्यों निकालें?
- **ऑटोमेशन** – ऐसे टूल बनाएं जो स्वचालित रूप से इमेज इन्वेंट्री जनरेट करें।  
- **वैधता** – प्रकाशित करने से पहले इमेज आकार आवश्यकताओं को पूरा करती हैं या नहीं, सुनिश्चित करें।  
- **इंटीग्रेशन** – OneNote सामग्री को अन्य सिस्टम (CMS, DAM आदि) के साथ जोड़ें जिन्हें इमेज विवरण चाहिए।  
- **परफ़ॉर्मेंस** – केवल आयाम चाहिए हों तो पूरे इमेज बाइनरी लोड करने से बचें।

## पूर्वापेक्षाएँ
1. **C# मूलभूत ज्ञान** – आपको बेसिक C# कोड लिखने में सहज होना चाहिए।  
2. **Aspose.Note for .NET** – आधिकारिक साइट से लाइब्रेरी डाउनलोड और इंस्टॉल करें [here](https://releases.aspose.com/note/net/)।  
3. **एक OneNote (.one) फ़ाइल** – कोई भी मौजूदा OneNote दस्तावेज़ जिसमें इमेज हों।

## नेमस्पेस इम्पोर्ट करें
शुरू करने से पहले, आवश्यक नेमस्पेस इम्पोर्ट करें:

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System;
```

## चरण 1: OneNote दस्तावेज़ लोड करें
पहले, लक्ष्य OneNote फ़ाइल को `Aspose.Note.Document` ऑब्जेक्ट में लोड करें। यह **load onenote document** चरण API को आगे की क्वेरीज़ के लिए तैयार करता है।

```csharp
// The path to the documents directory.
string dataDir = "Your Document Directory";

// Load the document into Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

`"Your Document Directory"` को उस वास्तविक फ़ोल्डर से बदलें जहाँ आपकी `.one` फ़ाइल स्थित है।

## चरण 2: सभी इमेज नोड्स प्राप्त करें
अब हम **how to extract images** करके दस्तावेज़ से प्रत्येक `Image` नोड निकालेंगे।

```csharp
// Get all Image nodes
IList<Aspose.Note.Image> images = oneFile.GetChildNodes<Aspose.Note.Image>();
```

`GetChildNodes<T>()` मेथड पूरे नोटबुक पदानुक्रम को स्कैन करता है और इमेज ऑब्जेक्ट्स का संग्रह लौटाता है।

## चरण 3: प्रत्येक इमेज पर इटररेट करें और **c# इमेज प्रॉपर्टीज़ प्राप्त करें**
हम संग्रह पर लूप करेंगे और मेटाडाटा प्रिंट करेंगे, जिसमें **get image dimensions** और **extract original image size** मान शामिल हैं।

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

आउटपुट प्रत्येक इमेज की वर्तमान चौड़ाई/ऊँचाई (पेज में रेंडर की गई), फ़ाइल में संग्रहीत मूल आयाम, फ़ाइल नाम, और अंतिम संशोधन का टाइमस्टैम्प दिखाता है।

## सामान्य समस्याएँ और समाधान
| समस्या | कारण | समाधान |
|-------|--------|-----|
| **NullReferenceException** जब `images` खाली हो | दस्तावेज़ में कोई इमेज नहीं है | सुनिश्चित करें कि स्रोत `.one` फ़ाइल में वास्तव में एम्बेडेड इमेज हैं। |
| **गलत आयाम** | इमेजेज़ OneNote में स्केल की गई हैं | सही आकार प्राप्त करने के लिए `OriginalWidth`/`OriginalHeight` का उपयोग करें। |
| **FileName खाली है** | इमेज क्लिपबोर्ड से पेस्ट की गई थी | API के पास फ़ाइलनाम नहीं हो सकता; अपने कोड में `null` या खाली स्ट्रिंग्स को संभालें। |

## अक्सर पूछे जाने वाले प्रश्न

**प्रश्न: क्या Aspose.Note सभी Microsoft OneNote संस्करणों के साथ संगत है?**  
**उत्तर:** Aspose.Note .one, .onepkg, और .onetoc2 फ़ॉर्मैट्स को सपोर्ट करता है, जो 2007 से आगे के अधिकांश OneNote संस्करणों को कवर करता है।

**प्रश्न: क्या मैं निकाले जाने के बाद इमेज प्रॉपर्टीज़ को संशोधित कर सकता हूँ?**  
**उत्तर:** हाँ, आप `Width`, `Height`, या `FileName` जैसी प्रॉपर्टीज़ बदल सकते हैं और फिर दस्तावेज़ को सहेज सकते हैं।

**प्रश्न: क्या Aspose.Note .NET Core के साथ काम करता है?**  
**उत्तर:** बिल्कुल। लाइब्रेरी पूरी तरह से .NET Core, .NET 5, और .NET 6 के साथ संगत है।

**प्रश्न: क्या कोई मुफ्त ट्रायल उपलब्ध है?**  
**उत्तर:** हाँ, आप Aspose वेबसाइट से ट्रायल संस्करण डाउनलोड करके सभी फीचर्स का अन्वेषण कर सकते हैं।

**प्रश्न: अतिरिक्त सहायता या समुदाय समर्थन कहाँ प्राप्त कर सकते हैं?**  
**उत्तर:** टिप्स, सैंपल कोड, और समुदाय के उत्तरों के लिए Aspose.Note फ़ोरम [here](https://forum.aspose.com/c/note/28) देखें।

---

**अंतिम अपडेट:** 2026-04-09  
**परीक्षित संस्करण:** Aspose.Note 24.11 for .NET  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}