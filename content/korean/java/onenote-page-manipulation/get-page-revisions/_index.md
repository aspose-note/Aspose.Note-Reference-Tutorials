---
title: OneNote에서 페이지 수정본 가져오기 - Aspose.Note
linktitle: OneNote에서 페이지 수정본 가져오기 - Aspose.Note
second_title: Aspose.Note 자바 API
description: Java용 Aspose.Note를 사용하여 OneNote에서 페이지 개정판을 검색하는 방법을 알아보세요. 변경사항을 효율적으로 추적하려면 단계별 가이드를 따르세요.
type: docs
weight: 14
url: /ko/java/onenote-page-manipulation/get-page-revisions/
---
## 소개

OneNote는 노트를 정리하고 관리하는 강력한 도구이지만 페이지의 변경 사항과 수정 사항을 추적해야 하는 경우도 있습니다. Aspose.Note for Java를 사용하면 프로그래밍 방식으로 페이지 개정판을 쉽게 검색할 수 있습니다. 이 튜토리얼에서는 Java용 Aspose.Note를 사용하여 OneNote에서 페이지 개정판을 가져오는 과정을 안내합니다.

## 전제조건

시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

### 1. 자바 개발 키트(JDK)

시스템에 JDK(Java Development Kit)가 설치되어 있는지 확인하십시오. Oracle 웹사이트에서 JDK를 다운로드하여 설치할 수 있습니다.

### 2. Java용 Aspose.Note

다음에서 Java용 Aspose.Note를 다운로드하여 설치하세요.[다운로드 링크](https://releases.aspose.com/note/java/).

### 3. 샘플 OneNote 문서

샘플 OneNote 문서 준비(`Sample1.one`)에는 개정판을 검색하려는 페이지가 포함되어 있습니다.

## 패키지 가져오기

먼저 Aspose.Note for Java에서 필요한 패키지를 가져와야 합니다.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

이제 제공된 예제를 여러 단계로 나누어 보겠습니다.

## 1단계: 문서 디렉토리 설정

OneNote 문서가 있는 디렉터리 경로를 정의합니다.

```java
String dataDir = "Your Document Directory";
```

## 2단계: OneNote 문서 로드

 다음을 사용하여 OneNote 문서를 로드합니다.`LoadOptions` 로딩 기록을 활성화합니다.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

## 3단계: 첫 페이지 가져오기

로드된 문서에서 첫 번째 페이지를 검색합니다.

```java
Page firstPage = document.getFirstChild();
```

## 4단계: 페이지 개정을 통해 반복

각 페이지 개정판을 반복하고 마지막 수정 시간, 생성 시간, 제목, 수준 및 작성자와 같은 관련 정보를 검색합니다.

```java
for (Page pageRevision : document.getPageHistory(firstPage)) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

## 결론

이 튜토리얼에서는 Java용 Aspose.Note를 사용하여 OneNote에서 페이지 개정판을 검색하는 방법을 배웠습니다. 다음 단계를 수행하면 OneNote 페이지의 변경 내용을 프로그래밍 방식으로 효율적으로 추적할 수 있습니다.

## FAQ

### Q1: Java용 Aspose.Note를 사용하여 페이지 개정판을 수정할 수 있습니까?

A1: 아니요, Java용 Aspose.Note는 현재 페이지 개정판 검색을 지원하지만 수정은 지원하지 않습니다.

### Q2: Java용 Aspose.Note는 다른 버전의 OneNote 문서와 호환됩니까?

A2: 예, Aspose.Note for Java는 다양한 버전의 OneNote 문서를 지원하므로 다양한 파일 형식으로 원활하게 작업할 수 있습니다.

### Q3: Aspose.Note for Java를 사용하려면 라이선스가 필요합니까?

A3: 네, 상용 프로젝트에서 Aspose.Note for Java를 사용하려면 라이선스를 구입해야 합니다. 그러나 평가 목적으로 임시 라이센스를 얻을 수도 있습니다.

### Q4: Aspose.Note for Java를 사용하는 동안 문제가 발생하면 지원을 요청할 수 있나요?

 A4: 예, Aspose.Note 포럼에서 지원을 요청할 수 있습니다.[여기](https://forum.aspose.com/c/note/28).

### Q5: Aspose.Note for Java에 대한 무료 평가판이 있습니까?

 A5: 예, 다음 사이트에서 Aspose.Note for Java 무료 평가판에 액세스할 수 있습니다.[웹사이트](https://releases.aspose.com/).