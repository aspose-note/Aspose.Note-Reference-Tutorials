---
date: 2026-03-19
description: Java와 Aspose.Note for Java를 사용하여 OneNote에 이미지를 추가하는 방법을 배우고, 이미지 크기를
  설정하는 방법과 OneNote를 PDF로 저장하는 방법을 포함합니다.
linktitle: Insert an Image in OneNote Document with Java
second_title: Aspose.Note Java API
title: Java를 사용하여 OneNote에 이미지 추가
url: /ko/java/onenote-hyperlinks-images/insert-image/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java를 사용하여 OneNote 문서에 이미지 삽입

## Introduction

이 튜토리얼에서는 Java와 Aspose.Note for Java 라이브러리를 사용하여 프로그래밍 방식으로 **OneNote에 이미지를 추가하는 방법**을 배웁니다. OneNote 페이지에 그림을 삽입하면 회의록, 자동 보고서, 텍스트와 시각 데이터를 결합한 문서를 생성할 때 유용합니다. 가이드를 마치면 기존 OneNote 파일을 로드하고, 이미지를 삽입하며, 필요에 따라 크기와 위치를 조정하고, **OneNote를 PDF로 저장**까지 할 수 있습니다 – OneNote UI를 열 필요 없이.

## Quick Answers
- **Java를 사용하여 OneNote에 이미지를 추가하는 가장 쉬운 방법은 무엇인가요?**  
  Aspose.Note for Java의 `Image` 클래스를 사용하고 페이지에 추가합니다.
- **프로덕션 사용에 라이선스가 필요합니까?**  
  예, 프로덕션 배포에는 상업용 라이선스가 필요합니다.
- **이미지에 사용자 지정 크기를 설정할 수 있나요?**  
  물론입니다 – `Image` 객체에 `setWidth()`와 `setHeight()`를 호출하면 됩니다.
- **이미지를 추가한 후 OneNote 파일을 PDF로 저장할 수 있나요?**  
  예, `save(..., SaveFormat.Pdf)`를 호출하여 **OneNote를 PDF로 저장**합니다.
- **지원되는 Java 버전은 무엇인가요?**  
  Aspose.Note for Java는 JDK 8 이상에서 작동합니다.

## Why add image to OneNote?

시각 요소를 추가하면 노트를 이해하기 쉽고 더 매력적으로 만들 수 있습니다. 이미지는 다이어그램, 스크린샷, 데이터 차트 등을 설명하는 데 도움이 되며, 텍스트만으로는 긴 설명이 필요할 수 있습니다. 이 단계를 자동화하면 특히 데이터 소스로부터 대량의 노트를 생성할 때 시간을 절약할 수 있습니다.

## Prerequisites

시작하기 전에 다음 준비물을 확인하십시오:

### 1. Java Development Kit (JDK)
JDK 8 이상을 설치하십시오. Oracle 웹사이트에서 다운로드하거나 OpenJDK 배포판을 사용할 수 있습니다.

### 2. Aspose.Note for Java Library
최신 Aspose.Note for Java 라이브러리를 다운로드하고 프로젝트의 클래스패스에 추가하십시오. 자세한 설정 방법은 공식 [documentation](https://reference.aspose.com/note/java/)에 있습니다.

## Import Packages

필요한 클래스를 import하여 시작합니다. 이 import문을 통해 핵심 Aspose.Note 기능과 기본 Java 유틸리티에 접근할 수 있습니다.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## Step‑by‑Step Guide

아래는 간결한 번호 매기기 단계별 안내입니다. 각 단계는 간단한 설명과 복사해서 사용할 수 있는 정확한 코드를 포함합니다.

### Step 1: Load the OneNote document

우리는 `LoadOptions` 인스턴스를 생성하고(향후 사용자 정의에 유용) 기존 `.one` 파일을 엽니다.

```java
LoadOptions options = new LoadOptions();
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", options);
```

### Step 2: Get the target page

간단히 문서의 첫 번째 페이지를 사용하지만 필요에 따라 다른 페이지로 이동할 수 있습니다.

```java
Page page = oneFile.getFirstChild();
```

### Step 3: Load the image you want to embed

`Image` 객체를 생성할 때 문서 참조와 이미지 파일 경로를 전달합니다.

```java
Image image = new Image(oneFile, dataDir + "Input.jpg");
```

### Step 4: Set image dimensions Java (optional)

이미지를 특정 영역에 맞추려면 너비, 높이 및 오프셋을 조정합니다. 여기서 보조 키워드 **set image dimensions java**가 활용됩니다.

```java
image.setWidth(100);
image.setHeight(100);
image.setVerticalOffset(400);
image.setHorizontalOffset(100);
image.setAlignment(HorizontalAlignment.Right);
```

### Step 5: Append the image to the page

`appendChildLast` 메서드는 선택한 페이지에 이미지를 마지막 요소로 추가합니다.

```java
page.appendChildLast(image);
```

### Step 6: Save the document – you can also save OneNote as PDF

마지막으로 변경 사항을 저장합니다. 예제는 파일을 PDF로 저장하는 방법을 보여주며, 보조 키워드 **save onenote as pdf**를 충족합니다.

```java
try {
    oneFile.save(dataDir + "InsertanImage_out.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Common Issues and Solutions

| 증상 | 가능한 원인 | 해결 방법 |
|---------|--------------|-----|
| `FileNotFoundException` 발생 (이미지 로드 시) | 이미지 경로가 올바르지 않음 | `dataDir`와 이미지 파일 이름이 올바른지 확인하십시오. |
| 이미지가 왜곡됨 | 너비/높이가 잘못 설정됨 | `setWidth`/`setHeight` 호출 전에 원본 이미지 크기를 사용하거나 적절한 종횡비를 계산하십시오. |
| PDF 출력이 비어 있음 | Aspose.Note 라이선스 누락 | `save` 호출 전에 유효한 라이선스를 적용하십시오. |

## Frequently Asked Questions

### Q1: 이 방법으로 하나의 OneNote 문서에 여러 이미지를 삽입할 수 있나요?

**A:** 예. 각 이미지마다 Steps 3‑5를 반복하면 됩니다.

### Q2: Aspose.Note for Java가 모든 버전의 OneNote와 호환되나요?

**A:** Aspose.Note for Java는 Microsoft OneNote 2010 및 이후 버전으로 만든 OneNote 파일을 지원합니다.

### Q3: PNG나 GIF와 같은 다양한 형식의 이미지를 OneNote 문서에 삽입할 수 있나요?

**A:** 물론 가능합니다. 라이브러리는 PNG, JPEG, GIF, BMP 및 기타 일반적인 형식을 지원합니다.

### Q4: 테스트용 Aspose.Note for Java 체험판이 있나요?

**A:** 예, 구매 전에 API를 평가할 수 있도록 Aspose 웹사이트에서 무료 체험판을 다운로드할 수 있습니다.

### Q5: Aspose.Note for Java에 대한 기술 지원은 어떻게 받을 수 있나요?

**A:** Aspose.Note 제품 전용 [forum](https://forum.aspose.com/c/note/28)에서 도움을 받을 수 있습니다.

## Conclusion

이제 Java를 사용하여 **OneNote에 이미지를 추가하는** 방법, 외관을 맞춤 설정하고 필요에 따라 **OneNote를 PDF로 저장**하는 완전한 프로덕션 준비 예제가 준비되었습니다. 보고 엔진, 자동 문서화 시스템, 맞춤형 노트 작성 애플리케이션 등 자신의 워크플로에 맞게 코드를 자유롭게 적용하십시오.

---

**마지막 업데이트:** 2026-03-19  
**테스트 환경:** Aspose.Note for Java 24.10  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}