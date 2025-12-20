---
date: 2025-12-20
description: Aspose.Note for Java का उपयोग करके OneNote में चित्र कैसे जोड़ें, सीखें।
  OneNote दस्तावेज़ बनाने और प्रोग्रामेटिक रूप से छवियों को सम्मिलित करने के लिए चरण‑दर‑चरण
  मार्गदर्शिका।
linktitle: How to add picture to OneNote using Java – Build Document and Insert Image
second_title: Aspose.Note Java API
title: Java का उपयोग करके OneNote में चित्र कैसे जोड़ें – दस्तावेज़ बनाएं और छवि सम्मिलित
  करें
url: /hi/java/onenote-hyperlinks-images/build-doc-insert-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java का उपयोग करके OneNote में चित्र कैसे जोड़ें – दस्तावेज़ बनाएं और छवि सम्मिलित करें

## परिचय

इस ट्यूटोरियल में, आप Aspose.Note Java API का उपयोग करके **OneNote में चित्र कैसे जोड़ें** सीखेंगे। हम शुरू से एक OneNote दस्तावेज़ बनाना, एक छवि सम्मिलित करना, और परिणाम को PDF के रूप में सहेजना दिखाएंगे। चाहे आप रिपोर्टिंग टूल बना रहे हों, नोट‑लेखन को स्वचालित कर रहे हों, या प्रोग्रामेटिक रूप से ग्राफ़िक्स एम्बेड करने की आवश्यकता हो, यह गाइड आपको एक स्पष्ट, व्यावहारिक मार्ग प्रदान करता है।

## त्वरित उत्तर
- **मुझे कौनसी लाइब्रेरी चाहिए?** Aspose.Note for Java.  
- **क्या मैं कोई भी इमेज फ़ॉर्मेट सम्मिलित कर सकता हूँ?** JPEG, PNG, BMP, GIF और अधिक समर्थित हैं।  
- **कौनसे आउटपुट फ़ॉर्मेट उपलब्ध हैं?** आप OneNote, PDF, XPS, HTML आदि के रूप में सहेज सकते हैं।  
- **क्या उत्पादन के लिए लाइसेंस चाहिए?** हाँ, गैर‑ट्रायल उपयोग के लिए एक व्यावसायिक लाइसेंस आवश्यक है।  
- **क्या कोड क्रॉस‑प्लेटफ़ॉर्म है?** बिल्कुल – Java Windows, Linux, और macOS पर चलता है।

## “OneNote में चित्र जोड़ना” क्या है?
OneNote में चित्र जोड़ना का अर्थ है प्रोग्रामेटिक रूप से एक इमेज फ़ाइल को OneNote पेज में एम्बेड करना ताकि वह टेक्स्ट, आउटलाइन या अन्य तत्वों के साथ दिखाई दे। Aspose.Note API OneNote फ़ाइल फ़ॉर्मेट को एब्स्ट्रैक्ट करता है, जिससे आप अंतर्निहित XML संरचना की बजाय सामग्री पर ध्यान केंद्रित कर सकते हैं।

## Java का उपयोग करके OneNote में चित्र क्यों जोड़ें?
- **ऑटोमेशन:** स्क्रीनशॉट के साथ मीटिंग मिनट्स स्वचालित रूप से जनरेट करें।  
- **संगतता:** सुनिश्चित करें कि हर पेज समान लेआउट और ब्रांडिंग का पालन करता है।  
- **इंटीग्रेशन:** अन्य सिस्टमों (जैसे, चार्ट) से डेटा को सीधे OneNote नोटबुक में संयोजित करें।  
- **क्रॉस‑प्लेटफ़ॉर्म:** Java आपको वही कोड किसी भी सर्वर या डेस्कटॉप वातावरण में चलाने देता है।

## पूर्वापेक्षाएँ

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

1. **Java Development Kit (JDK)** – कोई भी नवीनतम संस्करण (8 या बाद का)।  
2. **Aspose.Note for Java लाइब्रेरी** – इसे [website](https://releases.aspose.com/note/java/) से डाउनलोड करें।  
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

एक नया OneNote दस्तावेज़ और एक पेज कंटेनर बनाएं जहाँ सामग्री रहेगी।

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

### चरण 2: आउटलाइन को इनिशियलाइज़ करें

*आउटलाइन* टेक्स्ट और इमेज जैसे तत्वों के लिए कंटेनर की तरह काम करती है। हम इसके ऑफ़सेट को शून्य सेट करते हैं ताकि सामग्री शीर्ष‑बाएँ कोने से शुरू हो।

```java
Outline outline = new Outline();
outline.setVerticalOffset(0);
outline.setHorizontalOffset(0);
```

### चरण 3: इमेज लोड करें और संरेखित करें

जिस चित्र को आप एम्बेड करना चाहते हैं उसे लोड करें और पेज के दाएँ पक्ष में संरेखित करें। यही वह जगह है जहाँ हम वास्तव में **OneNote में चित्र जोड़ते** हैं।

```java
Image image = new Image(null, dataDir + "Input.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

### चरण 4: इमेज को आउटलाइन एलिमेंट से जोड़ें

`OutlineElement` के अंदर इमेज को रैप करें। यह चरण विज़ुअल ऑब्जेक्ट को दस्तावेज़ की आउटलाइन हाइरार्की से जोड़ता है।

```java
OutlineElement outlineElem = new OutlineElement();
outlineElem.appendChildLast(image);
```

### चरण 5: दस्तावेज़ संरचना को असेंबल करें

आउटलाइन एलिमेंट को आउटलाइन में जोड़ें, फिर आउटलाइन को पेज से जोड़ें, और अंत में पेज को दस्तावेज़ में जोड़ें।

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

### चरण 6: OneNote दस्तावेज़ सहेजें

दस्तावेज़ को डिस्क पर सहेजें। इस उदाहरण में हम PDF में एक्सपोर्ट करते हैं, लेकिन आप `SaveFormat` बदलकर इसे मूल OneNote फ़ाइल (`.one`) के रूप में भी सहेज सकते हैं।

```java
try {
    doc.save(dataDir + "NewOneNotedocument_out", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## सामान्य समस्याएँ और समाधान

| समस्या | क्यों होता है | समाधान |
|-------|----------------|-----|
| **छवि नहीं दिख रही** | गलत फ़ाइल पथ या असमर्थित फ़ॉर्मेट। | `dataDir` सही फ़ोल्डर की ओर इशारा कर रहा है, यह सुनिश्चित करें और समर्थित इमेज टाइप (JPEG, PNG, आदि) का उपयोग करें। |
| **दस्तावेज़ खाली PDF के रूप में सहेजा गया** | आउटलाइन ऑफ़सेट गलत सेट किए गए। | सुनिश्चित करें कि `setVerticalOffset(0)` और `setHorizontalOffset(0)` कॉल किए गए हैं, या ऑफ़सेट को समायोजित करें ताकि सामग्री पेज की सीमा के भीतर रहे। |
| **सेव पर IOException** | गंतव्य फ़ोल्डर मौजूद नहीं है या लिखने की अनुमति नहीं है। | फ़ोल्डर को पहले बनाएं या प्रोग्राम को उचित अनुमतियों के साथ चलाएँ। |

## अक्सर पूछे जाने वाले प्रश्न

**Q1: Aspose.Note for Java की डॉक्यूमेंटेशन कहाँ मिल सकती है?**  
A1: आप डॉक्यूमेंटेशन [here](https://reference.aspose.com/note/java/) पर एक्सेस कर सकते हैं।

**Q2: Aspose.Note for Java को कैसे डाउनलोड करें?**  
A2: आप Aspose.Note for Java को [download page](https://releases.aspose.com/note/java/) से डाउनलोड कर सकते हैं।

**Q3: क्या Aspose.Note for Java के लिए मुफ्त ट्रायल उपलब्ध है?**  
A3: हाँ, आप मुफ्त ट्रायल [website](https://releases.aspose.com/) से प्राप्त कर सकते हैं।

**Q4: Aspose.Note for Java के लिए सपोर्ट कहाँ मिल सकता है?**  
A4: सपोर्ट के लिए, [Aspose.Note forum](https://forum.aspose.com/c/note/28) पर जाएँ।

**Q5: क्या मैं Aspose.Note for Java के लिए अस्थायी लाइसेंस प्राप्त कर सकता हूँ?**  
A5: हाँ, आप अस्थायी लाइसेंस [here](https://purchase.aspose.com/temporary-license/) से अनुरोध कर सकते हैं।

---

**अंतिम अपडेट:** 2025-12-20  
**परीक्षित संस्करण:** Aspose.Note for Java 24.12 (latest)  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}