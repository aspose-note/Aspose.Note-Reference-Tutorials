---
date: 2026-04-30
description: Aspose.Note for Java का उपयोग करके OneNote को PDF के रूप में सहेजना और
  उप‑पृष्ठ जोड़ना सीखें। अपने नोट्स को प्रभावी ढंग से व्यवस्थित करने के लिए इस चरण‑दर‑चरण
  गाइड का पालन करें।
keywords:
- save onenote as pdf
- add sub pages onenote
- Aspose.Note Java
linktitle: OneNote को PDF के रूप में सहेजें और सब पेज जोड़ें
second_title: Aspose.Note Java API
title: OneNote को PDF के रूप में कैसे सहेजें और उप‑पृष्ठ जोड़ें
url: /hi/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote को PDF के रूप में सहेजें और उप‑पृष्ठ जोड़ें

## परिचय

इस ट्यूटोरियल में, आप Aspose.Note for Java का उपयोग करके रूट और सब‑पेज दोनों वाले दस्तावेज़ बनाते हुए **how to save onenote as pdf** की खोज करेंगे। अपने OneNote नोटबुक को स्पष्ट पदानुक्रम के साथ व्यवस्थित करने से नेविगेशन आसान हो जाता है, और PDF में निर्यात करने से आप अपने नोट्स को सार्वभौमिक रूप से पढ़े जाने योग्य फ़ॉर्मेट में साझा कर सकते हैं। हम आपको यह भी दिखाएंगे कि कैसे **add sub pages onenote** शैली में जोड़ें, ताकि आप आसानी से बहु‑स्तरीय संरचनाएँ बना सकें।

## त्वरित उत्तर

- **What does “save onenote as pdf” mean?** यह Aspose.Note for Java का उपयोग करके OneNote नोटबुक को PDF फ़ाइल में निर्यात करने को दर्शाता है।  
- **Which API is required?** Aspose.Note for Java आवश्यक क्लासेस और मेथड्स प्रदान करता है।  
- **Can I create hierarchical pages?** हाँ – रूट पेज और सब‑पेज बनाने के लिए पेज लेवल सेट करें।  
- **Do I need a license for production?** एक मुफ्त ट्रायल उपलब्ध है, लेकिन प्रोडक्शन उपयोग के लिए एक व्यावसायिक लाइसेंस आवश्यक है।  
- **Which formats can I export to?** PDF के अलावा आप BMP, PNG, JPEG, DOCX और अन्य फ़ॉर्मेट में निर्यात कर सकते हैं।

## OneNote को PDF के रूप में कैसे सहेजें

OneNote को PDF के रूप में सहेजने से प्रत्येक नोटबुक पेज एक स्थिर‑लेआउट दस्तावेज़ में बदल जाता है जो फ़ॉर्मेटिंग, छवियों और पेज पदानुक्रम को संरक्षित रखता है। यह नोट्स को साझा करने, संग्रहित करने या प्रिंट करने के लिए आदर्श है, जबकि मूल संरचना को अपरिवर्तित रखता है।

## OneNote में सब‑पृष्ठ क्यों जोड़ें?

सब‑पृष्ठ जोड़ने से आप संबंधित सामग्री को एक पैरेंट पेज के तहत समूहित कर सकते हैं, जो फ़ोल्डर‑जैसी संरचना को दर्शाता है। यह नोट्स की व्यवस्था को बेहतर बनाता है, खोज को तेज़ करता है, और जब नोटबुक को PDF में निर्यात किया जाता है तो पढ़ने का अनुभव बढ़ाता है।

## पूर्वापेक्षाएँ

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ हैं:

1. **Java Development Kit (JDK)** – सुनिश्चित करें कि आपके सिस्टम पर JDK स्थापित है।  
2. **Aspose.Note for Java** – Aspose.Note for Java को [website](https://purchase.aspose.com/buy) से डाउनलोड और इंस्टॉल करें।  
3. **Integrated Development Environment (IDE)** – IntelliJ IDEA, Eclipse, या NetBeans जैसे Java IDE चुनें।

## पैकेज आयात करें

अपने Java प्रोजेक्ट में आवश्यक पैकेज आयात करके शुरू करें:

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

## चरण 1: दस्तावेज़ निर्देशिका सेट करें

उस निर्देशिका को परिभाषित करें जहाँ आप अपना OneNote दस्तावेज़ सहेजना चाहते हैं:

```java
String dataDir = "Your Document Directory";
```

## चरण 2: दस्तावेज़ ऑब्जेक्ट बनाएं

`Document` ऑब्जेक्ट का उदाहरण बनाएं:

```java
Document doc = new Document();
```

## चरण 3: पृष्ठ बनाएं

पेज ऑब्जेक्ट को इनिशियलाइज़ करें और उनके लेवल सेट करें। लेवल सेट करने से निर्धारित होता है कि पेज रूट पेज है या सब‑पेज।

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## चरण 4: पृष्ठों में नोड्स जोड़ें

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

## चरण 5: दस्तावेज़ में पेज जोड़ें

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## चरण 6: दस्तावेज़ सहेजें

OneNote दस्तावेज़ को PDF (या इस उदाहरण में BMP) के रूप में सहेजें। `SaveFormat` बदलने से आप PDF में निर्यात कर सकते हैं, जो “save onenote as pdf” आवश्यकता को पूरा करता है:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Handle exception
}
```

> **Pro tip:** सीधे PDF में निर्यात करने के लिए, `SaveFormat.Bmp` को `SaveFormat.Pdf` से बदलें।

बधाई हो! आपने सफलतापूर्वक रूट और सब‑पेज वाले OneNote दस्तावेज़ बनाए हैं और Aspose.Note for Java का उपयोग करके **how to save onenote as pdf** सीखा है।

## यह क्यों महत्वपूर्ण है

- **Hierarchical organization:** रूट और सब‑पेज आपको OneNote के भीतर फ़ोल्डर संरचनाओं की नकल करने देते हैं।  
- **Seamless PDF export:** एक बार व्यवस्थित होने पर, PDF में निर्यात करने से पदानुक्रम संरक्षित रहता है, जिससे अंतिम दस्तावेज़ पढ़ने और साझा करने में आसान हो जाता है।  
- **Automation:** कोड को बड़े Java एप्लिकेशन में एकीकृत किया जा सकता है, जिससे संरचित नोटबुक की बैच निर्माण संभव हो जाता है।

## सामान्य समस्याएँ और उन्हें कैसे टालें

| समस्या | कारण | समाधान |
|-------|-------|----------|
| पेज एक ही स्तर पर दिख रहे हैं | `setLevel` मान गलत है | रूट पेज के लिए `setLevel((byte) 1)` और सब‑पेज के लिए `setLevel((byte) 2)` (या अधिक) का उपयोग करें। |
| PDF आउटपुट खाली दिख रहा है | `SaveFormat.Pdf` गायब है या फ़ाइल पाथ गलत है | डायरेक्टरी मौजूद है यह सुनिश्चित करें और `SaveFormat.Pdf` का उपयोग करें। |
| फ़ॉन्ट लागू नहीं हुआ | फ़ॉन्ट नाम गलत है या सिस्टम पर फ़ॉन्ट नहीं है | कोड चलाने वाले मशीन पर फ़ॉन्ट (जैसे “David Transparent”) स्थापित है यह सुनिश्चित करें। |

## अक्सर पूछे जाने वाले प्रश्न

**Q: Aspose.Note for Java का उपयोग करके मैं कई स्तरों के सब‑पेज बना सकता हूँ?**  
A: हाँ, आप उच्च स्तर संख्याएँ सेट करके गहरी पदानुक्रम बना सकते हैं (उदाहरण के लिए, तीसरे‑स्तर के सब‑पेज के लिए `setLevel((byte) 3)`).

**Q: क्या Aspose.Note for Java विभिन्न Java IDEs के साथ संगत है?**  
A: बिल्कुल। यह IntelliJ IDEA, Eclipse, NetBeans और किसी भी IDE के साथ काम करता है जो Java विकास का समर्थन करता है।

**Q: क्या मैं अपने OneNote दस्तावेज़ में टेक्स्ट के फ़ॉर्मेट को कस्टमाइज़ कर सकता हूँ?**  
A: हाँ। प्रत्येक `RichText` तत्व के लिए फ़ॉन्ट नाम, आकार, रंग और अन्य गुण सेट करने के लिए `ParagraphStyle` का उपयोग करें।

**Q: क्या Aspose.Note for Java BMP के अलावा अन्य फ़ॉर्मेट में दस्तावेज़ सहेजने का समर्थन करता है?**  
A: हाँ। समर्थित फ़ॉर्मेट में PDF, PNG, JPEG, DOCX और अधिक शामिल हैं। `SaveFormat` enum को तदनुसार बदलें।

**Q: क्या Aspose.Note for Java के लिए कोई ट्रायल संस्करण उपलब्ध है?**  
A: हाँ, आप Aspose वेबसाइट से मुफ्त ट्रायल डाउनलोड कर सकते हैं।

## निष्कर्ष

OneNote नोटबुक को स्पष्ट पदानुक्रमित संरचना में व्यवस्थित करना और उन्हें PDF के रूप में निर्यात करना आपके नोट्स को अधिक सुलभ और साझा करने योग्य बनाता है। ऊपर बताए गए चरणों का पालन करके, अब आप Aspose.Note for Java के साथ प्रोग्रामेटिक रूप से **how to save onenote as pdf** और **add sub pages onenote** शैली को जानते हैं।

---

**अंतिम अपडेट:** 2026-04-30  
**परीक्षण किया गया:** Aspose.Note for Java 24.11 (latest)  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}