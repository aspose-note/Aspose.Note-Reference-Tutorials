---
date: 2025-12-18
description: Aspose.Note के साथ जावा में निर्दिष्ट फ़ॉन्ट सबसिस्टम का उपयोग करके **OneNote
  को PDF के रूप में सहेजना** सीखें। यह गाइड यह भी दिखाता है कि OneNote को PDF में
  कैसे बदलें, कस्टम फ़ॉन्ट फ़ाइलें कैसे लोड करें, और डिफ़ॉल्ट फ़ॉन्ट कैसे निर्दिष्ट
  करें।
linktitle: Save OneNote as PDF Using Specified Fonts Subsystem
second_title: Aspose.Note Java API
title: निर्दिष्ट फ़ॉन्ट सबसिस्टम का उपयोग करके OneNote को PDF के रूप में सहेजें
url: /hi/java/onenote-document-saving/save-using-specified-fonts-subsystem/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# निर्दिष्ट फ़ॉन्ट सबसिस्टम का उपयोग करके OneNote को PDF के रूप में सहेजें

## परिचय

कई व्यावसायिक परिदृश्यों में आपको **OneNote को PDF के रूप में सहेजना** पड़ता है जबकि मूल पृष्ठों की सटीक रूपरेखा को बनाए रखा जाता है। Aspose.Note for Java इसे सरल बनाता है क्योंकि यह रूपांतरण के दौरान फ़ॉन्ट सबसिस्टम को नियंत्रित करने की अनुमति देता है। इस ट्यूटोरियल में हम **OneNote को PDF में बदलने** के तीन व्यावहारिक तरीकों को देखेंगे, जिसमें **कस्टम फ़ॉन्ट फ़ाइलें लोड करना**, **डिफ़ॉल्ट फ़ॉन्ट निर्दिष्ट करना**, और जब लक्ष्य मशीन पर फ़ॉन्ट उपलब्ध न हो तो **फ़ॉन्ट स्ट्रीम का उपयोग करना** शामिल है।

## त्वरित उत्तर
- **OneNote को PDF के रूप में सहेजना** का क्या अर्थ है? यह .one फ़ाइल को PDF में बदलता है जबकि लेआउट और शैली को अपरिवर्तित रखता है।  
- **कौन सा API फ़ॉन्ट्स को संभालता है?** `DocumentFontsSubsystem` आपको डिफ़ॉल्ट फ़ॉन्ट निर्धारित करने या कस्टम फ़ॉन्ट फ़ाइल/स्ट्रीम लोड करने की अनुमति देता है।  
- **क्या उत्पादन के लिए लाइसेंस चाहिए?** हाँ, गैर‑ट्रायल उपयोग के लिए एक व्यावसायिक Aspose.Note लाइसेंस आवश्यक है।  
- **क्या मैं बैच में कई फ़ाइलें बदल सकता हूँ?** बिल्कुल – बस `Document` लोडिंग और सहेजने की लॉजिक को लूप करें।  
- **कौन सा Java संस्करण आवश्यक है?** Java 15 या बाद का (उदाहरण में JDK 15 उपयोग किया गया है)।

## फ़ॉन्ट सबसिस्टम के साथ “OneNote को PDF के रूप में सहेजना” क्या है?
फ़ॉन्ट सबसिस्टम के साथ OneNote को PDF के रूप में सहेजना का अर्थ है कि रूपांतरण प्रक्रिया के दौरान Aspose.Note किसी भी लापता ग्लिफ़ को आपके द्वारा प्रदान किए गए फ़ॉन्ट से बदल देता है। इससे यह सुनिश्चित होता है कि PDF किसी भी डिवाइस पर समान दिखे, भले ही मूल फ़ॉन्ट स्थापित न हो।

## जब आप **OneNote को PDF में बदलते** हैं तो फ़ॉन्ट सबसिस्टम को नियंत्रित क्यों करें?
- **सुसंगत ब्रांडिंग** – कॉरपोरेट दस्तावेज़ सटीक टाइपफ़ेस को बनाए रखते हैं।  
- **क्रॉस‑प्लेटफ़ॉर्म विश्वसनीयता** – PDFs Windows, macOS, Linux, और मोबाइल पर समान रूप से रेंडर होते हैं।  
- **त्रुटियों में कमी** – लापता फ़ॉन्ट चेतावनियाँ गायब हो जाती हैं, जिससे साफ़ आउटपुट मिलता है।

## पूर्वापेक्षाएँ

### 1. Java Development Kit (JDK)

सुनिश्चित करें कि आपके सिस्टम पर Java Development Kit (JDK) स्थापित है। यदि अभी तक नहीं किया है तो आप इसे [यहाँ](https://www.oracle.com/java/technologies/javasedk15-downloads.html) से डाउनलोड कर सकते हैं।

### 2. Aspose.Note for Java लाइब्रेरी

Aspose.Note for Java लाइब्रेरी डाउनलोड करें और सेट अप करें। आप इसे [वेबसाइट](https://releases.aspose.com/note/java/) से डाउनलोड कर सकते हैं।

## इम्पोर्ट पैकेज

सुनिश्चित करें कि आप अपने Java प्रोजेक्ट में आवश्यक पैकेज इम्पोर्ट करें:

```java
import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
import com.aspose.note.fonts.DocumentFontsSubsystem;
import java.io.FileInputStream;
import java.io.IOException;
import java.io.InputStream;
import java.nio.file.Paths;
```

अब हम प्रत्येक उदाहरण को कई चरणों में विभाजित करेंगे ताकि प्रक्रिया को बेहतर समझा जा सके।

## डॉक्यूमेंट फ़ॉन्ट्स सबसिस्टम का उपयोग करके डिफ़ॉल्ट फ़ॉन्ट के साथ **OneNote को PDF के रूप में सहेजने** का तरीका

### चरण 1: डिफ़ॉल्ट फ़ॉन्ट नाम के साथ डॉक्यूमेंट फ़ॉन्ट्स सबसिस्टम का उपयोग करके सहेजें

यह चरण डिफ़ॉल्ट फ़ॉन्ट नाम निर्दिष्ट करके **OneNote को PDF के रूप में सहेजने** का सरल तरीका दर्शाता है।

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName() throws IOException
{
    // Load the document into Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Specify the default font.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFont("Times New Roman"));

    // Save the document as PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf", options);
}
```

इस चरण में:
- OneNote दस्तावेज़ Aspose.Note का उपयोग करके लोड किया गया है।
- **डिफ़ॉल्ट फ़ॉन्ट** को **"Times New Roman"** के रूप में निर्दिष्ट किया गया है।
- दस्तावेज़ को चुने हुए फ़ॉन्ट के साथ PDF फ़ॉर्मेट में सहेजा गया है।

### चरण 2: फ़ाइल से डिफ़ॉल्ट फ़ॉन्ट के साथ डॉक्यूमेंट फ़ॉन्ट्स सबसिस्टम का उपयोग करके सहेजें

यहाँ हम **कस्टम फ़ॉन्ट फ़ाइल लोड** करते हैं और इसे PDF में बदलते समय फ़ॉलबैक के रूप में उपयोग करते हैं।

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile() throws IOException
{
    // Load the document into Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Specify the path to the font file.
    String fontFile = "geo_1.ttf";

    // Specify the default font from the file.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromFile(fontFile));

    // Save the document as PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf", options);
}
```

मुख्य बिंदु:
- **कस्टम फ़ॉन्ट फ़ाइल** `geo_1.ttf` **डिस्क से लोड** की गई है।
- `usingDefaultFontFromFile` **फ़ाइल से डिफ़ॉल्ट फ़ॉन्ट निर्दिष्ट** करता है, जिससे मूल फ़ॉन्ट अनुपलब्ध होने पर PDF इस फ़ॉन्ट का उपयोग करता है।
- परिणामी PDF इच्छित रूप को बनाए रखता है।

### चरण 3: स्ट्रीम से डिफ़ॉल्ट फ़ॉन्ट के साथ डॉक्यूमेंट फ़ॉन्ट्स सबसिस्टम का उपयोग करके सहेजें

कभी-कभी फ़ॉन्ट डेटाबेस में संग्रहीत हो सकता है या नेटवर्क के माध्यम से प्राप्त हो सकता है। यह उदाहरण दिखाता है कि **फ़ॉन्ट स्ट्रीम का उपयोग कैसे करें**।

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream() throws IOException
{
    // Load the document into Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Specify the path to the font file.
    String fontFile = "geo_1.ttf";

    // Load the font file as a stream.
    InputStream stream = new FileInputStream(fontFile);

    try
    {
        // Specify the default font from the stream.
        PdfSaveOptions options = new PdfSaveOptions();
        options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromStream(stream));

        // Save the document as PDF.
        oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf", options);
    }
    catch (Exception e)
    {
        stream.close();
    }
}
```

यहाँ क्या होता है:
- फ़ॉन्ट फ़ाइल को **InputStream** के रूप में खोला जाता है, जो तब उपयोगी है जब फ़ॉन्ट फ़ाइल स्रोत नहीं होता।
- `usingDefaultFontFromStream` **फ़ॉन्ट स्ट्रीम का उपयोग** करके फ़ॉलबैक फ़ॉन्ट निर्धारित करता है।
- OneNote फ़ाइल को स्ट्रीम‑आधारित फ़ॉन्ट के साथ PDF के रूप में सहेजा जाता है।

## सामान्य समस्याएँ और समाधान

| समस्या | कारण | समाधान |
|-------|------|--------|
| **Missing font warnings** | स्रोत .one फ़ाइल में ऐसा फ़ॉन्ट संदर्भित है जो मशीन पर मौजूद नहीं है। | `usingDefaultFont`, `usingDefaultFontFromFile`, या `usingDefaultFontFromStream` के माध्यम से डिफ़ॉल्ट फ़ॉन्ट प्रदान करें। |
| **File not found for custom font** | `.ttf` फ़ाइल का पथ गलत है। | पूर्ण पथ (absolute path) का उपयोग करें या कार्य निर्देशिका से सापेक्ष पथ की जाँच करें। |
| **Stream not closed** | `close()` कॉल होने से पहले अपवाद (exception) उत्पन्न हो जाता है। | स्वचालित बंद करने के लिए try‑with‑resources (`try (InputStream stream = ...) { ... }`) का उपयोग करें। |

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या मैं दस्तावेज़ के विभिन्न भागों के लिए अलग-अलग फ़ॉन्ट निर्दिष्ट कर सकता हूँ?**  
A: हाँ, आप Aspose.Note में `Font` क्लास का उपयोग करके व्यक्तिगत रिच टेक्स्ट तत्वों पर कस्टम फ़ॉन्ट सेटिंग्स लागू कर सकते हैं।

**Q: क्या Aspose.Note सभी OneNote संस्करणों के साथ संगत है?**  
A: Aspose.Note हाल के डेस्कटॉप और मोबाइल संस्करणों की OneNote फ़ाइलों का समर्थन करता है, जिससे व्यापक संगतता सुनिश्चित होती है।

**Q: दस्तावेज़ सहेजते समय लापता फ़ॉन्ट्स को कैसे संभालूँ?**  
A: ऊपर दिखाए गए फ़ॉन्ट सबसिस्टम मेथड्स (`usingDefaultFont`, `usingDefaultFontFromFile`, `usingDefaultFontFromStream`) का उपयोग करके फ़ॉलबैक प्रदान करें।

**Q: क्या मैं फ़ॉन्ट गुण जैसे आकार और शैली को अनुकूलित कर सकता हूँ?**  
A: बिल्कुल – API आपको प्रत्येक रन के आधार पर आकार, शैली, रंग और अन्य गुण सेट करने की अनुमति देता है।

**Q: क्या Aspose.Note for Java का ट्रायल संस्करण उपलब्ध है?**  
A: हाँ, एक मुफ्त ट्रायल Aspose वेबसाइट से डाउनलोड किया जा सकता है।

## निष्कर्ष

इस ट्यूटोरियल में हमने Java में Aspose.Note के साथ फ़ॉन्ट सबसिस्टम को नियंत्रित करते हुए **OneNote को PDF के रूप में सहेजने** का तरीका सीखा। तीनों तरीकों—डिफ़ॉल्ट फ़ॉन्ट नाम निर्दिष्ट करना, कस्टम फ़ॉन्ट फ़ाइल लोड करना, या फ़ॉन्ट स्ट्रीम का उपयोग करना—का पालन करके आप अपने OneNote दस्तावेज़ों को निर्यात या सहेजते समय प्लेटफ़ॉर्म के बीच सुसंगत फ़ॉन्ट प्रतिनिधित्व सुनिश्चित कर सकते हैं।

---

**अंतिम अपडेट:** 2025-12-18  
**परीक्षित संस्करण:** Aspose.Note for Java 24.11  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}