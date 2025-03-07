---
title: OneNote में सेल पृष्ठभूमि रंग सेट करना - Aspose.Note
linktitle: OneNote में सेल पृष्ठभूमि रंग सेट करना - Aspose.Note
second_title: Aspose.नोट जावा एपीआई
description: Java के लिए Aspose.Note का उपयोग करके आसानी से OneNote दस्तावेज़ों को रूपांतरित करें। सेल पृष्ठभूमि रंगों को सहजता से अनुकूलित करें। अभी निशुल्क परीक्षण आज़माएं!
weight: 17
url: /hi/java/onenote-table-manipulation/setting-cell-background-color/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote में सेल पृष्ठभूमि रंग सेट करना - Aspose.Note

## परिचय
Java के लिए Aspose.Note का उपयोग करके OneNote में सेल पृष्ठभूमि रंग सेट करने पर हमारे ट्यूटोरियल में आपका स्वागत है! इस चरण-दर-चरण मार्गदर्शिका में, हम आपको आपके OneNote दस्तावेज़ों में सेल पृष्ठभूमि रंगों को सहजता से अनुकूलित करने की प्रक्रिया के बारे में बताएंगे।
## आवश्यक शर्तें
शुरू करने से पहले, सुनिश्चित करें कि आपके पास आवश्यक शर्तें हैं:
1.  जावा लाइब्रेरी के लिए Aspose.Note: इसे यहां से डाउनलोड और इंस्टॉल करें[यहाँ](https://releases.aspose.com/note/java/).
   
2. जावा विकास वातावरण: अपना जावा विकास वातावरण स्थापित करें।
3. दस्तावेज़ निर्देशिका: एक निर्देशिका तैयार रखें जहाँ आपका OneNote दस्तावेज़ स्थित है।
अब, आइए ट्यूटोरियल के बारे में गहराई से जानें!
## पैकेज आयात करें
सबसे पहले, अपने जावा प्रोजेक्ट में आवश्यक पैकेज आयात करें:
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.OutlineElement;
import com.aspose.note.RichText;
import com.aspose.note.TableCell;
import com.aspose.note.TableRow;
import com.aspose.note.ParagraphStyle;
```
## चरण 1: अपना प्रोजेक्ट सेट करें
सुनिश्चित करें कि आपका जावा विकास वातावरण तैयार है, और आपने जावा के लिए Aspose.Note को अपने प्रोजेक्ट में एकीकृत कर लिया है।
## चरण 2: अपना OneNote दस्तावेज़ लोड करें
```java
Document doc = new Document();
```
## चरण 3: TableRow ऑब्जेक्ट को आरंभ करें
अपनी OneNote तालिका में एक पंक्ति का प्रतिनिधित्व करने के लिए एक TableRow ऑब्जेक्ट बनाएं:
```java
TableRow row1 = new TableRow();
```
## चरण 4: टेबलसेल ऑब्जेक्ट को आरंभ करें
पंक्ति के भीतर एक टेबलसेल ऑब्जेक्ट प्रारंभ करें और वांछित टेक्स्ट सामग्री सेट करें:
```java
TableCell cell11 = new TableCell();
cell11.appendChildLast(GetOutlineElementWithText("Small text"));
```
## चरण 5: सेल पृष्ठभूमि रंग सेट करें
 उपयोग`setBackgroundColor` सेल के पृष्ठभूमि रंग को अनुकूलित करने की विधि (इस उदाहरण में, काले पर सेट):
```java
cell11.setBackgroundColor(Color.BLACK);
```
## चरण 6: अपना दस्तावेज़ सहेजें
आवश्यक परिवर्तन करने के बाद अपने संशोधित OneNote दस्तावेज़ को सहेजना न भूलें।
अतिरिक्त अनुकूलन के लिए आवश्यकतानुसार इन चरणों को दोहराएं, और आप पूरी तरह तैयार हैं!
## निष्कर्ष
बधाई हो! आपने Java के लिए Aspose.Note का उपयोग करके OneNote में सेल पृष्ठभूमि रंग सेट करना सफलतापूर्वक सीख लिया है। आगे के अनुकूलन विकल्पों का पता लगाने और अपने OneNote दस्तावेज़ों को निर्बाध रूप से बढ़ाने के लिए स्वतंत्र महसूस करें।
### पूछे जाने वाले प्रश्न
### क्या मैं इस विधि को एक साथ अनेक कोशिकाओं पर लागू कर सकता हूँ?
हां, आप पृष्ठभूमि रंग को एक साथ कई कोशिकाओं पर लागू करने के लिए अपनी तालिका की पंक्तियों और कोशिकाओं के माध्यम से लूप कर सकते हैं।
### क्या ऐसे पूर्वनिर्धारित रंग हैं जिनका मैं उपयोग कर सकता हूँ?
 Aspose.Note पूर्वनिर्धारित स्थिरांक सहित रंगों की एक विस्तृत श्रृंखला का समर्थन करता है`Color.BLACK` . दस्तावेज़ीकरण की जाँच करें[यहाँ](https://reference.aspose.com/note/java/) पूरी सूची के लिए.
### क्या कोई परीक्षण संस्करण उपलब्ध है?
 हाँ, आप निःशुल्क परीक्षण संस्करण प्राप्त कर सकते हैं[यहाँ](https://releases.aspose.com/).
### यदि मुझे कोई समस्या आती है तो मुझे सहायता कैसे मिल सकती है?
 सहायता फ़ोरम पर जाएँ[यहाँ](https://forum.aspose.com/c/note/28) Aspose समुदाय से सहायता प्राप्त करने के लिए।
### मैं जावा के लिए Aspose.Note कहां से खरीद सकता हूं?
 आप लाइब्रेरी खरीद सकते हैं[यहाँ](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
