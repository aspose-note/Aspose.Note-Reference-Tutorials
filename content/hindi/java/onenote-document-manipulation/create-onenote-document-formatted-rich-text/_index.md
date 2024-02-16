---
title: जावा में फ़ॉर्मेट किए गए रिच टेक्स्ट के साथ OneNote दस्तावेज़ बनाएं
linktitle: जावा में फ़ॉर्मेट किए गए रिच टेक्स्ट के साथ OneNote दस्तावेज़ बनाएं
second_title: Aspose.नोट जावा एपीआई
description: जानें कि जावा के लिए Aspose.Note का उपयोग करके जावा में प्रोग्रामेटिक रूप से बड़े पैमाने पर स्वरूपित OneNote दस्तावेज़ कैसे बनाएं। निर्बाध दस्तावेज़ स्वचालन के लिए हमारी चरण-दर-चरण मार्गदर्शिका का पालन करें।
type: docs
weight: 11
url: /hi/java/onenote-document-manipulation/create-onenote-document-formatted-rich-text/
---
## परिचय

प्रोग्रामेटिक रूप से बड़े पैमाने पर स्वरूपित OneNote दस्तावेज़ बनाना उन डेवलपर्स के लिए एक शक्तिशाली उपकरण हो सकता है जो जावा अनुप्रयोगों में दस्तावेज़ निर्माण कार्यों को स्वचालित करना चाहते हैं। जावा के लिए Aspose.Note इसे निर्बाध रूप से प्राप्त करने के लिए सुविधाओं और कार्यात्मकताओं का एक व्यापक सेट प्रदान करता है। इस ट्यूटोरियल में, हम जावा के लिए Aspose.Note का उपयोग करके स्वरूपित रिच टेक्स्ट के साथ OneNote दस्तावेज़ बनाने की प्रक्रिया में आपका मार्गदर्शन करेंगे।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ स्थापित हैं:

1. जावा डेवलपमेंट किट (जेडीके): सुनिश्चित करें कि आपके सिस्टम पर जेडीके स्थापित है।
2.  जावा JAR के लिए Aspose.Note: जावा JAR फ़ाइल के लिए Aspose.Note को डाउनलोड करें और अपने प्रोजेक्ट में शामिल करें। आप इसे यहां से प्राप्त कर सकते हैं[लिंक को डाउनलोड करें](https://releases.aspose.com/note/java/).
3. एकीकृत विकास पर्यावरण (आईडीई): अपनी पसंदीदा आईडीई जैसे इंटेलीजे आईडीईए या एक्लिप्स का उपयोग करें।

## पैकेज आयात करें

सबसे पहले, आपको अपने जावा प्रोजेक्ट में आवश्यक पैकेज आयात करने होंगे। अपनी जावा फ़ाइल की शुरुआत में निम्नलिखित आयात विवरण जोड़ें:

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

## चरण 1: दस्तावेज़ और पेज सेट करें

आइए दस्तावेज़ और पृष्ठ ऑब्जेक्ट को प्रारंभ करके प्रारंभ करें:

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

## चरण 2: फ़ॉर्मेटिंग के साथ शीर्षक बनाएं

अब, आइए स्वरूपित पाठ के साथ एक शीर्षक बनाएं:

```java
Title title = new Title();
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);

RichText titleText = new RichText().append("Title!");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
```

## चरण 3: फ़ॉर्मेटिंग के साथ रिच टेक्स्ट बनाएं

आगे, आइए विभिन्न स्वरूपण शैलियों के साथ समृद्ध टेक्स्ट बनाएं:

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();

TextStyle textStyleForHelloWord = new TextStyle()
                                        .setFontColor(Color.red)
                                        .setFontName("Arial")
                                        .setFontSize(10);

TextStyle textStyleForOneNoteWord = new TextStyle()
                                        .setFontColor(Color.green)
                                        .setFontName("Calibri")
                                        .setFontSize(10)
                                        .setItalic(true);

TextStyle textStyleForTextWord = new TextStyle()
                                        .setFontColor(Color.blue)
                                        .setFontName("Arial")
                                        .setFontSize(15)
                                        .setBold(true)
                                        .setItalic(true);

RichText text = new RichText()
        .append("Hello", textStyleForHelloWord)
        .append(" OneNote", textStyleForOneNoteWord)
        .append(" text", textStyleForTextWord)
        .append("!", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
```

## चरण 4: पेज और दस्तावेज़ में तत्व जोड़ें

अब, आइए पृष्ठ में शीर्षक और समृद्ध पाठ जोड़ें और तत्वों की रूपरेखा तैयार करें:

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.setTitle(title);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## चरण 5: दस्तावेज़ सहेजें

अंत में, बनाए गए OneNote दस्तावेज़ को सहेजें:

```java
doc.save(dataDir + "CreateOneNoteDocument_out.pdf", SaveFormat.Pdf);
```

## निष्कर्ष

इस ट्यूटोरियल में, हमने सीखा कि जावा के लिए Aspose.Note का उपयोग करके जावा में स्वरूपित रिच टेक्स्ट के साथ OneNote दस्तावेज़ कैसे बनाया जाए। इन चरण-दर-चरण निर्देशों का पालन करके, आप अपनी दस्तावेज़ स्वचालन क्षमताओं को बढ़ाते हुए आसानी से प्रोग्रामेटिक रूप से अनुकूलित OneNote दस्तावेज़ तैयार कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं फ़ॉन्ट शैलियों को और अधिक अनुकूलित कर सकता हूँ?

A1: हां, आप अपनी आवश्यकताओं के अनुरूप विभिन्न गुणों जैसे फ़ॉन्ट रंग, आकार, शैली इत्यादि को समायोजित कर सकते हैं।

### Q2: क्या जावा के लिए Aspose.Note सभी जावा आईडीई के साथ संगत है?

उ2: हां, आप जावा के लिए Aspose.Note का उपयोग किसी भी जावा आईडीई के साथ कर सकते हैं जो जावा विकास का समर्थन करता है।

### Q3: क्या मैं इस कार्यक्षमता को वेब अनुप्रयोगों में एकीकृत कर सकता हूँ?

A3: बिल्कुल, जावा के लिए Aspose.Note को गतिशील दस्तावेज़ निर्माण के लिए वेब अनुप्रयोगों में सहजता से एकीकृत किया जा सकता है।

### Q4: क्या जावा के लिए Aspose.Note का उपयोग करने के लिए कोई लाइसेंसिंग आवश्यकताएं हैं?

उ4: हां, आपको वाणिज्यिक परियोजनाओं में जावा के लिए Aspose.Note का उपयोग करने के लिए लाइसेंस प्राप्त करने की आवश्यकता है। हालाँकि, आप परीक्षण उद्देश्यों के लिए अस्थायी लाइसेंस का भी उपयोग कर सकते हैं।

### Q5: क्या Java के लिए Aspose.Note OneNote के अलावा अन्य दस्तावेज़ प्रारूपों का समर्थन करता है?

A5: हां, Java के लिए Aspose.Note पीडीएफ, HTML और छवि प्रारूपों सहित विभिन्न दस्तावेज़ प्रारूपों का समर्थन करता है।
