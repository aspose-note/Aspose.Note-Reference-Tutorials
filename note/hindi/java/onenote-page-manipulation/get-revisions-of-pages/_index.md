---
date: 2026-01-10
description: Aspose.Note for Java का उपयोग करके OneNote पृष्ठों का अंतिम संशोधित समय
  प्राप्त करना और संशोधन निकालना सीखें। इसे अपने Java एप्लिकेशनों में एकीकृत करके
  कुशल दस्तावेज़ प्रबंधन प्राप्त करें।
linktitle: Get Revisions of Pages in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: OneNote पृष्ठों का अंतिम संशोधित समय कैसे प्राप्त करें – Aspose.Note
url: /hi/java/onenote-page-manipulation/get-revisions-of-pages/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote में पृष्ठों के संशोधनों को प्राप्त करें - Aspose.Note

## परिचय

## त्वरित उत्तर
- **“get last modified time” क्या लौटाता है?** OneNote पृष्ठ पर सबसे हालिया संपादन का टाइमस्टैम्प।  
- **कौन सा क्लास संशोधन इतिहास प्रदान करता है?** `PageHistory` द्वारा `Document.getPageHistory(Page)`।  
- **क्या इस फीचर के लिए लाइसेंस आवश्यक है?** हाँ, उत्पादन उपयोग के लिए एक वैध Aspose.Note लाइसेंस आवश्यक है।  
- **कौन सा Java संस्करण समर्थित है?** Java 8 या उससे ऊपर (JDK 8+).  
- **क्या मैं लेखक के आधार पर संशोधनों को फ़िल्टर कर सकता हूँ?** आप प्रत्येक `Page` ऑब्जेक्ट की `Author` प्रॉपर्टी पढ़ सकते हैं और अपना फ़िल्टर लागू कर सकते हैं।

## OneNote में “get last modified time” क्या है?
**last modified time** एक मेटाडेटा फ़ील्ड है जो प्रत्येक पृष्ठ के साथ संग्रहीत होता है और यह रिकॉर्ड करता है कि पृष्ठ को आखिरी बार कब बदलाया गया था। Aspose.Note इस मान को `Page.getLastModifiedTime()` मेथड के माध्यम से उजागर करता है, जिससे परिवर्तन तिथियों को प्रदर्शित या लॉग करना आसान हो जाता है।

## पृष्ठ संशोधन क्यों प्राप्त करें?
- **ऑडिट ट्रेल्स:** कौन ने क्या और कब बदला, इसका रिकॉर्ड रखें।  
- **वर्ज़न तुलना:** ऐसी सुविधाएँ बनाएं जो दो संशोधनों की साइड‑बाय‑साइड तुलना करें।  
- **उपयोगकर्ता सहयोग अंतर्दृष्टि:** साझा नोटबुक्स में संपादन पैटर्न को समझें।  

## पूर्वापेक्षाएँ

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

### Java Development Kit (JDK) स्थापित है
Oracle वेबसाइट या अपने पसंदीदा पैकेज मैनेजर से JDK 8 या उसके बाद का संस्करण स्थापित करें।

### Aspose.Note for Java लाइब्रेरी
आधिकारिक साइट से लाइब्रेरी डाउनलोड करें। आप डाउनलोड लिंक **[here](https://releases.aspose.com/note/java/)** पर पा सकते हैं। दस्तावेज़ीकरण में स्थापित करने के निर्देश **[here](https://reference.aspose.com/note/java/)** देखें।

## पैकेज आयात करें

शुरू करने के लिए, आवश्यक पैकेजों को अपने Java प्रोजेक्ट में आयात करें। ये पैकेज आपको Aspose.Note for Java द्वारा प्रदान की गई कार्यक्षमता का उपयोग करने में सक्षम करेंगे।

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

अब, प्रदान किए गए उदाहरण कोड को कई चरणों में विभाजित करते हैं ताकि प्रत्येक घटक और उसकी कार्यक्षमता को समझ सकें।

## OneNote पृष्ठ का अंतिम संशोधित समय कैसे प्राप्त करें

### चरण 1: दस्तावेज़ निर्देशिका सेट करें
उस निर्देशिका को परिभाषित करें जहाँ आपका OneNote दस्तावेज़ स्थित है।

```java
String dataDir = "Your Document Directory";
```

### चरण 2: दस्तावेज़ लोड करें
OneNote दस्तावेज़ को Aspose.Note में लोड करें।

```java
Document doc = new Document(dataDir + "Sample1.one");
```

### चरण 3: पहला पृष्ठ प्राप्त करें
दस्तावेज़ से पहला पृष्ठ प्राप्त करें।

```java
Page firstPage = doc.getFirstChild();
```

### चरण 4: पृष्ठ संशोधन प्राप्त करें
पृष्ठ की संशोधन इतिहास प्राप्त करें।

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

### चरण 5: पृष्ठ संशोधनों को पार करें
पृष्ठ संशोधनों की सूची पर इटररेट करें और संबंधित जानकारी प्राप्त करें, जिसमें **last modified time** शामिल है।

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

## सामान्य समस्याएँ और समाधान
- **Null `PageHistory`:** सुनिश्चित करें कि दस्तावेज़ में वास्तव में संशोधन हैं; अन्यथा `getPageHistory` `null` लौट सकता है।  
- **समय क्षेत्र अंतर:** `getLastModifiedTime()` सिस्टम के डिफ़ॉल्ट टाइमज़ोन में `java.util.Date` लौटाता है। आवश्यकता होने पर इसे UTC में परिवर्तित करें।  
- **लाइसेंस लोड नहीं हुआ:** वैध लाइसेंस के बिना, Aspose.Note मूल्यांकन मोड में चल सकता है, जिससे प्रोसेस किए जाने वाले पृष्ठों की संख्या सीमित हो जाती है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं Aspose.Note for Java का उपयोग करके नए OneNote दस्तावेज़ बना सकता हूँ?
A1: हाँ, Aspose.Note for Java प्रोग्रामेटिक रूप से OneNote दस्तावेज़ बनाने, पढ़ने और संशोधित करने के लिए व्यापक समर्थन प्रदान करता है।

### Q2: क्या Aspose.Note for Java विभिन्न संस्करणों के OneNote फ़ाइलों के साथ संगत है?
A2: हाँ, Aspose.Note for Java Microsoft OneNote फ़ाइलों के विभिन्न संस्करणों का समर्थन करता है, जिससे विभिन्न परिवेशों में संगतता सुनिश्चित होती है।

### Q3: क्या मैं OneNote दस्तावेज़ निर्यात करते समय आउटपुट फ़ॉर्मेट को कस्टमाइज़ कर सकता हूँ?
A3: बिल्कुल, Aspose.Note for Java OneNote दस्तावेज़ों को विभिन्न फ़ॉर्मेट जैसे PDF, HTML, और इमेज़ में निर्यात करने में लचीलापन प्रदान करता है, जिसमें कस्टमाइज़ेशन विकल्प भी शामिल हैं।

### Q4: क्या Aspose.Note for Java को व्यावसायिक उपयोग के लिए लाइसेंस की आवश्यकता है?
A4: हाँ, Aspose.Note for Java के व्यावसायिक उपयोग के लिए एक वैध लाइसेंस आवश्यक है। आप Aspose वेबसाइट से लाइसेंस प्राप्त कर सकते हैं।

### Q5: यदि मुझे समस्याएँ आती हैं या Aspose.Note for Java के बारे में प्रश्न हैं तो मैं सहायता कहाँ प्राप्त कर सकता हूँ?
A5: समर्थन और सहायता के लिए, आप Aspose.Note फ़ोरम **[here](https://forum.aspose.com/c/note/28)** पर जा सकते हैं, जहाँ आप प्रश्न पूछ सकते हैं, अनुभव साझा कर सकते हैं, और अन्य उपयोगकर्ताओं व विशेषज्ञों के साथ संवाद कर सकते हैं।

---

**अंतिम अपडेट:** 2026-01-10  
**परीक्षित संस्करण:** Aspose.Note for Java 23.12 (लेखन के समय नवीनतम)  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}