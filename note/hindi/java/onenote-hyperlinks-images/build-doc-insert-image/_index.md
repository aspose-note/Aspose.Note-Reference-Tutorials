---
title: जावा का उपयोग करके OneNote में दस्तावेज़ बनाएँ और छवि सम्मिलित करें
linktitle: जावा का उपयोग करके OneNote में दस्तावेज़ बनाएँ और छवि सम्मिलित करें
second_title: Aspose.नोट जावा एपीआई
description: जावा के लिए Aspose.Note का उपयोग करके OneNote दस्तावेज़ बनाने और छवियाँ सम्मिलित करने का तरीका जानें। निर्बाध एकीकरण के लिए चरण-दर-चरण ट्यूटोरियल।
type: docs
weight: 12
url: /hi/java/onenote-hyperlinks-images/build-doc-insert-image/
---
## परिचय

इस ट्यूटोरियल में, हम देखेंगे कि OneNote दस्तावेज़ बनाने और उनमें छवियां सम्मिलित करने के लिए जावा के लिए Aspose.Note का उपयोग कैसे करें। Aspose.Note एक शक्तिशाली जावा एपीआई है जो डेवलपर्स को Microsoft OneNote फ़ाइलों के साथ प्रोग्रामेटिक रूप से काम करने में सक्षम बनाता है। प्रक्रिया में आपका मार्गदर्शन करने के लिए हम प्रत्येक चरण का विस्तार से वर्णन करेंगे।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यकताएँ हैं:

1. जावा डेवलपमेंट किट (जेडीके): सुनिश्चित करें कि आपके सिस्टम पर जेडीके स्थापित है।
2.  जावा लाइब्रेरी के लिए Aspose.Note: जावा लाइब्रेरी के लिए Aspose.Note को डाउनलोड और इंस्टॉल करें[वेबसाइट](https://releases.aspose.com/note/java/).
3. आईडीई (एकीकृत विकास पर्यावरण): कोडिंग के लिए किसी भी जावा-समर्थित आईडीई जैसे इंटेलीजे आईडीईए या एक्लिप्स का उपयोग करें।

## पैकेज आयात करें

अपने जावा कोड में आवश्यक पैकेज आयात करके प्रारंभ करें:

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

## चरण 1: दस्तावेज़ सेट करें

सबसे पहले, एक नया OneNote दस्तावेज़ बनाएं और आवश्यक ऑब्जेक्ट प्रारंभ करें:

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

## चरण 2: रूपरेखा आरंभ करें

दस्तावेज़ की रूपरेखा तैयार करें और ऑफसेट गुण निर्दिष्ट करें:

```java
Outline outline = new Outline();
outline.setVerticalOffset(0);
outline.setHorizontalOffset(0);
```

## चरण 3: छवि जोड़ें

एक छवि लोड करें और उसका संरेखण निर्दिष्ट करें:

```java
Image image = new Image(null, dataDir + "Input.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## चरण 4: रूपरेखा तत्व में छवि जोड़ें

छवि को किसी रूपरेखा तत्व से जोड़ें:

```java
OutlineElement outlineElem = new OutlineElement();
outlineElem.appendChildLast(image);
```

## चरण 5: रूपरेखा और पृष्ठ नोड्स जोड़ें

दस्तावेज़ में रूपरेखा और पृष्ठ नोड्स जोड़ें:

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## चरण 6: दस्तावेज़ सहेजें

अंत में, OneNote दस्तावेज़ सहेजें:

```java
try {
    doc.save(dataDir + "NewOneNotedocument_out", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## निष्कर्ष

बधाई हो! आपने जावा के लिए Aspose.Note का उपयोग करके OneNote दस्तावेज़ बनाना और उनमें छवियां सम्मिलित करना सफलतापूर्वक सीख लिया है। इन चरणों का पालन करके, आप अपने जावा अनुप्रयोगों में OneNote फ़ाइलों को कुशलतापूर्वक प्रबंधित और हेरफेर कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: मैं जावा के लिए Aspose.Note के लिए दस्तावेज़ कहां पा सकता हूं?

 A1: आप दस्तावेज़ तक पहुंच सकते हैं[यहाँ](https://reference.aspose.com/note/java/).

### Q2: मैं जावा के लिए Aspose.Note कैसे डाउनलोड करूं?

 A2: आप जावा के लिए Aspose.Note डाउनलोड कर सकते हैं[डाउनलोड पेज](https://releases.aspose.com/note/java/).

### Q3: क्या Java के लिए Aspose.Note का निःशुल्क परीक्षण उपलब्ध है?

 उ3: हाँ, आप नि:शुल्क परीक्षण प्राप्त कर सकते हैं[वेबसाइट](https://releases.aspose.com/).

### Q4: मुझे जावा के लिए Aspose.Note के लिए समर्थन कहां मिल सकता है?

 A4: सहायता के लिए, पर जाएँ[Aspose.नोट फोरम](https://forum.aspose.com/c/note/28).

### Q5: क्या मैं जावा के लिए Aspose.Note के लिए अस्थायी लाइसेंस प्राप्त कर सकता हूँ?

 A5: हाँ, आप अस्थायी लाइसेंस का अनुरोध कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/).
