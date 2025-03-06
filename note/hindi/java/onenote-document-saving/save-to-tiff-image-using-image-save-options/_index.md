---
title: OneNote में छवि सहेजें विकल्पों का उपयोग करके TIFF छवि में सहेजें
linktitle: OneNote में छवि सहेजें विकल्पों का उपयोग करके TIFF छवि में सहेजें
second_title: Aspose.नोट जावा एपीआई
description: OneNote दस्तावेज़ों को TIFF में बदलें और फ़ाइल आकार और गुणवत्ता नियंत्रित करें! जावा में जेपीईजी, पैकबिट्स या फैक्स कम्प्रेशन चुनें। कोड उदाहरण प्राप्त करें और सीखें कि कैसे! #वननोट #जावा #एस्पोज़
weight: 21
url: /hi/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote में छवि सहेजें विकल्पों का उपयोग करके TIFF छवि में सहेजें

## परिचय

इस ट्यूटोरियल में, आप सीखेंगे कि जावा के लिए Aspose.Note में विभिन्न संपीड़न विधियों का उपयोग करके किसी दस्तावेज़ को TIFF छवि प्रारूप में कैसे सहेजा जाए। हम पूर्वापेक्षाओं, पैकेजों को आयात करने, और प्रत्येक संपीड़न विधि के लिए चरण-दर-चरण मार्गदर्शिका प्रदान करेंगे।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

- आपके सिस्टम पर जावा डेवलपमेंट किट (जेडीके) स्थापित है।
- जावा लाइब्रेरी के लिए Aspose.Note डाउनलोड और कॉन्फ़िगर किया गया।
- जावा प्रोग्रामिंग भाषा की बुनियादी समझ।

## पैकेज आयात करें

सबसे पहले, आपको अपनी जावा फ़ाइल में आवश्यक पैकेज आयात करने होंगे:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## चरण 1: JPEG संपीड़न का उपयोग करके TIFF में सहेजें

```java
public static void SaveToTiffUsingJpegCompression() throws IOException {
    // दस्तावेज़ निर्देशिका का पथ.
    String dataDir = "Your Document Directory";

    // दस्तावेज़ को Aspose.Note में लोड करें।
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.Jpeg);
    options.setQuality(93);

    oneFile.save(Paths.get(dataDir,"SaveToTiffUsingJpegCompression.tiff").toString(), options);
}
```

-  का उपयोग करके दस्तावेज़ लोड करें`Document` कक्षा।
-  का एक उदाहरण बनाएं`ImageSaveOptions` और TIFF संपीड़न प्रकार को JPEG के रूप में निर्दिष्ट करें।
- वांछित गुणवत्ता सेट करें (वैकल्पिक)।
- निर्दिष्ट विकल्पों का उपयोग करके दस्तावेज़ को TIFF प्रारूप में सहेजें।

## चरण 2: पैकबिट्स कंप्रेशन का उपयोग करके TIFF में सहेजें

```java
public static void SaveToTiffUsingPackBitsCompression() throws IOException {
    // दस्तावेज़ निर्देशिका का पथ.
    String dataDir = "Your Document Directory";

    // दस्तावेज़ को Aspose.Note में लोड करें।
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.PackBits);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingPackBitsCompression.tiff").toString(), options);
}
```

-  का उपयोग करके दस्तावेज़ लोड करें`Document` कक्षा।
-  का एक उदाहरण बनाएं`ImageSaveOptions` और TIFF संपीड़न प्रकार को पैकबिट्स के रूप में निर्दिष्ट करें।
- निर्दिष्ट विकल्पों का उपयोग करके दस्तावेज़ को TIFF प्रारूप में सहेजें।

## चरण 3: CCITT समूह 3 फैक्स संपीड़न का उपयोग करके TIFF में सहेजें

```java
public static void SaveToTiffUsingCcitt3Compression() throws IOException {
    // दस्तावेज़ निर्देशिका का पथ.
    String dataDir = "Your Document Directory";

    // दस्तावेज़ को Aspose.Note में लोड करें।
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setColorMode(ColorMode.BlackAndWhite);
    options.setTiffCompression(TiffCompression.Ccitt3);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingCcitt3Compression.tiff").toString(), options);
}
```

-  का उपयोग करके दस्तावेज़ लोड करें`Document` कक्षा।
-  का एक उदाहरण बनाएं`ImageSaveOptions` और TIFF संपीड़न प्रकार को CCITT समूह 3 फैक्स के रूप में निर्दिष्ट करें।
- रंग मोड को काले और सफेद पर सेट करें।
- निर्दिष्ट विकल्पों का उपयोग करके दस्तावेज़ को TIFF प्रारूप में सहेजें।

## निष्कर्ष

इस ट्यूटोरियल में, आपने सीखा कि जावा के लिए Aspose.Note में विभिन्न संपीड़न विधियों का उपयोग करके किसी दस्तावेज़ को TIFF छवि प्रारूप में कैसे सहेजा जाए। चरण-दर-चरण मार्गदर्शिका का पालन करके, आप अपनी आवश्यकताओं को पूरा करने के लिए Aspose.Note की क्षमताओं का कुशलतापूर्वक उपयोग कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं अन्य दस्तावेज़ प्रारूपों को TIFF में बदलने के लिए Java के लिए Aspose.Note का उपयोग कर सकता हूँ?

A1: हाँ, Java के लिए Aspose.Note OneNote दस्तावेज़ों सहित विभिन्न दस्तावेज़ स्वरूपों से TIFF में रूपांतरण का समर्थन करता है।

### Q2: TIFF में सहेजते समय संपीड़न प्रकार निर्दिष्ट करने का क्या महत्व है?

A2: संपीड़न प्रकार निर्दिष्ट करने से आप छवि गुणवत्ता और फ़ाइल आकार को नियंत्रित कर सकते हैं। विभिन्न संपीड़न विधियाँ गुणवत्ता और संपीड़न अनुपात के बीच व्यापार-बंद की पेशकश करती हैं।

### Q3: क्या जावा के लिए Aspose.Note दस्तावेज़ों की बैच प्रोसेसिंग के लिए उपयुक्त है?

A3: हां, Java के लिए Aspose.Note बैच प्रोसेसिंग के लिए एपीआई प्रदान करता है, जो आपको दस्तावेज़ रूपांतरण कार्यों को कुशलतापूर्वक स्वचालित करने में सक्षम बनाता है।

### Q4: क्या मैं कम्प्रेशन सेटिंग्स को और अधिक अनुकूलित कर सकता हूँ?

A4: हां, आप अपनी आवश्यकताओं के अनुसार आउटपुट को तैयार करने के लिए गुणवत्ता, रिज़ॉल्यूशन और संपीड़न विधि जैसे मापदंडों को समायोजित कर सकते हैं।

### Q5: क्या जावा के लिए Aspose.Note तकनीकी सहायता प्रदान करता है?

A5: हाँ, Aspose मंचों और टिकट-आधारित प्रणालियों के माध्यम से व्यापक तकनीकी सहायता प्रदान करता है।
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
