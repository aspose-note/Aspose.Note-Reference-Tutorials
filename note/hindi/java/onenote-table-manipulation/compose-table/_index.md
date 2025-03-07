---
title: OneNote में तालिका लिखें - Aspose.Note
linktitle: OneNote में तालिका लिखें - Aspose.Note
second_title: Aspose.नोट जावा एपीआई
description: जावा के लिए Aspose.Note का उपयोग करके प्रोग्रामेटिक रूप से OneNote में तालिकाएँ बनाना सीखें। कुशल दस्तावेज़ निर्माण के लिए चरण-दर-चरण मार्गदर्शिका।
weight: 11
url: /hi/java/onenote-table-manipulation/compose-table/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote में तालिका लिखें - Aspose.Note

## परिचय
आज के प्रतिस्पर्धी कारोबारी माहौल में, प्रभावी संचार और सहयोग सफलता प्राप्त करने के प्रमुख कारक हैं। Java के लिए Aspose.Note OneNote दस्तावेज़ों को प्रोग्रामेटिक रूप से बनाने और उनमें हेरफेर करने के लिए एक शक्तिशाली समाधान प्रदान करता है। इस ट्यूटोरियल में, हम जावा के लिए Aspose.Note का उपयोग करके OneNote में तालिकाएँ बनाने का तरीका जानेंगे। अपनी दस्तावेज़ निर्माण प्रक्रिया को बेहतर बनाने के लिए नीचे दिए गए चरण-दर-चरण मार्गदर्शिका का पालन करें।
## आवश्यक शर्तें
ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित शर्तें हैं:
- जावा प्रोग्रामिंग का बुनियादी ज्ञान।
-  जावा लाइब्रेरी के लिए Aspose.Note स्थापित किया गया। आप इसे यहां से डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/note/java/).
- जावा विकास के लिए एक एकीकृत विकास वातावरण (आईडीई) स्थापित किया गया।
## पैकेज आयात करें
अपने प्रोजेक्ट को किकस्टार्ट करने के लिए आवश्यक पैकेज आयात करना सुनिश्चित करें। अपनी जावा क्लास में निम्नलिखित आयात विवरण जोड़ें:
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
"आपकी दस्तावेज़ निर्देशिका" को उस वास्तविक पथ से बदलना सुनिश्चित करें जहाँ आप अपना OneNote दस्तावेज़ सहेजना चाहते हैं।
## चरण 2: हेडर लिखें
```java
RichText headerText = new RichText().append("Super contest for suppliers.");
headerText.setParagraphStyle(new ParagraphStyle().setFontSize(18).setBold(true));
headerText.setAlignment(HorizontalAlignment.Center);
```
अपने दस्तावेज़ के लिए एक आकर्षक हेडर बनाएं। फ़ॉन्ट आकार, बोल्डनेस और संरेखण को आवश्यकतानुसार समायोजित करें।
## चरण 3: पेज और रूपरेखा बनाएं
```java
Page page = new Page();
Outline outline = page.appendChildLast(new Outline());
outline.setHorizontalOffset(50);
outline.appendChildLast(new OutlineElement()).appendChildLast(headerText);
```
एक नया पेज सेट करें और रूपरेखा बनाएं, फिर पहले से बनाए गए हेडर को रूपरेखा में जोड़ें।
## चरण 4: सारांश पाठ जोड़ें
```java
RichText bodyTextHeader = outline.appendChildLast(new OutlineElement()).appendChildLast(new RichText());
bodyTextHeader.setParagraphStyle(ParagraphStyle.getDefault());
bodyTextHeader.append("This is the final ranking of proposals got from our suppliers.");
```
तालिका के लिए संदर्भ प्रदान करने के लिए एक संक्षिप्त सारांश पाठ शामिल करें।
## चरण 5: तालिका लिखें
```java
Table ranking = outline.appendChildLast(new OutlineElement()).appendChildLast(new Table());
// शेष चरण तालिका संरचना, हेडर पंक्ति को स्थापित करने और खाली पंक्तियों को जोड़ने में शामिल हैं।
// विस्तृत कार्यान्वयन के लिए दिए गए कोड को देखें।
```
तालिका संरचना बनाएं और उसे प्रासंगिक जानकारी से भर दें। प्रदान किए गए कोड में 'संपर्क' कॉलम के लिए कॉलम, हेडर पंक्ति, खाली पंक्तियां और टेम्पलेट सामग्री जोड़ना शामिल है।
## चरण 6: दस्तावेज़ सहेजें
```java
Document d = new Document();
d.appendChildLast(page);
d.save(Paths.get(dataDir, "ComposeTable_out.one").toString());
```
अपने रचित दस्तावेज़ को एक निर्दिष्ट फ़ाइल नाम और निर्देशिका पथ के साथ सहेजें।
## निष्कर्ष
बधाई हो! आपने Java के लिए Aspose.Note का उपयोग करके OneNote में सफलतापूर्वक एक तालिका बना ली है। इस ट्यूटोरियल ने चरण-दर-चरण प्रक्रिया का प्रदर्शन किया, जो आपको अपनी दस्तावेज़ निर्माण क्षमताओं को प्रोग्रामेटिक रूप से बढ़ाने के लिए सशक्त बनाता है।
## अक्सर पूछे जाने वाले प्रश्नों
### प्रश्न: मैं जावा दस्तावेज़ के लिए Aspose.Note कहां पा सकता हूं?
 आप दस्तावेज़ का संदर्भ ले सकते हैं[यहाँ](https://reference.aspose.com/note/java/).
### प्रश्न: मैं जावा के लिए Aspose.Note कैसे डाउनलोड करूं?
 आप इसे यहां से डाउनलोड कर सकते हैं[इस लिंक](https://releases.aspose.com/note/java/).
### प्रश्न: क्या कोई निःशुल्क परीक्षण उपलब्ध है?
 हाँ, आप नि:शुल्क परीक्षण का उपयोग कर सकते हैं[यहाँ](https://releases.aspose.com/).
### प्रश्न: जावा के लिए Aspose.Note के लिए मुझे समर्थन कहां से मिल सकता है?
 सहायता फ़ोरम पर जाएँ[यहाँ](https://forum.aspose.com/c/note/28).
### प्रश्न: क्या मैं अस्थायी लाइसेंस प्राप्त कर सकता हूँ?
 हाँ, आप अस्थायी लाइसेंस प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
