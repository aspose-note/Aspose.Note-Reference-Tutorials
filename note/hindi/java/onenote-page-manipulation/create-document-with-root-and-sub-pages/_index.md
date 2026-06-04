---
description: Aspose.Note for Java का उपयोग करके OneNote PDF को कैसे सहेजें और OneNote
  में सब पेज कैसे जोड़ें, सीखें। अपने नोट्स को प्रभावी ढंग से व्यवस्थित करने के लिए
  इस चरण‑दर‑चरण गाइड का पालन करें।
linktitle: How to Save OneNote PDF and Add Sub Pages
second_title: Aspose.Note Java API
title: OneNote PDF को कैसे सहेजें और सब पेज जोड़ें
url: /hi/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote PDF को कैसे सेव करें और सब‑पेज जोड़ें

## परिचय

इस ट्यूटोरियल में आप **OneNote PDF को कैसे सेव करें** यह जानेंगे, साथ ही Aspose.Note for Java का उपयोग करके रूट और सब‑पेज दोनों वाले दस्तावेज़ को कैसे बनाएं। अपने OneNote नोटबुक को स्पष्ट पदानुक्रम के साथ व्यवस्थित करने से नेविगेशन आसान हो जाता है, और PDF में एक्सपोर्ट करने से आप अपने नोट्स को सार्वभौमिक रूप से पढ़े जाने योग्य फ़ॉर्मेट में साझा कर सकते हैं। हम यह भी दिखाएंगे कि **sub pages onenote** शैली में कैसे जोड़ें, ताकि आप आसानी से मल्टी‑लेवल स्ट्रक्चर बना सकें।

## त्वरित उत्तर
- **मुख्य कीवर्ड का क्या अर्थ है?** यह Aspose.Note का उपयोग करके OneNote नोटबुक को PDF में एक्सपोर्ट करने को दर्शाता है।  
- **कौन सा API उपयोग किया गया है?** Aspose.Note for Java।  
- **क्या मैं पदानुक्रमित पेज बना सकता हूँ?** हाँ – पेज लेवल सेट करके रूट और सब‑पेज बना सकते हैं।  
- **क्या लाइसेंस की आवश्यकता है?** एक फ्री ट्रायल उपलब्ध है; प्रोडक्शन के लिए कमर्शियल लाइसेंस आवश्यक है।  
- **कौन‑से आउटपुट फ़ॉर्मेट सपोर्टेड हैं?** BMP, PDF, PNG, और अधिक।

## “how to save OneNote PDF” क्या है?
OneNote को PDF के रूप में सेव करने से नोटबुक के पेज़ एक फिक्स्ड‑लेआउट दस्तावेज़ में बदल जाते हैं, जिसमें फ़ॉर्मेटिंग, इमेज़ और पदानुक्रम बरकरार रहता है। यह शेयरिंग, आर्काइविंग या प्रिंटिंग के लिए आदर्श है।

## सब‑पेज onenote क्यों जोड़ें?
सब‑पेज जोड़ने से आप संबंधित सामग्री को पैरेंट पेज के तहत समूहित कर सकते हैं, जो फ़ोल्डर‑जैसे स्ट्रक्चर को दर्शाता है। यह नोट ऑर्गनाइज़ेशन को बेहतर बनाता है, खोज को तेज़ करता है, और PDF में एक्सपोर्ट करने पर पढ़ने का अनुभव बढ़ाता है।

## पूर्वापेक्षाएँ

शुरू करने से पहले सुनिश्चित करें कि आपके पास निम्नलिखित प्री‑रिक्विज़िट्स हैं:

1. Java Development Kit (JDK): सुनिश्चित करें कि आपके सिस्टम पर JDK इंस्टॉल है।  
2. Aspose.Note for Java: [वेबसाइट](https://purchase.aspose.com/buy) से Aspose.Note for Java डाउनलोड और इंस्टॉल करें।  
3. Integrated Development Environment (IDE): IntelliJ IDEA, Eclipse, या NetBeans जैसे Java IDE में से कोई एक चुनें।

## पैकेज इम्पोर्ट करें

अपने Java प्रोजेक्ट में आवश्यक पैकेज इम्पोर्ट करें:

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

## चरण 1: डॉक्यूमेंट डायरेक्टरी सेट करें

वह डायरेक्टरी परिभाषित करें जहाँ आप अपना OneNote डॉक्यूमेंट सेव करना चाहते हैं:

```java
String dataDir = "Your Document Directory";
```

## चरण 2: डॉक्यूमेंट ऑब्जेक्ट बनाएं

एक `Document` ऑब्जेक्ट इंस्टैंशिएट करें:

```java
Document doc = new Document();
```

## चरण 3: पेज बनाएं

पेज ऑब्जेक्ट्स को इनिशियलाइज़ करें और उनके लेवल सेट करें। लेवल सेट करने से तय होता है कि पेज रूट पेज है या सब‑पेज:

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## चरण 4: पेज में नोड्स जोड़ें

### पहले पेज में नोड्स जोड़ना

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text = new RichText().append("First page.");
text.setParagraphStyle(textStyle);

outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page1.appendChildLast(outline);
```

### दूसरे पेज में नोड्स जोड़ना

```java
Outline outline2 = new Outline();
OutlineElement outlineElem2 = new OutlineElement();
ParagraphStyle textStyle2 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text2 = new RichText().append("Second page.");
text2.setParagraphStyle(textStyle2);

outlineElem2.appendChildLast(text2);
outline2.appendChildLast(outlineElem2);
page2.appendChildLast(outline2);
```

### तीसरे पेज में नोड्स जोड़ना

```java
Outline outline3 = new Outline();
OutlineElement outlineElem3 = new OutlineElement();
ParagraphStyle textStyle3 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Broadway")
                                    .setFontSize(10);

RichText text3 = new RichText().append("Third page.");
text3.setParagraphStyle(textStyle3);

outlineElem3.appendChildLast(text3);
outline3.appendChildLast(outlineElem3);
page3.appendChildLast(outline3);
```

## चरण 5: पेज को डॉक्यूमेंट में जोड़ें

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## चरण 6: डॉक्यूमेंट को सेव करें

OneNote डॉक्यूमेंट को PDF (या इस उदाहरण में BMP) के रूप में सेव करें। `SaveFormat` बदलने से आप PDF में एक्सपोर्ट कर सकते हैं, जो “how to save OneNote PDF” आवश्यकता को पूरा करता है:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Handle exception
}
```

> **प्रो टिप:** सीधे PDF में एक्सपोर्ट करने के लिए `SaveFormat.Bmp` को `SaveFormat.Pdf` से बदलें।

बधाई हो! आपने सफलतापूर्वक रूट और सब‑पेज वाले OneNote डॉक्यूमेंट को बनाया और Aspose.Note for Java का उपयोग करके **OneNote PDF को कैसे सेव करें** सीख लिया।

## यह क्यों महत्वपूर्ण है

- **पदानुक्रमित संगठन:** रूट और सब‑पेज आपको OneNote के अंदर फ़ोल्डर स्ट्रक्चर की नकल करने देते हैं।  
- **स्मूद PDF एक्सपोर्ट:** एक बार व्यवस्थित हो जाने पर, PDF में एक्सपोर्ट करने से पदानुक्रम बरकरार रहता है, जिससे अंतिम दस्तावेज़ पढ़ने और शेयर करने में आसान होता है।  
- **ऑटोमेशन:** कोड को बड़े Java एप्लिकेशन में इंटीग्रेट किया जा सकता है, जिससे स्ट्रक्चर्ड नोटबुक्स का बैच निर्माण संभव हो जाता है।

## सामान्य त्रुटियाँ और उनके समाधान

| समस्या | कारण | समाधान |
|-------|-------|----------|
| पेज एक ही लेवल पर दिख रहे हैं | `setLevel` का गलत मान | रूट पेज के लिए `setLevel((byte) 1)` और सब‑पेज के लिए `setLevel((byte) 2)` (या अधिक) उपयोग करें। |
| PDF आउटपुट खाली दिख रहा है | `SaveFormat.Pdf` नहीं दिया गया या फ़ाइल पाथ गलत है | डायरेक्टरी मौजूद है यह सुनिश्चित करें और `SaveFormat.Pdf` उपयोग करें। |
| फ़ॉन्ट लागू नहीं हो रहा | फ़ॉन्ट नाम गलत या सिस्टम में फ़ॉन्ट नहीं है | सुनिश्चित करें कि फ़ॉन्ट (जैसे “David Transparent”) कोड चलाने वाले मशीन पर इंस्टॉल है। |

## अक्सर पूछे जाने वाले प्रश्न

**प्रश्न: क्या मैं Aspose.Note for Java का उपयोग करके कई लेवल के सब‑पेज बना सकता हूँ?**  
उत्तर: हाँ, आप उच्च लेवल नंबर सेट करके गहरी पदानुक्रम बना सकते हैं (उदाहरण के लिए, तीसरे लेवल के सब‑पेज के लिए `setLevel((byte) 3)`).

**प्रश्न: क्या Aspose.Note for Java विभिन्न Java IDEs के साथ संगत है?**  
उत्तर: बिल्कुल। यह IntelliJ IDEA, Eclipse, NetBeans और किसी भी Java‑डिवेलपमेंट‑सपोर्टेड IDE के साथ काम करता है।

**प्रश्न: क्या मैं अपने OneNote डॉक्यूमेंट में टेक्स्ट फ़ॉर्मेटिंग कस्टमाइज़ कर सकता हूँ?**  
उत्तर: हाँ। प्रत्येक `RichText` एलिमेंट के लिए फ़ॉन्ट नाम, साइज, रंग आदि सेट करने हेतु `ParagraphStyle` का उपयोग करें।

**प्रश्न: क्या Aspose.Note for Java BMP के अलावा अन्य फ़ॉर्मेट में डॉक्यूमेंट सेव कर सकता है?**  
उत्तर: हाँ। समर्थित फ़ॉर्मेट में PDF, PNG, JPEG, DOCX आदि शामिल हैं। `SaveFormat` एनेम को उसी अनुसार बदलें।

**प्रश्न: क्या Aspose.Note for Java का ट्रायल वर्ज़न उपलब्ध है?**  
उत्तर: हाँ, आप Aspose वेबसाइट से फ्री ट्रायल डाउनलोड कर सकते हैं।

## निष्कर्ष

अपने OneNote नोटबुक को स्पष्ट पदानुक्रमित संरचना के साथ व्यवस्थित करना और उन्हें PDF में एक्सपोर्ट करना आपके नोट्स को अधिक सुलभ और शेयर करने योग्य बनाता है। ऊपर दिए गए चरणों का पालन करके आप अब **OneNote PDF को कैसे सेव करें** और **sub pages onenote** शैली को प्रोग्रामेटिकली Aspose.Note for Java के साथ लागू करना जानते हैं।

---

**अंतिम अपडेट:** 2026-01-07  
**टेस्टेड विथ:** Aspose.Note for Java 24.11 (latest)  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}