---
title: OneNote में ग्रेस्केल छवि में सहेजें - Aspose.Note
linktitle: OneNote में ग्रेस्केल छवि में सहेजें - Aspose.Note
second_title: Aspose.नोट जावा एपीआई
description: जावा के लिए Aspose.Note का उपयोग करके OneNote में किसी दस्तावेज़ को ग्रेस्केल छवि के रूप में सहेजना सीखें। Microsoft OneNote दस्तावेज़ों को प्रोग्रामेटिक रूप से आसानी से प्रबंधित करें।
weight: 17
url: /hi/java/onenote-document-saving/save-to-grayscale-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote में ग्रेस्केल छवि में सहेजें - Aspose.Note

## परिचय

इस ट्यूटोरियल में, हम यह पता लगाएंगे कि Java के लिए Aspose.Note का उपयोग करके OneNote में किसी दस्तावेज़ को ग्रेस्केल छवि के रूप में कैसे सहेजा जाए। ग्रेस्केल छवियां मोनोक्रोमैटिक छवियां होती हैं जहां रंग की जानकारी केवल भूरे रंग के रंगों द्वारा दर्शायी जाती है। Aspose.Note एक शक्तिशाली जावा एपीआई है जो Microsoft OneNote दस्तावेज़ों को प्रोग्रामेटिक रूप से हेरफेर करने की अनुमति देता है।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

1. आपके सिस्टम पर जावा डेवलपमेंट किट (जेडीके) स्थापित है।
2.  जावा लाइब्रेरी के लिए Aspose.Note। आप इसे यहां से डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/note/java/).
3. जावा प्रोग्रामिंग की बुनियादी समझ.

## पैकेज आयात करें

आरंभ करने के लिए, आवश्यक पैकेज आयात करें:

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## चरण 1: दस्तावेज़ लोड करें

 सबसे पहले, दस्तावेज़ को Aspose.Note में लोड करें। प्रतिस्थापित करें`"Your Document Directory"` आपके दस्तावेज़ निर्देशिका के पथ के साथ और`"Aspose.one"` आपके OneNote दस्तावेज़ के नाम के साथ।

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## चरण 2: आउटपुट पथ और विकल्प सेट करें

ग्रेस्केल छवि के लिए आउटपुट पथ परिभाषित करें और बचत विकल्प निर्दिष्ट करें। हम रंग मोड को ग्रेस्केल पर सेट करेंगे।

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## चरण 3: दस्तावेज़ सहेजें

अंत में, निर्दिष्ट विकल्पों का उपयोग करके दस्तावेज़ को ग्रेस्केल छवि के रूप में सहेजें।

```java
oneFile.save(dataDir, options);
```

## निष्कर्ष

बधाई हो! आपने जावा के लिए Aspose.Note का उपयोग करके OneNote में किसी दस्तावेज़ को ग्रेस्केल छवि के रूप में सहेजना सफलतापूर्वक सीख लिया है। यह विभिन्न अनुप्रयोगों के लिए अविश्वसनीय रूप से उपयोगी हो सकता है जहां ग्रेस्केल छवियों की आवश्यकता होती है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं ग्रेस्केल छवि को एक अलग प्रारूप में सहेज सकता हूँ?

 A1: हाँ, आप कर सकते हैं। बस बदलो`SaveFormat` में पैरामीटर`ImageSaveOptions` आपके इच्छित प्रारूप में कंस्ट्रक्टर।

### Q2: क्या Aspose.Note OneNote दस्तावेज़ों के सभी संस्करणों के साथ संगत है?

A2: Aspose.Note Microsoft OneNote 2010 और इसके बाद के संस्करण का समर्थन करता है।

### Q3: क्या Aspose.Note का उपयोग करने के लिए लाइसेंस की आवश्यकता होती है?

उ3: हां, उत्पादन परिवेश में Aspose.Note का उपयोग करने के लिए आपको एक वैध लाइसेंस की आवश्यकता है। हालाँकि, आप परीक्षण उद्देश्यों के लिए एक अस्थायी लाइसेंस प्राप्त कर सकते हैं।

### Q4: क्या मैं दस्तावेज़ को छवि के रूप में सहेजने से पहले उसके अन्य पहलुओं में हेरफेर कर सकता हूँ?

उ4: बिल्कुल! Aspose.Note OneNote दस्तावेज़ों को प्रोग्रामेटिक रूप से संपादित करने के लिए सुविधाओं की एक विस्तृत श्रृंखला प्रदान करता है।

### Q5: यदि मुझे कोई समस्या आती है तो मुझे सहायता कहां मिल सकती है?

A5: आप Aspose.Note फोरम पर समर्थन पा सकते हैं[यहाँ](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
