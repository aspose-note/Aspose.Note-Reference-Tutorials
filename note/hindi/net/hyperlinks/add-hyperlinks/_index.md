---
title: Aspose.Note दस्तावेज़ों में हाइपरलिंक जोड़ें
linktitle: Aspose.Note दस्तावेज़ों में हाइपरलिंक जोड़ें
second_title: Aspose.Note .NET API
description: .NET के लिए Aspose.Note का उपयोग करके Aspose.Note दस्तावेज़ों में हाइपरलिंक जोड़ने का तरीका जानें। इस चरण-दर-चरण ट्यूटोरियल के साथ दस्तावेज़ अन्तरक्रियाशीलता बढ़ाएँ।
weight: 10
url: /hi/net/hyperlinks/add-hyperlinks/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note दस्तावेज़ों में हाइपरलिंक जोड़ें

## परिचय

इस ट्यूटोरियल में, आप सीखेंगे कि .NET फ्रेमवर्क का उपयोग करके Aspose.Note दस्तावेज़ों के भीतर टेक्स्ट में हाइपरलिंक कैसे जोड़ें। Aspose.Note OneNote दस्तावेज़ों को प्रोग्रामेटिक रूप से हेरफेर करने के लिए शक्तिशाली सुविधाएँ प्रदान करता है। हाइपरलिंक जोड़ने से आपके दस्तावेज़ों की अन्तरक्रियाशीलता और उपयोगिता बढ़ सकती है, जिससे वे उपयोगकर्ताओं के लिए अधिक आकर्षक बन सकते हैं।

## पूर्वावश्यकताएँ:

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित शर्तें हैं:

1. C# प्रोग्रामिंग भाषा की बुनियादी समझ।
2. आपके सिस्टम पर विज़ुअल स्टूडियो स्थापित है।
3.  .NET लाइब्रेरी के लिए Aspose.Note स्थापित किया गया। आप इसे यहां से डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/note/net/).
4. Aspose.Note दस्तावेज़ों की संरचना और घटकों से परिचित होना।

## नामस्थान आयात करें:

सबसे पहले, आपको अपने C# प्रोजेक्ट में आवश्यक नेमस्पेस आयात करना होगा। ये नामस्थान Aspose.Note दस्तावेज़ों के साथ काम करने के लिए आवश्यक कक्षाओं और विधियों तक पहुंच प्रदान करते हैं।

```csharp
using System;
using System.Drawing;
```

## चरण 1: एक नया दस्तावेज़ ऑब्जेक्ट बनाएँ:

दस्तावेज़ वर्ग का एक नया उदाहरण बनाकर प्रारंभ करें। यह ऑब्जेक्ट आपके Aspose.Note दस्तावेज़ का प्रतिनिधित्व करेगा, जिसमें आप हाइपरलिंक जोड़ेंगे।

```csharp
Document doc = new Document();
```

## चरण 2: पाठ शैलियाँ परिभाषित करें:

नियमित टेक्स्ट और हाइपरलिंक टेक्स्ट के लिए टेक्स्ट शैलियों को परिभाषित करें। आप अपनी पसंद के अनुसार विभिन्न विशेषताओं जैसे फ़ॉन्ट रंग, फ़ॉन्ट नाम और फ़ॉन्ट आकार को अनुकूलित कर सकते हैं।

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

## चरण 3: रिचटेक्स्ट ऑब्जेक्ट बनाएं:

उन टेक्स्ट सेगमेंट के लिए रिचटेक्स्ट ऑब्जेक्ट बनाएं जिन्हें आप अपने दस्तावेज़ में शामिल करना चाहते हैं। उपयुक्त टेक्स्ट जोड़ें और प्रत्येक खंड में वांछित टेक्स्ट शैलियाँ लागू करें।

```csharp
RichText text = new RichText() { ParagraphStyle = ParagraphStyle.Default }
                    .Append("This is ", textStyleRed)
                    .Append("hyperlink", textStyleHyperlink)
                    .Append(". This text is not a hyperlink.", TextStyle.Default);
```

## चरण 4: रूपरेखा और रूपरेखा तत्व बनाएं:

अपने दस्तावेज़ की सामग्री को संरचित करने के लिए एक आउटलाइन ऑब्जेक्ट और एक आउटलाइनएलिमेंट ऑब्जेक्ट बनाएं। हाइपरलिंक वाले रिचटेक्स्ट ऑब्जेक्ट को आउटलाइनएलिमेंट में जोड़ें।

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

## चरण 5: पेज पर तत्व जोड़ें:

एक शीर्षक ऑब्जेक्ट और एक पेज ऑब्जेक्ट बनाएं। आउटलाइन ऑब्जेक्ट को पेज पर जोड़ें। अंत में, पेज को दस्तावेज़ में जोड़ें।

```csharp
Title title = new Title() { TitleText = titleText };
Page page = new Note.Page() { Title = title };

page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## चरण 6: दस्तावेज़ सहेजें:

वह फ़ाइल पथ निर्दिष्ट करें जहाँ आप Aspose.Note दस्तावेज़ को सहेजना चाहते हैं और इसे सहेजने के लिए सेव विधि को कॉल करें।

```csharp
string dataDir = "Your Document Directory";
string outputFilePath = Path.Combine(dataDir, "AddHyperlink_out.one");
doc.Save(outputFilePath);
```

## निष्कर्ष:

इस ट्यूटोरियल में, आपने सीखा कि .NET के लिए Aspose.Note का उपयोग करके Aspose.Note दस्तावेज़ों में हाइपरलिंक कैसे जोड़ें। इन चरणों का पालन करके, आप अपने दस्तावेज़ों की अन्तरक्रियाशीलता बढ़ा सकते हैं और उपयोगकर्ताओं को अधिक गतिशील अनुभव प्रदान कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं Aspose.Note का उपयोग करके एक ही दस्तावेज़ में एकाधिक हाइपरलिंक जोड़ सकता हूँ?

A1: हां, आप एक ही Aspose.Note दस्तावेज़ के भीतर विभिन्न टेक्स्ट सेगमेंट में एकाधिक हाइपरलिंक जोड़ सकते हैं।

### Q2: क्या मैं Aspose.Note दस्तावेज़ों में हाइपरलिंक्स की उपस्थिति को अनुकूलित कर सकता हूँ?

A2: हाँ, आप Aspose.Note दस्तावेज़ों में हाइपरलिंक के लिए फ़ॉन्ट रंग, फ़ॉन्ट आकार और फ़ॉन्ट शैली जैसी विभिन्न विशेषताओं को अनुकूलित कर सकते हैं।

### Q3: क्या Aspose.Note बाहरी वेबसाइटों के लिए हाइपरलिंक का समर्थन करता है?

A3: हां, Aspose.Note आपको हाइपरलिंक बनाने की अनुमति देता है जो उपयोगकर्ताओं को बाहरी वेबसाइटों या वेब पेजों पर ले जाता है।

### Q4: क्या Aspose.Note Microsoft OneNote के सभी संस्करणों के साथ संगत है?

A4: Aspose.Note को Microsoft OneNote 2010 और बाद के संस्करणों के साथ काम करने के लिए डिज़ाइन किया गया है।

### Q5: क्या मैं Aspose.Note API का उपयोग करके प्रोग्रामेटिक रूप से हाइपरलिंक जोड़ सकता हूँ?

A5: हां, Aspose.Note एपीआई प्रदान करता है जो आपको अपने .NET अनुप्रयोगों के भीतर प्रोग्रामेटिक रूप से टेक्स्ट में हाइपरलिंक जोड़ने की अनुमति देता है।
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
