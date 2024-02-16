---
title: OneNote में किसी पृष्ठ से टेक्स्ट निकालें - Aspose.Note
linktitle: OneNote में किसी पृष्ठ से टेक्स्ट निकालें - Aspose.Note
second_title: Aspose.नोट जावा एपीआई
description: जावा के लिए Aspose.Note का उपयोग करके OneNote पेजों से आसानी से टेक्स्ट निकालने का तरीका जानें। इस व्यापक चरण-दर-चरण मार्गदर्शिका के साथ अपनी प्रक्रियाओं को सुव्यवस्थित करें।
type: docs
weight: 16
url: /hi/java/onenote-text-manipulation/extract-text-from-a-page/
---
## परिचय
यदि आप जावा का उपयोग करके OneNote पेजों से कुशलतापूर्वक टेक्स्ट निकालने की क्षमता को अनलॉक करना चाहते हैं, तो आप सही जगह पर हैं। यह चरण-दर-चरण मार्गदर्शिका आपको जावा के लिए Aspose.Note का उपयोग करके प्रक्रिया के बारे में बताएगी। Aspose.Note एक शक्तिशाली API है जो OneNote दस्तावेज़ों के साथ काम करना सरल बनाता है, जिससे आप आसानी से पृष्ठों से पाठ को मूल रूप से निकाल सकते हैं।
## आवश्यक शर्तें
ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:
- जावा प्रोग्रामिंग की बुनियादी समझ।
-  जावा के लिए Aspose.Note स्थापित किया गया। आप इसे डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/note/java/).
## पैकेज आयात करें
Aspose.Note कार्यक्षमताओं का लाभ उठाने के लिए अपने जावा प्रोजेक्ट में आवश्यक पैकेज आयात करके प्रारंभ करें:
```java
import com.aspose.note.Document;
import com.aspose.note.Node;
import com.aspose.note.NodeType;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import java.util.List;
import java.util.stream.Collectors;
```
अब, आइए प्रत्येक चरण को विस्तार से देखें।
## चरण 1: दस्तावेज़ निर्देशिका सेट करें
 सुनिश्चित करें कि आपके पास एक निर्दिष्ट दस्तावेज़ निर्देशिका है जहाँ आपकी OneNote फ़ाइल संग्रहीत है। प्रतिस्थापित करें`"Your Document Directory"` वास्तविक पथ के साथ.
```java
// दस्तावेज़ निर्देशिका का पथ.
String dataDir = "Your Document Directory";
```
## चरण 2: OneNote दस्तावेज़ लोड करें
 उपयोग`Document` अपने OneNote दस्तावेज़ को लोड करने के लिए Aspose.Note से कक्षा:
```java
Document oneFile = new Document(dataDir + "Sample1.one");
```
 प्रतिस्थापित करें`"Sample1.one"` आपके OneNote फ़ाइल नाम के साथ.
## चरण 3: पृष्ठ नोड्स पुनः प्राप्त करें
लोड किए गए दस्तावेज़ से पृष्ठ नोड्स की सूची प्राप्त करें:
```java
List<Node> nodes = oneFile.getChildNodes(Node.class);
```
यह सुनिश्चित करता है कि आपके पास OneNote दस्तावेज़ के पृष्ठों तक पहुंच है।
## चरण 4: टेक्स्ट जांचें और निकालें
जांचें कि दस्तावेज़ में पृष्ठ हैं या नहीं, और यदि हां, तो पाठ पुनः प्राप्त करें:
```java
if (nodes.size() > 0 && nodes.get(0).getNodeType() == NodeType.Page)
{
    Page page = (Page)nodes.get(0);
    // पाठ पुनः प्राप्त करें
    List<RichText> textNodes = (List<RichText>) page.getChildNodes(RichText.class);
    StringBuilder text = new StringBuilder();
    for (RichText richText : textNodes) {
        text = text.append(richText.getText().toString());
    }
    
    // आउटपुट स्क्रीन पर टेक्स्ट प्रिंट करें
    System.out.println(text);
}
```
यह स्निपेट जाँचता है कि पहला नोड एक पेज है या नहीं और फिर टेक्स्ट को निकालता और प्रिंट करता है।
जावा के लिए Aspose.Note का उपयोग करके OneNote पेजों से टेक्स्ट निकालने में अपने जावा एप्लिकेशन की क्षमताओं को बढ़ाने के लिए इन चरणों को जारी रखें।
## निष्कर्ष
बधाई हो! आपने जावा के लिए Aspose.Note का उपयोग करके OneNote पृष्ठों से टेक्स्ट निकालने का तरीका सफलतापूर्वक सीख लिया है। इस ज्ञान को अपनी परियोजनाओं में शामिल करें और अपनी पाठ निष्कर्षण प्रक्रियाओं को सहजता से सुव्यवस्थित करें।
## अक्सर पूछे जाने वाले प्रश्नों
### क्या मैं अन्य प्रोग्रामिंग भाषाओं के साथ जावा के लिए Aspose.Note का उपयोग कर सकता हूँ?
Aspose.Note मुख्य रूप से जावा का समर्थन करता है लेकिन इसमें .NET जैसी अन्य भाषाओं के लिए संस्करण हैं। भाषा अनुकूलता के लिए दस्तावेज़ की जाँच करें.
### क्या जावा के लिए Aspose.Note का कोई परीक्षण संस्करण उपलब्ध है?
 हां, आप नि:शुल्क परीक्षण संस्करण तलाश सकते हैं[यहाँ](https://releases.aspose.com/).
### मुझे जावा के लिए Aspose.Note के लिए समर्थन कहां मिल सकता है?
 Aspose.Note पर जाएँ[मंच](https://forum.aspose.com/c/note/28) सामुदायिक समर्थन और चर्चा के लिए।
### मैं जावा के लिए Aspose.Note कैसे खरीद सकता हूँ?
 आप उत्पाद खरीद सकते हैं[यहाँ](https://purchase.aspose.com/buy).
### क्या मुझे Java के लिए Aspose.Note के लिए अस्थायी लाइसेंस की आवश्यकता है?
 यदि आपको अस्थायी लाइसेंस की आवश्यकता है, तो आप एक प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/).