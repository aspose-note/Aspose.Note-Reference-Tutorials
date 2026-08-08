---
date: 2026-08-08
description: Aspose.Note for Java का उपयोग करके प्रोग्रामेटिकली पेज रिवीजन प्राप्त
  करके OneNote में बदलावों को ट्रैक करना सीखें।
keywords:
- track changes in onenote
- aspose.note java
- onenote page revisions
- java document processing
lastmod: 2026-08-08
linktitle: OneNote में पेज रिवीजन प्राप्त करें - Aspose.Note
og_description: Aspose.Note for Java का उपयोग करके प्रोग्रामेटिकली पेज रिवीजन प्राप्त
  करके OneNote में बदलावों को ट्रैक करना सीखें।
og_image_alt: Guide showing how to track changes in OneNote using Aspose.Note Java
  API
og_title: OneNote में बदलावों को ट्रैक करें – Aspose.Note के साथ पेज रिवीजन
schemas:
- author: Aspose
  dateModified: '2026-08-08'
  description: Learn how to track changes in OneNote by retrieving page revisions
    programmatically using Aspose.Note for Java.
  headline: Track changes in OneNote – page revisions with Aspose.Note
  type: TechArticle
- description: Learn how to track changes in OneNote by retrieving page revisions
    programmatically using Aspose.Note for Java.
  name: Track changes in OneNote – page revisions with Aspose.Note
  steps:
  - name: set up document directory
    text: Define the folder where your OneNote file resides.
  - name: load OneNote document with history enabled
    text: '`LoadOptions` is a configuration class that tells Aspose.Note how to open
      a file, including whether to read revision data. Enable the flag before loading
      the document.'
  - name: get the first page
    text: Grab the first page object; this will be the reference point for retrieving
      its history.
  - name: iterate through page revisions
    text: Loop through each revision and print useful metadata such as timestamps,
      title, level, and author. > **Pro tip:** If you need to filter revisions by
      a specific author or date range, simply add conditional checks inside the `for`
      loop.
  type: HowTo
- questions:
  - answer: Retrieving page revision history from a OneNote file using Aspose.Note
      for Java.
    question: What does the tutorial cover?
  - answer: Any recent Aspose.Note for Java release that supports `LoadOptions.setLoadHistory`.
    question: Which library version is required?
  - answer: A temporary evaluation license works for testing; a commercial license
      is required for production.
    question: Do I need a license?
  - answer: The API is read‑only for revisions; you can only retrieve them.
    question: Can I modify revisions?
  - answer: Java JDK, Aspose.Note for Java, and a OneNote document with revision data.
    question: What are the main prerequisites?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- track changes
- Aspose.Note
- OneNote revisions
- Java API
title: OneNote में बदलावों को ट्रैक करें – Aspose.Note के साथ पेज रिवीजन
url: /hi/java/onenote-page-manipulation/get-page-revisions/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote में बदलाव ट्रैक करें – Aspose.Note के साथ पृष्ठ संशोधन

इस ट्यूटोरियल में आप सीखेंगे कि **OneNote में बदलाव ट्रैक** कैसे करें, Aspose.Note Java API का उपयोग करके पृष्ठ का पूरा संशोधन इतिहास निकालकर। हम विकास पर्यावरण सेटअप करने से लेकर प्रत्येक संशोधन के लेखक, टाइमस्टैम्प और शीर्षक को प्रिंट करने तक सब कुछ कवर करेंगे, ताकि आप किसी भी OneNote-आधारित समाधान के लिए विश्वसनीय ऑडिट‑ट्रेल फीचर बना सकें।

## त्वरित उत्तर
- **ट्यूटोरियल क्या कवर करता है?** Aspose.Note for Java का उपयोग करके OneNote फ़ाइल से पृष्ठ संशोधन इतिहास प्राप्त करना।  
- **कौन सा लाइब्रेरी संस्करण आवश्यक है?** `LoadOptions.setLoadHistory` को सपोर्ट करने वाला कोई भी नवीनतम Aspose.Note for Java रिलीज़।  
- **क्या मुझे लाइसेंस चाहिए?** टेस्टिंग के लिए एक अस्थायी इवैल्यूएशन लाइसेंस काम करता है; उत्पादन के लिए एक व्यावसायिक लाइसेंस आवश्यक है।  
- **क्या मैं संशोधनों को संशोधित कर सकता हूँ?** API संशोधनों के लिए केवल पढ़ने योग्य है; आप केवल उन्हें प्राप्त कर सकते हैं।  
- **मुख्य पूर्वापेक्षाएँ क्या हैं?** Java JDK, Aspose.Note for Java, और संशोधन डेटा वाला OneNote दस्तावेज़।

## “aspose.note पृष्ठ संशोधन ट्यूटोरियल” क्या है?
यह ट्यूटोरियल दिखाता है कि कैसे प्रोग्रामेटिक रूप से OneNote पृष्ठ के ऐतिहासिक संस्करणों तक पहुंचा जाए। प्रत्येक संशोधन में लेखक, निर्माण समय, और संशोधन समय जैसी मेटाडेटा शामिल होती है, जिससे आप अपने अनुप्रयोगों में ऑडिट ट्रेल या परिवर्तन‑लॉग फीचर बना सकते हैं।

## पृष्ठ संशोधन ट्रैकिंग के लिए Aspose.Note का उपयोग क्यों करें?
एक मानक 2 GHz CPU पर 500‑पृष्ठ फ़ाइल के लिए नोटबुक का पूरा संशोधन इतिहास 5 सेकंड से कम समय में लोड करें, और OneNote UI लॉन्च किए बिना मेटाडेटा प्राप्त करें। लाइब्रेरी 30+ इनपुट और आउटपुट फ़ॉर्मैट्स को सपोर्ट करती है, Windows, Linux, और macOS पर चलती है ( >95 % सर्वर पर्यावरण को कवर करती है), और प्रत्येक संशोधन प्रॉपर्टी पर पूर्ण नियंत्रण प्रदान करती है।

## पूर्वापेक्षाएँ

### 1. Java Development Kit (JDK)
सुनिश्चित करें कि एक नवीनतम JDK (8 या उससे ऊपर) स्थापित है और `JAVA_HOME` सेट है।

### 2. Aspose.Note for Java
लाइब्रेरी को [download link](https://releases.aspose.com/note/java/) से डाउनलोड करें।

### 3. नमूना OneNote दस्तावेज़
एक OneNote फ़ाइल बनाएं या प्राप्त करें (जैसे, `Sample1.one`) जिसमें पृष्ठों के साथ संशोधन इतिहास हो।

## पैकेज आयात करें
पहले, आवश्यक Aspose.Note क्लासेस को आयात करें।  
`Document` एक OneNote नोटबुक को दर्शाता है, `LoadOptions` लोडिंग व्यवहार को कॉन्फ़िगर करता है, और `Page` एक एकल पृष्ठ को दर्शाता है।

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## चरण‑दर‑चरण कार्यान्वयन

### चरण 1: दस्तावेज़ डायरेक्टरी सेट करें
उस फ़ोल्डर को परिभाषित करें जहाँ आपका OneNote फ़ाइल स्थित है।

```java
String dataDir = "Your Document Directory";
```

### चरण 2: इतिहास सक्षम के साथ OneNote दस्तावेज़ लोड करें
`LoadOptions` एक कॉन्फ़िगरेशन क्लास है जो Aspose.Note को बताती है कि फ़ाइल कैसे खोलें, जिसमें संशोधन डेटा पढ़ना शामिल है या नहीं। दस्तावेज़ लोड करने से पहले इस फ़्लैग को सक्षम करें।

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

### चरण 3: पहला पृष्ठ प्राप्त करें
पहले पृष्ठ ऑब्जेक्ट को प्राप्त करें; यह उसके इतिहास को प्राप्त करने के लिए संदर्भ बिंदु होगा।

```java
Page firstPage = document.getFirstChild();
```

### चरण 4: पृष्ठ संशोधनों के माध्यम से इटरेट करें
प्रत्येक संशोधन के माध्यम से लूप करें और टाइमस्टैम्प, शीर्षक, स्तर, और लेखक जैसी उपयोगी मेटाडेटा प्रिंट करें।

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

> **प्रो टिप:** यदि आपको किसी विशिष्ट लेखक या तिथि सीमा द्वारा संशोधनों को फ़िल्टर करने की आवश्यकता है, तो बस `for` लूप के अंदर शर्तीय जांच जोड़ें।

## सामान्य समस्याएँ एवं समाधान
- **कोई संशोधन नहीं मिला:** `loadOptions.setLoadHistory(true)` को दस्तावेज़ लोड करने से पहले कॉल किया गया है, यह सत्यापित करें।  
- **लेखक या शीर्षक null:** कुछ पुराने OneNote संस्करण इन फ़ील्ड्स को संग्रहीत नहीं कर सकते; `null` मानों को सहजता से संभालें।  
- **बड़े नोटबुक्स पर प्रदर्शन में देरी:** केवल आवश्यक सेक्शन लोड करें या JVM हीप साइज बढ़ाएँ।

## अक्सर पूछे जाने वाले प्रश्न

**Q1: क्या मैं Aspose.Note for Java का उपयोग करके पृष्ठ संशोधनों को संशोधित कर सकता हूँ?**  
A1: नहीं, API वर्तमान में केवल पृष्ठ संशोधनों के लिए पढ़ने‑के‑लिए‑ही पहुँच समर्थन करता है।

**Q2: क्या Aspose.Note for Java विभिन्न OneNote दस्तावेज़ संस्करणों के साथ संगत है?**  
A2: हाँ, यह विभिन्न OneNote फ़ाइल फ़ॉर्मैट्स के साथ काम करता है, जिससे संस्करणों के बीच सहज प्रोसेसिंग संभव होती है।

**Q3: क्या Aspose.Note for Java को उपयोग करने के लिए लाइसेंस चाहिए?**  
A3: उत्पादन उपयोग के लिए एक व्यावसायिक लाइसेंस आवश्यक है, लेकिन परीक्षण के लिए एक अस्थायी इवैल्यूएशन लाइसेंस उपलब्ध है।

**Q4: क्या मैं Aspose.Note for Java का उपयोग करते समय किसी भी समस्या का सामना करने पर समर्थन प्राप्त कर सकता हूँ?**  
A4: हाँ, आप Aspose.Note फ़ोरम पर प्रश्न पूछ सकते हैं [Aspose.Note forum](https://forum.aspose.com/c/note/28)।

**Q5: क्या Aspose.Note for Java के लिए कोई मुफ्त ट्रायल उपलब्ध है?**  
A5: हाँ, आप [website](https://releases.aspose.com/) से मुफ्त ट्रायल डाउनलोड कर सकते हैं।

---

**अंतिम अपडेट:** 2026-08-08  
**परीक्षित संस्करण:** Aspose.Note for Java (latest release)  
**लेखक:** Aspose  

{{< blocks/products/products-backtop-button >}}

## संबंधित ट्यूटोरियल

- [OneNote में बदलाव ट्रैक करें – Aspose.Note के साथ पृष्ठ संशोधन प्रबंधित करें](/note/java/onenote-page-manipulation/working-with-page-revisions/)
- [Aspose Java ट्यूटोरियल - OneNote में पृष्ठों की जानकारी प्राप्त करें - Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)
- [OneNote पृष्ठ पृष्ठभूमि बदलें – Aspose.Note for Java](/note/java/onenote-page-manipulation/set-page-background-color/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}