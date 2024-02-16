---
title: Aspose.Note में टेक्स्ट पर नंबरिंग लागू करें
linktitle: Aspose.Note में टेक्स्ट पर नंबरिंग लागू करें
second_title: Aspose.Note .NET API
description: इस व्यापक ट्यूटोरियल के साथ जानें कि .NET के लिए Aspose.Note में टेक्स्ट नंबरिंग कैसे लागू करें। अपने दस्तावेज़ स्वरूपण को सहजता से बढ़ाएँ।
type: docs
weight: 12
url: /hi/net/text-manipulation/apply-numbering-on-text/
---
## परिचय
.NET के लिए Aspose.Note C# अनुप्रयोगों में दस्तावेज़ हेरफेर के लिए शक्तिशाली उपकरण प्रदान करता है। इस ट्यूटोरियल में, हम Aspose.Note का उपयोग करके टेक्स्ट पर नंबरिंग लागू करने की प्रक्रिया का पता लगाएंगे। अपने दस्तावेज़ स्वरूपण को सहजता से बढ़ाने के लिए इन चरण-दर-चरण निर्देशों का पालन करें।
## आवश्यक शर्तें
ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:
- C# प्रोग्रामिंग भाषा की बुनियादी समझ।
-  .NET के लिए Aspose.Note स्थापित। आप इसे डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/note/net/).
- एक एकीकृत विकास वातावरण (आईडीई) जैसे विजुअल स्टूडियो।
## नामस्थान आयात करें
आरंभ करने के लिए, अपने C# प्रोजेक्ट में आवश्यक नामस्थान आयात करना सुनिश्चित करें:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## चरण 1: अपना दस्तावेज़ सेट करें
एक नया दस्तावेज़ बनाकर और आवश्यक ऑब्जेक्ट प्रारंभ करके प्रारंभ करें:
```csharp
// दस्तावेज़ निर्देशिका का पथ.
string dataDir = "Your Document Directory";
//दस्तावेज़ वर्ग का एक ऑब्जेक्ट बनाएं
Document doc = new Document();
// पेज क्लास ऑब्जेक्ट को इनिशियलाइज़ करें
Aspose.Note.Page page = new Aspose.Note.Page(doc);
// आउटलाइन क्लास ऑब्जेक्ट को इनिशियलाइज़ करें
Outline outline = new Outline(doc);
```
## चरण 2: डिफ़ॉल्ट शैली को परिभाषित करें
पैराग्राफ स्टाइल क्लास का उपयोग करके अपने टेक्स्ट के लिए डिफ़ॉल्ट स्टाइल सेट करें:
```csharp
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## चरण 3: नंबरिंग लागू करें
आउटलाइनएलिमेंट क्लास ऑब्जेक्ट को प्रारंभ करें और प्रत्येक तत्व पर नंबरिंग लागू करें:
```csharp
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
OutlineElement outlineElem2 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text2 = new RichText(doc) { Text = "Second", ParagraphStyle = defaultStyle };
outlineElem2.AppendChildLast(text2);
OutlineElement outlineElem3 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text3 = new RichText(doc) { Text = "Third", ParagraphStyle = defaultStyle };
outlineElem3.AppendChildLast(text3);
```
## चरण 4: रूपरेखा तत्व जोड़ें
रूपरेखा तत्वों को रूपरेखा में जोड़ें:
```csharp
outline.AppendChildLast(outlineElem1);
outline.AppendChildLast(outlineElem2);
outline.AppendChildLast(outlineElem3);
```
## चरण 5: दस्तावेज़ सहेजें
OneNote दस्तावेज़ को लागू क्रमांकन के साथ सहेजें:
```csharp
dataDir = dataDir + "ApplyNumberingOnText_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nNumbering applied successfully on a text.\nFile saved at " + dataDir); 
```
## निष्कर्ष
बधाई हो! आपने सफलतापूर्वक सीख लिया है कि .NET के लिए Aspose.Note में टेक्स्ट पर नंबरिंग कैसे लागू करें। आसानी से दिखने में आकर्षक दस्तावेज़ बनाने के लिए विभिन्न फ़ॉर्मेटिंग विकल्पों के साथ प्रयोग करें।
## अक्सर पूछे जाने वाले प्रश्न
### 1. क्या मैं क्रमांकन प्रारूप को अनुकूलित कर सकता हूँ?
हां, नंबरलिस्ट वर्ग आपको अपनी प्राथमिकताओं के अनुसार नंबरिंग प्रारूप को अनुकूलित करने की अनुमति देता है।
### 2. क्या अन्य फ़ॉर्मेटिंग विकल्प उपलब्ध हैं?
Aspose.Note फ़ॉन्ट शैली, रंग और बहुत कुछ सहित स्वरूपण विकल्पों की एक विस्तृत श्रृंखला प्रदान करता है।
### 3. क्या Aspose.Note विज़ुअल स्टूडियो के साथ संगत है?
बिल्कुल! Aspose.Note सहज विकास अनुभव के लिए विज़ुअल स्टूडियो के साथ सहजता से एकीकृत होता है।
### 4. क्या मैं खरीदने से पहले Aspose.Note आज़मा सकता हूँ?
 निश्चित रूप से! आप नि:शुल्क परीक्षण का पता लगा सकते हैं[यहाँ](https://releases.aspose.com/).
### 5. मुझे Aspose.Note के लिए समर्थन कहाँ से मिल सकता है?
 किसी भी सहायता या प्रश्न के लिए, पर जाएँ[Aspose.नोट फोरम](https://forum.aspose.com/c/note/28).