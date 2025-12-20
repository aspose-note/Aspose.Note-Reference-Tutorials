---
date: 2025-12-20
description: जावा के साथ Aspose.Note लाइब्रेरी का उपयोग करके OneNote को PDF के रूप
  में सहेजना और OneNote में हाइपरलिंक जोड़ना सीखें। OneNote से आसानी से PDF बनाएं।
linktitle: Save OneNote as PDF and Add Hyperlink in OneNote with Java
second_title: Aspose.Note Java API
title: OneNote को PDF के रूप में सहेजें और Java के साथ OneNote में हाइपरलिंक जोड़ें
url: /hi/java/onenote-hyperlinks-images/add-hyperlink/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java के साथ OneNote को PDF के रूप में सहेजें और OneNote में हाइपरलिंक जोड़ें

## Introduction

अपने OneNote दस्तावेज़ों में हाइपरलिंक जोड़ना और साथ ही उन्हें PDF के रूप में सहेजना आपके नोट्स की इंटरैक्टिविटी को काफी बढ़ा सकता है और शेयरिंग को आसान बना सकता है। इस ट्यूटोरियल में आप **OneNote को PDF के रूप में कैसे सहेजें** और Java तथा Aspose.Note लाइब्रेरी का उपयोग करके क्लिक करने योग्य लिंक एम्बेड करना सीखेंगे। चलिए साथ में चरणों को देखते हैं!

## Quick Answers
- **क्या मैं Java के साथ OneNote को PDF के रूप में सहेज सकता हूँ?** हाँ, Aspose.Note for Java एक ही `save` कॉल से PDF जेनरेट करता है।
- **हाइपरलिंक कैसे एम्बेड करें?** `RichText` सेगमेंट पर `TextStyle.setHyperlinkAddress` का उपयोग करें।
- **पूर्वापेक्षाएँ क्या हैं?** JDK 8+ और Aspose.Note for Java लाइब्रेरी।
- **कौन से आउटपुट फॉर्मेट समर्थित हैं?** PDF, DOCX, XPS, और अधिक।
- **प्रोडक्शन के लिए लाइसेंस आवश्यक है?** हाँ, गैर‑इवैल्यूएशन उपयोग के लिए एक कमर्शियल लाइसेंस आवश्यक है।

## What is “save onenote as pdf”?

OneNote नोटबुक को PDF के रूप में सहेजने से आपके नोट्स का एक पोर्टेबल, केवल‑पढ़ने योग्य संस्करण बनता है जिसे किसी भी डिवाइस पर OneNote ऐप के बिना खोला जा सकता है। यह विशेष रूप से आर्काइविंग, प्रिंटिंग, या उन उपयोगकर्ताओं के साथ शेयर करने के लिए उपयोगी है जिनके पास OneNote नहीं है।

## Why generate PDF from OneNote with Aspose.Note Java?

- **पूर्ण सटीकता:** फॉर्मेटिंग, इमेज़ और हाइपरलिंक को बरकरार रखता है।
- **प्रोग्रामेटिक नियंत्रण:** बैकएंड सर्विसेज़ में बैच कन्वर्ज़न को ऑटोमेट करें।
- **क्रॉस‑प्लेटफ़ॉर्म:** Windows, Linux, और macOS पर काम करता है।
- **रिच API:** सहेजने से पहले सामग्री को आसानी से जोड़ें या संशोधित करें।

## Prerequisites

Before we begin, ensure you have the following prerequisites installed and set up on your system:

### Java Development Kit (JDK)

Make sure you have Java Development Kit (JDK) installed on your system. You can download and install JDK from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).

### Aspose.Note for Java Library

Download and install the Aspose.Note for Java library. You can find the documentation and download link [here](https://reference.aspose.com/note/java/).

## Import Packages

To start with, import the necessary packages required for working with Aspose.Note for Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

Now, let's break down the provided example into multiple steps:

## Step 1: Set Up Document Structure

First, create a new document and a page where the content will live.

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
Title title = new Title();
```

## Step 2: Define Default Text Style

Define a default paragraph style that will be applied to most text elements.

```java
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                            .setFontName("Arial")
                                            .setFontSize(10)
                                            .setFontColor(java.awt.Color.GRAY);
```

## Step 3: Set Title Text

Create a title for the page and apply the default style.

```java
RichText titleText = new RichText().append("Title");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
page.setTitle(title);
```

## Step 4: Create Outline and Outline Elements

Outlines act like containers for paragraphs and other elements.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## Step 5: Define Text Style for Hyperlink

Here we define a red‑colored style that will be used for the clickable part.

```java
TextStyle textStyleRed = new TextStyle()
                                    .setFontName("Arial")
                                    .setFontSize(10)
                                    .setFontColor(java.awt.Color.red);
```

## Step 6: Add Text with Hyperlink

Now we build a `RichText` object that mixes normal text and a hyperlink.  
The `setHyperlinkAddress` method tells Aspose.Note that this segment should be clickable.

```java
RichText text = new RichText()
                            .append("This is ", textStyleRed)
                            .append("hyperlink", new TextStyle().setHyperlinkAddress("www.google.com"))
                            .append(". This text is not a hyperlink.", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
outlineElem.appendChildLast(text);
```

## Step 7: Add Outline to Page and Page to Document

Attach the outline element to the outline, the outline to the page, and finally the page to the document.

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## Step 8: Save the Document as PDF

The final step is to save the OneNote document as a PDF file. This is where the primary keyword **save onenote as pdf** comes into play.

```java
doc.save(dataDir + "AddHyperlink_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "AddHyperlink_out.pdf");
```

## Conclusion

बधाई हो! आपने सफलतापूर्वक **OneNote को PDF के रूप में सहेजा** और Java तथा Aspose.Note लाइब्रेरी का उपयोग करके डॉक्यूमेंट में हाइपरलिंक जोड़ा। यह क्षमता आपको सीधे अपने OneNote कंटेंट से इंटरैक्टिव, शेयर करने योग्य PDFs बनाने देती है।

## FAQ's

### Q1: क्या Aspose.Note सभी Java संस्करणों के साथ संगत है?

A1: हाँ, Aspose.Note for Java सभी प्रमुख Java संस्करणों का समर्थन करता है, जिसमें JDK 8 और उससे ऊपर शामिल हैं।

### Q2: क्या मैं Aspose.Note का उपयोग करके एक ही डॉक्यूमेंट में कई हाइपरलिंक जोड़ सकता हूँ?

A2: बिल्कुल! आप Aspose.Note for Java का उपयोग करके अपने OneNote डॉक्यूमेंट में जितने भी हाइपरलिंक चाहिए, जोड़ सकते हैं।

### Q3: क्या Aspose.Note अन्य प्रोग्रामिंग भाषाओं के लिए समर्थन देता है?

A3: हाँ, Aspose.Note विभिन्न प्रोग्रामिंग भाषाओं के लिए लाइब्रेरी प्रदान करता है, जिसमें .NET, Python, और Android शामिल हैं।

### Q4: क्या Aspose.Note को मौजूदा Java प्रोजेक्ट्स में इंटीग्रेट करना आसान है?

A4: हाँ, Aspose.Note को आपके Java प्रोजेक्ट्स में इंटीग्रेट करना सीधा और अच्छी तरह से दस्तावेज़ीकृत है, जिससे शुरू करना आसान हो जाता है।

### Q5: Aspose.Note का उपयोग करने के लिए अधिक मदद और संसाधन कहाँ मिल सकते हैं?

A5: आप विस्तृत दस्तावेज़ीकरण, ट्यूटोरियल और समुदाय समर्थन [Aspose.Note फ़ोरम](https://forum.aspose.com/c/note/28) पर पा सकते हैं।

## Frequently Asked Questions

**प्रश्न: हाइपरलिंक की उपस्थिति को कैसे कस्टमाइज़ करूँ?**  
उत्तर: `setHyperlinkAddress` कॉल करने से पहले `TextStyle` प्रॉपर्टीज़ जैसे `setFontColor`, `setUnderline`, या `setFontName` का उपयोग करें।

**प्रश्न: क्या मैं डॉक्यूमेंट को PDF के अलावा अन्य फॉर्मेट में सहेज सकता हूँ?**  
उत्तर: हाँ, Aspose.Note DOCX, XPS, HTML, और कई अन्य एक्सपोर्ट फॉर्मेट का समर्थन करता है।

**प्रश्न: यदि मुझे मौजूदा OneNote फ़ाइल में हाइपरलिंक जोड़ना हो तो क्या करें?**  
उत्तर: मौजूदा फ़ाइल को `new Document("input.one")` से लोड करें, दिखाए अनुसार सामग्री संशोधित करें, और फिर इच्छित फॉर्मेट के साथ `save` कॉल करें।

**प्रश्न: क्या PDF जनरेट होने के बाद हाइपरलिंक को प्रोग्रामेटिकली खोलने का कोई तरीका है?**  
उत्तर: PDF व्यूअर स्वचालित रूप से क्लिक करने योग्य लिंक को संभालेगा; अतिरिक्त कोड की आवश्यकता नहीं है।

**प्रश्न: विकास उपयोग के लिए क्या मुझे लाइसेंस चाहिए?**  
उत्तर: विकास और परीक्षण के लिए एक अस्थायी इवैल्यूएशन लाइसेंस पर्याप्त है, लेकिन प्रोडक्शन डिप्लॉयमेंट के लिए पूर्ण लाइसेंस आवश्यक है।

---

**अंतिम अपडेट:** 2025-12-20  
**टेस्टेड विथ:** Aspose.Note for Java 23.12  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}