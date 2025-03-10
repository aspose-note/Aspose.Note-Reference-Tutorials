---
title: OneNote में सभी पेजों पर टेक्स्ट बदलें - Aspose.Note
linktitle: OneNote में सभी पेजों पर टेक्स्ट बदलें - Aspose.Note
second_title: Aspose.नोट जावा एपीआई
description: जावा के लिए Aspose.Note की शक्ति का अन्वेषण करें! OneNote में सभी पेजों पर टेक्स्ट को आसानी से बदलना सीखें। निर्बाध दस्तावेज़ हेरफेर के लिए हमारी चरण-दर-चरण मार्गदर्शिका का पालन करें।
weight: 20
url: /hi/java/onenote-text-manipulation/replace-text-on-all-pages/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote में सभी पेजों पर टेक्स्ट बदलें - Aspose.Note

## परिचय
OneNote में सभी पेजों पर टेक्स्ट को बदलने के लिए Java के लिए Aspose.Note का उपयोग करने पर इस व्यापक ट्यूटोरियल में आपका स्वागत है। यदि आप अपने OneNote दस्तावेज़ों को कुशलतापूर्वक अद्यतन और व्यवस्थित करना चाहते हैं, तो आप सही जगह पर आए हैं। इस चरण-दर-चरण मार्गदर्शिका में, हम आपको प्रक्रिया के बारे में बताएंगे, यह सुनिश्चित करते हुए कि आप प्रत्येक चरण को समझें।
## आवश्यक शर्तें
इससे पहले कि हम ट्यूटोरियल में उतरें, सुनिश्चित करें कि आपके पास निम्नलिखित स्थान हैं:
-  जावा लाइब्रेरी के लिए Aspose.Note: सुनिश्चित करें कि आपके पास जावा लाइब्रेरी के लिए Aspose.Note स्थापित है। आप इसे यहां से डाउनलोड कर सकते हैं[लिंक को डाउनलोड करें](https://releases.aspose.com/note/java/).
- दस्तावेज़ निर्देशिका: एक निर्देशिका तैयार रखें जहाँ आपके OneNote दस्तावेज़ संग्रहीत हैं। कोड उदाहरणों में "आपकी दस्तावेज़ निर्देशिका" को अपनी वास्तविक दस्तावेज़ निर्देशिका के पथ से बदलें।
## पैकेज आयात करें
अपने जावा प्रोजेक्ट में, आवश्यक Aspose.Note पैकेज आयात करें। अपनी जावा फ़ाइल की शुरुआत में निम्नलिखित पंक्तियाँ जोड़ें:
```java
import java.io.IOException;
import java.util.HashMap;
import java.util.List;
import java.util.Map;
import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
```
आइए अब दिए गए कोड को चरणों की एक श्रृंखला में तोड़ें।
## चरण 1: दस्तावेज़ निर्देशिका स्थापित करें
```java
// दस्तावेज़ निर्देशिका का पथ.
String dataDir = "Your Document Directory";
```
"आपकी दस्तावेज़ निर्देशिका" को उस वास्तविक पथ से बदलना सुनिश्चित करें जहाँ आपके OneNote दस्तावेज़ संग्रहीत हैं।
## चरण 2: प्रतिस्थापन पाठ को परिभाषित करें
```java
Map<String, String> replacements = new HashMap<String, String>();
replacements.put("2. Get organized", "New Text Here");
```
वह टेक्स्ट निर्दिष्ट करें जिसे आप बदलना चाहते हैं और वह नया टेक्स्ट निर्दिष्ट करें जिसे आप सम्मिलित करना चाहते हैं। इस उदाहरण में, हम "2. व्यवस्थित हों" को "यहां नया टेक्स्ट" से बदल रहे हैं।
## चरण 3: OneNote दस्तावेज़ लोड करें
```java
// दस्तावेज़ को Aspose.Note में लोड करें।
LoadOptions options = new LoadOptions();
Document oneFile = new Document(dataDir + "Sample1.one", options);
```
Aspose.Note का उपयोग करके अपना OneNote दस्तावेज़ लोड करें। "Sample1.one" को अपनी OneNote फ़ाइल के वास्तविक नाम से बदलें।
## चरण 4: रिचटेक्स्ट नोड्स को ट्रैवर्स करें
```java
// सभी रिचटेक्स्ट नोड्स प्राप्त करें
List<RichText> textNodes = (List<RichText>) oneFile.getChildNodes(RichText.class);
```
लोड किए गए दस्तावेज़ से सभी रिचटेक्स्ट नोड्स पुनर्प्राप्त करें। इन नोड्स में वह टेक्स्ट होता है जिसे आप बदलना चाहते हैं।
## चरण 5: टेक्स्ट बदलें
```java
// सभी नोड्स को ट्रैस करें और मुख्य टेक्स्ट के साथ टेक्स्ट की तुलना करें
for (RichText richText : textNodes) {
    for (String key : replacements.keySet()) {
        richText.replace(key, replacements.get(key));
    }
}
```
रिचटेक्स्ट नोड्स के माध्यम से पुनरावृति करें और निर्दिष्ट टेक्स्ट को नए टेक्स्ट से बदलें।
## चरण 6: दस्तावेज़ सहेजें
```java
// किसी भी समर्थित फ़ाइल स्वरूप में सहेजें
oneFile.save(dataDir + "ReplaceTextonAllPages_out.pdf", SaveFormat.Pdf);
```
संशोधित दस्तावेज़ को अपने इच्छित फ़ाइल स्वरूप में सहेजें। इस उदाहरण में, हम इसे पीडीएफ के रूप में सहेज रहे हैं।
## निष्कर्ष
बधाई हो! आपने सफलतापूर्वक सीख लिया है कि OneNote में सभी पेजों पर टेक्स्ट को बदलने के लिए Java के लिए Aspose.Note का उपयोग कैसे करें। यह शक्तिशाली लाइब्रेरी दस्तावेज़ हेरफेर को सरल बनाती है, आपको लचीलापन और नियंत्रण प्रदान करती है।
## पूछे जाने वाले प्रश्न
### प्रश्न: क्या मैं अन्य दस्तावेज़ प्रारूपों के साथ जावा के लिए Aspose.Note का उपयोग कर सकता हूँ?
Aspose.Note मुख्य रूप से Microsoft OneNote फ़ाइलों का समर्थन करता है, लेकिन Aspose विभिन्न दस्तावेज़ प्रारूपों के लिए लाइब्रेरी प्रदान करता है।
### प्रश्न: मैं जावा के लिए Aspose.Note के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?
 आप यहां से अस्थायी लाइसेंस प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/).
### प्रश्न: क्या Aspose.Note के लिए सामुदायिक सहायता उपलब्ध है?
 हां, आप यहां सामुदायिक सहायता पा सकते हैं[Aspose.नोट फोरम](https://forum.aspose.com/c/note/28).
### प्रश्न: मैं जावा के लिए Aspose.Note के लिए दस्तावेज़ कहां पा सकता हूं?
 दस्तावेज़ उपलब्ध है[यहाँ](https://reference.aspose.com/note/java/).
### प्रश्न: क्या मैं जावा के लिए Aspose.Note खरीद सकता हूँ? 
 हां, आप जावा के लिए Aspose.Note खरीद सकते हैं[यहाँ](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
