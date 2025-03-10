---
title: OneNote में वर्तमान पृष्ठ संस्करण पुश करें - Aspose.Note
linktitle: OneNote में वर्तमान पृष्ठ संस्करण पुश करें - Aspose.Note
second_title: Aspose.नोट जावा एपीआई
description: OneNote सामग्री को ताज़ा रखें! पृष्ठ इतिहास को अद्यतन करना और संस्करण प्रबंधित करना सीखें, चरण-दर-चरण मार्गदर्शिका और कोड शामिल हैं। #वननोट #जावा #एस्पोज़
weight: 18
url: /hi/java/onenote-page-manipulation/push-current-page-version/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote में वर्तमान पृष्ठ संस्करण पुश करें - Aspose.Note

## परिचय

इस ट्यूटोरियल में, हम यह पता लगाएंगे कि OneNote में वर्तमान पेज संस्करण को पुश करने के लिए Java के लिए Aspose.Note का उपयोग कैसे करें। Aspose.Note एक शक्तिशाली जावा लाइब्रेरी है जो डेवलपर्स को Microsoft OneNote दस्तावेज़ों के साथ प्रोग्रामेटिक रूप से काम करने की अनुमति देती है, जिससे OneNote फ़ाइलों को बनाने, हेरफेर करने और परिवर्तित करने जैसे विभिन्न संचालन सक्षम होते हैं।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित शर्तें हैं:
1. जावा प्रोग्रामिंग भाषा का बुनियादी ज्ञान।
2. आपके सिस्टम पर जावा डेवलपमेंट किट (जेडीके) स्थापित किया गया।
3.  जावा लाइब्रेरी के लिए Aspose.Note। आप इसे यहां से डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/note/java/).
4. काम करने के लिए एक नमूना OneNote दस्तावेज़।

## पैकेज आयात करें

सबसे पहले, आपको Aspose.Note कार्यक्षमताओं का उपयोग करने के लिए अपने जावा प्रोजेक्ट में आवश्यक पैकेज आयात करने की आवश्यकता है।

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## चरण 1: OneNote दस्तावेज़ लोड करें

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
```

 यहाँ,`dataDir` उस निर्देशिका को इंगित करना चाहिए जहां आपका OneNote दस्तावेज़ स्थित है। प्रतिस्थापित करें`"Sample1.one"` आपकी OneNote फ़ाइल के नाम के साथ.

## चरण 2: वर्तमान पृष्ठ और उसका इतिहास प्राप्त करें

```java
Page page = document.getFirstChild();
PageHistory pageHistory = document.getPageHistory(page);
```

 हम दस्तावेज़ का पहला पृष्ठ पुनः प्राप्त करते हैं`getFirstChild()` और फिर इसका उपयोग करके इसका इतिहास प्राप्त करें`getPageHistory()`.

## चरण 3: वर्तमान पृष्ठ संस्करण को पुश करें

```java
pageHistory.addItem(page.deepClone());
```

यहां, हम पृष्ठ के वर्तमान संस्करण को उसके इतिहास में क्लोन करके और एक नए आइटम के रूप में जोड़ते हैं।

## चरण 4: दस्तावेज़ सहेजें

```java
document.save(dataDir + "PushCurrentPageVersion_out.one");
```

अंत में, हम संशोधित दस्तावेज़ को अद्यतन पृष्ठ इतिहास के साथ सहेजते हैं।

## निष्कर्ष

इस ट्यूटोरियल में, हमने सीखा कि Java के लिए Aspose.Note का उपयोग करके OneNote में वर्तमान पृष्ठ संस्करण को कैसे पुश किया जाए। इन चरणों का पालन करके, आप अपने OneNote दस्तावेज़ों के संस्करण को प्रोग्रामेटिक रूप से प्रभावी ढंग से प्रबंधित कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं एन्क्रिप्टेड OneNote फ़ाइलों के साथ काम करने के लिए Java के लिए Aspose.Note का उपयोग कर सकता हूँ?

A1: हाँ, Java के लिए Aspose.Note एन्क्रिप्टेड और अनएन्क्रिप्टेड OneNote फ़ाइलों दोनों के साथ काम करने का समर्थन करता है।

### Q2: क्या जावा के लिए Aspose.Note OneNote के नवीनतम संस्करण के साथ संगत है?

A2: Java के लिए Aspose.Note OneNote दस्तावेज़ों के नवीनतम संस्करणों के साथ संगतता बनाए रखने का प्रयास करता है।

### Q3: क्या मैं Java के लिए Aspose.Note का उपयोग करके OneNote दस्तावेज़ों में पाठ और छवियों में हेरफेर कर सकता हूँ?

A3: बिल्कुल, जावा के लिए Aspose.Note OneNote फ़ाइलों के भीतर पाठ, छवियों और अन्य तत्वों में हेरफेर करने के लिए व्यापक कार्यक्षमता प्रदान करता है।

### Q4: क्या जावा के लिए Aspose.Note OneNote फ़ाइलों को अन्य प्रारूपों में बदलने का समर्थन करता है?

A4: हां, Java के लिए Aspose.Note OneNote फ़ाइलों को पीडीएफ, HTML और छवि प्रारूपों जैसे विभिन्न प्रारूपों में परिवर्तित करने का समर्थन करता है।

### Q5: यदि मुझे कोई समस्या आती है तो मैं जावा के लिए Aspose.Note के लिए समर्थन कहां से प्राप्त कर सकता हूं?

 A5: आप यहां जा सकते हैं[Aspose.नोट फोरम](https://forum.aspose.com/c/note/28) समुदाय से सहायता लेने के लिए या सीधे Aspose समर्थन से संपर्क करने के लिए।
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
