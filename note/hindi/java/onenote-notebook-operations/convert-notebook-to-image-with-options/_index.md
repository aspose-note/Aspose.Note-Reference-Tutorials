---
title: OneNote में विकल्पों के साथ नोटबुक को छवि में बदलें - Aspose.Note
linktitle: OneNote में विकल्पों के साथ नोटबुक को छवि में बदलें - Aspose.Note
second_title: Aspose.नोट जावा एपीआई
description: जावा के लिए Aspose.Note का उपयोग करके विकल्पों के साथ नोटबुक को छवि में परिवर्तित करना सीखें। अपने जावा अनुप्रयोगों में निर्बाध एकीकरण के लिए हमारे चरण-दर-चरण ट्यूटोरियल का पालन करें।
weight: 14
url: /hi/java/onenote-notebook-operations/convert-notebook-to-image-with-options/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote में विकल्पों के साथ नोटबुक को छवि में बदलें - Aspose.Note

## परिचय

इस ट्यूटोरियल में, हम जावा के लिए Aspose.Note का उपयोग करके विभिन्न विकल्पों के साथ एक नोटबुक को एक छवि में परिवर्तित करने की प्रक्रिया के बारे में विस्तार से जानेंगे। Aspose.Note एक शक्तिशाली जावा एपीआई है जो डेवलपर्स को Microsoft OneNote फ़ाइलों के साथ प्रोग्रामेटिक रूप से काम करने में सक्षम बनाता है, जिससे उनके जावा अनुप्रयोगों में निर्बाध एकीकरण की अनुमति मिलती है।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

1. जावा डेवलपमेंट किट (जेडीके): सुनिश्चित करें कि आपके सिस्टम पर जेडीके स्थापित है।
2. जावा JAR फ़ाइलों के लिए Aspose.Note: जावा लाइब्रेरी के लिए Aspose.Note डाउनलोड करें[यहाँ](https://releases.aspose.com/note/java/) और इसे अपने प्रोजेक्ट के क्लासपाथ में शामिल करें।

## पैकेज आयात करें

सबसे पहले, आइए अपने जावा एप्लिकेशन के लिए आवश्यक पैकेज आयात करें:

```java
import java.io.IOException;

import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## चरण 1: नोटबुक लोड करें

आरंभ करने के लिए, हमें OneNote नोटबुक को लोड करना होगा जिसे हम एक छवि में परिवर्तित करना चाहते हैं।

```java
String dataDir = "Your Document Directory";
// OneNote नोटबुक लोड करें
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

## चरण 2: सहेजें विकल्प सेट करें

इसके बाद, हम वांछित प्रारूप (पीएनजी, जेपीईजी, आदि) और रिज़ॉल्यूशन सहित छवि सहेजने के विकल्पों को परिभाषित करेंगे।

```java
NotebookImageSaveOptions notebookSaveOptions = new NotebookImageSaveOptions(SaveFormat.Png);

ImageSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();

documentSaveOptions.setResolution(400);
```

## चरण 3: नोटबुक को छवि के रूप में सहेजें

अब, हम निर्दिष्ट विकल्पों के साथ नोटबुक को एक छवि के रूप में सहेजेंगे।

```java
dataDir = dataDir + "ExportNotebooktoImagewithOptions_out.png";

// नोटबुक सहेजें
notebook.save(dataDir, notebookSaveOptions);
```

## निष्कर्ष

इस ट्यूटोरियल में, हमने सीखा कि जावा के लिए Aspose.Note का उपयोग करके विभिन्न विकल्पों के साथ एक नोटबुक को एक छवि में कैसे परिवर्तित किया जाए। इन चरणों का पालन करके, आप इस कार्यक्षमता को अपने जावा अनुप्रयोगों में निर्बाध रूप से एकीकृत कर सकते हैं, जिससे OneNote फ़ाइलों को प्रोग्रामेटिक रूप से हेरफेर करने की संभावनाएं खुल जाती हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Aspose.Note जटिल OneNote फ़ाइलों को संभाल सकता है?

A1: हाँ, Aspose.Note जटिल OneNote फ़ाइलों को कुशलता से संभाल सकता है, जिससे आप प्रोग्रामेटिक रूप से उन पर विभिन्न ऑपरेशन कर सकते हैं।

### Q2: क्या जावा के लिए Aspose.Note को मौजूदा परियोजनाओं में एकीकृत करना आसान है?

ए2: बिल्कुल! जावा के लिए Aspose.Note एक सीधा एपीआई प्रदान करता है जिसे आपके जावा प्रोजेक्ट्स में एकीकृत करना आसान है, जिससे आपका समय और प्रयास बचता है।

### Q3: क्या मैं नोटबुक परिवर्तित करते समय छवि आउटपुट को अनुकूलित कर सकता हूँ?

A3: हाँ, Aspose.Note आपको रिज़ॉल्यूशन, प्रारूप और अधिक जैसे विकल्पों को निर्दिष्ट करके छवि आउटपुट को अनुकूलित करने की अनुमति देता है।

### Q4: क्या Aspose.Note डेवलपर्स के लिए समर्थन प्रदान करता है?

A4: हाँ, Aspose डेवलपर्स को उनके फ़ोरम और दस्तावेज़ीकरण के माध्यम से उत्कृष्ट समर्थन प्रदान करता है, जिससे सुचारू एकीकरण और समस्या निवारण सुनिश्चित होता है।

### Q5: क्या Java के लिए Aspose.Note का कोई निःशुल्क परीक्षण उपलब्ध है?

 A5: हाँ, आप Java के लिए Aspose.Note के निःशुल्क परीक्षण का लाभ उठा सकते हैं[यहाँ](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
