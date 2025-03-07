---
title: Aspose.Note टेक्स्ट में बुलेट या नंबर सूची पुनः प्राप्त करें
linktitle: Aspose.Note टेक्स्ट में बुलेट या नंबर सूची पुनः प्राप्त करें
second_title: Aspose.Note .NET API
description: बुलेट या संख्या सूचियाँ पुनर्प्राप्त करने पर हमारे चरण-दर-चरण मार्गदर्शिका के साथ .NET के लिए Aspose.Note की क्षमता को अनलॉक करें। अपने OneNote दस्तावेज़ हेरफेर कौशल को उन्नत करें!
weight: 23
url: /hi/net/text-manipulation/retrieve-bullet-number-list/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note टेक्स्ट में बुलेट या नंबर सूची पुनः प्राप्त करें

## परिचय
.NET के लिए Aspose.Note की दुनिया में आपका स्वागत है, एक मजबूत और बहुमुखी लाइब्रेरी जो डेवलपर्स को OneNote दस्तावेज़ हेरफेर को सहजता से संभालने में सक्षम बनाती है। इस ट्यूटोरियल में, हम .NET के लिए Aspose.Note का उपयोग करके बुलेट या नंबर सूचियों को पुनर्प्राप्त करने की प्रक्रिया के बारे में विस्तार से जानेंगे। चाहे आप एक अनुभवी डेवलपर हों या कोडिंग के शौकीन हों, यह मार्गदर्शिका आपको Aspose.Note में सूचियों के साथ काम करने की जटिलताओं के माध्यम से नेविगेट करने के ज्ञान से लैस करेगी।
## आवश्यक शर्तें
इससे पहले कि हम इस कोडिंग यात्रा को शुरू करें, सुनिश्चित करें कि आपके पास निम्नलिखित शर्तें हैं:
-  .NET के लिए Aspose.Note: सुनिश्चित करें कि आपके पास Aspose.Note लाइब्रेरी स्थापित है। यदि नहीं, तो आप इसे यहां से डाउनलोड कर सकते हैं[.NET दस्तावेज़ीकरण के लिए Aspose.Note](https://reference.aspose.com/note/net/).
- विकास परिवेश: अपनी मशीन पर एक कार्यशील विकास परिवेश स्थापित करें, अधिमानतः Microsoft Visual Studio।
- C# का बुनियादी ज्ञान: C# से खुद को परिचित करें क्योंकि यह ट्यूटोरियल इसी भाषा में लिखा गया है।
## नामस्थान आयात करें
.NET के लिए Aspose.Note के साथ इंटरैक्ट करने के लिए, आपको अपने प्रोजेक्ट में आवश्यक नेमस्पेस आयात करने की आवश्यकता है। अपने कोड की शुरुआत में निम्नलिखित नामस्थान शामिल करें:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
```
अब, आइए चरण दर चरण बुलेट या संख्या सूचियों को पुनः प्राप्त करने की प्रक्रिया को तोड़ें:
## चरण 1: अपनी दस्तावेज़ निर्देशिका सेट करें
```csharp
// दस्तावेज़ निर्देशिका का पथ.
string dataDir = "Your Document Directory";
```
 प्रतिस्थापित करें`"Your Document Directory"` उस वास्तविक पथ के साथ जहां आपका Aspose.Note दस्तावेज़ स्थित है।
## चरण 2: दस्तावेज़ लोड करें
```csharp
// दस्तावेज़ को Aspose.Note में लोड करें।
Document oneFile = new Document(dataDir + "ApplyNumberingOnText.one");
```
 सुनिश्चित करें कि आप प्रतिस्थापित करें`"ApplyNumberingOnText.one"` आपके विशिष्ट OneNote दस्तावेज़ के नाम के साथ।
## चरण 3: नोड्स का संग्रह पुनः प्राप्त करें
```csharp
// रूपरेखा तत्व के नोड्स का संग्रह पुनः प्राप्त करें।
IList<OutlineElement> nodes = oneFile.GetChildNodes<OutlineElement>();
```
यह चरण लोड किए गए दस्तावेज़ से रूपरेखा नोड्स का एक संग्रह पुनर्प्राप्त करता है।
## चरण 4: प्रत्येक नोड के माध्यम से पुनरावृति करें
```csharp
// प्रत्येक नोड के माध्यम से पुनरावृति करें.
foreach (OutlineElement node in nodes)
{
    if (node.NumberList != null)
    {
        NumberList list = node.NumberList;
        // अगले चरणों पर जारी रखें...
    }
}
```
यह लूप सुनिश्चित करता है कि हम केवल उन नोड्स के साथ काम कर रहे हैं जिनमें एक संख्या सूची है।
## चरण 5: फ़ॉन्ट जानकारी पुनः प्राप्त करें
```csharp
// फ़ॉन्ट नाम पुनः प्राप्त करें
Console.WriteLine("Font Name: " + list.Font);
// फ़ॉन्ट लंबाई पुनः प्राप्त करें
Console.WriteLine("Font Length: " + list.Font.Length);
// फ़ॉन्ट आकार पुनः प्राप्त करें
Console.WriteLine("Font Size: " + list.FontSize);
// फ़ॉन्ट रंग पुनः प्राप्त करें
Console.WriteLine("Font Color: " + list.FontColor);
// प्रारूप पुनः प्राप्त करें
Console.WriteLine("Font format: " + list.Format);
// बोल्ड चेक करें
Console.WriteLine("Is bold: " + list.IsBold);
// इटैलिक जांचें
Console.WriteLine("Is italic: " + list.IsItalic);
Console.WriteLine();
```
कोड की ये पंक्तियाँ संख्या सूची से विभिन्न फ़ॉन्ट-संबंधित जानकारी निकालती हैं।
## निष्कर्ष
 बधाई हो! आपने सफलतापूर्वक सीख लिया है कि .NET के लिए Aspose.Note का उपयोग करके बुलेट या संख्या सूचियाँ कैसे प्राप्त की जाती हैं। जैसे ही आप अपना अन्वेषण जारी रखें, देखें[प्रलेखन](https://reference.aspose.com/note/net/) अधिक गहन अंतर्दृष्टि और कार्यप्रणाली के लिए।
## अक्सर पूछे जाने वाले प्रश्न
### क्या मैं अन्य प्रोग्रामिंग भाषाओं के साथ .NET के लिए Aspose.Note का उपयोग कर सकता हूँ?
Aspose.Note मुख्य रूप से .NET का समर्थन करता है, लेकिन विभिन्न प्लेटफार्मों और भाषाओं के लिए तैयार लाइब्रेरी के अन्य संस्करण भी हैं।
### क्या Aspose.Note नवीनतम OneNote प्रारूपों के साथ संगत है?
हां, Aspose.Note नवीनतम संस्करणों के साथ संगतता सुनिश्चित करते हुए, OneNote प्रारूपों की एक विस्तृत श्रृंखला का समर्थन करता है।
### मैं Aspose.Note के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूँ?
 मिलने जाना[इस लिंक](https://purchase.aspose.com/temporary-license/) मूल्यांकन उद्देश्यों के लिए अस्थायी लाइसेंस प्राप्त करना।
### Aspose.Note उपयोगकर्ताओं के लिए कौन से समर्थन विकल्प उपलब्ध हैं?
आप इसका अन्वेषण कर सकते हैं और सहायता प्राप्त कर सकते हैं[Aspose.नोट फोरम](https://forum.aspose.com/c/note/28) आपके सामने आने वाले किसी भी प्रश्न या समस्या के लिए।
### क्या .NET के लिए Aspose.Note का कोई निःशुल्क परीक्षण संस्करण है?
 हां, आप .NET के लिए Aspose.Note के निःशुल्क परीक्षण संस्करण तक पहुंच सकते हैं[यहाँ](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
