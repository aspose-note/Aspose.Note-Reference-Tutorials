---
title: OneNote에서 특정 페이지를 PNG 이미지로 변환 - Java
linktitle: OneNote에서 특정 페이지를 PNG 이미지로 변환 - Java
second_title: Aspose.Note 자바 API
description: OneNote 페이지를 PNG로 변환하여 Java용 Aspose.Note를 사용하는 방법을 알아보세요. 쉬운 단계를 따르고, 문서를 로드하고, 옵션을 설정하세요. 이 기능으로 Java 앱을 향상하세요.
type: docs
weight: 13
url: /ko/java/onenote-document-loading/convert-page-to-png-image/
---
## 소개

이 튜토리얼에서는 Java용 Aspose.Note를 사용하여 OneNote 문서의 특정 페이지를 PNG 이미지로 변환하는 방법을 배웁니다. 이 기능을 Java 애플리케이션에 원활하게 통합하는 데 도움이 되도록 프로세스를 따라하기 쉬운 단계로 나누어 보겠습니다.

## 전제조건

시작하기 전에 다음 사항을 확인하세요.

1. JDK(Java Development Kit): 시스템에 JDK가 설치되어 있는지 확인하세요.
2.  Aspose.Note for Java 라이브러리: 다음에서 Aspose.Note for Java 라이브러리를 다운로드하고 설치하세요.[웹사이트](https://releases.aspose.com/note/java/).
3. OneNote 문서: 특정 페이지를 PNG로 변환하려는 OneNote 문서를 준비하세요.

## 패키지 가져오기

먼저 필요한 패키지를 Java 파일로 가져와야 합니다.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.LoadOptions;
import com.aspose.note.SaveFormat;
```

## 1단계: OneNote 문서 로드

```java
// 문서를 Aspose.Note에 로드합니다.
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", new LoadOptions());
```

 이 단계에서는 Aspose.Note를 사용하여 OneNote 문서를 로드합니다.`Document` 수업.

## 2단계: ImageSaveOptions 객체 초기화

```java
// ImageSaveOptions 객체 초기화
ImageSaveOptions opts = new ImageSaveOptions(SaveFormat.Png);
```

 여기서는`ImageSaveOptions` 개체를 선택하고 저장 형식을 PNG로 지정합니다.

## 3단계: 페이지 색인 설정

```java
// 페이지 색인 설정
opts.setPageIndex(0);
```

변환하려는 페이지의 인덱스를 설정하세요. 페이지 색인은 0부터 시작됩니다.

## 4단계: 문서를 PNG로 저장

```java
// 문서를 PNG로 저장합니다.
oneFile.save(dataDir + "ConvertSpecificPageToPngImage_out.png", opts);
```

마지막으로 지정된 페이지를 PNG 이미지로 변환하여 문서를 저장합니다.

## 결론

축하해요! Java용 Aspose.Note를 사용하여 OneNote 문서의 특정 페이지를 PNG 이미지로 변환하는 방법을 성공적으로 배웠습니다. 이 기능을 Java 응용 프로그램에 통합하면 OneNote 문서를 프로그래밍 방식으로 조작하여 생산성을 높이고 소프트웨어 기능을 확장할 수 있습니다.

## FAQ

### Q1: Java용 Aspose.Note를 사용하여 한 번에 여러 페이지를 PNG 이미지로 변환할 수 있나요?

A1: 예, 페이지를 반복하고 개별적으로 저장하면 일괄 변환을 수행할 수 있습니다.

### Q2: Java용 Aspose.Note는 PNG 외에 다른 이미지 형식을 지원합니까?

A2: 예, Aspose.Note는 JPEG, GIF, BMP 및 TIFF와 같은 다양한 이미지 형식을 지원합니다.

### Q3: Aspose.Note for Java에 대한 무료 평가판이 있습니까?

 A3: 예, 다음에서 무료 평가판에 액세스할 수 있습니다.[웹사이트](https://releases.aspose.com/).

### Q4: Aspose.Note for Java에 문제가 발생하면 기술 지원을 받을 수 있나요?

 A4: 물론입니다. Aspose 커뮤니티 포럼에서 지원을 요청할 수 있습니다.[여기](https://forum.aspose.com/c/note/28).

### Q5: Aspose.Note for Java 라이선스는 어디서 구매할 수 있나요?

 A5: 다음에서 라이센스를 구입할 수 있습니다.[구매 페이지](https://purchase.aspose.com/buy).