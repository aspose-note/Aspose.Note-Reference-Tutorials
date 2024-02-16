---
title: OneNote दस्तावेज़ बनाएं और HTML - Java में सहेजें
linktitle: OneNote दस्तावेज़ बनाएं और HTML - Java में सहेजें
second_title: Aspose.नोट जावा एपीआई
description: Java के लिए Aspose.Note का उपयोग करके OneNote दस्तावेज़ों को HTML के रूप में बनाना और सहेजना सीखें। प्रोग्रामेटिक OneNote फ़ाइल प्रबंधन के लिए जावा अनुप्रयोगों में एकीकृत करें।

type: docs
weight: 18
url: /hi/java/onenote-document-loading/create-onenote-save-to-html/
---
## परिचय

जावा के लिए Aspose.Note एक शक्तिशाली लाइब्रेरी है जो डेवलपर्स को Microsoft OneNote फ़ाइलों के साथ प्रोग्रामेटिक रूप से काम करने की अनुमति देती है। इस ट्यूटोरियल में, हम जानेंगे कि OneNote दस्तावेज़ कैसे बनाएं और Java के लिए Aspose.Note का उपयोग करके इसे HTML प्रारूप में कैसे सहेजें।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

1. आपके सिस्टम पर जावा डेवलपमेंट किट (जेडीके) स्थापित है।
2.  जावा लाइब्रेरी के लिए Aspose.Note। आप इसे यहां से डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/note/java/).
3. जावा प्रोग्रामिंग का बुनियादी ज्ञान।

## पैकेज आयात करें

सबसे पहले, अपने जावा प्रोजेक्ट में आवश्यक पैकेज आयात करें:

```java
import java.io.ByteArrayOutputStream;
import java.io.File;
import java.io.FileOutputStream;
import java.io.IOException;
import java.io.OutputStream;
import java.io.OutputStreamWriter;
import java.nio.file.Paths;
import com.aspose.note.CssSavingArgs;
import com.aspose.note.Document;
import com.aspose.note.FontFaceType;
import com.aspose.note.FontSavingArgs;
import com.aspose.note.HtmlSaveOptions;
import com.aspose.note.ICssSavingCallback;
import com.aspose.note.IFontSavingCallback;
import com.aspose.note.IImageSavingCallback;
import com.aspose.note.ImageSavingArgs;
import com.aspose.note.ResourceExportType;
```

## चरण 1: एक OneNote दस्तावेज़ ऑब्जेक्ट बनाएँ

```java
Document document = new Document("Path_to_your_sample_one_file");
```

 यह कोड आरंभ करता है a`Document` एक नमूना OneNote फ़ाइल लोड करके ऑब्जेक्ट करें।

## चरण 2: मेमोरी स्ट्रीम में HTML के रूप में सहेजें

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

यहां, हम HTML सेव विकल्प सेट करते हैं और दस्तावेज़ को मेमोरी स्ट्रीम में सेव करते हैं।

## चरण 3: अलग-अलग फ़ाइलों में संसाधनों के साथ HTML के रूप में सहेजें

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

यह चरण दस्तावेज़ को HTML के रूप में CSS, फ़ॉन्ट और छवियों जैसे संसाधनों के साथ अलग-अलग फ़ाइलों में सहेजता है।

## चरण 4: संसाधनों को बचाने के लिए कॉलबैक के साथ मेमोरी स्ट्रीम में HTML के रूप में सहेजें

```java
Document document = new Document("Path_to_your_sample_one_file");

UserSavingCallbacks savingCallbacks = new UserSavingCallbacks();
savingCallbacks.setRootFolder("documentFolder");
savingCallbacks.setCssFolder("css");
savingCallbacks.setKeepCssStreamOpened(true);
savingCallbacks.setImagesFolder("images");
savingCallbacks.setFontsFolder("fonts");

HtmlSaveOptions options = new HtmlSaveOptions();
options.setFontFaceTypes(FontFaceType.Ttf);
options.setCssSavingCallback(savingCallbacks);
options.setImageSavingCallback(savingCallbacks);
options.setFontSavingCallback(savingCallbacks);
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);

File dir = new File(savingCallbacks.getRootFolder());
if (!dir.exists()) {
    dir.mkdir();
}

document.save(Paths.get(savingCallbacks.getRootFolder(), "document.html").toString(), options);
```

यहां, हम संसाधन बचत को संभालने के लिए कॉलबैक का उपयोग करके दस्तावेज़ को HTML के रूप में मेमोरी स्ट्रीम में सहेजते हैं।

## निष्कर्ष

बधाई हो! आपने सीखा है कि जावा के लिए Aspose.Note का उपयोग करके OneNote दस्तावेज़ कैसे बनाएं और इसे HTML प्रारूप में कैसे सहेजें। अब आप OneNote फ़ाइलों के साथ प्रोग्रामेटिक रूप से काम करने के लिए इस कार्यक्षमता को अपने जावा अनुप्रयोगों में एकीकृत कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं एक ही बार में एकाधिक OneNote दस्तावेज़ों को HTML में परिवर्तित कर सकता हूँ?

A1: हाँ, आप एकाधिक दस्तावेज़ों को लूप कर सकते हैं और बचत प्रक्रिया को पुनरावृत्तीय रूप से लागू कर सकते हैं।

### Q2: क्या Java के लिए Aspose.Note HTML के अलावा अन्य आउटपुट स्वरूपों का समर्थन करता है?

A2: हाँ, Java के लिए Aspose.Note PDF, DOCX और छवि स्वरूपों सहित विभिन्न आउटपुट स्वरूपों का समर्थन करता है।

### Q3: क्या Java के लिए Aspose.Note का कोई परीक्षण संस्करण उपलब्ध है?

उ3: हां, आप यहां से नि:शुल्क परीक्षण संस्करण डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/).

### Q4: मुझे जावा के लिए Aspose.Note के लिए समर्थन कहां मिल सकता है?

 A4: आप से समर्थन प्राप्त कर सकते हैं[Aspose.नोट फोरम](https://forum.aspose.com/c/note/28).

### Q5: मैं जावा के लिए Aspose.Note का लाइसेंस कैसे खरीद सकता हूं?

 A5: आप यहां से लाइसेंस खरीद सकते हैं[Aspose वेबसाइट](https://purchase.aspose.com/buy).