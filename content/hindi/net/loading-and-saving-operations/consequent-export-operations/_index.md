---
title: Aspose.Note में परिणामी निर्यात संचालन
linktitle: Aspose.Note में परिणामी निर्यात संचालन
second_title: Aspose.Note .NET API
description: OneNote दस्तावेज़ों को विभिन्न स्वरूपों में कुशलतापूर्वक सहेजने के लिए .NET के लिए Aspose.Note में परिणामी निर्यात संचालन करना सीखें।
type: docs
weight: 10
url: /hi/net/loading-and-saving-operations/consequent-export-operations/
---
## परिचय

इस ट्यूटोरियल में, हम .NET के लिए Aspose.Note का उपयोग करके परिणामी निर्यात संचालन करने के बारे में विस्तार से जानेंगे। Aspose.Note एक शक्तिशाली लाइब्रेरी है जो डेवलपर्स को Microsoft OneNote फ़ाइलों के साथ प्रोग्रामेटिक रूप से काम करने में सक्षम बनाती है। दस्तावेज़ों को विभिन्न प्रारूपों में निर्यात करना एक सामान्य आवश्यकता है, और Aspose.Note इस कार्य को कुशलता से सरल बनाता है। आइए जानें कि किसी दस्तावेज़ को चरण दर चरण विभिन्न प्रारूपों में कैसे सहेजा जाए।

## आवश्यक शर्तें

इस ट्यूटोरियल के साथ आगे बढ़ने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

1. C# प्रोग्रामिंग भाषा की बुनियादी समझ।
2. आपके सिस्टम पर विज़ुअल स्टूडियो स्थापित है।
3. .NET लाइब्रेरी के लिए Aspose.Note आपके प्रोजेक्ट में एकीकृत है।

## नामस्थान आयात करें

आरंभ करने के लिए, अपने C# कोड में आवश्यक नामस्थान आयात करना सुनिश्चित करें:

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Drawing;
using System.Globalization;
```

## चरण 1: दस्तावेज़ को प्रारंभ करें

 सबसे पहले, एक नया प्रारंभ करें`Document` स्वचालित लेआउट परिवर्तन का पता लगाने वाली वस्तु अक्षम:

```csharp
Document doc = new Document() { AutomaticLayoutChangesDetectionEnabled = false };
```

## चरण 2: एक नया पेज आरंभ करें

 कोई नया बनाएं`Page` ऑब्जेक्ट बनाएं और उसके गुण निर्दिष्ट करें:

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## चरण 3: पृष्ठ शीर्षक सेट करें

दिनांक और समय की जानकारी के साथ पृष्ठ का शीर्षक परिभाषित करें:

```csharp
ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
page.Title = new Title(doc)
{
    TitleText = new RichText(doc) { Text = "Title text.", ParagraphStyle = textStyle },
    TitleDate = new RichText(doc) { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
    TitleTime = new RichText(doc) { Text = "12:34", ParagraphStyle = textStyle }
};
```

## चरण 4: पेज नोड जोड़ें

दस्तावेज़ में पेज नोड जोड़ें:

```csharp
doc.AppendChildLast(page);
```

## चरण 5: दस्तावेज़ को विभिन्न प्रारूपों में सहेजें

अब, OneNote दस्तावेज़ को विभिन्न स्वरूपों में सहेजें:

```csharp
string dataDir = "Your Document Directory";
doc.Save(dataDir + "ConsequentExportOperations_out.html");            
doc.Save(dataDir + "ConsequentExportOperations_out.pdf");            
doc.Save(dataDir + "ConsequentExportOperations_out.jpg");            
textStyle.FontSize = 11;           
doc.DetectLayoutChanges();            
doc.Save(dataDir + "ConsequentExportOperations_out.bmp");
```

## निष्कर्ष

अंत में, हमने सीखा है कि .NET के लिए Aspose.Note का उपयोग करके परिणामी निर्यात संचालन कैसे करें। इस ट्यूटोरियल में बताए गए चरणों का पालन करके, आप OneNote दस्तावेज़ों को विभिन्न स्वरूपों में निर्बाध रूप से सहेज सकते हैं, जिससे आपके एप्लिकेशन की बहुमुखी प्रतिभा बढ़ सकती है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं पृष्ठ शीर्षक को और अधिक अनुकूलित कर सकता हूँ?

A1: हाँ, आप दस्तावेज़ को सहेजने से पहले अपनी आवश्यकताओं के अनुसार शीर्षक पाठ, दिनांक और समय को संशोधित कर सकते हैं।

### Q2: मैं लेआउट परिवर्तन का पता कैसे लगाऊं?

 ए2: जैसा कि दिखाया गया है, आप इसका उपयोग करके लेआउट परिवर्तनों का मैन्युअल रूप से पता लगा सकते हैं`DetectLayoutChanges()` Aspose.Note द्वारा प्रदान की गई विधि।

### Q3: क्या Aspose.Note उल्लिखित प्रारूपों के अलावा अन्य निर्यात प्रारूपों का समर्थन करता है?

A3: हां, Aspose.Note DOCX, PNG, TIFF और अन्य सहित निर्यात प्रारूपों की एक विस्तृत श्रृंखला का समर्थन करता है।

### Q4: क्या Aspose.Note .NET कोर के साथ संगत है?

A4: हाँ, Aspose.Note .NET Framework और .NET कोर वातावरण दोनों के साथ संगत है।

### Q5: Aspose.Note के लिए मुझे अधिक संसाधन और समर्थन कहां मिल सकता है?

A5: आप व्यापक गाइड, ट्यूटोरियल और सामुदायिक समर्थन के लिए Aspose.Note दस्तावेज़ और फ़ोरम पर जा सकते हैं।