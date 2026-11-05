---
date: 2026-11-05
description: Aspose.Note का उपयोग करके Java में OneNote नोटबुक्स को TIFF में परिवर्तित
  करते समय TIFF फ़ाइल आकार को कैसे कम करें, सीखें। इसमें JPEG, PackBits और ब्लैक‑वाइट
  TIFF विकल्प शामिल हैं।
keywords:
- reduce tiff file size
- black white tiff
- tiff jpeg compression
- aspose note java
lastmod: 2026-11-05
linktitle: Java में OneNote को परिवर्तित करते समय TIFF फ़ाइल आकार कैसे कम करें
og_description: Aspose.Note का उपयोग करके Java में OneNote नोटबुक्स को TIFF में परिवर्तित
  करते समय TIFF फ़ाइल आकार को कैसे कम करें, सीखें। इसमें JPEG, PackBits और ब्लैक‑वाइट
  TIFF विकल्प शामिल हैं।
og_image_alt: Developer guide showing OneNote to TIFF conversion with compression
  options in Java
og_title: Java में OneNote को परिवर्तित करते समय TIFF फ़ाइल आकार कैसे कम करें
schemas:
- author: Aspose
  dateModified: '2026-11-05'
  description: Learn how to reduce TIFF file size when converting OneNote notebooks
    to TIFF in Java using Aspose.Note. Includes JPEG, PackBits and black‑white TIFF
    options.
  headline: How to reduce TIFF file size when converting OneNote in Java
  type: TechArticle
- description: Learn how to reduce TIFF file size when converting OneNote notebooks
    to TIFF in Java using Aspose.Note. Includes JPEG, PackBits and black‑white TIFF
    options.
  name: How to reduce TIFF file size when converting OneNote in Java
  steps:
  - name: Point `dataDir` to the folder containing your `.one` file.
    text: Point `dataDir` to the folder containing your `.one` file.
  - name: Call `SaveToTiffUsingJpegCompression()` from your main method or service.
    text: Call `SaveToTiffUsingJpegCompression()` from your main method or service.
  - name: The resulting `.tiff` file will appear in the same directory.
    text: The resulting `.tiff` file will appear in the same directory.
  type: HowTo
- questions:
  - answer: Yes. While Aspose.Note focuses on OneNote files, Aspose.PDF, Aspose.Words,
      and other libraries provide similar `ImageSaveOptions` for their formats.
    question: Can I convert other document types (e.g., PDF, DOCX) to TIFF with these
      options?
  - answer: The JPEG algorithm is the same, but the image data lives inside a TIFF
      container, which can hold multiple pages and richer metadata.
    question: How does TIFF JPEG compression differ from a standard JPEG file?
  - answer: Absolutely. Iterate over a directory, call any of the three methods for
      each file, and collect the resulting TIFFs.
    question: Is it possible to batch‑process many `.one` files?
  - answer: Yes. Use `options.setResolution(int dpi)` before saving.
    question: Can I control the DPI/resolution of the output TIFF?
  - answer: The API itself is synchronous, but you can wrap calls in Java’s `CompletableFuture`
      or a thread pool for parallel execution.
    question: Does Aspose.Note support asynchronous processing?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- reduce tiff file size
- aspose.note
- java tiff conversion
- black white tiff
- image compression
title: Java में OneNote को परिवर्तित करते समय TIFF फ़ाइल आकार कैसे कम करें
url: /hi/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote को Java में परिवर्तित करते समय TIFF फ़ाइल आकार कैसे घटाएँ

## परिचय

इस ट्यूटोरियल में आप सीखेंगे कि Aspose.Note for Java का उपयोग करके OneNote नोटबुक को TIFF छवियों में परिवर्तित करते समय **TIFF फ़ाइल आकार घटाएँ**। हम तीन संपीड़न विधियों—TIFF JPEG, PackBits, और CCITT Group 3 (ब्लैक‑वाइट TIFF)—के माध्यम से चलेंगे, आपको दिखाएंगे कि कैसे इमेज क्वालिटी को समायोजित करें, कलर मोड को नियंत्रित करें, और वेब, अभिलेखीय, या फैक्स‑टाइप परिदृश्यों के लिए फ़ाइल आकार को इष्टतम रखें।

## त्वरित उत्तर
- **TIFF JPEG संपीड़न क्या है?** एक लॉसी संपीड़न विधि जो दृश्य गुणवत्ता को बनाए रखते हुए TIFF फ़ाइल आकार को घटाती है।  
- **कौन सी लाइब्रेरी परिवर्तन को संभालती है?** Aspose.Note for Java।  
- **क्या मुझे लाइसेंस चाहिए?** परीक्षण के लिए एक मुफ्त ट्रायल काम करता है; उत्पादन के लिए लाइसेंस आवश्यक है।  
- **क्या मैं इमेज क्वालिटी बदल सकता हूँ?** हाँ, `ImageSaveOptions` पर `quality` प्रॉपर्टी सेट करें।  
- **क्या बैच रूपांतरण संभव है?** बिल्कुल – दस्तावेज़ों के माध्यम से लूप करें और समान विकल्प लागू करें।

## TIFF JPEG संपीड़न अवलोकन

TIFF JPEG संपीड़न इमेज डेटा को एक TIFF कंटेनर में संग्रहीत करता है लेकिन फ़ाइल को छोटा करने के लिए JPEG के लॉसी एल्गोरिद्म को लागू करता है। यह तब आदर्श है जब आपको **tiff image quality** और छोटे फ़ाइल आकार के बीच संतुलन चाहिए, विशेष रूप से वेब या अभिलेखीय परिदृश्यों के लिए।

## विभिन्न TIFF संपीड़न प्रकारों का उपयोग क्यों करें?

आप सामग्री और संग्रहण आवश्यकताओं के आधार पर संपीड़न प्रकार चुनते हैं: फ़ोटोग्राफ़ के लिए JPEG सबसे अच्छा काम करता है, बड़े समान क्षेत्रों वाले ग्राफ़िक्स के लिए PackBits लॉस‑लेस संपीड़न प्रदान करता है, और मोनोक्रोम फैक्स‑स्टाइल दस्तावेज़ों के लिए CCITT Group 3 उच्च‑अनुपात संपीड़न देता है। सही विधि का चयन करने से आप **TIFF फ़ाइल आकार घटाएँ** बिना आपके एप्लिकेशन द्वारा आवश्यक दृश्य सत्यता से समझौता किए।

## सही संपीड़न चुनना

- **JPEG** – समायोज्य गुणवत्ता (0‑100) आपको आकार बनाम विवरण का संतुलन करने देती है, रंग‑समृद्ध पृष्ठों के लिए परिपूर्ण।  
- **PackBits** – लॉस‑लेस रन‑लेंथ एन्कोडिंग; जब आपको हर पिक्सेल को सटीक रखना हो तो आदर्श।  
- **CCITT Group 3** – केवल मोनोक्रोम; स्कैन किए गए टेक्स्ट या फैक्स दस्तावेज़ों के लिए संपीड़न को अधिकतम करता है।  

## Aspose.Note का उपयोग करके OneNote को TIFF में परिवर्तित करें

यदि आपका लक्ष्य **OneNote को TIFF में परिवर्तित करना** है, तो नीचे दी गई तीन विधियाँ सबसे सामान्य परिदृश्यों को कवर करती हैं। प्रत्येक विधि एक `.one` फ़ाइल लोड करती है, `ImageSaveOptions` को कॉन्फ़िगर करती है, और परिणाम को एक `.tiff` फ़ाइल के रूप में सहेजती है।

## पूर्वापेक्षाएँ

- Java Development Kit (JDK) स्थापित हो।  
- Aspose.Note for Java लाइब्रेरी आपके प्रोजेक्ट में जोड़ी गई हो (Maven/Gradle या मैन्युअल JAR)।  
- Java सिंटैक्स की बुनियादी परिचितता।  

## पैकेज आयात करें

`ImageSaveOptions`, `TiffCompression`, और `ColorMode` क्लासेज़ रूपांतरण API का मूल हैं।

`ImageSaveOptions` इमेज को सहेजने के विकल्प निर्धारित करता है, जैसे फ़ॉर्मेट और संपीड़न।  
`TiffCompression` समर्थित TIFF संपीड़न एल्गोरिद्म को सूचीबद्ध करता है।  
`ColorMode` रंग गहराई निर्दिष्ट करता है, उदाहरण के लिए, रंग या ब्लैक‑एंड‑व्हाइट।  

```java
// Placeholder for import statements – keep your imports here
```

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## चरण 1: TIFF JPEG संपीड़न का उपयोग करके TIFF सहेजें

### Java में JPEG संपीड़न के साथ TIFF सहेजना

OneNote फ़ाइल लोड करें, `ImageSaveOptions` को JPEG संपीड़न के साथ कॉन्फ़िगर करें, वैकल्पिक रूप से `quality` मान सेट करें, और सहेजने की विधि को कॉल करें। यह दो‑चरणीय पैटर्न आपको आउटपुट आकार और दृश्य सत्यता पर पूर्ण नियंत्रण देता है।

1. `dataDir` को उस फ़ोल्डर की ओर इंगित करें जिसमें आपकी `.one` फ़ाइल है।  
2. अपने मुख्य मेथड या सर्विस से `SaveToTiffUsingJpegCompression()` को कॉल करें।  
3. परिणामी `.tiff` फ़ाइल उसी डायरेक्टरी में दिखाई देगी।  

```java
// Placeholder for the JPEG compression method implementation
```

```java
public static void SaveToTiffUsingJpegCompression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.Jpeg);
    options.setQuality(93);

    oneFile.save(Paths.get(dataDir,"SaveToTiffUsingJpegCompression.tiff").toString(), options);
}
```

**व्याख्या**

- `ImageSaveOptions` Aspose.Note को TIFF फ़ाइल आउटपुट करने के लिए बताता है।  
- `setTiffCompression(TiffCompression.Jpeg)` JPEG संपीड़न चुनता है।  
- `setQuality(93)` (वैकल्पिक) इमेज क्वालिटी को सूक्ष्म‑समायोजित करता है; कम मान छोटे फ़ाइलें उत्पन्न करते हैं।  

## TIFF PackBits संपीड़न अवलोकन

PackBits एक लॉसलेस संपीड़न एल्गोरिद्म है जो ठोस रंग के बड़े क्षेत्रों वाली छवियों के लिए सबसे अच्छा काम करता है। इसे दस्तावेज़ में अक्सर **tiff packbits compression** कहा जाता है।

## Java में PackBits संपीड़न के साथ TIFF सहेजना

यदि आपको लॉस‑लेस विकल्प चाहिए, तो PackBits एक सरल रन‑लेंथ एल्गोरिद्म है जो ठोस रंग वाले ग्राफ़िक्स के लिए अच्छा काम करता है। `ImageSaveOptions` को `TiffCompression.PackBits` के साथ कॉन्फ़िगर करें और दस्तावेज़ को सहेजें।

```java
// Placeholder for the PackBits compression method implementation
```

```java
public static void SaveToTiffUsingPackBitsCompression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.PackBits);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingPackBitsCompression.tiff").toString(), options);
}
```

**व्याख्या**

- `setTiffCompression(TiffCompression.PackBits)` संपीड़न विधि बदलता है।  
- PackBits लॉस‑लेस होने के कारण कोई क्वालिटी सेटिंग आवश्यक नहीं है।  

## Java में CCITT Group 3 संपीड़न के साथ TIFF सहेजना

फ़ैक्स‑स्टाइल दस्तावेज़ों के लिए आप अक्सर एक **ब्लैक एंड व्हाइट TIFF** चाहते हैं। CCITT Group 3 मोनोक्रोम इमेज के लिए उच्च संपीड़न प्रदान करता है। कलर मोड को ब्लैक‑एंड‑व्हाइट सेट करें और CCITT 3 संपीड़न एन्‍युम चुनें।

```java
// Placeholder for the CCITT Group 3 compression method implementation
```

```java
public static void SaveToTiffUsingCcitt3Compression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setColorMode(ColorMode.BlackAndWhite);
    options.setTiffCompression(TiffCompression.Ccitt3);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingCcitt3Compression.tiff").toString(), options);
}
```

**व्याख्या**

- `setColorMode(ColorMode.BlackAndWhite)` मोनोक्रोम आउटपुट को बाध्य करता है।  
- `setTiffCompression(TiffCompression.Ccitt3)` फैक्स‑उन्मुख संपीड़न लागू करता है।  

## सामान्य समस्याएँ और टिप्स

| Issue | Solution |
|-------|----------|
| **आउटपुट फ़ाइल अपेक्षा से बड़ी है** | JPEG `quality` मान को घटाने का प्रयास करें या यदि लॉसलेस स्वीकार्य है तो PackBits पर स्विच करें। |
| **रंग फीके दिख रहे हैं** | सुनिश्चित करें कि जब आपको पूर्ण रंग चाहिए तो आपने अनजाने में `ColorMode.BlackAndWhite` सेट नहीं किया है। |
| **असमर्थित इमेज फ़ॉर्मेट त्रुटि** | पुष्टि करें कि आप Aspose.Note का नवीनतम संस्करण उपयोग कर रहे हैं; पुराने बिल्ड में कुछ संपीड़न एन्‍युम नहीं हो सकते। |
| **रनटाइम पर LicenseException** | एक वैध Aspose.Note लाइसेंस स्थापित करें (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`). |

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या मैं इन विकल्पों के साथ अन्य दस्तावेज़ प्रकार (जैसे PDF, DOCX) को TIFF में परिवर्तित कर सकता हूँ?**  
A: हाँ। जबकि Aspose.Note OneNote फ़ाइलों पर केंद्रित है, Aspose.PDF, Aspose.Words, और अन्य लाइब्रेरीज़ अपने फ़ॉर्मेट्स के लिए समान `ImageSaveOptions` प्रदान करती हैं।

**Q: TIFF JPEG संपीड़न मानक JPEG फ़ाइल से कैसे अलग है?**  
A: JPEG एल्गोरिद्म समान है, लेकिन इमेज डेटा एक TIFF कंटेनर के भीतर रहता है, जो कई पृष्ठ और अधिक समृद्ध मेटाडेटा रख सकता है।

**Q: कई `.one` फ़ाइलों को बैच‑प्रोसेस करना संभव है क्या?**  
A: बिल्कुल। एक डायरेक्टरी पर इटररेट करें, प्रत्येक फ़ाइल के लिए तीन में से कोई भी विधि कॉल करें, और परिणामी TIFFs एकत्र करें।

**Q: क्या मैं आउटपुट TIFF की DPI/रिज़ॉल्यूशन नियंत्रित कर सकता हूँ?**  
A: हाँ। सहेजने से पहले `options.setResolution(int dpi)` का उपयोग करें।

**Q: क्या Aspose.Note असिंक्रोनस प्रोसेसिंग का समर्थन करता है?**  
A: API स्वयं सिंक्रोनस है, लेकिन आप कॉल्स को Java के `CompletableFuture` या थ्रेड पूल में रैप करके समानांतर निष्पादन कर सकते हैं।

## निष्कर्ष

अब आपके पास एक पूर्ण **Java TIFF रूपांतरण** टूलकिट है जो आपको JPEG, PackBits, या CCITT Group 3 फ़ैक्स संपीड़न का उपयोग करके OneNote दस्तावेज़ों को TIFF फ़ाइलों के रूप में सहेजते समय **TIFF फ़ाइल आकार घटाएँ** देता है। गुणवत्ता, कलर मोड, और रिज़ॉल्यूशन को अपनी विशिष्ट आवश्यकताओं के अनुसार समायोजित करें, और अधिकतम उत्पादकता के लिए इन विधियों को बैच वर्कफ़्लो में एकीकृत करें।

---

**अंतिम अपडेट:** 2026-11-05  
**परीक्षित संस्करण:** Aspose.Note for Java 26.4 (latest at time of writing)  
**लेखक:** Aspose

## संबंधित ट्यूटोरियल

- [Aspose.Note for Java के साथ सेव फॉर्मेट का उपयोग करके OneNote पेज इमेज (JPEG) कैसे रेंडर करें](/note/java/onenote-document-saving/save-to-jpeg-image-using-save-format/)
- [Aspose.Note for Java का उपयोग करके OneNote को PNG के रूप में विकल्पों के साथ सहेजें – नोटबुक को इमेज में परिवर्तित करें](/note/java/onenote-notebook-operations/convert-notebook-to-image-with-options/)
- [OneNote को ग्रेस्केल इमेज के रूप में एक्सपोर्ट कैसे करें – Aspose.Note](/note/java/onenote-document-saving/save-to-grayscale-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}