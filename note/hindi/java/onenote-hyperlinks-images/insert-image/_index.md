---
date: 2026-03-19
description: जावा के साथ Aspose.Note for Java का उपयोग करके OneNote में इमेज कैसे
  जोड़ें, इमेज के आयाम कैसे सेट करें, और OneNote को PDF के रूप में कैसे सहेजें, यह
  सीखें।
linktitle: Insert an Image in OneNote Document with Java
second_title: Aspose.Note Java API
title: Java का उपयोग करके OneNote में छवि जोड़ें
url: /hi/java/onenote-hyperlinks-images/insert-image/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java के साथ OneNote दस्तावेज़ में छवि सम्मिलित करें

## परिचय

इस ट्यूटोरियल में आप **OneNote में छवि कैसे जोड़ें** यह प्रोग्रामेटिक रूप से Java और Aspose.Note for Java लाइब्रेरी का उपयोग करके सीखेंगे। OneNote पेज़ में चित्र एम्बेड करना उपयोगी होता है जब आपको मीटिंग मिनट्स, स्वचालित रिपोर्ट या ऐसा दस्तावेज़ बनाना हो जिसमें टेक्स्ट के साथ विज़ुअल डेटा भी हो। गाइड के अंत तक आप एक मौजूदा OneNote फ़ाइल लोड कर सकेंगे, छवि सम्मिलित कर सकेंगे, वैकल्पिक रूप से उसका आकार और स्थिति समायोजित कर सकेंगे, और यहाँ तक कि **OneNote को PDF के रूप में सहेजें** भी कर सकेंगे – बिना OneNote UI खोले।

## त्वरित उत्तर
- **Java का उपयोग करके OneNote में छवि जोड़ने का सबसे आसान तरीका क्या है?**  
  Aspose.Note for Java की `Image` क्लास का उपयोग करें और उसे पेज में जोड़ें।
- **उत्पादन उपयोग के लिए लाइसेंस चाहिए क्या?**  
  हाँ, उत्पादन परिनियोजन के लिए एक व्यावसायिक लाइसेंस आवश्यक है।
- **क्या मैं छवि के लिए कस्टम आयाम सेट कर सकता हूँ?**  
  बिल्कुल – `Image` ऑब्जेक्ट पर `setWidth()` और `setHeight()` कॉल करें।
- **छवि जोड़ने के बाद OneNote फ़ाइल को PDF के रूप में सहेजना संभव है क्या?**  
  हाँ, `save(..., SaveFormat.Pdf)` कॉल करके **OneNote को PDF के रूप में सहेजें**।
- **कौन सा Java संस्करण समर्थित है?**  
  Aspose.Note for Java JDK 8 और उसके बाद के संस्करणों के साथ काम करता है।

## OneNote में छवि क्यों जोड़ें?

विज़ुअल तत्व जोड़ने से नोट्स समझने में आसान और अधिक आकर्षक बनते हैं। छवियाँ आरेख, स्क्रीनशॉट या डेटा चार्ट को दर्शा सकती हैं, जिन्हें otherwise लंबी टेक्स्ट विवरण की आवश्यकता होगी। इस चरण को स्वचालित करने से समय बचता है, विशेषकर जब डेटा स्रोतों से बड़ी मात्रा में नोट्स उत्पन्न करने हों।

## पूर्वापेक्षाएँ

शुरू करने से पहले सुनिश्चित करें कि आपके पास निम्नलिखित तैयार हैं:

### 1. Java Development Kit (JDK)
JDK 8 या नया स्थापित करें। आप इसे Oracle वेबसाइट से डाउनलोड कर सकते हैं या कोई OpenJDK वितरण उपयोग कर सकते हैं।

### 2. Aspose.Note for Java Library
नवीनतम Aspose.Note for Java लाइब्रेरी डाउनलोड करें और उसे अपने प्रोजेक्ट की क्लासपाथ में जोड़ें। विस्तृत सेटअप निर्देश आधिकारिक [documentation](https://reference.aspose.com/note/java/) में उपलब्ध हैं।

## पैकेज आयात करें

आवश्यक क्लासेज़ को इम्पोर्ट करके शुरू करें। ये इम्पोर्ट्स आपको कोर Aspose.Note कार्यक्षमता और बेसिक Java यूटिलिटीज़ तक पहुँच प्रदान करते हैं।

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## चरण‑दर‑चरण मार्गदर्शिका

नीचे एक संक्षिप्त, क्रमांकित walkthrough दिया गया है। प्रत्येक चरण में एक छोटा स्पष्टीकरण और वह सटीक कोड है जिसे आपको कॉपी करना है।

### चरण 1: OneNote दस्तावेज़ लोड करें

हम एक `LoadOptions` इंस्टेंस बनाते हैं (भविष्य में कस्टमाइज़ेशन के लिए उपयोगी) और मौजूदा `.one` फ़ाइल खोलते हैं।

```java
LoadOptions options = new LoadOptions();
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", options);
```

### चरण 2: लक्ष्य पृष्ठ प्राप्त करें

सरलता के लिए हम दस्तावेज़ के पहले पृष्ठ पर काम करते हैं, लेकिन आप अपनी आवश्यकता अनुसार किसी भी पृष्ठ पर नेविगेट कर सकते हैं।

```java
Page page = oneFile.getFirstChild();
```

### चरण 3: वह छवि लोड करें जिसे आप एम्बेड करना चाहते हैं

डॉक्यूमेंट रेफ़रेंस और चित्र फ़ाइल के पथ को पास करके एक `Image` ऑब्जेक्ट बनाएं।

```java
Image image = new Image(oneFile, dataDir + "Input.jpg");
```

### चरण 4: छवि आयाम सेट करें Java (वैकल्पिक)

यदि आपको चित्र को किसी विशिष्ट क्षेत्र में फिट करना है, तो उसकी चौड़ाई, ऊँचाई और ऑफ़सेट समायोजित करें। यही वह जगह है जहाँ द्वितीयक कीवर्ड **set image dimensions java** काम आता है।

```java
image.setWidth(100);
image.setHeight(100);
image.setVerticalOffset(400);
image.setHorizontalOffset(100);
image.setAlignment(HorizontalAlignment.Right);
```

### चरण 5: छवि को पृष्ठ में जोड़ें

`appendChildLast` मेथड चयनित पृष्ठ पर छवि को अंतिम तत्व के रूप में जोड़ता है।

```java
page.appendChildLast(image);
```

### चरण 6: दस्तावेज़ सहेजें – आप OneNote को PDF के रूप में भी सहेज सकते हैं

अंत में परिवर्तन को स्थायी बनाएं। उदाहरण में फ़ाइल को PDF के रूप में सहेजने का प्रदर्शन किया गया है, जो द्वितीयक कीवर्ड **save onenote as pdf** को पूरा करता है।

```java
try {
    oneFile.save(dataDir + "InsertanImage_out.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## सामान्य समस्याएँ और समाधान

| लक्षण | संभावित कारण | समाधान |
|---------|--------------|-----|
| `FileNotFoundException` जब छवि लोड कर रहे हों | गलत छवि पथ | `dataDir` और छवि फ़ाइलनाम को सही होने की पुष्टि करें। |
| छवि विकृत दिख रही है | चौड़ाई/ऊँचाई गलत सेट की गई | मूल छवि आयाम उपयोग करें या `setWidth`/`setHeight` कॉल करने से पहले उचित अनुपात गणना करें। |
| PDF आउटपुट खाली है | Aspose.Note के लिए लाइसेंस नहीं है | `save` कॉल करने से पहले वैध लाइसेंस लागू करें। |

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं इस विधि से एक ही OneNote दस्तावेज़ में कई छवियाँ सम्मिलित कर सकता हूँ?

**A:** हाँ। प्रत्येक छवि के लिए चरण 3‑5 दोहराएँ, चाहे वही पृष्ठ हो या अलग पृष्ठ।

### Q2: क्या Aspose.Note for Java सभी OneNote संस्करणों के साथ संगत है?

**A:** Aspose.Note for Java Microsoft OneNote 2010 और बाद के संस्करणों में निर्मित OneNote फ़ाइलों को सपोर्ट करता है।

### Q3: क्या मैं PNG या GIF जैसे विभिन्न फ़ॉर्मेट की छवियाँ OneNote दस्तावेज़ में सम्मिलित कर सकता हूँ?

**A:** बिल्कुल। लाइब्रेरी PNG, JPEG, GIF, BMP और कई अन्य सामान्य फ़ॉर्मेट स्वीकार करती है।

### Q4: क्या Aspose.Note for Java का परीक्षण संस्करण उपलब्ध है?

**A:** हाँ, आप Aspose वेबसाइट से एक मुफ्त ट्रायल डाउनलोड कर सकते हैं ताकि API का मूल्यांकन कर सकें।

### Q5: Aspose.Note for Java के लिए तकनीकी समर्थन कैसे प्राप्त करूँ?

**A:** आप Aspose.Note उत्पादों के लिए समर्पित [forum](https://forum.aspose.com/c/note/28) पर जाकर मदद ले सकते हैं।

## निष्कर्ष

अब आपके पास एक पूर्ण, उत्पादन‑तैयार उदाहरण है जो **Java का उपयोग करके OneNote में छवि कैसे जोड़ें** दिखाता है, उसकी उपस्थिति को कस्टमाइज़ करता है, और वैकल्पिक रूप से **OneNote को PDF के रूप में सहेजें**। इस कोड को अपने कार्यप्रवाह में अनुकूलित करने में संकोच न करें—चाहे आप रिपोर्टिंग इंजन, स्वचालित दस्तावेज़ीकरण प्रणाली, या कस्टम नोट‑लेने एप्लिकेशन बना रहे हों।

---

**अंतिम अपडेट:** 2026-03-19  
**परीक्षण किया गया:** Aspose.Note for Java 24.10  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}