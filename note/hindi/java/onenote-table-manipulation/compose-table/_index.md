---
date: 2026-01-23
description: Aspose.Note for Java का उपयोग करके प्रोग्रामेटिक रूप से OneNote में तालिका
  जोड़ना सीखें। कुशल दस्तावेज़ निर्माण के लिए चरण-दर-चरण मार्गदर्शिका।
linktitle: How to add table to OneNote with Aspose.Note for Java
second_title: Aspose.Note Java API
title: Aspose.Note for Java के साथ OneNote में तालिका कैसे जोड़ें
url: /hi/java/onenote-table-manipulation/compose-table/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote में तालिका जोड़ने का तरीका Aspose.Note for Java के साथ

## परिचय
इस ट्यूटोरियल में, आप सीखेंगे कि **OneNote में तालिका कैसे जोड़ें** Aspose.Note for Java का उपयोग करके, जिससे आप प्रोग्रामेटिक रूप से समृद्ध, संरचित दस्तावेज़ बना सकें जो सहयोग और रिपोर्टिंग को बेहतर बनाते हैं। Aspose.Note OneNote पेज, रूपरेखा और तालिकाएँ बनाने के लिए एक शक्तिशाली API प्रदान करता है, बिना मैन्युअल संपादन के।

## त्वरित उत्तर
- **इस ट्यूटोरियल में क्या कवर किया गया है?** Aspose.Note for Java के साथ OneNote में तालिका जोड़ना।  
- **कितना समय चाहिए?** बुनियादी कार्यान्वयन के लिए लगभग 10‑15 मिनट।  
- **क्या मुझे लाइसेंस चाहिए?** मूल्यांकन के लिए एक फ्री ट्रायल काम करता है; उत्पादन के लिए एक व्यावसायिक लाइसेंस आवश्यक है।  
- **कौन सा Java संस्करण समर्थित है?** Java 8 और उसके बाद के संस्करण।  
- **क्या मैं तालिका शैलियों को अनुकूलित कर सकता हूँ?** हाँ – आप API के माध्यम से फ़ॉन्ट, रंग और सेल बॉर्डर को संशोधित कर सकते हैं।

## पूर्वापेक्षाएँ
ट्यूटोरियल में डुबकी लगाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ हैं:
- Java प्रोग्रामिंग का बुनियादी ज्ञान।  
- Aspose.Note for Java लाइब्रेरी स्थापित है। आप इसे [here](https://releases.aspose.com/note/java/) से डाउनलोड कर सकते हैं।  
- Java विकास के लिए एक एकीकृत विकास वातावरण (IDE) सेट अप किया हुआ।

## पैकेज आयात करें
अपने प्रोजेक्ट को शुरू करने के लिए आवश्यक पैकेज आयात करना सुनिश्चित करें। अपने Java क्लास में निम्नलिखित आयात कथन जोड़ें:

```java
import com.aspose.note.*;
import java.awt.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.stream.StreamSupport;
```

## चरण 1: दस्तावेज़ निर्देशिका सेट करें
```java
String dataDir = "Your Document Directory";
```
`"Your Document Directory"` को उस वास्तविक पथ से बदलें जहाँ आप अपना OneNote दस्तावेज़ सहेजना चाहते हैं।

## चरण 2: हेडर बनाएं
```java
RichText headerText = new RichText().append("Super contest for suppliers.");
headerText.setParagraphStyle(new ParagraphStyle().setFontSize(18).setBold(true));
headerText.setAlignment(HorizontalAlignment.Center);
```
अपने दस्तावेज़ के लिए एक आकर्षक हेडर बनाएं। आवश्यकतानुसार फ़ॉन्ट आकार, बोल्डनेस और संरेखण को समायोजित करें।

## चरण 3: पेज और रूपरेखा बनाएं
```java
Page page = new Page();
Outline outline = page.appendChildLast(new Outline());
outline.setHorizontalOffset(50);
outline.appendChildLast(new OutlineElement()).appendChildLast(headerText);
```
एक नया पेज और रूपरेखा सेट करें, फिर पहले बनाए गए हेडर को रूपरेखा में जोड़ें।

## चरण 4: सारांश पाठ जोड़ें
```java
RichText bodyTextHeader = outline.appendChildLast(new OutlineElement()).appendChildLast(new RichText());
bodyTextHeader.setParagraphStyle(ParagraphStyle.getDefault());
bodyTextHeader.append("This is the final ranking of proposals got from our suppliers.");
```
तालिका के संदर्भ के लिए एक संक्षिप्त सारांश पाठ शामिल करें।

## चरण 5: OneNote में तालिका जोड़ें
```java
Table ranking = outline.appendChildLast(new OutlineElement()).appendChildLast(new Table());
// Remaining steps are involved in setting up the table structure, header row, and adding empty rows.
// Refer to the provided code for detailed implementation.
```
तालिका की संरचना बनाएं और इसे प्रासंगिक जानकारी से भरें। प्रदान किया गया कोड कॉलम जोड़ना, हेडर पंक्ति, खाली पंक्तियाँ, और “Contacts” कॉलम के लिए टेम्पलेट सामग्री शामिल करता है।

## चरण 6: दस्तावेज़ सहेजें
```java
Document d = new Document();
d.appendChildLast(page);
d.save(Paths.get(dataDir, "ComposeTable_out.one").toString());
```
निर्दिष्ट फ़ाइलनाम और निर्देशिका पथ के साथ अपने तैयार दस्तावेज़ को सहेजें।

## निष्कर्ष
बधाई हो! आपने सफलतापूर्वक Aspose.Note for Java का उपयोग करके **OneNote में तालिका जोड़ दी** है। इस ट्यूटोरियल ने चरण‑दर‑चरण प्रक्रिया को प्रदर्शित किया, जिससे आप प्रोग्रामेटिक रूप से अपने दस्तावेज़ निर्माण क्षमताओं को बढ़ा सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न
### प्रश्न: मैं Aspose.Note for Java दस्तावेज़ीकरण कहाँ पा सकता हूँ?
आप दस्तावेज़ीकरण को [here](https://reference.aspose.com/note/java/) पर देख सकते हैं।

### प्रश्न: मैं Aspose.Note for Java कैसे डाउनलोड करूँ?
आप इसे [this link](https://releases.aspose.com/note/java/) से डाउनलोड कर सकते हैं।

### प्रश्न: क्या कोई फ्री ट्रायल उपलब्ध है?
हाँ, आप फ्री ट्रायल को [here](https://releases.aspose.com/) पर एक्सेस कर सकते हैं।

### प्रश्न: मैं Aspose.Note for Java के लिए समर्थन कहाँ प्राप्त कर सकता हूँ?
समर्थन फ़ोरम को [here](https://forum.aspose.com/c/note/28) पर देखें।

### प्रश्न: क्या मैं अस्थायी लाइसेंस प्राप्त कर सकता हूँ?
हाँ, आप अस्थायी लाइसेंस को [here](https://purchase.aspose.com/temporary-license/) पर प्राप्त कर सकते हैं।

---

**अंतिम अपडेट:** 2026-01-23  
**परीक्षण किया गया:** Aspose.Note for Java (नवीनतम रिलीज़)  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}