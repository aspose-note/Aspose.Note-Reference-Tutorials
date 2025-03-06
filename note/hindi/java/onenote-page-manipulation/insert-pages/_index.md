---
title: OneNote में पृष्ठ सम्मिलित करें - Aspose.Note
linktitle: OneNote में पृष्ठ सम्मिलित करें - Aspose.Note
second_title: Aspose.नोट जावा एपीआई
description: जावा के लिए Aspose.Note का उपयोग करके प्रोग्रामेटिक रूप से OneNote दस्तावेज़ों में पेज सम्मिलित करना सीखें। चरण-दर-चरण निर्देशों के साथ व्यापक ट्यूटोरियल।
weight: 16
url: /hi/java/onenote-page-manipulation/insert-pages/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote में पृष्ठ सम्मिलित करें - Aspose.Note

## परिचय

इस ट्यूटोरियल में, हम सीखेंगे कि जावा के लिए Aspose.Note का उपयोग करके OneNote दस्तावेज़ में पेज कैसे सम्मिलित करें।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:
1. आपके सिस्टम पर जावा डेवलपमेंट किट (जेडीके) स्थापित है।
2.  जावा लाइब्रेरी के लिए Aspose.Note डाउनलोड किया गया। आप इसे यहां से डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/note/java/).
3. एकीकृत विकास पर्यावरण (आईडीई) जैसे इंटेलीजे आईडीईए या एक्लिप्स स्थापित।

## पैकेज आयात करें

सबसे पहले, आपको अपनी जावा फ़ाइल में आवश्यक पैकेज आयात करने होंगे:

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

## चरण 1: एक दस्तावेज़ ऑब्जेक्ट बनाएँ

 आरंभ करें a`Document` वस्तु:

```java
Document doc = new Document();
```

## चरण 2: पेज ऑब्जेक्ट आरंभ करें

 प्रारंभ`Page` वस्तुएं और उनके स्तर निर्धारित करें:

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## चरण 3: पेजों में नोड्स जोड़ें

प्रत्येक पृष्ठ के लिए, वांछित सामग्री के साथ नोड्स जोड़ें:

```java
// प्रथम पृष्ठ पर नोड्स जोड़ना
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

// अन्य पृष्ठों के लिए समान चरण दोहराएँ
```

## चरण 4: दस्तावेज़ में पेज जोड़ें

बनाए गए पृष्ठों को OneNote दस्तावेज़ में जोड़ें:

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## चरण 5: दस्तावेज़ सहेजें

दस्तावेज़ को वांछित प्रारूप में सहेजें:

```java
String dataDir = "Your Document Directory";

doc.save(dataDir + "InsertPages_out.bmp" , SaveFormat.Bmp);
doc.save(dataDir + "InsertPages_out.pdf", SaveFormat.Pdf);
doc.save(dataDir + "InsertPages_out.gif", SaveFormat.Gif);
doc.save(dataDir + "InsertPages_out.jpeg", SaveFormat.Jpeg);
doc.save(dataDir + "InsertPages_out.png", SaveFormat.Png);
doc.save(dataDir + "InsertPages_out.tiff", SaveFormat.Tiff);

System.out.println("Files Saved Successfully!");
```

## निष्कर्ष

इस ट्यूटोरियल में, हमने सीखा है कि जावा के लिए Aspose.Note का उपयोग करके OneNote दस्तावेज़ में पेज कैसे सम्मिलित करें। दिए गए चरणों का पालन करके, आप OneNote दस्तावेज़ों को प्रोग्रामेटिक रूप से कुशलतापूर्वक प्रबंधित कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं Java के लिए Aspose.Note का उपयोग करके OneNote दस्तावेज़ में छवियां सम्मिलित कर सकता हूं?

A1: हां, आप Aspose.Note द्वारा प्रदान की गई उपयुक्त कक्षाओं और विधियों का उपयोग करके छवियां सम्मिलित कर सकते हैं।

### Q2: क्या Aspose.Note OneNote के विभिन्न संस्करणों के साथ संगत है?

A2: Aspose.Note निर्बाध एकीकरण और कार्यक्षमता सुनिश्चित करते हुए, OneNote के विभिन्न संस्करणों के साथ अनुकूलता प्रदान करता है।

### Q3: Aspose.Note के साथ काम करते समय मैं त्रुटियों या अपवादों को कैसे संभाल सकता हूँ?

A3: आप अपवादों को शानदार ढंग से प्रबंधित करने और अपने एप्लिकेशन की स्थिरता बनाए रखने के लिए ट्राई-कैच ब्लॉक जैसी त्रुटि प्रबंधन तकनीकों को लागू कर सकते हैं।

### Q4: क्या Aspose.Note क्रॉस-प्लेटफ़ॉर्म विकास का समर्थन करता है?

उ4: हाँ, आप विंडोज़, लिनक्स और मैकओएस सहित विभिन्न प्लेटफार्मों पर जावा के लिए Aspose.Note का उपयोग करके एप्लिकेशन विकसित कर सकते हैं।

### Q5: क्या मैं OneNote में सम्मिलित पृष्ठों के स्वरूप को अनुकूलित कर सकता हूँ?

A5: बिल्कुल, Aspose.Note आपकी विशिष्ट आवश्यकताओं को पूरा करने के लिए पेज लेआउट, शैलियों और सामग्री को अनुकूलित करने के लिए व्यापक विकल्प प्रदान करता है।
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
