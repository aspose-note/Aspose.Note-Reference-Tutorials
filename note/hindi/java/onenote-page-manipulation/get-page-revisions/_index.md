---
title: OneNote में पृष्ठ संशोधन प्राप्त करें - Aspose.Note
linktitle: OneNote में पृष्ठ संशोधन प्राप्त करें - Aspose.Note
second_title: Aspose.नोट जावा एपीआई
description: जावा के लिए Aspose.Note का उपयोग करके OneNote में पृष्ठ संशोधन पुनः प्राप्त करने का तरीका जानें। परिवर्तनों की कुशल ट्रैकिंग के लिए हमारी चरण-दर-चरण मार्गदर्शिका का पालन करें।
type: docs
weight: 14
url: /hi/java/onenote-page-manipulation/get-page-revisions/
---
## परिचय

OneNote आपके नोट्स को व्यवस्थित और प्रबंधित करने के लिए एक शक्तिशाली उपकरण है, लेकिन कभी-कभी आपको अपने पृष्ठों में किए गए परिवर्तनों और संशोधनों को ट्रैक करने की आवश्यकता होती है। जावा के लिए Aspose.Note के साथ, आप प्रोग्रामेटिक रूप से पृष्ठ संशोधनों को आसानी से पुनः प्राप्त कर सकते हैं। इस ट्यूटोरियल में, हम जावा के लिए Aspose.Note का उपयोग करके OneNote में पेज संशोधन प्राप्त करने की प्रक्रिया में आपका मार्गदर्शन करेंगे।

## आवश्यक शर्तें

आरंभ करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

### 1. जावा डेवलपमेंट किट (जेडीके)

सुनिश्चित करें कि आपके सिस्टम पर जावा डेवलपमेंट किट (जेडीके) स्थापित है। आप Oracle वेबसाइट से JDK डाउनलोड और इंस्टॉल कर सकते हैं।

### 2. जावा के लिए Aspose.Note

जावा के लिए Aspose.Note को डाउनलोड और इंस्टॉल करें[लिंक को डाउनलोड करें](https://releases.aspose.com/note/java/).

### 3. नमूना वननोट दस्तावेज़

एक नमूना OneNote दस्तावेज़ तैयार करें (`Sample1.one`) जिसमें वे पृष्ठ शामिल हैं जिनसे आप संशोधन पुनः प्राप्त करना चाहते हैं।

## पैकेज आयात करें

सबसे पहले, आपको Java के लिए Aspose.Note से आवश्यक पैकेज आयात करने होंगे।

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

अब, आइए दिए गए उदाहरण को कई चरणों में तोड़ें:

## चरण 1: दस्तावेज़ निर्देशिका सेट करें

उस निर्देशिका पथ को परिभाषित करें जहाँ आपका OneNote दस्तावेज़ स्थित है।

```java
String dataDir = "Your Document Directory";
```

## चरण 2: OneNote दस्तावेज़ लोड करें

 OneNote दस्तावेज़ का उपयोग करके लोड करें`LoadOptions` लोडिंग इतिहास सक्षम करने के लिए।

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

## चरण 3: पहला पृष्ठ प्राप्त करें

लोड किए गए दस्तावेज़ से पहला पृष्ठ पुनर्प्राप्त करें।

```java
Page firstPage = document.getFirstChild();
```

## चरण 4: पृष्ठ संशोधन के माध्यम से पुनरावृति करें

प्रत्येक पृष्ठ संशोधन के माध्यम से पुनरावृत्ति करें और अंतिम संशोधित समय, निर्माण समय, शीर्षक, स्तर और लेखक जैसी प्रासंगिक जानकारी पुनः प्राप्त करें।

```java
for (Page pageRevision : document.getPageHistory(firstPage)) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

## निष्कर्ष

इस ट्यूटोरियल में, हमने सीखा कि Java के लिए Aspose.Note का उपयोग करके OneNote में पेज संशोधन कैसे प्राप्त करें। इन चरणों का पालन करके, आप अपने OneNote पृष्ठों में किए गए परिवर्तनों को प्रोग्रामेटिक रूप से कुशलतापूर्वक ट्रैक कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं पृष्ठ संशोधनों को संशोधित करने के लिए जावा के लिए Aspose.Note का उपयोग कर सकता हूँ?

A1: नहीं, Java के लिए Aspose.Note वर्तमान में पृष्ठ संशोधनों को पुनर्प्राप्त करने का समर्थन करता है लेकिन उन्हें संशोधित नहीं करता है।

### Q2: क्या जावा के लिए Aspose.Note OneNote दस्तावेज़ों के विभिन्न संस्करणों के साथ संगत है?

A2: हाँ, Java के लिए Aspose.Note OneNote दस्तावेज़ों के विभिन्न संस्करणों का समर्थन करता है, जिससे आप विभिन्न फ़ाइल स्वरूपों के साथ निर्बाध रूप से काम कर सकते हैं।

### Q3: क्या Java के लिए Aspose.Note का उपयोग करने के लिए लाइसेंस की आवश्यकता है?

उ3: हां, आपको वाणिज्यिक परियोजनाओं में जावा के लिए Aspose.Note का उपयोग करने के लिए लाइसेंस खरीदने की आवश्यकता है। हालाँकि, आप मूल्यांकन उद्देश्यों के लिए एक अस्थायी लाइसेंस भी प्राप्त कर सकते हैं।

### Q4: यदि जावा के लिए Aspose.Note का उपयोग करते समय मुझे कोई समस्या आती है तो क्या मैं सहायता मांग सकता हूँ?

 उ4: हां, आप Aspose.Note फोरम से समर्थन मांग सकते हैं[यहाँ](https://forum.aspose.com/c/note/28).

### Q5: क्या Java के लिए Aspose.Note का कोई निःशुल्क परीक्षण उपलब्ध है?

 A5: हां, आप जावा के लिए Aspose.Note का निःशुल्क परीक्षण प्राप्त कर सकते हैं[वेबसाइट](https://releases.aspose.com/).