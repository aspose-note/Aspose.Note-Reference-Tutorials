---
title: OneNote에서 현재 페이지 버전 푸시 - Aspose.Note
linktitle: OneNote에서 현재 페이지 버전 푸시 - Aspose.Note
second_title: Aspose.Note 자바 API
description: OneNote 콘텐츠를 최신 상태로 유지하세요! 페이지 기록을 업데이트하고 버전을 관리하는 방법, 단계별 가이드 및 코드가 포함되어 있습니다. #OneNote #Java #Aspose
type: docs
weight: 18
url: /ko/java/onenote-page-manipulation/push-current-page-version/
---
## 소개

이 튜토리얼에서는 Java용 Aspose.Note를 활용하여 OneNote에 현재 페이지 버전을 푸시하는 방법을 살펴보겠습니다. Aspose.Note는 개발자가 Microsoft OneNote 문서를 프로그래밍 방식으로 작업하여 OneNote 파일 생성, 조작 및 변환과 같은 다양한 작업을 수행할 수 있도록 하는 강력한 Java 라이브러리입니다.

## 전제조건

시작하기 전에 다음 필수 구성 요소가 있는지 확인하세요.
1. Java 프로그래밍 언어에 대한 기본 지식.
2. 시스템에 JDK(Java Development Kit)를 설치했습니다.
3.  Java 라이브러리용 Aspose.Note. 다음에서 다운로드할 수 있습니다.[여기](https://releases.aspose.com/note/java/).
4. 작업할 샘플 OneNote 문서입니다.

## 패키지 가져오기

먼저 Aspose.Note 기능을 사용하려면 Java 프로젝트에 필요한 패키지를 가져와야 합니다.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## 1단계: OneNote 문서 로드

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
```

 여기,`dataDir` OneNote 문서가 있는 디렉터리를 가리켜야 합니다. 바꾸다`"Sample1.one"` OneNote 파일 이름으로.

## 2단계: 현재 페이지 및 해당 기록 가져오기

```java
Page page = document.getFirstChild();
PageHistory pageHistory = document.getPageHistory(page);
```

 다음을 사용하여 문서의 첫 번째 페이지를 검색합니다.`getFirstChild()` 그런 다음 다음을 사용하여 기록을 얻습니다.`getPageHistory()`.

## 3단계: 현재 페이지 버전 푸시

```java
pageHistory.addItem(page.deepClone());
```

여기에서는 페이지를 복제하고 새 항목으로 추가하여 페이지의 현재 버전을 기록에 추가합니다.

## 4단계: 문서 저장

```java
document.save(dataDir + "PushCurrentPageVersion_out.one");
```

마지막으로 업데이트된 페이지 기록과 함께 수정된 문서를 저장합니다.

## 결론

이 자습서에서는 Java용 Aspose.Note를 사용하여 OneNote에서 현재 페이지 버전을 푸시하는 방법을 배웠습니다. 다음 단계를 수행하면 OneNote 문서의 버전 관리를 프로그래밍 방식으로 효과적으로 관리할 수 있습니다.

## FAQ

### Q1: 암호화된 OneNote 파일을 작업하기 위해 Java용 Aspose.Note를 사용할 수 있나요?

A1: 예, Java용 Aspose.Note는 암호화된 OneNote 파일과 암호화되지 않은 OneNote 파일 작업을 모두 지원합니다.

### Q2: Java용 Aspose.Note는 최신 버전의 OneNote와 호환됩니까?

A2: Aspose.Note for Java는 최신 버전의 OneNote 문서와의 호환성을 유지하기 위해 노력하고 있습니다.

### Q3: Java용 Aspose.Note를 사용하여 OneNote 문서 내의 텍스트와 이미지를 조작할 수 있습니까?

A3: 물론입니다. Aspose.Note for Java는 OneNote 파일 내의 텍스트, 이미지 및 기타 요소를 조작하기 위한 광범위한 기능을 제공합니다.

### Q4: Java용 Aspose.Note는 OneNote 파일을 다른 형식으로 변환하는 것을 지원합니까?

A4: 예, Java용 Aspose.Note는 OneNote 파일을 PDF, HTML, 이미지 형식과 같은 다양한 형식으로 변환하는 것을 지원합니다.

### Q5: 문제가 발생하면 Java용 Aspose.Note에 대한 지원을 어디서 받을 수 있나요?

 A5: 다음을 방문할 수 있습니다.[Aspose.Note 포럼](https://forum.aspose.com/c/note/28) 커뮤니티에서 도움을 구하거나 Aspose 지원팀에 직접 문의하세요.