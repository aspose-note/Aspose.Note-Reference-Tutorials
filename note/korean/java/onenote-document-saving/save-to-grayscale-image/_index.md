---
title: OneNote에서 회색조 이미지로 저장 - Aspose.Note
linktitle: OneNote에서 회색조 이미지로 저장 - Aspose.Note
second_title: Aspose.Note 자바 API
description: Java용 Aspose.Note를 사용하여 OneNote에서 문서를 회색조 이미지로 저장하는 방법을 알아보세요. 프로그래밍 방식으로 Microsoft OneNote 문서를 쉽게 조작할 수 있습니다.
weight: 17
url: /ko/java/onenote-document-saving/save-to-grayscale-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote에서 회색조 이미지로 저장 - Aspose.Note

## 소개

이 튜토리얼에서는 Java용 Aspose.Note를 사용하여 OneNote에서 문서를 회색조 이미지로 저장하는 방법을 살펴보겠습니다. 회색조 이미지는 색상 정보가 회색 음영으로만 표현되는 단색 이미지입니다. Aspose.Note는 Microsoft OneNote 문서를 프로그래밍 방식으로 조작할 수 있는 강력한 Java API입니다.

## 전제조건

시작하기 전에 다음 사항이 있는지 확인하세요.

1. 시스템에 JDK(Java Development Kit)가 설치되어 있습니다.
2.  Java 라이브러리용 Aspose.Note. 다음에서 다운로드할 수 있습니다.[여기](https://releases.aspose.com/note/java/).
3. Java 프로그래밍에 대한 기본 이해.

## 패키지 가져오기

시작하려면 필요한 패키지를 가져옵니다.

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## 1단계: 문서 로드

 먼저 문서를 Aspose.Note에 로드합니다. 바꾸다`"Your Document Directory"` 문서 디렉토리의 경로와`"Aspose.one"` OneNote 문서 이름으로.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## 2단계: 출력 경로 및 옵션 설정

회색조 이미지의 출력 경로를 정의하고 저장 옵션을 지정합니다. 색상 모드를 회색조로 설정하겠습니다.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## 3단계: 문서 저장

마지막으로 지정된 옵션을 사용하여 문서를 회색조 이미지로 저장합니다.

```java
oneFile.save(dataDir, options);
```

## 결론

축하해요! Java용 Aspose.Note를 사용하여 OneNote에서 문서를 회색조 이미지로 저장하는 방법을 성공적으로 배웠습니다. 이는 회색조 이미지가 필요한 다양한 응용 프로그램에 매우 유용할 수 있습니다.

## FAQ

### Q1: 회색조 이미지를 다른 형식으로 저장할 수 있나요?

 A1: 네, 가능합니다. 간단히 변경`SaveFormat` 매개변수`ImageSaveOptions` 원하는 형식으로 생성자를 생성합니다.

### Q2: Aspose.Note는 모든 버전의 OneNote 문서와 호환됩니까?

A2: Aspose.Note는 Microsoft OneNote 2010 이상을 지원합니다.

### Q3: Aspose.Note를 사용하려면 라이선스가 필요합니까?

A3: 예, 프로덕션 환경에서 Aspose.Note를 사용하려면 유효한 라이선스가 필요합니다. 그러나 테스트 목적으로 임시 라이센스를 얻을 수 있습니다.

### Q4: 문서를 이미지로 저장하기 전에 문서의 다른 측면을 조작할 수 있습니까?

A4: 물론이죠! Aspose.Note는 OneNote 문서를 프로그래밍 방식으로 편집하기 위한 다양한 기능을 제공합니다.

### Q5: 문제가 발생하면 어디서 지원을 받을 수 있나요?

A5: Aspose.Note 포럼에서 지원을 찾을 수 있습니다.[여기](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
