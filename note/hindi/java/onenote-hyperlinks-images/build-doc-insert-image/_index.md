---
date: 2026-03-19
description: जानेँ कि Aspose.Note for Java का उपयोग करके OneNote में चित्र कैसे जोड़ें।
  यह चरण‑दर‑चरण गाइड दिखाता है कि OneNote दस्तावेज़ कैसे बनाएं, OneNote में चित्र
  डालें, और OneNote को PDF के रूप में सहेजें।
linktitle: How to add picture to OneNote using Java – Build Document and Insert Image
second_title: Aspose.Note Java API
title: जावा का उपयोग करके वननोट में चित्र कैसे जोड़ें – दस्तावेज़ बनाएं और छवि सम्मिलित
  करें
url: /hi/java/onenote-hyperlinks-images/build-doc-insert-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java का उपयोग करके OneNote में चित्र कैसे जोड़ें – दस्तावेज़ बनाएं और छवि सम्मिलित करें

## परिचय

इस ट्यूटोरियल में, आप **OneNote में चित्र कैसे जोड़ें** सीखेंगे Aspose.Note Java API का उपयोग करके। हम एक नई OneNote दस्तावेज़ बनाएँगे, उसमें एक छवि सम्मिलित करेंगे, और परिणाम को PDF के रूप में सहेजेंगे। चाहे आप रिपोर्टिंग टूल बना रहे हों, नोट‑लेखन को स्वचालित कर रहे हों, या प्रोग्रामेटिक रूप से ग्राफ़िक्स एम्बेड करना चाहते हों, यह गाइड आपको स्पष्ट, व्यावहारिक मार्ग प्रदान करता है।

## त्वरित उत्तर
- **मुझे कौन सा लाइब्रेरी चाहिए?** Aspose.Note for Java.  
- **क्या मैं कोई भी इमेज फ़ॉर्मेट सम्मिलित कर सकता हूँ?** JPEG, PNG, BMP, GIF और अधिक समर्थित हैं।  
- **कौन‑से आउटपुट फ़ॉर्मेट उपलब्ध हैं?** आप OneNote, PDF, XPS, HTML आदि के रूप में सहेज सकते हैं।  
- **क्या उत्पादन के लिए लाइसेंस चाहिए?** हाँ, गैर‑ट्रायल उपयोग के लिए एक व्यावसायिक लाइसेंस आवश्यक है।  
- **क्या कोड क्रॉस‑प्लेटफ़ॉर्म है?** बिल्कुल – Java Windows, Linux और macOS पर चलता है।

## Java का उपयोग करके OneNote में चित्र कैसे जोड़ें

OneNote में चित्र जोड़ना मतलब प्रोग्रामेटिक रूप से एक इमेज फ़ाइल को OneNote पेज में एम्बेड करना है ताकि वह टेक्स्ट, आउटलाइन या अन्य तत्वों के साथ दिखाई दे। Aspose.Note API OneNote फ़ाइल फ़ॉर्मेट को एब्स्ट्रैक्ट करता है, जिससे आप सामग्री पर ध्यान केंद्रित कर सकते हैं न कि अंतर्निहित XML संरचना पर।

### OneNote में इमेज एम्बेड क्यों करें?

- **ऑटोमेशन:** स्क्रीनशॉट के साथ मीटिंग मिनट्स स्वचालित रूप से जनरेट करें।  
- **संगति:** सुनिश्चित करें कि हर पेज समान लेआउट और ब्रांडिंग का पालन करे।  
- **इंटीग्रेशन:** अन्य सिस्टम (जैसे चार्ट) से डेटा को सीधे OneNote नोटबुक में जोड़ें।  
- **क्रॉस‑प्लेटफ़ॉर्म:** Java आपको कोड को किसी भी सर्वर या डेस्कटॉप वातावरण में चलाने की सुविधा देता है।

## पूर्वापेक्षाएँ

शुरू करने से पहले सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

1. **Java Development Kit (JDK)** – कोई भी हालिया संस्करण (8 या बाद का)।  
2. **Aspose.Note for Java लाइब्रेरी** – इसे [वेबसाइट](https://releases.aspose.com/note/java/) से डाउनलोड करें।  
3. **IDE** – IntelliJ IDEA, Eclipse, या कोई भी Java‑संगत एडिटर जो आप पसंद करते हैं।  

## पैकेज आयात करें

अपने Java स्रोत फ़ाइल में आवश्यक क्लासेज़ को आयात करके शुरू करें:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## चरण‑दर‑चरण गाइड

### चरण 1: दस्तावेज़ सेट अप करें

एक नई OneNote दस्तावेज़ और एक पेज कंटेनर बनाएं जहाँ सामग्री रहेगी।

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

### चरण 2: आउटलाइन को प्रारंभ करें

एक *आउटलाइन* टेक्स्ट और इमेज जैसे तत्वों के कंटेनर की तरह काम करता है। हम इसके ऑफ़सेट को शून्य सेट करते हैं ताकि सामग्री शीर्ष‑बाएँ कोने से शुरू हो।

```java
Outline outline = new Outline();
outline.setVerticalOffset(0);
outline.setHorizontalOffset(0);
```

### चरण 3: इमेज लोड करें और संरेखित करें

जिस चित्र को आप एम्बेड करना चाहते हैं उसे लोड करें और पेज के दाएँ पक्ष पर संरेखित करें। यही वह जगह है जहाँ हम वास्तव में **OneNote में चित्र जोड़ते** हैं। `Image` कंस्ट्रक्टर दिखाता है कि **इमेज फ़ाइल java** को कोड‑स्तर पर कैसे लोड किया जाता है।

```java
Image image = new Image(null, dataDir + "Input.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

### चरण 4: इमेज को आउटलाइन एलिमेंट से जोड़ें

इमेज को `OutlineElement` के अंदर रैप करें। यह चरण विज़ुअल ऑब्जेक्ट को दस्तावेज़ की आउटलाइन पदानुक्रम से जोड़ता है और प्रभावी रूप से **OneNote में इमेज सम्मिलित** करता है।

```java
OutlineElement outlineElem = new OutlineElement();
outlineElem.appendChildLast(image);
```

### चरण 5: दस्तावेज़ संरचना को संयोजित करें

आउटलाइन एलिमेंट को आउटलाइन में जोड़ें, फिर आउटलाइन को पेज से संलग्न करें, और अंत में पेज को दस्तावेज़ में जोड़ें।

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

### चरण 6: OneNote दस्तावेज़ सहेजें

दस्तावेज़ को डिस्क पर स्थायी रूप से लिखें। इस उदाहरण में हम PDF में एक्सपोर्ट करते हैं, जो दर्शाता है कि **OneNote को PDF के रूप में सहेजें** या **OneNote को PDF में बदलें** कैसे किया जाता है। आप `SaveFormat` बदलकर मूल OneNote फ़ाइल (`.one`) के रूप में भी सहेज सकते हैं।

```java
try {
    doc.save(dataDir + "NewOneNotedocument_out", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## सामान्य समस्याएँ और समाधान

| समस्या | क्यों होती है | समाधान |
|-------|----------------|-----|
| **इमेज नहीं दिख रही** | फ़ाइल पाथ गलत है या फ़ॉर्मेट असमर्थित है। | सुनिश्चित करें `dataDir` सही फ़ोल्डर की ओर इशारा कर रहा है और समर्थित इमेज टाइप (JPEG, PNG आदि) उपयोग करें। |
| **डॉक्यूमेंट खाली PDF के रूप में सहेजा गया** | आउटलाइन ऑफ़सेट गलत सेट है। | `setVerticalOffset(0)` और `setHorizontalOffset(0)` को कॉल करें, या ऑफ़सेट को समायोजित करके सामग्री को पेज की सीमाओं के भीतर रखें। |
| **सेव पर IOException** | गंतव्य फ़ोल्डर मौजूद नहीं है या लिखने की अनुमति नहीं है। | फ़ोल्डर पहले से बनाएं या प्रोग्राम को उचित अनुमतियों के साथ चलाएँ। |

## अक्सर पूछे जाने वाले प्रश्न

**प्रश्न 1: Aspose.Note for Java की दस्तावेज़ीकरण कहाँ मिल सकती है?**  
उत्तर: आप दस्तावेज़ीकरण [यहाँ](https://reference.aspose.com/note/java/) पा सकते हैं।

**प्रश्न 2: Aspose.Note for Java कैसे डाउनलोड करें?**  
उत्तर: आप Aspose.Note for Java को [डाउनलोड पेज](https://releases.aspose.com/note/java/) से डाउनलोड कर सकते हैं।

**प्रश्न 3: क्या Aspose.Note for Java के लिए मुफ्त ट्रायल उपलब्ध है?**  
उत्तर: हाँ, आप [वेबसाइट](https://releases.aspose.com/) से मुफ्त ट्रायल प्राप्त कर सकते हैं।

**प्रश्न 4: Aspose.Note for Java के लिए समर्थन कहाँ मिल सकता है?**  
उत्तर: समर्थन के लिए, [Aspose.Note फ़ोरम](https://forum.aspose.com/c/note/28) पर जाएँ।

**प्रश्न 5: क्या मैं Aspose.Note for Java के लिए अस्थायी लाइसेंस प्राप्त कर सकता हूँ?**  
उत्तर: हाँ, आप अस्थायी लाइसेंस [यहाँ](https://purchase.aspose.com/temporary-license/) से अनुरोध कर सकते हैं।

**प्रश्न 6: क्या मैं इस कोड को **Linux सर्वर पर OneNote को PDF के रूप में सहेजने** के लिए उपयोग कर सकता हूँ?**  
उत्तर: बिल्कुल। Aspose.Note लाइब्रेरी प्लेटफ़ॉर्म‑निर्भर नहीं है, इसलिए वही कोड Windows, Linux और macOS पर काम करता है।

**प्रश्न 7: क्या API **OneNote में इमेज एम्बेड** करने के लिए पारदर्शी PNG का समर्थन करता है?**  
उत्तर: हाँ, अल्फा चैनल वाले PNG फ़ाइलें पूरी तरह समर्थित हैं और सम्मिलित होने पर पारदर्शिता बरकरार रहती है।

---

**अंतिम अपडेट:** 2026-03-19  
**परीक्षित संस्करण:** Aspose.Note for Java 24.12 (नवीनतम)  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}