---
date: 2025-11-29
description: जावा का उपयोग करके OneNote पेजों को इमेज में एक्सपोर्ट करना सीखें, और
  Aspose.Note के साथ OneNote पेज इमेज को कैसे कन्वर्ट करें, यह जानें। तेज़ इंटीग्रेशन
  के लिए हमारे चरण‑दर‑चरण गाइड का पालन करें।
linktitle: How to Export OneNote Page to Image Using Java
second_title: Aspose.Note Java API
title: जावा का उपयोग करके OneNote पेज को इमेज में निर्यात कैसे करें
url: /hi/java/onenote-document-loading/convert-page-to-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java का उपयोग करके OneNote पेज को इमेज में निर्यात कैसे करें

## परिचय

इस ट्यूटोरियल में, आप **OneNote पेज को इमेज फ़ाइलों में निर्यात** करना सीखेंगे Java के साथ Aspose.Note का उपयोग करके। OneNote पेज को इमेज में बदलना उपयोगी होता है जब आपको नोटबुक सामग्री को रिपोर्ट में एम्बेड करना हो, गैर‑OneNote उपयोगकर्ताओं के साथ स्नैपशॉट साझा करना हो, या दस्तावेज़ प्रबंधन प्रणालियों के लिए थंबनेल बनाना हो। हम प्रत्येक चरण को विस्तार से बताएँगे, प्रत्येक पंक्ति का महत्व समझाएँगे, और आउटपुट को कैसे कस्टमाइज़ करें दिखाएँगे।

## त्वरित उत्तर
- **कौनसी लाइब्रेरी आवश्यक है?** Aspose.Note for Java  
- **क्या मैं इमेज फ़ॉर्मेट चुन सकता हूँ?** हाँ – JPEG, PNG, BMP, आदि `ImageSaveOptions` के माध्यम से  
- **क्या उत्पादन के लिए लाइसेंस चाहिए?** व्यावसायिक उपयोग के लिए वैध Aspose.Note लाइसेंस आवश्यक है।  
- **मैं कौन सा पेज निर्यात कर सकता हूँ?** `PageIndex` (शून्य‑आधारित) सेट करके कोई भी पेज।  
- **परिवर्तन में कितना समय लगता है?** सामान्य पेज के लिए आमतौर पर एक सेकंड से कम।

## OneNote पेज को इमेज में निर्यात करना क्या है?
OneNote पेज को इमेज में निर्यात करना मतलब पेज की समृद्ध सामग्री—टेक्स्ट, ड्रॉइंग, टेबल—को एक स्थिर इमेज फ़ाइल (जैसे JPEG) में रेंडर करना है। यह प्रक्रिया एक पोर्टेबल विज़ुअल प्रतिनिधित्व बनाती है जिसे कहीं भी दिखाया जा सकता है, यहाँ तक कि जहाँ OneNote क्लाइंट स्थापित नहीं है।

## OneNote पेज को परिवर्तित करने के लिए Aspose.Note क्यों उपयोग करें?
- **पूर्ण सटीकता** – लेआउट, फ़ॉन्ट और इंक स्ट्रोक को संरक्षित करता है।  
- **Microsoft Office निर्भरता नहीं** – Java को सपोर्ट करने वाले किसी भी प्लेटफ़ॉर्म पर काम करता है।  
- **सूक्ष्म नियंत्रण** – इमेज फ़ॉर्मेट, क्वालिटी, और विशिष्ट पेज इंडेक्स चुनें।  
- **स्केलेबल** – कई पेजों की बैच प्रोसेसिंग के लिए उपयुक्त।

## पूर्वापेक्षाएँ

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:

1. **Java Development Kit (JDK)** – JDK 11 या बाद का संस्करण स्थापित करें। यदि अभी तक डाउनलोड नहीं किया है तो आप इसे [Oracle official site](https://www.com/java/technologies/javase-jdk11-downloads.html) से डाउनलोड कर सकते हैं।  
2. **Aspose.Note for Java** – नवीनतम लाइब्रेरी [Aspose.Note download page](https://releases.aspose.com/note/java/) से प्राप्त करें। JAR को अपने प्रोजेक्ट के क्लासपाथ में जोड़ें।

## पैकेज इम्पोर्ट करें

पहले, आवश्यक पैकेज इम्पोर्ट करें जो हमें दस्तावेज़ हैंडलिंग और इमेज‑सेविंग विकल्पों तक पहुँच प्रदान करते हैं।

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## चरण 1: OneNote दस्तावेज़ लोड करें

हम `.one` फ़ाइल को `Aspose.Note` `Document` ऑब्जेक्ट में लोड करके शुरू करते हैं।

```java
String dataDir = "Your Document Directory";
// Load the document into Aspose.Note
Document oneFile = new Document(dataDir + "Sample1.one");
```

> **Pro tip:** यदि आपकी फ़ाइल JAR के अंदर स्थित है तो एब्सोल्यूट पाथ या रिसोर्स स्ट्रीम का उपयोग करें।

## चरण 2: Image Save Options को इनिशियलाइज़ करें

आउटपुट फ़ॉर्मेट (इस उदाहरण में JPEG) को परिभाषित करने के लिए `ImageSaveOptions` इंस्टेंस बनाएं। आप `SaveFormat` बदलकर PNG, BMP, या GIF में स्विच कर सकते हैं।

```java
// Initialize ImageSaveOptions object
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
```

## चरण 3: पेज इंडेक्स निर्दिष्ट करें

पेजेज़ शून्य‑आधारित होते हैं, इसलिए `1` **दूसरे** पेज को चुनता है। इस मान को बदलकर आप किसी भी आवश्यक पेज को निर्यात कर सकते हैं।

```java
// Specify second page for conversion
options.setPageIndex(1);
```

## चरण 4: दस्तावेज़ को इमेज के रूप में सहेजें

अब हम `Document` ऑब्जेक्ट पर `save` को कॉल करते हैं, जिसमें लक्ष्य फ़ाइल नाम और हमने कॉन्फ़िगर किए हुए विकल्प पास करते हैं।

```java
// Save the document
oneFile.save(dataDir + "ConvertSpecificPageToImage_out.jpg", options);
```

## चरण 5: पुष्टि प्रिंट करें

एक साधारण कंसोल संदेश पुष्टि करता है कि इमेज सफलतापूर्वक जेनरेट हुई है।

```java
// Print confirmation message
System.out.println("File saved: " + dataDir + "ConvertSpecificPageToImage_out.jpg");
```

## OneNote पेज को इमेज में बदलने के तरीके (वैकल्पिक परिदृश्य)

यदि आपको **OneNote पेज इमेज** फ़ाइलों को बल्क में बदलना है, तो ऊपर दिया गया कोड `Document.getPages()` पर इटररेट करने वाले लूप में रखें। प्रत्येक इटररेशन के लिए `options.setPageIndex(i)` बदलें, और वैकल्पिक रूप से `options.setQuality(90)` सेट करके JPEG कम्प्रेशन को नियंत्रित करें।

## सामान्य समस्याएँ और समाधान

| समस्या | कारण | समाधान |
|-------|--------|-----|
| **इमेज खाली है** | पेज इंडेक्स सीमा से बाहर है या दस्तावेज़ सही से लोड नहीं हुआ। | `options.setPageIndex` को `0 .. document.getPages().size() - 1` के भीतर है, यह सत्यापित करें। |
| **असमर्थित फ़ॉर्मेट** | ऐसी पुरानी Aspose.Note संस्करण का उपयोग करना जिसमें कुछ फ़ॉर्मेट नहीं हैं। | नवीनतम Aspose.Note for Java रिलीज़ में अपडेट करें। |
| **OutOfMemoryError** | कम मेमोरी वाले JVM पर बहुत बड़े पेजों को बदलना। | हीप साइज बढ़ाएँ (`-Xmx2g`) या पेजों को एक‑एक करके प्रोसेस करें। |

## अक्सर पूछे जाने वाले प्रश्न

**Q1: क्या मैं इस विधि से कई पेजों को इमेज में बदल सकता हूँ?**  
A: हाँ। सेव लॉजिक को लूप में रखें और प्रत्येक पेज के लिए `options.setPageIndex(i)` बदलें जिसे आप निर्यात करना चाहते हैं।

**Q2: क्या Aspose.Note विभिन्न संस्करणों की OneNote फ़ाइलों के साथ संगत है?**  
A: बिल्कुल। Aspose.Note OneNote 2007, 2010, 2013 और बाद के संस्करणों की .one फ़ाइलों को सपोर्ट करता है।

**Q3: क्या मैं परिवर्तन के दौरान इमेज फ़ॉर्मेट और क्वालिटी को कस्टमाइज़ कर सकता हूँ?**  
A: हाँ। `SaveFormat.Png`, `SaveFormat.Bmp` आदि चुनें, और JPEG क्वालिटी (0‑100) के लिए `options.setQuality(int)` सेट करें।

**Q4: क्या Aspose.Note अन्य प्रोग्रामिंग भाषाओं के लिए समर्थन प्रदान करता है?**  
A: हाँ। .NET, Python, C++, और अन्य के लिए लाइब्रेरी उपलब्ध हैं।

**Q5: अतिरिक्त समर्थन या सहायता कहाँ प्राप्त कर सकता हूँ?**  
A: Aspose.Note फ़ोरम देखें ([Aspose.Note forum](https://forum.aspose.com/c/note/28)) या आधिकारिक दस्तावेज़ीकरण देखें [here](https://reference.aspose.com/note/java/)।

**अंतिम अपडेट:** 2025-11-29  
**परीक्षण किया गया:** Aspose.Note for Java 24.12  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}