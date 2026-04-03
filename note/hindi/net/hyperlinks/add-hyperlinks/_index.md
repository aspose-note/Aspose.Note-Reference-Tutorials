---
date: 2026-04-03
description: Aspose.Note for .NET का उपयोग करके Aspose.Note दस्तावेज़ों में हाइपरलिंक
  कैसे जोड़ें, हाइपरलिंक की उपस्थिति को अनुकूलित करें, और अधिक समृद्ध OneNote फ़ाइलों
  के लिए कई हाइपरलिंक सम्मिलित करें, यह सीखें।
keywords:
- how to add hyperlink
- insert multiple hyperlinks
- add hyperlink to onenote
- customize hyperlink appearance
- generate one file hyperlink
linktitle: Aspose.Note दस्तावेज़ों में हाइपरलिंक कैसे जोड़ें
second_title: Aspose.Note .NET API
title: Aspose.Note दस्तावेज़ों में हाइपरलिंक कैसे जोड़ें
url: /hi/net/hyperlinks/add-hyperlinks/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note दस्तावेज़ों में हाइपरलिंक कैसे जोड़ें

## परिचय

इस ट्यूटोरियल में आप Aspose.Note दस्तावेज़ों के भीतर .NET API के साथ टेक्स्ट में **हाइपरलिंक कैसे जोड़ें** की खोज करेंगे। हाइपरलिंक जोड़ने से स्थिर नोट्स इंटरैक्टिव, क्लिक करने योग्य सामग्री में बदल जाते हैं—वेब संसाधनों, आंतरिक अनुभागों या बाहरी फ़ाइलों से लिंक करने के लिए उपयुक्त। हम प्रत्येक चरण को विस्तार से बताएँगे, आपको **हाइपरलिंक की उपस्थिति को अनुकूलित** करने का तरीका दिखाएँगे, और जब आपको अधिक समृद्ध OneNote पृष्ठों की आवश्यकता हो तो **एकाधिक हाइपरलिंक सम्मिलित करने** की व्याख्या करेंगे।

## त्वरित उत्तर
- **OneNote फ़ाइल बनाने के लिए मुख्य क्लास कौन सी है?** `Document` from Aspose.Note.
- **कौन सी प्रॉपर्टी टेक्स्ट को हाइपरलिंक बनाती है?** `IsHyperlink = true` on `TextStyle`.
- **क्या मैं बाहरी वेबसाइटों से लिंक कर सकता हूँ?** हाँ, `HyperlinkAddress` को `https://www.google.com` जैसी URL पर सेट करें।
- **उत्पादन उपयोग के लिए क्या मुझे लाइसेंस चाहिए?** गैर‑मूल्यांकन बिल्ड्स के लिए एक वैध Aspose.Note लाइसेंस आवश्यक है।
- **कौन से .NET संस्करण समर्थित हैं?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6+.

## Aspose.Note में “हाइपरलिंक कैसे जोड़ें” क्या है?
हाइपरलिंक जोड़ने का मतलब है टेक्स्ट के एक भाग से URL संलग्न करना ताकि जब उपयोगकर्ता OneNote के भीतर उस पर क्लिक करे, तो लिंक किया गया संसाधन ब्राउज़र या किसी अन्य एप्लिकेशन में खुले। Aspose.Note प्रोग्रामेटिक रूप से यह संभव बनाने के लिए `TextStyle.IsHyperlink` फ़्लैग और `HyperlinkAddress` प्रॉपर्टी प्रदान करता है।

## OneNote दस्तावेज़ों में हाइपरलिंक क्यों जोड़ें?
- **बेहतर नेविगेशन:** संबंधित वेब पेजों या अनुभागों पर सीधे जाएँ।
- **उन्नत दस्तावेज़ीकरण:** नोट छोड़े बिना संदर्भ, ट्यूटोरियल या स्रोत फ़ाइलें प्रदान करें।
- **पेशेवर रूप:** अनुकूलन योग्य रंग और शैलियाँ हाइपरलिंक को आपके दस्तावेज़ डिज़ाइन के साथ मिलाने देती हैं।

## पूर्वापेक्षाएँ

1. C# और Visual Studio का बुनियादी ज्ञान।
2. Aspose.Note for .NET लाइब्रेरी स्थापित – इसे [here](https://releases.aspose.com/note/net/) से डाउनलोड करें।
3. Aspose.Note दस्तावेज़ संरचना (पृष्ठ, रूपरेखा, रिच टेक्स्ट) की समझ।

## नेमस्पेस आयात करें

सबसे पहले, उन नेमस्पेस को आयात करें जो आपको कोर Aspose.Note क्लासेस और बुनियादी .NET प्रकारों तक पहुँच प्रदान करते हैं।

```csharp
using System;
using System.Drawing;
```

## चरण‑दर‑चरण गाइड

### चरण 1: नया Document ऑब्जेक्ट बनाएं

`Document` को इंस्टैंशिएट करें जो आपके सभी पृष्ठों और सामग्री को रखेगा।

```csharp
Document doc = new Document();
```

### चरण 2: टेक्स्ट स्टाइल्स परिभाषित करें (हाइपरलिंक स्टाइल सहित)

दो `TextStyle` ऑब्जेक्ट बनाएं – एक सामान्य टेक्स्ट के लिए और एक हाइपरलिंक के लिए।  
यहाँ हम फ़ॉन्ट रंग सेट करके **हाइपरलिंक की उपस्थिति को अनुकूलित** भी करते हैं।

```csharp
TextStyle textStyleRed = new TextStyle
{
    FontColor = Color.Red,
    FontName = "Arial",
    FontSize = 10,
};

TextStyle textStyleHyperlink = new TextStyle
{
    IsHyperlink = true,
    HyperlinkAddress = "www.google.com"
};
```

> **प्रो टिप:** **एकाधिक हाइपरलिंक** सम्मिलित करने के लिए, विभिन्न `HyperlinkAddress` मानों वाले अतिरिक्त `TextStyle` ऑब्जेक्ट परिभाषित करें और उन्हें बाद के `RichText` खंडों में पुनः उपयोग करें।

### चरण 3: RichText ऑब्जेक्ट बनाएं

एक पैराग्राफ बनाएं जो सामान्य टेक्स्ट और हाइपरलिंक को मिलाता है। `Append` मेथड आपको स्टाइल्ड फ्रैगमेंट्स को चेन करने देता है।

```csharp
RichText text = new RichText() { ParagraphStyle = ParagraphStyle.Default }
                    .Append("This is ", textStyleRed)
                    .Append("hyperlink", textStyleHyperlink)
                    .Append(". This text is not a hyperlink.", TextStyle.Default);
```

### चरण 4: Outline और Outline एलिमेंट बनाएं

Outlines पृष्ठ पर दृश्य तत्वों के कंटेनर की तरह कार्य करते हैं। आवश्यकतानुसार आकार और स्थिति सेट करें।

```csharp
Outline outline = new Outline()
{
    MaxWidth = 200,
    MaxHeight = 200,
    VerticalOffset = 100,
    HorizontalOffset = 100
};

OutlineElement outlineElem = new OutlineElement();
outlineElem.AppendChildLast(text);
```

### चरण 5: पृष्ठ में एलिमेंट जोड़ें

प्रत्येक OneNote फ़ाइल पृष्ठों से बनी होती है। हम एक `Title` और एक `Page` बनाते हैं, फिर outline को संलग्न करते हैं।

```csharp
Title title = new Title() { TitleText = titleText };
Page page = new Note.Page() { Title = title };

page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

### चरण 6: दस्तावेज़ सहेजें

एक फ़ोल्डर चुनें, पूर्ण फ़ाइल नाम बनाएं, और `Save` को कॉल करें। आउटपुट फ़ाइल आपके हाइपरलिंक वाले एक वैध OneNote `.one` फ़ाइल होगी।

```csharp
string dataDir = "Your Document Directory";
string outputFilePath = Path.Combine(dataDir, "AddHyperlink_out.one");
doc.Save(outputFilePath);
```

## सामान्य समस्याएँ और समाधान

| समस्या | समाधान |
|-------|----------|
| हाइपरलिंक नहीं खुल रहा है | सुनिश्चित करें कि `HyperlinkAddress` में प्रोटोकॉल (`http://` या `https://`) शामिल है। |
| टेक्स्ट रंग लागू नहीं हुआ | `Hyperlink` के लिए उपयोग किए गए `TextStyle` पर `FontColor` सेट करें। |
| एक पृष्ठ पर कई लिंक चाहिए | कई `TextStyle` ऑब्जेक्ट बनाएं, प्रत्येक का अपना `HyperlinkAddress` हो, और उन्हें समान या अलग `RichText` ऑब्जेक्ट्स में जोड़ें। |
| दस्तावेज़ OneNote में लोड नहीं हो रहा | जाँचें कि आप समर्थित OneNote संस्करण (2010+) का उपयोग कर रहे हैं। |

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या मैं Aspose.Note का उपयोग करके उसी दस्तावेज़ में कई हाइपरलिंक जोड़ सकता हूँ?**  
A: हाँ, बस विभिन्न `HyperlinkAddress` मानों वाले अतिरिक्त `TextStyle` इंस्टेंस बनाएं और उन्हें अपने `RichText` ऑब्जेक्ट्स में जोड़ें।

**Q: हाइपरलिंक की उपस्थिति को मैं कैसे अनुकूलित कर सकता हूँ?**  
A: `IsHyperlink = true` वाले `TextStyle` पर `FontColor`, `FontName`, और `FontSize` जैसी प्रॉपर्टीज़ का उपयोग करें। इससे आप अपने दस्तावेज़ की ब्रांडिंग से मेल कर सकते हैं।

**Q: क्या Aspose.Note बाहरी वेबसाइटों के लिए हाइपरलिंक का समर्थन करता है?**  
A: बिल्कुल। `HyperlinkAddress` को किसी भी वैध URL (जिसमें `http://` या `https://` शामिल है) पर सेट करें ताकि OneNote फ़ाइल से बाहर लिंक किया जा सके।

**Q: क्या कई हाइपरलिंक वाले एकल OneNote फ़ाइल बनाना संभव है?**  
A: हाँ। विभिन्न हाइपरलिंक पतों वाले स्टाइल्ड `RichText` खंडों को बार‑बार जोड़कर आप **एक फ़ाइल हाइपरलिंक** संग्रह बना सकते हैं।

**Q: क्या Aspose.Note नवीनतम OneNote संस्करणों के साथ संगत है?**  
A: लाइब्रेरी OneNote 2010 और बाद के संस्करणों के साथ काम करती है, जिसमें Windows 10 UWP संस्करण भी शामिल है।

---

**अंतिम अपडेट:** 2026-04-03  
**परीक्षण किया गया:** Aspose.Note for .NET 24.11  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}