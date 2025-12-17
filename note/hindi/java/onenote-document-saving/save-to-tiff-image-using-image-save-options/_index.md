---
date: 2025-12-17
description: जावा में TIFF JPEG संपीड़न, PackBits, या CCITT Group 3 फ़ैक्स का उपयोग
  करके OneNote दस्तावेज़ों को TIFF फ़ाइलों के रूप में सहेजना सीखें। Aspose.Note के
  साथ छवि गुणवत्ता, फ़ाइल आकार और रंग मोड को नियंत्रित करें।
linktitle: Save to TIFF Image Using TIFF JPEG Compression in OneNote
second_title: Aspose.Note Java API
title: OneNote में TIFF JPEG संपीड़न का उपयोग करके TIFF इमेज सहेजें
url: /hi/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# TIFF JPEG संपीड़न का उपयोग करके OneNote में TIFF इमेज सहेजें

## परिचय

इस ट्यूटोरियल में आप **TIFF JPEG संपीड़न का उपयोग करके OneNote दस्तावेज़ को TIFF फ़ाइल में सहेजने** के तरीके और दो अन्य लोकप्रिय संपीड़न विधियों की खोज करेंगे। हम आवश्यक सेटअप, आवश्यक Java पैकेजों को इम्पोर्ट करने, और प्रत्येक संपीड़न विकल्प के लिए स्पष्ट चरण‑दर‑चरण कोड प्रदान करेंगे। अंत तक आप **TIFF इमेज क्वालिटी** को नियंत्रित कर सकेंगे, फ़ाइल आकार घटा सकेंगे, और यहाँ तक कि फ़ैक्स‑स्टाइल आउटपुट के लिए ब्लैक‑एंड‑व्हाइट TIFF भी बना सकेंगे।

## त्वरित उत्तर
- **TIFF JPEG संपीड़न क्या है?** एक लॉसी संपीड़न विधि जो दृश्य गुणवत्ता को बनाए रखते हुए TIFF फ़ाइल आकार को कम करती है।  
- **कौन सा लाइब्रेरी रूपांतरण संभालता है?** Aspose.Note for Java।  
- **क्या मुझे लाइसेंस चाहिए?** परीक्षण के लिए एक मुफ्त ट्रायल काम करता है; उत्पादन के लिए लाइसेंस आवश्यक है।  
- **क्या मैं इमेज क्वालिटी बदल सकता हूँ?** हाँ, `ImageSaveOptions` पर `quality` प्रॉपर्टी सेट करें।  
- **क्या बैच रूपांतरण संभव है?** बिल्कुल – दस्तावेज़ों के माध्यम से लूप करें और समान विकल्प लागू करें।

## TIFF JPEG संपीड़न क्या है?

TIFF JPEG संपीड़न इमेज डेटा को TIFF कंटेनर में संग्रहीत करता है लेकिन फ़ाइल को छोटा करने के लिए JPEG के लॉसी एल्गोरिदम को लागू करता है। यह **tiff इमेज क्वालिटी** और छोटे फ़ाइल आकार के बीच संतुलन की आवश्यकता होने पर आदर्श है, विशेष रूप से वेब या अभिलेखीय परिदृश्यों के लिए।

## विभिन्न TIFF संपीड़न प्रकारों का उपयोग क्यों करें?

- **JPEG** – फ़ोटोग्राफ़ के लिए अच्छा; समायोज्य क्वालिटी प्रदान करता है।  
- **PackBits** – सरल, लॉस‑लेस रन‑लेन्थ एन्कोडिंग; बड़े समान क्षेत्रों वाले ग्राफ़िक्स के लिए उपयोगी।  
- **CCITT Group 3 Fax** – केवल ब्लैक‑एंड‑व्हाइट; स्कैन किए गए दस्तावेज़ और फ़ैक्स ट्रांसमिशन के लिए परिपूर्ण।  

सही संपीड़न चुनने से आप स्टोरेज प्रतिबंधों को पूरा कर सकते हैं बिना आपके एप्लिकेशन के लिए आवश्यक दृश्य सटीकता से समझौता किए।

## पूर्वापेक्षाएँ

- Java Development Kit (JDK) स्थापित हो।  
- Aspose.Note for Java लाइब्रेरी आपके प्रोजेक्ट में जोड़ी गई हो (Maven/Gradle या मैन्युअल JAR)।  
- Java सिंटैक्स की बुनियादी परिचितता।

## पैकेज इम्पोर्ट करें

पहले, आवश्यक Aspose.Note क्लासेज़ को अपने Java फ़ाइल में लाएँ:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## चरण 1: TIFF JPEG संपीड़न का उपयोग करके TIFF सहेजें

नीचे वह पूर्ण मेथड है जो OneNote फ़ाइल को लोड करता है और JPEG संपीड़न के साथ TIFF के रूप में सहेजता है। **tiff इमेज क्वालिटी** को नियंत्रित करने के लिए `quality` मान (0‑100) को समायोजित करें।

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
- `setQuality(93)` (वैकल्पिक) इमेज क्वालिटी को बारीकी से समायोजित करता है; कम मान छोटे फ़ाइलें बनाते हैं।

### Java में JPEG संपीड़न के साथ TIFF कैसे सहेजें

1. `dataDir` को उस फ़ोल्डर की ओर इंगित करें जिसमें आपका `.one` फ़ाइल हो।  
2. अपने मुख्य मेथड या सर्विस से `SaveToTiffUsingJpegCompression()` को कॉल करें।  
3. परिणामी `.tiff` फ़ाइल उसी डायरेक्टरी में दिखाई देगी।

## चरण 2: PackBits संपीड़न का उपयोग करके TIFF सहेजें

यदि आपको लॉस‑लेस विकल्प चाहिए, तो PackBits एक सरल रन‑लेन्थ एल्गोरिदम है जो ठोस रंगों वाले ग्राफ़िक्स के लिए अच्छा काम करता है।

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
- PackBits लॉस‑लेस होने के कारण क्वालिटी सेटिंग की आवश्यकता नहीं है।

## चरण 3: CCITT Group 3 Fax संपीड़न (ब्लैक‑एंड‑व्हाइट TIFF) का उपयोग करके TIFF सहेजें

फ़ैक्स‑स्टाइल दस्तावेज़ों के लिए आप अक्सर **ब्लैक एंड व्हाइट TIFF** चाहते हैं। CCITT Group 3 मोनोक्रोम इमेज के लिए उच्च संपीड़न प्रदान करता है।

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
- `setTiffCompression(TiffCompression.Ccitt3)` फ़ैक्स‑उन्मुख संपीड़न लागू करता है।

## सामान्य समस्याएँ और सुझाव

| समस्या | समाधान |
|-------|----------|
| **आउटपुट फ़ाइल अपेक्षा से बड़ी है** | JPEG `quality` मान को कम करने का प्रयास करें या यदि लॉसलेस स्वीकार्य है तो PackBits पर स्विच करें। |
| **रंग फीके दिख रहे हैं** | सुनिश्चित करें कि पूर्ण रंग की आवश्यकता होने पर आप अनजाने में `ColorMode.BlackAndWhite` सेट नहीं कर रहे हैं। |
| **असमर्थित इमेज फॉर्मेट त्रुटि** | जाँचें कि आप Aspose.Note का नवीनतम संस्करण उपयोग कर रहे हैं; पुराने बिल्ड में कुछ संपीड़न एनोम नहीं हो सकते। |
| **रनटाइम पर LicenseException** | एक वैध Aspose.Note लाइसेंस स्थापित करें (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`). |

## अक्सर पूछे जाने वाले प्रश्न

**प्रश्न: क्या मैं इन विकल्पों के साथ अन्य दस्तावेज़ प्रकार (जैसे PDF, DOCX) को TIFF में बदल सकता हूँ?**  
**उत्तर:** हाँ। Aspose.Note OneNote फ़ाइलों पर केंद्रित है, लेकिन Aspose की अन्य लाइब्रेरीज़ (PDF, Words) उनके संबंधित फ़ॉर्मेट्स के लिए समान `ImageSaveOptions` प्रदान करती हैं।

**प्रश्न: TIFF JPEG संपीड़न मानक JPEG फ़ाइलों से कैसे अलग है?**  
**उत्तर:** इमेज डेटा TIFF कंटेनर के अंदर संग्रहीत होता है, जिससे मेटाडाटा संरक्षित रहता है और कई पृष्ठों की अनुमति मिलती है, जबकि संपीड़न एल्गोरिदम वही JPEG रहता है।

**प्रश्न: क्या कई `.one` फ़ाइलों को बैच‑प्रोसेस करना संभव है?**  
**उत्तर:** बिल्कुल। एक फ़ोल्डर के माध्यम से लूप करें, प्रत्येक फ़ाइल के लिए तीन में से कोई भी मेथड कॉल करें, और परिणामी TIFFs को एकत्र करें।

**प्रश्न: क्या मैं आउटपुट TIFF की DPI/रिज़ॉल्यूशन नियंत्रित कर सकता हूँ?**  
**उत्तर:** हाँ। सहेजने से पहले `options.setResolution(int dpi)` का उपयोग करें।

**प्रश्न: क्या Aspose.Note असिंक्रोनस प्रोसेसिंग का समर्थन करता है?**  
**उत्तर:** API स्वयं सिंक्रोनस है, लेकिन आप कॉल्स को Java के `CompletableFuture` या थ्रेड पूल में रैप करके समानांतर निष्पादन कर सकते हैं।

## निष्कर्ष

अब आपके पास एक पूर्ण, **java tiff conversion** टूलकिट है जो आपको OneNote दस्तावेज़ों को JPEG, PackBits, या CCITT Group 3 Fax संपीड़न का उपयोग करके TIFF फ़ाइलों के रूप में सहेजने देता है। अपनी विशिष्ट **tiff इमेज क्वालिटी** आवश्यकताओं को पूरा करने के लिए क्वालिटी, कलर मोड, और रिज़ॉल्यूशन को समायोजित करें, और अधिकतम उत्पादकता के लिए इन मेथड्स को बैच वर्कफ़्लो में एकीकृत करें।

---

**अंतिम अपडेट:** 2025-12-17  
**परीक्षित संस्करण:** Aspose.Note for Java 23.12 (लेखन समय पर नवीनतम)  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}