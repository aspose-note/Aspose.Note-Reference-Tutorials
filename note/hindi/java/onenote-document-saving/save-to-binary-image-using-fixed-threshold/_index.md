---
title: OneNote में निश्चित थ्रेशोल्ड का उपयोग करके बाइनरी छवि में सहेजें
linktitle: OneNote में निश्चित थ्रेशोल्ड का उपयोग करके बाइनरी छवि में सहेजें
second_title: Aspose.नोट जावा एपीआई
description: Aspose.Note Java के साथ निश्चित सीमा का उपयोग करके आसानी से Microsoft OneNote दस्तावेज़ों को बाइनरी छवियों के रूप में सहेजें। अपनी OneNote फ़ाइल हेरफेर क्षमताओं को उन्नत करें।
weight: 14
url: /hi/java/onenote-document-saving/save-to-binary-image-using-fixed-threshold/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote में निश्चित थ्रेशोल्ड का उपयोग करके बाइनरी छवि में सहेजें

## परिचय

Java के लिए Aspose.Note एक शक्तिशाली API है जो डेवलपर्स को Microsoft OneNote फ़ाइलों के साथ प्रोग्रामेटिक रूप से काम करने की अनुमति देता है। इस ट्यूटोरियल में, हम यह पता लगाएंगे कि एक निश्चित सीमा का उपयोग करके किसी दस्तावेज़ को बाइनरी छवि के रूप में कैसे सहेजा जाए। इसे प्राप्त करने के लिए नीचे दिए गए चरणों का पालन करें।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

1. आपके सिस्टम पर जावा डेवलपमेंट किट (जेडीके) स्थापित है।
2.  जावा लाइब्रेरी के लिए Aspose.Note डाउनलोड किया गया। आप इसे यहां से डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/note/java/).
3. जावा प्रोग्रामिंग का बुनियादी ज्ञान।

## पैकेज आयात करें

सबसे पहले, अपनी जावा फ़ाइल में आवश्यक पैकेज आयात करें।

```java
import com.aspose.note.*;
import java.io.IOException;
```

## चरण 1: दस्तावेज़ लोड करें

Aspose.Note API का उपयोग करके OneNote दस्तावेज़ लोड करें।

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## चरण 2: बाइनराइज़ेशन विकल्प सेट करें

दस्तावेज़ को बाइनरी छवि के रूप में सहेजने के लिए बाइनराइज़ेशन विकल्पों को परिभाषित करें।

```java
dataDir = dataDir + "SaveToBinaryImageUsingFixedThreshold_out.png";
ImageBinarizationOptions binarizationOptions = new ImageBinarizationOptions();
binarizationOptions.setBinarizationMethod(BinarizationMethod.FixedThreshold);
binarizationOptions.setBinarizationThreshold(123);
```

## चरण 3: छवि सहेजें विकल्प सेट करें

रंग मोड और बाइनराइज़ेशन विकल्पों सहित छवि सहेजने के विकल्प सेट करें।

```java
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.BlackAndWhite);
options.setBinarizationOptions(binarizationOptions);
```

## चरण 4: दस्तावेज़ सहेजें

निर्दिष्ट विकल्पों के साथ दस्तावेज़ को बाइनरी छवि के रूप में सहेजें।

```java
oneFile.save(dataDir, options);
```

## निष्कर्ष

इस ट्यूटोरियल में, हमने सीखा कि जावा के लिए Aspose.Note में एक निश्चित सीमा का उपयोग करके किसी दस्तावेज़ को बाइनरी छवि के रूप में कैसे सहेजा जाए। इन चरणों का पालन करके, आप OneNote फ़ाइलों को प्रोग्रामेटिक रूप से आसानी से हेरफेर कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं बाइनराइज़ेशन के लिए सीमा मान को समायोजित कर सकता हूँ?

 A1: हाँ, आप अपनी आवश्यकताओं के अनुसार सीमा मान को संशोधित करके समायोजित कर सकते हैं`setBinarizationThreshold()` विधि पैरामीटर.

### Q2: क्या Java के लिए Aspose.Note Microsoft OneNote के सभी संस्करणों के साथ संगत है?

A2: Java के लिए Aspose.Note 2010, 2013 और 2016 सहित Microsoft OneNote के विभिन्न संस्करणों का समर्थन करता है।

### Q3: क्या संसाधित किए जा सकने वाले दस्तावेज़ों के आकार पर कोई सीमाएँ हैं?

A3: Java के लिए Aspose.Note में संसाधित किए जा सकने वाले दस्तावेज़ों के आकार पर कोई सीमा नहीं है, जिससे आप बड़ी फ़ाइलों को कुशलतापूर्वक संभाल सकते हैं।

### Q4: क्या मैं एक से अधिक OneNote दस्तावेज़ों को एक साथ परिवर्तित कर सकता हूँ?

उ4: हाँ, आप प्रत्येक फ़ाइल पर पुनरावृत्ति करके और आवश्यक संचालन लागू करके एकाधिक OneNote दस्तावेज़ों को बैच प्रोसेस कर सकते हैं।

### Q5: क्या Java के लिए Aspose.Note के लिए तकनीकी सहायता उपलब्ध है?

 A5: हाँ, तकनीकी सहायता उपलब्ध है[Aspose.नोट फोरम](https://forum.aspose.com/c/note/28), जहां आप प्रश्न पूछ सकते हैं और विशेषज्ञों से सहायता ले सकते हैं।
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
