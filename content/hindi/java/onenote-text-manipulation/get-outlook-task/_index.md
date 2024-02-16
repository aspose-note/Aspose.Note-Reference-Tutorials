---
title: OneNote में आउटलुक कार्य प्राप्त करें - Aspose.Note
linktitle: OneNote में आउटलुक कार्य प्राप्त करें - Aspose.Note
second_title: Aspose.नोट जावा एपीआई
description: OneNote दस्तावेज़ों से आसानी से Outlook कार्य विवरण निकालने में Java के लिए Aspose.Note की क्षमता का अन्वेषण करें। इस मजबूत लाइब्रेरी के साथ अपने जावा विकास को उन्नत करें।
type: docs
weight: 10
url: /hi/java/onenote-text-manipulation/get-outlook-task/
---
## परिचय
जावा के लिए Aspose.Note की दुनिया में आपका स्वागत है - एक शक्तिशाली उपकरण जो जावा डेवलपर्स को Microsoft OneNote फ़ाइलों के साथ निर्बाध रूप से काम करने में सक्षम बनाता है। इस चरण-दर-चरण मार्गदर्शिका में, हम आपको जावा के लिए Aspose.Note का उपयोग करके OneNote दस्तावेज़ से आउटलुक कार्य जानकारी निकालने की प्रक्रिया के बारे में बताएंगे।
## आवश्यक शर्तें
ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:
- जावा डेवलपमेंट किट (जेडीके): सुनिश्चित करें कि आपके सिस्टम पर जावा स्थापित है।
-  जावा के लिए Aspose.Note: Aspose.Note लाइब्रेरी को डाउनलोड और इंस्टॉल करें[डाउनलोड पेज](https://releases.aspose.com/note/java/).
## पैकेज आयात करें
अपने जावा प्रोजेक्ट में आवश्यक पैकेज आयात करके शुरुआत करें। अपनी जावा फ़ाइल की शुरुआत में निम्नलिखित पंक्तियाँ जोड़ें:
```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.ITag;
import com.aspose.note.NoteTask;
import com.aspose.note.RichText;
```
## चरण 1: अपना प्रोजेक्ट सेट करें
एक नया जावा प्रोजेक्ट बनाएं और अपने प्रोजेक्ट की निर्भरता में Aspose.Note लाइब्रेरी को शामिल करें। सुनिश्चित करें कि आपकी परियोजना संरचना व्यवस्थित है, और आपके पास अपने दस्तावेज़ों के लिए एक समर्पित निर्देशिका है।
## चरण 2: OneNote दस्तावेज़ लोड करें
अपने OneNote दस्तावेज़ को Aspose.Note में लोड करने के लिए निम्नलिखित कोड का उपयोग करें:
```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```
अपने OneNote दस्तावेज़ के पथ के साथ "आपकी दस्तावेज़ निर्देशिका" को बदलना सुनिश्चित करें।
## चरण 3: रिचटेक्स्ट नोड्स पुनर्प्राप्त करें
निम्नलिखित कोड का उपयोग करके दस्तावेज़ से सभी रिचटेक्स्ट नोड्स निकालें:
```java
List<RichText> nodes = (List<RichText>) doc.getChildNodes(RichText.class);
```
## चरण 4: प्रत्येक नोड के माध्यम से पुनरावृति करें
प्रत्येक रिचटेक्स्ट नोड के माध्यम से लूप करें और पहचानें कि इसमें नोटटास्क टैग है या नहीं:
```java
for (RichText richText : nodes) {
    for (ITag tag : richText.getTags()) {
        if (tag.getClass() == NoteTask.class) {
            // NoteTask को संभालने के लिए आपका कोड
        }
    }
}
```
## चरण 5: कार्य गुण पुनः प्राप्त करें
नोटटास्क के विभिन्न गुणों को पुनः प्राप्त करें और प्रिंट करें, जैसे पूर्ण समय, निर्माण समय, नियत तिथि, स्थिति और आइकन:
```java
NoteTask noteTask = (NoteTask) tag;
System.out.println("Completed Time: " + noteTask.getCompletedTime());
System.out.println("Create Time: " + noteTask.getCreationTime());
System.out.println("Due Date: " + noteTask.getDueDate());
System.out.println("Status: " + noteTask.getStatus());
System.out.println("Icon: " + noteTask.getIcon());
```
दस्तावेज़ में सभी नोटटास्क नोड्स के लिए इस प्रक्रिया को दोहराएं।
## निष्कर्ष
बधाई हो! आपने OneNote दस्तावेज़ से Outlook कार्य जानकारी निकालने के लिए Java के लिए Aspose.Note का उपयोग करना सफलतापूर्वक सीख लिया है। यह शक्तिशाली लाइब्रेरी Microsoft OneNote फ़ाइलों के साथ काम करने वाले जावा डेवलपर्स के लिए संभावनाओं की दुनिया खोलती है।
## पूछे जाने वाले प्रश्न
### प्रश्न: क्या मैं अन्य जावा फ्रेमवर्क के साथ जावा के लिए Aspose.Note का उपयोग कर सकता हूं?
उत्तर: हां, जावा के लिए Aspose.Note विभिन्न जावा फ्रेमवर्क के साथ संगत है, जो एकीकरण में लचीलापन प्रदान करता है।
### प्रश्न: क्या जावा के लिए Aspose.Note का निःशुल्क परीक्षण उपलब्ध है?
 उत्तर: हां, आप जावा के लिए Aspose.Note का निःशुल्क परीक्षण देख सकते हैं[यहाँ](https://releases.aspose.com/).
### प्रश्न: मैं जावा के लिए Aspose.Note के लिए समर्थन कैसे प्राप्त कर सकता हूं?
 ए: पर जाएँ[Aspose.नोट फोरम](https://forum.aspose.com/c/note/28) सामुदायिक सहायता के लिए या प्रीमियम सहायता विकल्प तलाशने के लिए।
### प्रश्न: मैं जावा के लिए Aspose.Note के लिए विस्तृत दस्तावेज़ कहां पा सकता हूं?
 ए: का संदर्भ लें[जावा दस्तावेज़ीकरण के लिए Aspose.Note](https://reference.aspose.com/note/java/) गहन जानकारी के लिए.
### प्रश्न: मैं जावा के लिए Aspose.Note के लिए अस्थायी लाइसेंस कैसे प्राप्त करूं?
 उत्तर: अपना अस्थायी लाइसेंस प्राप्त करें[यहाँ](https://purchase.aspose.com/temporary-license/).