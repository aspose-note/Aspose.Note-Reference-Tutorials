---
title: Java를 사용하여 OneNote 문서에서 이미지 추출
linktitle: Java를 사용하여 OneNote 문서에서 이미지 추출
second_title: Aspose.Note 자바 API
description: Aspose.Note 라이브러리와 함께 Java를 사용하여 OneNote 문서에서 이미지를 추출하는 방법을 알아보세요. 원활한 이미지 추출을 위한 단계별 가이드를 따르세요.
type: docs
weight: 14
url: /ko/java/onenote-hyperlinks-images/extract-images/
---
## 소개

이 튜토리얼에서는 Aspose.Note 라이브러리의 도움으로 Java를 사용하여 OneNote 문서에서 이미지를 추출하는 과정을 안내합니다.

## 전제조건

시작하기 전에 다음 사항이 있는지 확인하세요.

1.  JDK(Java Development Kit): 시스템에 Java가 설치되어 있는지 확인하세요. 에서 다운로드하여 설치할 수 있습니다.[웹사이트](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).

2.  Aspose.Note 라이브러리: Aspose.Note 라이브러리를 다운로드하여 Java 프로젝트에 포함시킵니다. 에서 받으실 수 있습니다.[다운로드 링크](https://releases.aspose.com/note/java/).

## 패키지 가져오기

시작하려면 필요한 패키지를 가져옵니다.

```java
import java.io.IOException;
import java.nio.file.Files;
import java.nio.file.Paths;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.Image;
```

## 1단계: 문서 로드

먼저 Aspose.Note를 사용하여 OneNote 문서를 로드합니다.

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```

## 2단계: 모든 이미지 가져오기

다음으로 문서에서 모든 이미지를 검색합니다.

```java
List<Image> list = doc.getChildNodes(Image.class);
System.out.printf("Total Images: %s\n\n", list.size());
```

## 3단계: 이미지 추출

이미지 목록을 반복하고 각 이미지를 파일에 저장합니다.

```java
for (int i = 0; i < list.size(); i++) {
    Image image = list.get(i);
    String outputFile = "ExtractImages_out" + i + "_" + image.getFileName();
    byte[] buffer = image.getBytes();
    Files.write(Paths.get(dataDir + outputFile), buffer);
    System.out.printf("File saved: %s\n", dataDir);
}
```

## 결론

Aspose.Note 라이브러리를 사용하면 Java를 사용하여 OneNote 문서에서 이미지를 원활하게 추출할 수 있습니다. 이 튜토리얼에 설명된 단계를 따르면 추가 처리 또는 분석을 위해 문서에서 이미지를 쉽게 검색할 수 있습니다.

## FAQ

### Q1: 암호로 보호된 OneNote 문서에서 이미지를 추출할 수 있나요?

A1: 예, Aspose.Note는 비밀번호로 보호된 문서에서도 이미지 추출을 지원합니다.

### Q2: Aspose.Note는 다른 버전의 Java와 호환됩니까?

A2: Aspose.Note는 다양한 버전의 Java와 호환되므로 개발자에게 유연성을 보장합니다.

### Q3: 단일 실행으로 여러 OneNote 문서에서 이미지를 추출할 수 있나요?

A3: 물론 Aspose.Note를 사용하여 여러 문서를 반복하고 각 문서에서 이미지를 추출할 수 있습니다.

### Q4: OneNote 문서에 크기 제한이 있나요?

A4: Aspose.Note는 다양한 크기의 문서를 효율적으로 처리하므로 이미지 추출을 위한 문서 크기에 제한이 없습니다.

### Q5: Aspose.Note는 이미지 이외의 다른 유형의 콘텐츠 추출을 지원합니까?

A5: 예, 이미지 외에도 Aspose.Note를 사용하면 OneNote 문서에서 텍스트, 첨부 파일 및 기타 콘텐츠 유형을 추출할 수 있습니다.