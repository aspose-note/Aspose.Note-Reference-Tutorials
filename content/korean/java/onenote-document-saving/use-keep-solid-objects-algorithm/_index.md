---
title: OneNote에서 솔리드 개체 유지 알고리즘 사용 - Aspose.Note
linktitle: OneNote에서 솔리드 개체 유지 알고리즘 사용 - Aspose.Note
second_title: Aspose.Note 자바 API
description: Java에서 솔리드 개체 유지 알고리즘을 사용하여 PDF로 변환할 때 Aspose.Note 문서에서 솔리드 개체를 보존하는 방법을 알아보세요.
type: docs
weight: 25
url: /ko/java/onenote-document-saving/use-keep-solid-objects-algorithm/
---
## 소개

이 튜토리얼에서는 Java용 Aspose.Note에서 Keep Solid Objects 알고리즘을 활용하는 방법을 살펴보겠습니다. 이 알고리즘은 문서를 PDF 형식으로 변환할 때 문서 내의 솔리드 개체의 무결성을 유지하는 데 매우 중요합니다. 우리는 프로세스를 단계별로 분석하여 각 단계의 명확성과 이해를 보장합니다.

## 전제조건

시작하기 전에 다음 사항이 있는지 확인하세요.

1. 시스템에 JDK(Java Development Kit)가 설치되어 있습니다.
2.  Java 라이브러리용 Aspose.Note. 다음에서 다운로드할 수 있습니다.[여기](https://releases.aspose.com/note/java/).

## 패키지 가져오기

먼저 필요한 패키지를 가져오겠습니다.

```java
import java.io.IOException;
import com.aspose.note.AlwaysSplitObjectsAlgorithm;
import com.aspose.note.Document;
import com.aspose.note.KeepPartAndCloneSolidObjectToNextPageAlgorithm;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.PdfSaveOptions;
```

## 1단계: 문서 로드

다음 코드 조각을 사용하여 문서를 Aspose.Note에 로드합니다.

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Aspose.one");
```

## 2단계: PDF 저장 옵션 구성

PdfSaveOptions를 정의하고 PageSplittingAlgorithm을 KeepSolidObjectsAlgorithm으로 설정합니다.

```java
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
pdfSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm());
```

## 3단계: 높이 제한 조정(선택 사항)

필요한 경우 복제된 부품의 높이 제한을 조정할 수 있습니다.

```java
float heightLimitOfClonedPart = 500;
pdfSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm(heightLimitOfClonedPart));
```

## 4단계: 문서 저장

마지막으로 지정된 PDF 저장 옵션을 사용하여 문서를 저장합니다.

```java
String outputDir = "Your Output Directory";
String outputFile = outputDir + "UsingKeepSolidObjectsAlgorithm_out.pdf";
doc.save(outputFile);
```

## 결론

이 튜토리얼에서는 Java용 Aspose.Note에서 Keep Solid Objects 알고리즘을 활용하는 방법을 배웠습니다. 이 알고리즘은 문서를 PDF 형식으로 변환할 때 문서 내의 솔리드 개체를 보존하여 문서 무결성을 유지합니다.

## FAQ

### Q1: 복제된 부품의 높이 제한을 조정할 수 있나요?

 A1: 예. 요구 사항에 따라 복제된 부품의 높이 제한을 조정할 수 있습니다.`heightLimitOfClonedPart` 매개변수.

### Q2: 추가 문서는 어디서 찾을 수 있나요?

 A2: Java용 Aspose.Note에 대한 자세한 문서를 찾을 수 있습니다.[여기](https://reference.aspose.com/note/java/).

### Q3: 무료 평가판이 제공됩니까?

 A3: 예, Aspose.Note for Java 무료 평가판을 받을 수 있습니다.[여기](https://releases.aspose.com/).

### Q4: 문제가 발생하면 어떻게 지원을 받을 수 있나요?

 A4: Aspose 커뮤니티에서 지원을 받을 수 있습니다[여기](https://forum.aspose.com/c/note/28).

### Q5: 라이센스는 어디서 구매할 수 있나요?

 A5: Aspose.Note for Java 라이선스를 구매할 수 있습니다.[여기](https://purchase.aspose.com/buy).
