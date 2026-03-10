---
date: 2025-12-21
description: जावा के साथ Aspose.Note for Java का उपयोग करके OneNote दस्तावेज़ों में
  छवि कैसे जोड़ें, सीखें। छवियों को सम्मिलित करने और वैकल्पिक रूप से OneNote को PDF
  के रूप में सहेजने के लिए हमारे चरण‑दर‑चरण मार्गदर्शिका का पालन करें।
linktitle: Insert an Image in OneNote Document with Java
second_title: Aspose.Note Java API
title: जावा का उपयोग करके वननोट में चित्र कैसे जोड़ें
url: /hi/java/onenote-hyperlinks-images/insert-image/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java के साथ OneNote दस्तावेज़ में छवि सम्मिलित करें

## परिचय

इस ट्यूटोरियल में हम Aspose.Note for Java की मदद से Java का उपयोग करके OneNote दस्तावेज़ में छवि कैसे सम्मिलित की जाए, इसे देखेंगे। Aspose.Note for Java एक शक्तिशाली लाइब्रेरी है जो डेवलपर्स को Microsoft OneNote फ़ाइलों के साथ प्रोग्रामेटिक रूप से काम करने की सुविधा देती है, जिससे आप दस्तावेज़ बनाना, पढ़ना और संशोधित करना जैसे विभिन्न कार्य कर सकते हैं।

## त्वरित उत्तर
- **Java का उपयोग करके OneNote में छवि जोड़ने का सबसे आसान तरीका क्या है?**  
  Aspose.Note for Java की `Image` क्लास का उपयोग करें और इसे पृष्ठ में जोड़ें।
- **क्या उत्पादन उपयोग के लिए लाइसेंस चाहिए?**  
  हाँ, उत्पादन परिनियोजन के लिए एक व्यावसायिक लाइसेंस आवश्यक है।
- **क्या मैं छवि के लिए कस्टम आयाम सेट कर सकता हूँ?**  
  बिल्कुल – `Image` ऑब्जेक्ट पर `setWidth()` और `setHeight()` कॉल करें।
- **छवि जोड़ने के बाद OneNote फ़ाइल को PDF के रूप में सहेजना संभव है?**  
  हाँ, `save(..., SaveFormat.Pdf)` कॉल करके **OneNote को PDF के रूप में सहेजें**।
- **कौन सा Java संस्करण समर्थित है?**  
  Aspose.Note for Java JDK 8 और उसके बाद के संस्करणों के साथ काम करता है।

## Java का उपयोग करके OneNote में छवि कैसे जोड़ें?

कोड में उतरने से पहले, आइए संक्षेप में चर्चा करें कि आप प्रोग्रामेटिक रूप से OneNote में छवियों को क्यों एम्बेड करना चाहेंगे। चाहे आप मीटिंग मिनट्स बना रहे हों, स्वचालित रिपोर्ट तैयार कर रहे हों, या दस्तावेज़ीकरण पाइपलाइन बना रहे हों, छवियों को सम्मिलित करने से आपके नोट्स को वह दृश्य संदर्भ मिलता है जो साधारण टेक्स्ट नहीं दे सकता। Aspose.Note for Java के साथ आप यह पूरी तरह कोड में, OneNote UI खोले बिना कर सकते हैं।

## पूर्वापेक्षाएँ

### 1. Java Development Kit (JDK)
सुनिश्चित करें कि आपके सिस्टम पर Java Development Kit (JDK) स्थापित है। आप Oracle की वेबसाइट से JDK डाउनलोड और इंस्टॉल कर सकते हैं।

### 2. Aspose.Note for Java लाइब्रेरी
[डॉक्यूमेंटेशन](https://reference.aspose.com/note/java/) का पालन करके Aspose.Note for Java लाइब्रेरी डाउनलोड और सेट अप करें।

## पैकेज आयात करें

अपने Java प्रोजेक्ट में आवश्यक पैकेज आयात करके शुरू करें। इन पैकेजों में Aspose.Note लाइब्रेरी और अन्य आवश्यक निर्भरताएँ शामिल हैं।

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

OneNote दस्तावेज़ में छवि सम्मिलित करने की प्रक्रिया को कई चरणों में विभाजित करते हैं:

## चरण 1: OneNote दस्तावेज़ लोड करें

जिस OneNote दस्तावेज़ में आप छवि सम्मिलित करना चाहते हैं, उसे लोड करें।

```java
LoadOptions options = new LoadOptions();
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", options);
```

## चरण 2: पृष्ठ प्राप्त करें

दस्तावेज़ में वह पृष्ठ प्राप्त करें जहाँ आप छवि जोड़ना चाहते हैं।

```java
Page page = oneFile.getFirstChild();
```

## चरण 3: छवि लोड करें

जिस छवि को आप OneNote दस्तावेज़ में सम्मिलित करना चाहते हैं, उसे लोड करें।

```java
Image image = new Image(oneFile, dataDir + "Input.jpg");
```

## चरण 4: छवि गुण अनुकूलित करें (वैकल्पिक)

वैकल्पिक रूप से, आप अपनी आवश्यकताओं के अनुसार छवि का आकार, स्थान और संरेखण अनुकूलित कर सकते हैं। यह वह जगह है जहाँ आप **set image dimensions Java** शैली में छवि के आयाम सेट करते हैं।

```java
image.setWidth(100);
image.setHeight(100);
image.setVerticalOffset(400);
image.setHorizontalOffset(100);
image.setAlignment(HorizontalAlignment.Right);
```

## चरण 5: पृष्ठ में छवि जोड़ें

OneNote दस्तावेज़ के पृष्ठ में छवि जोड़ें।

```java
page.appendChildLast(image);
```

## चरण 6: दस्तावेज़ सहेजें

परिवर्तित दस्तावेज़ को सहेजें, जिसमें सम्मिलित छवि भी शामिल है। आप इस चरण पर **OneNote को PDF के रूप में सहेज** भी सकते हैं।

```java
try {
    oneFile.save(dataDir + "InsertanImage_out.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## निष्कर्ष

इस ट्यूटोरियल में हमने Aspose.Note for Java लाइब्रेरी की मदद से Java का उपयोग करके OneNote दस्तावेज़ में छवि कैसे सम्मिलित की जाए, सीखा। चरण‑दर‑चरण मार्गदर्शिका का पालन करके आप प्रोग्रामेटिक रूप से अपने OneNote दस्तावेज़ों में आसानी से छवियाँ जोड़ सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं इस विधि से एक ही OneNote दस्तावेज़ में कई छवियाँ सम्मिलित कर सकता हूँ?

A1: हाँ, आप इस ट्यूटोरियल में बताए गए प्रक्रिया को प्रत्येक छवि के लिए दोहराकर एक ही OneNote दस्तावेज़ में कई छवियाँ सम्मिलित कर सकते हैं।

### Q2: क्या Aspose.Note for Java सभी OneNote संस्करणों के साथ संगत है?

A2: Aspose.Note for Java Microsoft OneNote 2010 और उसके बाद के संस्करणों में निर्मित OneNote फ़ाइलों के साथ काम करने का समर्थन करता है।

### Q3: क्या मैं PNG या GIF जैसे विभिन्न फ़ॉर्मेट की छवियों को OneNote दस्तावेज़ में सम्मिलित कर सकता हूँ?

A3: हाँ, Aspose.Note for Java PNG, JPEG, GIF आदि सहित विभिन्न फ़ॉर्मेट की छवियों को सम्मिलित करने का समर्थन करता है।

### Q4: क्या परीक्षण उद्देश्यों के लिए Aspose.Note for Java का ट्रायल संस्करण उपलब्ध है?

A4: हाँ, आप मूल्यांकन के लिए Aspose.Note for Java का मुफ्त ट्रायल संस्करण वेबसाइट से डाउनलोड कर सकते हैं।

### Q5: मैं Aspose.Note for Java के लिए तकनीकी समर्थन कैसे प्राप्त कर सकता हूँ?

A5: आप Aspose.Note उत्पादों के लिए समर्पित [फ़ोरम](https://forum.aspose.com/c/note/28) पर जाकर तकनीकी समर्थन प्राप्त कर सकते हैं।

---

**Last Updated:** 2025-12-21  
**Tested With:** Aspose.Note for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}