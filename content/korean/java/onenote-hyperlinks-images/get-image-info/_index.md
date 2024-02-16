---
title: Java를 사용하여 OneNote에서 이미지 정보 가져오기
linktitle: Java를 사용하여 OneNote에서 이미지 정보 가져오기
second_title: Aspose.Note 자바 API
description: Java의 OneNote 문서에서 이미지 정보를 추출하세요! 이미지 크기, 파일 이름 등을 확인하세요. 쉬운 단계 및 코드 예제가 포함되어 있습니다. #OneNote #Java #Aspose
type: docs
weight: 15
url: /ko/java/onenote-hyperlinks-images/get-image-info/
---
## 소개

Java 개발 영역에서는 다양한 문서 형식에서 정보를 추출하는 것이 일반적인 작업입니다. 인기 있는 메모 작성 플랫폼인 OneNote에는 텍스트와 함께 이미지가 포함되어 있는 경우가 많습니다. Java를 사용하여 OneNote 파일에서 프로그래밍 방식으로 이미지 정보를 검색하면 문서 처리 워크플로를 간소화할 수 있습니다. 이 튜토리얼에서는 Aspose.Note for Java를 사용하여 OneNote 문서에서 이미지 세부 정보를 추출하는 방법을 살펴보겠습니다.

## 전제조건

구현을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

### 1. 자바 개발 키트(JDK)

시스템에 JDK(Java Development Kit)가 설치되어 있는지 확인하십시오. 최신 JDK를 다운로드하여 설치할 수 있습니다.[오라클 웹사이트](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).

### 2. Java 라이브러리용 Aspose.Note

 프로젝트에 Java용 Aspose.Note 라이브러리를 다운로드하고 포함하세요. 도서관에서 도서관을 구할 수 있습니다.[다운로드 페이지](https://releases.aspose.com/note/java/).

### 3. 원노트 문서

이미지가 포함된 샘플 OneNote 문서를 준비합니다. 이 문서는 프로그래밍 방식으로 이미지 정보를 추출하는 데 사용됩니다.

## 패키지 가져오기

시작하려면 Aspose.Note for Java에서 필요한 패키지를 가져옵니다.

```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.Image;
```

위의 코드를 단계별 지침으로 나누어 보겠습니다.

## 1단계: 문서 디렉터리 설정

```java
String dataDir = "Your Document Directory";
```

 바꾸다`"Your Document Directory"` OneNote 문서의 경로를 사용하세요.

## 2단계: 문서 로드

```java
Document doc = new Document(dataDir + "Sample1.one");
```

Aspose.Note for Java 라이브러리를 사용하여 OneNote 문서를 로드합니다. 문서에 올바른 경로를 제공했는지 확인하세요.

## 3단계: 모든 이미지 가져오기

```java
List<Image> list = doc.getChildNodes(Image.class);
```

로드된 OneNote 문서에서 모든 이미지를 검색합니다.

## 4단계: 총 이미지 수 인쇄

```java
System.out.printf("Total Images: %s\n\n", list.size());
```

문서에서 발견된 총 이미지 수를 인쇄합니다.

## 5단계: 이미지 정보 탐색 및 인쇄

```java
for (Image image : list) {
    System.out.println("Width: " + image.getWidth());
    System.out.println("Height: " + image.getHeight());
    System.out.println("OriginalWidth: " + image.getOriginalWidth());
    System.out.println("OriginalHeight: " + image.getOriginalHeight());
    System.out.println("FileName: " + image.getFileName());
    System.out.println("LastModifiedTime: " + image.getLastModifiedTime());
    System.out.println();
}
```

이미지 목록을 반복하고 각 이미지의 너비, 높이, 원본 크기, 파일 이름 및 마지막 수정 시간과 같은 세부 정보를 인쇄합니다.

## 결론

이 튜토리얼에 설명된 단계를 따르면 Aspose.Note for Java 라이브러리의 도움으로 Java를 사용하여 OneNote 문서에서 이미지 정보를 효과적으로 검색할 수 있습니다. 이 기능을 애플리케이션에 통합하면 문서 처리와 관련된 작업을 자동화하여 효율성과 생산성을 높일 수 있습니다.

## FAQ

### Q1: Java용 Aspose.Note는 OneNote 이외의 다른 문서 형식을 처리할 수 있습니까?

A1: 예, Aspose.Note for Java는 OneNote, PDF, Microsoft Word를 포함한 다양한 문서 형식을 지원합니다.

### Q2: Aspose.Note for Java는 개인용 및 상업용 모두에 적합합니까?

A2: 네, 개인적 목적과 상업적 목적 모두로 Aspose.Note for Java를 활용할 수 있습니다.

### Q3: Aspose.Note for Java는 기술 지원을 제공합니까?

 A3: 예, Aspose 포럼을 통해 기술 지원을 받을 수 있습니다.[여기](https://forum.aspose.com/c/note/28).

### Q4: 구매하기 전에 Java용 Aspose.Note를 사용해 볼 수 있나요?

 A4: 예, 다음에서 Java용 Aspose.Note의 무료 평가판을 탐색할 수 있습니다.[Java용 Aspose.Note](https://releases.aspose.com/note/java/).

### Q5: Aspose.Note for Java의 임시 라이선스를 어떻게 얻을 수 있나요?
 
 A5: 다음에서 임시 라이센스를 취득할 수 있습니다.[임시면허/](https://purchase.aspose.com/temporary-license/).