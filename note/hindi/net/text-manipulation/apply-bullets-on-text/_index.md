---
title: Aspose.Note में टेक्स्ट पर बुलेट्स लागू करें
linktitle: Aspose.Note में टेक्स्ट पर बुलेट्स लागू करें
second_title: Aspose.Note .NET API
description: अपने OneNote दस्तावेज़ों को बेहतर बनाने के लिए .NET के लिए Aspose.Note में टेक्स्ट पर बुलेट्स लगाने का तरीका जानें। प्रभावी फ़ॉर्मेटिंग के लिए इस चरण-दर-चरण मार्गदर्शिका का पालन करें।
type: docs
weight: 10
url: /hi/net/text-manipulation/apply-bullets-on-text/
---
## परिचय
.NET के लिए Aspose.Note का उपयोग करके टेक्स्ट में बुलेट लगाने की इस चरण-दर-चरण मार्गदर्शिका में आपका स्वागत है। Aspose.Note एक शक्तिशाली लाइब्रेरी है जो डेवलपर्स को उनके .NET अनुप्रयोगों में Microsoft OneNote फ़ाइलों के साथ निर्बाध रूप से काम करने की अनुमति देती है। इस ट्यूटोरियल में, हम आपको टेक्स्ट में बुलेट्स लगाने, आपके OneNote दस्तावेज़ों की दृश्य अपील को बढ़ाने की प्रक्रिया के बारे में बताएंगे।
## आवश्यक शर्तें
इससे पहले कि हम ट्यूटोरियल में उतरें, सुनिश्चित करें कि आपके पास निम्नलिखित शर्तें हैं:
- C# और .NET प्रोग्रामिंग का बुनियादी ज्ञान।
-  .NET लाइब्रेरी के लिए Aspose.Note स्थापित किया गया। आप इसे डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/note/net/).
## नामस्थान आयात करें
अपने C# कोड में, आवश्यक नामस्थान शामिल करना सुनिश्चित करें:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## चरण 1: अपना दस्तावेज़ सेट करें
```csharp
// दस्तावेज़ निर्देशिका का पथ.
string dataDir = "Your Document Directory";
//दस्तावेज़ वर्ग का एक ऑब्जेक्ट बनाएं
Aspose.Note.Document doc = new Aspose.Note.Document();
```
## चरण 2: पृष्ठ और रूपरेखा प्रारंभ करें
```csharp
// पेज क्लास ऑब्जेक्ट को इनिशियलाइज़ करें
Aspose.Note.Page page = new Aspose.Note.Page(doc);
// आउटलाइन क्लास ऑब्जेक्ट को इनिशियलाइज़ करें
Outline outline = new Outline(doc);
```
## चरण 3: डिफ़ॉल्ट टेक्स्ट शैली सेट करें
```csharp
// टेक्स्टस्टाइल क्लास ऑब्जेक्ट को प्रारंभ करें और फ़ॉर्मेटिंग गुण सेट करें
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## चरण 4: बुलेट के साथ रूपरेखा तत्व बनाएं
```csharp
// आउटलाइनएलिमेंट क्लास ऑब्जेक्ट को प्रारंभ करें और बुलेट लागू करें
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("*", "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
// अन्य रूपरेखा तत्वों के लिए दोहराएँ
```
## चरण 5: रूपरेखा तत्वों को रूपरेखा में जोड़ें
```csharp
// रूपरेखा तत्व जोड़ें
outline.AppendChildLast(outlineElem1);
// अन्य रूपरेखा तत्वों के लिए दोहराएँ
```
## चरण 6: पृष्ठ पर रूपरेखा जोड़ें
```csharp
// आउटलाइन नोड जोड़ें
page.AppendChildLast(outline);
```
## चरण 7: दस्तावेज़ में पेज जोड़ें
```csharp
//पेज नोड जोड़ें
doc.AppendChildLast(page);
```
## चरण 8: OneNote दस्तावेज़ सहेजें
```csharp
// OneNote दस्तावेज़ सहेजें
dataDir = dataDir + "ApplyBulletsOnText_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nBullets applied successfully on a text.\nFile saved at " + dataDir); 
```
## निष्कर्ष
बधाई हो! आपने .NET के लिए Aspose.Note का उपयोग करके टेक्स्ट पर बुलेट्स लगाना सफलतापूर्वक सीख लिया है। यह सुविधा आपके OneNote दस्तावेज़ों के स्वरूपण को महत्वपूर्ण रूप से बढ़ा सकती है, जिससे वे अधिक आकर्षक बन सकते हैं।
## अक्सर पूछे जाने वाले प्रश्न
### क्या मैं सूची में प्रत्येक आइटम पर अलग-अलग बुलेट शैलियाँ लागू कर सकता हूँ?
 हाँ, आप बुलेट शैलियों को संशोधित करके अनुकूलित कर सकते हैं`NumberList` प्रत्येक के लिए गुण`OutlineElement`.
### क्या Aspose.Note Microsoft OneNote के नवीनतम संस्करण के साथ संगत है?
Aspose.Note Microsoft OneNote के विभिन्न संस्करणों का समर्थन करता है, जो पुराने और नए दोनों संस्करणों के साथ संगतता सुनिश्चित करता है।
### क्या मैं व्यावसायिक उद्देश्यों के लिए Aspose.Note का उपयोग कर सकता हूँ?
 हाँ, आप व्यावसायिक परियोजनाओं में .NET के लिए Aspose.Note का उपयोग कर सकते हैं। लाइसेंस प्राप्त करने के लिए, यहाँ जाएँ[यहाँ](https://purchase.aspose.com/buy).
### क्या .NET के लिए Aspose.Note का कोई परीक्षण संस्करण उपलब्ध है?
 हाँ, आप निःशुल्क परीक्षण डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/).
### मुझे अतिरिक्त सहायता और संसाधन कहां मिल सकते हैं?
 आप Aspose.Note सामुदायिक मंच पर जा सकते हैं[यहाँ](https://forum.aspose.com/c/note/28) समर्थन और चर्चा के लिए.