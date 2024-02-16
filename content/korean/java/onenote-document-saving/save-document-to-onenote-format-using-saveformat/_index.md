---
title: SaveFormat을 사용하여 OneNote에 문서 저장 - Aspose.Note
linktitle: SaveFormat을 사용하여 OneNote에 문서 저장 - Aspose.Note
second_title: Aspose.Note 자바 API
description: Java용 Aspose.Note를 사용하여 문서를 OneNote 형식으로 저장하는 방법을 알아보세요. Java 애플리케이션에 원활하게 통합하려면 이 단계별 튜토리얼을 따르십시오.
type: docs
weight: 12
url: /ko/java/onenote-document-saving/save-document-to-onenote-format-using-saveformat/
---
## 소개

Aspose.Note for Java는 개발자가 Microsoft OneNote 파일을 프로그래밍 방식으로 작업할 수 있게 해주는 강력한 라이브러리입니다. SaveFormat을 사용하여 문서를 OneNote 형식으로 저장하는 과정은 간단합니다. 이 자습서에서는 이 작업을 수행하는 데 필요한 단계를 살펴보겠습니다.

## 전제조건

시작하기 전에 다음 사항이 있는지 확인하세요.

1. 시스템에 JDK(Java Development Kit)가 설치되어 있습니다.
2.  Java 라이브러리용 Aspose.Note가 다운로드되었습니다. 당신은 그것을 얻을 수 있습니다[여기](https://releases.aspose.com/note/java/).
3. Java 프로그래밍 언어에 대한 기본 이해.

## 패키지 가져오기

 먼저 필요한 패키지를 Java 프로젝트로 가져와야 합니다. 여기에는 다음을 가져오는 것이 포함됩니다.`com.aspose.note` Aspose.Note 기능을 사용하기 위한 패키지입니다.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.SaveFormat;
```

## 1단계: 문서 디렉토리 설정

문서가 있는 디렉터리와 출력 파일을 저장할 디렉터리를 정의합니다.

```java
String dataDir = "Your Document Directory";
```

## 2단계: 문서 로드

 다음을 사용하여 문서를 Java 애플리케이션에 로드합니다.`Document` Aspose.Note에서 제공하는 클래스입니다.

```java
Document document = new Document(dataDir + "Sample1.one");
```

## 3단계: 문서를 OneNote 형식으로 저장

로드된 문서를 다음을 사용하여 OneNote 형식으로 저장합니다.`save` 방법을 사용하고 원하는 출력 파일 형식을 다음과 같이 지정합니다.`SaveFormat.One`.

```java
document.save(dataDir + "SaveDocToOneNoteFormatUsingSaveformat_out.one", SaveFormat.One);
```

## 결론

이 튜토리얼에서는 Java용 Aspose.Note에서 SaveFormat을 사용하여 문서를 OneNote 형식으로 저장하는 방법을 배웠습니다. 이러한 간단한 단계를 따르면 이 기능을 Java 애플리케이션에 원활하게 통합할 수 있습니다.

## FAQ

### Q1: Aspose.Note for Java는 모든 버전의 Microsoft OneNote와 호환됩니까?

A1: Aspose.Note for Java는 다양한 버전의 Microsoft OneNote를 지원하여 다양한 환경에서 호환성을 보장합니다.

### Q2: 구매하기 전에 Java용 Aspose.Note를 사용해 볼 수 있나요?

 A2: 예, 다음 사이트에서 Java용 Aspose.Note 무료 평가판을 다운로드할 수 있습니다.[여기](https://releases.aspose.com/).

### Q3: Java용 Aspose.Note에 대한 문서는 어디서 찾을 수 있나요?

 A3: Java용 Aspose.Note에 대한 자세한 문서를 찾을 수 있습니다.[여기](https://reference.aspose.com/note/java/).

### Q4: Aspose.Note for Java에 대한 기술 지원은 어떻게 받을 수 있나요?

 A4: 기술 지원 및 지원을 받으려면 Aspose.Note 포럼을 방문하세요.[여기](https://forum.aspose.com/c/note/28).

### Q5: Aspose.Note for Java에 사용할 수 있는 임시 라이선스 옵션이 있나요?

 A5: 예, Aspose.Note for Java에 대한 임시 라이센스를 다음에서 얻을 수 있습니다.[여기](https://purchase.aspose.com/temporary-license/).