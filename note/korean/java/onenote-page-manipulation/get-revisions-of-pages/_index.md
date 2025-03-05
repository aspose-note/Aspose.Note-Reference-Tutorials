---
title: OneNote에서 페이지 개정판 가져오기 - Aspose.Note
linktitle: OneNote에서 페이지 개정판 가져오기 - Aspose.Note
second_title: Aspose.Note 자바 API
description: Aspose.Note Java를 사용하여 OneNote 문서 내의 페이지 개정판을 검색하는 방법을 알아보세요. 효율적인 문서 관리를 위해 이를 Java 앱에 통합하세요.
type: docs
weight: 15
url: /ko/java/onenote-page-manipulation/get-revisions-of-pages/
---
## 소개

이 튜토리얼에서는 Java 애플리케이션에서 Microsoft OneNote 파일을 원활하게 사용할 수 있게 해주는 강력한 라이브러리인 Aspose.Note for Java의 기능을 자세히 살펴보겠습니다. 특히 OneNote 문서 내에서 페이지 수정본을 검색하는 방법에 중점을 둘 것입니다. 이 가이드를 마치면 마지막 수정 시간, 생성 시간, 제목, 수준, 작성자 등의 세부 정보를 포함하여 페이지 개정판을 효율적으로 추출하는 지식을 갖추게 됩니다.

## 전제조건

이 튜토리얼을 시작하기 전에 다음 전제 조건이 설정되어 있는지 확인하세요.

### JDK(Java 개발 키트)가 설치되었습니다.

시스템에 Java Development Kit가 설치되어 있는지 확인하십시오. Oracle 웹 사이트에서 다운로드하여 설치할 수 있으며 Unix 기반 시스템을 사용하는 경우 패키지 관리자를 사용할 수 있습니다.

### Java 라이브러리용 Aspose.Note

 웹사이트에서 Aspose.Note for Java 라이브러리를 다운로드하여 설치하세요. 다운로드 링크를 찾을 수 있습니다[여기](https://releases.aspose.com/note/java/) . 설명서에 제공된 설치 지침을 따르십시오.[여기](https://reference.aspose.com/note/java/).

## 패키지 가져오기

시작하려면 필요한 패키지를 Java 프로젝트로 가져옵니다. 이 패키지를 사용하면 Aspose.Note for Java가 제공하는 기능을 활용할 수 있습니다.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

이제 제공된 예제 코드를 여러 단계로 나누어 각 구성 요소와 해당 기능을 이해해 보겠습니다.

## 1단계: 문서 디렉터리 설정

OneNote 문서가 있는 디렉터리를 정의합니다.

```java
String dataDir = "Your Document Directory";
```

## 2단계: 문서 로드

OneNote 문서를 Aspose.Note에 로드합니다.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## 3단계: 첫 페이지 가져오기

문서의 첫 번째 페이지를 검색합니다.

```java
Page firstPage = doc.getFirstChild();
```

## 4단계: 페이지 개정판 가져오기

페이지의 개정 내역을 가져옵니다.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## 5단계: 페이지 개정 트래버스

페이지 개정 목록을 반복하고 관련 정보를 검색합니다.

```java
for (Page pageRevision : revisions) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

## 결론

이 튜토리얼에서는 Java용 Aspose.Note를 사용하여 OneNote 문서 내의 페이지 개정판을 검색하는 방법을 살펴보았습니다. 단계별 가이드를 따르고 제공된 예제 코드를 활용하면 이 기능을 Java 응용 프로그램에 쉽게 통합하여 OneNote 파일을 효율적으로 관리할 수 있습니다.

## FAQ

### Q1: Java용 Aspose.Note를 사용하여 새 OneNote 문서를 만들 수 있나요?

A1: 예, Aspose.Note for Java는 OneNote 문서를 프로그래밍 방식으로 생성, 읽기 및 조작하기 위한 포괄적인 지원을 제공합니다.

### Q2: Java용 Aspose.Note는 다른 버전의 OneNote 파일과 호환됩니까?

A2: 예, Aspose.Note for Java는 다양한 버전의 Microsoft OneNote 파일을 지원하여 다양한 환경에서 호환성을 보장합니다.

### Q3: OneNote 문서를 내보낼 때 출력 형식을 사용자 지정할 수 있나요?

A3: 물론입니다. Java용 Aspose.Note는 사용자 지정 옵션을 통해 OneNote 문서를 PDF, HTML, 이미지 등 다양한 형식으로 내보낼 수 있는 유연성을 제공합니다.

### Q4: Java용 Aspose.Note를 상업적으로 사용하려면 라이선스가 필요합니까?

A4: 네, Aspose.Note for Java를 상업적으로 사용하려면 유효한 라이선스가 필요합니다. Aspose 웹사이트에서 라이선스를 얻을 수 있습니다.

### Q5: Aspose.Note for Java에 대해 문제가 발생하거나 질문이 있는 경우 어디서 도움을 받을 수 있나요?

 A5: 지원 및 지원을 받으려면 Aspose.Note 포럼을 방문하세요.[여기](https://forum.aspose.com/c/note/28)에서 질문하고, 경험을 공유하고, 다른 사용자 및 전문가와 상호 작용할 수 있습니다.