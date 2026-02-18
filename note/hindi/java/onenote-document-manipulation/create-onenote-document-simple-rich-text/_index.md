---
date: 2026-02-18
description: जावा में Aspose.Note का उपयोग करके OneNote दस्तावेज़ बनाते समय पैराग्राफ
  शैली सेट करना और आउटलाइन तत्व जोड़ना सीखें। OneNote को PDF में निर्यात करें, OneNote
  को PDF के रूप में सहेजें, और OneNote फ़ाइलें आसानी से बनाएं।
linktitle: Set Paragraph Style while Creating OneNote Document in Java
second_title: Aspose.Note Java API
title: OneNote को PDF में निर्यात करें – Java में OneNote दस्तावेज़ बनाते समय पैराग्राफ
  शैली सेट करें
url: /hi/java/onenote-document-manipulation/create-onenote-document-simple-rich-text/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote दस्तावेज़ को Java में बनाते समय पैराग्राफ शैली सेट करें

## परिचय

आज के तेज़ गति वाले विकास परिदृश्य में, प्रोग्रामेटिक रूप से **OneNote को PDF में निर्यात** करने में सक्षम होना परिष्कृत, शेयर‑तैयार दस्तावेज़ बनाने के लिए आवश्यक है। यह ट्यूटोरियल आपको OneNote फ़ाइल बनाने, एक कस्टम पैराग्राफ शैली लागू करने, और अंत में Aspose.Note for Java का उपयोग करके **OneNote को PDF में निर्यात** करने की प्रक्रिया दिखाता है। चाहे आप रिपोर्टिंग इंजन, स्वचालित नोट‑लेने का समाधान, या दस्तावेज़‑परिवर्तन सेवा बना रहे हों, यहाँ कवर की गई तकनीकें आपको सटीक फ़ॉर्मेटिंग नियंत्रण के साथ **OneNote को PDF के रूप में सहेजने** में मदद करेंगी।

## त्वरित उत्तर
- **set paragraph style** का क्या अर्थ है? यह फ़ॉन्ट, आकार, रंग और अन्य फ़ॉर्मेटिंग को टेक्स्ट के पैराग्राफ पर लागू करता है।  
- **क्या मैं परिणाम को PDF में निर्यात कर सकता हूँ?** हाँ – ट्यूटोरियल OneNote फ़ाइल को PDF के रूप में सहेजने के साथ समाप्त होता है।  
- **क्या मुझे Aspose.Note के लिए लाइसेंस चाहिए?** मूल्यांकन के लिए एक मुफ्त ट्रायल काम करता है; उत्पादन के लिए लाइसेंस आवश्यक है।  
- **कौन से IDE समर्थित हैं?** कोई भी Java IDE – Eclipse, IntelliJ IDEA, NetBeans, आदि।  
- **इम्प्लीमेंटेशन में कितना समय लगेगा?** बेसिक दस्तावेज़ के लिए लगभग 10‑15 मिनट।

## Aspose.Note में “set paragraph style” क्या है?
पैराग्राफ शैली सेट करना एक `ParagraphStyle` ऑब्जेक्ट (फ़ॉन्ट नाम, आकार, रंग, आदि) को कॉन्फ़िगर करने और इसे एक `RichText` नोड से जोड़ने को दर्शाता है। यह आपको OneNote पेज के भीतर टेक्स्ट के दिखने के तरीके पर पूर्ण नियंत्रण देता है।

## OneNote में पैराग्राफ शैली कैसे सेट करें?
एक शैली लागू करना इतना सरल है कि आप एक `ParagraphStyle` इंस्टेंस बनाते हैं, उसकी प्रॉपर्टीज़ को कस्टमाइज़ करते हैं, और इसे एक `RichText` एलिमेंट को असाइन करते हैं। स्टाइल ऑब्जेक्ट तैयार होने पर API इसे एक‑लाइन ऑपरेशन बनाता है।

## OneNote को PDF में निर्यात क्यों करें?
- **सुसंगत ब्रांडिंग:** बाहरी रूप से नोट्स साझा करते समय कॉरपोरेट फ़ॉन्ट और रंग संरक्षित रखें।  
- **पढ़ने योग्य:** PDF सटीक लेआउट को बनाए रखता है, जिससे यह प्रिंटिंग या आर्काइविंग के लिए आदर्श बनता है।  
- **क्रॉस‑प्लेटफ़ॉर्म एक्सेस:** प्राप्तकर्ता OneNote की आवश्यकता के बिना किसी भी डिवाइस पर PDF देख सकते हैं।

## पूर्वापेक्षाएँ

शुरू करने से पहले, सुनिश्चित करें कि आपके पास है:

1. **Java Development Kit (JDK) 1.8+** – कोई भी नवीनतम JDK काम करेगा।  
2. **Aspose.Note for Java** – नवीनतम JAR [Aspose.Note डाउनलोड पेज](https://releases.aspose.com/note/java/) से डाउनलोड करें।  
3. **एक IDE** (Eclipse, IntelliJ IDEA, या NetBeans) सैंपल को कंपाइल और रन करने के लिए।  

> **Pro tip:** Maven के माध्यम से या अपने IDE में JAR को मैन्युअली रेफ़रेंस करके Aspose.Note JAR को अपने प्रोजेक्ट की क्लासपाथ में जोड़ें।

## पैकेज इम्पोर्ट करें

पहले, उन क्लासेज़ को इम्पोर्ट करें जिनकी हमें आवश्यकता होगी। यह ब्लॉक अपरिवर्तित रहता है।

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

> `ParagraphStyle` क्लास ट्यूटोरियल में बाद में **set paragraph style** करने की कुंजी है।

## स्टेप‑बाय‑स्टेप गाइड

नीचे प्रत्येक ऑपरेशन का संक्षिप्त walkthrough दिया गया है। कोड ब्लॉक्स मूल सैंपल के समान हैं; हमने केवल व्याख्यात्मक टेक्स्ट जोड़ा है।

### स्टेप 1: दस्तावेज़ डायरेक्टरी सेट करें
परिभाषित करें कि उत्पन्न फ़ाइलें कहाँ सहेजी जाएँगी।

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"` को अपने मशीन पर एक absolute या relative पाथ से बदलें।

### स्टेप 2: Document ऑब्जेक्ट इनिशियलाइज़ करें
रूट `Document` बनाएं जो OneNote फ़ाइल का प्रतिनिधित्व करता है।

```java
Document doc = new Document();
```

### स्टेप 3: Page ऑब्जेक्ट इनिशियलाइज़ करें
एक OneNote फ़ाइल में एक या अधिक पेज होते हैं; हम एक सिंगल पेज से शुरू करते हैं।

```java
Page page = new Page();
```

### स्टेप 4: Outline ऑब्जेक्ट इनिशियलाइज़ करें
Outlines आउटलाइन एलिमेंट्स के कंटेनर के रूप में कार्य करते हैं (इन्हें सेक्शन मानें)।

```java
Outline outline = new Outline();
```

### स्टेप 5: OutlineElement ऑब्जेक्ट इनिशियलाइज़ करें
यहाँ हम **outline element** जोड़ते हैं जो हमारे rich text को रखेगा।

```java
OutlineElement outlineElem = new OutlineElement();
```

### स्टेप 6: टेक्स्ट स्टाइल सेट करें (Set Paragraph Style)
```java
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```

`ParagraphStyle` इंस्टेंस फ़ॉन्ट, आकार, और रंग को परिभाषित करता है—यह वह जगह है जहाँ हम आगामी टेक्स्ट नोड के लिए **set paragraph style** करते हैं।

### स्टेप 7: RichText ऑब्जेक्ट इनिशियलाइज़ करें
```java
RichText text = new RichText().append("Hello OneNote text!");
text.setParagraphStyle(textStyle);
```

हम एक `RichText` नोड बनाते हैं, एक साधारण स्ट्रिंग डालते हैं, और पहले परिभाषित स्टाइल को अटैच करते हैं।

### स्टेप 8: RichText नोड को OutlineElement में जोड़ें
```java
outlineElem.appendChildLast(text);
```

अब स्टाइल्ड टेक्स्ट OutlineElement के अंदर रहता है।

### स्टेप 9: OutlineElement नोड को Outline में जोड़ें
```java
outline.appendChildLast(outlineElem);
```

अब Outline में वह एलिमेंट है जो हमारे पैराग्राफ को रखता है।

### स्टेप 10: Outline नोड को Page में जोड़ें
```java
page.appendChildLast(outline);
```

हम Outline को Page पर रखते हैं।

### स्टेप 11: Page नोड को Document में जोड़ें
```java
doc.appendChildLast(page);
```

Document में अब एक सिंगल पेज है जिसमें हमारा स्टाइल्ड टेक्स्ट है।

### स्टेप 12: Document को सहेजें (Export OneNote PDF)
```java
doc.save(dataDir + "CreateOneNoteDocumentWithSimpleRichText_out.pdf", SaveFormat.Pdf);
```

`save` मेथड OneNote फ़ाइल लिखता है और **OneNote PDF** को एक ही स्टेप में निर्यात करता है। यदि आपको नेटिव फ़ॉर्मेट चाहिए तो आप `SaveFormat.One` का उपयोग करके `.one` के रूप में भी सहेज सकते हैं।

## सामान्य समस्याएँ और समाधान

| समस्या | कारण | समाधान |
|-------|--------|-----|
| **फ़ाइल नहीं मिली** | `dataDir` एक गैर‑मौजूद फ़ोल्डर की ओर इशारा करता है। | सुनिश्चित करें कि डायरेक्टरी मौजूद है या प्रोग्रामेटिकली बनाएं (`new File(dataDir).mkdirs();`)। |
| **खाली PDF** | सहेजने से पहले कोई कंटेंट नहीं जोड़ा गया था। | पुष्टि करें कि `RichText` नोड जोड़ दिया गया है और स्टाइल सेट है। |
| **असमर्थित फ़ॉन्ट** | फ़ॉन्ट नाम सिस्टम पर इंस्टॉल नहीं है। | `"Arial"` जैसे सामान्य फ़ॉन्ट का उपयोग करें या प्रोजेक्ट में फ़ॉन्ट एम्बेड करें। |

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या Aspose.Note टेबल या इमेज जैसी जटिल फ़ॉर्मेटिंग को संभाल सकता है?**  
A: हाँ, API टेबल, इमेज, हाइपरलिंक, और अधिक उन्नत लेआउट फीचर को सपोर्ट करता है।

**Q: क्या **OneNote PDF को** वापस OneNote फ़ाइल में **convert** करना संभव है?**  
A: सीधे रूपांतरण उपलब्ध नहीं है, लेकिन आप PDF कंटेंट निकालकर API का उपयोग करके OneNote दस्तावेज़ फिर से बना सकते हैं।

**Q: क्या लाइब्रेरी Linux/macOS वातावरण में काम करती है?**  
A: बिल्कुल। Aspose.Note for Java प्लेटफ़ॉर्म‑इंडिपेंडेंट है; बस सुनिश्चित करें कि JDK इंस्टॉल है।

**Q: मैं कई पेज या outlines कैसे जोड़ूँ?**  
A: अतिरिक्त `Page` और `Outline` ऑब्जेक्ट बनाएं, फिर उन्हें `Document` में सिंगल‑पेज उदाहरण की तरह जोड़ें।

**Q: मैं और उदाहरण कहाँ पा सकता हूँ?**  
A: आधिकारिक Aspose.Note डाक्यूमेंटेशन और [सपोर्ट फ़ोरम](https://forum.aspose.com/c/note/28) में कई कोड सैंपल्स हैं।

## निष्कर्ष

अब आपने देखा कि कैसे **set paragraph style**, **add outline element**, और Aspose.Note for Java का उपयोग करके **OneNote फ़ाइल जनरेट** की जा सकती है जिसे **PDF में निर्यात** किया जा सकता है। निर्माण प्रक्रिया में शुरुआती चरण में स्टाइल्ड टेक्स्ट को शामिल करने से अंतिम दस्तावेज़ प्रोफेशनल दिखता है और कोई भी बाद का **convert OneNote PDF** ऑपरेशन फ़ॉर्मेटिंग को बरकरार रखता है। अपने प्रोजेक्ट की जरूरतों के अनुसार इस बुनियाद को इमेज, टेबल, या कस्टम मेटाडेटा के साथ विस्तारित करने में संकोच न करें।

---

**अंतिम अपडेट:** 2026-02-18  
**परीक्षित संस्करण:** Aspose.Note for Java 24.11 (नवीनतम रिलीज़)  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}