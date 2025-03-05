---
title: OneNote에서 저장 옵션 지정 - Aspose.Note
linktitle: OneNote에서 저장 옵션 지정 - Aspose.Note
second_title: Aspose.Note 자바 API
description: Java용 Aspose.Note를 사용하여 OneNote에서 저장 옵션을 지정하는 방법을 알아보세요. 페이지 색인, 개수, 압축 설정을 손쉽게 사용자 정의하세요.
type: docs
weight: 24
url: /ko/java/onenote-document-saving/specify-save-options/
---
## 소개

이 튜토리얼에서는 Java용 Aspose.Note를 사용하여 OneNote에서 저장 옵션을 지정하는 방법을 알아봅니다. Aspose.Note는 개발자가 OneNote 문서를 프로그래밍 방식으로 생성, 조작 및 변환할 수 있는 강력한 Java 라이브러리입니다. Aspose.Note를 사용하면 다양한 저장 옵션을 쉽게 제어하여 요구 사항에 따라 출력을 사용자 지정할 수 있습니다.

## 전제조건

시작하기 전에 다음 필수 구성 요소가 있는지 확인하세요.

1. Java 프로그래밍 언어에 대한 기본 지식.
2. 시스템에 JDK(Java Development Kit)가 설치되어 있습니다.
3.  Java 라이브러리용 Aspose.Note가 설치되었습니다. 다음에서 다운로드할 수 있습니다.[여기](https://releases.aspose.com/note/java/).

## 패키지 가져오기

시작하려면 Java 코드에 필요한 패키지를 가져옵니다.

```java
import com.aspose.note.Document;
import com.aspose.note.PdfImageCompression;
import com.aspose.note.PdfSaveOptions;
import java.io.IOException;
```

예제를 여러 단계로 나누어 보겠습니다.

## 1단계: OneNote 문서 로드

```java
// 문서 디렉터리의 경로입니다.
String dataDir = "Your Document Directory";

// 문서를 Aspose.Note에 로드합니다.
Document doc = new Document(dataDir + "Aspose.one");
```

 이 단계에서는 OneNote 문서의 경로를 지정하고 이를`Document` 물체.

## 2단계: PdfSaveOptions 개체 초기화

```java
// PdfSaveOptions 객체 초기화
PdfSaveOptions opts = new PdfSaveOptions();
```

 여기서는`PdfSaveOptions` 문서를 PDF로 저장하기 위한 옵션을 지정하는 데 사용되는 개체입니다.

## 3단계: 페이지 색인 및 개수 설정

```java
// 페이지 색인 설정
opts.setPageIndex(2);

// 페이지 수 설정
opts.setPageCount(3);
```

이 줄은 저장할 페이지의 색인과 개수를 설정합니다. 이 예에서는 인덱스 2부터 시작하여 총 3개의 페이지를 저장합니다.

## 4단계: 압축 설정 지정

```java
// 필요한 경우 압축을 지정하세요.
opts.setImageCompression(PdfImageCompression.Jpeg);
opts.setJpegQuality(90);
```

여기서는 PDF의 이미지 압축 설정을 지정합니다. 압축을 JPEG 형식으로 설정하고 JPEG 품질을 90%로 지정합니다.

## 5단계: 옵션과 함께 문서 저장

```java
dataDir = dataDir + "Document.SaveWithOptions_out.pdf";
doc.save(dataDir, opts);
```

마지막으로 지정된 옵션으로 문서를 저장합니다. 출력 PDF는 주어진 옵션을 사용하여 지정된 위치에 저장됩니다.

## 결론

이 튜토리얼에서는 Aspose.Note for Java를 사용하여 OneNote에서 저장 옵션을 지정하는 방법을 배웠습니다. 저장 옵션을 사용자 정의하면 페이지 색인, 개수, 압축 설정 등 출력 문서의 다양한 측면을 제어할 수 있습니다.

## FAQ

### Q1: Aspose.Note가 대용량 OneNote 문서를 처리할 수 있나요?

A1: 예, Aspose.Note는 대규모 OneNote 문서를 효율적으로 처리하도록 설계되었습니다.

### Q2: Aspose.Note는 최신 Java 버전과 호환됩니까?

A2: 예, Aspose.Note는 최신 Java 버전과 호환됩니다.

### Q3: Aspose.Note를 사용하여 OneNote 문서를 다른 형식으로 변환할 수 있나요?

A3: 예, Aspose.Note는 OneNote 문서를 PDF, DOCX, HTML과 같은 다양한 형식으로 변환하는 것을 지원합니다.

### Q4: Aspose.Note는 OneNote 문서의 암호화 및 암호 해독을 지원합니까?

A4: 예, Aspose.Note는 OneNote 문서의 암호화 및 암호 해독을 위한 API를 제공합니다.

### Q5: Aspose.Note는 상업용으로 적합한가요?

A5: 네, Aspose.Note는 라이선스를 구매하여 상업적 목적으로 사용할 수 있습니다.