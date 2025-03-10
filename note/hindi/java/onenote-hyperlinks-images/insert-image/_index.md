---
title: जावा के साथ OneNote दस्तावेज़ में एक छवि सम्मिलित करें
linktitle: जावा के साथ OneNote दस्तावेज़ में एक छवि सम्मिलित करें
second_title: Aspose.नोट जावा एपीआई
description: जावा लाइब्रेरी के लिए Aspose.Note के साथ जावा का उपयोग करके OneNote दस्तावेज़ों में छवियां सम्मिलित करना सीखें। निर्बाध एकीकरण के लिए हमारी चरण-दर-चरण मार्गदर्शिका का पालन करें।
weight: 16
url: /hi/java/onenote-hyperlinks-images/insert-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# जावा के साथ OneNote दस्तावेज़ में एक छवि सम्मिलित करें

## परिचय

इस ट्यूटोरियल में, हम यह पता लगाएंगे कि जावा के लिए Aspose.Note की सहायता से जावा का उपयोग करके OneNote दस्तावेज़ में एक छवि कैसे सम्मिलित की जाए। जावा के लिए Aspose.Note एक शक्तिशाली लाइब्रेरी है जो डेवलपर्स को Microsoft OneNote फ़ाइलों के साथ प्रोग्रामेटिक रूप से काम करने की अनुमति देती है, जिससे OneNote दस्तावेज़ बनाने, पढ़ने और हेरफेर करने जैसे विभिन्न संचालन सक्षम होते हैं।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ स्थापित हैं:

### 1. जावा डेवलपमेंट किट (जेडीके)
सुनिश्चित करें कि आपके सिस्टम पर जावा डेवलपमेंट किट (जेडीके) स्थापित है। आप Oracle वेबसाइट से JDK डाउनलोड और इंस्टॉल कर सकते हैं।

### 2. जावा लाइब्रेरी के लिए Aspose.Note
 निम्नलिखित का पालन करके जावा लाइब्रेरी के लिए Aspose.Note डाउनलोड करें और सेट करें[प्रलेखन](https://reference.aspose.com/note/java/).

## पैकेज आयात करें

अपने जावा प्रोजेक्ट में आवश्यक पैकेज आयात करके प्रारंभ करें। इन पैकेजों में Aspose.Note लाइब्रेरी और अन्य आवश्यक निर्भरताएँ शामिल हैं।

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

आइए OneNote दस्तावेज़ में एक छवि सम्मिलित करने की प्रक्रिया को कई चरणों में विभाजित करें:

## चरण 1: OneNote दस्तावेज़ लोड करें

सबसे पहले, OneNote दस्तावेज़ को लोड करें जिसमें आप छवि सम्मिलित करना चाहते हैं।

```java
LoadOptions options = new LoadOptions();
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", options);
```

## चरण 2: पृष्ठ प्राप्त करें

दस्तावेज़ में वह पृष्ठ पुनः प्राप्त करें जहाँ आप छवि सम्मिलित करना चाहते हैं।

```java
Page page = oneFile.getFirstChild();
```

## चरण 3: छवि लोड करें

वह छवि लोड करें जिसे आप OneNote दस्तावेज़ में सम्मिलित करना चाहते हैं।

```java
Image image = new Image(oneFile, dataDir + "Input.jpg");
```

## चरण 4: छवि विशेषताओं को अनुकूलित करें (वैकल्पिक)

वैकल्पिक रूप से, आप अपनी आवश्यकताओं के अनुसार छवि के आकार, स्थान और संरेखण को अनुकूलित कर सकते हैं।

```java
image.setWidth(100);
image.setHeight(100);
image.setVerticalOffset(400);
image.setHorizontalOffset(100);
image.setAlignment(HorizontalAlignment.Right);
```

## चरण 5: पृष्ठ पर छवि जोड़ें

OneNote दस्तावेज़ में पृष्ठ पर छवि जोड़ें।

```java
page.appendChildLast(image);
```

## चरण 6: दस्तावेज़ सहेजें

सम्मिलित छवि सहित संशोधित दस्तावेज़ सहेजें।

```java
try {
    oneFile.save(dataDir + "InsertanImage_out.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## निष्कर्ष

इस ट्यूटोरियल में, हमने सीखा है कि जावा लाइब्रेरी के लिए Aspose.Note की मदद से जावा का उपयोग करके OneNote दस्तावेज़ में एक छवि कैसे सम्मिलित की जाए। चरण-दर-चरण मार्गदर्शिका का पालन करके, आप आसानी से छवियों को अपने OneNote दस्तावेज़ों में प्रोग्रामेटिक रूप से शामिल कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं इस पद्धति का उपयोग करके एक ही OneNote दस्तावेज़ में एकाधिक छवियाँ सम्मिलित कर सकता हूँ?

उ1: हां, आप प्रत्येक छवि के लिए इस ट्यूटोरियल में उल्लिखित प्रक्रिया को दोहराकर एक ही OneNote दस्तावेज़ में एकाधिक छवियां सम्मिलित कर सकते हैं।

### Q2: क्या Java के लिए Aspose.Note OneNote के सभी संस्करणों के साथ संगत है?

A2: Java के लिए Aspose.Note Microsoft OneNote 2010 और बाद के संस्करणों में बनाई गई OneNote फ़ाइलों के साथ काम करने का समर्थन करता है।

### Q3: क्या मैं OneNote दस्तावेज़ में PNG या GIF जैसे विभिन्न प्रारूपों की छवियाँ सम्मिलित कर सकता हूँ?

A3: हां, जावा के लिए Aspose.Note पीएनजी, जेपीईजी, जीआईएफ और अन्य सहित विभिन्न प्रारूपों में छवियों को सम्मिलित करने का समर्थन करता है।

### Q4: क्या परीक्षण उद्देश्यों के लिए जावा के लिए Aspose.Note का कोई परीक्षण संस्करण उपलब्ध है?

उ4: हाँ, आप मूल्यांकन उद्देश्यों के लिए वेबसाइट से जावा के लिए Aspose.Note का निःशुल्क परीक्षण संस्करण डाउनलोड कर सकते हैं।

### Q5: मैं जावा के लिए Aspose.Note के लिए तकनीकी सहायता कैसे प्राप्त कर सकता हूं?

 A5: आप जावा के लिए Aspose.Note के लिए तकनीकी सहायता प्राप्त कर सकते हैं[मंच](https://forum.aspose.com/c/note/28) Aspose.Note उत्पादों को समर्पित।
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
