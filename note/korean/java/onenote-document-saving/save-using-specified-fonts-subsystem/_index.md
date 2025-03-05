---
title: OneNote에서 지정된 글꼴 하위 시스템을 사용하여 저장
linktitle: OneNote에서 지정된 글꼴 하위 시스템을 사용하여 저장
second_title: Aspose.Note 자바 API
description: Aspose.Note를 사용하여 Java에서 지정된 글꼴 하위 시스템을 사용하여 OneNote 문서를 저장하는 방법을 알아보세요. 플랫폼 전체에서 손쉽게 일관된 글꼴 표현을 보장합니다.
type: docs
weight: 22
url: /ko/java/onenote-document-saving/save-using-specified-fonts-subsystem/
---
## 소개

Aspose.Note for Java는 OneNote 문서 작업을 위한 강력한 기능을 제공합니다. 이러한 문서 작업 시 일반적인 요구 사항 중 하나는 특히 문서를 PDF와 같은 다른 형식으로 내보내거나 저장하는 경우 글꼴이 제대로 유지되는지 확인하는 것입니다. 이 튜토리얼은 글꼴 하위 시스템을 지정하면서 OneNote 문서를 저장하는 과정을 안내하여 다양한 플랫폼에서 텍스트를 일관되고 정확하게 표현하도록 합니다.

## 전제조건

튜토리얼을 시작하기 전에 다음 전제 조건이 설정되어 있는지 확인하세요.

### 1. 자바 개발 키트(JDK)

 시스템에 JDK(Java Development Kit)가 설치되어 있는지 확인하십시오. 다음에서 다운로드할 수 있습니다.[여기](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html) 아직 하지 않았다면.

### 2. Java 라이브러리용 Aspose.Note

 Java 라이브러리용 Aspose.Note를 다운로드하고 설정하세요. 다음에서 다운로드할 수 있습니다.[웹사이트](https://releases.aspose.com/note/java/).

## 패키지 가져오기

Java 프로젝트에서 필요한 패키지를 가져와야 합니다.

```java
import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
import com.aspose.note.fonts.DocumentFontsSubsystem;
import java.io.FileInputStream;
import java.io.IOException;
import java.io.InputStream;
import java.nio.file.Paths;
```

이제 프로세스를 더 잘 이해하기 위해 각 예를 여러 단계로 나누어 보겠습니다.

## 1단계: 기본 글꼴 이름으로 문서 글꼴 하위 시스템을 사용하여 저장

이 단계에서는 지정된 기본 글꼴 이름을 사용하여 문서를 PDF 형식으로 저장하는 방법을 보여줍니다.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName() throws IOException
{
    // 문서를 Aspose.Note에 로드합니다.
    Document oneFile = new Document("missing-font.one");

    // 기본 글꼴을 지정합니다.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFont("Times New Roman"));

    // 문서를 PDF로 저장합니다.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf", options);
}
```

이 단계에서는 다음을 수행합니다.
- OneNote 문서는 Aspose.Note를 사용하여 로드됩니다.
- 기본 글꼴은 "Times New Roman"으로 지정됩니다.
- 문서는 지정된 글꼴을 사용하여 PDF 형식으로 저장됩니다.

## 2단계: 파일의 기본 글꼴과 함께 문서 글꼴 하위 시스템을 사용하여 저장

이 단계에서는 파일에서 로드된 기본 글꼴을 사용하여 문서를 PDF 형식으로 저장하는 방법을 보여줍니다.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile() throws IOException
{
    // 문서를 Aspose.Note에 로드합니다.
    Document oneFile = new Document("missing-font.one");

    // 글꼴 파일의 경로를 지정합니다.
    String fontFile = "geo_1.ttf";

    // 파일에서 기본 글꼴을 지정합니다.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromFile(fontFile));

    // 문서를 PDF로 저장합니다.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf", options);
}
```

이 단계에서는 다음을 수행합니다.
- 글꼴 파일 "geo_1.ttf"가 로드됩니다.
- 기본 글꼴은 로드된 글꼴 파일에서 지정됩니다.
- 문서는 지정된 글꼴을 사용하여 PDF 형식으로 저장됩니다.

## 3단계: 스트림의 기본 글꼴과 함께 문서 글꼴 하위 시스템을 사용하여 저장

이 단계에서는 스트림에서 로드된 기본 글꼴을 사용하여 문서를 PDF 형식으로 저장하는 방법을 보여줍니다.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream() throws IOException
{
    // 문서를 Aspose.Note에 로드합니다.
    Document oneFile = new Document("missing-font.one");

    // 글꼴 파일의 경로를 지정합니다.
    String fontFile = "geo_1.ttf";

    // 글꼴 파일을 스트림으로 로드합니다.
    InputStream stream = new FileInputStream(fontFile);

    try
    {
        // 스트림에서 기본 글꼴을 지정합니다.
        PdfSaveOptions options = new PdfSaveOptions();
        options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromStream(stream));

        // 문서를 PDF로 저장합니다.
        oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf", options);
    }
    catch (Exception e)
    {
        stream.close();
    }
}
```

이 단계에서는 다음을 수행합니다.
- 글꼴 파일 "geo_1.ttf"가 스트림으로 로드됩니다.
- 기본 글꼴은 로드된 스트림에서 지정됩니다.
- 문서는 지정된 글꼴을 사용하여 PDF 형식으로 저장됩니다.

## 결론

이 튜토리얼에서는 Aspose.Note를 사용하여 Java에서 지정된 글꼴 하위 시스템을 사용하여 OneNote 문서를 저장하는 방법을 배웠습니다. 다음 단계를 수행하면 문서를 내보내거나 저장할 때 다양한 플랫폼에서 일관된 글꼴 표현을 보장할 수 있습니다.

## FAQ

### Q1: 문서의 각 부분에 대해 서로 다른 글꼴을 지정할 수 있습니까?

A1: 예, Aspose.Note for Java를 사용하여 문서의 각 부분에 대해 서로 다른 글꼴을 지정할 수 있습니다.

### Q2: Aspose.Note는 모든 버전의 OneNote와 호환됩니까?

A2: Aspose.Note는 다양한 버전의 OneNote를 지원하여 다양한 환경에서의 호환성을 보장합니다.

### Q3: 문서를 저장할 때 누락된 글꼴을 처리하려면 어떻게 해야 합니까?

A3: Aspose.Note는 문서 저장 중에 누락된 글꼴을 효과적으로 처리하기 위해 기본 글꼴을 지정하는 옵션을 제공합니다.

### Q4: 크기, 스타일 등 글꼴 속성을 사용자 정의할 수 있나요?

A4: 예, Aspose.Note for Java를 사용하여 크기, 스타일, 색상과 같은 글꼴 속성을 사용자 정의할 수 있습니다.

### Q5: Aspose.Note for Java에 사용할 수 있는 평가판이 있나요?

A5: 예, 웹사이트에서 Aspose.Note for Java의 무료 평가판을 받을 수 있습니다.