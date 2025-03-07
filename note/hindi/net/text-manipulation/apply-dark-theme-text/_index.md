---
title: .NET के लिए Aspose.Note के साथ डार्क थीम परिवर्तन
linktitle: Aspose.Note में टेक्स्ट पर डार्क थीम लागू करें
second_title: Aspose.Note .NET API
description: .NET के लिए Aspose.Note के साथ अपने OneNote दस्तावेज़ों को रूपांतरित करें! सहजता से एक आकर्षक डार्क थीम लागू करें। अभी डाउनलोड करें और अपने नोट लेने के अनुभव को बेहतर बनाएं।
weight: 11
url: /hi/net/text-manipulation/apply-dark-theme-text/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# .NET के लिए Aspose.Note के साथ डार्क थीम परिवर्तन

## परिचय
.NET के लिए Aspose.Note में टेक्स्ट में डार्क थीम लागू करने के बारे में हमारी चरण-दर-चरण मार्गदर्शिका में आपका स्वागत है। Aspose.Note एक शक्तिशाली .NET API है जो डेवलपर्स को Microsoft OneNote फ़ाइलों के साथ प्रोग्रामेटिक रूप से काम करने की अनुमति देता है। इस ट्यूटोरियल में, हम यह पता लगाएंगे कि टेक्स्ट पर डार्क थीम लागू करके अपने OneNote दस्तावेज़ों को एक आकर्षक और आधुनिक रूप कैसे दिया जाए।
## आवश्यक शर्तें
इससे पहले कि हम ट्यूटोरियल में उतरें, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:
-  .NET के लिए Aspose.Note: सुनिश्चित करें कि आपके पास .NET के लिए Aspose.Note स्थापित है। यदि नहीं, तो आप इसे यहां से डाउनलोड कर सकते हैं[Aspose.नोट दस्तावेज़ीकरण](https://reference.aspose.com/note/net/).
- विकास परिवेश: अपना पसंदीदा .NET विकास परिवेश सेट करें, जैसे विज़ुअल स्टूडियो।
- दस्तावेज़ निर्देशिका: वह निर्देशिका तैयार करें जहाँ आपका OneNote दस्तावेज़ स्थित है।
## नामस्थान आयात करें
अपने .NET प्रोजेक्ट में, Aspose.Note के साथ काम करने के लिए आवश्यक नेमस्पेस आयात करें:
```csharp
    using System;
    using System.Drawing;
    using System.IO;
```
## चरण 1: OneNote दस्तावेज़ लोड करें
निम्नलिखित कोड का उपयोग करके अपने OneNote दस्तावेज़ को Aspose.Note में लोड करें:
```csharp
// दस्तावेज़ निर्देशिका का पथ.
string dataDir = "Your Document Directory";
// दस्तावेज़ को Aspose.Note में लोड करें।
Document doc = new Document(Path.Combine(dataDir, "Aspose.one"));
```
## चरण 2: पृष्ठभूमि का रंग सेट करें
प्रत्येक पृष्ठ का पृष्ठभूमि रंग काला पर सेट करें:
```csharp
foreach (var page in doc)
{
    page.BackgroundColor = Color.Black;
}
```
## चरण 3: टेक्स्ट का रंग समायोजित करें
बेहतर दृश्यता के लिए टेक्स्ट के फ़ॉन्ट रंग को सफेद में समायोजित करें:
```csharp
foreach (var node in doc.GetChildNodes<RichText>())
{
    var c = node.ParagraphStyle.FontColor;
    if (c.IsEmpty || Math.Abs(c.R - Color.Black.R) + Math.Abs(c.G - Color.Black.G) + Math.Abs(c.B - Color.Black.B) <= 30)
    {
        node.ParagraphStyle.FontColor = Color.White;
    }
}
```
## चरण 4: दस्तावेज़ सहेजें
संशोधित OneNote दस्तावेज़ को PDF के रूप में सहेजें:
```csharp
doc.Save(Path.Combine(dataDir, "AsposeDarkTheme.pdf"));
```
## निष्कर्ष
बधाई हो! आपने अपने Aspose.Note दस्तावेज़ में टेक्स्ट पर एक डार्क थीम सफलतापूर्वक लागू कर दी है। यह सरल लेकिन प्रभावी एन्हांसमेंट आपकी OneNote फ़ाइलों को अधिक परिष्कृत रूप दे सकता है।
## अक्सर पूछे जाने वाले प्रश्नों
### क्या मैं अपने OneNote दस्तावेज़ के विशिष्ट अनुभागों में डार्क थीम लागू कर सकता हूँ?
हाँ, आप अपने दस्तावेज़ के विशिष्ट पृष्ठों या अनुभागों को लक्षित करने के लिए कोड को अनुकूलित कर सकते हैं।
### क्या Aspose.Note पीडीएफ के अलावा अन्य निर्यात प्रारूपों का समर्थन करता है?
बिल्कुल! Aspose.Note छवियों और Microsoft Word सहित विभिन्न निर्यात प्रारूपों का समर्थन करता है।
### क्या दस्तावेज़ के आकार की कोई सीमा है जिसे Aspose.Note संभाल सकता है?
Aspose.Note विभिन्न आकारों के दस्तावेज़ों को संभाल सकता है, और इसका प्रदर्शन दक्षता के लिए अनुकूलित है।
### क्या मैं डार्क थीम लागू करने के बाद मूल थीम पर वापस लौट सकता हूँ?
हां, आप अपनी प्राथमिकताओं के आधार पर थीम के बीच स्विच करने के लिए कोड को संशोधित कर सकते हैं।
### मुझे Aspose.Note-संबंधित प्रश्नों के लिए सहायता कहाँ से मिल सकती है?
 किसी भी सहायता के लिए, पर जाएँ[Aspose.नोट फोरम](https://forum.aspose.com/c/note/28) या अन्वेषण करें[प्रलेखन](https://reference.aspose.com/note/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
