---
title: OneNote에서 고정 임계값을 사용하여 이진 이미지에 저장
linktitle: OneNote에서 고정 임계값을 사용하여 이진 이미지에 저장
second_title: Aspose.Note 자바 API
description: Aspose.Note Java의 고정 임계값을 사용하여 Microsoft OneNote 문서를 바이너리 이미지로 쉽게 저장할 수 있습니다. OneNote 파일 조작 기능을 향상하세요.
weight: 14
url: /ko/java/onenote-document-saving/save-to-binary-image-using-fixed-threshold/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote에서 고정 임계값을 사용하여 이진 이미지에 저장

## 소개

Aspose.Note for Java는 개발자가 Microsoft OneNote 파일을 프로그래밍 방식으로 작업할 수 있게 해주는 강력한 API입니다. 이 튜토리얼에서는 고정된 임계값을 사용하여 문서를 바이너리 이미지로 저장하는 방법을 살펴보겠습니다. 이를 달성하려면 아래 단계를 따르십시오.

## 전제조건

시작하기 전에 다음 사항이 있는지 확인하세요.

1. 시스템에 JDK(Java Development Kit)가 설치되어 있습니다.
2.  Java 라이브러리용 Aspose.Note가 다운로드되었습니다. 다음에서 다운로드할 수 있습니다.[여기](https://releases.aspose.com/note/java/).
3. Java 프로그래밍에 대한 기본 지식.

## 패키지 가져오기

먼저 필요한 패키지를 Java 파일로 가져옵니다.

```java
import com.aspose.note.*;
import java.io.IOException;
```

## 1단계: 문서 로드

Aspose.Note API를 사용하여 OneNote 문서를 로드합니다.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## 2단계: 이진화 옵션 설정

문서를 바이너리 이미지로 저장하기 위한 바이너리화 옵션을 정의합니다.

```java
dataDir = dataDir + "SaveToBinaryImageUsingFixedThreshold_out.png";
ImageBinarizationOptions binarizationOptions = new ImageBinarizationOptions();
binarizationOptions.setBinarizationMethod(BinarizationMethod.FixedThreshold);
binarizationOptions.setBinarizationThreshold(123);
```

## 3단계: 이미지 저장 옵션 설정

색상 모드 및 이진화 옵션을 포함한 이미지 저장 옵션을 설정합니다.

```java
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.BlackAndWhite);
options.setBinarizationOptions(binarizationOptions);
```

## 4단계: 문서 저장

지정된 옵션을 사용하여 문서를 바이너리 이미지로 저장합니다.

```java
oneFile.save(dataDir, options);
```

## 결론

이 튜토리얼에서는 Java용 Aspose.Note에서 고정 임계값을 사용하여 문서를 바이너리 이미지로 저장하는 방법을 배웠습니다. 다음 단계를 수행하면 OneNote 파일을 프로그래밍 방식으로 쉽게 조작할 수 있습니다.

## FAQ

### Q1: 이진화 임계값을 조정할 수 있나요?

 A1: 예, 요구 사항에 따라 임계값을 수정하여 임계값을 조정할 수 있습니다.`setBinarizationThreshold()` 메소드 매개변수.

### Q2: Aspose.Note for Java는 모든 버전의 Microsoft OneNote와 호환됩니까?

A2: Aspose.Note for Java는 2010, 2013, 2016을 포함한 다양한 버전의 Microsoft OneNote를 지원합니다.

### Q3: 처리할 수 있는 문서 크기에 제한이 있나요?

A3: Aspose.Note for Java는 처리할 수 있는 문서 크기에 제한이 없으므로 대용량 파일을 효율적으로 처리할 수 있습니다.

### Q4: 여러 OneNote 문서를 동시에 변환할 수 있나요?

A4: 예, 각 파일을 반복하고 필요한 작업을 적용하여 여러 OneNote 문서를 일괄 처리할 수 있습니다.

### Q5: Aspose.Note for Java에 대한 기술 지원이 가능한가요?

 A5: 예, 기술 지원은 다음을 통해 제공됩니다.[Aspose.Note 포럼](https://forum.aspose.com/c/note/28)에서 질문을 하고 전문가에게 도움을 구할 수 있습니다.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
