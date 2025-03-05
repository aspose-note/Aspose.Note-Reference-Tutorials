---
title: OneNote에서 저장 형식을 사용하여 JPEG 이미지로 저장
linktitle: OneNote에서 저장 형식을 사용하여 JPEG 이미지로 저장
second_title: Aspose.Note 자바 API
description: OneNote 문서를 JPEG 이미지로 쉽게 변환하세요! 이 Java 튜토리얼은 Aspose.Note를 사용하는 방법을 보여줍니다. 코드 예제로 변환 및 자동화하세요! #OneNote #Java #Aspose
type: docs
weight: 18
url: /ko/java/onenote-document-saving/save-to-jpeg-image-using-save-format/
---
## 소개

이 튜토리얼에서는 Aspose.Note for Java를 사용하여 문서를 JPEG 이미지 형식으로 저장하는 과정을 살펴보겠습니다. Aspose.Note는 개발자가 프로그래밍 방식으로 Microsoft OneNote 파일을 사용하여 콘텐츠 변환, 조작 및 추출과 같은 다양한 작업을 수행할 수 있도록 하는 강력한 Java API입니다.

## 전제조건

시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

1. Java 개발 환경: 시스템에 JDK(Java Development Kit)가 설치되어 있는지 확인하십시오.
2.  Aspose.Note for Java 라이브러리: Aspose.Note for Java 라이브러리를 다운로드하고 설치하세요. 다음에서 다운로드할 수 있습니다.[여기](https://releases.aspose.com/note/java/).

## 패키지 가져오기

먼저 Java 코드에 필요한 필수 패키지를 가져옵니다.

```java
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## 1단계: 문서 로드

 초기 단계는 문서를 Aspose.Note에 로드하는 것입니다. 이는 다음을 사용하여 수행할 수 있습니다.`Document` Aspose.Note에서 제공하는 클래스입니다.

```java
// 문서 디렉터리의 경로입니다.
String dataDir = "Your Document Directory";

// 문서를 Aspose.Note에 로드합니다.
Document oneFile = new Document(dataDir + "Aspose.one");
```

## 2단계: JPEG 이미지로 저장

 다음으로 출력 파일 경로를 지정하고 다음을 사용하여 문서를 JPEG 이미지 형식으로 저장합니다.`save()` 방법과 함께`SaveFormat.Jpeg` 매개변수.

```java
// 출력 파일 경로를 지정합니다.
dataDir = dataDir + "SaveToJpegImageUsingSaveFormat_out.jpg";

// 문서를 저장합니다.
oneFile.save(dataDir, SaveFormat.Jpeg);
```

## 결론

이 튜토리얼에서는 Aspose.Note for Java를 사용하여 문서를 JPEG 이미지로 저장하는 방법을 배웠습니다. 제공된 단계를 따르면 OneNote 파일을 프로그래밍 방식으로 JPEG 형식으로 원활하게 변환하여 Java 응용 프로그램의 통합 및 자동화를 위한 다양한 가능성을 활성화할 수 있습니다.

## FAQ

### Q1: Aspose.Note가 복잡한 OneNote 파일을 처리할 수 있나요?

A1: 예, Aspose.Note는 복잡한 OneNote 파일을 효율적으로 처리하여 정확한 변환 및 조작을 보장하도록 설계되었습니다.

### Q2: Aspose.Note for Java에 사용할 수 있는 평가판이 있나요?

 A2: 예, 다음 사이트에서 Java용 Aspose.Note 무료 평가판을 구할 수 있습니다.[여기](https://releases.aspose.com/).

### Q3: Java용 Aspose.Note에 대한 지원을 어떻게 받을 수 있나요?

 A3: 다음을 방문하여 Java용 Aspose.Note에 대한 지원을 받을 수 있습니다.[Aspose.Note 포럼](https://forum.aspose.com/c/note/28).

### Q4: Aspose.Note for Java의 임시 라이선스를 구입할 수 있나요?

 A4: 예, 다음에서 임시 라이센스를 구입할 수 있습니다.[여기](https://purchase.aspose.com/temporary-license/).

### Q5: Aspose.Note for Java에 대한 자세한 문서는 어디서 찾을 수 있나요?

A5: Java용 Aspose.Note에 대한 자세한 문서를 찾을 수 있습니다.[여기](https://reference.aspose.com/note/java/).