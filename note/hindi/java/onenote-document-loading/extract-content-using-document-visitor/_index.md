---
date: 2025-12-04
description: Aspose.Note का उपयोग करके Java में OneNote फ़ाइलों से छवियों को निकालना
  और OneNote को टेक्स्ट में बदलना सीखें। कोड उदाहरणों के साथ चरण‑दर‑चरण गाइड।
linktitle: Extract Images from OneNote using Document Visitor - Java
second_title: Aspose.Note Java API
title: डॉक्यूमेंट विज़िटर का उपयोग करके वननोट से चित्र निकालें - जावा
url: /hi/java/onenote-document-loading/extract-content-using-document-visitor/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote से छवियों को निकालना Document Visitor का उपयोग करके - Java

## परिचय

Aspose.Note for Java, OneNote नोटबुक से **छवियों को निकालना** आसान बनाता है तथा Java में अंतर्निहित `.one` फ़ाइल को पढ़ता है। इस ट्यूटोरियल में हम आपको एक पूर्ण, व्यावहारिक उदाहरण के माध्यम से ले जाएंगे जो दिखाता है कि OneNote फ़ाइल को कैसे लोड करें, कस्टम `DocumentVisitor` के साथ उसकी संरचना को कैसे पार करें, और दोनों छवियों और साधारण टेक्स्ट को कैसे निकालें। अंत में आप यह भी जानेंगे कि यदि केवल टेक्स्ट सामग्री चाहिए तो **OneNote को टेक्स्ट में कैसे बदलें**।

## त्वरित उत्तर
- **मुझे कौनसी लाइब्रेरी चाहिए?** Aspose.Note for Java (नीचे डाउनलोड लिंक)।  
- **क्या मैं केवल छवियों को निकाल सकता हूँ?** हाँ – `DocumentVisitor` में `VisitImageStart` मेथड को इम्प्लीमेंट करें।  
- **Java में .one फ़ाइल को कैसे पढ़ें?** `new Document(path, new LoadOptions())` का उपयोग करें।  
- **उत्पादन के लिए लाइसेंस चाहिए?** गैर‑ट्रायल उपयोग के लिए एक वाणिज्यिक लाइसेंस आवश्यक है।  
- **कौनसे Java संस्करण समर्थित हैं?** JDK 8 या उससे ऊपर।

## पूर्वापेक्षाएँ

शुरू करने से पहले सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

1. Java Development Kit (JDK) 8 या नया स्थापित हो।  
2. Aspose.Note for Java लाइब्रेरी डाउनलोड की हुई। आप इसे **[here](https://releases.aspose.com/note/java/)** से डाउनलोड कर सकते हैं।  
3. वह OneNote दस्तावेज़ (`.one` फ़ाइल) जिसे आप छवियों के लिए निकालना या टेक्स्ट में बदलना चाहते हैं।

## पैकेज इम्पोर्ट करें

पहले, Aspose.Note API से आवश्यक क्लासेज़ को इम्पोर्ट करें।

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.DocumentVisitor;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.OutlineGroup;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.Title;
```

## चरण 1: कस्टम Document Visitor सेट अप करें

एक क्लास बनाएं जो `DocumentVisitor` को एक्सटेंड करे। यह क्लास OneNote दस्तावेज़ के प्रत्येक नोड के लिए कॉल किया जाएगा, जिससे आप **OneNote से छवियों को निकालना** और वैकल्पिक रूप से टेक्स्ट एकत्र कर सकेंगे।

```java
public class ExtractOneNoteContentUsingDocumentvisitor extends DocumentVisitor {
    
    final private StringBuilder mBuilder;
    final private boolean mIsSkipText;
    private int nodecount;

    public ExtractOneNoteContentUsingDocumentvisitor() {
        nodecount = 0;
        mIsSkipText = false;
        mBuilder = new StringBuilder();
    }
    
    // Other methods will be implemented here
}
```

## चरण 2: Visitor मेथड्स इम्प्लीमेंट करें

उन नोड प्रकारों के लिए ओवरराइड जोड़ें जिनमें आपकी रुचि है। नीचे हम रिच‑टेक्स्ट, छवियां, शीर्षक, पेज, आउटलाइन और आउटलाइन एलिमेंट्स को हैंडल करते हैं। `VisitImageStart` मेथड वह जगह है जहाँ छवि निकाली जाती है।

```java
// Visitor methods for different types of nodes

public /* override */ void VisitRichTextStart(RichText run) {
    ++nodecount;
    AppendText(run.getText());
}

public /* override */ void VisitDocumentStart(Document document) {
    ++nodecount;
}

public /* override */ void VisitPageStart(Page page) {
    ++nodecount;
}

public /* override */ void VisitTitleStart(Title title) {
    ++nodecount;
}

public /* override */ void VisitImageStart(Image image) {
    ++nodecount;
    // Here you could save the image to disk or process it further
    System.out.println("Found image with size: " + image.getData().length + " bytes");
}

public /* override */ void VisitOutlineGroupStart(OutlineGroup outlineGroup) {
    ++nodecount;
}

public void VisitOutlineStart(Outline outline) {
    ++nodecount;
}

public void VisitOutlineElementStart(OutlineElement outlineElement) {
    ++nodecount;
}
```

### ये मेथड्स क्यों इम्प्लीमेंट करें?

- **OneNote से छवियों को निकालना:** `VisitImageStart` आपको रॉ इमेज बाइट्स तक सीधा एक्सेस देता है।  
- **OneNote को टेक्स्ट में बदलना:** `VisitRichTextStart` टेक्स्ट सामग्री एकत्र करता है, जिससे एक सरल **OneNote को टेक्स्ट में बदलें** ऑपरेशन संभव होता है।  
- **.one फ़ाइल को Java में पढ़ना:** विज़िटर पैटर्न अंतर्निहित `.one` फ़ाइल संरचना को एब्स्ट्रैक्ट करता है, इसलिए आपको बाइनरी फ़ॉर्मेट को स्वयं पार्स करने की ज़रूरत नहीं पड़ती।

## चरण 3: मुख्य मेथड से Visitor चलाएँ

`.one` फ़ाइल को लोड करें, अपने विज़िटर को इंस्टैंशिएट करें, और ट्रैवर्सल शुरू करें।

```java
public static void main(String[] args) throws IOException {
    // Open the document we want to convert.
    String dataDir = "Your Document Directory";
    Document doc = new Document(dataDir + "Sample1.one", new LoadOptions());
    
    // Create an object that inherits from the DocumentVisitor class.
    ExtractOneNoteContentUsingDocumentvisitor myConverter = new ExtractOneNoteContentUsingDocumentvisitor();
    
    // Accept the visitor to start the visiting process.
    doc.accept(myConverter);
    
    // Retrieve the result of the operation.
    System.out.println(myConverter.GetText());   // Text extracted from the notebook
    System.out.println(myConverter.NodeCount()); // Total nodes visited
}
```

## सामान्य उपयोग के केस

- **स्वचालित रिपोर्टिंग:** OneNote मीटिंग नोटबुक से छवियों और टेक्स्ट को निकालकर PDF या HTML सारांश बनाएं।  
- **सामग्री माइग्रेशन:** लेगेसी OneNote आर्काइव को प्लेन‑टेक्स्ट फ़ाइलों में बदलें ताकि इंडेक्सिंग या सर्च‑इंजन इन्जेस्टशन आसान हो।  
- **डिजिटल एसेट एक्सट्रैक्शन:** एम्बेडेड स्क्रीनशॉट, डायग्राम या फ़ोटो को निकालें और अन्य एप्लिकेशन में पुनः उपयोग करें।

## समस्या निवारण और टिप्स

- **बड़ी नोटबुक्स:** यदि मेमोरी समस्याएँ आती हैं, तो पेज‑वाइज़ प्रोसेस करें; `VisitPageStart` को चेक करें और आवश्यक होने पर पेज‑लेवल रिसोर्सेज़ लोड करें।  
- **इमेज फ़ॉर्मेट्स:** `Image` ऑब्जेक्ट रॉ बाइट्स रिटर्न करता है; सेव करने से पहले फ़ॉर्मेट (PNG, JPEG) का पता लगाना पड़ सकता है।  
- **लाइसेंस त्रुटियाँ:** उत्पादन में दस्तावेज़ लोड करने से पहले Aspose लाइसेंस सेट करें (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`)।

## अक्सर पूछे जाने वाले प्रश्न

**प्रश्न: क्या मैं OneNote दस्तावेज़ से विशिष्ट प्रकार की सामग्री निकाल सकता हूँ?**  
उत्तर: हाँ – केवल उन विज़िटरथड्स को ओवरराइड करें जिनकी आपको ज़रूरत है (जैसे छवियों के लिए `VisitImageStart`, टेक्स्ट के लिए `VisitRichTextStart`)।

**प्रश्न: क्या Aspose.Note for Java विभिन्न संस्करणों की OneNote फ़ाइलों के साथ संगत है?**  
उत्तर: बिल्कुल। लाइब्रेरी सभी प्रमुख OneNote फ़ाइल संस्करणों को सपोर्ट करती है, इसलिए आप सुरक्षित रूप से **.one फ़ाइल Java** प्रोजेक्ट्स को पढ़ सकते हैं, चाहे मूल OneNote संस्करण कुछ भी हो।

**प्रश्न: क्या मैं इस एक्सट्रैक्शन प्रोसेस को अपने Java एप्लिकेशन में इंटीग्रेट कर सकता हूँ?**  
उत्तर: हाँ। विज़िटर पैटर्न किसी भी Java कोडबेस में सहजता से काम करता है; बस लाइब्रेरी JAR जोड़ें और ऊपर दिखाए गए उदाहरण को कॉल करें।

**प्रश्न: क्या Aspose.Note for Java जटिल OneNote दस्तावेज़ों को संभालने के लिए समर्थन प्रदान करता है?**  
उत्तर: करता है। नेस्टेड आउटलाइन, एम्बेडेड मीडिया, और कस्टम डेटा सभी विज़िटर API के माध्यम से एक्सपोज़ होते हैं।

**प्रश्न: क्या OneNote दस्तावेज़ के आकार पर कोई सीमा है?**  
उत्तर: कोई हार्ड लिमिट नहीं है, लेकिन अत्यधिक बड़ी नोटबुक्स के लिए अधिक हीप मेमोरी की आवश्यकता हो सकती है; पेज‑बाय‑पेज प्रोसेसिंग पर विचार करें।

**प्रश्न: निकाले गए टेक्स्ट को प्लेन‑टेक्स्ट फ़ाइल में कैसे बदलूँ?**  
उत्तर: `myConverter.GetText()` एक `String` रिटर्न करता है; इसे मानक Java I/O (`Files.write(Paths.get("output.txt"), text.getBytes());`) से फ़ाइल में लिखें।

---  

**अंतिम अपडेट:** 2025-12-04  
**टेस्टेड वर्ज़न:** Aspose.Note for Java 24.10  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}