---
date: 2026-06-05
description: Aspose.Note for Java के साथ OneNote में फ़ॉन्ट आकार बदलना, फ़ॉन्ट रंग
  सेट करना, और टेक्स्ट को हाइलाइट करना सीखें – कोड स्निपेट्स के साथ चरण‑दर‑चरण गाइड।
keywords:
- change font size onenote
- how to change text
- set font color onenote
linktitle: OneNote में फ़ॉन्ट आकार बदलें - Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-06-05'
  description: Learn how to change font size onenote, set font color, and highlight
    text with Aspose.Note for Java – step‑by‑step guide with code snippets.
  headline: Change Font Size in OneNote - Aspose.Note
  type: TechArticle
- description: Learn how to change font size onenote, set font color, and highlight
    text with Aspose.Note for Java – step‑by‑step guide with code snippets.
  name: Change Font Size in OneNote - Aspose.Note
  steps:
  - name: Import Packages
    text: 'The `Document`, `RichText`, and `TextRun` classes live in the `com.aspose.note`
      namespace. Import them at the top of your Java source file:'
  - name: Load the Document
    text: The `Document` class is Aspose.Note's top‑level object that represents a
      single OneNote file in memory. Loading a file is as simple as passing the file
      path to its constructor.
  - name: Access RichText Nodes
    text: '`RichText` nodes contain the actual paragraph text. By iterating over `document.getRichTextNodes()`,
      you gain access to every piece of editable text in the notebook.'
  - name: Change Text Style
    text: '`TextRun` represents a contiguous run of characters sharing the same formatting.
      Within the loop, set `FontColor` to yellow, `HighlightColor` to blue, and `FontSize`
      to **20** points to achieve the desired styling.'
  - name: Save the Document
    text: Call `document.save("StyledSample.one")` to write the changes back to a
      OneNote file. The save operation preserves all original content while applying
      the new styles.
  type: HowTo
- questions:
  - answer: Yes, filter the `RichText` collection by page or section ID before applying
      style changes.
    question: Can I apply these text style changes to specific sections of my OneNote
      document?
  - answer: Absolutely, you can modify font family, bold/italic, underline, alignment,
      and paragraph spacing using the same object model.
    question: Does Aspose.Note support other formatting options beyond color, highlight,
      and size?
  - answer: Yes, Aspose.Note works seamlessly with libraries like Apache POI, Jackson,
      or Spring to build complex document pipelines.
    question: Can I integrate Aspose.Note with other Java libraries for advanced processing?
  - answer: A commercial license is required for production deployments; a free evaluation
      license is available for development and testing.
    question: Is Aspose.Note licensed for commercial use?
  - answer: Visit the Aspose.Note documentation portal, download the full API reference
      PDF, and explore the GitHub repository for community examples.
    question: Where can I find additional samples and API reference?
  type: FAQPage
second_title: Aspose.Note Java API
title: OneNote में फ़ॉन्ट आकार बदलें - Aspose.Note
url: /hi/java/onenote-styles/change-text-style/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote में फ़ॉन्ट आकार बदलें - Aspose.Note

## परिचय

इस ट्यूटोरियल में आप Aspose.Note for Java का उपयोग करके **OneNote दस्तावेज़ों में फ़ॉन्ट आकार कैसे बदलें** सीखेंगे। हम OneNote फ़ाइल को लोड करने, उसके टेक्स्ट नोड्स तक पहुँचने, रंग, हाइलाइट और फ़ॉन्ट‑साइज़ परिवर्तन लागू करने, और अंत में अपडेटेड फ़ाइल को सहेजने की प्रक्रिया को देखेंगे। चाहे आप रिपोर्ट जनरेशन को ऑटोमेट कर रहे हों या मीटिंग नोट्स को पॉलिश कर रहे हों, यह गाइड आपको प्रोग्रामेटिक रूप से OneNote सामग्री को स्टाइल करने का विश्वसनीय तरीका देता है।

## त्वरित उत्तर
- **OneNote में Java के साथ फ़ॉन्ट आकार कैसे बदलें?** दस्तावेज़ को लोड करें, प्रत्येक `TextRun` की `FontSize` प्रॉपर्टी को संशोधित करें, फिर सहेजें – तीन सरल चरण।  
- **क्या मैं टेक्स्ट रंग और हाइलाइट भी बदल सकता हूँ?** हाँ, उसी `TextRun` पर `FontColor` और `HighlightColor` सेट करें।  
- **Aspose.Note का कौन सा संस्करण आवश्यक है?** कोई भी 23.10+ रिलीज़ इन स्टाइलिंग API को सपोर्ट करती है।  
- **क्या विकास के लिए लाइसेंस चाहिए?** परीक्षण के लिए एक फ्री ट्रायल काम करता है; प्रोडक्शन के लिए एक कमर्शियल लाइसेंस आवश्यक है।  
- **क्या यह तरीका बड़े नोटबुक्स के लिए उपयुक्त है?** हाँ – Aspose.Note पूरी फ़ाइल को मेमोरी में लोड किए बिना सैकड़ों पेज़ वाले नोटबुक्स को प्रोसेस करता है।

## change font size onenote क्या है?
**change font size onenote** का अर्थ है OneNote नोटबुक के भीतर टेक्स्ट तत्वों के `FontSize` एट्रिब्यूट को प्रोग्रामेटिक रूप से समायोजित करना। Aspose.Note का उपयोग करके, डेवलपर्स इस प्रॉपर्टी को API के माध्यम से बदल सकते हैं, जो सीधे अंतर्निहित OneNote फ़ाइल संरचना को अपडेट करता है, जिससे दृश्य रूप में बदलाव मैन्युअल एडिट या UI इंटरैक्शन के बिना हो जाता है।

## OneNote में टेक्स्ट स्टाइल बदलने के लिए Aspose.Note क्यों उपयोग करें?
Aspose.Note 30 से अधिक फ़ॉर्मेटिंग विकल्प प्रदान करता है—जैसे फ़ॉन्ट फ़ैमिली, आकार, रंग, हाइलाइट, अलाइनमेंट, और पैराग्राफ स्पेसिंग—और बड़े नोटबुक्स को कुशलतापूर्वक प्रोसेस करने के लिए डिज़ाइन किया गया है। यह 500 से अधिक पेज़ वाले नोटबुक्स को 150 MB से कम RAM उपयोग करते हुए संभाल सकता है, जिससे एंटरप्राइज़‑स्तर के दस्तावेज़ वर्कफ़्लो के लिए विश्वसनीय, हाई‑परफ़ॉर्मेंस ऑटोमेशन मिलता है।

## पूर्वापेक्षाएँ

1. बुनियादी Java प्रोग्रामिंग ज्ञान।  
2. आपके मशीन पर JDK 8 या उससे ऊपर स्थापित होना चाहिए।  
3. Aspose.Note for Java लाइब्रेरी (Aspose वेबसाइट से डाउनलोड करें)।  
4. OneNote की पदानुक्रमित संरचना (पेज़, सेक्शन, RichText नोड्स) की परिचितता।

## Aspose.Note का उपयोग करके OneNote में फ़ॉन्ट आकार कैसे बदलें?
अपनी OneNote फ़ाइल लोड करें, प्रत्येक `RichText` नोड को खोजें, प्रत्येक `TextRun` की स्टाइल अपडेट करें, और दस्तावेज़ को सहेजें। यह एंड‑टू‑एंड फ्लो केवल कुछ लाइनों के कोड में पूरा हो जाता है और सामान्य नोटबुक्स के लिए एक सेकंड से भी कम समय में चलता है।

### चरण 1: पैकेज इम्पोर्ट करें

`Document`, `RichText`, और `TextRun` क्लासेज `com.aspose.note` नेमस्पेस में स्थित हैं। इन्हें अपने Java स्रोत फ़ाइल के शीर्ष पर इम्पोर्ट करें:

```java
import java.awt.Color;
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.RichText;
import com.aspose.note.TextRun;
import com.aspose.note.TextStyle;
```

### चरण 2: दस्तावेज़ लोड करें

`Document` क्लास Aspose.Note का टॉप‑लेवल ऑब्जेक्ट है जो मेमोरी में एकल OneNote फ़ाइल का प्रतिनिधित्व करता है। फ़ाइल लोड करना इतना सरल है कि फ़ाइल पाथ को उसके कन्स्ट्रक्टर में पास करें।

```java
// Load the document into Aspose.Note
Document document = new Document("Your Document Directory/Sample1.one");
```

### चरण 3: RichText नोड्स तक पहुँचें

`RichText` नोड्स वास्तविक पैराग्राफ टेक्स्ट रखते हैं। `document.getRichTextNodes()` पर इटरेट करके, आपको नोटबुक में प्रत्येक संपादन योग्य टेक्स्ट तक पहुँच मिलती है।

```java
// Get a particular RichText node
List<RichText> richTextNodes = document.getChildNodes(RichText.class);
RichText richText = richTextNodes.get(0);
```

### चरण 4: टेक्स्ट स्टाइल बदलें

`TextRun` एक सतत कैरेक्टर रन को दर्शाता है जो समान फ़ॉर्मेटिंग साझा करता है। लूप के भीतर, `FontColor` को पीला, `HighlightColor` को नीला, और `FontSize` को **20** पॉइंट सेट करें ताकि वांछित स्टाइल प्राप्त हो सके।

```java
for (TextRun run : richText.getTextRuns()) {
    // Set font color
    run.getStyle().setFontColor(Color.yellow);
    // Set highlight color
    run.getStyle().setHighlight(Color.blue);
    // Set font size
    run.getStyle().setFontSize(20);
}
```

### चरण 5: दस्तावेज़ सहेजें

`document.save("StyledSample.one")` को कॉल करके बदलावों को OneNote फ़ाइल में वापस लिखें। सहेजने का ऑपरेशन सभी मूल सामग्री को संरक्षित रखता है जबकि नई स्टाइल लागू करता है।

```java
document.save("Your Document Directory/ChangeTextStyle_out.pdf");
System.out.printf("File saved: %s\n", "Your Document Directory/ChangeTextStyle_out.pdf");
```

## सामान्य समस्याएँ और समाधान

- **टेक्स्ट नहीं बदल रहा:** सुनिश्चित करें कि आप प्रत्येक `RichText` नोड के भीतर `TextRun` ऑब्जेक्ट्स पर इटरेट कर रहे हैं; इस स्तर को छोड़ने से फ़ॉर्मेटिंग अपरिवर्तित रहेगी।  
- **रंग अलग दिख रहा है:** Aspose.Note RGB मानों का उपयोग करता है; सुनिश्चित करें कि आप सही `java.awt.Color` कॉन्स्टेंट्स उपयोग कर रहे हैं।  
- **बड़ा नोटबुक धीमा हो रहा है:** LoadOptions निर्धारित करता है कि Aspose.Note फ़ाइल को कैसे लोड करता है, जिससे स्ट्रीमिंग और फ़ॉर्मेट चयन संभव होता है। `document.setLoadOptions(new LoadOptions(LoadFormat.OneNote))` का उपयोग करके स्ट्रीमिंग मोड सक्षम करें, जो मेमोरी फ़ुटप्रिंट को कम करता है।

## अक्सर पूछे जाने वाले प्रश्न

**प्र: क्या मैं इन टेक्स्ट स्टाइल बदलावों को अपने OneNote दस्तावेज़ के विशिष्ट सेक्शन पर लागू कर सकता हूँ?**  
**उ:** हाँ, स्टाइल बदलाव लागू करने से पहले `RichText` कलेक्शन को पेज या सेक्शन ID द्वारा फ़िल्टर करें।

**प्र: क्या Aspose.Note रंग, हाइलाइट और आकार के अलावा अन्य फ़ॉर्मेटिंग विकल्पों को सपोर्ट करता है?**  
**उ:** बिल्कुल, आप वही ऑब्जेक्ट मॉडल उपयोग करके फ़ॉन्ट फ़ैमिली, बोल्ड/इटैलिक, अंडरलाइन, अलाइनमेंट, और पैराग्राफ स्पेसिंग को भी बदल सकते हैं।

**प्र: क्या मैं उन्नत प्रोसेसिंग के लिए Aspose.Note को अन्य Java लाइब्रेरीज़ के साथ इंटीग्रेट कर सकता हूँ?**  
**उ:** हाँ, Aspose.Note Apache POI, Jackson, या Spring जैसी लाइब्रेरीज़ के साथ सहजता से काम करता है ताकि जटिल दस्तावेज़ पाइपलाइन बनाई जा सके।

**प्र: क्या Aspose.Note का व्यावसायिक उपयोग के लिए लाइसेंस है?**  
**उ:** प्रोडक्शन डिप्लॉयमेंट के लिए एक कमर्शियल लाइसेंस आवश्यक है; विकास और परीक्षण के लिए एक फ्री इवैल्यूएशन लाइसेंस उपलब्ध है।

**प्र: अतिरिक्त सैंपल्स और API रेफ़रेंस कहाँ मिल सकते हैं?**  
**उ:** Aspose.Note डॉक्यूमेंटेशन पोर्टल पर जाएँ, पूर्ण API रेफ़रेंस PDF डाउनलोड करें, और कम्युनिटी उदाहरणों के लिए GitHub रिपॉज़िटरी देखें।

## निष्कर्ष

ऊपर दिए गए चरणों का पालन करके, अब आप **OneNote फ़ाइलों में फ़ॉन्ट आकार कैसे बदलें** जानते हैं, टेक्स्ट रंग समायोजित कर सकते हैं, और Aspose.Note for Java का उपयोग करके हाइलाइट लागू कर सकते हैं। यह क्षमता आपको मीटिंग नोट्स, प्रशिक्षण सामग्री, या किसी भी OneNote‑आधारित सामग्री का दृश्य रूप से बड़े पैमाने पर ऑटोमेट करने देती है।

---

**अंतिम अपडेट:** 2026-06-05  
**परीक्षित संस्करण:** Aspose.Note 23.10 for Java  
**लेखक:** Aspose

## संबंधित ट्यूटोरियल

- [OneNote में डिफ़ॉल्ट पैराग्राफ स्टाइल सेट करें - Aspose.Note](/note/java/onenote-styles/set-default-paragraph-style/)
- [OneNote में टेक्स्ट के लिए प्रूफिंग लैंग्वेज सेट करें - Aspose.Note](/note/java/onenote-text-manipulation/set-proofing-language-for-text/)
- [Microsoft OneNote स्टाइल में पेज टाइटल सेट करना - Aspose.Note](/note/java/onenote-text-manipulation/setting-page-title-in-microsoft-onenote-style/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-wrap-class >}}