---
title: OneNote में आउटपुट छवि रिज़ॉल्यूशन सेट करें - Aspose.Note
linktitle: OneNote में आउटपुट छवि रिज़ॉल्यूशन सेट करें - Aspose.Note
second_title: Aspose.नोट जावा एपीआई
description: जावा के लिए Aspose.Note का उपयोग करके OneNote दस्तावेज़ों में छवि रिज़ॉल्यूशन को समायोजित करना सीखें। आसान कार्यान्वयन के लिए हमारी चरण-दर-चरण मार्गदर्शिका का पालन करें
weight: 23
url: /hi/java/onenote-document-saving/set-output-image-resolution/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote में आउटपुट छवि रिज़ॉल्यूशन सेट करें - Aspose.Note

## परिचय

क्या आप जावा का उपयोग करके अपने OneNote दस्तावेज़ों में छवियों के रिज़ॉल्यूशन में हेरफेर करना चाह रहे हैं? जावा के लिए Aspose.Note ऐसे कार्यों के लिए एक मजबूत समाधान प्रदान करता है। इस ट्यूटोरियल में, हम Aspose.Note का उपयोग करके आउटपुट छवि रिज़ॉल्यूशन सेट करने के चरणों के बारे में जानेंगे।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यकताएँ हैं:

1. जावा डेवलपमेंट किट (जेडीके): अपने सिस्टम पर जेडीके इंस्टॉल करें।
2. जावा के लिए Aspose.Note: जावा के लिए Aspose.Note को डाउनलोड और इंस्टॉल करें[वेबसाइट](https://releases.aspose.com/note/java/).
3. एकीकृत विकास पर्यावरण (आईडीई): एक्लिप्स या इंटेलीजे आईडीईए जैसी अपनी पसंदीदा आईडीई चुनें।

## पैकेज आयात करें

अपने जावा प्रोजेक्ट में, आवश्यक Aspose.Note पैकेज आयात करें:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## चरण 1: OneNote दस्तावेज़ लोड करें

OneNote दस्तावेज़ को अपने Java एप्लिकेशन में लोड करके प्रारंभ करें:

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```

 प्रतिस्थापित करें`"Your Document Directory"` उस वास्तविक निर्देशिका के साथ जहां आपका OneNote दस्तावेज़ स्थित है।

## चरण 2: छवि सहेजें विकल्प सेट करें

छवि सहेजने के विकल्पों को परिभाषित करें और वांछित रिज़ॉल्यूशन निर्दिष्ट करें:

```java
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Jpeg);
imageSaveOptions.setResolution(120);
```

 यहां, हम संकल्प को इस पर सेट कर रहे हैं`120 dpi`. आप इस मान को अपनी आवश्यकताओं के अनुसार समायोजित कर सकते हैं।

## चरण 3: दस्तावेज़ को संशोधित रिज़ॉल्यूशन के साथ सहेजें

दस्तावेज़ को अद्यतन छवि रिज़ॉल्यूशन के साथ सहेजें:

```java
doc.save(dataDir + "SetOutputImageResolution_out.jpeg", imageSaveOptions);
```

यह संशोधित दस्तावेज़ को निर्दिष्ट रिज़ॉल्यूशन के साथ सहेजेगा।

## निष्कर्ष

इस ट्यूटोरियल में, हमने पता लगाया है कि जावा के लिए Aspose.Note का उपयोग करके OneNote दस्तावेज़ों में आउटपुट छवि रिज़ॉल्यूशन कैसे सेट करें। इन सरल चरणों का पालन करके, आप अपने एप्लिकेशन की आवश्यकताओं को पूरा करने के लिए छवियों के रिज़ॉल्यूशन में कुशलतापूर्वक हेरफेर कर सकते हैं।


## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं छवि रिज़ॉल्यूशन को 120 डीपीआई से अधिक मान पर समायोजित कर सकता हूँ?

A1: हाँ, आप अपनी आवश्यकताओं के अनुसार रिज़ॉल्यूशन को किसी भी वांछित मान पर सेट कर सकते हैं।

### Q2: क्या Aspose.Note JPEG के अलावा अन्य छवि प्रारूपों का समर्थन करता है?

A2: हाँ, Aspose.Note विभिन्न छवि प्रारूपों जैसे PNG, BMP, GIF, आदि का समर्थन करता है।

### Q3: क्या Aspose.Note जावा के सभी संस्करणों के साथ संगत है?

A3: Aspose.Note जावा 1.6 या बाद के संस्करणों के साथ संगत है।

### Q4: क्या मैं Aspose.Note का उपयोग करके OneNote दस्तावेज़ों में छवियों के अन्य पहलुओं में हेरफेर कर सकता हूँ?

A4: हाँ, Aspose.Note आकार बदलने, क्रॉप करने और घुमाने सहित छवि हेरफेर के लिए व्यापक सुविधाएँ प्रदान करता है।

### Q5: Aspose.Note-संबंधित प्रश्नों के लिए मुझे सहायता कहाँ से मिल सकती है?

 A5: आप Aspose.Note सामुदायिक मंच से सहायता ले सकते हैं[यहाँ](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
