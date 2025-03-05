---
title: OneNote में डिफ़ॉल्ट पैराग्राफ शैली सेट करें - Aspose.Note
linktitle: OneNote में डिफ़ॉल्ट पैराग्राफ शैली सेट करें - Aspose.Note
second_title: Aspose.नोट जावा एपीआई
description: Java के लिए Aspose.Note का उपयोग करके OneNote में डिफ़ॉल्ट पैराग्राफ शैलियाँ सेट करने का तरीका जानें। अपने जावा अनुप्रयोगों में कुशल टेक्स्ट फ़ॉर्मेटिंग के लिए हमारी चरण-दर-चरण मार्गदर्शिका का पालन करें।
type: docs
weight: 11
url: /hi/java/onenote-styles/set-default-paragraph-style/
---
## परिचय

जावा के लिए Aspose.Note डिफ़ॉल्ट पैराग्राफ शैलियों को सेट करने सहित, टेक्स्ट फ़ॉर्मेटिंग में हेरफेर करने के लिए शक्तिशाली क्षमताएं प्रदान करता है। यह ट्यूटोरियल Aspose.Note का उपयोग करके OneNote में डिफ़ॉल्ट पैराग्राफ शैलियों को सेट करने की प्रक्रिया में आपका मार्गदर्शन करेगा।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

1. जावा डेवलपमेंट किट (जेडीके): सुनिश्चित करें कि आपके सिस्टम पर जेडीके स्थापित है।
2.  जावा लाइब्रेरी के लिए Aspose.Note: जावा के लिए Aspose.Note को डाउनलोड और इंस्टॉल करें[डाउनलोड पेज](https://releases.aspose.com/note/java/).
3. एकीकृत विकास पर्यावरण (आईडीई): कोडिंग सुविधा के लिए आपके पास एक आईडीई स्थापित होना चाहिए, जैसे कि एक्लिप्स या इंटेलीजे आईडीईए।

## पैकेज आयात करें

सबसे पहले, कोडिंग शुरू करने के लिए आवश्यक पैकेज आयात करें:

```java
import com.aspose.note.*;

import java.awt.*;
import java.io.FileInputStream;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.List;
```

अब, आइए उदाहरण कोड को कई चरणों में विभाजित करें:

## चरण 1: दस्तावेज़, पृष्ठ और रूपरेखा आरंभ करें

```java
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
Outline outline = new Outline();
```

## चरण 2: एक रूपरेखा तत्व बनाएं

```java
OutlineElement outlineElem = new OutlineElement();
```

## चरण 3: डिफ़ॉल्ट पैराग्राफ़ शैली को परिभाषित करें

```java
ParagraphStyle defaultStyle = new ParagraphStyle()
										.setFontName("Courier New")
										.setFontSize(20);
```

## चरण 4: डिफ़ॉल्ट शैली के साथ रिच टेक्स्ट बनाएं

```java
RichText text = new RichText()
					.append("DefaultParagraphFontAndSize")
					.append(System.lineSeparator())
					.append("OnlyDefaultParagraphFont", new TextStyle().setFontSize(14))
					.append(System.lineSeparator())
					.append("OnlyDefaultParagraphFontSize", new TextStyle().setFontName("Verdana"));
text.setParagraphStyle(defaultStyle);
```

## चरण 5: रूपरेखा तत्व में रिच टेक्स्ट जोड़ें

```java
outlineElem.appendChildLast(text);
```

## चरण 6: रूपरेखा तत्व को रूपरेखा में जोड़ें

```java
outline.appendChildLast(outlineElem);
```

## चरण 7: पृष्ठ पर रूपरेखा जोड़ें

```java
page.appendChildLast(outline);
```

## चरण 8: पृष्ठ को दस्तावेज़ में जोड़ें

```java
document.appendChildLast(page);
```

## चरण 9: दस्तावेज़ सहेजें

```java
document.save(Paths.get(dataDir, "SetDefaultParagraphStyle.one").toString());
```

यह कोड Java के लिए Aspose.Note का उपयोग करके OneNote में डिफ़ॉल्ट पैराग्राफ़ शैली सेट करेगा।

## निष्कर्ष

OneNote में डिफ़ॉल्ट पैराग्राफ शैलियों को प्रोग्रामेटिक रूप से सेट करना Java के लिए Aspose.Note के साथ कुशलतापूर्वक प्राप्त किया जा सकता है। इस ट्यूटोरियल में बताए गए चरणों का पालन करके, आप इस कार्यक्षमता को अपने जावा अनुप्रयोगों में सहजता से एकीकृत कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं डिफ़ॉल्ट पैराग्राफ़ शैली को और अधिक अनुकूलित कर सकता हूँ?

A1: हाँ, आप अपनी आवश्यकताओं के अनुरूप फ़ॉन्ट नाम, आकार, रंग और संरेखण जैसे विभिन्न मापदंडों को समायोजित कर सकते हैं।

### Q2: क्या Aspose.Note अन्य टेक्स्ट फ़ॉर्मेटिंग परिचालनों का समर्थन करता है?

A2: बिल्कुल, Aspose.Note फ़ॉन्ट शैली, बुलेट पॉइंट और इंडेंटेशन सहित टेक्स्ट फ़ॉर्मेटिंग में हेरफेर करने के लिए व्यापक समर्थन प्रदान करता है।

### Q3: क्या Aspose.Note OneNote के सभी संस्करणों के साथ संगत है?

A3: Aspose.Note को व्यापक अनुकूलता सुनिश्चित करते हुए विभिन्न संस्करणों में Microsoft OneNote फ़ाइलों के साथ काम करने के लिए डिज़ाइन किया गया है।

### Q4: क्या मैं Aspose.Note को अपने मौजूदा जावा प्रोजेक्ट में एकीकृत कर सकता हूँ?

A4: हाँ, आप आवश्यक निर्भरताएँ जोड़कर और आवश्यक पैकेज आयात करके Aspose.Note को अपने जावा प्रोजेक्ट्स में आसानी से एकीकृत कर सकते हैं।

### Q5: क्या Aspose.Note के लिए कोई परीक्षण संस्करण उपलब्ध है?

 A5: हाँ, आप Aspose.Note का निःशुल्क परीक्षण प्राप्त कर सकते हैं[वेबसाइट](https://releases.aspose.com/).