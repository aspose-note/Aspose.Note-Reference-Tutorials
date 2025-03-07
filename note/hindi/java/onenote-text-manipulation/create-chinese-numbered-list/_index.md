---
title: OneNote में चीनी क्रमांकित सूची बनाएं - Aspose.Note
linktitle: OneNote में चीनी क्रमांकित सूची बनाएं - Aspose.Note
second_title: Aspose.नोट जावा एपीआई
description: Aspose.Note के साथ जावा में दस्तावेज़ निर्माण बढ़ाएँ। OneNote में चरण दर चरण चीनी क्रमांकित सूची बनाना सीखें। Aspose.Note की शक्तिशाली विशेषताओं का अन्वेषण करें।
weight: 13
url: /hi/java/onenote-text-manipulation/create-chinese-numbered-list/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote में चीनी क्रमांकित सूची बनाएं - Aspose.Note

## परिचय
यदि आप जावा में अपनी दस्तावेज़ निर्माण क्षमताओं को बढ़ाना चाहते हैं, तो Aspose.Note आपके लिए उपयुक्त समाधान है। इस ट्यूटोरियल में, हम जावा के लिए Aspose.Note का उपयोग करके OneNote में एक चीनी क्रमांकित सूची बनाने की प्रक्रिया में आपका मार्गदर्शन करेंगे। यह शक्तिशाली लाइब्रेरी आपको OneNote दस्तावेज़ों को प्रोग्रामेटिक रूप से हेरफेर करने की अनुमति देती है, जिससे आपको उनकी संरचना और सामग्री पर पूर्ण नियंत्रण मिलता है।
## आवश्यक शर्तें
ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:
1. जावा विकास वातावरण: सुनिश्चित करें कि आपकी मशीन पर जावा विकास वातावरण स्थापित है।
2.  Aspose.Note लाइब्रेरी: Aspose.Note लाइब्रेरी डाउनलोड और इंस्टॉल करें। आप डाउनलोड लिंक पा सकते हैं[यहाँ](https://releases.aspose.com/note/java/).
## पैकेज आयात करें
अपने जावा प्रोजेक्ट में आवश्यक पैकेज आयात करके शुरुआत करें। जावा के लिए Aspose.Note की सुविधाओं का उपयोग करने के लिए ये पैकेज आवश्यक हैं। यहां एक नमूना कोड स्निपेट है:
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NumberFormat;
import com.aspose.note.NumberList;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.ParagraphStyle;
```
अब, आइए कोड को अलग-अलग चरणों में विभाजित करें:
## चरण 1: दस्तावेज़ ऑब्जेक्ट बनाएँ
```java
// दस्तावेज़ निर्देशिका का पथ.
String dataDir = "Your Document Directory";
// दस्तावेज़ वर्ग का एक ऑब्जेक्ट बनाएं
Document doc = new Document();
```
## चरण 2: पेज ऑब्जेक्ट को आरंभ करें
```java
// पेज क्लास ऑब्जेक्ट को इनिशियलाइज़ करें
Page page = new Page();
```
## चरण 3: आउटलाइन ऑब्जेक्ट को आरंभ करें
```java
// आउटलाइन क्लास ऑब्जेक्ट को इनिशियलाइज़ करें
Outline outline = new Outline();
```
## चरण 4: टेक्स्टस्टाइल ऑब्जेक्ट को आरंभ करें
```java
// टेक्स्टस्टाइल क्लास ऑब्जेक्ट को प्रारंभ करें और फ़ॉर्मेटिंग गुण सेट करें
ParagraphStyle defaultStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```
## चरण 5: आउटलाइनएलिमेंट ऑब्जेक्ट को आरंभ करें और नंबरिंग लागू करें
```java
// आउटलाइनएलिमेंट क्लास ऑब्जेक्ट को इनिशियलाइज़ करें और नंबरिंग लागू करें
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10));
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
OutlineElement outlineElem2 = new OutlineElement();
outlineElem2.setNumberList(new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10));
RichText text2 = new RichText().append("Second");
text2.setParagraphStyle(defaultStyle);
outlineElem2.appendChildLast(text2);
OutlineElement outlineElem3 = new OutlineElement();
outlineElem3.setNumberList(new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10));
RichText text3 = new RichText().append("Third");
text3.setParagraphStyle(defaultStyle);
outlineElem3.appendChildLast(text3);
```
## चरण 6: रूपरेखा तत्व जोड़ें
```java
// रूपरेखा तत्व जोड़ें
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```
## चरण 7: पेज पर आउटलाइन नोड जोड़ें
```java
// आउटलाइन नोड जोड़ें
page.appendChildLast(outline);
```
## चरण 8: दस्तावेज़ में पेज नोड जोड़ें
```java
// पेज नोड जोड़ें
doc.appendChildLast(page);
```
## चरण 9: दस्तावेज़ सहेजें
```java
// दस्तावेज़ सहेजें
doc.save(dataDir + "CreateChineseNumberedList_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "CreateChineseNumberedList_out.pdf");
```
अब आपने Java के लिए Aspose.Note का उपयोग करके OneNote में सफलतापूर्वक एक चीनी क्रमांकित सूची बना ली है!
## निष्कर्ष
इस ट्यूटोरियल में, हमने OneNote में चीनी क्रमांकित सूची तैयार करने के लिए Java के लिए Aspose.Note का लाभ उठाने की प्रक्रिया का पता लगाया है। अपनी शक्तिशाली विशेषताओं के साथ, Aspose.Note डेवलपर्स को दस्तावेज़ सामग्री को प्रोग्रामेटिक रूप से हेरफेर करने और बढ़ाने का अधिकार देता है।
## अक्सर पूछे जाने वाले प्रश्नों
### क्या Aspose.Note विभिन्न जावा IDE के साथ संगत है?
हाँ, Aspose.Note Eclipse और IntelliJ IDEA जैसे लोकप्रिय जावा IDE के साथ संगत है।
### क्या मैं क्रमांकित सूची के स्वरूपण को अनुकूलित कर सकता हूँ?
बिल्कुल। जैसा कि ट्यूटोरियल में दिखाया गया है, आप अपनी विशिष्ट आवश्यकताओं को पूरा करने के लिए फ़ॉन्ट, रंग और आकार को समायोजित कर सकते हैं।
### क्या Aspose.Note के लिए कोई परीक्षण संस्करण उपलब्ध है?
 हां, आप परीक्षण संस्करण का पता लगा सकते हैं[यहाँ](https://releases.aspose.com/).
### मुझे Aspose.Note के लिए विस्तृत दस्तावेज़ कहाँ मिल सकते हैं?
 दस्तावेज़ देखें[यहाँ](https://reference.aspose.com/note/java/).
### मैं Aspose.Note के लिए समर्थन कैसे प्राप्त कर सकता हूँ?
 सहायता फ़ोरम पर जाएँ[यहाँ](https://forum.aspose.com/c/note/28) किसी भी सहायता या प्रश्न के लिए।
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
