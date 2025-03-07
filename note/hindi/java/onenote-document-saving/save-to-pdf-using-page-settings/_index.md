---
title: OneNote में पेज सेटिंग्स का उपयोग करके पीडीएफ में सहेजें - Aspose.Note
linktitle: OneNote में पेज सेटिंग्स का उपयोग करके पीडीएफ में सहेजें - Aspose.Note
second_title: Aspose.नोट जावा एपीआई
description: Aspose.Note लाइब्रेरी का उपयोग करके जावा में OneNote दस्तावेज़ों को PDF में सहेजना सीखें। विभिन्न पेज सेटिंग्स के लिए कोड उदाहरणों के साथ चरण-दर-चरण मार्गदर्शिका।
weight: 19
url: /hi/java/onenote-document-saving/save-to-pdf-using-page-settings/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote में पेज सेटिंग्स का उपयोग करके पीडीएफ में सहेजें - Aspose.Note

## परिचय

इस ट्यूटोरियल में, हम सीखेंगे कि जावा के लिए Aspose.Note के साथ विभिन्न पेज सेटिंग्स का उपयोग करके OneNote दस्तावेज़ों को पीडीएफ प्रारूप में कैसे सहेजा जाए। हम दो तरीकों को कवर करेंगे: लेटर पेज सेटिंग्स के साथ सेविंग और ऊंचाई सीमा के बिना ए4 पेज सेटिंग्स के साथ सेविंग।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

1. आपके सिस्टम पर जावा डेवलपमेंट किट (जेडीके) स्थापित है।
2. जावा लाइब्रेरी के लिए Aspose.Note डाउनलोड किया गया और आपके जावा प्रोजेक्ट में शामिल किया गया।
3. जावा प्रोग्रामिंग भाषा की बुनियादी समझ।

## पैकेज आयात करें

सुनिश्चित करें कि आपने अपने प्रोजेक्ट में Java के लिए Aspose.Note का उपयोग करने के लिए आवश्यक पैकेज आयात किए हैं। यहाँ आयात विवरण है:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## पत्र पृष्ठ सेटिंग्स का उपयोग करके पीडीएफ में सहेजें

### चरण 1: दस्तावेज़ लोड करें

सबसे पहले, OneNote दस्तावेज़ को Aspose.Note में लोड करें:

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### चरण 2: गंतव्य पथ को परिभाषित करें

पीडीएफ फ़ाइल के लिए गंतव्य पथ निर्दिष्ट करें:

```java
String dst = "path/to/your/SaveToPdfUsingLetterPageSettings.pdf";
```

### चरण 3: दस्तावेज़ सहेजें

दस्तावेज़ को पत्र पृष्ठ सेटिंग्स के साथ सहेजें:

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getLetter());
oneFile.save(dst, options);
```

## ऊंचाई सीमा के बिना A4 पेज सेटिंग्स का उपयोग करके पीडीएफ में सहेजें

### चरण 1: दस्तावेज़ लोड करें

इसी प्रकार, OneNote दस्तावेज़ को Aspose.Note में लोड करें:

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### चरण 2: गंतव्य पथ को परिभाषित करें

पीडीएफ फ़ाइल के लिए गंतव्य पथ निर्दिष्ट करें:

```java
String dst = "path/to/your/SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf";
```

### चरण 3: दस्तावेज़ सहेजें

दस्तावेज़ को ऊंचाई सीमा के बिना A4 पेज सेटिंग्स के साथ सहेजें:

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getA4NoHeightLimit());
oneFile.save(dst, options);
```

इन चरणों का पालन करने के बाद, आपने विभिन्न पेज सेटिंग्स का उपयोग करके अपने OneNote दस्तावेज़ को पीडीएफ में सफलतापूर्वक सहेज लिया होगा।

## निष्कर्ष

इस ट्यूटोरियल में, हमने पता लगाया है कि जावा लाइब्रेरी के लिए Aspose.Note का उपयोग करके OneNote दस्तावेज़ों को पीडीएफ प्रारूप में कैसे सहेजा जाए। चरण-दर-चरण मार्गदर्शिका का पालन करके, आप इस कार्यक्षमता को अपने जावा अनुप्रयोगों में आसानी से एकीकृत कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं पेज सेटिंग्स को और अधिक अनुकूलित कर सकता हूँ?

A1: हां, आप Java के लिए Aspose.Note का उपयोग करके अपनी आवश्यकताओं के अनुसार पेज सेटिंग्स को कस्टमाइज़ कर सकते हैं।

### Q2: क्या Aspose.Note पीडीएफ के अलावा अन्य आउटपुट स्वरूपों का समर्थन करता है?

A2: हाँ, Aspose.Note छवियों और HTML सहित विभिन्न आउटपुट स्वरूपों का समर्थन करता है।

### Q3: क्या Aspose.Note OneNote फ़ाइलों के विभिन्न संस्करणों के साथ संगत है?

A3: हाँ, Aspose.Note .one और .onetoc2 सहित विभिन्न संस्करणों की OneNote फ़ाइलों का समर्थन करता है।

### Q4: क्या मैं एक ही बार में एकाधिक OneNote फ़ाइलों को PDF में परिवर्तित कर सकता हूँ?

A4: हाँ, आप Java के लिए Aspose.Note का उपयोग करके एकाधिक OneNote फ़ाइलों को बैच प्रोसेस कर सकते हैं।

### Q5: क्या परीक्षण प्रयोजनों के लिए कोई परीक्षण संस्करण उपलब्ध है?

A5: हाँ, आप वेबसाइट से Java के लिए Aspose.Note का निःशुल्क परीक्षण प्राप्त कर सकते हैं।
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
