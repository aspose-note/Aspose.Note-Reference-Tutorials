---
title: Aspose.Note में TIFF छवि में सहेजें
linktitle: Aspose.Note में TIFF छवि में सहेजें
second_title: Aspose.Note .NET API
description: .NET के लिए Aspose.Note का उपयोग करके विभिन्न संपीड़न विधियों के साथ OneNote दस्तावेज़ों को TIFF छवियों के रूप में सहेजना सीखें।
type: docs
weight: 27
url: /hi/net/loading-and-saving-operations/save-to-tiff-image/
---
## परिचय

इस ट्यूटोरियल में, हम यह पता लगाएंगे कि .NET के लिए Aspose.Note का उपयोग करके दस्तावेज़ों को TIFF प्रारूप में छवियों के रूप में कैसे सहेजा जाए। Aspose.Note एक शक्तिशाली API है जो डेवलपर्स को Microsoft OneNote फ़ाइलों के साथ प्रोग्रामेटिक रूप से काम करने की अनुमति देता है। OneNote दस्तावेज़ों को TIFF छवियों के रूप में सहेजना विभिन्न अनुप्रयोगों जैसे संग्रहण, साझाकरण या मुद्रण के लिए उपयोगी हो सकता है।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

1.  .NET के लिए Aspose.Note: सुनिश्चित करें कि आपने .NET के लिए Aspose.Note इंस्टॉल कर लिया है। आप इसे यहां से डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/note/net/).

2. विकास परिवेश: विज़ुअल स्टूडियो या किसी अन्य .NET IDE के साथ एक विकास परिवेश स्थापित करें।

3. OneNote दस्तावेज़: एक नमूना OneNote दस्तावेज़ तैयार करें जिसे आप TIFF प्रारूप में कनवर्ट करना चाहते हैं।

## नामस्थान आयात करें

सबसे पहले, आपको अपने प्रोजेक्ट में आवश्यक नामस्थान आयात करने की आवश्यकता है:

```csharp
using System;
using System.IO;

using Aspose.Note.Saving;

```

## चरण 1: JPEG संपीड़न का उपयोग करके TIFF में सहेजें

गुणवत्ता बनाए रखते हुए छवियों के आकार को कम करने के लिए JPEG संपीड़न एक व्यापक रूप से उपयोग की जाने वाली विधि है। यहां बताया गया है कि आप OneNote दस्तावेज़ को JPEG संपीड़न के साथ TIFF छवि के रूप में कैसे सहेज सकते हैं:

```csharp
public static void SaveToTiffUsingJpegCompression()
{
    // दस्तावेज़ को Aspose.Note में लोड करें।
    Document oneFile = new Document("Path_to_your_OneNote_document");

    // TIFF छवि के लिए गंतव्य पथ सेट करें।
    var dst = "Destination_path_for_TIFF_image";

    // दस्तावेज़ को JPEG संपीड़न के साथ TIFF छवि के रूप में सहेजें।
    oneFile.Save(dst, new ImageSaveOptions(SaveFormat.Tiff)
    {
        TiffCompression = TiffCompression.Jpeg,
        Quality = 93 // आवश्यकतानुसार गुणवत्ता समायोजित करें
    });

    Console.WriteLine("\nOneNote document converted successfully to image in TIFF format using JPEG compression.\nFile saved at " + dst);
}
```

## चरण 2: पैकबिट्स कंप्रेशन का उपयोग करके TIFF में सहेजें

पैकबिट्स कम्प्रेशन एक सरल और कुशल कम्प्रेशन एल्गोरिदम है जिसका उपयोग आमतौर पर टीआईएफएफ छवियों में किया जाता है। यहां बताया गया है कि आप OneNote दस्तावेज़ को पैकबिट्स संपीड़न के साथ TIFF छवि के रूप में कैसे सहेज सकते हैं:

```csharp
public static void SaveToTiffUsingPackBitsCompression()
{
    // दस्तावेज़ को Aspose.Note में लोड करें।
    Document oneFile = new Document("Path_to_your_OneNote_document");

    // TIFF छवि के लिए गंतव्य पथ सेट करें।
    var dst = "Destination_path_for_TIFF_image";

    // पैकबिट्स संपीड़न के साथ दस्तावेज़ को TIFF छवि के रूप में सहेजें।
    oneFile.Save(dst, new ImageSaveOptions(SaveFormat.Tiff)
    {
        TiffCompression = TiffCompression.PackBits
    });

    Console.WriteLine("\nOneNote document converted successfully to image in TIFF format using PackBits compression.\nFile saved at " + dst);
}
```

## चरण 3: CCITT समूह 3 संपीड़न का उपयोग करके TIFF में सहेजें

CCITT समूह 3 संपीड़न, जिसे फैक्स संपीड़न के रूप में भी जाना जाता है, काले और सफेद छवियों के लिए उपयुक्त है। यहां बताया गया है कि आप CCITT समूह 3 संपीड़न के साथ OneNote दस्तावेज़ को TIFF छवि के रूप में कैसे सहेज सकते हैं:

```csharp
public static void SaveToTiffUsingCcitt3Compression()
{
    // दस्तावेज़ को Aspose.Note में लोड करें।
    Document oneFile = new Document("Path_to_your_OneNote_document");

    // TIFF छवि के लिए गंतव्य पथ सेट करें।
    var dst = "Destination_path_for_TIFF_image";

    // CCITT समूह 3 संपीड़न के साथ दस्तावेज़ को TIFF छवि के रूप में सहेजें।
    oneFile.Save(dst, new ImageSaveOptions(SaveFormat.Tiff)
    {
        ColorMode = ColorMode.BlackAndWhite,
        TiffCompression = TiffCompression.Ccitt3
    });

    Console.WriteLine("\nOneNote document converted successfully to image in TIFF format using CCITT Group 3 fax compression.\nFile saved at " + dst);
}
```

इन चरणों का पालन करके, आप .NET के लिए Aspose.Note का उपयोग करके विभिन्न संपीड़न विकल्पों के साथ अपने OneNote दस्तावेज़ों को TIFF छवियों के रूप में आसानी से सहेज सकते हैं।

## निष्कर्ष

इस ट्यूटोरियल में, हमने सीखा कि .NET के लिए Aspose.Note के साथ विभिन्न संपीड़न विधियों का उपयोग करके OneNote दस्तावेज़ों को TIFF छवियों के रूप में कैसे सहेजा जाए। चाहे आपको JPEG, पैकबिट्स, या CCITT ग्रुप 3 कम्प्रेशन की आवश्यकता हो, Aspose.Note विभिन्न आवश्यकताओं को कुशलतापूर्वक संभालने के लिए लचीलापन प्रदान करता है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं JPEG संपीड़न की गुणवत्ता को समायोजित कर सकता हूँ?

A1: हाँ, आप छवि गुणवत्ता और फ़ाइल आकार के बीच संतुलन बनाने के लिए JPEG संपीड़न के साथ सहेजते समय गुणवत्ता पैरामीटर को समायोजित कर सकते हैं।

### Q2: क्या Aspose.Note विकास के लिए विज़ुअल स्टूडियो के साथ संगत है?

A2: हाँ, Aspose.Note को .NET विकास के लिए विज़ुअल स्टूडियो में सहजता से एकीकृत किया जा सकता है।

### Q3: क्या OneNote दस्तावेज़ों के आकार पर कोई सीमाएँ हैं जिन्हें परिवर्तित किया जा सकता है?

A3: Aspose.Note महत्वपूर्ण प्रदर्शन समस्याओं के बिना बड़े OneNote दस्तावेज़ों को संभाल सकता है।

### Q4: क्या मैं एकाधिक दस्तावेज़ों के लिए रूपांतरण प्रक्रिया को स्वचालित कर सकता हूँ?

A4: हां, आप Aspose.Note API के साथ बैच प्रोसेसिंग का उपयोग करके रूपांतरण प्रक्रिया को स्वचालित कर सकते हैं।

### Q5: क्या Aspose.Note के लिए कोई परीक्षण संस्करण उपलब्ध है?

 A5: हाँ, आप Aspose.Note का निःशुल्क परीक्षण प्राप्त कर सकते हैं[यहाँ](https://releases.aspose.com/).