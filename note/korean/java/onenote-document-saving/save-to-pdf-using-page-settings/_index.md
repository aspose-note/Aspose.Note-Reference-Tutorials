---
title: OneNote의 페이지 설정을 사용하여 PDF로 저장 - Aspose.Note
linktitle: OneNote의 페이지 설정을 사용하여 PDF로 저장 - Aspose.Note
second_title: Aspose.Note 자바 API
description: Aspose.Note 라이브러리를 사용하여 Java에서 OneNote 문서를 PDF로 저장하는 방법을 알아보세요. 다양한 페이지 설정에 대한 코드 예제가 포함된 단계별 가이드입니다.
weight: 19
url: /ko/java/onenote-document-saving/save-to-pdf-using-page-settings/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote의 페이지 설정을 사용하여 PDF로 저장 - Aspose.Note

## 소개

이 튜토리얼에서는 Aspose.Note for Java의 다양한 페이지 설정을 사용하여 OneNote 문서를 PDF 형식으로 저장하는 방법을 알아봅니다. Letter 페이지 설정으로 저장하는 방법과 높이 제한 없이 A4 페이지 설정으로 저장하는 두 가지 방법을 다루겠습니다.

## 전제조건

시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

1. 시스템에 JDK(Java Development Kit)가 설치되어 있습니다.
2. Java 프로젝트에 다운로드되어 포함된 Java 라이브러리용 Aspose.Note입니다.
3. Java 프로그래밍 언어에 대한 기본 이해.

## 패키지 가져오기

프로젝트에서 Aspose.Note for Java를 사용하는 데 필요한 패키지를 가져왔는지 확인하세요. 수입 명세서는 다음과 같습니다.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Letter 페이지 설정을 사용하여 PDF에 저장

### 1단계: 문서 로드

먼저 OneNote 문서를 Aspose.Note에 로드합니다.

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### 2단계: 대상 경로 정의

PDF 파일의 대상 경로를 지정합니다.

```java
String dst = "path/to/your/SaveToPdfUsingLetterPageSettings.pdf";
```

### 3단계: 문서 저장

Letter 페이지 설정으로 문서를 저장합니다.

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getLetter());
oneFile.save(dst, options);
```

## 높이 제한 없이 A4 페이지 설정을 사용하여 PDF로 저장

### 1단계: 문서 로드

마찬가지로 OneNote 문서를 Aspose.Note에 로드합니다.

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### 2단계: 대상 경로 정의

PDF 파일의 대상 경로를 지정합니다.

```java
String dst = "path/to/your/SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf";
```

### 3단계: 문서 저장

높이 제한 없이 A4 페이지 설정으로 문서를 저장합니다.

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getA4NoHeightLimit());
oneFile.save(dst, options);
```

이러한 단계를 수행하면 다양한 페이지 설정을 사용하여 OneNote 문서를 PDF에 성공적으로 저장하게 됩니다.

## 결론

이 튜토리얼에서는 Aspose.Note for Java 라이브러리를 사용하여 OneNote 문서를 PDF 형식으로 저장하는 방법을 살펴보았습니다. 단계별 가이드를 따르면 이 기능을 Java 애플리케이션에 쉽게 통합할 수 있습니다.

## FAQ

### Q1: 페이지 설정을 추가로 사용자 정의할 수 있나요?

A1: 예, Aspose.Note for Java를 사용하여 요구 사항에 따라 페이지 설정을 사용자 정의할 수 있습니다.

### Q2: Aspose.Note는 PDF 외에 다른 출력 형식을 지원합니까?

A2: 네, Aspose.Note는 이미지와 HTML을 포함한 다양한 출력 형식을 지원합니다.

### Q3: Aspose.Note는 다른 버전의 OneNote 파일과 호환됩니까?

A3: 예, Aspose.Note는 .one 및 .onetoc2를 포함한 다양한 버전의 OneNote 파일을 지원합니다.

### Q4: 한 번에 여러 OneNote 파일을 PDF로 변환할 수 있나요?

A4: 예, Aspose.Note for Java를 사용하여 여러 OneNote 파일을 일괄 처리할 수 있습니다.

### Q5: 테스트 목적으로 사용할 수 있는 평가판이 있습니까?

A5: 예, 웹사이트에서 Aspose.Note for Java의 무료 평가판을 받을 수 있습니다.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
