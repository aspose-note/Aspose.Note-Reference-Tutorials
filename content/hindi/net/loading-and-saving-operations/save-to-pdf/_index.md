---
title: Aspose.Note में PDF में सहेजें
linktitle: Aspose.Note में PDF में सहेजें
second_title: Aspose.Note .NET API
description: .NET के लिए Aspose.Note का उपयोग करके Microsoft OneNote दस्तावेज़ों को PDF प्रारूप में सहेजना सीखें। लेटर और ए4 पेज लेआउट के लिए कोड उदाहरणों के साथ चरण-दर-चरण ट्यूटोरियल।
type: docs
weight: 26
url: /hi/net/loading-and-saving-operations/save-to-pdf/
---
## परिचय

इस ट्यूटोरियल में, हम जानेंगे कि .NET के लिए Aspose.Note का उपयोग करके दस्तावेज़ों को पीडीएफ प्रारूप में कैसे सहेजा जाए। Aspose.Note एक शक्तिशाली लाइब्रेरी है जो डेवलपर्स को Microsoft OneNote फ़ाइलों के साथ प्रोग्रामेटिक रूप से काम करने में सक्षम बनाती है। हम आवश्यक शर्तें कवर करेंगे, नेमस्पेस आयात करेंगे, और विभिन्न पेज लेआउट में दस्तावेज़ों को पीडीएफ में सहेजने के लिए चरण-दर-चरण मार्गदर्शिकाएँ प्रदान करेंगे।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

- आपके सिस्टम पर विज़ुअल स्टूडियो स्थापित है।
-  .NET लाइब्रेरी के लिए Aspose.Note डाउनलोड और इंस्टॉल किया गया। आप इसे यहां से डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/note/net/).
- C# प्रोग्रामिंग भाषा का बुनियादी ज्ञान।

## नामस्थान आयात करें

सबसे पहले, आइए अपने C# कोड में आवश्यक नामस्थान आयात करें:

```csharp
using System;
using System.IO;

using Aspose.Note.Saving;
```

अब जब हमने आवश्यक शर्तें पूरी कर ली हैं और नेमस्पेस आयात कर लिया है, तो आइए अलग-अलग पेज लेआउट में दस्तावेज़ों को पीडीएफ में सहेजने के लिए आगे बढ़ें।

## चरण 1: पत्र पृष्ठ सेटिंग्स का उपयोग करके पीडीएफ में सहेजें


```csharp
public static void SaveToPdfUsingLetterPageSettings()
{
    // दस्तावेज़ निर्देशिका का पथ.
    string dataDir = "Your Document Directory";

    // दस्तावेज़ को Aspose.Note में लोड करें।
    Document oneFile = new Document(dataDir + "OneNote.one");

    var dst = Path.Combine(dataDir, "SaveToPdfUsingLetterPageSettings.pdf");

    // दस्तावेज़ सहेजें.
    oneFile.Save(dst, new PdfSaveOptions() { PageSettings = PageSettings.Letter });

    Console.WriteLine("\nOneNote document saved successfully.\nFile saved at " + dst);
}
```

### स्पष्टीकरण:

- हम OneNote दस्तावेज़ को Aspose.Note में लोड करते हैं।
- सहेजी गई पीडीएफ फ़ाइल के लिए गंतव्य पथ परिभाषित करें।
-  का उपयोग करके दस्तावेज़ को पीडीएफ में सहेजें`PdfSaveOptions` साथ`PageSettings` करने के लिए सेट`Letter`.

## चरण 2: ऊंचाई सीमा के बिना ए4 पेज सेटिंग्स का उपयोग करके पीडीएफ में सहेजें

```csharp
public static void SaveToPdfUsingA4PageSettingsWithoutHeightLimit()
{
    // दस्तावेज़ निर्देशिका का पथ.
    string dataDir = "Your Document Directory";

    // दस्तावेज़ को Aspose.Note में लोड करें।
    Document oneFile = new Document(dataDir + "OneNote.one");

    var dst = Path.Combine(dataDir, "SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf");

    // दस्तावेज़ सहेजें.
    oneFile.Save(dst, new PdfSaveOptions() { PageSettings = PageSettings.A4NoHeightLimit });

    Console.WriteLine("\nOneNote document saved successfully.\nFile saved at " + dst);
}
```

### स्पष्टीकरण:

- पिछले चरण के समान, हम OneNote दस्तावेज़ को Aspose.Note में लोड करते हैं।
- सहेजी गई पीडीएफ फ़ाइल के लिए गंतव्य पथ परिभाषित करें।
-  का उपयोग करके दस्तावेज़ को पीडीएफ में सहेजें`PdfSaveOptions` साथ`PageSettings` करने के लिए सेट`A4NoHeightLimit`.

## निष्कर्ष

इस ट्यूटोरियल में, हमने सीखा कि .NET के लिए Aspose.Note का उपयोग करके दस्तावेज़ों को पीडीएफ प्रारूप में कैसे सहेजा जाए। हमने दो अलग-अलग पेज लेआउट को कवर किया: लेटर और A4 बिना ऊंचाई की सीमा के। Aspose.Note के साथ, डेवलपर्स दस्तावेज़ प्रबंधन कार्यों में लचीलापन और दक्षता प्रदान करते हुए, OneNote फ़ाइलों को प्रोग्रामेटिक रूप से आसानी से हेरफेर कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Aspose.Note जटिल OneNote फ़ाइलों को संभाल सकता है?

A1: हाँ, Aspose.Note जटिल OneNote फ़ाइलों को प्रभावी ढंग से संभालने के लिए विभिन्न सुविधाओं और कार्यात्मकताओं का समर्थन करता है।

### Q2: क्या Aspose.Note व्यावसायिक परियोजनाओं के लिए उपयुक्त है?

 A2: बिल्कुल, Aspose.Note का उपयोग व्यावसायिक परियोजनाओं में आसानी से किया जा सकता है। आप लाइसेंस खरीद सकते हैं[यहाँ](https://purchase.aspose.com/buy).

### Q3: क्या Aspose.Note निःशुल्क परीक्षण की पेशकश करता है?

 उ3: हां, आप नि:शुल्क परीक्षण के साथ Aspose.Note को एक्सप्लोर कर सकते हैं[यहाँ](https://releases.aspose.com/).

### Q4: मुझे Aspose.Note के लिए दस्तावेज़ कहां मिल सकते हैं?

 A4: आप विस्तृत दस्तावेज़ पा सकते हैं[यहाँ](https://reference.aspose.com/note/net/).

### Q5: अतिरिक्त सहायता की आवश्यकता है?

 A5: बेझिझक कोई भी प्रश्न पूछें या Aspose.Note फोरम पर समर्थन मांगें[यहाँ](https://forum.aspose.com/c/note/28).