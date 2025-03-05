---
title: OneNote में टेक्स्ट पर डार्क थीम लागू करें - Aspose.Note
linktitle: OneNote में टेक्स्ट पर डार्क थीम लागू करें - Aspose.Note
second_title: Aspose.नोट जावा एपीआई
description: Java के लिए Aspose.Note का उपयोग करके अपने OneNote टेक्स्ट पर डार्क थीम लागू करने के आसान चरणों का पता लगाएं। अपने डिजिटल दस्तावेज़ीकरण अनुभव को सहजता से उन्नत करें।
type: docs
weight: 11
url: /hi/java/onenote-text-manipulation/apply-dark-theme/
---
## परिचय
डिजिटल दस्तावेज़ीकरण के निरंतर विकसित हो रहे परिदृश्य में, आपके नोट्स का सौंदर्यशास्त्र पठनीयता और उपयोगकर्ता अनुभव को महत्वपूर्ण रूप से प्रभावित कर सकता है। एक उल्लेखनीय पहलू एक डार्क थीम का कार्यान्वयन है, जो देखने में आकर्षक और आरामदायक वातावरण प्रदान करता है। इस ट्यूटोरियल में, हम जावा के लिए Aspose.Note का उपयोग करके OneNote में टेक्स्ट पर डार्क थीम लागू करने की प्रक्रिया में आपका मार्गदर्शन करेंगे।
## आवश्यक शर्तें
ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित शर्तें हैं:
-  जावा के लिए Aspose.Note: जावा लाइब्रेरी के लिए Aspose.Note को डाउनलोड और इंस्टॉल करें[यहाँ](https://releases.aspose.com/note/java/).
- जावा डेवलपमेंट किट (जेडीके): सुनिश्चित करें कि आपकी मशीन पर जावा स्थापित है।
- एकीकृत विकास पर्यावरण (आईडीई): निर्बाध विकास के लिए एक्लिप्स या इंटेलीजे जैसी आईडीई चुनें।
## पैकेज आयात करें
आरंभ करने के लिए, अपने जावा प्रोजेक्ट में आवश्यक पैकेज आयात करें:
```java
import com.aspose.note.*;
import java.awt.*;
import java.io.IOException;
import java.nio.file.Paths;
```
## चरण 1: पृष्ठ पृष्ठभूमि रंग सेट करें
```java
// दस्तावेज़ निर्देशिका का पथ.
String dataDir = "Your Document Directory";
// दस्तावेज़ को Aspose.Note में लोड करें।
Document doc = new Document(Paths.get(dataDir, "Aspose.one").toString());
for (Page page: doc)
{
    page.setBackgroundColor(Color.BLACK);
}
```
## चरण 2: टेक्स्ट का रंग समायोजित करें
```java
for (RichText node: doc.getChildNodes(RichText.class))
{
    Color c = node.getParagraphStyle().getFontColor();
    if (c.getAlpha() <= 10 || Math.abs(c.getRed() - Color.BLACK.getRed()) + Math.abs(c.getGreen() - Color.BLACK.getGreen()) + Math.abs(c.getBlue() - Color.BLACK.getBlue()) <= 30)
    {
        node.getParagraphStyle().setFontColor(Color.WHITE);
    }
}
```
## चरण 3: दस्तावेज़ सहेजें
```java
doc.save(Paths.get(dataDir, "AsposeDarkTheme.pdf").toString());
```
प्रत्येक दस्तावेज़ के लिए इन चरणों को दोहराएं, और आप जावा के लिए Aspose.Note का उपयोग करके अपने OneNote टेक्स्ट पर एक डार्क थीम सफलतापूर्वक लागू कर लेंगे।
## निष्कर्ष
अंत में, जावा के लिए Aspose.Note के साथ अपने डिजिटल नोट्स की दृश्य अपील को बढ़ाना आसान है। इस चरण-दर-चरण मार्गदर्शिका का पालन करके, आप आसानी से OneNote में टेक्स्ट पर एक डार्क थीम लागू कर सकते हैं, जिससे आपका दस्तावेज़ीकरण अनुभव बेहतर हो जाएगा।
## पूछे जाने वाले प्रश्न
### क्या मैं डार्क थीम को केवल विशिष्ट अनुभागों पर ही लागू कर सकता हूँ?
हां, आप अपने दस्तावेज़ के विशिष्ट अनुभागों में डार्क थीम को चुनिंदा रूप से लागू करने के लिए कोड को संशोधित कर सकते हैं।
### क्या Java के लिए Aspose.Note में पूर्वनिर्धारित डार्क थीम उपलब्ध हैं?
अभी तक, जावा के लिए Aspose.Note आपको थीम को अनुकूलित करने की अनुमति देता है, लेकिन कोई पूर्वनिर्धारित डार्क थीम नहीं हैं।
### क्या जावा के लिए Aspose.Note अन्य दस्तावेज़ प्रारूपों का समर्थन करता है?
हाँ, Java के लिए Aspose.Note PDF, DOCX और HTML सहित विभिन्न दस्तावेज़ स्वरूपों का समर्थन करता है।
### क्या जावा के लिए Aspose.Note का कोई परीक्षण संस्करण उपलब्ध है?
 हां, आप निःशुल्क परीक्षण संस्करण तक पहुंच सकते हैं[यहाँ](https://releases.aspose.com/).
### मैं जावा के लिए Aspose.Note के लिए समर्थन कैसे प्राप्त कर सकता हूँ?
 दौरा करना[Aspose.नोट फोरम](https://forum.aspose.com/c/note/28) सामुदायिक सहायता के लिए या प्रीमियम सहायता विकल्प तलाशने के लिए[यहाँ](https://purchase.aspose.com/temporary-license/).