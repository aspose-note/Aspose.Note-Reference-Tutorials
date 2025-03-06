---
title: जावा का उपयोग करके OneNote से छवि जानकारी प्राप्त करें
linktitle: जावा का उपयोग करके OneNote से छवि जानकारी प्राप्त करें
second_title: Aspose.नोट जावा एपीआई
description: जावा में OneNote डॉक्स से छवि जानकारी निकालें! छवि आयाम, फ़ाइल नाम और बहुत कुछ प्राप्त करें। आसान चरण और कोड उदाहरण शामिल हैं। #वननोट #जावा #एस्पोज़
weight: 15
url: /hi/java/onenote-hyperlinks-images/get-image-info/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# जावा का उपयोग करके OneNote से छवि जानकारी प्राप्त करें

## परिचय

जावा विकास के क्षेत्र में, विभिन्न दस्तावेज़ प्रारूपों से जानकारी निकालना एक सामान्य कार्य है। नोट लेने के लिए एक लोकप्रिय मंच OneNote में अक्सर पाठ के साथ-साथ छवियां भी होती हैं। जावा का उपयोग करके OneNote फ़ाइलों से प्रोग्रामेटिक रूप से छवि जानकारी पुनर्प्राप्त करना दस्तावेज़ प्रसंस्करण वर्कफ़्लो को सुव्यवस्थित कर सकता है। इस ट्यूटोरियल में, हम जावा के लिए Aspose.Note का उपयोग करके OneNote दस्तावेज़ों से छवि विवरण निकालने के तरीके के बारे में विस्तार से जानेंगे।

## आवश्यक शर्तें

इससे पहले कि हम कार्यान्वयन में उतरें, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ हैं:

### 1. जावा डेवलपमेंट किट (जेडीके)

सुनिश्चित करें कि आपके सिस्टम पर जावा डेवलपमेंट किट (जेडीके) स्थापित है। आप नवीनतम JDK को यहां से डाउनलोड और इंस्टॉल कर सकते हैं[ओरेकल वेबसाइट](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).

### 2. जावा लाइब्रेरी के लिए Aspose.Note

 जावा लाइब्रेरी के लिए Aspose.Note को डाउनलोड करें और अपने प्रोजेक्ट में शामिल करें। आप यहां से लाइब्रेरी प्राप्त कर सकते हैं[डाउनलोड पेज](https://releases.aspose.com/note/java/).

### 3. वननोट दस्तावेज़

एक नमूना OneNote दस्तावेज़ तैयार करें जिसमें छवियाँ हों। इस दस्तावेज़ का उपयोग प्रोग्रामेटिक रूप से छवि जानकारी निकालने के लिए किया जाएगा।

## पैकेज आयात करें

आरंभ करने के लिए, Java के लिए Aspose.Note से आवश्यक पैकेज आयात करें:

```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.Image;
```

आइए उपरोक्त कोड को चरण-दर-चरण निर्देशों में विभाजित करें:

## चरण 1: दस्तावेज़ निर्देशिका सेट करें

```java
String dataDir = "Your Document Directory";
```

 प्रतिस्थापित करें`"Your Document Directory"` आपके OneNote दस्तावेज़ के पथ के साथ।

## चरण 2: दस्तावेज़ लोड करें

```java
Document doc = new Document(dataDir + "Sample1.one");
```

जावा लाइब्रेरी के लिए Aspose.Note का उपयोग करके OneNote दस्तावेज़ लोड करें। सुनिश्चित करें कि आप अपने दस्तावेज़ को सही पथ प्रदान करें।

## चरण 3: सभी छवियाँ प्राप्त करें

```java
List<Image> list = doc.getChildNodes(Image.class);
```

लोड किए गए OneNote दस्तावेज़ से सभी छवियाँ पुनर्प्राप्त करें।

## चरण 4: कुल छवियों की संख्या प्रिंट करें

```java
System.out.printf("Total Images: %s\n\n", list.size());
```

दस्तावेज़ में पाई गई छवियों की कुल संख्या प्रिंट करें।

## चरण 5: छवि जानकारी को ट्रैवर्स और प्रिंट करें

```java
for (Image image : list) {
    System.out.println("Width: " + image.getWidth());
    System.out.println("Height: " + image.getHeight());
    System.out.println("OriginalWidth: " + image.getOriginalWidth());
    System.out.println("OriginalHeight: " + image.getOriginalHeight());
    System.out.println("FileName: " + image.getFileName());
    System.out.println("LastModifiedTime: " + image.getLastModifiedTime());
    System.out.println();
}
```

छवियों की सूची और प्रत्येक छवि के लिए चौड़ाई, ऊंचाई, मूल आयाम, फ़ाइल नाम और अंतिम संशोधित समय जैसे प्रिंट विवरण के माध्यम से पुनरावृत्त करें।

## निष्कर्ष

इस ट्यूटोरियल में उल्लिखित चरणों का पालन करके, आप जावा लाइब्रेरी के लिए Aspose.Note की सहायता से जावा का उपयोग करके OneNote दस्तावेज़ों से छवि जानकारी को प्रभावी ढंग से पुनर्प्राप्त कर सकते हैं। इस कार्यक्षमता को अपने अनुप्रयोगों में एकीकृत करने से दस्तावेज़ प्रसंस्करण, दक्षता और उत्पादकता बढ़ाने से संबंधित कार्य स्वचालित हो सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Java के लिए Aspose.Note OneNote के अलावा अन्य दस्तावेज़ प्रारूपों को संभाल सकता है?

A1: हाँ, Java के लिए Aspose.Note OneNote, PDF और Microsoft Word सहित विभिन्न दस्तावेज़ स्वरूपों का समर्थन करता है।

### Q2: क्या जावा के लिए Aspose.Note व्यक्तिगत और व्यावसायिक उपयोग दोनों के लिए उपयुक्त है?

A2: हाँ, आप व्यक्तिगत और व्यावसायिक दोनों उद्देश्यों के लिए Java के लिए Aspose.Note का उपयोग कर सकते हैं।

### Q3: क्या जावा के लिए Aspose.Note तकनीकी सहायता प्रदान करता है?

 उ3: हाँ, तकनीकी सहायता Aspose फ़ोरम के माध्यम से उपलब्ध है[यहाँ](https://forum.aspose.com/c/note/28).

### Q4: क्या मैं खरीदारी करने से पहले जावा के लिए Aspose.Note आज़मा सकता हूँ?

 उ4: हां, आप जावा के लिए Aspose.Note का निःशुल्क परीक्षण संस्करण देख सकते हैं[जावा के लिए Aspose.Note](https://releases.aspose.com/note/java/).

### Q5: मैं जावा के लिए Aspose.Note के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?
 
 A5: आप यहां से अस्थायी लाइसेंस प्राप्त कर सकते हैं[अस्थायी लाइसेंस/](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
