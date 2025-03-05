---
title: OneNote में रूट और उप पेजों के साथ दस्तावेज़ बनाएं
linktitle: OneNote में रूट और उप पेजों के साथ दस्तावेज़ बनाएं
second_title: Aspose.नोट जावा एपीआई
description: Java के लिए Aspose.Note का उपयोग करके OneNote में रूट और उप पृष्ठों के साथ एक दस्तावेज़ बनाएं। अपने नोट्स को कुशलतापूर्वक व्यवस्थित करने के लिए चरण-दर-चरण मार्गदर्शिका का पालन करें।
type: docs
weight: 11
url: /hi/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
---
## परिचय

इस ट्यूटोरियल में, हम जावा के लिए Aspose.Note का उपयोग करके OneNote में रूट और उप पेजों के साथ एक दस्तावेज़ बनाने की प्रक्रिया में आपका मार्गदर्शन करेंगे। इन चरणों का पालन करके, आप अपने OneNote दस्तावेज़ों को पदानुक्रमित संरचना के साथ कुशलतापूर्वक व्यवस्थित करने में सक्षम होंगे।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित शर्तें हैं:

1. जावा डेवलपमेंट किट (जेडीके): सुनिश्चित करें कि आपके सिस्टम पर जेडीके स्थापित है।
2. जावा के लिए Aspose.Note: जावा के लिए Aspose.Note को डाउनलोड और इंस्टॉल करें[वेबसाइट](https://purchase.aspose.com/buy).
3. एकीकृत विकास पर्यावरण (आईडीई): एक जावा आईडीई चुनें जैसे इंटेलीजे आईडीईए, एक्लिप्स, या नेटबीन्स।

## पैकेज आयात करें

अपने जावा प्रोजेक्ट में आवश्यक पैकेज आयात करके प्रारंभ करें:

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

## चरण 1: दस्तावेज़ निर्देशिका सेट करें

उस निर्देशिका को परिभाषित करें जहाँ आप अपना OneNote दस्तावेज़ सहेजना चाहते हैं:

```java
String dataDir = "Your Document Directory";
```

## चरण 2: दस्तावेज़ ऑब्जेक्ट बनाएँ

 त्वरित करें ए`Document` वस्तु:

```java
Document doc = new Document();
```

## चरण 3: पेज बनाएं

पेज ऑब्जेक्ट आरंभ करें और उनके स्तर निर्धारित करें:

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## चरण 4: पेजों में नोड्स जोड़ें

### प्रथम पृष्ठ पर नोड्स जोड़ना

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text = new RichText().append("First page.");
text.setParagraphStyle(textStyle);

outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page1.appendChildLast(outline);
```

### दूसरे पृष्ठ पर नोड्स जोड़ना

```java
Outline outline2 = new Outline();
OutlineElement outlineElem2 = new OutlineElement();
ParagraphStyle textStyle2 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text2 = new RichText().append("Second page.");
text2.setParagraphStyle(textStyle2);

outlineElem2.appendChildLast(text2);
outline2.appendChildLast(outlineElem2);
page2.appendChildLast(outline2);
```

### तीसरे पृष्ठ पर नोड्स जोड़ना

```java
Outline outline3 = new Outline();
OutlineElement outlineElem3 = new OutlineElement();
ParagraphStyle textStyle3 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Broadway")
                                    .setFontSize(10);

RichText text3 = new RichText().append("Third page.");
text3.setParagraphStyle(textStyle3);

outlineElem3.appendChildLast(text3);
outline3.appendChildLast(outlineElem3);
page3.appendChildLast(outline3);
```

## चरण 5: दस्तावेज़ में पेज जोड़ें

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## चरण 6: दस्तावेज़ सहेजें

OneNote दस्तावेज़ सहेजें:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // अपवाद संभालें
}
```

बधाई हो! आपने जावा के लिए Aspose.Note का उपयोग करके OneNote में रूट और उप पृष्ठों के साथ सफलतापूर्वक एक दस्तावेज़ बनाया है।

## निष्कर्ष

बेहतर प्रबंधन और नेविगेशन के लिए अपने OneNote दस्तावेज़ों को पदानुक्रमित संरचना के साथ व्यवस्थित करना आवश्यक है। जावा के लिए Aspose.Note के साथ, आप कुशलतापूर्वक रूट और उप पृष्ठों के साथ दस्तावेज़ बना सकते हैं, जो आपके नोट्स के लिए एक स्पष्ट और व्यवस्थित लेआउट प्रदान करता है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं जावा के लिए Aspose.Note का उपयोग करके उप-पृष्ठों के कई स्तर बना सकता हूँ?

उ1: हां, आप प्रत्येक पृष्ठ के लिए उचित स्तर निर्धारित करके उप-पृष्ठों के कई स्तर बना सकते हैं।

### Q2: क्या जावा के लिए Aspose.Note विभिन्न जावा आईडीई के साथ संगत है?

A2: हाँ, Java के लिए Aspose.Note IntelliJ IDEA, Eclipse और NetBeans जैसे लोकप्रिय Java IDE के साथ संगत है।

### Q3: क्या मैं अपने OneNote दस्तावेज़ में टेक्स्ट के स्वरूपण को अनुकूलित कर सकता हूँ?

उ3: हाँ, आप जावा की समृद्ध पाठ सुविधाओं के लिए Aspose.Note का उपयोग करके फ़ॉन्ट, रंग, आकार और अन्य स्वरूपण विकल्पों को अनुकूलित कर सकते हैं।

### Q4: क्या जावा के लिए Aspose.Note दस्तावेज़ों को विभिन्न स्वरूपों में सहेजने का समर्थन करता है?

A4: हाँ, Java के लिए Aspose.Note BMP, PDF, PNG और अन्य सहित विभिन्न स्वरूपों में दस्तावेज़ों को सहेजने का समर्थन करता है।

### Q5: क्या Java के लिए Aspose.Note का कोई परीक्षण संस्करण उपलब्ध है?

A5: हाँ, आप वेबसाइट से Java के लिए Aspose.Note का निःशुल्क परीक्षण संस्करण डाउनलोड कर सकते हैं।