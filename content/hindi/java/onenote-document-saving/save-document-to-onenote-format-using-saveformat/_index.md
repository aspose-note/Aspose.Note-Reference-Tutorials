---
title: SaveFormat का उपयोग करके दस्तावेज़ को OneNote में सहेजें - Aspose.Note
linktitle: SaveFormat का उपयोग करके दस्तावेज़ को OneNote में सहेजें - Aspose.Note
second_title: Aspose.नोट जावा एपीआई
description: जावा के लिए Aspose.Note का उपयोग करके दस्तावेज़ों को OneNote प्रारूप में सहेजना सीखें। अपने जावा अनुप्रयोगों में निर्बाध एकीकरण के लिए इस चरण-दर-चरण ट्यूटोरियल का पालन करें।
type: docs
weight: 12
url: /hi/java/onenote-document-saving/save-document-to-onenote-format-using-saveformat/
---
## परिचय

Java के लिए Aspose.Note एक शक्तिशाली लाइब्रेरी है जो डेवलपर्स को Microsoft OneNote फ़ाइलों के साथ प्रोग्रामेटिक रूप से काम करने में सक्षम बनाती है। SaveFormat का उपयोग करके किसी दस्तावेज़ को OneNote प्रारूप में सहेजना एक सीधी प्रक्रिया है। इस ट्यूटोरियल में, हम इस कार्य को पूरा करने के लिए आवश्यक चरणों से गुजरेंगे।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

1. आपके सिस्टम पर जावा डेवलपमेंट किट (जेडीके) स्थापित है।
2.  जावा लाइब्रेरी के लिए Aspose.Note डाउनलोड किया गया। आप इसे यहां से प्राप्त कर सकते हैं[यहाँ](https://releases.aspose.com/note/java/).
3. जावा प्रोग्रामिंग भाषा की बुनियादी समझ।

## पैकेज आयात करें

 सबसे पहले, आपको अपने जावा प्रोजेक्ट में आवश्यक पैकेज आयात करने होंगे। इसमें आयात करना भी शामिल है`com.aspose.note` Aspose.Note कार्यक्षमताओं के साथ काम करने के लिए पैकेज।

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.SaveFormat;
```

## चरण 1: दस्तावेज़ निर्देशिका सेट करें

उस निर्देशिका को परिभाषित करें जहां आपका दस्तावेज़ स्थित है और जहां आप आउटपुट फ़ाइल को सहेजना चाहते हैं।

```java
String dataDir = "Your Document Directory";
```

## चरण 2: दस्तावेज़ लोड करें

 का उपयोग करके दस्तावेज़ को अपने जावा एप्लिकेशन में लोड करें`Document` Aspose.Note द्वारा प्रदान की गई कक्षा।

```java
Document document = new Document(dataDir + "Sample1.one");
```

## चरण 3: दस्तावेज़ को OneNote प्रारूप में सहेजें

का उपयोग करके लोड किए गए दस्तावेज़ को OneNote प्रारूप में सहेजें`save` विधि और वांछित आउटपुट फ़ाइल स्वरूप को निर्दिष्ट करना`SaveFormat.One`.

```java
document.save(dataDir + "SaveDocToOneNoteFormatUsingSaveformat_out.one", SaveFormat.One);
```

## निष्कर्ष

इस ट्यूटोरियल में, हमने सीखा कि जावा के लिए Aspose.Note में SaveFormat का उपयोग करके किसी दस्तावेज़ को OneNote प्रारूप में कैसे सहेजा जाए। इन सरल चरणों का पालन करके, आप इस कार्यक्षमता को अपने जावा अनुप्रयोगों में सहजता से एकीकृत कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Java के लिए Aspose.Note Microsoft OneNote के सभी संस्करणों के साथ संगत है?

A1: Java के लिए Aspose.Note विभिन्न परिवेशों में अनुकूलता सुनिश्चित करते हुए, Microsoft OneNote के विभिन्न संस्करणों का समर्थन करता है।

### Q2: क्या मैं जावा खरीदने से पहले Aspose.Note को आज़मा सकता हूँ?

 उ2: हाँ, आप जावा के लिए Aspose.Note का निःशुल्क परीक्षण संस्करण डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/).

### Q3: मैं जावा के लिए Aspose.Note के लिए दस्तावेज़ कहां पा सकता हूं?

 A3: Java के लिए Aspose.Note के लिए विस्तृत दस्तावेज़ पाया जा सकता है[यहाँ](https://reference.aspose.com/note/java/).

### Q4: मैं जावा के लिए Aspose.Note के लिए तकनीकी सहायता कैसे प्राप्त कर सकता हूं?

 A4: तकनीकी सहायता और समर्थन के लिए, आप Aspose.Note फोरम पर जा सकते हैं[यहाँ](https://forum.aspose.com/c/note/28).

### Q5: क्या Java के लिए Aspose.Note के लिए कोई अस्थायी लाइसेंस विकल्प उपलब्ध है?

 A5: हाँ, आप Java के लिए Aspose.Note के लिए एक अस्थायी लाइसेंस प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/).