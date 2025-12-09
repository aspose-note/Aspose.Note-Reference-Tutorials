---
date: 2025-11-29
description: Aspose.Note for Java를 사용하여 OneNote 페이지를 PNG로 내보내는 방법을 배워보세요. 페이지 인덱스를
  설정하고, 페이지를 변환하고, 이미지를 저장하는 단계별 지침을 따라하세요.
linktitle: Export OneNote Page to PNG Image in Java
second_title: Aspose.Note Java API
title: Aspose.Note를 사용하여 Java에서 OneNote 페이지를 PNG 이미지로 내보내기
url: /ko/java/onenote-document-loading/convert-page-to-png-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Note를 사용하여 Java에서 OneNote 페이지를 PNG 이미지로 내보내기

## Introduction

이 튜토리얼에서는 Aspose.Note for Java 라이브러리를 사용하여 **OneNote 페이지를 PNG 이미지로 내보내는 방법**을 알아봅니다. 환경 설정부터 페이지 인덱스 지정, 최종적으로 고품질 PNG 파일로 저장하는 과정까지 모든 단계를 안내합니다. 끝까지 진행하면 OneNote 문서를 다루는 모든 Java 애플리케이션에 이 기능을 추가할 수 있게 됩니다.

## Quick Answers
- **필요한 라이브러리는?** Aspose.Note for Java.  
- **단일 페이지를 내보낼 수 있나요?** 예—`setPageIndex`를 사용하여 정확한 페이지를 지정합니다.  
- **지원되는 이미지 형식?** PNG, JPEG, GIF, BMP, TIFF (여기서는 PNG).  
- **라이선스가 필요한가요?** 무료 체험판을 사용할 수 있으며, 프로덕션에서는 라이선스가 필요합니다.  
- **구현에 걸리는 시간은?** 기본 변환은 보통 10분 이내입니다.

## What is “export OneNote page”?

OneNote 페이지를 내보낸다는 것은 `.one` 문서 내부의 특정 페이지를 독립적인 이미지 파일(PNG)로 변환하는 것을 의미합니다. OneNote 환경 외부에서 콘텐츠를 공유하거나, 삽입하거나, 처리해야 할 때 유용합니다.

## Why use Aspose.Note for Java to convert OneNote to PNG?
- **Microsoft Office 의존성 없음** – Java가 실행되는 모든 플랫폼에서 작동합니다.  
- **세밀한 제어** – `setPageIndex`를 통해 원하는 페이지를 선택할 수 있습니다.  
- **고품질 출력** – PNG는 벡터 그래픽과 텍스트 선명도를 유지합니다.  
- **배치 처리 가능** – 페이지를 순회하며 대량 변환을 쉽게 할 수 있습니다.

## Prerequisites

시작하기 전에 다음이 준비되어 있는지 확인하세요:

1. **Java Development Kit (JDK)** – 버전 8 이상.  
2. **Aspose.Note for Java** – 최신 JAR 파일을 [Aspose 웹사이트](https://releases.aspose.com/note/java/)에서 다운로드합니다.  
3. **내보내려는 페이지가 포함된 OneNote 문서** (`.one`).

## Import Packages

First, import the necessary Java classes:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.LoadOptions;
import com.aspose.note.SaveFormat;
```

## Step‑by‑Step Guide

### Step 1: Load the OneNote Document

```java
// Load the document into Aspose.Note.
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", new LoadOptions());
```

우리는 `Document` 클래스를 사용하여 디스크에서 OneNote 파일을 읽습니다. 필요에 따라 `LoadOptions` 객체로 로딩 동작을 맞춤 설정할 수 있습니다.

### Step 2: Initialize ImageSaveOptions

```java
// Initialize ImageSaveOptions object
ImageSaveOptions opts = new ImageSaveOptions(SaveFormat.Png);
```

`ImageSaveOptions`는 Aspose.Note에 출력 형식을 **PNG**로 지정한다는 것을 알려줍니다. `SaveFormat`을 변경하면 JPEG, BMP 등으로 전환할 수 있습니다.

### Step 3: Set the Page Index (How to convert OneNote page)

```java
// set page index
opts.setPageIndex(0);
```

`setPageIndex` 메서드는 내보낼 페이지를 선택합니다. 페이지 번호는 **0**부터 시작하므로 `0`은 첫 번째 페이지를 의미합니다. 다른 페이지를 내보내려면 이 값을 조정하세요.

### Step 4: Save the Document as PNG (Save OneNote as PNG)

```java
// Save the document as PNG.
oneFile.save(dataDir + "ConvertSpecificPageToPngImage_out.png", opts);
```

`save`를 호출하면 선택한 페이지가 디스크에 PNG 파일로 저장됩니다. 파일 이름 `ConvertSpecificPageToPngImage_out.png`는 예시일 뿐이며 원하는 이름으로 지정할 수 있습니다.

## Common Issues & Tips

- **잘못된 페이지 인덱스** – 인덱스가 0부터 시작한다는 점을 기억하세요. 빈 이미지가 나오면 인덱스 값을 확인하십시오.  
- **Aspose.Note JAR 누락** – JAR가 클래스패스에 포함되어 있는지 확인하세요. 그렇지 않으면 `ClassNotFoundException`이 발생합니다.  
- **큰 페이지** – 매우 큰 페이지의 경우 JVM 힙 크기(`-Xmx`)를 늘려 `OutOfMemoryError`를 방지하세요.

## Frequently Asked Questions

### Q1: Can I convert multiple pages to PNG images in one go using Aspose.Note for Java?
A1: 예, 문서의 페이지를 순회하면서 `opts.setPageIndex(i)`를 업데이트하고 각 반복마다 `save`를 호출하면 됩니다.

### Q2: Does Aspose.Note for Java support other image formats besides PNG?
A2: 물론입니다. `ImageSaveOptions`에서 `SaveFormat.Jpeg`, `SaveFormat.Gif`, `SaveFormat.Bmp`, `SaveFormat.Tiff` 등을 설정할 수 있습니다.

### Q3: Is there a free trial available for Aspose.Note for Java?
A3: 예, [웹사이트](https://releases.aspose.com/)에서 무료 체험판을 다운로드할 수 있습니다.

### Q4: Can I get technical assistance if I encounter any issues with Aspose.Note for Java?
A4: 예, Aspose 커뮤니티 포럼 [여기](https://forum.aspose.com/c/note/28)에서 지원을 받을 수 있습니다.

### Q5: Where can I purchase a license for Aspose.Note for Java?
A5: 라이선스는 [구매 페이지](https://purchase.aspose.com/buy)에서 구매할 수 있습니다.

### Q6: How do I export a page that contains embedded images?
A6: 삽입된 이미지는 PNG 출력에 자동으로 렌더링되며 별도의 코드는 필요하지 않습니다.

### Q7: Can I set the DPI or image resolution?
A7: 예, `save` 호출 전에 `opts.setResolution(int dpi)`를 사용하여 출력 품질을 조정할 수 있습니다.

---

**Last Updated:** 2025-11-29  
**Tested With:** Aspose.Note for Java 24.11 (latest)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}