---
date: 2025-12-09
description: Aspose.Note for Java का उपयोग करके जावा में फ़ॉर्मेटेड रिच टेक्स्ट के
  साथ OneNote को PDF के रूप में सहेजना सीखें। सहज दस्तावेज़ ऑटोमेशन के लिए हमारे चरण‑दर‑चरण
  गाइड का पालन करें।
linktitle: Save OneNote as PDF with Formatted Rich Text in Java
second_title: Aspose.Note Java API
title: जावा में फ़ॉर्मेटेड रिच टेक्स्ट के साथ वननोट को पीडीएफ के रूप में सहेजें
url: /hi/java/onenote-document-manipulation/create-onenote-document-formatted-rich-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java में फ़ॉर्मेटेड रिच टेक्स्ट के साथ OneNote को PDF के रूप में सहेजें

## परिचय

यदि आपको **save OneNote as PDF** करते समय रिच‑टेक्स्ट फ़ॉर्मेटिंग को बनाए रखना है, तो आप सही जगह पर आए हैं। इस ट्यूटोरियल में हम OneNote दस्तावेज़ बनाना, कस्टम स्टाइल लागू करना, और Aspose.Note for Java का उपयोग करके सीधे PDF में एक्सपोर्ट करना सीखेंगे। अंत तक आपके पास एक पुन: उपयोग योग्य कोड स्निपेट होगा जिसे आप किसी भी Java प्रोजेक्ट में डाल कर पॉलिश्ड OneNote‑to‑PDF कन्वर्ज़न को ऑटोमेट कर सकते हैं।

## त्वरित उत्तर
- **इस ट्यूटोरियल में क्या सिखाया जाता है?** How to create a OneNote document with styled text and save it as a PDF.  
- **कौन सी लाइब्रेरी आवश्यक है?** Aspose.Note for Java (downloadable from the official site).  
- **क्या मुझे लाइसेंस चाहिए?** A temporary license works for testing; a full license is required for production.  
- **मैं कौन सा IDE उपयोग कर सकता हूँ?** Any Java IDE—IntelliJ IDEA, Eclipse, or NetBeans.  
- **क्या मैं आउटपुट फ़ॉर्मेट बदल सकता हूँ?** Yes, Aspose.Note supports PDF, HTML, PNG, and more.

## “save onenote as pdf” क्या है?
Saving OneNote as PDF का अर्थ है OneNote पेज संरचना—टेक्स्ट, इमेज और फ़ॉर्मेटिंग सहित—को एक स्थिर PDF फ़ाइल में बदलना, जिसे किसी भी प्लेटफ़ॉर्म पर OneNote की आवश्यकता के बिना देखा जा सकता है।

## जावा में रिच टेक्स्ट फ़ॉर्मेट क्यों?
जावा में सीधे रिच‑टेक्स्ट फ़ॉर्मेटिंग (फ़ॉन्ट, रंग, स्टाइल) लागू करने से आप ऐसे दस्तावेज़ बना सकते हैं जो प्रोफ़ेशनल दिखते हैं और आपके ब्रांड गाइडलाइन के अनुरूप होते हैं, बिना मैन्युअल एडिटिंग के।

## आवश्यकताएँ

1. **Java Development Kit (JDK)** – कोई भी नवीनतम संस्करण (8 या उससे ऊपर)।  
2. **Aspose.Note for Java JAR** – इसे [download link](https://releases.aspose.com/note/java/) से डाउनलोड करें।  
3. **IDE** – IntelliJ IDEA, Eclipse, या कोई भी एडिटर जो आप पसंद करें।  

## पैकेज इम्पोर्ट करें

सबसे पहले, आपको अपने Java प्रोजेक्ट में आवश्यक पैकेज इम्पोर्ट करने होंगे। अपने Java फ़ाइल की शुरुआत में निम्नलिखित इम्पोर्ट स्टेटमेंट्स जोड़ें:

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

## चरण 1: दस्तावेज़ और पेज सेट अप करें

आइए `Document` और `Page` ऑब्जेक्ट्स को इनिशियलाइज़ करके शुरू करते हैं:

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

## चरण 2: फ़ॉर्मेटिंग के साथ शीर्षक बनाएं

अब, फ़ॉर्मेटेड टेक्स्ट के साथ एक शीर्षक बनाते हैं:

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

अगले, विभिन्न फ़ॉर्मेटिंग स्टाइल के साथ रिच टेक्स्ट बनाते हैं:

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

अब, शीर्षक और रिच टेक्स्ट को पेज और आउटलाइन तत्वों में जोड़ते हैं:

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.setTitle(title);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## चरण 5: दस्तावेज़ सहेजें

अंत में, बनाए गए OneNote दस्तावेज़ को PDF के रूप में सहेजें:

```java
doc.save(dataDir + "CreateOneNoteDocument_out.pdf", SaveFormat.Pdf);
```

## सामान्य समस्याएँ और समाधान

| समस्या | समाधान |
|-------|----------|
| **फ़ाइल नहीं मिली** | Verify `dataDir` points to an existing folder and you have write permissions. |
| **फ़ॉन्ट गायब** | Ensure the fonts you reference (e.g., *Calibri*) are installed on the host machine. |
| **लाइसेंस लागू नहीं हुआ** | Load your Aspose license before creating the `Document` to avoid evaluation watermarks. |

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या मैं फ़ॉन्ट स्टाइल को और कस्टमाइज़ कर सकता हूँ?**  
A: हाँ, आप `TextStyle` और `ParagraphStyle` क्लासेज़ के माध्यम से अंडरलाइन, स्ट्राइक‑थ्रू, और टेक्स्ट अलाइनमेंट जैसी अतिरिक्त प्रॉपर्टीज़ को समायोजित कर सकते हैं।

**Q: क्या Aspose.Note for Java सभी Java IDEs के साथ संगत है?**  
A: बिल्कुल। जब तक IDE मानक Java विकास का समर्थन करता है, आप Aspose.Note JAR को प्रोजेक्ट की क्लासपाथ में जोड़ सकते हैं।

**Q: क्या मैं इस फ़ंक्शनैलिटी को वेब एप्लिकेशन में इंटीग्रेट कर सकता हूँ?**  
A: हाँ, वही कोड सर्वलेट‑आधारित या Spring Boot एप्लिकेशन में काम करता है, जिससे सर्वर साइड पर डायनामिक OneNote‑to‑PDF जेनरेशन संभव होता है।

**Q: Aspose.Note for Java उपयोग करने के लिए लाइसेंसिंग आवश्यकताएँ हैं क्या?**  
A: उत्पादन उपयोग के लिए एक व्यावसायिक लाइसेंस आवश्यक है। मूल्यांकन और परीक्षण के लिए एक अस्थायी लाइसेंस उपलब्ध है।

**Q: क्या Aspose.Note for Java OneNote के अलावा अन्य दस्तावेज़ फ़ॉर्मेट्स को सपोर्ट करता है?**  
A: यह PDF, HTML, PNG, JPEG, और कई अन्य एक्सपोर्ट फ़ॉर्मेट्स को सपोर्ट करता है, जिससे आप OneNote पेज को अपनी आवश्यकता के अनुसार विभिन्न फ़ॉर्मेट्स में बदल सकते हैं।

## निष्कर्ष

इस गाइड में हमने Aspose.Note for Java का उपयोग करके फ़ॉर्मेटेड रिच‑टेक्स्ट के साथ **save One** करने का तरीका दिखाया। चरण‑दर‑चरण निर्देशों का पालन करके आप पॉलिश्ड OneNote दस्तावेज़ बना सकते हैं और उन्हें किसी भी Java‑आधारित समाधान में PDF में बदल सकते हैं।

---

**Last Updated:** 2025-12-09  
**परीक्षण किया गया:** Aspose.Note for Java 24.11 (latest at time of writing)  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}