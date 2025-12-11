---
date: 2025-12-08
description: जावा में Aspose.Note का उपयोग करके OneNote दस्तावेज़ बनाते समय पैराग्राफ
  शैली सेट करना और आउटलाइन तत्व जोड़ना सीखें। OneNote को PDF में निर्यात करें और आसानी
  से OneNote फ़ाइलें जनरेट करें।
language: hi
linktitle: Set Paragraph Style while Creating OneNote Document in Java
second_title: Aspose.Note Java API
title: जावा में वननोट दस्तावेज़ बनाते समय पैराग्राफ शैली सेट करें
url: /java/onenote-document-manipulation/create-onenote-document-simple-rich-text/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java में OneNote दस्तावेज़ बनाते समय पैराग्राफ शैली सेट करें

## परिचय

आज के तेज़ गति वाले विकास परिदृश्य में, प्रोग्रामेटिक रूप से **पैराग्राफ शैली सेट** करना परिष्कृत OneNote फ़ाइलें बनाने के लिए आवश्यक है। यह ट्यूटोरियल आपको चरण‑दर‑चरण दिखाता है कि कैसे सरल रिच टेक्स्ट के साथ OneNote दस्तावेज़ बनाएं, कस्टम पैराग्राफ फ़ॉर्मेटिंग लागू करें, और अंत में Aspose.Note for Java का उपयोग करके **OneNote को PDF में निर्यात** करें। चाहे आप रिपोर्टिंग इंजन, स्वचालित नोट‑लेने का समाधान, या दस्तावेज़‑परिवर्तन सेवा बना रहे हों, यहाँ कवर की गई तकनीकें आपको **OneNote फ़ाइलें बनाना** मदद करेंगी जो बिल्कुल वही दिखेंगी जैसा आप चाहते हैं।

## त्वरित उत्तर
- **“पैराग्राफ शैली सेट” का क्या अर्थ है?** यह फ़ॉन्ट, आकार, रंग और अन्य फ़ॉर्मेटिंग को टेक्स्ट के पैराग्राफ पर लागू करता है।  
- **क्या मैं परिणाम को PDF में निर्यात कर सकता हूँ?** हां – ट्यूटोरियल OneNote फ़ाइल को PDF के रूप में सहेजने के साथ समाप्त होता है।  
- **क्या मुझे Aspose.Note के लिए लाइसेंस चाहिए?** मूल्यांकन के लिए एक फ्री ट्रायल काम करता है; उत्पादन के लिए लाइसेंस आवश्यक है।  
- **कौन से IDE समर्थित हैं?** कोई भी Java IDE – Eclipse, IntelliJ IDEA, NetBeans, आदि।  
- **इम्प्लीमेंटेशन में कितना समय लगता है?** एक बुनियादी दस्तावेज़ के लिए लगभग 10‑15 मिनट।

## Aspose.Note में “पैराग्राफ शैली सेट” क्या है?
पैराग्राफ शैली सेट करना एक `ParagraphStyle` ऑब्जेक्ट (फ़ॉन्ट नाम, आकार, रंग, आदि) को कॉन्फ़िगर करने और उसे एक `RichText` नोड से जोड़ने को दर्शाता है। यह आपको OneNote पेज के भीतर टेक्स्ट कैसे दिखेगा, इस पर पूर्ण नियंत्रण देता है।

## OneNote फ़ाइलें बनाते समय पैराग्राफ शैली क्यों सेट करें?
- **सुसंगत ब्रांडिंग:** कॉर्पोरेट फ़ॉन्ट और रंग स्वचालित रूप से लागू करें।  
- **पढ़ने योग्य:** बड़े फ़ॉन्ट या विशिष्ट रंग पहुंचयोग्यता को बेहतर बनाते हैं।  
- **निर्यात की सटीकता:** जब आप बाद में **OneNote PDF को कनवर्ट** करते हैं, तो स्टाइल किया गया टेक्स्ट संरक्षित रहता है।  

## पूर्वापेक्षाएँ

शुरू करने से पहले, सुनिश्चित करें कि आपके पास है:

1. **Java Development Kit (JDK) 1.8+** – कोई भी नवीनतम JDK काम करेगा।  
2. **Aspose.Note for Java** – नवीनतम JAR को [Aspose.Note download page](https://releases.aspose.com/note/java/) से डाउनलोड करें।  
3. **एक IDE** (Eclipse, IntelliJ IDEA, या NetBeans) नमूना को संकलित और चलाने के लिए।  

> **Pro tip:** Maven के माध्यम से या अपने IDE में JAR को मैन्युअली रेफ़र करके Aspose.Note JAR को अपने प्रोजेक्ट की क्लासपाथ में जोड़ें।

## पैकेज आयात करें

पहले, उन क्लासों को आयात करें जिनकी हमें आवश्यकता होगी। यह ब्लॉक अपरिवर्तित रहता है।

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

`ParagraphStyle` क्लास बाद में ट्यूटोरियल में **पैराग्राफ शैली सेट** करने की कुंजी है।

## चरण‑दर‑चरण गाइड

नीचे प्रत्येक ऑपरेशन का संक्षिप्त walkthrough दिया गया है। कोड ब्लॉक्स मूल नमूने जैसा ही हैं; हम केवल व्याख्यात्मक टेक्स्ट जोड़ते हैं।

### चरण 1: दस्तावेज़ डायरेक्टरी सेट करें
परिभाषित करें कि उत्पन्न फ़ाइलें कहाँ सहेजी जाएँगी।

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"` को अपने मशीन पर एक पूर्ण या सापेक्ष पथ से बदलें।

### चरण 2: Document ऑब्जेक्ट को इनिशियलाइज़ करें
`Document` रूट बनाएं जो OneNote फ़ाइल का प्रतिनिधित्व करता है।

```java
Document doc = new Document();
```

### चरण 3: Page ऑब्जेक्ट को इनिशियलाइज़ करें
एक OneNote फ़ाइल में एक या अधिक पेज होते हैं; हम एक सिंगल पेज से शुरू करते हैं।

```java
Page page = new Page();
```

### चरण 4: Outline ऑब्जेक्ट को इनिशियलाइज़ करें
Outlines आउटलाइन एलिमेंट्स के कंटेनर के रूप में कार्य करते हैं (इन्हें सेक्शन मानें)।

```java
Outline outline = new Outline();
```

### चरण 5: OutlineElement ऑब्जेक्ट को इनिशियलाइज़ करें
यहाँ हम **outline element जोड़ते** हैं जो हमारे रिच टेक्स्ट को रखेगा।

```java
OutlineElement outlineElem = new OutlineElement();
```

### चरण 6: टेक्स्ट शैली सेट करें (पैराग्राफ शैली सेट करें)
```java
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```

`ParagraphStyle` इंस्टेंस फ़ॉन्ट, आकार और रंग को परिभाषित करता है—यह वह जगह है जहाँ हम आगामी टेक्स्ट नोड के लिए **पैराग्राफ शैली सेट** करते हैं।

### चरण 7: RichText ऑब्जेक्ट को इनिशियलाइज़ करें
```java
RichText text = new RichText().append("Hello OneNote text!");
text.setParagraphStyle(textStyle);
```

हम एक `RichText` नोड बनाते हैं, एक साधारण स्ट्रिंग डालते हैं, और पहले परिभाषित शैली को संलग्न करते हैं।

### चरण 8: RichText नोड को OutlineElement में जोड़ें
```java
outlineElem.appendChildLast(text);
```

अब स्टाइल किया हुआ टेक्स्ट OutlineElement के अंदर रहता है।

### चरण 9: OutlineElement नोड को Outline में जोड़ें
```java
outline.appendChildLast(outlineElem);
```

अब Outline में वह एलिमेंट है जो हमारे पैराग्राफ को रखता है।

### चरण 10: Outline नोड को Page में जोड़ें
```java
page.appendChildLast(outline);
```

हम Outline को पेज पर रखते हैं।

### चरण 11: Page नोड को Document में जोड़ें
```java
doc.appendChildLast(page);
```

अब दस्तावेज़ में हमारे स्टाइल किए हुए टेक्स्ट के साथ एक सिंगल पेज है।

### चरण 12: दस्तावेज़ सहेजें (OneNote PDF निर्यात करें)
```java
doc.save(dataDir + "CreateOneNoteDocumentWithSimpleRichText_out.pdf", SaveFormat.Pdf);
```

`save` मेथड OneNote फ़ाइल लिखता है और **OneNote PDF को एक ही चरण में निर्यात** करता है। यदि आपको मूल फ़ॉर्मेट चाहिए तो आप `SaveFormat.One` का उपयोग करके `.one` के रूप में भी सहेज सकते हैं।

## सामान्य समस्याएँ और समाधान

| समस्या | कारण | समाधान |
|--------|------|--------|
| **फ़ाइल नहीं मिली** | `dataDir` एक गैर‑मौजूद फ़ोल्डर की ओर इशारा करता है। | सुनिश्चित करें कि डायरेक्टरी मौजूद है या इसे प्रोग्रामेटिक रूप से बनाएं (`new File(dataDir).mkdirs();`). |
| **खाली PDF** | सहेजने से पहले कोई कंटेंट नहीं जोड़ा गया था। | जाँचें कि `RichText` नोड जोड़ा गया है और शैली सेट है। |
| **असमर्थित फ़ॉन्ट** | फ़ॉन्ट नाम सिस्टम पर स्थापित नहीं है। | `"Arial"` जैसे सामान्य फ़ॉन्ट का उपयोग करें या फ़ॉन्ट को प्रोजेक्ट में एम्बेड करें। |

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या Aspose.Note टेबल या इमेज जैसी जटिल फ़ॉर्मेटिंग को संभाल सकता है?**  
A: हां, API टेबल, इमेज, हाइपरलिंक और अधिक उन्नत लेआउट फीचर को सपोर्ट करता है।

**Q: क्या **OneNote PDF को** वापस OneNote फ़ाइल में **कनवर्ट** करना संभव है?**  
A: सीधे रूपांतरण उपलब्ध नहीं है, लेकिन आप PDF कंटेंट निकालकर API का उपयोग करके OneNote दस्तावेज़ फिर से बना सकते हैं।

**Q: क्या लाइब्रेरी Linux/macOS वातावरण में काम करती है?**  
A: बिल्कुल। Aspose.Note for Java प्लेटफ़ॉर्म‑निर्भर नहीं है; बस यह सुनिश्चित करें कि JDK स्थापित है।

**Q: मैं कई पेज या outlines कैसे जोड़ूँ?**  
A: अतिरिक्त `Page` और `Outline` ऑब्जेक्ट बनाएं, फिर उन्हें `Document` में सिंगल‑पेज उदाहरण की तरह जोड़ें।

**Q: मैं और उदाहरण कहाँ पा सकता हूँ?**  
A: आधिकारिक Aspose.Note दस्तावेज़ और [सपोर्ट फ़ोरम](https://forum.aspose.com/c/note/28) में कई कोड नमूने हैं।

## निष्कर्ष

आपने अब देखा कि कैसे **पैराग्राफ शैली सेट** करें, **outline element जोड़ें**, और Aspose.Note for Java का उपयोग करके **OneNote फ़ाइल जनरेट** करें जिसे **PDF में निर्यात** किया जा सकता है। निर्माण प्रक्रिया में शुरुआती चरण में स्टाइल किया हुआ टेक्स्ट शामिल करने से अंतिम दस्तावेज़ पेशेवर दिखता है और कोई भी बाद का **OneNote PDF कनवर्ट** ऑपरेशन फ़ॉर्मेटिंग को बरकरार रखता है। अपने प्रोजेक्ट की जरूरतों को पूरा करने के लिए इस बुनियाद को इमेज, टेबल या कस्टम मेटाडेटा के साथ विस्तारित करने में संकोच न करें।

---

**अंतिम अपडेट:** 2025-12-08  
**परीक्षण किया गया:** Aspose.Note for Java 24.11 (नवीनतम रिलीज़)  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}