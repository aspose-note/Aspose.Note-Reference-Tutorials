---
title: OneNote में लॉक किए गए कॉलम के साथ तालिका बनाएं - Aspose.Note
linktitle: OneNote में लॉक किए गए कॉलम के साथ तालिका बनाएं - Aspose.Note
second_title: Aspose.नोट जावा एपीआई
description: Java के लिए Aspose.Note के साथ अपने OneNote अनुभव को बेहतर बनाएं। चरण-दर-चरण मार्गदर्शिका का उपयोग करके लॉक किए गए कॉलम के साथ तालिकाएँ बनाना सीखें। अभी अपने मुफ़्त ट्रायल को डाउनलोड करें!
weight: 12
url: /hi/java/onenote-table-manipulation/create-table-with-locked-columns/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote में लॉक किए गए कॉलम के साथ तालिका बनाएं - Aspose.Note

## परिचय
OneNote जानकारी व्यवस्थित करने के लिए एक शक्तिशाली उपकरण है, और Java के लिए Aspose.Note लॉक किए गए कॉलम के साथ तालिकाएँ बनाने का एक सहज तरीका प्रदान करके अपनी क्षमताओं को बढ़ाता है। इस ट्यूटोरियल में, हम OneNote में लॉक किए गए कॉलम के साथ एक तालिका बनाने के लिए Java के लिए Aspose.Note का उपयोग करने की प्रक्रिया में आपका मार्गदर्शन करेंगे।
## आवश्यक शर्तें
शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:
- [जावा डेवलपमेंट किट (जेडीके)](https://www.oracle.com/java/technologies/javase-downloads.html)आपकी मशीन पर स्थापित.
- [जावा के लिए Aspose.Note](https://downloads.aspose.com/note/java) लाइब्रेरी डाउनलोड की गई और आपके प्रोजेक्ट में जोड़ी गई।
## पैकेज आयात करें
अपने जावा प्रोजेक्ट में, Aspose.Note के साथ काम करने के लिए आवश्यक पैकेज आयात करें:
```java
import com.aspose.note.*;
import java.io.IOException;
```
## चरण 1: अपना प्रोजेक्ट सेट करें
एक नया जावा प्रोजेक्ट बनाकर और Aspose.Note लाइब्रेरी को अपने क्लासपाथ में जोड़कर प्रारंभ करें। सुनिश्चित करें कि आपका प्रोजेक्ट JDK का उपयोग करने के लिए कॉन्फ़िगर किया गया है।
## चरण 2: दस्तावेज़ और पृष्ठ ऑब्जेक्ट प्रारंभ करें
```java
// दस्तावेज़ निर्देशिका का पथ.
String dataDir = "Your Document Directory";
//दस्तावेज़ वर्ग का एक ऑब्जेक्ट बनाएं
Document doc = new Document();
// पेज क्लास ऑब्जेक्ट को इनिशियलाइज़ करें
Page page = new Page();
```
## चरण 3: तालिका पंक्तियाँ और कक्ष बनाएँ
```java
// TableRow क्लास ऑब्जेक्ट को इनिशियलाइज़ करें
TableRow row1 = new TableRow();
// टेबलसेल क्लास ऑब्जेक्ट को प्रारंभ करें और टेक्स्ट सामग्री सेट करें
TableCell cell11 = new TableCell();
cell11.appendChildLast(InsertTable.GetOutlineElementWithText("Small text"));
row1.appendChildLast(cell11);
// TableRow क्लास ऑब्जेक्ट को इनिशियलाइज़ करें
TableRow row2 = new TableRow();
// टेबलसेल क्लास ऑब्जेक्ट को प्रारंभ करें और टेक्स्ट सामग्री सेट करें
TableCell cell21 = new TableCell();
cell21.appendChildLast(InsertTable.GetOutlineElementWithText("Long   text    with    several   words and    spaces."));
row2.appendChildLast(cell21);
```
## चरण 4: तालिका बनाएं और अनुकूलित करें
```java
// टेबल क्लास ऑब्जेक्ट को इनिशियलाइज़ करें
Table table = new Table();
table.setBordersVisible(true);
TableColumn col = new TableColumn();
col.setWidth(200);
col.setLockedWidth(true);
table.getColumns().addItem(col);
// पंक्तियाँ जोड़ें
table.appendChildLast(row1);
table.appendChildLast(row2);
```
## चरण 5: रूपरेखा और पृष्ठ में तालिका जोड़ें
```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
// तालिका नोड जोड़ें
outlineElem.appendChildLast(table);
// बाह्यरेखा तत्व नोड जोड़ें
outline.appendChildLast(outlineElem);
// रूपरेखा नोड जोड़ें
page.appendChildLast(outline);
// पेज नोड जोड़ें
doc.appendChildLast(page);
```
## चरण 6: दस्तावेज़ सहेजें
```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```
बधाई हो! आपने Java के लिए Aspose.Note का उपयोग करके OneNote में लॉक किए गए कॉलम वाली एक तालिका सफलतापूर्वक बना ली है।
## निष्कर्ष
इस ट्यूटोरियल में, हमने लॉक किए गए कॉलम के साथ तालिकाएँ बनाकर आपके OneNote अनुभव को बढ़ाने के लिए Java के लिए Aspose.Note का उपयोग करने की प्रक्रिया का पता लगाया। यह कार्यक्षमता आपके नोट्स में संगठन और संरचना की एक नई परत जोड़ती है।
## पूछे जाने वाले प्रश्न
### क्या जावा के लिए Aspose.Note सभी जावा संस्करणों के साथ संगत है?
हाँ, Java के लिए Aspose.Note Java 6 और बाद के संस्करणों के साथ संगत है।
### क्या मैं तालिका के स्वरूप को और अधिक अनुकूलित कर सकता हूँ?
बिल्कुल! जावा के लिए Aspose.Note तालिकाओं को अनुकूलित करने के लिए व्यापक विकल्प प्रदान करता है, जैसे बॉर्डर समायोजित करना, सेल रिक्ति और बहुत कुछ।
### क्या खरीदने से पहले कोई परीक्षण संस्करण उपलब्ध है?
 हाँ तुम कर सकते हो[निःशुल्क परीक्षण डाउनलोड करें](https://releases.aspose.com/) जावा के लिए Aspose.Note की क्षमताओं का पता लगाने के लिए।
### मुझे अतिरिक्त सहायता या सामुदायिक चर्चाएँ कहाँ मिल सकती हैं?
 दौरा करना[Aspose.नोट फोरम](https://forum.aspose.com/c/note/28) समर्थन और सामुदायिक चर्चा के लिए।
### मैं जावा के लिए Aspose.Note के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?
 मिलने जाना[इस लिंक](https://purchase.aspose.com/temporary-license/) परीक्षण उद्देश्यों के लिए अस्थायी लाइसेंस प्राप्त करना।
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
