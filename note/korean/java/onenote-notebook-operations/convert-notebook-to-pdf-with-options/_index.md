---
title: OneNote의 옵션을 사용하여 노트북을 PDF로 변환 - Aspose.Note
linktitle: OneNote의 옵션을 사용하여 노트북을 PDF로 변환 - Aspose.Note
second_title: Aspose.Note 자바 API
description: OneNote 전자 필기장을 쉽게 사용자 지정하고 PDF로 내보낼 수 있습니다! Aspose.Note for Java는 무거운 작업을 처리합니다. 단계별 가이드가 포함되어 있습니다! #OneNote #Java #Aspose
type: docs
weight: 17
url: /ko/java/onenote-notebook-operations/convert-notebook-to-pdf-with-options/
---
## 소개

이 튜토리얼에서는 Aspose.Note for Java를 사용하여 사용자 정의 가능한 옵션을 사용하여 노트북을 PDF로 변환하는 방법을 살펴보겠습니다. Aspose.Note는 개발자가 Microsoft OneNote 문서를 프로그래밍 방식으로 조작할 수 있는 강력한 Java API입니다. 노트북을 PDF 형식으로 변환하는 것은 다양한 애플리케이션에서 일반적인 요구 사항이며 Aspose.Note를 사용하면 이 작업이 간소화되고 효율적이 됩니다.

## 전제조건

시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

1. JDK(Java Development Kit): 시스템에 JDK가 설치되어 있는지 확인하세요.
2. Java용 Aspose.Note: 다음 사이트에서 Java용 Aspose.Note를 다운로드하고 설치하세요.[다운로드 링크](https://releases.aspose.com/note/java/).
3. IDE(통합 개발 환경): Java 개발을 위해 선호하는 IDE를 선택하세요. IntelliJ IDEA, Eclipse 또는 NetBeans가 널리 사용됩니다.

## 패키지 가져오기

먼저 필요한 패키지를 Java 프로젝트로 가져와야 합니다. 이러한 패키지는 OneNote 문서 작업에 필요한 클래스와 메서드를 제공합니다.

```java
import com.aspose.note.Notebook;
import java.io.IOException;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookPdfSaveOptions;
import com.aspose.note.PdfSaveOptions;
```

## 1단계: OneNote 노트북 로드

전자 필기장을 PDF로 변환하려면 먼저 OneNote 전자 필기장을 로드해야 합니다. 노트북 파일 경로가 올바르게 지정되었는지 확인하세요.

```java
String dataDir = "Your Document Directory";
// OneNote 전자 필기장 로드
Notebook notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## 2단계: PDF 저장 옵션 지정

Aspose.Note는 PDF 출력을 사용자 정의하기 위한 다양한 옵션을 제공합니다. 페이지 분할 알고리즘, 머리글/바닥글 설정 등과 같은 옵션을 지정할 수 있습니다.

```java
// PDF 저장 옵션 지정
NotebookPdfSaveOptions notebookSaveOptions = new NotebookPdfSaveOptions();
PdfSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();
documentSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm());
```

## 3단계: 노트북을 PDF로 저장

노트북을 로드하고 저장 옵션을 지정했으면 이제 노트북을 PDF 파일로 저장할 차례입니다.

```java
dataDir = dataDir + "ExportNotebooktoPDFwithOptions_out.pdf";
// 노트북 저장
notebook.save(dataDir, notebookSaveOptions);
```

## 결론

이 튜토리얼에서는 Java용 Aspose.Note를 사용하여 OneNote 노트북을 PDF 형식으로 변환하는 방법을 살펴보았습니다. 이러한 간단한 단계를 따르면 Java 애플리케이션에서 문서 변환을 효율적으로 처리할 수 있습니다.

---

## FAQ

### Q1: PDF 출력의 모양을 사용자 정의할 수 있습니까?

A1: 예, Aspose.Note는 머리글/바닥글 설정, 페이지 분할 알고리즘 등을 포함하여 PDF 출력을 사용자 정의하기 위한 다양한 옵션을 제공합니다.

### Q2: Aspose.Note는 모든 버전의 OneNote와 호환됩니까?

A2: Aspose.Note는 Microsoft OneNote 2010 이상 버전을 지원합니다.

### Q3: Aspose.Note는 무료 평가판을 제공합니까?

 A3: 예, Aspose.Note의 무료 평가판을 다운로드할 수 있습니다.[여기](https://releases.aspose.com/).

### Q4: Aspose.Note에 대한 문서는 어디서 찾을 수 있나요?

 A4: Aspose.Note에 대한 포괄적인 문서를 찾을 수 있습니다.[여기](https://reference.aspose.com/note/java/).

### Q5: Aspose.Note에 대한 지원은 어떻게 받을 수 있나요?

 A5: 기술 지원이나 문의 사항이 있는 경우 Aspose.Note 지원 포럼을 방문하세요.[여기](https://forum.aspose.com/c/note/28).