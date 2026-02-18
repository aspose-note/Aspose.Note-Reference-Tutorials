---
date: 2026-02-18
description: Aspose.Note का उपयोग करके जावा में OneNote दस्तावेज़ बनाना, रिच टेक्स्ट
  फॉर्मेट करना और PDF के रूप में सहेजना सीखें। सहज ऑटोमेशन के लिए चरण‑दर‑चरण गाइड।
linktitle: Create OneNote document and save as PDF in Java
second_title: Aspose.Note Java API
title: Java में OneNote दस्तावेज़ बनाएं और PDF के रूप में सहेजें
url: /hi/java/onenote-document-manipulation/create-onenote-document-formatted-rich-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java में OneNote दस्तावेज़ बनाएं और PDF के रूप में सहेजें

## Introduction

यदि आपको **OneNote दस्तावेज़ बनाना** है और **OneNote को PDF के रूप में सहेजना** है जबकि रिच‑टेक्स्ट फ़ॉर्मेटिंग को बनाए रखें, तो आप सही जगह पर आए हैं। इस ट्यूटोरियल में हम OneNote दस्तावेज़ बनाने, कस्टम स्टाइल लागू करने, और Aspose.Note for Java का उपयोग करके सीधे PDF में एक्सपोर्ट करने की प्रक्रिया देखेंगे। अंत तक आपके पास एक पुन: उपयोग योग्य स्निपेट होगा जिसे आप किसी भी Java प्रोजेक्ट में डालकर परिष्कृत OneNote‑to‑PDF रूपांतरण को स्वचालित कर सकते हैं।

## Quick Answers
- **यह ट्यूटोरियल क्या सिखाता है?** कैसे स्टाइल्ड टेक्स्ट के साथ OneNote दस्तावेज़ बनाएं और उसे PDF के रूप में सहेजें।  
- **कौनसी लाइब्रेरी आवश्यक है?** Aspose.Note for Java (आधिकारिक साइट से डाउनलोड करने योग्य)।  
- **क्या मुझे लाइसेंस चाहिए?** परीक्षण के लिए एक अस्थायी लाइसेंस काम करता है; उत्पादन के लिए पूर्ण लाइसेंस आवश्यक है।  
- **मैं कौन सा IDE उपयोग कर सकता हूँ?** कोई भी Java IDE—IntelliJ IDEA, Eclipse, या NetBeans।  
- **क्या मैं आउटपुट फ़ॉर्मेट बदल सकता हूँ?** हाँ, Aspose.Note PDF, HTML, PNG और अधिक को सपोर्ट करता है।

## What is “save onenote pdf”?

OneNote को PDF के रूप में सहेजना का मतलब है OneNote पेज संरचना—टेक्स्ट, इमेज और फ़ॉर्मेटिंग सहित—को एक स्थिर PDF फ़ाइल में बदलना, जिसे किसी भी प्लेटफ़ॉर्म पर OneNote की आवश्यकता के बिना देखा जा सकता है।

## Why format rich text java?

Java में सीधे **रिच टेक्स्ट फ़ॉर्मेट** लागू करने से आप ऐसे दस्तावेज़ बना सकते हैं जो पेशेवर दिखते हैं और आपके ब्रांड गाइडलाइन के अनुरूप होते हैं, बिना मैन्युअल एडिटिंग के।

## Prerequisites

1. **Java Development Kit (JDK)** – कोई भी नवीनतम संस्करण (8 या उससे ऊपर)।  
2. **Aspose.Note for Java JAR** – इसे [download link](https://releases.aspose.com/note/java/) से डाउनलोड करें।  
3. **IDE** – IntelliJ IDEA, Eclipse, या कोई भी एडिटर जो आप पसंद करते हैं।  

## Import Packages

शुरू करने से पहले, आवश्यक क्लासेस को अपने Java फ़ाइल में इम्पोर्ट करें:

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

## How to create OneNote document – Step‑by‑step guide

### Step 1: Set Up Document and Page

सभी सामग्री रखने वाले `Document` और `Page` ऑब्जेक्ट को इनिशियलाइज़ करें:

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

### Step 2: Create Title with Formatting

एक टाइटल एलिमेंट जोड़ें और उसकी उपस्थिति को नियंत्रित करने के लिए **set paragraph style** लागू करें:

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

### Step 3: Create Rich Text with Formatting

यहाँ हम कई `TextStyle` ऑब्जेक्ट्स का उपयोग करके रिच‑टेक्स्ट कंटेंट बनाते हैं ताकि **रिच टेक्स्ट फ़ॉर्मेटिंग** दिखा सकें:

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

### Step 4: Add Elements to Page and Document

टाइटल और रिच टेक्स्ट को पेज हायरार्की में संयोजित करें:

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.setTitle(title);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

### Step 5: Save Document – export onenote pdf

अंत में, OneNote दस्तावेज़ को PDF फ़ाइल के रूप में एक्सपोर्ट करें:

```java
doc.save(dataDir + "CreateOneNoteDocument_out.pdf", SaveFormat.Pdf);
```

## Common Issues and Solutions

| समस्या | समाधान |
|-------|----------|
| **फ़ाइल नहीं मिली** | `dataDir` किसी मौजूदा फ़ोल्डर की ओर इशारा करता है और आपके पास लिखने की अनुमति है, यह सत्यापित करें। |
| **फ़ॉन्ट गायब** | सुनिश्चित करें कि आप जिन फ़ॉन्ट्स का उल्लेख करते हैं (जैसे *Calibri*) होस्ट मशीन पर इंस्टॉल हैं। |
| **लाइसेंस लागू नहीं हुआ** | `Document` बनाने से पहले अपना Aspose लाइसेंस लोड करें ताकि मूल्यांकन वॉटरमार्क न आएँ। |

## Frequently Asked Questions

**प्रश्न: क्या मैं फ़ॉन्ट स्टाइल को और कस्टमाइज़ कर सकता हूँ?**  
उत्तर: हाँ, आप `TextStyle` और `ParagraphStyle` क्लासेस के माध्यम से अंडरलाइन, स्ट्राइक‑थ्रू, और टेक्स्ट अलाइनमेंट जैसी अतिरिक्त प्रॉपर्टीज़ को समायोजित कर सकते हैं।

**प्रश्न: क्या Aspose.Note for Java सभी Java IDEs के साथ संगत है?**  
उत्तर: बिल्कुल। जब तक IDE मानक Java विकास को सपोर्ट करता है, आप Aspose.Note JAR को प्रोजेक्ट के क्लासपाथ में जोड़ सकते हैं।

**प्रश्न: क्या मैं इस फ़ंक्शनैलिटी को वेब एप्लिकेशन में इंटीग्रेट कर सकता हूँ?**  
उत्तर: हाँ, वही कोड सर्वलेट‑आधारित या Spring Boot एप्लिकेशन में काम करता है, जिससे सर्वर साइड पर डायनामिक OneNote‑to‑PDF जेनरेशन संभव होता है।

**प्रश्न: Aspose.Note for Java उपयोग करने के लिए लाइसेंसिंग आवश्यकताएँ क्या हैं?**  
उत्तर: उत्पादन उपयोग के लिए एक व्यावसायिक लाइसेंस आवश्यक है। मूल्यांकन और परीक्षण के लिए एक अस्थायी लाइसेंस उपलब्ध है।

**प्रश्न: क्या Aspose.Note for Java OneNote के अलावा अन्य दस्तावेज़ फ़ॉर्मेट्स को सपोर्ट करता है?**  
उत्तर: यह PDF, HTML, PNG, JPEG, और कई अन्य एक्सपोर्ट फ़ॉर्मेट्स को सपोर्ट करता है, जिससे आप OneNote पेज को आवश्यक फ़ॉर्मेट में बदलने की लचीलापन प्राप्त करते हैं।

## Conclusion

इस गाइड में हमने दिखाया कि कैसे Aspose.Note for Java का उपयोग करके **OneNote दस्तावेज़ बनाएं**, **रिच टेक्स्ट फ़ॉर्मेटिंग** लागू करें, और **OneNote को PDF के रूप में सहेजें**। चरण‑दर‑चरण निर्देशों का पालन करके आप परिष्कृत OneNote दस्तावेज़ों के निर्माण को स्वचालित कर सकते हैं और उन्हें किसी भी Java‑आधारित समाधान में PDF में बदल सकते हैं।

---

**अंतिम अपडेट:** 2026-02-18  
**परीक्षण किया गया:** Aspose.Note for Java 24.11 (लेखन के समय नवीनतम)  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}