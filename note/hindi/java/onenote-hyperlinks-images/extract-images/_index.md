---
title: जावा का उपयोग करके OneNote दस्तावेज़ से छवियाँ निकालें
linktitle: जावा का उपयोग करके OneNote दस्तावेज़ से छवियाँ निकालें
second_title: Aspose.नोट जावा एपीआई
description: Aspose.Note लाइब्रेरी के साथ जावा का उपयोग करके OneNote दस्तावेज़ों से छवियां निकालने का तरीका जानें। निर्बाध छवि निष्कर्षण के लिए हमारी चरण-दर-चरण मार्गदर्शिका का पालन करें।
weight: 14
url: /hi/java/onenote-hyperlinks-images/extract-images/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# जावा का उपयोग करके OneNote दस्तावेज़ से छवियाँ निकालें

## परिचय

इस ट्यूटोरियल में, हम Aspose.Note लाइब्रेरी की मदद से जावा का उपयोग करके OneNote दस्तावेज़ से छवियां निकालने की प्रक्रिया में आपका मार्गदर्शन करेंगे।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

1.  जावा डेवलपमेंट किट (जेडीके): सुनिश्चित करें कि आपके सिस्टम पर जावा स्थापित है। आप इसे यहां से डाउनलोड और इंस्टॉल कर सकते हैं[वेबसाइट](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).

2.  Aspose.Note लाइब्रेरी: Aspose.Note लाइब्रेरी को डाउनलोड करें और अपने जावा प्रोजेक्ट में शामिल करें। आप इसे यहां से प्राप्त कर सकते हैं[लिंक को डाउनलोड करें](https://releases.aspose.com/note/java/).

## पैकेज आयात करें

आरंभ करने के लिए, आवश्यक पैकेज आयात करें:

```java
import java.io.IOException;
import java.nio.file.Files;
import java.nio.file.Paths;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.Image;
```

## चरण 1: दस्तावेज़ लोड करें

सबसे पहले, Aspose.Note का उपयोग करके OneNote दस्तावेज़ लोड करें:

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```

## चरण 2: सभी छवियाँ प्राप्त करें

इसके बाद, दस्तावेज़ से सभी छवियाँ पुनः प्राप्त करें:

```java
List<Image> list = doc.getChildNodes(Image.class);
System.out.printf("Total Images: %s\n\n", list.size());
```

## चरण 3: छवियाँ निकालें

छवियों की सूची में पुनरावृति करें और प्रत्येक छवि को एक फ़ाइल में सहेजें:

```java
for (int i = 0; i < list.size(); i++) {
    Image image = list.get(i);
    String outputFile = "ExtractImages_out" + i + "_" + image.getFileName();
    byte[] buffer = image.getBytes();
    Files.write(Paths.get(dataDir + outputFile), buffer);
    System.out.printf("File saved: %s\n", dataDir);
}
```

## निष्कर्ष

जावा का उपयोग करके OneNote दस्तावेज़ से छवियां निकालना Aspose.Note लाइब्रेरी के साथ सहजता से प्राप्त किया जा सकता है। इस ट्यूटोरियल में बताए गए चरणों का पालन करके, आप आगे की प्रक्रिया या विश्लेषण के लिए आसानी से अपने दस्तावेज़ों से छवियां पुनर्प्राप्त कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं पासवर्ड से सुरक्षित OneNote दस्तावेज़ों से छवियाँ निकाल सकता हूँ?

A1: हां, Aspose.Note पासवर्ड-सुरक्षित दस्तावेज़ों से छवियां निकालने का भी समर्थन करता है।

### Q2: क्या Aspose.Note जावा के विभिन्न संस्करणों के साथ संगत है?

A2: Aspose.Note जावा के विभिन्न संस्करणों के साथ संगत है, जो डेवलपर्स के लिए लचीलापन सुनिश्चित करता है।

### Q3: क्या मैं एक ही निष्पादन में एकाधिक OneNote दस्तावेज़ों से छवियाँ निकाल सकता हूँ?

उ3: बिल्कुल, आप Aspose.Note का उपयोग करके कई दस्तावेज़ों को दोहरा सकते हैं और उनमें से प्रत्येक से छवियां निकाल सकते हैं।

### Q4: क्या OneNote दस्तावेज़ों के लिए कोई आकार सीमाएँ हैं?

A4: Aspose.Note विभिन्न आकारों के दस्तावेज़ों को कुशलतापूर्वक संभालता है, यह सुनिश्चित करता है कि छवि निष्कर्षण के लिए दस्तावेज़ के आकार पर कोई सीमा न हो।

### Q5: क्या Aspose.Note छवियों के अलावा अन्य प्रकार की सामग्री निकालने का समर्थन करता है?

A5: हाँ, छवियों के अलावा, Aspose.Note OneNote दस्तावेज़ों से पाठ, अनुलग्नक और अन्य सामग्री प्रकारों को निकालने की अनुमति देता है।
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
