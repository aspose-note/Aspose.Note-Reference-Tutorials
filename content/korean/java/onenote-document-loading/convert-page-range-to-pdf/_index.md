---
title: Java를 사용하여 OneNote에서 특정 페이지 범위를 PDF로 변환
linktitle: Java를 사용하여 OneNote에서 특정 페이지 범위를 PDF로 변환
second_title: Aspose.Note 자바 API
description: Java용 Aspose.Note를 사용하여 OneNote의 특정 페이지 범위를 PDF로 원활하게 변환하는 방법을 알아보세요. 서식과 레이아웃을 손쉽게 유지하세요.
type: docs
weight: 11
url: /ko/java/onenote-document-loading/convert-page-range-to-pdf/
---
## 소개

OneNote는 노트를 정리하는 강력한 도구이지만 때로는 공유 또는 보관 목적으로 특정 페이지 범위를 PDF로 내보내야 할 수도 있습니다. 이 튜토리얼에서는 Aspose.Note for Java를 사용하여 특정 페이지 범위를 PDF로 변환하는 과정을 안내합니다.

## 전제조건

시작하기 전에 다음 필수 구성 요소가 있는지 확인하세요.

1. JDK(Java Development Kit): 시스템에 Java가 설치되어 있는지 확인하십시오.
2.  Java용 Aspose.Note: 다음에서 Java용 Aspose.Note를 다운로드하고 설치하세요.[여기](https://releases.aspose.com/note/java/).
3. 샘플 OneNote 문서: 특정 페이지 범위를 추출하려는 샘플 OneNote 문서를 준비합니다.

## 패키지 가져오기

Java 프로젝트에서 Aspose.Note를 사용하는 데 필요한 패키지를 가져옵니다.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
```

## 1단계: OneNote 문서 로드

Aspose.Note를 사용하여 OneNote 문서를 로드합니다.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one");
```

## 2단계: PDF 저장 옵션 초기화

PdfSaveOptions 객체를 초기화하고 페이지 인덱스와 개수를 지정합니다.

```java
PdfSaveOptions opts = new PdfSaveOptions();
opts.setPageIndex(2);  // 시작 페이지 색인
opts.setPageCount(3);  // 포함할 페이지 수
```

## 3단계: PDF로 저장

지정된 페이지 범위를 PDF 파일로 저장합니다.

```java
oneFile.save(dataDir + "ConvertSpecificPageRangeToPdf_out.pdf", opts);
System.out.println("File saved: " + dataDir + "ConvertSpecificPageRangeToPdf_out.pdf");
```

축하해요! Aspose.Note for Java를 사용하여 OneNote 문서의 특정 페이지 범위를 PDF로 성공적으로 변환했습니다.

## 결론

이 튜토리얼에서는 Aspose.Note for Java를 사용하여 OneNote 문서의 특정 페이지 범위를 PDF로 변환하는 방법을 배웠습니다. 이 기능은 선택적 정보 공유, 보관 복사본 생성 등 다양한 목적에 유용할 수 있습니다.

## FAQ

### Q1: 변환을 위해 연속되지 않은 여러 페이지 범위를 지정할 수 있습니까?

A1: 불행하게도 Java용 Aspose.Note는 현재 인접한 페이지 범위만 PDF로 변환하는 것을 지원합니다.

### Q2: Java용 Aspose.Note는 원본 OneNote 문서의 형식을 유지합니까?

A2: 예, Aspose.Note는 원본 OneNote 문서의 서식과 레이아웃이 생성된 PDF에 유지되도록 합니다.

### Q3: 비밀번호로 보호된 OneNote 문서를 PDF로 변환할 수 있나요?

A3: Java용 Aspose.Note는 비밀번호로 보호된 OneNote 문서를 직접 변환하는 것을 지원하지 않습니다. 변환하기 전에 비밀번호 보호를 제거해야 합니다.

### Q4: 생성된 PDF 파일의 모양을 사용자 정의할 수 있습니까?

A4: 예, Aspose.Note의 PDF 저장 옵션을 사용하여 페이지 크기, 방향, 머리글/바닥글 설정과 같은 다양한 측면을 사용자 정의할 수 있습니다.

### Q5: Java용 Aspose.Note는 여러 OneNote 문서의 일괄 변환을 지원합니까?

A5: 예, 각 문서를 반복하고 변환 프로세스를 적용하여 여러 OneNote 문서를 PDF로 일괄 변환할 수 있습니다.