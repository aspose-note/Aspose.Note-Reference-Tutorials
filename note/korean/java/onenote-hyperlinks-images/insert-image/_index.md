---
date: 2025-12-21
description: Aspose.Note for Java를 사용하여 Java로 OneNote 문서에 이미지를 추가하는 방법을 배워보세요. 단계별
  가이드를 따라 이미지를 삽입하고 필요에 따라 OneNote를 PDF로 저장할 수 있습니다.
linktitle: Insert an Image in OneNote Document with Java
second_title: Aspose.Note Java API
title: Java를 사용하여 OneNote에 이미지 추가하는 방법
url: /ko/java/onenote-hyperlinks-images/insert-image/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java를 사용하여 OneNote 문서에 이미지 삽입하기

## 소개

이 튜토리얼에서는 Aspose.Note for Java의 도움을 받아 Java를 사용해 OneNote 문서에 이미지를 삽입하는 방법을 살펴봅니다. Aspose.Note for Java은 개발자가 Microsoft OneNote 파일을 프로그래밍 방식으로 작업할 수 있게 해 주는 강력한 라이브러리로, 문서 생성, 읽기 및 조작과 같은 다양한 작업을 가능하게 합니다.

## 빠른 답변
- **Java를 사용하여 OneNote에 이미지를 추가하는 가장 쉬운 방법은 무엇인가요?**  
  Aspose.Note for Java의 `Image` 클래스를 사용하고 페이지에 추가합니다.
- **프로덕션 사용을 위해 라이선스가 필요합니까?**  
  네, 프로덕션 배포를 위해서는 상업용 라이선스가 필요합니다.
- **이미지의 사용자 정의 크기를 설정할 수 있나요?**  
  물론입니다 – `Image` 객체에서 `setWidth()`와 `setHeight()`를 호출하면 됩니다.
- **이미지를 추가한 후 OneNote 파일을 PDF로 저장할 수 있나요?**  
  네, `save(..., SaveFormat.Pdf)`를 호출하여 **OneNote를 PDF로 저장**할 수 있습니다.
- **지원되는 Java 버전은 무엇인가요?**  
  Aspose.Note for Java은 JDK 8 이상에서 작동합니다.

## Java를 사용하여 OneNote에 이미지 추가하는 방법?

코드에 들어가기 전에, 왜 프로그래밍 방식으로 OneNote에 이미지를 삽입하고 싶을지 간략히 살펴보겠습니다. 회의록을 자동으로 생성하거나, 자동 보고서를 만들거나, 문서화 파이프라인을 구축할 때, 이미지는 순수 텍스트만으로는 전달할 수 없는 시각적 컨텍스트를 제공합니다. Aspose.Note for Java를 사용하면 OneNote UI를 열지 않고도 코드만으로 이러한 작업을 수행할 수 있습니다.

## 사전 요구 사항

시작하기 전에 다음 사전 요구 사항이 설정되어 있는지 확인하십시오:

### 1. Java Development Kit (JDK)
시스템에 Java Development Kit (JDK)가 설치되어 있는지 확인하십시오. Oracle 웹사이트에서 JDK를 다운로드하고 설치할 수 있습니다.

### 2. Aspose.Note for Java Library
[Aspose.Note for Java 문서](https://reference.aspose.com/note/java/)를 따라 라이브러리를 다운로드하고 설정하십시오.

## 패키지 가져오기

Java 프로젝트에 필요한 패키지를 가져옵니다. 여기에는 Aspose.Note 라이브러리와 기타 종속성이 포함됩니다.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

OneNote 문서에 이미지를 삽입하는 과정을 여러 단계로 나누어 살펴보겠습니다:

## 단계 1: OneNote 문서 로드

이미지를 삽입하려는 OneNote 문서를 먼저 로드합니다.

```java
LoadOptions options = new LoadOptions();
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", options);
```

## 단계 2: 페이지 가져오기

이미지를 삽입하려는 문서 내 페이지를 가져옵니다.

```java
Page page = oneFile.getFirstChild();
```

## 단계 3: 이미지 로드

OneNote 문서에 삽입할 이미지를 로드합니다.

```java
Image image = new Image(oneFile, dataDir + "Input.jpg");
```

## 단계 4: 이미지 속성 사용자 지정 (선택 사항)

필요에 따라 이미지의 크기, 위치 및 정렬을 사용자 지정할 수 있습니다. 여기서 **set image dimensions Java** 스타일로 이미지 크기를 설정합니다.

```java
image.setWidth(100);
image.setHeight(100);
image.setVerticalOffset(400);
image.setHorizontalOffset(100);
image.setAlignment(HorizontalAlignment.Right);
```

## 단계 5: 페이지에 이미지 추가

이미지를 OneNote 문서의 페이지에 추가합니다.

```java
page.appendChildLast(image);
```

## 단계 6: 문서 저장

삽입된 이미지를 포함한 수정된 문서를 저장합니다. 이 단계에서 **OneNote를 PDF로 저장**할 수도 있습니다.

```java
try {
    oneFile.save(dataDir + "InsertanImage_out.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## 결론

이 튜토리얼을 통해 Aspose.Note for Java 라이브러리를 활용하여 Java로 OneNote 문서에 이미지를 삽입하는 방법을 배웠습니다. 단계별 가이드를 따라 하면 프로그래밍 방식으로 OneNote 문서에 이미지를 손쉽게 포함시킬 수 있습니다.

## FAQ

### Q1: 이 방법으로 하나의 OneNote 문서에 여러 이미지를 삽입할 수 있나요?

A1: 네, 각 이미지를 삽입할 때마다 이 튜토리얼의 과정을 반복하면 하나의 OneNote 문서에 여러 이미지를 삽입할 수 있습니다.

### Q2: Aspose.Note for Java는 모든 버전의 OneNote와 호환되나요?

A2: Aspose.Note for Java는 Microsoft OneNote 2010 및 이후 버전에서 만든 OneNote 파일을 지원합니다.

### Q3: PNG나 GIF와 같은 다양한 형식의 이미지를 OneNote 문서에 삽입할 수 있나요?

A3: 네, Aspose.Note for Java는 PNG, JPEG, GIF 등 다양한 이미지 형식을 삽입하는 것을 지원합니다.

### Q4: 테스트용으로 사용할 수 있는 Aspose.Note for Java 체험판이 있나요?

A4: 네, 평가 목적으로 Aspose.Note for Java의 무료 체험판을 웹사이트에서 다운로드할 수 있습니다.

### Q5: Aspose.Note for Java에 대한 기술 지원은 어떻게 받을 수 있나요?

A5: Aspose.Note 제품 전용 [포럼](https://forum.aspose.com/c/note/28)에서 기술 지원을 받을 수 있습니다.

---

**마지막 업데이트:** 2025-12-21  
**테스트 대상:** Aspose.Note for Java 24.10  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}