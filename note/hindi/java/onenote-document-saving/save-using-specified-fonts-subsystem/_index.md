---
title: OneNote में निर्दिष्ट फ़ॉन्ट सबसिस्टम का उपयोग करके सहेजें
linktitle: OneNote में निर्दिष्ट फ़ॉन्ट सबसिस्टम का उपयोग करके सहेजें
second_title: Aspose.नोट जावा एपीआई
description: Aspose.Note के साथ जावा में निर्दिष्ट फ़ॉन्ट सबसिस्टम का उपयोग करके OneNote दस्तावेज़ों को सहेजना सीखें। सभी प्लेटफ़ॉर्म पर सहजता से लगातार फ़ॉन्ट प्रतिनिधित्व सुनिश्चित करें।
weight: 22
url: /hi/java/onenote-document-saving/save-using-specified-fonts-subsystem/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote में निर्दिष्ट फ़ॉन्ट सबसिस्टम का उपयोग करके सहेजें

## परिचय

Java के लिए Aspose.Note OneNote दस्तावेज़ों के साथ काम करने के लिए मजबूत क्षमताएं प्रदान करता है। ऐसे दस्तावेज़ों के साथ काम करते समय एक सामान्य आवश्यकता यह सुनिश्चित करना है कि फ़ॉन्ट ठीक से बनाए रखा जाए, खासकर यदि दस्तावेज़ को पीडीएफ जैसे विभिन्न प्रारूपों में निर्यात या सहेजा जाना है। यह ट्यूटोरियल फ़ॉन्ट सबसिस्टम को निर्दिष्ट करते हुए OneNote दस्तावेज़ों को सहेजने की प्रक्रिया में आपका मार्गदर्शन करेगा, जिससे विभिन्न प्लेटफ़ॉर्म पर टेक्स्ट का सुसंगत और सटीक प्रतिनिधित्व सुनिश्चित होगा।

## आवश्यक शर्तें

इससे पहले कि हम ट्यूटोरियल में उतरें, सुनिश्चित करें कि आपने निम्नलिखित पूर्वापेक्षाएँ स्थापित कर ली हैं:

### 1. जावा डेवलपमेंट किट (जेडीके)

 सुनिश्चित करें कि आपके सिस्टम पर जावा डेवलपमेंट किट (जेडीके) स्थापित है। आप इसे यहां से डाउनलोड कर सकते हैं[यहाँ](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html) यदि आपने पहले से नहीं किया है।

### 2. जावा लाइब्रेरी के लिए Aspose.Note

 जावा लाइब्रेरी के लिए Aspose.Note डाउनलोड करें और सेट करें। आप इसे यहां से डाउनलोड कर सकते हैं[वेबसाइट](https://releases.aspose.com/note/java/).

## पैकेज आयात करें

अपने जावा प्रोजेक्ट में आवश्यक पैकेज आयात करना सुनिश्चित करें:

```java
import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
import com.aspose.note.fonts.DocumentFontsSubsystem;
import java.io.FileInputStream;
import java.io.IOException;
import java.io.InputStream;
import java.nio.file.Paths;
```

आइए अब प्रक्रिया को बेहतर ढंग से समझने के लिए प्रत्येक उदाहरण को कई चरणों में विभाजित करें।

## चरण 1: डिफ़ॉल्ट फ़ॉन्ट नाम के साथ दस्तावेज़ फ़ॉन्ट सबसिस्टम का उपयोग करके सहेजें

यह चरण दर्शाता है कि निर्दिष्ट डिफ़ॉल्ट फ़ॉन्ट नाम का उपयोग करके किसी दस्तावेज़ को पीडीएफ प्रारूप में कैसे सहेजा जाए।

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName() throws IOException
{
    // दस्तावेज़ को Aspose.Note में लोड करें।
    Document oneFile = new Document("missing-font.one");

    // डिफ़ॉल्ट फ़ॉन्ट निर्दिष्ट करें.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFont("Times New Roman"));

    // दस्तावेज़ को पीडीएफ के रूप में सहेजें।
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf", options);
}
```

इस चरण में:
- OneNote दस्तावेज़ Aspose.Note का उपयोग करके लोड किया गया है।
- डिफ़ॉल्ट फ़ॉन्ट "टाइम्स न्यू रोमन" के रूप में निर्दिष्ट है।
- दस्तावेज़ निर्दिष्ट फ़ॉन्ट के साथ पीडीएफ प्रारूप में सहेजा गया है।

## चरण 2: फ़ाइल से डिफ़ॉल्ट फ़ॉन्ट के साथ दस्तावेज़ फ़ॉन्ट सबसिस्टम का उपयोग करके सहेजें

यह चरण दर्शाता है कि किसी फ़ाइल से लोड किए गए डिफ़ॉल्ट फ़ॉन्ट का उपयोग करके किसी दस्तावेज़ को पीडीएफ प्रारूप में कैसे सहेजा जाए।

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile() throws IOException
{
    // दस्तावेज़ को Aspose.Note में लोड करें।
    Document oneFile = new Document("missing-font.one");

    // फ़ॉन्ट फ़ाइल का पथ निर्दिष्ट करें.
    String fontFile = "geo_1.ttf";

    // फ़ाइल से डिफ़ॉल्ट फ़ॉन्ट निर्दिष्ट करें.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromFile(fontFile));

    // दस्तावेज़ को पीडीएफ के रूप में सहेजें।
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf", options);
}
```

इस चरण में:
- फ़ॉन्ट फ़ाइल "geo_1.ttf" लोड हो गई है।
- डिफ़ॉल्ट फ़ॉन्ट लोड की गई फ़ॉन्ट फ़ाइल से निर्दिष्ट किया गया है।
- दस्तावेज़ निर्दिष्ट फ़ॉन्ट के साथ पीडीएफ प्रारूप में सहेजा गया है।

## चरण 3: स्ट्रीम से डिफ़ॉल्ट फ़ॉन्ट के साथ दस्तावेज़ फ़ॉन्ट सबसिस्टम का उपयोग करके सहेजें

यह चरण दर्शाता है कि स्ट्रीम से लोड किए गए डिफ़ॉल्ट फ़ॉन्ट का उपयोग करके किसी दस्तावेज़ को पीडीएफ प्रारूप में कैसे सहेजा जाए।

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream() throws IOException
{
    // दस्तावेज़ को Aspose.Note में लोड करें।
    Document oneFile = new Document("missing-font.one");

    // फ़ॉन्ट फ़ाइल का पथ निर्दिष्ट करें.
    String fontFile = "geo_1.ttf";

    // फ़ॉन्ट फ़ाइल को स्ट्रीम के रूप में लोड करें।
    InputStream stream = new FileInputStream(fontFile);

    try
    {
        // स्ट्रीम से डिफ़ॉल्ट फ़ॉन्ट निर्दिष्ट करें.
        PdfSaveOptions options = new PdfSaveOptions();
        options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromStream(stream));

        // दस्तावेज़ को पीडीएफ के रूप में सहेजें।
        oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf", options);
    }
    catch (Exception e)
    {
        stream.close();
    }
}
```

इस चरण में:
- फ़ॉन्ट फ़ाइल "geo_1.ttf" एक स्ट्रीम के रूप में लोड की गई है।
- डिफ़ॉल्ट फ़ॉन्ट लोड की गई स्ट्रीम से निर्दिष्ट किया गया है।
- दस्तावेज़ निर्दिष्ट फ़ॉन्ट के साथ पीडीएफ प्रारूप में सहेजा गया है।

## निष्कर्ष

इस ट्यूटोरियल में, हमने सीखा कि Aspose.Note का उपयोग करके जावा में निर्दिष्ट फ़ॉन्ट सबसिस्टम का उपयोग करके OneNote दस्तावेज़ों को कैसे सहेजा जाए। इन चरणों का पालन करके, आप अपने दस्तावेज़ों को निर्यात या सहेजते समय विभिन्न प्लेटफार्मों पर लगातार फ़ॉन्ट प्रतिनिधित्व सुनिश्चित कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं दस्तावेज़ के विभिन्न भागों के लिए अलग-अलग फ़ॉन्ट निर्दिष्ट कर सकता हूँ?

A1: हाँ, आप Java के लिए Aspose.Note का उपयोग करके दस्तावेज़ के विभिन्न भागों के लिए अलग-अलग फ़ॉन्ट निर्दिष्ट कर सकते हैं।

### Q2: क्या Aspose.Note OneNote के सभी संस्करणों के साथ संगत है?

A2: Aspose.Note विभिन्न परिवेशों में अनुकूलता सुनिश्चित करते हुए, OneNote के विभिन्न संस्करणों का समर्थन करता है।

### Q3: दस्तावेज़ सहेजते समय मैं गुम फ़ॉन्ट को कैसे संभाल सकता हूँ?

A3: Aspose.Note दस्तावेज़ सहेजने के दौरान लापता फ़ॉन्ट को प्रभावी ढंग से संभालने के लिए डिफ़ॉल्ट फ़ॉन्ट निर्दिष्ट करने के विकल्प प्रदान करता है।

### Q4: क्या मैं आकार और शैली जैसे फ़ॉन्ट गुणों को अनुकूलित कर सकता हूँ?

A4: हाँ, आप Java के लिए Aspose.Note का उपयोग करके फ़ॉन्ट गुणों जैसे आकार, शैली और रंग को अनुकूलित कर सकते हैं।

### Q5: क्या Java के लिए Aspose.Note का कोई परीक्षण संस्करण उपलब्ध है?

A5: हाँ, आप वेबसाइट से Java के लिए Aspose.Note का निःशुल्क परीक्षण प्राप्त कर सकते हैं।
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
