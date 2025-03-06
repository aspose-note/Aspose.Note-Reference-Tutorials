---
title: OneNote में टैग के साथ नया छवि नोड जोड़ें - Aspose.Note
linktitle: OneNote में टैग के साथ नया छवि नोड जोड़ें - Aspose.Note
second_title: Aspose.नोट जावा एपीआई
description: जावा के लिए Aspose.Note का उपयोग करके OneNote में एक टैग के साथ एक नया छवि नोड जोड़ने का तरीका जानें। अपने जावा प्रोग्रामिंग कौशल को सहजता से उन्नत करें।
weight: 10
url: /hi/java/onenote-tag-operations/add-new-image-node-with-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote में टैग के साथ नया छवि नोड जोड़ें - Aspose.Note

## परिचय
जावा प्रोग्रामिंग के क्षेत्र में, Aspose.Note OneNote दस्तावेज़ों को आसानी से संभालने के लिए एक शक्तिशाली उपकरण के रूप में सामने आता है। यदि आप अपने कौशल को बढ़ाना चाहते हैं और Aspose.Note का उपयोग करके OneNote में एक टैग के साथ एक नया छवि नोड जोड़ना सीखना चाहते हैं, तो आप सही जगह पर आए हैं। यह चरण-दर-चरण मार्गदर्शिका आपको प्रक्रिया के बारे में बताएगी, यह सुनिश्चित करते हुए कि आप प्रत्येक अवधारणा को अच्छी तरह से समझ लें।
## आवश्यक शर्तें
इससे पहले कि हम ट्यूटोरियल में उतरें, आइए सुनिश्चित करें कि आपके पास वह सब कुछ है जो आपको चाहिए:
1.  जावा के लिए Aspose.Note: सुनिश्चित करें कि आपके पास Aspose.Note लाइब्रेरी स्थापित है। यदि नहीं, तो आप इसे डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/note/java/).
2. जावा विकास पर्यावरण: सुनिश्चित करें कि आपकी मशीन पर एक कार्यशील जावा विकास वातावरण स्थापित है।
अब चूँकि हमारे पास पूर्वापेक्षाएँ मौजूद हैं, आइए अगले चरणों पर आगे बढ़ें।
## पैकेज आयात करें
अपने जावा प्रोजेक्ट में, आवश्यक पैकेज आयात करके प्रारंभ करें:
```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Image;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
import com.aspose.note.TagIcon;
```
## चरण 1: दस्तावेज़ ऑब्जेक्ट बनाएँ
```java
// दस्तावेज़ निर्देशिका का पथ.
String dataDir = "Your Document Directory";
// दस्तावेज़ वर्ग का एक ऑब्जेक्ट बनाएं
Document doc = new Document();
```
## चरण 2: पेज क्लास ऑब्जेक्ट को आरंभ करें
```java
// पेज क्लास ऑब्जेक्ट को इनिशियलाइज़ करें
Page page = new Page();
```
## चरण 3: आउटलाइन क्लास ऑब्जेक्ट को आरंभ करें
```java
// आउटलाइन क्लास ऑब्जेक्ट को इनिशियलाइज़ करें
Outline outline = new Outline();
```
## चरण 4: आउटलाइनएलिमेंट क्लास ऑब्जेक्ट को आरंभ करें
```java
// आउटलाइनएलिमेंट क्लास ऑब्जेक्ट को इनिशियलाइज़ करें
OutlineElement outlineElem = new OutlineElement();
```
## चरण 5: छवि लोड करें और डालें
```java
// एक छवि लोड करें
Image image = new Image(null, dataDir + "Input.jpg");
// दस्तावेज़ नोड में छवि डालें
outlineElem.appendChildLast(image);
```
## चरण 6: छवि में नोट टैग जोड़ें
```java
// छवि में एक पीला सितारा नोट टैग जोड़ें
NoteTag noteTag = NoteTag.createYellowStar();
image.getTags().add(noteTag);
```
## चरण 7: आउटलाइन एलिमेंट नोड जोड़ें
```java
// रूपरेखा तत्व नोड जोड़ें
outline.appendChildLast(outlineElem);
```
## चरण 8: आउटलाइन नोड जोड़ें
```java
// रूपरेखा नोड जोड़ें
page.appendChildLast(outline);
```
## चरण 9: पेज नोड जोड़ें
```java
// पेज नोड जोड़ें
doc.appendChildLast(page);
```
## चरण 10: OneNote दस्तावेज़ सहेजें
```java
// OneNote दस्तावेज़ को PDF के रूप में सहेजें
doc.save(dataDir + "AddNewImageNodeWithTag_out.pdf", SaveFormat.Pdf);
```
बधाई हो! आपने जावा के लिए Aspose.Note का उपयोग करके OneNote में एक टैग के साथ एक नया छवि नोड सफलतापूर्वक जोड़ा है।
## निष्कर्ष
 जावा के लिए Aspose.Note में महारत हासिल करने से OneNote दस्तावेज़ हेरफेर में रोमांचक संभावनाएं खुलती हैं। इस ट्यूटोरियल का अनुसरण करके, आपने एक व्यावहारिक कौशल प्राप्त किया है जिसे विभिन्न परियोजनाओं पर लागू किया जा सकता है। Aspose.Note दस्तावेज़ की खोज करते रहें[यहाँ](https://reference.aspose.com/note/java/)अधिक उन्नत सुविधाओं और संभावनाओं के लिए।
## पूछे जाने वाले प्रश्न
### मुझे Aspose.Note दस्तावेज़ कहाँ मिल सकता है?
 आप दस्तावेज़ पा सकते हैं[यहाँ](https://reference.aspose.com/note/java/).
### मैं जावा के लिए Aspose.Note कैसे डाउनलोड करूं?
 आप इसे रिलीज़ पृष्ठ से डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/note/java/).
### क्या कोई निःशुल्क परीक्षण उपलब्ध है?
 हाँ, आप नि:शुल्क परीक्षण का उपयोग कर सकते हैं[यहाँ](https://releases.aspose.com/).
### मुझे Aspose.Note के लिए समर्थन कहाँ से मिल सकता है?
 सामुदायिक मंच पर जाएँ[यहाँ](https://forum.aspose.com/c/note/28) समर्थन के लिए।
### क्या मुझे अस्थायी लाइसेंस की आवश्यकता है?
 यदि आवश्यक हो, तो आप अस्थायी लाइसेंस प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
