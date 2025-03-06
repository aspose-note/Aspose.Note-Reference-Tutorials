---
title: OneNote दस्तावेज़ को छवि में कनवर्ट करें - जावा
linktitle: OneNote दस्तावेज़ को छवि में कनवर्ट करें - जावा
second_title: Aspose.नोट जावा एपीआई
description: Java के लिए Aspose.Note का उपयोग करके OneNote को छवि में परिवर्तित करना सीखें। आसान चरणों का पालन करें, दस्तावेज़ लोड करें, विकल्पों को आरंभ करें और पीएनजी के रूप में सहेजें।
weight: 14
url: /hi/java/onenote-document-loading/convert-to-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote दस्तावेज़ को छवि में कनवर्ट करें - जावा

## परिचय

इस ट्यूटोरियल में, हम OneNote दस्तावेज़ को एक छवि में परिवर्तित करने के लिए Java के लिए Aspose.Note का उपयोग करने की प्रक्रिया में आपका मार्गदर्शन करेंगे। हम प्रत्येक चरण को पालन करने में आसान निर्देशों में विभाजित करेंगे।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

1. आपके सिस्टम पर जावा डेवलपमेंट किट (जेडीके) स्थापित है।
2.  जावा लाइब्रेरी के लिए Aspose.Note। आप इसे यहां से डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/note/java/).

## पैकेज आयात करें

सबसे पहले, अपने जावा कोड में आवश्यक पैकेज आयात करें:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

आइए अब दिए गए उदाहरण कोड को कई चरणों में तोड़ें:

## चरण 1: दस्तावेज़ निर्देशिका स्थापित करें

उस निर्देशिका को परिभाषित करें जहाँ आपका OneNote दस्तावेज़ स्थित है:

```java
String dataDir = "Your Document Directory";
```

 प्रतिस्थापित करें`"Your Document Directory"` आपके OneNote दस्तावेज़ के पथ के साथ।

## चरण 2: दस्तावेज़ लोड करें

OneNote दस्तावेज़ को Aspose.Note में लोड करें:

```java
Document oneFile = new Document(dataDir + "Sample1.one");
```

 सुनिश्चित करना`"Sample1.one"` आपके OneNote दस्तावेज़ फ़ाइल के नाम से मेल खाता है।

## चरण 3: ImageSaveOptions को आरंभ करें

 को आरंभ करें`ImageSaveOptions` सहेजें प्रारूप को निर्दिष्ट करने के लिए ऑब्जेक्ट:

```java
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
```

यहां, हम दस्तावेज़ को पीएनजी छवि के रूप में सहेज रहे हैं। यदि आवश्यक हो तो आप JPEG या BMP जैसे अन्य प्रारूप चुन सकते हैं।

## चरण 4: दस्तावेज़ को छवि के रूप में सहेजें

लोड किए गए दस्तावेज़ को छवि के रूप में सहेजें:

```java
oneFile.save(dataDir + "ConvertToImage_out.png", options);
```

यह पंक्ति निर्दिष्ट विकल्पों के साथ दस्तावेज़ को पीएनजी छवि के रूप में सहेजती है।

## चरण 5: पुष्टिकरण प्रिंट करें

यह पुष्टि करने के लिए एक संदेश प्रिंट करें कि फ़ाइल सहेजी गई है:

```java
System.out.println("File saved: " + dataDir + "ConvertToImage_out.png");
```

यह पंक्ति आपको सफल रूपांतरण और सहेजी गई छवि फ़ाइल के स्थान के बारे में सूचित करती है।

## निष्कर्ष

ऊपर बताए गए चरणों का पालन करके, आप जावा के लिए Aspose.Note का उपयोग करके आसानी से OneNote दस्तावेज़ को एक छवि में परिवर्तित कर सकते हैं। यह आपके जावा अनुप्रयोगों में दस्तावेज़ रूपांतरणों को संभालने का एक सरल और प्रभावी तरीका है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं एक ही बार में अनेक OneNote दस्तावेज़ों को परिवर्तित कर सकता हूँ?

A1: हाँ, आप दस्तावेज़ों की सूची के माध्यम से लूप कर सकते हैं और प्रत्येक दस्तावेज़ के लिए रूपांतरण ऑपरेशन कर सकते हैं।

### Q2: क्या Aspose.Note छवियों के अलावा अन्य आउटपुट स्वरूपों का समर्थन करता है?

A2: हाँ, Aspose.Note विभिन्न आउटपुट स्वरूपों जैसे PDF, HTML और Microsoft Word स्वरूपों का समर्थन करता है।

### Q3: क्या Aspose.Note OneNote फ़ाइलों के सभी संस्करणों के साथ संगत है?

A3: Aspose.Note Microsoft OneNote के विभिन्न संस्करणों में बनाई गई OneNote फ़ाइलों के साथ संगतता प्रदान करता है।

### Q4: क्या मैं आउटपुट छवियों के रिज़ॉल्यूशन को अनुकूलित कर सकता हूँ?

A4: हाँ, आप Aspose.Note में उपलब्ध विकल्पों का उपयोग करके रिज़ॉल्यूशन और अन्य मापदंडों को समायोजित कर सकते हैं।

### Q5: क्या Aspose.Note को दस्तावेज़ रूपांतरण के लिए इंटरनेट कनेक्टिविटी की आवश्यकता है?

A5: नहीं, Aspose.Note इंटरनेट कनेक्शन की आवश्यकता के बिना स्थानीय रूप से संचालित होता है।
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
