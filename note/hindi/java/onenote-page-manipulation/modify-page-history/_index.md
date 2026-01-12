---
date: 2026-01-12
description: Aspose.Note for Java का उपयोग करके OneNote पेज इतिहास को संशोधित करना,
  OneNote पेज शीर्षक बदलना, और पेज इतिहास को हटाना सीखें।
linktitle: Modify Page History in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Aspose.Note के साथ OneNote पेज इतिहास को कैसे संशोधित करें
url: /hi/java/onenote-page-manipulation/modify-page-history/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note के साथ OneNote पेज इतिहास को कैसे संशोधित करें

इस ट्यूटोरियल में आप **OneNote** दस्तावेज़ों को प्रोग्रामेटिक रूप से पेज इतिहास के साथ काम करके कैसे संशोधित किया जाए, यह जानेंगे। हम OneNote फ़ाइल को लोड करने, उसके इतिहास प्रविष्टियों को संपादित करने, पेज शीर्षक बदलने, और अंत में अपडेटेड नोटबुक को सहेजने की प्रक्रिया को Aspose.Note for Java API का उपयोग करके दिखाएंगे। चाहे आपको पुराने संशोधनों को साफ़ करना हो या पेजों का नाम बदलना हो, नीचे दिए गए चरण एक पूर्ण, प्रोडक्शन‑रेडी समाधान प्रदान करते हैं।

## त्वरित उत्तर
- **OneNote में “पेज इतिहास” का क्या अर्थ है?**  
  यह OneNote फ़ाइल के भीतर संग्रहीत पिछले पेज संस्करणों का संग्रह है।  
- **क्या मैं किसी विशिष्ट इतिहास प्रविष्टि को हटा सकता हूँ?**  
  हाँ, `PageHistory` ऑब्जेक्ट पर `removeRange` या `removeItem` मेथड का उपयोग करें।  
- **क्या पेज शीर्षक बदलना इतिहास संशोधन का हिस्सा है?**  
  बिल्कुल—प्रत्येक इतिहास आइटम का अपना शीर्षक होता है जिसे आप संशोधित कर सकते हैं।  
- **क्या इस कोड को चलाने के लिए लाइसेंस चाहिए?**  
  परीक्षण के लिए एक अस्थायी मूल्यांकन लाइसेंस काम करता है; प्रोडक्शन के लिए पूर्ण लाइसेंस आवश्यक है।  
- **कौन सा Java संस्करण समर्थित है?**  
  Aspose.Note for Java JDK 8 और उसके बाद के संस्करणों को समर्थन देता है।

## पूर्वापेक्षाएँ

शुरू करने से पहले सुनिश्चित करें कि आपके पास निम्नलिखित हों:

1. **Java Development Kit (JDK)** – आपके मशीन पर JDK 8 या नया स्थापित हो।  
2. **Aspose.Note for Java लाइब्रेरी** – इसे [डाउनलोड पेज](https://releases.aspose.com/note/java/) से डाउनलोड करें।  
3. **एक नमूना OneNote दस्तावेज़** – उदाहरण के लिए, `Sample1.one` जिसे आप सुरक्षित रूप से संशोधित कर सकते हैं।

## पैकेज आयात करें

सबसे पहले, उन क्लासों को आयात करें जिनकी आपको आवश्यकता होगी। नीचे दिया गया कोड ब्लॉक बिल्कुल जैसा है वैसा ही रखें।

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## चरण‑दर‑चरण मार्गदर्शिका

### चरण 1: OneNote दस्तावेज़ लोड करें

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
```

### चरण 2: पहला पेज और उसका इतिहास प्राप्त करें

```java
Page page = document.getFirstChild();
PageHistory pageHistory = document.getPageHistory(page);
```

### चरण 3: इतिहास आइटम की एक रेंज हटाएँ

यदि आपको **OneNote पेज इतिहास** प्रविष्टियों को हटाना है, तो `removeRange` को कॉल करें। उदाहरण पहले प्रविष्टि को हटाता है।

```java
pageHistory.removeRange(0, 1);
```

### चरण 4: एक इतिहास आइटम को बदलें

आप मौजूदा इतिहास प्रविष्टि को एक नई `Page` ऑब्जेक्ट से बदल सकते हैं।

```java
pageHistory.set_Item(0, new Page());
```

### चरण 5: इतिहास पेज का शीर्षक बदलें

विशिष्ट संशोधन के लिए **OneNote पेज शीर्षक बदलना** आम अनुरोध है।

```java
pageHistory.get_Item(1).getTitle().getTitleText().clear().append("New Title");
```

### चरण 6: नया इतिहास प्रविष्टि जोड़ें

इतिहास संग्रह में एक नई पेज जोड़ें।

```java
pageHistory.addItem(new Page());
```

### चरण 7: विशिष्ट स्थिति पर पेज डालें

इंडेक्स 1 पर पेज डालें, जिससे मौजूदा आइटम आगे बढ़ जाएँ।

```java
pageHistory.insertItem(1, new Page());
```

### चरण 8: संशोधित नोटबुक सहेजें

```java
document.save(dataDir + "ModifyPageHistory_out.one");
```

## OneNote पेज इतिहास को संशोधित क्यों करें?

- **संस्करण नियंत्रण:** केवल प्रासंगिक संशोधन रखें और अनावश्यक ड्राफ्ट हटाएँ।  
- **संगति:** सभी ऐतिहासिक संस्करणों में पेज शीर्षकों को समान बनाकर बेहतर नेविगेशन प्राप्त करें।  
- **प्रदर्शन:** छोटा इतिहास संग्रह फ़ाइल आकार घटाता है और लोडिंग गति बढ़ाता है।

## सामान्य गलतियाँ और सुझाव

- **इंडेक्स सीमा से बाहर:** `removeRange` या `insertItem` कॉल करने से पहले हमेशा संग्रह का आकार जाँचें।  
- **नल शीर्षक:** कुछ ऐतिहासिक पेजों में शीर्षक नहीं हो सकता; `getTitle()` कॉल करते समय `null` की जाँच करें।  
- **सहेजने का स्थान:** आउटपुट पथ (`ModifyPageHistory_out.one`) लिखने योग्य हो, अन्यथा `IOException` फेंका जाएगा।

## अक्सर पूछे जाने वाले प्रश्न

**प्र: क्या मैं Aspose.Note for Java को अन्य Java फ्रेमवर्क के साथ उपयोग कर सकता हूँ?**  
उ: हाँ, Aspose.Note for Java Spring, Hibernate आदि जैसे विभिन्न Java फ्रेमवर्क के साथ संगत है।

**प्र: क्या Aspose.Note for Java विभिन्न OneNote फ़ाइल संस्करणों के साथ काम करता है?**  
उ: Aspose.Note for Java पुराने और नए दोनों OneNote फ़ाइल संस्करणों के साथ काम करने का समर्थन करता है।

**प्र: क्या Aspose.Note for Java को अतिरिक्त निर्भरताओं की आवश्यकता है?**  
उ: नहीं, Aspose.Note for Java एक स्टैंडअलोन लाइब्रेरी है और अतिरिक्त निर्भरताएँ नहीं मांगती।

**प्र: क्या मैं कई OneNote फ़ाइलों पर एक साथ बड़े पैमाने पर संशोधन कर सकता हूँ?**  
उ: हाँ, Aspose.Note for Java बड़े पैमाने पर संशोधनों को कुशलता से संभालने के लिए API प्रदान करता है।

**प्र: क्या Aspose.Note for Java के लिए कोई समुदाय फ़ोरम है जहाँ मैं मदद मांग सकूँ?**  
उ: हाँ, आप [Aspose.Note फ़ोरम](https://forum.aspose.com/c/note/28) पर लाइब्रेरी से संबंधित किसी भी सहायता या प्रश्न के लिए जा सकते हैं।

---

**अंतिम अपडेट:** 2026-01-12  
**परीक्षित संस्करण:** Aspose.Note for Java 24.11 (लेखन के समय नवीनतम)  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}