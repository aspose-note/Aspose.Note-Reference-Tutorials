---
title: OneNote में नोटबुक को चपटी छवि में कनवर्ट करें - Aspose.Note
linktitle: OneNote में नोटबुक को चपटी छवि में कनवर्ट करें - Aspose.Note
second_title: Aspose.नोट जावा एपीआई
description: जावा के लिए Aspose.Note का उपयोग करके OneNote में नोटबुक को एक चपटी छवि में बदलने का तरीका जानें। सभी तत्वों को एक ही छवि फ़ाइल में सहजता से सुरक्षित रखें।
weight: 13
url: /hi/java/onenote-notebook-operations/convert-notebook-to-flattened-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote में नोटबुक को चपटी छवि में कनवर्ट करें - Aspose.Note

## परिचय

इस ट्यूटोरियल में, हम जावा के लिए Aspose.Note का उपयोग करके OneNote में एक नोटबुक को एक चपटी छवि में परिवर्तित करने की प्रक्रिया के बारे में आपका मार्गदर्शन करेंगे। यह आपको अपनी नोटबुक को एक छवि फ़ाइल के रूप में सहेजने की अनुमति देता है, यह सुनिश्चित करते हुए कि सभी तत्व एक ही छवि प्रारूप में संरक्षित हैं।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

1. आपके सिस्टम पर जावा डेवलपमेंट किट (जेडीके) स्थापित है।
2.  जावा लाइब्रेरी के लिए Aspose.Note डाउनलोड करें और अपने जावा प्रोजेक्ट में सेट करें। आप यहां से लाइब्रेरी डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/note/java/).
3. जावा प्रोग्रामिंग का बुनियादी ज्ञान।

## पैकेज आयात करें

आरंभ करने के लिए, आपको जावा के लिए Aspose.Note से आवश्यक पैकेज आयात करने होंगे:

```java
import java.io.IOException;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## चरण 1: दस्तावेज़ निर्देशिका सेट करें

सबसे पहले, उस निर्देशिका को परिभाषित करें जहां आपकी नोटबुक फ़ाइल स्थित है:

```java
String dataDir = "Your Document Directory";
```

 प्रतिस्थापित करें`"Your Document Directory"` आपकी नोटबुक फ़ाइल के पथ के साथ।

## चरण 2: नोटबुक लोड करें

 इसके बाद, का उपयोग करके नोटबुक फ़ाइल लोड करें`Notebook` कक्षा:

```java
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

 प्रतिस्थापित करना सुनिश्चित करें`"test.onetoc2"` आपकी नोटबुक फ़ाइल के नाम के साथ.

## चरण 3: छवि सहेजें विकल्प सेट करें

अब, नोटबुक को एक छवि के रूप में सहेजने के लिए विकल्प सेट करें। हम सेव फॉर्मेट को पीएनजी के रूप में निर्दिष्ट करेंगे और रिज़ॉल्यूशन को 400 डीपीआई पर सेट करेंगे:

```java
NotebookImageSaveOptions saveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
ImageSaveOptions documentSaveOptions = saveOptions.getDocumentSaveOptions();
documentSaveOptions.setResolution(400);
```

आप अपनी आवश्यकताओं के अनुसार रिज़ॉल्यूशन को समायोजित कर सकते हैं।

## चरण 4: नोटबुक को समतल करें

यह सुनिश्चित करने के लिए कि सभी तत्व एक ही छवि में समतल हो गए हैं, सेट करें`flatten` का विकल्प`true`:

```java
saveOptions.setFlatten(true);
```

यह सुनिश्चित करता है कि परिणामी छवि आपकी नोटबुक के लेआउट को बनाए रखती है।

## चरण 5: छवि सहेजें

अंत में, नोटबुक को एक चपटी छवि के रूप में सहेजें:

```java
notebook.save(dataDir + "ExportImageasFlattenedNotebook_out.png", saveOptions);
```

 प्रतिस्थापित करें`"ExportImageasFlattenedNotebook_out.png"` आपके इच्छित आउटपुट फ़ाइल नाम के साथ।

## निष्कर्ष

अंत में, जावा के लिए Aspose.Note का उपयोग करके, आप आसानी से अपनी नोटबुक को OneNote में एक चपटी छवि में परिवर्तित कर सकते हैं। यह प्रक्रिया सुनिश्चित करती है कि सभी तत्व एक ही छवि प्रारूप में संरक्षित हैं, जिससे साझा करना और देखना आसान हो जाता है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं आउटपुट छवि के रिज़ॉल्यूशन को समायोजित कर सकता हूँ?

 A1: हाँ, आप अपनी आवश्यकताओं के अनुसार रिज़ॉल्यूशन को संशोधित करके समायोजित कर सकते हैं`setResolution` विधि पैरामीटर.

### Q2: क्या Aspose.Note निर्यात के लिए अन्य छवि प्रारूपों का समर्थन करता है?

A2: हाँ, Aspose.Note नोटबुक निर्यात करने के लिए विभिन्न छवि प्रारूपों जैसे PNG, JPEG, BMP, आदि का समर्थन करता है।

### Q3: क्या मैं आउटपुट छवि को और अधिक अनुकूलित कर सकता हूँ?

A3: हाँ, Aspose.Note पेज आकार, ओरिएंटेशन और गुणवत्ता सेटिंग्स सहित आउटपुट छवि को अनुकूलित करने के लिए व्यापक विकल्प प्रदान करता है।

### Q4: क्या Java के लिए Aspose.Note का कोई परीक्षण संस्करण उपलब्ध है?

 उ4: हाँ, आप नि:शुल्क परीक्षण संस्करण प्राप्त कर सकते हैं[यहाँ](https://releases.aspose.com/).

### Q5: मुझे जावा के लिए Aspose.Note के लिए समर्थन कहां मिल सकता है?

 A5: आप Aspose.Note फोरम पर समर्थन और संसाधन पा सकते हैं[यहाँ](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
