---
date: 2025-12-20
description: जावा के साथ Aspose.Note लाइब्रेरी का उपयोग करके OneNote को PDF के रूप
  में सहेजना और OneNote में हाइपरलिंक जोड़ना सीखें। OneNote से आसानी से PDF बनाएं।
linktitle: Save OneNote as PDF and Add Hyperlink in OneNote with Java
second_title: Aspose.Note Java API
title: OneNote को PDF के रूप में सहेजें और Java के साथ OneNote में हाइपरलिंक जोड़ें
url: /hi/java/onenote-hyperlinks-images/add-hyperlink/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java के साथ OneNote को PDF के रूप में बचाएं और OneNote में हाइपरलिंक जोड़ें

## परिचय

अपने OneNote डॉक्यूमेंट्स में हाइपरलिंक जोड़ना और साथ ही उन्हें PDF के रूप में बचाएं, आपके नोट्स की कनेक्टिविटी को काफी बढ़ा सकता है और शेयरिंग को आसान बना सकता है। इस ट्यूटोरियल में आप **OneNote को PDF के रूप में कैसे बचाएं** और Java तथा Aspose.Note लाइब्रेरी का इस्तेमाल करके क्लिक करने योग्य लिंक एम्बेड करना सिखाएं। भरोसेमंद साथ में चरणों को देखते हैं!

## क्विक आंसर्स
- **क्या मैं Java के साथ OneNote को PDF के रूप में बचाएं हूँ?** हाँ, Aspose.Note for Java एक ही `save` कॉल से PDF बनाता है।

- **हाइपरलिंक कैसे एम्बेड करें?** `RichText` को बदलें पर `TextStyle.setHyperlinkAddress` का इस्तेमाल करें।

- **पूर्वापेक्षाएँ क्या हैं?** JDK 8+ और Aspose.Note for Java लाइब्रेरी।
- **कौन से आउटपुट फॉर्मेट समर्थित हैं?** PDF, DOCX, XPS, और अधिक।

- **प्रोडक्शन के लिए लाइसेंस आवश्यक है?** हाँ, गैर-इवैल्यूएशन उपयोग के लिए एक आउटपुट लाइसेंस आवश्यक है।

## “save onenote as pdf” क्या है?

OneNote नोटबुक को PDF के रूप में सहेजने से आपके नोट्स का एक पोर्टेबल, केवल-पढ़ने योग्य संस्करण बनता है जिसे किसी भी डिवाइस पर OneNote ऐप के बिना खोला जा सकता है। यह विशेष रूप से आर्काइविंग, प्रिंटिंग, या उन उपयोगकर्ताओं के साथ शेयर करने के लिए उपयोगी है जिनके पास OneNote नहीं है।

## Aspose.Note Java के साथ OneNote से PDF क्यों जेनरेट करें?

- **पूर्ण सिंक्रनाइज़ेशन:** फॉर्मेटिंग, इमेज़ और हाइपरलिंक को निरंतर रखता है।

- **प्रोग्रामेटिक कंट्रोल:** बैकएंड सर्विसेज़ में बैच कन्वर्ज़न को ऑटोमेट करें।

- **क्रॉस-प्लेटफ़ॉर्म:** Windows, Linux, और macOS पर काम करता है।
- **रिच API:** लिंक करने से पहले सामग्री को आसानी से जोड़ें या कॉन्फ़िगर करें।

## ज़रूरी शर्तें

शुरू करने से पहले, पक्का करें कि आपके सिस्टम पर ये ज़रूरी शर्तें इंस्टॉल और सेट अप हैं:

### Java Development Kit (JDK)

पक्का करें कि आपके सिस्टम पर Java Development Kit (JDK) इंस्टॉल है। आप [Oracle वेबसाइट](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) से JDK डाउनलोड और इंस्टॉल कर सकते हैं।

### Aspose.Note for Java लाइब्रेरी

Aspose.Note for Java लाइब्रेरी डाउनलोड और इंस्टॉल करें। आप डॉक्यूमेंटेशन और डाउनलोड लिंक [यहां](https://reference.aspose.com/note/java/) पा सकते हैं।

## पैकेज इंपोर्ट करें

शुरू करने के लिए, Aspose.Note for Java के साथ काम करने के लिए ज़रूरी पैकेज इंपोर्ट करें।

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

अब, दिए गए उदाहरण को कई स्टेप्स में समझते हैं:

## स्टेप 1: डॉक्यूमेंट स्ट्रक्चर सेट अप करें

सबसे पहले, एक नया डॉक्यूमेंट और एक पेज बनाएं जहां कंटेंट रहेगा।

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
Title title = new Title();
```

## स्टेप 2: डिफ़ॉल्ट टेक्स्ट स्टाइल तय करें

एक डिफ़ॉल्ट पैराग्राफ़ स्टाइल तय करें जो ज़्यादातर टेक्स्ट एलिमेंट्स पर लागू होगा।

```java
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                            .setFontName("Arial")
                                            .setFontSize(10)
                                            .setFontColor(java.awt.Color.GRAY);
```

## स्टेप 3: टाइटल टेक्स्ट सेट करें

पेज के लिए एक टाइटल बनाएं और डिफ़ॉल्ट स्टाइल लागू करें।

```java
RichText titleText = new RichText().append("Title");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
page.setTitle(title);
```

## स्टेप 4: आउटलाइन और आउटलाइन एलिमेंट्स बनाएं

आउटलाइन पैराग्राफ़ और दूसरे एलिमेंट्स के लिए कंटेनर की तरह काम करते हैं।

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## स्टेप 5: हाइपरलिंक के लिए टेक्स्ट स्टाइल तय करें

यहां हम एक लाल रंग का स्टाइल तय करते हैं जिसका इस्तेमाल क्लिक करने वाले हिस्से के लिए किया जाएगा।

```java
TextStyle textStyleRed = new TextStyle()
                                    .setFontName("Arial")
                                    .setFontSize(10)
                                    .setFontColor(java.awt.Color.red);
```

## स्टेप 6: हाइपरलिंक के साथ टेक्स्ट जोड़ें

अब हम एक `RichText` ऑब्जेक्ट बनाते हैं जो नॉर्मल टेक्स्ट और हाइपरलिंक को मिलाता है।

`setHyperlinkAddress` मेथड Aspose.Note को बताता है कि यह सेगमेंट क्लिक करने लायक होना चाहिए।

```java
RichText text = new RichText()
                            .append("This is ", textStyleRed)
                            .append("hyperlink", new TextStyle().setHyperlinkAddress("https://www.google.com"))
                            .append(". This text is not a hyperlink.", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
outlineElem.appendChildLast(text);
```

## स्टेप 7: पेज में आउटलाइन और डॉक्यूमेंट में पेज जोड़ें

आउटलाइन एलिमेंट को आउटलाइन से, आउटलाइन को पेज से, और आखिर में पेज को डॉक्यूमेंट से अटैच करें।

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## स्टेप 8: डॉक्यूमेंट को PDF के तौर पर सेव करें

आखिरी स्टेप OneNote डॉक्यूमेंट को PDF फ़ाइल के तौर पर सेव करना है। यहीं पर प्राइमरी कीवर्ड **save onenote as pdf** काम आता है।

```java
doc.save(dataDir + "AddHyperlink_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "AddHyperlink_out.pdf");
```

## निष्कर्ष

बधाई हो! आपने सफलतापूर्वक **OneNote को PDF के रूप में सहेजा** और Java तथा Aspose.Note लाइब्रेरी का उपयोग करके डॉक्यूमेंट में हाइपरलिंक जोड़ा। यह क्षमता आपको सीधे अपने OneNote सामग्री से लिंक, शेयर करने योग्य PDF बनाती है।

## अक्सर पूछे जाने वाले प्रश्न

**प्रश्न: हाइपरलिंक की उपस्थिति को कैसे कस्टमाइज़ करूँ?**  
उत्तर: `setHyperlinkAddress` कॉल करने से पहले `TextStyle` प्रॉपर्टीज़ जैसे `setFontColor`, `setUnderline`, या `setFontName` का उपयोग करें।

**प्रश्न: क्या मैं डॉक्यूमेंट को PDF के अलावा अन्य फॉर्मेट में सहेज सकता हूँ?**  
उत्तर: हाँ, Aspose.Note DOCX, XPS, HTML, और कई अन्य एक्सपोर्ट फॉर्मेट का समर्थन करता है।

**प्रश्न: यदि मुझे मौजूदा OneNote फ़ाइल में हाइपरलिंक जोड़ना हो तो क्या करें?**  
उत्तर: मौजूदा फ़ाइल को `new Document("input.one")` से लोड करें, दिखाए अनुसार सामग्री संशोधित करें, और फिर इच्छित फॉर्मेट के साथ `save` कॉल करें।

**प्रश्न: क्या PDF जनरेट होने के बाद हाइपरलिंक को प्रोग्रामेटिकली खोलने का कोई तरीका है?**  
उत्तर: PDF व्यूअर स्वचालित रूप से क्लिक करने योग्य लिंक को संभालेगा; अतिरिक्त कोड की आवश्यकता नहीं है।

**प्रश्न: विकास उपयोग के लिए क्या मुझे लाइसेंस चाहिए?**  
उत्तर: विकास और परीक्षण के लिए एक अस्थायी इवैल्यूएशन लाइसेंस पर्याप्त है, लेकिन प्रोडक्शन डिप्लॉयमेंट के लिए पूर्ण लाइसेंस आवश्यक है।

---

**अंतिम अपडेट:** 2025-12-20  
**टेस्टेड विथ:** Aspose.Note for Java 26.4  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}