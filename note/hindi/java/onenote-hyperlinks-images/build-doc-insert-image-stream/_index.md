---
title: दस्तावेज़ बनाएँ और OneNote - Java में स्ट्रीम के साथ छवि सम्मिलित करें
linktitle: दस्तावेज़ बनाएँ और OneNote - Java में स्ट्रीम के साथ छवि सम्मिलित करें
second_title: Aspose.नोट जावा एपीआई
description: जावा के लिए Aspose.Note का उपयोग करके OneNote दस्तावेज़ों में छवियों को आसानी से एकीकृत करने का तरीका जानें। जावा डेवलपर्स के लिए चरण-दर-चरण ट्यूटोरियल।
weight: 13
url: /hi/java/onenote-hyperlinks-images/build-doc-insert-image-stream/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# दस्तावेज़ बनाएँ और OneNote - Java में स्ट्रीम के साथ छवि सम्मिलित करें

## परिचय

दस्तावेज़ बनाने और OneNote में छवि स्ट्रीम का उपयोग करके छवियां सम्मिलित करने के लिए जावा के लिए Aspose.Note का उपयोग करने पर हमारे व्यापक ट्यूटोरियल में आपका स्वागत है! इस ट्यूटोरियल में, हम आपको चरण दर चरण प्रक्रिया के माध्यम से मार्गदर्शन करेंगे, यह सुनिश्चित करते हुए कि आपको प्रत्येक चरण की स्पष्ट समझ हो। अंत तक, आप जावा का उपयोग करके आसानी से छवियों को अपने OneNote दस्तावेज़ों में एकीकृत करने में सक्षम होंगे।

## आवश्यक शर्तें

इससे पहले कि हम ट्यूटोरियल में उतरें, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

### जावा डेवलपमेंट किट (जेडीके)

सुनिश्चित करें कि आपके सिस्टम पर जावा डेवलपमेंट किट (जेडीके) स्थापित है। आप इसे Oracle वेबसाइट से डाउनलोड कर सकते हैं।

### जावा लाइब्रेरी के लिए Aspose.Note

 दिए गए जावा लाइब्रेरी के लिए Aspose.Note को डाउनलोड और इंस्टॉल करें[जोड़ना](https://releases.aspose.com/note/java/).

### आईडीई सेटअप

जावा परियोजनाओं के साथ काम करने के लिए आवश्यक कॉन्फ़िगरेशन के साथ अपना एकीकृत विकास पर्यावरण (आईडीई) स्थापित करें।

## पैकेज आयात करें

आरंभ करने के लिए, अपने जावा प्रोजेक्ट में आवश्यक पैकेज आयात करें। ये पैकेज OneNote दस्तावेज़ों और छवियों के साथ काम करने के लिए आवश्यक कार्यक्षमता प्रदान करेंगे।

```java
import java.io.FileInputStream;
import java.io.FileNotFoundException;
import java.io.IOException;
import java.io.InputStream;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## चरण 1: दस्तावेज़ निर्देशिका सेट करें

 उस निर्देशिका को परिभाषित करें जहां आपका दस्तावेज़ और छवियां स्थित हैं। प्रतिस्थापित करें`"Your Document Directory"` आपकी निर्देशिका के पथ के साथ।

```java
String dataDir = "Your Document Directory";
```

## चरण 2: दस्तावेज़ ऑब्जेक्ट बनाएँ

 का एक उदाहरण प्रारंभ करें`Document` अपने OneNote दस्तावेज़ के साथ काम करना शुरू करने के लिए कक्षा।

```java
Document doc = new Document();
```

## चरण 3: पेज ऑब्जेक्ट को आरंभ करें

 एक बनाने के`Page` दस्तावेज़ के भीतर पृष्ठ का प्रतिनिधित्व करने के लिए ऑब्जेक्ट।

```java
Page page = new Page();
```

## चरण 4: रूपरेखा बनाएं

 एक आरंभ करें`Outline` पृष्ठ के भीतर सामग्री को संरचित करने के लिए ऑब्जेक्ट।

```java
Outline outline1 = new Outline();
outline1.setVerticalOffset(600);
outline1.setHorizontalOffset(0);
```

## चरण 5: रूपरेखा तत्व बनाएं

 एक बनाएं`OutlineElement` छवि को पकड़ने और उसकी स्थिति निर्दिष्ट करने के लिए।

```java
OutlineElement outlineElem1 = new OutlineElement();
```

## चरण 6: छवि स्ट्रीम लोड करें

 का उपयोग करके छवि स्ट्रीम लोड करें`FileInputStream` वांछित छवि के लिए.

```java
InputStream fs = null;
try {
    fs = new FileInputStream(dataDir + "image.jpg");
} catch (FileNotFoundException e) {
    e.printStackTrace();
}
```

## चरण 7: छवि सम्मिलित करें

 छवि बनाकर दस्तावेज़ में डालें`Image` ऑब्जेक्ट और उसका संरेखण सेट करना।

```java
Image image = new Image(null, dataDir + "image1.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## चरण 8: छवि को रूपरेखा तत्व में जोड़ें

छवि को रूपरेखा तत्व में जोड़ें।

```java
outlineElem1.appendChildLast(image);
```

## चरण 9: रूपरेखा तत्व को रूपरेखा में जोड़ें

रूपरेखा तत्व को रूपरेखा में जोड़ें.

```java
outline1.appendChildLast(outlineElem1);
```

## चरण 10: पृष्ठ पर रूपरेखा जोड़ें

पृष्ठ पर रूपरेखा जोड़ें.

```java
page.appendChildLast(outline1);
```

## चरण 11: पृष्ठ को दस्तावेज़ में जोड़ें

अंत में, पृष्ठ को दस्तावेज़ में जोड़ें।

```java
doc.appendChildLast(page);
```

## चरण 12: दस्तावेज़ सहेजें

वांछित प्रारूप (जैसे, पीडीएफ) निर्दिष्ट करते हुए, संशोधित दस्तावेज़ सहेजें।

```java
try {
    doc.save("D://Aspose_JavaProjects//OneNote//out3.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

इन चरणों का पालन करके, आप जावा के लिए Aspose.Note का उपयोग करके OneNote में छवि स्ट्रीम का उपयोग करके आसानी से दस्तावेज़ बना सकते हैं और छवियां सम्मिलित कर सकते हैं।

## निष्कर्ष

अंत में, जावा का उपयोग करके अपने OneNote दस्तावेज़ों में छवियों के एकीकरण में महारत हासिल करने से आपकी दस्तावेज़ निर्माण प्रक्रिया में उल्लेखनीय वृद्धि हो सकती है। जावा के लिए Aspose.Note के साथ, आपके पास इस कार्य को निर्बाध रूप से पूरा करने के लिए एक शक्तिशाली उपकरण है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Java के लिए Aspose.Note OneNote के सभी संस्करणों के साथ संगत है?

A1: Java के लिए Aspose.Note OneNote के विभिन्न संस्करणों का समर्थन करता है, जो विभिन्न वातावरणों में अनुकूलता सुनिश्चित करता है।

### Q2: क्या मैं Java के लिए Aspose.Note का उपयोग करके OneNote दस्तावेज़ों में सम्मिलित छवियों के स्वरूप को अनुकूलित कर सकता हूँ?

A2: हां, आप अपनी विशिष्ट आवश्यकताओं के अनुरूप सम्मिलित छवियों के विभिन्न पहलुओं, जैसे संरेखण, आकार और अभिविन्यास को अनुकूलित कर सकते हैं।

### Q3: क्या जावा के लिए Aspose.Note पीडीएफ के अलावा अन्य दस्तावेज़ प्रारूपों के लिए समर्थन प्रदान करता है?

A3: हाँ, Java के लिए Aspose.Note DOCX, HTML और अन्य सहित दस्तावेज़ स्वरूपों की एक विस्तृत श्रृंखला का समर्थन करता है, जो आपको अपने दस्तावेज़ प्रबंधन कार्यों में लचीलापन देता है।

### Q4: जावा के लिए Aspose.Note के लिए मुझे अतिरिक्त संसाधन और समर्थन कहां मिल सकता है?

A4: आप दिए गए लिंक के माध्यम से जावा के लिए Aspose.Note के दस्तावेज़, डाउनलोड लिंक, समर्थन फ़ोरम और अस्थायी लाइसेंस तक पहुंच सकते हैं।

### Q5: क्या Java के लिए Aspose.Note का कोई परीक्षण संस्करण उपलब्ध है?

A5: हाँ, आप खरीदारी का निर्णय लेने से पहले जावा की विशेषताओं और क्षमताओं का पता लगाने के लिए Aspose.Note का निःशुल्क परीक्षण प्राप्त कर सकते हैं।

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
