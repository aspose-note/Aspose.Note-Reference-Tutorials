---
date: 2026-03-14
description: जावा में TIFF JPEG संपीड़न, TIFF PackBits संपीड़न, या CCITT Group 3 फ़ैक्स
  का उपयोग करके OneNote दस्तावेज़ों को TIFF फ़ाइलों के रूप में सहेजना सीखें। Aspose.Note
  के साथ छवि गुणवत्ता, फ़ाइल आकार और रंग मोड को नियंत्रित करें।
linktitle: Save to TIFF Image Using TIFF JPEG Compression in OneNote
second_title: Aspose.Note Java API
title: OneNote में TIFF JPEG संपीड़न का उपयोग करके TIFF इमेज सहेजें
url: /hi/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote में TIFF JPEG संपीड़न का उपयोग करके TIFF छवि को सहेजें

## परिचय

इस ट्यूटोरियल में आप **OneNote दस्तावेज़ को TIFF फ़ाइल में TIFF JPEG संपीड़न के साथ सहेजना** और दो अन्य लोकप्रिय संपीड़न विधियों को सीखेंगे। हम आवश्यक सेटअप, आवश्यक Java पैकेजों को इम्पोर्ट करने, और प्रत्येक संपीड़न विकल्प के लिए स्पष्ट चरण‑दर‑चरण कोड प्रदान करेंगे। अंत तक आप **TIFF छवि गुणवत्ता** को नियंत्रित कर सकेंगे, फ़ाइल आकार घटा सकेंगे, और फ़ैक्स‑स्टाइल आउटपुट के लिए काली‑और‑सफ़ेद TIFF भी बना सकेंगे।

## त्वरित उत्तर
- **TIFF JPEG संपीड़न क्या है?** एक लॉसी संपीड़न विधि जो TIFF फ़ाइल आकार को घटाती है जबकि दृश्य गुणवत्ता को बनाए रखती है।  
- **कौन सा लाइब्रेरी रूपांतरण संभालता है?** Aspose.Note for Java।  
- **क्या लाइसेंस चाहिए?** परीक्षण के लिए मुफ्त ट्रायल चलती है; उत्पादन के लिए लाइसेंस आवश्यक है।  
- **क्या मैं छवि गुणवत्ता बदल सकता हूँ?** हाँ, `ImageSaveOptions` पर `quality` प्रॉपर्टी सेट करें।  
- **क्या बैच रूपांतरण संभव है?** बिल्कुल – दस्तावेज़ों पर लूप चलाएँ और समान विकल्प लागू करें।

## TIFF JPEG संपीड़न क्या है?
TIFF JPEG संपीड़न छवि डेटा को TIFF कंटेनर में संग्रहीत करता है लेकिन फ़ाइल को छोटा करने के लिए JPEG के लॉसी एल्गोरिद्म को लागू करता है। यह **tiff image quality** और छोटे फ़ाइल आकार के बीच संतुलन चाहिए होने पर आदर्श है, विशेषकर वेब या अभिलेखीय परिदृश्यों में।

## विभिन्न TIFF संपीड़न प्रकारों का उपयोग क्यों करें?
- **JPEG** – फ़ोटोग्राफ़ के लिए उपयुक्त; गुणवत्ता समायोज्य।  
- **PackBits** – सरल, लॉस‑लेस रन‑लेंथ एन्कोडिंग; बड़े समान रंग क्षेत्रों वाली ग्राफ़िक्स के लिए उपयोगी।  
- **CCITT Group 3 Fax** – केवल काली‑और‑सफ़ेद; स्कैन किए गए दस्तावेज़ और फ़ैक्स ट्रांसमिशन के लिए परिपूर्ण।  

सही संपीड़न चुनने से आप स्टोरेज प्रतिबंधों को पूरा कर सकते हैं बिना आपके एप्लिकेशन की दृश्य सटीकता से समझौता किए।

## Aspose.Note का उपयोग करके One को TIFF में बदलें
यदि आपका लक्ष्य **OneNote को TIFF में बदलना** है, तो नीचे दी गई तीन विधियाँ सबसे सामान्य परिदृश्यों को कवर करती हैं। प्रत्येक विधि एक `.one` फ़ाइल लोड करती है, `ImageSaveOptions` को कॉन्फ़िगर करती है, और परिणाम को `.tiff` फ़ाइल के रूप में सहेजती है।

## पूर्वापेक्षाएँ

- Java Development Kit (JDK) स्थापित हो।  
- आपके प्रोजेक्ट में Aspose.Note for Java लाइब्रेरी जोड़ी गई हो (Maven/Gradle या मैन्युअल JAR)।  
- Java सिंटैक्स की बुनियादी समझ।

## पैकेज इम्पोर्ट करें

सबसे पहले, आवश्यक Aspose.Note क्लासेज़ को अपने Java फ़ाइल में इम्पोर्ट करें:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## चरण 1: TIFF JPEG संपीड़न का उपयोग करके TIFF में सहेजें

नीचे वह पूर्ण मेथड है जो OneNote फ़ाइल लोड करता है और JPEG संपीड़न के साथ TIFF के रूप में सहेजता है। `quality` मान (0‑100) को समायोजित करके **tiff image quality** को नियंत्रित करें।

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
- `setQuality(93)` (वैकल्पिक) छवि गुणवत्ता को फाइन‑ट्यून करता है; कम मान छोटे फ़ाइल बनाते हैं।

### Java में JPEG संपीड़न के साथ TIFF कैसे सहेजें
1. `dataDir` को अपनी `.one` फ़ाइल वाले फ़ोल्डर की ओर इंगित करें।  
2. अपने मुख्य मेथड या सर्विस से `SaveToTiffUsingJpegCompression()` को कॉल करें।  
3. परिणामी `.tiff` फ़ाइल उसी डायरेक्टरी में दिखाई देगी।

## TIFF PackBits संपीड़न का अवलोकन

PackBits एक लॉसलेस संपीड़न एल्गोरिद्म है जो बड़े ठोस रंग क्षेत्रों वाली छवियों के लिए सबसे अच्छा काम करता है। दस्तावेज़ीकरण में इसे अक्सर **tiff packbits compression** कहा जाता है।

## चरण 2: PackBits संपीड़न का उपयोग करके TIFF में सहेजें

यदि आपको लॉस‑लेस विकल्प चाहिए, तो PackBits एक सरल रन‑लेंथ एल्गोरिद्म है जो ठोस रंग वाली ग्राफ़िक्स के लिए उपयुक्त है।

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
- गुणवत्ता सेटिंग की आवश्यकता नहीं है क्योंकि PackBits लॉसलेस है।

## चरण 3: CCITT Group 3 Fax संपीड़न (काली‑और‑सफ़ेद TIFF) का उपयोग करके TIFF में सहेजें

फ़ैक्स‑स्टाइल दस्तावेज़ों के लिए अक्सर **काली और सफ़ेद TIFF** चाहिए होती है। CCITT Group 3 मोनोक्रोम छवियों के लिए उच्च संपीड़न प्रदान करता है।

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

- `setColorMode(ColorMode.BlackAndWhite)` मोनोक्रोम आउटपुट को मजबूर करता है।  
- `setTiffCompression(TiffCompression.Ccitt3)` फ़ैक्स‑उन्मुख संपीड़न लागू करता है।

## सामान्य समस्याएँ और सुझाव

| समस्या | समाधान |
|-------|----------|
| **आउटपुट फ़ाइल अपेक्षा से बड़ी है** | JPEG `quality` मान घटाएँ या यदि लॉसलेस स्वीकार्य है तो PackBits पर स्विच करें। |
| **रंग फीके दिख रहे हैं** | सुनिश्चित करें कि आप अनजाने में `ColorMode.BlackAndWhite` सेट नहीं कर रहे हैं जब आपको पूर्ण रंग चाहिए। |
| **Unsupported image format त्रुटि** | जांचें कि आप Aspose.Note का नवीनतम संस्करण उपयोग कर रहे हैं; पुराने बिल्ड में कुछ संपीड़न एनोम नहीं हो सकते। |
| **LicenseException रनटाइम पर** | वैध Aspose.Note लाइसेंस इंस्टॉल करें (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`)। |

## अक्सर पूछे जाने वाले प्रश्न

**प्रश्न: क्या मैं अन्य दस्तावेज़ प्रकार (जैसे PDF, DOCX) को भी इन विकल्पों के साथ TIFF में बदल सकता हूँ?**  
उत्तर: हाँ। जबकि Aspose.Note मुख्यतः OneNote फ़ाइलों पर केंद्रित है, Aspose.PDF, Aspose.Words, और अन्य लाइब्रेरी अपने‑अपने फ़ॉर्मेट्स के लिए समान `ImageSaveOptions` प्रदान करती हैं।

**प्रश्न: TIFF JPEG संपीड़न मानक JPEG फ़ाइल से कैसे अलग है?**  
उत्तर: JPEG एल्गोरिद्म समान है, लेकिन छवि डेटा TIFF कंटेनर के भीतर रहता है, जो कई पृष्ठ और समृद्ध मेटाडेटा रख सकता है।

**प्रश्न: क्या कई `.one` फ़ाइलों को बैच‑प्रोसेस करना संभव है?**  
उत्तर: बिल्कुल। किसी डायरेक्टरी पर इटररेट करें, प्रत्येक फ़ाइल के लिए ऊपर दी गई तीन विधियों में से कोई भी कॉल करें, और परिणामी TIFFs को इकट्ठा करें।

**प्रश्न: क्या मैं आउटपुट TIFF की DPI/रिज़ॉल्यूशन नियंत्रित कर सकता हूँ?**  
उत्तर: हाँ। सहेजने से पहले `options.setResolution(int dpi)` का उपयोग करें।

**प्रश्न: क्या Aspose.Note असिंक्रोनस प्रोसेसिंग का समर्थन करता है?**  
उत्तर: API स्वयं सिंक्रोनस है, लेकिन आप कॉल को Java के `CompletableFuture` या थ्रेड पूल में रैप करके समानांतर निष्पादन प्राप्त कर सकते हैं।

## निष्कर्ष

अब आपके पास एक पूर्ण **java tiff conversion** टूलकिट है जो आपको OneNote दस्तावेज़ों को JPEG, PackBits, या CCITT Group 3 Fax संपीड़न का उपयोग करके TIFF फ़ाइलों के रूप में सहेजने की अनुमति देता है। गुणवत्ता, रंग मोड, और रिज़ॉल्यूशन को अपनी विशिष्ट **tiff image quality** आवश्यकताओं के अनुसार समायोजित करें, और अधिकतम उत्पादकता के लिए इन विधियों को बैच वर्कफ़्लो में एकीकृत करें।

---

**अंतिम अपडेट:** 2026-03-14  
**परीक्षित संस्करण:** Aspose.Note for Java 23.12 (लेखन समय पर नवीनतम)  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}