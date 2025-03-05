---
title: OneNote में क्रमांकित सूची बनाएं - Aspose.Note
linktitle: OneNote में क्रमांकित सूची बनाएं - Aspose.Note
second_title: Aspose.नोट जावा एपीआई
description: जावा के लिए Aspose.Note के साथ OneNote में आसानी से क्रमांकित सूची बनाने का तरीका जानें। निःशुल्क परीक्षण डाउनलोड करें और जावा विकास की दुनिया में उतरें!
type: docs
weight: 14
url: /hi/java/onenote-text-manipulation/create-numbered-list/
---
## परिचय
Java के लिए Aspose.Note जावा डेवलपर्स को Microsoft OneNote फ़ाइलों के साथ निर्बाध रूप से काम करने का अधिकार देता है। इस ट्यूटोरियल में, हम आपको जावा लाइब्रेरी के लिए शक्तिशाली Aspose.Note के साथ OneNote में एक क्रमांकित सूची तैयार करने की प्रक्रिया के बारे में बताएंगे।
## आवश्यक शर्तें
ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि निम्नलिखित आवश्यक शर्तें मौजूद हैं:
- आपकी मशीन पर जावा डेवलपमेंट किट (जेडीके) स्थापित किया गया।
-  जावा लाइब्रेरी के लिए Aspose.Note से डाउनलोड किया गया[यहाँ](https://releases.aspose.com/note/java/).
## पैकेज आयात करना
सबसे पहले, आइए Aspose.Note कार्यात्मकताओं का अधिकतम लाभ उठाने के लिए अपने जावा प्रोजेक्ट में आवश्यक पैकेज आयात करें। अपने प्रोजेक्ट में निम्नलिखित कोड शामिल करें:
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
## चरण 1: दस्तावेज़, पृष्ठ और रूपरेखा वस्तुओं को आरंभ करना
```java
// आपकी दस्तावेज़ निर्देशिका
String dataDir = "Your Document Directory";
// दस्तावेज़, पृष्ठ और रूपरेखा ऑब्जेक्ट बनाएँ
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
// डिफ़ॉल्ट पाठ शैली सेट करें
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
```
## चरण 2: डिफ़ॉल्ट टेक्स्ट शैली सेट करना
```java
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
```
## चरण 3: रूपरेखा तत्व बनाना
अब, आइए आपकी क्रमांकित सूची के लिए तत्व बनाएं।
```java
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10));
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
// अन्य तत्वों के लिए दोहराएँ (रूपरेखाElem2 और रूपरेखाElem3)
```
## चरण 4: रूपरेखा तत्वों को रूपरेखा में जोड़ना
```java
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```
## चरण 5: पृष्ठ पर रूपरेखा जोड़ना
```java
page.appendChildLast(outline);
```
## चरण 6: दस्तावेज़ सहेजना
```java
doc.appendChildLast(page);
doc.save(dataDir + "CreateNumberedList_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "CreateNumberedList_out.pdf");
```
इन चरणों का सावधानीपूर्वक पालन करें, और आप जावा के लिए Aspose.Note का उपयोग करके आसानी से OneNote में एक क्रमांकित सूची बना लेंगे।
## निष्कर्ष
इस ट्यूटोरियल में, हमने जावा के लिए Aspose.Note का उपयोग करके OneNote में एक क्रमांकित सूची बनाने की निर्बाध प्रक्रिया का पता लगाया। लाइब्रेरी की मजबूत विशेषताएं इसे Microsoft OneNote फ़ाइलों के साथ काम करने वाले जावा डेवलपर्स के लिए एक अमूल्य उपकरण बनाती हैं।
## अक्सर पूछे जाने वाले प्रश्नों
### प्रश्न: क्या मैं अपनी OneNote सूची में क्रमांकन प्रारूप को अनुकूलित कर सकता हूँ?
उत्तर: बिल्कुल! आप जावा के लिए Aspose.Note द्वारा प्रदान की गई NumberList क्लास का उपयोग करके नंबरिंग प्रारूप को अनुकूलित कर सकते हैं।
### प्रश्न: क्या जावा के लिए Aspose.Note का कोई परीक्षण संस्करण उपलब्ध है?
 उ: हाँ, आप निःशुल्क परीक्षण डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/).
### प्रश्न: मैं जावा के लिए Aspose.Note के लिए समर्थन कैसे प्राप्त कर सकता हूं?
 ए: पर जाएँ[जावा फोरम के लिए Aspose.Note](https://forum.aspose.com/c/note/28) सामुदायिक समर्थन के लिए.
### प्रश्न: मैं जावा के लिए Aspose.Note के लिए विस्तृत दस्तावेज़ कहां पा सकता हूं?
 ए: का संदर्भ लें[प्रलेखन](https://reference.aspose.com/note/java/) विस्तृत जानकारी के लिए.
### प्रश्न: मैं जावा के लिए Aspose.Note का लाइसेंस कैसे खरीदूं?
 उत्तर: आप लाइसेंस खरीद सकते हैं[यहाँ](https://purchase.aspose.com/buy).