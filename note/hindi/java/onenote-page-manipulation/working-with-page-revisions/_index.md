---
title: OneNote में पृष्ठ संशोधनों के साथ कार्य करना - Aspose.Note
linktitle: OneNote में पृष्ठ संशोधनों के साथ कार्य करना - Aspose.Note
second_title: Aspose.नोट जावा एपीआई
description: जानें कि Java के लिए Aspose.Note का उपयोग करके OneNote दस्तावेज़ों में पृष्ठ संशोधन कैसे प्रबंधित करें। प्रभावी पुनरीक्षण ट्रैकिंग और सहयोग के लिए चरण-दर-चरण मार्गदर्शिका प्रदान करता है।
type: docs
weight: 21
url: /hi/java/onenote-page-manipulation/working-with-page-revisions/
---
## परिचय

नोट्स को व्यवस्थित और प्रबंधित करने के लिए OneNote एक शक्तिशाली उपकरण है, लेकिन कभी-कभी आपको परिवर्तनों को ट्रैक करने और प्रभावी ढंग से सहयोग करने के लिए संशोधनों के साथ काम करने की आवश्यकता होती है। Java के लिए Aspose.Note के साथ, आप OneNote दस्तावेज़ों में प्रोग्रामेटिक रूप से पृष्ठ संशोधनों को आसानी से प्रबंधित कर सकते हैं। यह ट्यूटोरियल चरण दर चरण प्रक्रिया में आपका मार्गदर्शन करेगा।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

### जावा विकास पर्यावरण

सुनिश्चित करें कि आपके सिस्टम पर जावा डेवलपमेंट किट (जेडीके) स्थापित है।

### जावा लाइब्रेरी के लिए Aspose.Note

जावा लाइब्रेरी के लिए Aspose.Note को डाउनलोड और इंस्टॉल करें[यहाँ](https://releases.aspose.com/note/java/).

### वननोट दस्तावेज़

परीक्षण उद्देश्यों के लिए एक नमूना OneNote दस्तावेज़ तैयार रखें।

## पैकेज आयात करें

अपने जावा प्रोजेक्ट में, जावा के लिए Aspose.Note के साथ काम करने के लिए आवश्यक पैकेज आयात करें।

```java
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.RevisionSummary;
import java.io.IOException;
import java.util.Calendar;
```

आइए स्पष्ट समझ के लिए दिए गए उदाहरण को कई चरणों में तोड़ें।

## चरण 1: OneNote दस्तावेज़ लोड करें

सबसे पहले, OneNote दस्तावेज़ लोड करें और पहला चाइल्ड पेज प्राप्त करें।

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
Page page = document.getFirstChild();
```

## चरण 2: पृष्ठ संशोधन सारांश पढ़ें

पृष्ठ के लिए सामग्री संशोधन सारांश पढ़ें.

```java
RevisionSummary pageRevisionInfo = page.getPageContentRevisionSummary();
System.out.println(String.format("Author:\t%s\nModified:\t%s",
        pageRevisionInfo.getAuthorMostRecent(),
        pageRevisionInfo.getLastModifiedTime().toString()));
```

## चरण 3: पृष्ठ संशोधन सारांश अद्यतन करें

नए लेखक और संशोधित तिथि के साथ पृष्ठ संशोधन सारांश को अपडेट करें।

```java
pageRevisionInfo.setAuthorMostRecent("New Author");
Calendar modifiedDate = Calendar.getInstance();
pageRevisionInfo.setLastModifiedTime(modifiedDate.getTime());
document.save(dataDir + "WorkingWithPageRevisions_out.one");
```

## निष्कर्ष

OneNote दस्तावेज़ों में पृष्ठ संशोधनों को प्रोग्रामेटिक रूप से प्रबंधित करना Java के लिए Aspose.Note के साथ सरल बनाया जा सकता है। इस ट्यूटोरियल में बताए गए चरणों का पालन करके, आप परिवर्तनों को ट्रैक करने और निर्बाध रूप से सहयोग करने के लिए पृष्ठ संशोधनों के साथ प्रभावी ढंग से काम कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं अन्य जावा लाइब्रेरीज़ के साथ जावा के लिए Aspose.Note का उपयोग कर सकता हूँ?

उत्तर: हाँ, जावा के लिए Aspose.Note को कार्यक्षमता बढ़ाने के लिए अन्य जावा लाइब्रेरी के साथ एकीकृत किया जा सकता है।

### Q2: क्या Java के लिए Aspose.Note OneNote दस्तावेज़ों के सभी संस्करणों का समर्थन करता है?

उ: Java के लिए Aspose.Note पुराने संस्करणों सहित OneNote दस्तावेज़ों के विभिन्न संस्करणों का समर्थन करता है।

### Q3: क्या जावा के लिए Aspose.Note एंटरप्राइज़-स्तरीय अनुप्रयोगों के लिए उपयुक्त है?

उत्तर: बिल्कुल, जावा के लिए Aspose.Note को मजबूत सुविधाओं और स्केलेबिलिटी के साथ एंटरप्राइज़-स्तरीय अनुप्रयोगों की जरूरतों को पूरा करने के लिए डिज़ाइन किया गया है।

### Q4: क्या मैं जावा के लिए Aspose.Note के साथ पृष्ठ संशोधनों को अनुकूलित कर सकता हूँ?

उत्तर: हाँ, आप Java के लिए Aspose.Note का उपयोग करके अपनी आवश्यकताओं के अनुसार पृष्ठ संशोधनों को अनुकूलित कर सकते हैं।

### Q5: जावा के लिए Aspose.Note के लिए मुझे समर्थन कहां से मिल सकता है?

 उ: आप जावा के लिए Aspose.Note के लिए समर्थन प्राप्त कर सकते हैं[Aspose.नोट फोरम](https://forum.aspose.com/c/note/28).