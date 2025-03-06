---
title: OneNote - Java में विशिष्ट पृष्ठ को PNG छवि में कनवर्ट करें
linktitle: OneNote - Java में विशिष्ट पृष्ठ को PNG छवि में कनवर्ट करें
second_title: Aspose.नोट जावा एपीआई
description: जावा के लिए Aspose.Note का उपयोग करना सीखें, OneNote पेज को PNG में परिवर्तित करना। आसान चरणों का पालन करें, दस्तावेज़ लोड करें और विकल्प सेट करें। इस कार्यक्षमता के साथ जावा ऐप्स को बेहतर बनाएं।
weight: 13
url: /hi/java/onenote-document-loading/convert-page-to-png-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote - Java में विशिष्ट पृष्ठ को PNG छवि में कनवर्ट करें

## परिचय

इस ट्यूटोरियल में, आप सीखेंगे कि OneNote दस्तावेज़ से किसी विशिष्ट पृष्ठ को PNG छवि में परिवर्तित करने के लिए Java के लिए Aspose.Note का उपयोग कैसे करें। इस कार्यक्षमता को आपके जावा एप्लिकेशन में निर्बाध रूप से एकीकृत करने में आपकी सहायता के लिए हम इस प्रक्रिया को आसान-से-पालन करने योग्य चरणों में विभाजित करेंगे।

## आवश्यक शर्तें

आरंभ करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

1. जावा डेवलपमेंट किट (जेडीके): सुनिश्चित करें कि आपके सिस्टम पर जेडीके स्थापित है।
2.  जावा लाइब्रेरी के लिए Aspose.Note: जावा लाइब्रेरी के लिए Aspose.Note को डाउनलोड और इंस्टॉल करें[वेबसाइट](https://releases.aspose.com/note/java/).
3. OneNote दस्तावेज़: एक OneNote दस्तावेज़ तैयार रखें जिससे आप एक विशिष्ट पृष्ठ को PNG में कनवर्ट करना चाहते हैं।

## पैकेज आयात करें

सबसे पहले, आपको अपनी जावा फ़ाइल में आवश्यक पैकेज आयात करने होंगे:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.LoadOptions;
import com.aspose.note.SaveFormat;
```

## चरण 1: OneNote दस्तावेज़ लोड करें

```java
// दस्तावेज़ को Aspose.Note में लोड करें।
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", new LoadOptions());
```

 इस चरण में, हम Aspose.Note का उपयोग करके OneNote दस्तावेज़ लोड करते हैं`Document` कक्षा।

## चरण 2: ImageSaveOptions ऑब्जेक्ट को आरंभ करें

```java
// ImageSaveOptions ऑब्जेक्ट को प्रारंभ करें
ImageSaveOptions opts = new ImageSaveOptions(SaveFormat.Png);
```

 यहां, हम एक प्रारंभ करते हैं`ImageSaveOptions` ऑब्जेक्ट बनाएं और सेव फॉर्मेट को पीएनजी के रूप में निर्दिष्ट करें।

## चरण 3: पेज इंडेक्स सेट करें

```java
// पेज इंडेक्स सेट करें
opts.setPageIndex(0);
```

उस पेज का इंडेक्स सेट करें जिसे आप कनवर्ट करना चाहते हैं। ध्यान दें कि पेज इंडेक्सिंग 0 से शुरू होती है।

## चरण 4: दस्तावेज़ को पीएनजी के रूप में सहेजें

```java
// दस्तावेज़ को पीएनजी के रूप में सहेजें।
oneFile.save(dataDir + "ConvertSpecificPageToPngImage_out.png", opts);
```

अंत में, दस्तावेज़ को निर्दिष्ट पृष्ठ के साथ पीएनजी छवि में परिवर्तित करके सहेजें।

## निष्कर्ष

बधाई हो! आपने जावा के लिए Aspose.Note का उपयोग करके OneNote दस्तावेज़ से किसी विशिष्ट पृष्ठ को PNG छवि में परिवर्तित करने का तरीका सफलतापूर्वक सीख लिया है। इस कार्यक्षमता को अपने जावा अनुप्रयोगों में एकीकृत करने से आप OneNote दस्तावेज़ों को प्रोग्रामेटिक रूप से हेरफेर करने, अपनी उत्पादकता बढ़ाने और अपने सॉफ़्टवेयर की क्षमताओं का विस्तार करने में सशक्त होंगे।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं जावा के लिए Aspose.Note का उपयोग करके एक बार में कई पृष्ठों को PNG छवियों में परिवर्तित कर सकता हूँ?

A1: हाँ, आप पृष्ठों को पुनरावृत्त करके और उन्हें व्यक्तिगत रूप से सहेजकर बैच रूपांतरण प्राप्त कर सकते हैं।

### Q2: क्या जावा के लिए Aspose.Note पीएनजी के अलावा अन्य छवि प्रारूपों का समर्थन करता है?

A2: हाँ, Aspose.Note JPEG, GIF, BMP और TIFF जैसे विभिन्न छवि प्रारूपों का समर्थन करता है।

### Q3: क्या Java के लिए Aspose.Note का निःशुल्क परीक्षण उपलब्ध है?

 उ3: हाँ, आप नि:शुल्क परीक्षण का उपयोग कर सकते हैं[वेबसाइट](https://releases.aspose.com/).

### Q4: यदि मुझे जावा के लिए Aspose.Note के साथ कोई समस्या आती है तो क्या मुझे तकनीकी सहायता मिल सकती है?

 A4: बिल्कुल, आप Aspose सामुदायिक मंच से समर्थन मांग सकते हैं[यहाँ](https://forum.aspose.com/c/note/28).

### Q5: मैं जावा के लिए Aspose.Note का लाइसेंस कहां से खरीद सकता हूं?

 A5: आप यहां से लाइसेंस खरीद सकते हैं[खरीद पृष्ठ](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
