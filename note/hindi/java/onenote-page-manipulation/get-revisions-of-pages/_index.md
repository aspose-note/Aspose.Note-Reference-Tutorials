---
title: OneNote में पृष्ठों का संशोधन प्राप्त करें - Aspose.Note
linktitle: OneNote में पृष्ठों का संशोधन प्राप्त करें - Aspose.Note
second_title: Aspose.नोट जावा एपीआई
description: जानें कि Aspose.Note Java का उपयोग करके OneNote दस्तावेज़ों में पृष्ठों के संशोधन कैसे प्राप्त करें। कुशल दस्तावेज़ प्रबंधन के लिए इसे अपने जावा ऐप्स में एकीकृत करें।
weight: 15
url: /hi/java/onenote-page-manipulation/get-revisions-of-pages/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote में पृष्ठों का संशोधन प्राप्त करें - Aspose.Note

## परिचय

इस ट्यूटोरियल में, हम जावा के लिए Aspose.Note की क्षमताओं के बारे में विस्तार से जानेंगे, जो एक शक्तिशाली लाइब्रेरी है जो आपको अपने जावा अनुप्रयोगों में Microsoft OneNote फ़ाइलों के साथ निर्बाध रूप से काम करने में सक्षम बनाती है। विशेष रूप से, हम इस बात पर ध्यान केंद्रित करेंगे कि OneNote दस्तावेज़ में पृष्ठों के संशोधनों को कैसे पुनः प्राप्त किया जाए। इस गाइड के अंत तक, आप पृष्ठ संशोधनों को कुशलतापूर्वक निकालने के ज्ञान से लैस हो जाएंगे, जिसमें अंतिम संशोधित समय, निर्माण समय, शीर्षक, स्तर और लेखक जैसे विवरण शामिल होंगे।

## आवश्यक शर्तें

इस ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपने निम्नलिखित आवश्यक शर्तें स्थापित कर ली हैं:

### जावा डेवलपमेंट किट (जेडीके) स्थापित

सुनिश्चित करें कि आपके सिस्टम पर जावा डेवलपमेंट किट स्थापित है। आप इसे Oracle वेबसाइट से डाउनलोड और इंस्टॉल कर सकते हैं या यदि आप यूनिक्स-आधारित सिस्टम पर हैं तो पैकेज मैनेजर का उपयोग कर सकते हैं।

### जावा लाइब्रेरी के लिए Aspose.Note

 वेबसाइट से जावा लाइब्रेरी के लिए Aspose.Note डाउनलोड और इंस्टॉल करें। आप डाउनलोड लिंक पा सकते हैं[यहाँ](https://releases.aspose.com/note/java/) . दस्तावेज़ में दिए गए इंस्टॉलेशन निर्देशों का पालन करें[यहाँ](https://reference.aspose.com/note/java/).

## पैकेज आयात करें

आरंभ करने के लिए, अपने जावा प्रोजेक्ट में आवश्यक पैकेज आयात करें। ये पैकेज आपको जावा के लिए Aspose.Note द्वारा प्रदान की गई कार्यक्षमता का लाभ उठाने की अनुमति देंगे।

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

अब, आइए प्रत्येक घटक और उसकी कार्यक्षमता को समझने के लिए दिए गए उदाहरण कोड को कई चरणों में विभाजित करें।

## चरण 1: दस्तावेज़ निर्देशिका सेट करें

उस निर्देशिका को परिभाषित करें जहाँ आपका OneNote दस्तावेज़ स्थित है।

```java
String dataDir = "Your Document Directory";
```

## चरण 2: दस्तावेज़ लोड करें

OneNote दस्तावेज़ को Aspose.Note में लोड करें।

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## चरण 3: पहला पृष्ठ प्राप्त करें

दस्तावेज़ से पहला पृष्ठ पुनः प्राप्त करें.

```java
Page firstPage = doc.getFirstChild();
```

## चरण 4: पृष्ठ संशोधन प्राप्त करें

पृष्ठ का संशोधन इतिहास प्राप्त करें।

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## चरण 5: ट्रैवर्स पृष्ठ संशोधन

पृष्ठ संशोधनों की सूची को दोबारा दोहराएं और प्रासंगिक जानकारी पुनः प्राप्त करें।

```java
for (Page pageRevision : revisions) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

## निष्कर्ष

इस ट्यूटोरियल में, हमने पता लगाया है कि जावा के लिए Aspose.Note का उपयोग करके OneNote दस्तावेज़ के भीतर पृष्ठों के संशोधन कैसे प्राप्त करें। चरण-दर-चरण मार्गदर्शिका का पालन करके और दिए गए उदाहरण कोड का लाभ उठाकर, आप OneNote फ़ाइलों के कुशल प्रबंधन को सक्षम करते हुए, इस कार्यक्षमता को अपने जावा अनुप्रयोगों में आसानी से एकीकृत कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं नए OneNote दस्तावेज़ बनाने के लिए Java के लिए Aspose.Note का उपयोग कर सकता हूँ?

A1: हाँ, Java के लिए Aspose.Note OneNote दस्तावेज़ों को प्रोग्रामेटिक रूप से बनाने, पढ़ने और हेरफेर करने के लिए व्यापक समर्थन प्रदान करता है।

### Q2: क्या जावा के लिए Aspose.Note OneNote फ़ाइलों के विभिन्न संस्करणों के साथ संगत है?

A2: हाँ, Java के लिए Aspose.Note Microsoft OneNote फ़ाइलों के विभिन्न संस्करणों का समर्थन करता है, जो विभिन्न वातावरणों में अनुकूलता सुनिश्चित करता है।

### Q3: क्या मैं OneNote दस्तावेज़ निर्यात करते समय आउटपुट स्वरूप को अनुकूलित कर सकता हूँ?

A3: बिल्कुल, जावा के लिए Aspose.Note अनुकूलन के विकल्पों के साथ OneNote दस्तावेज़ों को पीडीएफ, HTML और छवियों जैसे विभिन्न प्रारूपों में निर्यात करने में लचीलापन प्रदान करता है।

### Q4: क्या जावा के लिए Aspose.Note को व्यावसायिक उपयोग के लिए लाइसेंस की आवश्यकता है?

A4: हाँ, Java के लिए Aspose.Note के व्यावसायिक उपयोग के लिए एक वैध लाइसेंस आवश्यक है। आप Aspose वेबसाइट से लाइसेंस प्राप्त कर सकते हैं।

### Q5: अगर मुझे जावा के लिए Aspose.Note के बारे में कोई समस्या आती है या मेरे कोई प्रश्न हैं तो मैं कहां सहायता ले सकता हूं?

 A5: समर्थन और सहायता के लिए, आप Aspose.Note फोरम पर जा सकते हैं[यहाँ](https://forum.aspose.com/c/note/28)जहां आप प्रश्न पूछ सकते हैं, अनुभव साझा कर सकते हैं और अन्य उपयोगकर्ताओं और विशेषज्ञों के साथ बातचीत कर सकते हैं।
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
