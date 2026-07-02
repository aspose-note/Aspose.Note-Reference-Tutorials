---
date: 2026-01-10
description: जावा के लिए Aspose.Note पेज रिवीजन ट्यूटोरियल सीखें – Aspose.Note का
  उपयोग करके OneNote पेज रिवीजन को प्रोग्रामेटिकली प्राप्त करें। हमारी चरण‑दर‑चरण
  गाइड का पालन करें।
linktitle: Get Page Revisions in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: aspose.note पेज संशोधन ट्यूटोरियल – OneNote में पेज संशोधन प्राप्त करें
url: /hi/java/onenote-page-manipulation/get-page-revisions/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote में पेज रिवीजन प्राप्त करें - Aspose.Note

OneNote एक शक्तिशाली नोट‑लेने वाला प्लेटफ़ॉर्म है, और जब आपको बदलावों का ऑडिट करना हो, तो **aspose.note page revisions tutorial** आपको ठीक‑ठीक दिखाता है कि कैसे कुछ ही Java कोड लाइनों से रिवीजन इतिहास प्राप्त किया जाए। इस गाइड में हम सब कुछ कवर करेंगे—पर्यावरण सेटअप से लेकर प्रत्येक रिवीजन के विवरण प्रिंट करने तक—ताकि आप आसानी से संपादन, लेखक योगदान, और टाइमस्टैम्प ट्रैक कर सकें।

## त्वरित उत्तर
- **ट्यूटोरियल क्या कवर करता है?** Aspose.Note for Java का उपयोग करके OneNote फ़ाइल से पेज रिवीजन इतिहास प्राप्त करना।  
- **कौन सा लाइब्रेरी संस्करण आवश्यक है?** कोई भी हालिया Aspose.Note for Java रिलीज़ जो `LoadOptions.setLoadHistory` को सपोर्ट करता हो।  
- **क्या मुझे लाइसेंस चाहिए?** टेस्टिंग के लिए एक अस्थायी इवैल्यूएशन लाइसेंस काम करता है; प्रोडक्शन के लिए एक कमर्शियल लाइसेंस आवश्यक है।  
- **क्या मैं रिवीजन को संशोधित कर सकता हूँ?** API रिवीजन के लिए केवल रीड‑ओनली है; आप केवल उन्हें प्राप्त कर सकते हैं।  
- **मुख्य पूर्वापेक्षाएँ क्या हैं?** Java JDK, Aspose.Note for Java, और रिवीजन डेटा वाला OneNote दस्तावेज़।

## “aspose.note page revisions tutorial” क्या है?
यह ट्यूटोरियल दिखाता है कि कैसे प्रोग्रामेटिक रूप से OneNote पेज के ऐतिहासिक संस्करणों तक पहुंचा जाए। प्रत्येक रिवीजन में लेखक, निर्माण समय, और संशोधन समय जैसी मेटाडेटा शामिल होती है, जिससे आप अपने एप्लिकेशन में ऑडिट ट्रेल या चेंज‑लॉग फीचर बना सकते हैं।

## पेज रिवीजन ट्रैकिंग के लिए Aspose.Note का उपयोग क्यों करें?
- **UI निर्भरता नहीं** – पूरी तरह कोड में काम करता है, बैकएंड सर्विसेज़ के लिए उपयुक्त।  
- **क्रॉस‑प्लेटफ़ॉर्म** – Java Windows, Linux, और macOS पर चलता है।  
- **पूर्ण नियंत्रण** – OneNote को मैन्युअली खोले बिना प्रत्येक रिवीजन प्रॉपर्टी प्राप्त करें।  
- **परफॉर्मेंस** – इतिहास लोड करना ऑप्टिमाइज़्ड है, इसलिए बड़े नोटबुक भी जल्दी प्रोसेस होते हैं।

## पूर्वापेक्षाएँ

### 1. Java Development Kit (JDK)
सुनिश्चित करें कि एक हालिया JDK (8 या उससे ऊपर) स्थापित है और `JAVA_HOME` सेट है।

### 2. Aspose.Note for Java
लाइब्रेरी को [download link](https://releases.aspose.com/note/java/) से डाउनलोड करें।

### 3. Sample OneNote Document
एक OneNote फ़ाइल बनाएं या प्राप्त करें (उदा., `Sample1.one`) जिसमें रिवीजन इतिहास वाली पेज हों।

## पैकेज इम्पोर्ट करें
सबसे पहले, आवश्यक Aspose.Note क्लासेस को इम्पोर्ट करें।

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## स्टेप‑बाय‑स्टेप इम्प्लीमेंटेशन

### स्टेप 1: डॉक्यूमेंट डायरेक्टरी सेट करें
उस फ़ोल्डर को परिभाषित करें जहाँ आपका OneNote फ़ाइल स्थित है।

```java
String dataDir = "Your Document Directory";
```

### स्टेप 2: इतिहास सक्षम करके OneNote डॉक्यूमेंट लोड करें
`LoadOptions` फ्लैग को सक्षम करें ताकि रिवीजन डेटा प्राप्त किया जा सके।

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

### स्टेप 3: पहली पेज प्राप्त करें
पहले पेज ऑब्जेक्ट को प्राप्त करें; यह उसके इतिहास को प्राप्त करने के लिए रेफ़रेंस पॉइंट होगा।

```java
Page firstPage = document.getFirstChild();
```

### स्टेप 4: पेज रिवीजन पर इटररेट करें
प्रत्येक रिवीजन पर लूप करें और टाइमस्टैम्प, शीर्षक, स्तर, और लेखक जैसी उपयोगी मेटाडेटा प्रिंट करें।

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

> **Pro tip:** यदि आपको किसी विशिष्ट लेखक या तिथि सीमा द्वारा रिवीजन फ़िल्टर करने की आवश्यकता है, तो बस `for` लूप के अंदर कंडीशनल चेक जोड़ें।

## सामान्य समस्याएँ और समाधान
- **कोई रिवीजन नहीं मिला:** सुनिश्चित करें कि डॉक्यूमेंट लोड करने से पहले `loadOptions.setLoadHistory(true)` कॉल किया गया है।  
- **नल लेखक या शीर्षक:** कुछ पुराने OneNote संस्करण इन फ़ील्ड्स को स्टोर नहीं कर सकते; `null` वैल्यू को सावधानीपूर्वक हैंडल करें।  
- **बड़े नोटबुक पर परफॉर्मेंस लैग:** केवल आवश्यक सेक्शन लोड करें या JVM हीप साइज बढ़ाएँ।

## अक्सर पूछे जाने वाले प्रश्न

**Q1: क्या मैं Aspose.Note for Java का उपयोग करके पेज रिवीजन को संशोधित कर सकता हूँ?**  
A1: नहीं, API वर्तमान में केवल पेज रिवीजन के रीड‑ओनली एक्सेस को सपोर्ट करता है।

**Q2: क्या Aspose.Note for Java विभिन्न OneNote दस्तावेज़ संस्करणों के साथ संगत है?**  
A2: हाँ, यह विभिन्न OneNote फ़ाइल फ़ॉर्मैट्स के साथ काम करता है, जिससे संस्करणों के बीच सहज प्रोसेसिंग संभव होती है।

**Q3: क्या Aspose.Note for Java के उपयोग के लिए लाइसेंस आवश्यक है?**  
A3: प्रोडक्शन उपयोग के लिए एक कमर्शियल लाइसेंस आवश्यक है, लेकिन टेस्टिंग के लिए एक अस्थायी इवैल्यूएशन लाइसेंस उपलब्ध है।

**Q4: क्या मैं Aspose.Note for Java उपयोग करते समय किसी भी समस्या का सामना करने पर सपोर्ट ले सकता हूँ?**  
A4: हाँ, आप Aspose.Note फ़ोरम पर प्रश्न पूछ सकते हैं [here](https://forum.aspose.com/c/note/28)।

**Q5: क्या Aspose.Note for Java के लिए कोई फ्री ट्रायल उपलब्ध है?**  
A5: हाँ, आप फ्री ट्रायल को [website](https://releases.aspose.com/) से डाउनलोड कर सकते हैं।

---

**अंतिम अपडेट:** 2026-01-10  
**परीक्षण किया गया:** Aspose.Note for Java (latest release)  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}