---
date: 2026-01-15
description: Aspose.Note for Java का उपयोग करके OneNote में परिवर्तन कैसे ट्रैक करें
  और पृष्ठ संशोधनों को कैसे प्रबंधित करें, सीखें। इसमें एक संशोधन सारांश उदाहरण और
  संशोधन तिथि को कैसे बदलें, शामिल है।
linktitle: Working with Page Revisions in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: ट्रैक चेंजेज़ वननोट – Aspose.Note के साथ पेज संशोधनों का प्रबंधन
url: /hi/java/onenote-page-manipulation/working-with-page-revisions/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote में पेज संशोधनों के साथ काम करना - Aspose.Note

## परिचय

OneNote नोट्स को व्यवस्थित करने के लिए एक शक्तिशाली उपकरण है, और जब आपको **track changes onenote** की आवश्यकता होती है, तो पेज संशोधनों का प्रबंधन प्रभावी सहयोग के लिए आवश्यक हो जाता है। Aspose.Note for Java के साथ, आप प्रोग्रामेटिक रूप से संशोधनों को संभाल सकते हैं, देख सकते हैं कि किसने पेज संपादित किया, और यहाँ तक कि टाइमस्टैम्प को समायोजित कर सकते हैं। यह ट्यूटोरियल आपको प्रत्येक चरण के माध्यम से ले जाता है, दस्तावेज़ लोड करने से लेकर संशोधन सारांश को अपडेट करने तक।

## त्वरित उत्तर
- **What does “track changes onenote” mean?** यह OneNote पेज को किसने और कब संपादित किया, इसे मॉनिटर करने को दर्शाता है।
- **Which library is required?** Aspose.Note for Java.
- **Can I change the author or date of a revision?** हाँ, RevisionSummary API (`modify revision date`) का उपयोग करके।
- **Do I need a OneNote file beforehand?** हाँ, एक नमूना `.one` फ़ाइल आवश्यक है।
- **Is a license needed for production?** व्यावसायिक उपयोग के लिए एक वैध Aspose.Note लाइसेंस आवश्यक है।

## संशोधन सारांश उदाहरण क्या है?
*revision summary* पेज पर सबसे हालिया बदलावों के बारे में मेटाडाटा प्रदान करता है—लेखक का नाम, अंतिम संशोधित समय, और अन्य विवरण। इस गाइड में हम उस जानकारी को प्राप्त करेंगे और प्रदर्शित करेंगे, फिर दिखाएंगे कि कैसे **modify revision date** किया जाए।

## Aspose.Note के साथ track changes onenote क्यों?
- **Collaboration:** जल्दी से देखें कि किसने नवीनतम संपादन किए।
- **Auditing:** अनुपालन के लिए बदलावों का विश्वसनीय इतिहास रखें।
- **Automation:** बैक‑एंड सेवाओं या माइग्रेशन टूल्स में संशोधन हैंडलिंग को एकीकृत करें।

## Prerequisites

### Java विकास पर्यावरण
सुनिश्चित करें कि आपके सिस्टम पर Java Development Kit (JDK) स्थापित है।

### Aspose.Note for Java लाइब्रेरी
Aspose.Note for Java लाइब्रेरी को [here](https://releases.aspose.com/note/java/) से डाउनलोड और इंस्टॉल करें।

### OneNote दस्तावेज़
परीक्षण के उद्देश्य से एक नमूना OneNote दस्तावेज़ तैयार रखें।

## पैकेज आयात करें

अपने Java प्रोजेक्ट में, Aspose.Note for Java के साथ काम करने के लिए आवश्यक पैकेज आयात करें।

```java
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.RevisionSummary;
import java.io.IOException;
import java.util.Calendar;
```

आइए प्रदान किए गए उदाहरण को कई चरणों में विभाजित करें ताकि स्पष्ट समझ प्राप्त हो सके।

## चरण 1: OneNote दस्तावेज़ लोड करें

सबसे पहले, OneNote दस्तावेज़ लोड करें और पहली चाइल्ड पेज प्राप्त करें।

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
Page page = document.getFirstChild();
```

## चरण 2: पेज संशोधन सारांश पढ़ें

पेज के लिए कंटेंट संशोधन सारांश पढ़ें। यह **revision summary example** है जो दिखाता है कि आखिरी बार पेज किसने संपादित किया।

```java
RevisionSummary pageRevisionInfo = page.getPageContentRevisionSummary();
System.out.println(String.format("Author:\t%s\nModified:\t%s",
        pageRevisionInfo.getAuthorMostRecent(),
        pageRevisionInfo.getLastModifiedTime().toString()));
```

## चरण 3: पेज संशोधन सारांश अपडेट करें

नए लेखक और नई संशोधित तिथि के साथ पेज संशोधन सारांश अपडेट करें। यह दर्शाता है कि कैसे प्रोग्रामेटिक रूप से **modify revision date** किया जाता है।

```java
pageRevisionInfo.setAuthorMostRecent("New Author");
Calendar modifiedDate = Calendar.getInstance();
pageRevisionInfo.setLastModifiedTime(modifiedDate.getTime());
document.save(dataDir + "WorkingWithPageRevisions_out.one");
```

## निष्कर्ष

OneNote दस्तावेज़ों में पेज संशोधनों को प्रोग्रामेटिक रूप से प्रबंधित करना Aspose.Note for Java के साथ सरल बनाया जा सकता है। इस ट्यूटोरियल में बताए गए चरणों का पालन करके, आप प्रभावी रूप से **track changes onenote** कर सकते हैं, संशोधन विवरण देख सकते हैं, और यहाँ तक कि अपने कार्यप्रवाह के अनुसार **modify revision date** भी कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं दूसरी Java लाइब्रेरी के साथ Aspose.Note for Java का इस्तेमाल कर सकता हूँ?

A: हाँ, Aspose.Note for Java को दूसरी Java लाइब्रेरी के साथ इस्तेमाल किया जा सकता है ताकि काम बढ़ सके।

### Q2: क्या Aspose.Note for Java OneNote डॉक्यूमेंट के सभी वर्शन को सपोर्ट करता है?

A: Aspose.Note for Java के अलग-अलग वर्शन के OneNote डॉक्यूमेंट को सपोर्ट करता है, जिसमें पुराने वर्शन भी शामिल हैं।

### Q3: क्या Aspose.Note for Java एंटरप्राइज़-लेवल एप्लिकेशन के लिए सही है?

A: बिल्कुल, Aspose.Note for Java को दूसरी लाइब्रेरी के साथ इस्तेमाल करने की ज़रूरत नहीं है, इसलिए इसे पूरा करने के लिए मज़बूत फीचर्स और स्केल एडजस्टमेंट के साथ डिज़ाइन किया गया है।

### Q4: क्या मैं Aspose.Note for Java से पेज रिविज़न को कस्टमाइज़ कर सकता हूँ?

A: हाँ, आप अपनी ज़रूरत के हिसाब से Aspose.Note for Java का इस्तेमाल करके पेज में बदलाव को कस्टमाइज़ कर सकते हैं।

### Q5: मुझे Aspose.Note for Java के लिए सपोर्ट कहाँ से मिल सकता है?

A: आप Aspose.Note for Java के लिए समर्थन [Aspose.Note forum](https://forum.aspose.com/c/note/28) से प्राप्त कर सकते हैं।

---

**Last Updated:** 2026-01-15  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}