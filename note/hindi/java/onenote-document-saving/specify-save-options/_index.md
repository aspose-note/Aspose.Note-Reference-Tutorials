---
title: OneNote में सहेजें विकल्प निर्दिष्ट करें - Aspose.Note
linktitle: OneNote में सहेजें विकल्प निर्दिष्ट करें - Aspose.Note
second_title: Aspose.नोट जावा एपीआई
description: जानें कि Java के लिए Aspose.Note का उपयोग करके OneNote में सेव विकल्प कैसे निर्दिष्ट करें। पेज इंडेक्स, गिनती और संपीड़न सेटिंग्स को सहजता से अनुकूलित करें।
weight: 24
url: /hi/java/onenote-document-saving/specify-save-options/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote में सहेजें विकल्प निर्दिष्ट करें - Aspose.Note

## परिचय

इस ट्यूटोरियल में, हम सीखेंगे कि Java के लिए Aspose.Note का उपयोग करके OneNote में सेव विकल्प कैसे निर्दिष्ट करें। Aspose.Note एक शक्तिशाली जावा लाइब्रेरी है जो डेवलपर्स को OneNote दस्तावेज़ों को प्रोग्रामेटिक रूप से बनाने, हेरफेर करने और परिवर्तित करने की अनुमति देती है। Aspose.Note के साथ, आप अपनी आवश्यकताओं के अनुसार आउटपुट को अनुकूलित करने के लिए विभिन्न सेव विकल्पों को आसानी से नियंत्रित कर सकते हैं।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित शर्तें हैं:

1. जावा प्रोग्रामिंग भाषा का बुनियादी ज्ञान।
2. आपके सिस्टम पर JDK (जावा डेवलपमेंट किट) स्थापित है।
3.  जावा लाइब्रेरी के लिए Aspose.Note स्थापित किया गया। आप इसे यहां से डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/note/java/).

## पैकेज आयात करें

आरंभ करने के लिए, अपने जावा कोड में आवश्यक पैकेज आयात करें:

```java
import com.aspose.note.Document;
import com.aspose.note.PdfImageCompression;
import com.aspose.note.PdfSaveOptions;
import java.io.IOException;
```

आइए उदाहरण को कई चरणों में विभाजित करें:

## चरण 1: OneNote दस्तावेज़ लोड करें

```java
// दस्तावेज़ निर्देशिका का पथ.
String dataDir = "Your Document Directory";

// दस्तावेज़ को Aspose.Note में लोड करें।
Document doc = new Document(dataDir + "Aspose.one");
```

 इस चरण में, हम OneNote दस्तावेज़ का पथ निर्दिष्ट करते हैं और उसे इसमें लोड करते हैं`Document` वस्तु।

## चरण 2: PdfSaveOptions ऑब्जेक्ट को आरंभ करें

```java
// PdfSaveOptions ऑब्जेक्ट को प्रारंभ करें
PdfSaveOptions opts = new PdfSaveOptions();
```

 यहां, हम a आरंभ करते हैं`PdfSaveOptions` ऑब्जेक्ट जिसका उपयोग दस्तावेज़ को पीडीएफ के रूप में सहेजने के विकल्पों को निर्दिष्ट करने के लिए किया जाएगा।

## चरण 3: पृष्ठ अनुक्रमणिका और गणना सेट करें

```java
// पेज इंडेक्स सेट करें
opts.setPageIndex(2);

// पृष्ठ संख्या निर्धारित करें
opts.setPageCount(3);
```

ये पंक्तियाँ सहेजे जाने वाले पृष्ठों की अनुक्रमणिका और गिनती निर्धारित करती हैं। इस उदाहरण में, हम इंडेक्स 2 से शुरू करके कुल 3 पेज सहेज रहे हैं।

## चरण 4: संपीड़न सेटिंग्स निर्दिष्ट करें

```java
// यदि आवश्यक हो तो संपीड़न निर्दिष्ट करें
opts.setImageCompression(PdfImageCompression.Jpeg);
opts.setJpegQuality(90);
```

यहां, हम पीडीएफ के लिए छवि संपीड़न सेटिंग्स निर्दिष्ट करते हैं। हम संपीड़न को JPEG प्रारूप में सेट करते हैं और JPEG गुणवत्ता को 90% के रूप में निर्दिष्ट करते हैं।

## चरण 5: दस्तावेज़ को विकल्पों के साथ सहेजें

```java
dataDir = dataDir + "Document.SaveWithOptions_out.pdf";
doc.save(dataDir, opts);
```

अंत में, हम दस्तावेज़ को निर्दिष्ट विकल्पों के साथ सहेजते हैं। आउटपुट पीडीएफ दिए गए विकल्पों के साथ निर्दिष्ट स्थान पर सहेजा जाएगा।

## निष्कर्ष

इस ट्यूटोरियल में, हमने सीखा है कि Java के लिए Aspose.Note का उपयोग करके OneNote में सेव विकल्प कैसे निर्दिष्ट करें। सेव विकल्पों को अनुकूलित करके, आप आउटपुट दस्तावेज़ के विभिन्न पहलुओं, जैसे पेज इंडेक्स, गिनती और संपीड़न सेटिंग्स को नियंत्रित कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Aspose.Note बड़े OneNote दस्तावेज़ों को संभाल सकता है?

A1: हाँ, Aspose.Note को बड़े OneNote दस्तावेज़ों को कुशलतापूर्वक संभालने के लिए डिज़ाइन किया गया है।

### Q2: क्या Aspose.Note नवीनतम जावा संस्करणों के साथ संगत है?

A2: हां, Aspose.Note नवीनतम जावा संस्करणों के साथ संगत है।

### Q3: क्या मैं Aspose.Note का उपयोग करके OneNote दस्तावेज़ों को अन्य प्रारूपों में परिवर्तित कर सकता हूँ?

A3: हाँ, Aspose.Note OneNote दस्तावेज़ों को PDF, DOCX और HTML जैसे विभिन्न स्वरूपों में बदलने का समर्थन करता है।

### Q4: क्या Aspose.Note OneNote दस्तावेज़ों के एन्क्रिप्शन और डिक्रिप्शन के लिए समर्थन प्रदान करता है?

A4: हाँ, Aspose.Note OneNote दस्तावेज़ों के एन्क्रिप्शन और डिक्रिप्शन के लिए API प्रदान करता है।

### Q5: क्या Aspose.Note व्यावसायिक उपयोग के लिए उपयुक्त है?

A5: हाँ, Aspose.Note का उपयोग लाइसेंस खरीदकर व्यावसायिक उद्देश्यों के लिए किया जा सकता है।
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
