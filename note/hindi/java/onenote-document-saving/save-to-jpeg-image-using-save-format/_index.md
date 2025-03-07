---
title: OneNote में सेव फ़ॉर्मेट का उपयोग करके JPEG छवि में सेव करें
linktitle: OneNote में सेव फ़ॉर्मेट का उपयोग करके JPEG छवि में सेव करें
second_title: Aspose.नोट जावा एपीआई
description: OneNote दस्तावेज़ को आसानी से JPEG छवि में बदलें! यह जावा ट्यूटोरियल Aspose.Note का उपयोग करने का तरीका दिखाता है। कोड उदाहरणों के साथ कनवर्ट और स्वचालित करें! #वननोट #जावा #एस्पोज़
weight: 18
url: /hi/java/onenote-document-saving/save-to-jpeg-image-using-save-format/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote में सेव फ़ॉर्मेट का उपयोग करके JPEG छवि में सेव करें

## परिचय

इस ट्यूटोरियल में, हम Java के लिए Aspose.Note का उपयोग करके किसी दस्तावेज़ को JPEG छवि प्रारूप में सहेजने की प्रक्रिया के बारे में विस्तार से जानेंगे। Aspose.Note एक शक्तिशाली जावा एपीआई है जो डेवलपर्स को Microsoft OneNote फ़ाइलों के साथ प्रोग्रामेटिक रूप से काम करने की अनुमति देता है, जिससे सामग्री के रूपांतरण, हेरफेर और निष्कर्षण जैसे विभिन्न संचालन सक्षम होते हैं।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

1. जावा विकास पर्यावरण: सुनिश्चित करें कि आपके सिस्टम पर जावा डेवलपमेंट किट (जेडीके) स्थापित है।
2.  जावा लाइब्रेरी के लिए Aspose.Note: जावा लाइब्रेरी के लिए Aspose.Note को डाउनलोड और इंस्टॉल करें। आप इसे यहां से डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/note/java/).

## पैकेज आयात करें

सबसे पहले, आइए अपने जावा कोड के लिए आवश्यक आवश्यक पैकेज आयात करें:

```java
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## चरण 1: दस्तावेज़ लोड करें

 प्रारंभिक चरण दस्तावेज़ को Aspose.Note में लोड करना है। का उपयोग करके इसे पूरा किया जा सकता है`Document` Aspose.Note द्वारा प्रदान की गई कक्षा।

```java
// दस्तावेज़ निर्देशिका का पथ.
String dataDir = "Your Document Directory";

// दस्तावेज़ को Aspose.Note में लोड करें।
Document oneFile = new Document(dataDir + "Aspose.one");
```

## चरण 2: JPEG छवि के रूप में सहेजें

 इसके बाद, हम आउटपुट फ़ाइल पथ निर्दिष्ट करेंगे और दस्तावेज़ को JPEG छवि प्रारूप का उपयोग करके सहेजेंगे`save()` विधि के साथ`SaveFormat.Jpeg` पैरामीटर.

```java
// आउटपुट फ़ाइल पथ निर्दिष्ट करें.
dataDir = dataDir + "SaveToJpegImageUsingSaveFormat_out.jpg";

// दस्तावेज़ सहेजें.
oneFile.save(dataDir, SaveFormat.Jpeg);
```

## निष्कर्ष

इस ट्यूटोरियल में, हमने सीखा कि जावा के लिए Aspose.Note का उपयोग करके किसी दस्तावेज़ को JPEG छवि के रूप में कैसे सहेजा जाए। दिए गए चरणों का पालन करके, आप अपने OneNote फ़ाइलों को प्रोग्रामेटिक रूप से JPEG प्रारूप में परिवर्तित कर सकते हैं, जिससे आपके जावा अनुप्रयोगों में एकीकरण और स्वचालन की विभिन्न संभावनाएं सक्षम हो सकती हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Aspose.Note जटिल OneNote फ़ाइलों को संभाल सकता है?

A1: हाँ, Aspose.Note को जटिल OneNote फ़ाइलों को कुशलतापूर्वक संभालने, सटीक रूपांतरण और हेरफेर सुनिश्चित करने के लिए डिज़ाइन किया गया है।

### Q2: क्या Java के लिए Aspose.Note का कोई परीक्षण संस्करण उपलब्ध है?

 उ2: हाँ, आप जावा के लिए Aspose.Note का निःशुल्क परीक्षण संस्करण प्राप्त कर सकते हैं[यहाँ](https://releases.aspose.com/).

### Q3: मैं जावा के लिए Aspose.Note के लिए समर्थन कैसे प्राप्त कर सकता हूं?

 उ3: आप यहां जाकर जावा के लिए Aspose.Note के लिए समर्थन प्राप्त कर सकते हैं[Aspose.नोट फोरम](https://forum.aspose.com/c/note/28).

### Q4: क्या मैं जावा के लिए Aspose.Note के लिए एक अस्थायी लाइसेंस खरीद सकता हूँ?

 उ4: हां, आप यहां से अस्थायी लाइसेंस खरीद सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/).

### Q5: मैं जावा के लिए Aspose.Note के लिए विस्तृत दस्तावेज़ कहां पा सकता हूं?

A5: आप Java के लिए Aspose.Note के लिए विस्तृत दस्तावेज़ पा सकते हैं[यहाँ](https://reference.aspose.com/note/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
