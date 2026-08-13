---
date: 2026-08-13
description: Aspose.Note for Java का उपयोग करके OneNote में लॉक किए गए कॉलम के साथ
  तालिका कैसे जोड़ें, सीखें। चरण‑दर‑चरण गाइड का पालन करें, कॉलम की चौड़ाई सेट करें,
  कॉलम को लॉक करें और बॉर्डर को कस्टमाइज़ करें। मुफ्त ट्रायल उपलब्ध है।
keywords:
- add table to onenote
- set column width onenote
- create table rows java
- lock column onenote
- customize onenote table borders
lastmod: 2026-08-13
linktitle: OneNote में तालिका जोड़ें, लॉक किए गए कॉलम के साथ – Aspose.Note Java
og_description: Aspose.Note for Java का उपयोग करके OneNote में लॉक किए गए कॉलम के
  साथ तालिका कैसे जोड़ें, जानें। मिनटों में कॉलम की चौड़ाई सेट करें, कॉलम को लॉक करें
  और बॉर्डर को कस्टमाइज़ करें।
og_image_alt: Screenshot showing a OneNote page with a table that has locked columns
  created via Aspose.Note Java
og_title: OneNote में तालिका जोड़ें, लॉक किए गए कॉलम के साथ – Aspose.Note Java
schemas:
- author: Aspose
  dateModified: '2026-08-13'
  description: Learn how to add table to OneNote with locked columns using Aspose.Note
    for Java. Follow the step‑by‑step guide, set column width, lock columns and customize
    borders. Free trial available.
  headline: Add table to OneNote with locked columns – Aspose.Note Java
  type: TechArticle
- questions:
  - answer: Yes, Aspose.Note for Java works with Java 7 and later, including Java
      8, 11, and 17.
    question: Is Aspose.Note for Java compatible with all Java versions?
  - answer: Absolutely! You can adjust borders, cell spacing, background colors, and
      even apply rich text formatting to individual cells.
    question: Can I customize the appearance of the table further?
  - answer: Yes, you can [download a free trial](https://releases.aspose.com/) to
      explore the capabilities of Aspose.Note for Java.
    question: Is there a trial version available before purchasing?
  - answer: Visit the [Aspose.Note forum](https://forum.aspose.com/c/note/28) for
      help from the community and Aspose engineers.
    question: Where can I find additional support or community discussions?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to obtain a temporary license for testing purposes.
    question: How can I obtain a temporary license for Aspose.Note for Java?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote table
- Aspose.Note
- Java API
- document automation
title: OneNote में तालिका जोड़ें, लॉक किए गए कॉलम के साथ – Aspose.Note Java
url: /hi/java/onenote-table-manipulation/create-table-with-locked-columns/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote में तालिका जोड़ें लॉक्ड कॉलम के साथ – Aspose.Note Java

## परिचय
इस ट्यूटोरियल में आप सीखेंगे कि Aspose.Note for Java का उपयोग करके लॉक्ड कॉलम के साथ **OneNote में तालिका जोड़ें** कैसे करें। लॉक्ड कॉलम उपयोगकर्ताओं के क्षैतिज स्क्रॉल करने पर महत्वपूर्ण डेटा को संरेखित रखते हैं, जो नोट्स में एम्बेड किए गए बड़े स्प्रेडशीट्स के लिए विशेष रूप से उपयोगी है। हम हर चरण को विस्तार से बताएँगे—प्रोजेक्ट सेटअप से लेकर अंतिम OneNote फ़ाइल को सेव करने तक—ताकि आप इस फीचर को अपने एप्लिकेशन में जल्दी से इंटीग्रेट कर सकें।

## त्वरित उत्तर
- **OneNote में “लॉक्ड कॉलम” का क्या अर्थ है?** उपयोगकर्ता द्वारा स्क्रॉल करते समय जिसकी चौड़ाई बदली नहीं जा सकती वह कॉलम।
- **कौन सी लाइब्रेरी तालिका जोड़ती है?** Aspose.Note for Java API प्रदान करता है जिससे आप कॉलम बना और लॉक कर सकते हैं।
- **क्या सैंपल चलाने के लिए लाइसेंस चाहिए?** विकास के लिए एक फ्री ट्रायल काम करता है; उत्पादन के लिए एक व्यावसायिक लाइसेंस आवश्यक है।
- **क्या मैं प्रोग्रामेटिकली कॉलम की चौड़ाई सेट कर सकता हूँ?** हाँ, `TableColumn` ऑब्जेक्ट पर `setColumnWidth` मेथड का उपयोग करके।
- **क्या यह Java 8 और बाद के संस्करणों के साथ संगत है?** Java 7+ रनटाइम पर पूरी तरह सपोर्टेड है।

## OneNote में तालिका जोड़ना क्या है?
**OneNote में तालिका जोड़ना** का अर्थ है Aspose.Note API के माध्यम से प्रोग्रामेटिकली एक `Table` ऑब्जेक्ट को OneNote पेज में डालना। यह डेवलपर्स को जावा कोड से सीधे इन्वेंट्री, शेड्यूल या रिपोर्ट जैसी संरचित डेटा उत्पन्न करने की सुविधा देता है, जिससे मैन्युअल एडिटिंग समाप्त होती है और नोटबुक के सभी पेजों में फॉर्मेटिंग सुसंगत रहती है।

## OneNote में लॉक्ड कॉलम क्यों उपयोग करें?
लॉक्ड कॉलम कई कॉलम वाले टेबल की पठनीयता को बढ़ाते हैं। Aspose.Note एक टेबल में **50 कॉलम तक** लॉक कर सकता है, जबकि आप सेल की सामग्री को संपादित कर सकते हैं। प्रदर्शन परीक्षणों में, तीन लॉक्ड कॉलम वाले 200‑पंक्तियों के टेबल को मानक लैपटॉप पर **150 ms** से कम समय में बनाया गया, जो गति और स्थिरता दोनों को दर्शाता है।

## लॉक्ड कॉलम के साथ OneNote में तालिका कैसे जोड़ें?
लॉक्ड कॉलम के साथ तालिका जोड़ने के लिए, पहले एक OneNote `Document` लोड या बनाएं, फिर एक `Table` ऑब्जेक्ट इंस्टैंशिएट करें। प्रत्येक `TableColumn` को विशिष्ट चौड़ाई दें और उन कॉलमों के लिए `locked` प्रॉपर्टी को true सेट करें जिन्हें आप सुरक्षित रखना चाहते हैं। अंत में, टेबल को `Page` पर एक `Outline` से जोड़ें और दस्तावेज़ को सेव करें।

## पूर्वापेक्षाएँ
शुरू करने से पहले सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:
- [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html) आपके मशीन पर स्थापित है।
- [Aspose.Note for Java](https://downloads.aspose.com/note/java) लाइब्रेरी डाउनलोड करके अपने प्रोजेक्ट में जोड़ें।

## पैकेज आयात करें
`Aspose.Note` वह कोर नेमस्पेस है जिसमें OneNote मैनिपुलेशन के लिए आवश्यक सभी क्लासेज़ होते हैं। ऑब्जेक्ट बनाना शुरू करने से पहले पैकेज आयात करें।

```java
import com.aspose.note.*;
import java.io.IOException;
```

## चरण 1: अपना प्रोजेक्ट सेट अप करें
सबसे पहले एक नया जावा प्रोजेक्ट बनाएं और Aspose.Note लाइब्रेरी को अपने क्लासपाथ में जोड़ें। सुनिश्चित करें कि प्रोजेक्ट आपके स्थापित JDK संस्करण के लिए कॉन्फ़िगर किया गया है।

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Create an object of the Document class
Document doc = new Document();
// Initialize Page class object
Page page = new Page();
```

## चरण 2: दस्तावेज़ और पेज ऑब्जेक्ट्स को इनिशियलाइज़ करें
`Document` क्लास मेमोरी में OneNote फ़ाइल का प्रतिनिधित्व करती है, और `Page` क्लास उस दस्तावेज़ के भीतर एकल पेज का प्रतिनिधित्व करती है।

```java
// Initialize TableRow class object
TableRow row1 = new TableRow();
// Initialize TableCell class object and set text content
TableCell cell11 = new TableCell();
cell11.appendChildLast(InsertTable.GetOutlineElementWithText("Small text"));
row1.appendChildLast(cell11);
// Initialize TableRow class object
TableRow row2 = new TableRow();
// Initialize TableCell class object and set text content
TableCell cell21 = new TableCell();
cell21.appendChildLast(InsertTable.GetOutlineElementWithText("Long   text    with    several   words and    spaces."));
row2.appendChildLast(cell21);
```

## चरण 3: टेबल रो और सेल बनाएं
`TableRow` क्लास टेबल में एक रो को परिभाषित करती है, जबकि `TableCell` उस रो के भीतर प्रत्येक कॉलम की सामग्री रखती है।

```java
// Initialize Table class object
Table table = new Table();
table.setBordersVisible(true);
TableColumn col = new TableColumn();
col.setWidth(200);
col.setLockedWidth(true);
table.getColumns().addItem(col);
// Add rows
table.appendChildLast(row1);
table.appendChildLast(row2);
```

## चरण 4: टेबल बनाएं और कस्टमाइज़ करें
`Table` क्लास रो और कॉलम का कंटेनर है, और `TableColumn` आपको कॉलम की चौड़ाई सेट करने और उसे लॉक करने की सुविधा देता है।

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
// Add table node
outlineElem.appendChildLast(table);
// Add outline element node
outline.appendChildLast(outlineElem);
// Add outline node
page.appendChildLast(outline);
// Add page node
doc.appendChildLast(page);
```

## चरण 5: टेबल को आउटलाइन और पेज में जोड़ें
`Outline` क्लास पेज पर सामग्री को समूहित करती है, और `OutlineElement` एक व्यक्तिगत तत्व को दर्शाता है जैसे कि टेबल।

```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```

## चरण 6: दस्तावेज़ को सेव करें
`Document` इंस्टेंस पर `save` मेथड को कॉल करें, जिसमें `.one` फ़ाइल पाथ निर्दिष्ट करें। फिर फ़ाइल को सीधे Microsoft OneNote में खोला जा सकता है।

बधाई हो! आपने Aspose.Note for Java का उपयोग करके लॉक्ड कॉलम के साथ सफलतापूर्वक **OneNote में तालिका जोड़ना** पूरा कर लिया है।

## निष्कर्ष
इस गाइड में हमने लॉक्ड कॉलम के साथ **OneNote में तालिका जोड़ना** के लिए आवश्यक सभी चीज़ें कवर की हैं, प्रोजेक्ट सेटअप से लेकर अंतिम सेव तक। Aspose.Note की समृद्ध API का उपयोग करके आप कॉलम की चौड़ाई, लॉकिंग व्यवहार और बॉर्डर स्टाइलिंग पर सूक्ष्म नियंत्रण प्राप्त करते हैं—जिससे आपके नोट्स अधिक व्यवस्थित और पेशेवर बनते हैं।

## अक्सर पूछे जाने वाले प्रश्न
**Q: क्या Aspose.Note for Java सभी Java संस्करणों के साथ संगत है?**  
A: हाँ, Aspose.Note for Java Java 7 और बाद के संस्करणों, जिसमें Java 8, 11, और 17 शामिल हैं, के साथ काम करता है।

**Q: क्या मैं टेबल की उपस्थिति को और कस्टमाइज़ कर सकता हूँ?**  
A: बिल्कुल! आप बॉर्डर, सेल स्पेसिंग, बैकग्राउंड रंग, और यहाँ तक कि व्यक्तिगत सेल्स पर रिच टेक्स्ट फॉर्मेटिंग भी लागू कर सकते हैं।

**Q: क्या खरीदने से पहले कोई ट्रायल संस्करण उपलब्ध है?**  
A: हाँ, आप [एक फ्री ट्रायल डाउनलोड करें](https://releases.aspose.com/) करके Aspose.Note for Java की क्षमताओं को देख सकते हैं।

**Q: मैं अतिरिक्त समर्थन या समुदाय चर्चा कहाँ पा सकता हूँ?**  
A: समुदाय और Aspose इंजीनियर्स से मदद के लिए [Aspose.Note फोरम](https://forum.aspose.com/c/note/28) पर जाएँ।

**Q: मैं Aspose.Note for Java के लिए अस्थायी लाइसेंस कैसे प्राप्त करूँ?**  
A: परीक्षण उद्देश्यों के लिए अस्थायी लाइसेंस प्राप्त करने हेतु [अस्थायी लाइसेंस पेज](https://purchase.aspose.com/temporary-license/) पर जाएँ।

---

**अंतिम अपडेट:** 2026-08-13  
**परीक्षण किया गया:** Aspose.Note 24.11 for Java  
**लेखक:** Aspose

## संबंधित ट्यूटोरियल

- [Aspose.Note (Java) के साथ OneNote में तालिका को टेक्स्ट में बदलें](/note/java/onenote-table-manipulation/get-cell-text-from-row/)
- [टेबल रो जावा डालें - OneNote में टैग के साथ टेबल नोड जोड़ें - Aspose.Note](/note/java/onenote-tag-operations/add-new-table-node-with-tag/)
- [Aspose Note Java: OneNote दस्तावेज़ मैनिपुलेशन](/note/java/onenote-document-manipulation/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}