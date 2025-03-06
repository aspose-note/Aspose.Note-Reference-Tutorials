---
title: OneNote 문서 만들기 및 HTML에 저장 - Java
linktitle: OneNote 문서 만들기 및 HTML에 저장 - Java
second_title: Aspose.Note 자바 API
description: Java용 Aspose.Note를 사용하여 OneNote 문서를 HTML로 만들고 저장하는 방법을 알아보세요. 프로그래밍 방식의 OneNote 파일 처리를 위해 Java 애플리케이션에 통합합니다.

weight: 18
url: /ko/java/onenote-document-loading/create-onenote-save-to-html/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote 문서 만들기 및 HTML에 저장 - Java

## 소개

Aspose.Note for Java는 개발자가 Microsoft OneNote 파일을 프로그래밍 방식으로 작업할 수 있게 해주는 강력한 라이브러리입니다. 이 튜토리얼에서는 OneNote 문서를 만들고 Aspose.Note for Java를 사용하여 HTML 형식으로 저장하는 방법을 살펴보겠습니다.

## 전제조건

시작하기 전에 다음 사항이 있는지 확인하세요.

1. 시스템에 JDK(Java Development Kit)가 설치되어 있습니다.
2.  Java 라이브러리용 Aspose.Note. 다음에서 다운로드할 수 있습니다.[여기](https://releases.aspose.com/note/java/).
3. Java 프로그래밍에 대한 기본 지식.

## 패키지 가져오기

먼저 필요한 패키지를 Java 프로젝트로 가져옵니다.

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

## 1단계: OneNote 문서 개체 만들기

```java
Document document = new Document("Path_to_your_sample_one_file");
```

 이 코드는`Document` 샘플 OneNote 파일을 로드하여 개체를 만듭니다.

## 2단계: 메모리 스트림에 HTML로 저장

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

여기서는 HTML 저장 옵션을 설정하고 문서를 메모리 스트림에 저장합니다.

## 3단계: 별도의 파일에 리소스를 포함하여 HTML로 저장

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

이 단계에서는 문서를 CSS, 글꼴, 이미지와 같은 리소스가 포함된 HTML로 별도의 파일로 저장합니다.

## 4단계: 리소스를 저장하기 위한 콜백을 사용하여 메모리 스트림에 HTML로 저장

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

여기서는 리소스 절약을 처리하기 위해 콜백을 사용하여 문서를 메모리 스트림에 HTML로 저장합니다.

## 결론

축하해요! OneNote 문서를 만들고 Java용 Aspose.Note를 사용하여 HTML 형식으로 저장하는 방법을 배웠습니다. 이제 이 기능을 Java 응용 프로그램에 통합하여 프로그래밍 방식으로 OneNote 파일을 작업할 수 있습니다.

## FAQ

### Q1: 여러 OneNote 문서를 한 번에 HTML로 변환할 수 있나요?

A1: 예, 여러 문서를 반복하여 저장 프로세스를 반복적으로 적용할 수 있습니다.

### Q2: Java용 Aspose.Note는 HTML 외에 다른 출력 형식을 지원합니까?

A2: 예, Aspose.Note for Java는 PDF, DOCX 및 이미지 형식을 포함한 다양한 출력 형식을 지원합니다.

### Q3: Aspose.Note for Java에 사용할 수 있는 평가판이 있나요?

A3: 예, 다음에서 무료 평가판을 다운로드할 수 있습니다.[여기](https://releases.aspose.com/).

### Q4: Java용 Aspose.Note에 대한 지원은 어디서 받을 수 있나요?

 A4: 다음으로부터 지원을 받을 수 있습니다.[Aspose.Note 포럼](https://forum.aspose.com/c/note/28).

### Q5: Aspose.Note for Java 라이선스는 어떻게 구매할 수 있나요?

 A5: 다음에서 라이센스를 구입할 수 있습니다.[Aspose 웹사이트](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
