---
date: 2025-11-29
description: Aspose.Note for Java का उपयोग करके OneNote पेज को PNG में निर्यात करना
  सीखें। पेज इंडेक्स सेट करने, पेज को परिवर्तित करने और छवि को सहेजने के लिए चरण‑दर‑चरण
  निर्देशों का पालन करें।
language: hi
linktitle: Export OneNote Page to PNG Image in Java
second_title: Aspose.Note Java API
title: Aspose.Note का उपयोग करके जावा में OneNote पेज को PNG इमेज में निर्यात करें
url: /java/onenote-document-loading/convert-page-to-png-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java में Aspose.Note का उपयोग करके OneNote पेज को PNG इमेज में एक्सपोर्ट करें

## परिचय

इस ट्यूटोरियल में आप **OneNote पेज को PNG इमेज में एक्सपोर्ट** करने का तरीका Aspose.Note for Java लाइब्रेरी का उपयोग करके सीखेंगे। हम आपको पर्यावरण सेटअप से लेकर पेज इंडेक्स सेट करने और अंत में पेज को उच्च‑गुणवत्ता वाले PNG फ़ाइल के रूप में सेव करने तक सभी चरणों से परिचित कराएंगे। अंत तक, आप इस क्षमता को किसी भी Java एप्लिकेशन में जोड़ सकेंगे जो OneNote दस्तावेज़ों के साथ काम करता है।

## त्वरित उत्तर
- **कौन सी लाइब्रेरी चाहिए?** Aspose.Note for Java.  
- **क्या मैं एकल पेज एक्सपोर्ट कर सकता हूँ?** हाँ—सटीक पेज को लक्षित करने के लिए `setPageIndex` का उपयोग करें।  
- **समर्थित इमेज फ़ॉर्मेट?** PNG, JPEG, GIF, BMP, TIFF (यहाँ PNG दिखाया गया है)।  
- **क्या लाइसेंस की आवश्यकता है?** एक फ्री ट्रायल उपलब्ध है; प्रोडक्शन के लिए लाइसेंस आवश्यक है।  
- **इम्प्लीमेंटेशन में कितना समय लगेगा?** बेसिक कन्वर्ज़न के लिए आमतौर पर 10 मिनट से कम।

## “Export OneNote page” क्या है?
OneNote पेज को एक्सपोर्ट करना मतलब `.one` दस्तावेज़ के भीतर किसी विशिष्ट पेज को एक स्वतंत्र इमेज फ़ाइल (यहाँ PNG) में बदलना है। यह तब उपयोगी होता है जब आपको OneNote सामग्री को OneNote के बाहर शेयर, एम्बेड या प्रोसेस करना हो।

## OneNote को PNG में बदलने के लिए Aspose.Note for Java क्यों उपयोग करें?
- **Microsoft Office पर निर्भरता नहीं** – वह किसी भी प्लेटफ़ॉर्म पर काम करता है जहाँ Java चलती है।  
- **सूक्ष्म नियंत्रण** – आप `setPageIndex` के माध्यम से कोई भी पेज चुन सकते हैं।  
- **उच्च‑गुणवत्ता आउटपुट** – PNG वेक्टर ग्राफ़िक्स और टेक्स्ट की स्पष्टता को बनाए रखता है।  
- **बैच‑रेडी** – बड़े पैमाने पर कन्वर्ज़न के लिए पेजों पर लूप करना आसान है।

## पूर्वापेक्षाएँ

शुरू करने से पहले सुनिश्चित करें कि आपके पास हैं:

1. **Java Development Kit (JDK)** – संस्करण 8 या उससे ऊपर।  
2. **Aspose.Note for Java** – नवीनतम JAR [Aspose वेबसाइट](https://releases.aspose.com/note/java/) से डाउनलोड करें।  
3. **एक OneNote दस्तावेज़** (`.one`) जिसमें वह पेज हो जिसे आप एक्सपोर्ट करना चाहते हैं।

## पैकेज इम्पोर्ट करें

सबसे पहले, आवश्यक Java क्लासेज़ इम्पोर्ट करें:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.LoadOptions;
import com.aspose.note.SaveFormat;
```

 चरण‑दर‑चरण गाइड

### चरण 1: OneNote दस्तावेज़ लोड करें

```java
// Load the document into Aspose.Note.
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", new LoadOptions());
```

हम `Document` क्लास का उपयोग करके डिस्क से OneNote फ़ाइल पढ़ते हैं। `LoadOptions` ऑब्जेक्ट आपको लोडिंग व्यवहार को आवश्यकतानुसार कस्टमाइज़ करने की सुविधा देता है।

### चरण 2: ImageSaveOptions इनिशियलाइज़ करें

```java
// Initialize ImageSaveOptions object
ImageSaveOptions opts = new ImageSaveOptions(SaveFormat.Png);
```

`ImageSaveOptions` Aspose.Note को बताता है कि हम आउटपुट **PNG** फ़ॉर्मेट में चाहते हैं। आप `SaveFormat` बदलकर JPEG, BMP आदि भी चुन सकते हैं।

### चरण 3: पेज इंडेक्स सेट करें (OneNote पेज कैसे कन्वर्ट करें)

```java
// set page index
opts.setPageIndex(0);
```

`setPageIndex` मेथड वह पेज चुनता है जिसे एक्सपोर्ट करना है। पेज नंबरिंग **0** से शुरू होती है, इसलिए `0` पहला पेज दर्शाता है। किसी अन्य पेज को एक्सपोर्ट करने के लिए इस मान को बदलें।

### चरण 4: दस्तावेज़ को PNG के रूप में सेव करें (OneNote को PNG में सेव करें)

```java
// Save the document as PNG.
oneFile.save(dataDir + "ConvertSpecificPageToPngImage_out.png", opts);
```

`save` कॉल चयनित पेज को डिस्क पर PNG फ़ाइल के रूप में लिखता है। फ़ाइल नाम `ConvertSpecificPageToPngImage_out.png` केवल एक उदाहरण है—आप इसे अपनी पसंद के अनुसार रख सकते हैं।

## सामान्य समस्याएँ और टिप्स

- **गलत पेज इंडेक्स** – याद रखें कि इंडेक्सिंग 0 से शुरू होती है। यदि आपको खाली इमेज मिल रही है, तो इंडेक्स मान की जाँच करें।  
- **Aspose.Note JAR नहीं मिला** – सुनिश्चित करें कि JAR आपके क्लासपाथ में है; नहीं तो `ClassNotFoundException` दिखेगा।  
- **बड़ी पेजें** – बहुत बड़े पेजों के लिए JVM हीप साइज (`-Xmx`) बढ़ाएँ ताकि `OutOfMemoryError` से बचा जा सके।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं Aspose.Note for Java का उपयोग करके एक ही बार में कई पेज को PNG इमेज में कन्वर्ट कर सकता हूँ?
A1: हाँ, आप दस्तावेज़ के पेजों पर लूप कर सकते हैं, `opts.setPageIndex(i)` को अपडेट करें, और प्रत्येक इटरेशन में `save` कॉल करें।

### Q2: क्या Aspose.Note for Java PNG के अलावा अन्य इमेज फ़ॉर्मेट सपोर्ट करता है?
A2: बिल्कुल। आप `ImageSaveOptions` में `SaveFormat.Jpeg`, `SaveFormat.Gif`, `SaveFormat.Bmp`, या `SaveFormat.Tiff` सेट कर सकते हैं।

### Q3: क्या Aspose.Note for Java के लिए फ्री ट्रायल उपलब्ध है?
A3: हाँ, आप [वेबसाइट](https://releases.aspose.com/) से फ्री ट्रायल डाउनलोड कर सकते हैं।

### Q4: यदि मैं Aspose.Note for Java के साथ कोई समस्या सामना करता हूँ तो क्या तकनीकी सहायता मिल सकती है?
A4: बिल्कुल, आप Aspose कम्युनिटी फ़ोरम पर समर्थन प्राप्त कर सकते हैं [यहाँ](https://forum.aspose.com/c/note/28)।

### Q5: Aspose.Note for Java का लाइसेंस कहाँ खरीद सकता हूँ?
A5: आप लाइसेंस [पर्चेज पेज](https://purchase.aspose.com/buy) से खरीद सकते हैं।

### Q6: मैं ऐसे पेज को कैसे एक्सपोर्ट करूँ जिसमें एम्बेडेड इमेज हों?
A6: एम्बेडेड इमेज़ स्वचालित रूप से PNG आउटपुट में रेंडर हो जाते हैं; अतिरिक्त कोड की आवश्यकता नहीं है।

### Q7: क्या मैं DPI या इमेज रिज़ॉल्यूशन सेट कर सकता हूँ?
A7: हाँ, `save` कॉल करने से पहले `opts.setResolution(int dpi)` का उपयोग करके आउटपुट क्वालिटी नियंत्रित कर सकते हैं।

---

**अंतिम अपडेट:** 2025-11-29  
**टेस्टेड वर्ज़न:** Aspose.Note for Java 24.11 (नवीनतम)  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
