---
title: Aspose.Note टेक्स्ट में चीनी नंबर सूची डालें
linktitle: Aspose.Note टेक्स्ट में चीनी नंबर सूची डालें
second_title: Aspose.Note .NET API
description: जानें कि .NET दस्तावेज़ों के लिए Aspose.Note में आसानी से चीनी नंबर सूचियाँ कैसे सम्मिलित करें। इस चरण-दर-चरण मार्गदर्शिका के साथ अपने दस्तावेज़ स्वरूपण कौशल को उन्नत करें।
weight: 20
url: /hi/net/text-manipulation/insert-chinese-number-list/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note टेक्स्ट में चीनी नंबर सूची डालें

## परिचय
क्या आप अपने दस्तावेज़ों में चीनी नंबर सूचियों को शामिल करके .NET कौशल के लिए अपने Aspose.Note को बढ़ाना चाह रहे हैं? यदि हां, तो आप सही जगह पर हैं! इस ट्यूटोरियल में, हम आपको .NET के लिए Aspose.Note का उपयोग करके चीनी नंबर सूचियाँ सम्मिलित करने की प्रक्रिया के बारे में बताएंगे। यह शक्तिशाली लाइब्रेरी आपको OneNote दस्तावेज़ों में निर्बाध रूप से हेरफेर करने की अनुमति देती है।
## आवश्यक शर्तें
इससे पहले कि हम ट्यूटोरियल में उतरें, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:
- सी# प्रोग्रामिंग का बुनियादी ज्ञान।
-  .NET के लिए Aspose.Note स्थापित। आप इसे डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/note/net/).
## नामस्थान आयात करें
आरंभ करने के लिए, अपने प्रोजेक्ट में आवश्यक नामस्थान आयात करें:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## चरण 1: OneNote दस्तावेज़ प्रारंभ करें
```csharp
string dataDir = "Your Document Directory";
Aspose.Note.Document doc = new Aspose.Note.Document();
```
## चरण 2: OneNote पृष्ठ प्रारंभ करें
```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
Outline outline = new Outline(doc);
```
## चरण 3: टेक्स्ट स्टाइल सेटिंग्स लागू करें
```csharp
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## चरण 4: रूपरेखा तत्व बनाएं
अब, आइए चीनी संख्या सूचियों के साथ तीन रूपरेखा तत्व बनाएं:
### चरण 4.1: पहला तत्व
```csharp
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
```
### चरण 4.2: दूसरा तत्व
```csharp
OutlineElement outlineElem2 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text2 = new RichText(doc) { Text = "Second", ParagraphStyle = defaultStyle };
outlineElem2.AppendChildLast(text2);
```
### चरण 4.3: तीसरा तत्व
```csharp
OutlineElement outlineElem3 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text3 = new RichText(doc) { Text = "Third", ParagraphStyle = defaultStyle };
outlineElem3.AppendChildLast(text3);
```
## चरण 5: तत्वों को रूपरेखा में जोड़ें
```csharp
outline.AppendChildLast(outlineElem1);
outline.AppendChildLast(outlineElem2);
outline.AppendChildLast(outlineElem3);
```
## चरण 6: पृष्ठ पर रूपरेखा जोड़ें
```csharp
page.AppendChildLast(outline);
```
## चरण 7: पृष्ठ को दस्तावेज़ में जोड़ें
```csharp
doc.AppendChildLast(page);
```
## चरण 8: OneNote दस्तावेज़ सहेजें
```csharp
dataDir = dataDir + "InsertChineseNumberList_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nChinese number list inserted successfully.\nFile saved at " + dataDir);
```
बधाई हो! आपने .NET लाइब्रेरी का उपयोग करके अपने Aspose.Note दस्तावेज़ में चीनी नंबर सूचियाँ सफलतापूर्वक सम्मिलित कर ली हैं।
## निष्कर्ष
इस ट्यूटोरियल में, हमने .NET दस्तावेज़ों के लिए आपके Aspose.Note में चीनी नंबर सूचियों को शामिल करने की चरण-दर-चरण प्रक्रिया को कवर किया है। अपने दस्तावेज़ स्वरूपण कौशल को बढ़ाएं और इन तकनीकों के साथ अपनी सामग्री को अधिक आकर्षक बनाएं।
## पूछे जाने वाले प्रश्न
### प्रश्न: क्या मैं चीनी संख्या सूचियों के स्वरूपण को अनुकूलित कर सकता हूँ?
 उ: हाँ, आप पैरामीटर्स को समायोजित करके फ़ॉर्मेटिंग को अनुकूलित कर सकते हैं`NumberList` निर्माता.
### प्रश्न: क्या Aspose.Note .NET के नवीनतम संस्करण के साथ संगत है?
उत्तर: हां, Aspose.Note को .NET के नवीनतम संस्करणों का समर्थन करने के लिए नियमित रूप से अपडेट किया जाता है।
### प्रश्न: मुझे अतिरिक्त उदाहरण और दस्तावेज कहां मिल सकते हैं?
ए: व्यापक का अन्वेषण करें[Aspose.नोट दस्तावेज़ीकरण](https://reference.aspose.com/note/net/).
### प्रश्न: मैं Aspose.Note के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?
 उत्तर: एक अस्थायी लाइसेंस प्राप्त करें[यहाँ](https://purchase.aspose.com/temporary-license/).
### प्रश्न: मैं कहां सहायता मांग सकता हूं या Aspose.Note से संबंधित प्रश्नों पर चर्चा कर सकता हूं?
 ए: पर जाएँ[Aspose.नोट समर्थन मंच](https://forum.aspose.com/c/note/28) सामुदायिक समर्थन के लिए.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
