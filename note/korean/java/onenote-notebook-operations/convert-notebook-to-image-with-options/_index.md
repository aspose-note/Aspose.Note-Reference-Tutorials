---
date: 2025-12-28
description: Aspose.Note를 사용하여 Java에서 OneNote를 이미지로 변환하고 이미지 해상도를 설정하는 방법을 배워보세요.
  이 단계별 가이드에서는 OneNote PNG 파일을 내보내는 방법도 보여줍니다.
linktitle: Convert OneNote to Image with Options - Aspose.Note
second_title: Aspose.Note Java API
title: 옵션을 사용하여 OneNote를 이미지로 변환 - Aspose.Note
url: /ko/java/onenote-notebook-operations/convert-notebook-to-image-with-options/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 옵션을 사용한 OneNote 이미지 변환 - Aspose.Note

## Introduction

이 튜토리얼에서는 Aspose.Note for Java를 사용하여 다양한 옵션으로 **OneNote를 이미지로 변환**하는 방법을 배웁니다. 보고서를 위한 고해상도 PNG가 필요하든 빠른 JPEG 썸네일이 필요하든, 아래 단계에서는 정확히 어떻게 수행하고 Java 애플리케이션에 통합하는지 보여줍니다.

## Quick Answers
- **“OneNote를 이미지로 변환”이란 무엇인가요?** 전체 OneNote 노트북을 래스터 이미지 파일(PNG, JPEG 등)로 변환합니다.
- **무손실 품질에 권장되는 포맷은?** PNG, 압축 아티팩트 없이 모든 세부 정보를 보존합니다.
- **Java에서 이미지 해상도를 어떻게 설정하나요?** `NotebookImageSaveOptions`를 통해 `ImageSaveOptions.setResolution(int dpi)`를 사용합니다.
- **OneNote 노트북을 한 번에 PNG로 내보낼 수 있나요?** 네, Aspose.Note는 적절한 옵션을 사용한 단일 `save` 호출을 제공합니다.
- **프로덕션 사용에 라이선스가 필요합니까?** 프로덕션에는 상용 라이선스가 필요하며, 평가용 무료 체험판을 사용할 수 있습니다.

## What is “convert OneNote to image”?

OneNote 노트북을 이미지로 변환한다는 것은 노트북의 각 페이지를 비트맵 파일로 렌더링하는 것을 의미합니다. 이는 정적 미리보기 생성, 콘텐츠 아카이빙, 또는 원본 OneNote 형식을 지원하지 않는 보고서에 노트북 페이지를 삽입할 때 유용합니다.

## Why use Aspose.Note for Java?
- **전체 제어**: 출력 포맷, 해상도 및 색 깊이를 자유롭게 설정.  
- **Microsoft Office 의존 없음** – 모든 서버‑사이드 Java 환경에서 작동합니다.  
- **복잡한 노트북 지원**: 임베디드 파일, 잉크, 풍부한 텍스트를 포함한 노트북을 지원합니다.

## Prerequisites

1. **Java Development Kit (JDK)** – 버전 8 이상.  
2. **Aspose.Note for Java JAR 파일** – 최신 라이브러리를 [여기](https://releases.aspose.com/note/java/)에서 다운로드하고 프로젝트 클래스패스에 추가합니다.  

## Import Packages

First, import the classes we’ll need for loading the notebook and configuring the image output.

```java
import java.io.IOException;

import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Step 1: Load the Notebook

Load the OneNote notebook you want to convert. Replace the path with the location of your `.onetoc2` file.

```java
String dataDir = "Your Document Directory";
// Load a OneNote Notebook
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

## Step 2: Set Save Options (How to **set image resolution java**)

Create a `NotebookImageSaveOptions` instance, choose the output format, and specify the desired resolution. In this example we use PNG at 400 dpi.

```java
NotebookImageSaveOptions notebookSaveOptions = new NotebookImageSaveOptions(SaveFormat.Png);

ImageSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();

documentSaveOptions.setResolution(400);
```

> **프로 팁:** 대형 노트북을 빠르게 처리하려면 해상도를 낮추세요(예: 150 dpi). 인쇄용 그래픽이 필요하면 해상도를 높이세요.

## Step 3: Save the Notebook as Image (How to **export OneNote PNG**)

Define the output file name and call `save`. The same options are applied to every page in the notebook.

```java
dataDir = dataDir + "ExportNotebooktoImagewithOptions_out.png";

// Save the Notebook
notebook.save(dataDir, notebookSaveOptions);
```

위 코드는 설정한 해상도로 PNG 파일(또는 페이지당 하나씩 여러 PNG 파일)을 생성합니다.

## Common Issues and Solutions

| 문제 | 해결책 |
|-------|----------|
| **OutOfMemoryError** 대형 노트북에서 | JVM 힙 크기(`-Xmx2g`)를 늘리거나 해상도를 낮추세요. |
| **출력에 빈 페이지** | 노트북에 비밀번호가 설정되어 있지 않은지 확인하고, 필요하면 `Notebook.load(path, password)`를 사용하세요. |
| **지원되지 않는 이미지 포맷** | `SaveFormat.Png`, `SaveFormat.Jpeg`, `SaveFormat.Bmp`만 사용하세요 – 다른 포맷은 노트북 내보내기를 지원하지 않습니다. |

## Frequently Asked Questions

**Q: Aspose.Note가 복잡한 OneNote 파일을 처리할 수 있나요?**  
A: 네, 임베디드 파일, 잉크 주석 및 풍부한 서식을 포함한 노트북을 효율적으로 처리합니다.

**Q: Aspose.Note for Java를 기존 프로젝트에 쉽게 통합할 수 있나요?**  
A: 물론입니다. API가 직관적이며 JAR 파일을 클래스패스에 추가하기만 하면 됩니다.

**Q: 노트북을 변환할 때 이미지 출력을 사용자 정의할 수 있나요?**  
A: 네. `ImageSaveOptions`를 통해 해상도, 포맷, 색 깊이 등을 설정할 수 있습니다.

**Q: Aspose.Note가 개발자를 위한 지원을 제공하나요?**  
A: 네. Aspose는 방대한 문서, 포럼 및 신속한 지원 채널을 제공합니다.

**Q: Aspose.Note for Java에 무료 체험판이 있나요?**  
A: 네, [여기](https://releases.aspose.com/)에서 체험판을 다운로드할 수 있습니다.

---

**마지막 업데이트:** 2025-12-28  
**테스트 환경:** Aspose.Note 24.11 for Java  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}