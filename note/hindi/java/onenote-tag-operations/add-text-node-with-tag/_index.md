---
title: OneNote में टैग के साथ टेक्स्ट नोड जोड़ें - Aspose.Note
linktitle: OneNote में टैग के साथ टेक्स्ट नोड जोड़ें - Aspose.Note
second_title: Aspose.नोट जावा एपीआई
description: जावा के लिए Aspose.Note का उपयोग करके OneNote में टैग के साथ टेक्स्ट नोड्स जोड़ने का तरीका जानें। आसान, कुशल और डेवलपर-अनुकूल। अभी लाइब्रेरी डाउनलोड करें!
weight: 13
url: /hi/java/onenote-tag-operations/add-text-node-with-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote में टैग के साथ टेक्स्ट नोड जोड़ें - Aspose.Note

## परिचय
इस ट्यूटोरियल में, हम देखेंगे कि Java के लिए Aspose.Note का उपयोग करके OneNote में एक टैग के साथ टेक्स्ट नोड कैसे जोड़ा जाए। Aspose.Note एक शक्तिशाली जावा लाइब्रेरी है जो डेवलपर्स को Microsoft OneNote फ़ाइलों के साथ प्रोग्रामेटिक रूप से काम करने की अनुमति देती है। दस्तावेज़ प्रसंस्करण में टैग के साथ टेक्स्ट नोड्स जोड़ना एक सामान्य आवश्यकता है, और Aspose.Note इस कार्य को सरल बनाता है।
## आवश्यक शर्तें
इससे पहले कि हम ट्यूटोरियल में उतरें, सुनिश्चित करें कि आपके पास निम्नलिखित शर्तें हैं:
- जावा प्रोग्रामिंग का बुनियादी ज्ञान।
-  जावा लाइब्रेरी के लिए Aspose.Note स्थापित किया गया। आप इसे डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/note/java/).
- जावा विकास के लिए एक एकीकृत विकास पर्यावरण (आईडीई) स्थापित किया गया।
## पैकेज आयात करें
अपने जावा प्रोजेक्ट के लिए आवश्यक पैकेज आयात करके शुरुआत करें। अपने कोड में, निम्नलिखित आयात शामिल करें:
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.TagIcon;
import com.aspose.note.ParagraphStyle;
```
## चरण 1: दस्तावेज़ ऑब्जेक्ट बनाएँ
OneNote दस्तावेज़ का प्रतिनिधित्व करने के लिए दस्तावेज़ वर्ग ऑब्जेक्ट को प्रारंभ करें:
```java
// दस्तावेज़ निर्देशिका का पथ.
String dataDir = "Your Document Directory";
//दस्तावेज़ वर्ग का एक ऑब्जेक्ट बनाएं
Document doc = new Document();
```
## चरण 2: पेज क्लास ऑब्जेक्ट को आरंभ करें
दस्तावेज़ के भीतर पेज का प्रतिनिधित्व करने के लिए पेज क्लास ऑब्जेक्ट को प्रारंभ करें:
```java
// पेज क्लास ऑब्जेक्ट को इनिशियलाइज़ करें
Page page = new Page();
```
## चरण 3: आउटलाइन क्लास ऑब्जेक्ट को आरंभ करें
पृष्ठ के भीतर सामग्री को संरचित करने के लिए एक आउटलाइन क्लास ऑब्जेक्ट को प्रारंभ करें:
```java
// आउटलाइन क्लास ऑब्जेक्ट को इनिशियलाइज़ करें
Outline outline = new Outline();
```
## चरण 4: आउटलाइनएलिमेंट क्लास ऑब्जेक्ट को आरंभ करें
रूपरेखा के भीतर एक तत्व का प्रतिनिधित्व करने के लिए एक आउटलाइनएलिमेंट क्लास ऑब्जेक्ट को प्रारंभ करें:
```java
// आउटलाइनएलिमेंट क्लास ऑब्जेक्ट को इनिशियलाइज़ करें
OutlineElement outlineElem = new OutlineElement();
```
## चरण 5: टेक्स्ट शैली को अनुकूलित करें
टेक्स्ट नोड के लिए शैली सेट करें, जैसे फ़ॉन्ट रंग, नाम और आकार:
```java
// पाठ शैली को अनुकूलित करें
ParagraphStyle textStyle = new ParagraphStyle()
                                .setFontColor(Color.BLACK)
                                .setFontName("Arial")
                                .setFontSize(10);
```
## चरण 6: रिचटेक्स्ट ऑब्जेक्ट बनाएं
एक रिचटेक्स्ट ऑब्जेक्ट बनाएं और उसमें वांछित टेक्स्ट जोड़ें:
```java
// रिचटेक्स्ट ऑब्जेक्ट बनाएं
RichText text = new RichText().append("OneNote text.");
text.setParagraphStyle(textStyle);
```
## चरण 7: नोट टैग जोड़ें
टेक्स्ट में एक नोट टैग, जैसे पीला सितारा, जोड़ें:
```java
// नोट टैग जोड़ें
NoteTag noteTag = NoteTag.createYellowStar();
text.getTags().add(noteTag);
```
## चरण 8: टेक्स्ट नोड जोड़ें
आउटलाइन तत्व में टेक्स्ट नोड जोड़ें:
```java
// टेक्स्ट नोड जोड़ें
outlineElem.appendChildLast(text);
```
## चरण 9: आउटलाइन में आउटलाइन तत्व जोड़ें
रूपरेखा तत्व को रूपरेखा में जोड़ें:
```java
// बाह्यरेखा तत्व नोड जोड़ें
outline.appendChildLast(outlineElem);
```
## चरण 10: पृष्ठ पर रूपरेखा जोड़ें
पृष्ठ पर रूपरेखा जोड़ें:
```java
// रूपरेखा नोड जोड़ें
page.appendChildLast(outline);
```
## चरण 11: दस्तावेज़ में पेज जोड़ें
दस्तावेज़ में पृष्ठ जोड़ें:
```java
// पेज नोड जोड़ें
doc.appendChildLast(page);
```
## चरण 12: OneNote दस्तावेज़ सहेजें
OneNote दस्तावेज़ को निर्दिष्ट निर्देशिका में सहेजें:
```java
// OneNote दस्तावेज़ सहेजें
doc.save(dataDir + "AddTextNodeWithTag_out.one");
```
बधाई हो! आपने जावा के लिए Aspose.Note का उपयोग करके OneNote में एक टैग के साथ एक टेक्स्ट नोड सफलतापूर्वक जोड़ा है।
## निष्कर्ष
इस ट्यूटोरियल में, हमने जावा लाइब्रेरी के लिए Aspose.Note का उपयोग करके OneNote में एक टैग के साथ टेक्स्ट नोड जोड़ने की चरण-दर-चरण प्रक्रिया को कवर किया है। यह शक्तिशाली लाइब्रेरी दस्तावेज़ प्रसंस्करण कार्यों को सरल बनाती है, जिससे डेवलपर्स के लिए OneNote फ़ाइलों को प्रोग्रामेटिक रूप से हेरफेर करना आसान हो जाता है।
## अक्सर पूछे जाने वाले प्रश्नों
### प्रश्न: क्या मैं अन्य जावा लाइब्रेरीज़ के साथ जावा के लिए Aspose.Note का उपयोग कर सकता हूँ?
उत्तर: हाँ, जावा के लिए Aspose.Note को दस्तावेज़ प्रसंस्करण क्षमताओं को बढ़ाने के लिए अन्य जावा पुस्तकालयों के साथ सहजता से एकीकृत किया जा सकता है।
### प्रश्न: क्या जावा के लिए Aspose.Note का निःशुल्क परीक्षण उपलब्ध है?
 उत्तर: हाँ, आप नि:शुल्क परीक्षण का उपयोग कर सकते हैं[यहाँ](https://releases.aspose.com/).
### प्रश्न: मैं जावा के लिए Aspose.Note के लिए समर्थन कैसे प्राप्त कर सकता हूं?
उ: आप Aspose.Note समुदाय से समर्थन मांग सकते हैं[मंच](https://forum.aspose.com/c/note/28).
### प्रश्न: क्या जावा के लिए Aspose.Note के लिए अस्थायी लाइसेंस उपलब्ध हैं?
 उत्तर: हाँ, आप अस्थायी लाइसेंस प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/).
### प्रश्न: मैं जावा के लिए Aspose.Note के लिए दस्तावेज़ कहां पा सकता हूं?
 उत्तर: दस्तावेज़ उपलब्ध है[यहाँ](https://reference.aspose.com/note/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
