---
date: 2026-01-23
description: Aspose.Note for Java का उपयोग करके OneNote में तालिका जोड़ते समय कॉलम
  की चौड़ाई को लॉक करना सीखें। कोड, टिप्स और अक्सर पूछे जाने वाले प्रश्नों के साथ
  चरण‑दर‑चरण गाइड।
linktitle: How to Lock Column in OneNote Table – Aspose.Note
second_title: Aspose.Note Java API
title: OneNote टेबल में कॉलम को लॉक करने का तरीका – Aspose.Note
url: /hi/java/onenote-table-manipulation/create-table-with-locked-columns/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote तालिका में कॉलम को लॉक कैसे करें – Aspose.Note

## Introduction
OneNote एक बहुमुखी नोट‑लेने वाला प्लेटफ़ॉर्म है, और Aspose.Note for Java आपको OneNote में तालिका जोड़ते समय **कॉलम को लॉक करने** की चौड़ाई को आसानी से सेट करने में मदद करता है। इस ट्यूटोरियल में आप एक पूर्ण, व्यावहारिक उदाहरण देखेंगे जो दिखाता है कि तालिका कॉलम की चौड़ाई कैसे सेट करें, उस चौड़ाई को लॉक करें, और OneNote तालिका की बॉर्डर को कस्टमाइज़ करें—सिर्फ कुछ लाइनों के Java कोड के साथ।

## Quick Answers
- **What does “lock column” mean?** यह कॉलम की चौड़ाई को स्थिर कर देता है ताकि उपयोगकर्ता OneNote में इसे री‑साइज़ न कर सके।  
- **Which library provides this feature?** Aspose.Note for Java.  
- **Do I need a license to run the sample?** मुफ़्त ट्रायल मूल्यांकन के लिए काम करता है; उत्पादन के लिए एक व्यावसायिक लाइसेंस आवश्यक है।  
- **Can I add more rows after locking the column?** हाँ, आप पंक्तियों को जोड़ते रह सकते हैं; लॉक की गई चौड़ाई लागू रहती है।  
- **What version of Java is supported?** Java 6 और उसके बाद के संस्करण।

## What is “how to lock column” in a OneNote table?
कॉलम को लॉक करना मतलब `TableColumn` ऑब्जेक्ट को एक निश्चित चौड़ाई असाइन करना और उसकी `LockedWidth` प्रॉपर्टी को `true` सेट करना है। यह अंतिम उपयोगकर्ताओं द्वारा आकस्मिक री‑साइज़िंग को रोकता है और आपका लेआउट सुसंगत रखता है।

## Why lock column width in OneNote?
- **Consistent layout** – आपके नोट्स हर डिवाइस पर समान दिखते हैं।  
- **Better readability** – लंबा टेक्स्ट एक पूर्वनिर्धारित कॉलम आकार में रैप होता है।  
- **Professional appearance** – लॉक किए गए कॉलम एक परिष्कृत, रिपोर्ट‑जैसी भावना देते हैं।

## Prerequisites
शुरू करने से पहले, सुनिश्चित करें कि निम्नलिखित तैयार हैं:

- [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html) installed on your machine.  
- [Aspose.Note for Java](https://downloads.aspose.com/note/java) library downloaded and added to your project’s classpath.

## Import Packages
अपने Java प्रोजेक्ट में, Aspose.Note के साथ काम करने के लिए आवश्यक पैकेज इम्पोर्ट करें:

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Step 1: Set Up Your Project
एक नया Java प्रोजेक्ट बनाएं (या मौजूदा का उपयोग करें) और Aspose.Note JAR फ़ाइलों को बिल्ड पाथ में जोड़ें। सुनिश्चित करें कि प्रोजेक्ट आपके स्थापित JDK के साथ संकलित हो।

## Step 2: Initialize Document and Page Objects
हम एक नया `Document` और एक `Page` बनाकर शुरू करते हैं जहाँ तालिका स्थित होगी।

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Create an object of the Document class
Document doc = new Document();
// Initialize Page class object
Page page = new Page();
```

## Step 3: Create Table Rows and Cells
यहाँ हम दो पंक्तियाँ बनाते हैं, प्रत्येक में एकल सेल होता है जिसमें कुछ नमूना टेक्स्ट होता है। यह दर्शाता है कि लॉक किया गया कॉलम छोटे और बड़े कंटेंट के साथ कैसे व्यवहार करता है।

```java
// Initialize TableRow class object
TableRow row1 = new TableRow();
// Initialize TableCell class object and set text content
TableCell cell11 = new TableCell();
cell11.appendChildLast(InsertTable.GetOutlineElementWithText("Small text"));
row1.appendChildLast(cell11);
// Initialize TableRow class object
TableRow row2 = new TableRow();
// Initialize TableCell class object and set text content
TableCell cell21 = new TableCell();
cell21.appendChildLast(InsertTable.GetOutlineElementWithText("Long   text    with    several   words and    spaces."));
row2.appendChildLast(cell21);
```

## Step 4: Create and Customize the Table
अब हम तालिका बनाते हैं, **set table column width**, **lock the column**, और **customize OneNote table borders**।

```java
// Initialize Table class object
Table table = new Table();
table.setBordersVisible(true);               // customize onenote table borders
TableColumn col = new TableColumn();
col.setWidth(200);                           // set table column width
col.setLockedWidth(true);                    // onenote table locked width
table.getColumns().addItem(col);
// Add rows
table.appendChildLast(row1);
table.appendChildLast(row2);
```

## Step 5: Add Table to Outline and Page
हम अब तालिका को एक `OutlineElement` से जोड़ते हैं और अंत में इसे पेज में जोड़ते हैं—यह **add outline element java** चरण है।

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
// Add table node
outlineElem.appendChildLast(table);
// Add outline element node
outline.appendChildLast(outlineElem);
// Add outline node
page.appendChildLast(outline);
// Add page node
doc.appendChildLast(page);
```

## Step 6: Save the Document
OneNote फ़ाइल (`.one`) को उस डायरेक्टरी में सहेजें जिसे आपने पहले निर्दिष्ट किया था।

```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```

बधाई हो! आपने Aspose.Note for Java का उपयोग करके लॉक किए गए कॉलम, निश्चित चौड़ाई, और कस्टमाइज़्ड बॉर्डर के साथ **OneNote में तालिका जोड़ने** को सफलतापूर्वक किया है।

## Common Issues and Solutions
| समस्या | समाधान |
|-------|----------|
| टेबल में कोई बॉर्डर नहीं दिख रहा है | Ensure `table.setBordersVisible(true);` is called. |
| पंक्तियों को जोड़ने के बाद कॉलम की चौड़ाई बदलती है | Verify `col.setLockedWidth(true);` **before** rows are appended. |
| फ़ाइल सहेजी नहीं गई | Check that `dataDir` points to a writable folder and ends with a valid filename. |

## Frequently Asked Questions

**Q: क्या Aspose.Note for Java सभी Java संस्करणों के साथ संगत है?**  
A: हाँ, यह Java 6 और उसके बाद के संस्करणों के साथ काम करता है, जिसमें Java 11 और Java 17 शामिल हैं।

**Q: क्या मैं तालिका की उपस्थिति को और अधिक कस्टमाइज़ कर सकता हूँ?**  
A: बिल्कुल! आप `Table` और `TableCell` प्रॉपर्टीज़ के माध्यम से बॉर्डर स्टाइल, सेल पैडिंग, बैकग्राउंड रंग, और अधिक संशोधित कर सकते हैं।

**Q: क्या खरीदने से पहले कोई ट्रायल संस्करण उपलब्ध है?**  
A: हाँ, आप Aspose.Note for Java की क्षमताओं को जानने के लिए [एक मुफ्त ट्रायल डाउनलोड कर सकते हैं](https://releases.aspose.com/)।

**Q: अतिरिक्त समर्थन या समुदाय चर्चा कहाँ मिल सकती है?**  
A: समर्थन और समुदाय चर्चा के लिए [Aspose.Note फ़ोरम](https://forum.aspose.com/c/note/28) पर जाएँ।

**Q: मैं Aspose.Note for Java के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूँ?**  
A: परीक्षण उद्देश्यों के लिए अस्थायी लाइसेंस प्राप्त करने हेतु [इस लिंक पर जाएँ](https://purchase.aspose.com/temporary-license/)।

---

**अंतिम अपडेट:** 2026-01-23  
**परीक्षित संस्करण:** Aspose.Note for Java 24.11  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}