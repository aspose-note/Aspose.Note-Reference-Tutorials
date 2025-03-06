---
title: OneNote 문서를 이미지로 변환 - Java
linktitle: OneNote 문서를 이미지로 변환 - Java
second_title: Aspose.Note 자바 API
description: Java용 Aspose.Note를 사용하여 OneNote를 이미지로 변환하는 방법을 알아보세요. 간단한 단계를 따르고, 문서를 로드하고, 옵션을 초기화하고, PNG로 저장하세요.
weight: 14
url: /ko/java/onenote-document-loading/convert-to-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote 문서를 이미지로 변환 - Java

## 소개

이 튜토리얼에서는 Aspose.Note for Java를 사용하여 OneNote 문서를 이미지로 변환하는 과정을 안내합니다. 각 단계를 따라하기 쉬운 지침으로 나누어 보겠습니다.

## 전제조건

시작하기 전에 다음 사항이 있는지 확인하세요.

1. 시스템에 JDK(Java Development Kit)가 설치되어 있습니다.
2.  Java 라이브러리용 Aspose.Note. 다음에서 다운로드할 수 있습니다.[여기](https://releases.aspose.com/note/java/).

## 패키지 가져오기

먼저 Java 코드에 필요한 패키지를 가져옵니다.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

이제 제공된 예제 코드를 여러 단계로 나누어 보겠습니다.

## 1단계: 문서 디렉터리 설정

OneNote 문서가 있는 디렉터리를 정의합니다.

```java
String dataDir = "Your Document Directory";
```

 바꾸다`"Your Document Directory"` OneNote 문서의 경로를 사용하세요.

## 2단계: 문서 로드

OneNote 문서를 Aspose.Note에 로드합니다.

```java
Document oneFile = new Document(dataDir + "Sample1.one");
```

 보장하다`"Sample1.one"` OneNote 문서 파일의 이름과 일치합니다.

## 3단계: ImageSaveOptions 초기화

 초기화`ImageSaveOptions` 저장 형식을 지정하는 객체:

```java
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
```

여기서는 문서를 PNG 이미지로 저장합니다. 필요한 경우 JPEG 또는 BMP와 같은 다른 형식을 선택할 수 있습니다.

## 4단계: 문서를 이미지로 저장

로드된 문서를 이미지로 저장합니다.

```java
oneFile.save(dataDir + "ConvertToImage_out.png", options);
```

이 줄은 문서를 지정된 옵션을 사용하여 PNG 이미지로 저장합니다.

## 5단계: 인쇄 확인

파일이 저장되었는지 확인하는 메시지를 인쇄합니다.

```java
System.out.println("File saved: " + dataDir + "ConvertToImage_out.png");
```

이 줄은 성공적인 변환과 저장된 이미지 파일의 위치를 알려줍니다.

## 결론

위에 설명된 단계를 따르면 Aspose.Note for Java를 사용하여 OneNote 문서를 이미지로 쉽게 변환할 수 있습니다. 이는 Java 애플리케이션에서 문서 변환을 처리하는 간단하고 효과적인 방법입니다.

## FAQ

### Q1: 여러 OneNote 문서를 한 번에 변환할 수 있나요?

A1: 예, 문서 목록을 반복하여 각 문서에 대한 변환 작업을 수행할 수 있습니다.

### Q2: Aspose.Note는 이미지 외에 다른 출력 형식을 지원합니까?

A2: 예, Aspose.Note는 PDF, HTML, Microsoft Word 형식과 같은 다양한 출력 형식을 지원합니다.

### Q3: Aspose.Note는 모든 버전의 OneNote 파일과 호환됩니까?

A3: Aspose.Note는 다양한 버전의 Microsoft OneNote에서 생성된 OneNote 파일과의 호환성을 제공합니다.

### Q4: 출력 이미지의 해상도를 맞춤 설정할 수 있나요?

A4: 예, Aspose.Note에서 사용 가능한 옵션을 사용하여 해상도 및 기타 매개변수를 조정할 수 있습니다.

### Q5: Aspose.Note는 문서 변환을 위해 인터넷 연결이 필요합니까?

A5: 아니요, Aspose.Note는 인터넷 연결 없이 로컬로 작동합니다.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
