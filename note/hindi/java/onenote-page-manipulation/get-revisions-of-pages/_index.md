---
date: 2026-08-13
description: जानेँ कि Aspose.Note for Java के साथ OneNote पेज का संशोधित समय कैसे
  प्राप्त करें और पेज संशोधनों को पुनः प्राप्त करें, जो ऑडिटिंग और दस्तावेज़ प्रबंधन
  के लिए आदर्श है।
keywords:
- get onenote page modified
- onenote page revisions
- aspose.note java
- java onenote api
lastmod: 2026-08-13
linktitle: OneNote में पेजों के संशोधन प्राप्त करें - Aspose.Note
og_description: Aspose.Note for Java के साथ OneNote पेज का संशोधित समय कैसे प्राप्त
  करें और पेजों के संशोधन कैसे पुनः प्राप्त करें, जानें। त्वरित चरण, कोड स्निपेट और
  समस्या निवारण।
og_image_alt: Screenshot of Aspose.Note Java API showing page revision retrieval
og_title: Aspose.Note का उपयोग करके OneNote पेज संशोधित समय प्राप्त करें – Java ट्यूटोरियल
schemas:
- author: Aspose
  dateModified: '2026-08-13'
  description: Learn how to get onenote page modified time and retrieve page revisions
    with Aspose.Note for Java, ideal for auditing and document management.
  headline: Get OneNote page modified time using Aspose.Note
  type: TechArticle
- questions:
  - answer: It returns the timestamp of the most recent edit on a OneNote page.
    question: What does “get last modified time” return?
  - answer: '`PageHistory` via `Document.getPageHistory(Page)`.'
    question: Which class provides revision history?
  - answer: Yes, a valid Aspose.Note license is required for production use.
    question: Do I need a license for this feature?
  - answer: Java 8 or higher (JDK 8+).
    question: What Java version is supported?
  - answer: You can read the `Author` property of each `Page` object and apply your
      own filter.
    question: Can I filter revisions by author?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote page modified
- aspose.note
- java document management
title: Aspose.Note का उपयोग करके OneNote पेज संशोधित समय प्राप्त करें
url: /hi/java/onenote-page-manipulation/get-revisions-of-pages/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note का उपयोग करके OneNote पेज संशोधित समय प्राप्त करें

## परिचय

इस ट्यूटोरियल में आप सीखेंगे कि Aspose.Note for Java के साथ OneNote पेज के **संशोधित** टाइमस्टैम्प कैसे प्राप्त करें और OneNote पेज का पूर्ण संशोधन इतिहास कैसे निकालें। चाहे आप ऑडिट‑ट्रेल फीचर बना रहे हों, चेंज‑लॉग व्यूअर, या डैशबोर्ड में सबसे हालिया संपादन तिथि दिखाने की आवश्यकता हो, यह गाइड आपको हर चरण के माध्यम से ले जाता है—पर्यावरण सेटअप से लेकर सामान्य समस्याओं को संभालने तक।

## त्वरित उत्तर
- **“get last modified time” क्या लौटाता है?** यह OneNote पेज पर सबसे हालिया संपादन का टाइमस्टैम्प लौटाता है।  
- **कौन सा क्लास संशोधन इतिहास प्रदान करता है?** `PageHistory` द्वारा `Document.getPageHistory(Page)`।  
- **क्या इस फीचर के लिए लाइसेंस आवश्यक है?** हाँ, प्रोडक्शन उपयोग के लिए एक वैध Aspose.Note लाइसेंस आवश्यक है।  
- **कौन सा Java संस्करण समर्थित है?** Java 8 या उससे ऊपर (JDK 8+).  
- **क्या मैं लेखक के आधार पर संशोधनों को फ़िल्टर कर सकता हूँ?** आप प्रत्येक `Page` ऑब्जेक्ट की `Author` प्रॉपर्टी पढ़ सकते हैं और अपना फ़िल्टर लागू कर सकते हैं।

## OneNote में “get last modified time” क्या है?

अंतिम संशोधित समय प्रत्येक OneNote पेज पर एक मेटाडाटा एट्रिब्यूट के रूप में संग्रहीत होता है जो सबसे हालिया संपादन के क्षण को दर्शाता है। Aspose.Note इस मान को `Page.getLastModifiedTime()` मेथड के माध्यम से उजागर करता है, जो एक `java.util.Date` ऑब्जेक्ट लौटाता है जिसे आपके एप्लिकेशन की आवश्यकताओं के अनुसार फ़ॉर्मेट या लॉग किया जा सकता है।

## पेज संशोधन क्यों प्राप्त करें?

पेज संशोधनों को प्राप्त करने से आपको OneNote पेज पर किए गए प्रत्येक परिवर्तन का पूर्ण ऑडिट ट्रेल मिलता है, जिससे आप यह ट्रैक कर सकते हैं कि किसने क्या और कब संपादित किया। इस इतिहास का उपयोग संस्करणों की तुलना करने, पिछले स्थितियों को पुनर्स्थापित करने, या टीमों के बीच सहयोग पैटर्न का विश्लेषण करने के लिए किया जा सकता है, जिससे यह अनुपालन और गुणवत्ता नियंत्रण के लिए आवश्यक बन जाता है।

## पूर्वापेक्षाएँ

- **Java Development Kit (JDK) 8 या बाद का** – Oracle वेबसाइट या किसी भी संगत विक्रेता से इंस्टॉल करें।  
- **Aspose.Note for Java लाइब्रेरी** – Aspose.Note Java रिलीज़ पेज से JAR डाउनलोड करें **[Aspose.Note Java releases](https://releases.aspose.com/note/java/)** और इंस्टॉलेशन गाइड **[Aspose.Note Java documentation](https://reference.aspose.com/note/java/)** का पालन करें।  

## पैकेज आयात करें

`Document` क्लास एक OneNote नोटबुक को मेमोरी में लोड करने का प्रतिनिधित्व करता है, जबकि `Page` और `PageHistory` व्यक्तिगत पेजों और उनके संशोधन डेटा तक पहुँच प्रदान करते हैं।

```text
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
import java.util.Date;
```

*(वास्तविक इम्पोर्ट स्टेटमेंट्स को मूल कोड‑ब्लॉक गिनती बनाए रखने के लिए प्लेन टेक्स्ट में दिखाया गया है।)*

## OneNote पेज संशोधित समय कैसे प्राप्त करें?

अंतिम संशोधित टाइमस्टैम्प प्राप्त करने के लिए, पहले OneNote दस्तावेज़ को एक `Document` ऑब्जेक्ट में लोड करें, फिर इच्छित `Page` चुनें। उस पेज पर `getLastModifiedTime()` मेथड को कॉल करें, जो एक `java.util.Date` लौटाता है। आप फिर इस तिथि को `SimpleDateFormat` का उपयोग करके फ़ॉर्मेट कर सकते हैं या टाइम ज़ोन के बीच सुसंगत रिपोर्टिंग के लिए इसे UTC में बदल सकते हैं।

## चरण 1: दस्तावेज़ डायरेक्टरी सेट करें

उस फ़ोल्डर को परिभाषित करें जिसमें आपका OneNote फ़ाइल है।

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## चरण 2: दस्तावेज़ लोड करें

अपने `.one` फ़ाइल के पूर्ण पथ को पास करके एक `Document` इंस्टेंस बनाएं।

```java
String dataDir = "Your Document Directory";
```

## चरण 3: पहला पेज प्राप्त करें

दस्तावेज़ के पेज संग्रह से पहला `Page` ऑब्जेक्ट प्राप्त करें।

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## चरण 4: पेज संशोधन प्राप्त करें

चयनित पेज के लिए `PageHistory` प्राप्त करें। यदि नोटबुक कभी संपादित नहीं हुई है, तो यह कॉल `null` लौटा सकती है।

```java
Page firstPage = doc.getFirstChild();
```

## चरण 5: पेज संशोधनों को पार करें

प्रत्येक `Page` संशोधन पर इटररेट करें, उसका `Author` और `LastModifiedTime` पढ़ें, और जानकारी प्रदर्शित करें।

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## सामान्य समस्याएँ और समाधान

- **Null `PageHistory`** – सत्यापित करें कि नोटबुक में वास्तव में संशोधन हैं; अन्यथा `getPageHistory` `null` लौटाता है।  
- **Time‑zone अंतर** – `getLastModifiedTime()` JVM की डिफ़ॉल्ट टाइम ज़ोन का उपयोग करता है। यदि आपके एप्लिकेशन को मानक ज़ोन चाहिए तो `SimpleDateFormat` के साथ UTC में बदलें।  
- **License लोड नहीं हुआ** – वैध लाइसेंस के बिना Aspose.Note मूल्यांकन मोड में चलता है, जो पेज प्रोसेसिंग को सीमित करता है। इस प्रतिबंध से बचने के लिए एप्लिकेशन स्टार्ट‑अप पर अपना लाइसेंस फ़ाइल लोड करें।

## अक्सर पूछे जाने वाले प्रश्न

**Q1: क्या मैं Aspose.Note for Java का उपयोग करके नए OneNote दस्तावेज़ बना सकता हूँ?**  
A: हाँ, API आपको प्रोग्रामेटिक रूप से शून्य से OneNote नोटबुक बनाना, संपादित करना और सहेजना देता है।

**Q2: क्या Aspose.Note for Java विभिन्न OneNote फ़ाइल संस्करणों के साथ संगत है?**  
A: हाँ, यह OneNote 2007‑2021 फ़ाइल फ़ॉर्मेट्स का समर्थन करता है, जिससे डेस्कटॉप और क्लाउड वातावरण में व्यापक संगतता सुनिश्चित होती है।

**Q3: क्या मैं OneNote दस्तावेज़ निर्यात करते समय आउटपुट फ़ॉर्मेट को कस्टमाइज़ कर सकता हूँ?**  
A: बिल्कुल। आप PDF, HTML, PNG, या SVG में निर्यात कर सकते हैं, और इमेज रेज़ोल्यूशन और फ़ॉन्ट एम्बेडिंग जैसी विकल्पों को नियंत्रित कर सकते हैं।

**Q4: क्या Aspose.Note for Java को व्यावसायिक उपयोग के लिए लाइसेंस की आवश्यकता है?**  
A: हाँ, प्रोडक्शन डिप्लॉयमेंट्स के लिए एक व्यावसायिक लाइसेंस अनिवार्य है। मूल्यांकन के लिए एक फ्री ट्रायल उपलब्ध है।

**Q5: यदि मुझे समस्याएँ आती हैं तो मैं सहायता कहाँ प्राप्त कर सकता हूँ?**  
A: Aspose.Note कम्युनिटी फ़ोरम **[Aspose.Note forum](https://forum.aspose.com/c/note/28)** पर जाएँ, जहाँ आप प्रश्न पूछ सकते हैं, अनुभव साझा कर सकते हैं, और समुदाय तथा Aspose इंजीनियर्स से मदद प्राप्त कर सकते हैं।

**अंतिम अपडेट:** 2026-08-13  
**परीक्षित संस्करण:** Aspose.Note for Java 23.12 (latest at time of writing)  
**लेखक:** Aspose

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

## संबंधित ट्यूटोरियल

- [Aspose Java ट्यूटोरियल - OneNote में पेजों के बारे में जानकारी प्राप्त करें - Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)
- [aspose.note पेज रिवीजन ट्यूटोरियल – OneNote में पेज रिवीजन प्राप्त करें](/note/java/onenote-page-manipulation/get-page-revisions/)
- [track changes onenote – Aspose.Note के साथ पेज रिवीजन प्रबंधित करें](/note/java/onenote-page-manipulation/working-with-page-revisions/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}