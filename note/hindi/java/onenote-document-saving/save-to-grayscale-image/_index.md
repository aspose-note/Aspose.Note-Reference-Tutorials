---
date: 2025-12-17
description: Aspose.Note for Java का उपयोग करके एक दस्तावेज़ को ग्रेस्केल PNG छवि
  के रूप में सहेजकर OneNote को निर्यात करना सीखें। इसमें OneNote दस्तावेज़ को लोड
  करने और ग्रेस्केल छवि बनाने के चरण शामिल हैं।
linktitle: How to Export OneNote as Grayscale Image – Aspose.Note
second_title: Aspose.Note Java API
title: OneNote को ग्रेस्केल इमेज के रूप में निर्यात कैसे करें – Aspose.Note
url: /hi/java/onenote-document-saving/save-to-grayscale-image/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote में ग्रेस्केल इमेज को सहेजें - Aspose.Note

## परिचय

इस ट्यूटोरियल में, हम आपको Aspose.Note for Java का उपयोग करके एक दस्तावेज़ को ग्रेस्केल इमेज के रूप में सहेजकर **how to export onenote** दिखाएंगे। ग्रेस्केल इमेज मोनोक्रोमेटिक चित्र होते हैं जिनमें केवल ग्रे के शेड होते हैं, जो प्रिंटिंग, अभिलेखीय या फ़ाइल आकार कम करने के लिए उपयोगी हो सकते हैं। हम OneNote दस्तावेज़ को लोड करने, सेव विकल्प को **create a grayscale image** के लिए कॉन्फ़िगर करने, और अंत में **save document as PNG** करने की प्रक्रिया बताएँगे।

## त्वरित उत्तर
- **What does “how to export onenote” mean?** यह एक OneNote फ़ाइल को प्रोग्रामेटिक रूप से किसी अन्य फ़ॉर्मेट, जैसे इमेज, में बदलने को दर्शाता है।  
- **Which format is best for grayscale output?** PNG अच्छा काम करता है क्योंकि यह loss‑less क्वालिटी को बनाए रखता है और ग्रेस्केल कलर मोड को सपोर्ट करता है।  
- **Do I need a license?** एक वैध Aspose.Note लाइसेंस प्रोडक्शन उपयोग के लिए आवश्यक है; परीक्षण के लिए एक अस्थायी ट्रायल लाइसेंस उपलब्ध है।  
- **What Java version is required?** Java 8 या उससे ऊपर की सिफ़ारिश की जाती है।  
- **Can I change the image size?** हाँ, आप `ImageSaveOptions` की प्रॉपर्टीज़ जैसे `Resolution` या `PageSize` को सेव करने से पहले समायोजित कर सकते हैं।

## “how to export onenote” क्या है?
OneNote को एक्सपोर्ट करना मतलब प्रोग्रामेटिक रूप से OneNote `.one` फ़ाइल को किसी अन्य प्रतिनिधित्व—जैसे PDF, HTML, या इमेज—में बदलना है। इस गाइड में हम **grayscale PNG** इमेज में एक्सपोर्ट करने पर ध्यान केंद्रित करते हैं, जो दस्तावेज़ीकरण या प्रिंटिंग वर्कफ़्लो के लिए सामान्य आवश्यकता है।

## OneNote को ग्रेस्केल इमेज के रूप में एक्सपोर्ट क्यों करें?
- **Reduced file size** – ग्रेस्केल PNG आमतौर पर फुल‑कलर इमेज की तुलना में छोटे होते हैं।  
- **Better readability** – प्रिंटेड रिपोर्ट्स के लिए, ग्रेस्केल अक्सर स्पष्ट कंट्रास्ट प्रदान करता है।  
- **Compatibility** – PNG ब्राउज़र्स, एडिटर्स और मोबाइल डिवाइसेज़ में व्यापक रूप से सपोर्टेड है।

## पूर्वापेक्षाएँ

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

1. आपके सिस्टम पर Java Development Kit (JDK) स्थापित हो।  
2. Aspose.Note for Java लाइब्रेरी। आप इसे [here](https://releases.aspose.com/note/java/) से डाउनलोड कर सकते हैं।  
3. Java प्रोग्रामिंग की बुनियादी समझ।

## पैकेज इम्पोर्ट करें

शुरू करने के लिए, आवश्यक पैकेज इम्पोर्ट करें:

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## चरण 1: OneNote दस्तावेज़ लोड करें

पहले, **load onenote document** को Aspose.Note में लोड करें। `"Your Document Directory"` को अपने स्थानीय फ़ोल्डर के पथ से और `"Aspose.one"` को अपने OneNote फ़ाइल के नाम से बदलें।

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## चरण 2: आउटपुट पाथ और विकल्प सेट करें

ग्रेस्केल इमेज के लिए आउटपुट पाथ निर्धारित करें और सेव विकल्प निर्दिष्ट करें। हम `ColorMode` को `GrayScale` सेट करेंगे और **save document as png** फ़ॉर्मेट का उपयोग करेंगे।

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## चरण 3: दस्तावेज़ सहेजें

अंत में, कॉन्फ़िगर किए गए विकल्पों का उपयोग करके दस्तावेज़ को ग्रेस्केल PNG इमेज के रूप में सहेजें।

```java
oneFile.save(dataDir, options);
```

## सामान्य समस्याएँ और समाधान
- **FileNotFoundException** – यह सुनिश्चित करें कि `dataDir` सही फ़ोल्डर की ओर इशारा कर रहा है और `.one` फ़ाइल मौजूद है।  
- **LicenseException** – `save` कॉल करने से पहले सुनिश्चित करें कि आपने वैध Aspose.Note लाइसेंस लागू किया है।  
- **Low‑resolution output** – यदि आवश्यक हो तो DPI बढ़ाने के लिए `options.setResolution(300)` समायोजित करें।

## अक्सर पूछे जाने वाले प्रश्न

**Q1: क्या मैं ग्रेस्केल इमेज को किसी अलग फ़ॉर्मेट में सहेज सकता हूँ?**  
A1: हाँ, बस `ImageSaveOptions` कंस्ट्रक्टर में `SaveFormat` पैरामीटर को `Jpeg`, `Bmp` आदि में बदल दें।

**Q2: क्या Aspose.Note सभी संस्करणों के OneNote दस्तावेज़ों के साथ संगत है?**  
A2: Aspose.Note Microsoft OneNote 2010 और उसके बाद के संस्करणों को सपोर्ट करता है।

**Q3: क्या Aspose.Note उपयोग करने के लिए लाइसेंस की आवश्यकता है?**  
A3: प्रोडक्शन उपयोग के लिए वैध लाइसेंस आवश्यक है, लेकिन मूल्यांकन के लिए एक अस्थायी ट्रायल लाइसेंस प्राप्त किया जा सकता है।

**Q4: क्या मैं इमेज के रूप में सहेजने से पहले दस्तावेज़ के अन्य पहलुओं को बदल सकता हूँ?**  
A4: बिल्कुल! Aspose.Note एक्सपोर्ट से पहले सेक्शन, पेज और कंटेंट को एडिट करने के लिए एक व्यापक API प्रदान करता है।

**Q5: यदि मुझे समस्याएँ आती हैं तो मैं समर्थन कहाँ पा सकता हूँ?**  
A5: आप Aspose.Note फ़ोरम पर समर्थन पा सकते हैं [here](https://forum.aspose.com/c/note/28)।

## निष्कर्ष

अब आपने **how to export onenote** को OneNote फ़ाइल लोड करके, सेव विकल्प को **create a grayscale image** के लिए कॉन्फ़िगर करके, और **saving the document as PNG** करके सीखा है। यह तकनीक OneNote नोटबुक्स से हल्के, प्रिंट‑रेडी विज़ुअल्स बनाने में उपयोगी है। अपने प्रोजेक्ट की जरूरतों के अनुसार अन्य `ColorMode` सेटिंग्स या इमेज फ़ॉर्मेट्स के साथ प्रयोग करने में संकोच न करें।

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**अंतिम अपडेट:** 2025-12-17  
**परीक्षित संस्करण:** Aspose.Note 24.12 for Java  
**लेखक:** Aspose  

---