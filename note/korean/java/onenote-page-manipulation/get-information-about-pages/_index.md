---
title: OneNote에서 페이지에 대한 정보 가져오기 - Aspose.Note
linktitle: OneNote에서 페이지에 대한 정보 가져오기 - Aspose.Note
second_title: Aspose.Note 자바 API
description: OneNote 문서에서 페이지 비밀을 찾아보세요! Aspose.Note를 사용하여 개정판, 생성 시간 등을 추출하세요. 단계별 가이드 및 코드가 포함되어 있습니다! #OneNote #Java #Aspose
type: docs
weight: 12
url: /ko/java/onenote-page-manipulation/get-information-about-pages/
---
## 소개

이 튜토리얼에서는 Aspose.Note for Java를 사용하여 OneNote에서 페이지에 대한 정보를 추출하는 과정을 안내합니다. Aspose.Note는 Microsoft OneNote 문서를 프로그래밍 방식으로 작업할 수 있는 강력한 API입니다. 페이지 개정판, 생성 시간, 제목 또는 작성자에 액세스해야 하는 경우 Aspose.Note는 직관적인 인터페이스로 작업을 단순화합니다.

## 전제조건

시작하기 전에 다음 사항이 있는지 확인하세요.

1. JDK(Java Development Kit): 시스템에 JDK가 설치되어 있는지 확인하세요.
2.  Aspose.Note for Java: Aspose.Note for Java 라이브러리를 다운로드하고 설치하세요. 에서 받으실 수 있습니다.[웹사이트](https://purchase.aspose.com/buy).
3. 샘플 OneNote 문서: 정보를 검색하는 데 사용할 샘플 OneNote 문서를 준비합니다.

## 패키지 가져오기

먼저 Java 프로젝트에서 Aspose.Note를 사용하는 데 필요한 패키지를 가져와야 합니다.

```java
import java.io.IOException;
import java.util.List;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## 1단계: OneNote 문서 로드

Aspose.Note를 사용하여 OneNote 문서를 로드하는 것으로 시작하세요.

```java
String dataDir = "Your Document Directory";
// Aspose.Note에 문서를 로드합니다.
LoadOptions options = new LoadOptions();
Document doc = new Document(dataDir + "Sample1.one", options);
```

 바꾸다`"Your Document Directory"` OneNote 문서의 경로를 사용하세요.

## 2단계: 페이지 정보 검색

다음으로 OneNote 문서의 페이지에 대한 정보를 검색합니다.

```java
// 페이지 개정판 가져오기
List<Page> pages = doc.getChildNodes(Page.class);

// 페이지 목록 탐색
for (Page pageRevision : pages) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
}
```

이 코드 조각은 문서의 각 페이지를 반복하고 각 페이지의 마지막 수정 시간, 생성 시간, 제목, 수준 및 작성자와 같은 정보를 인쇄합니다.

## 결론

이 자습서에서는 Java용 Aspose.Note를 사용하여 OneNote의 페이지에 대한 정보를 검색하는 방법을 배웠습니다. 위에 설명된 단계를 따르면 Aspose.Note를 Java 애플리케이션에 원활하게 통합하여 OneNote 문서에서 중요한 데이터를 추출할 수 있습니다.

## FAQ

### Q1: OneNote 문서를 편집하기 위해 Java용 Aspose.Note를 사용할 수 있습니까?

A1: 예, Aspose.Note는 OneNote 문서를 프로그래밍 방식으로 편집하고 조작하기 위한 포괄적인 기능 세트를 제공합니다.

### Q2: Aspose.Note는 모든 버전의 OneNote와 호환됩니까?

A2: Aspose.Note는 다양한 버전의 OneNote를 지원하여 다양한 환경에서의 호환성을 보장합니다.

### Q3: Aspose.Note를 사용하여 OneNote 문서를 다른 형식으로 변환할 수 있나요?

A3: 물론입니다. Aspose.Note를 사용하면 OneNote 문서를 PDF, HTML, 이미지 등의 형식으로 쉽게 변환할 수 있습니다.

### Q4: Aspose.Note는 개발자에게 기술 지원을 제공합니까?

A4: 예, Aspose는 Aspose.Note를 사용하는 동안 개발자가 직면하는 모든 문제를 지원하기 위해 전담 기술 지원을 제공합니다.

### Q5: Aspose.Note for Java에 사용할 수 있는 평가판이 있나요?

 A5: 예, 다음 사이트에서 Java용 Aspose.Note 무료 평가판을 다운로드할 수 있습니다.[여기](https://releases.aspose.com/).