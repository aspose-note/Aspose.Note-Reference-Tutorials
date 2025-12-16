---
date: 2025-12-16
description: Aspose.Note for Java의 이미지 저장 옵션을 사용하여 OneNote 문서를 BMP 이미지로 저장하는 방법을 배웁니다.
  또한 OneNote를 PDF 또는 PNG로 저장하는 방법도 확인하세요.
linktitle: how to save onenote to BMP Image Using Image Save Options
second_title: Aspose.Note Java API
title: 이미지 저장 옵션을 사용하여 OneNote를 BMP 이미지로 저장하는 방법
url: /ko/java/onenote-document-saving/save-to-bmp-image-using-image-save-options/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Image Save Options를 사용하여 OneNote를 BMP 이미지로 저장하는 방법

## Introduction

Aspose.Note for Java는 Microsoft OneNote 파일을 프로그래밍 방식으로 다룰 수 있게 해 주는 강력한 라이브러리입니다. **이 튜토리얼에서는 Aspose.Note for Java의 Image Save Options 기능을 사용해 OneNote 문서를 BMP 이미지로 저장하는 방법을 배웁니다**. 각 단계를 차근차근 살펴보고, BMP를 다른 포맷보다 선택해야 하는 이유를 설명하며, 이 기능을 여러분의 애플리케이션에 어떻게 통합할 수 있는지 보여드립니다.

## Quick Answers
- **Image Save Options 클래스는 무엇을 하나요?** OneNote 페이지를 변환할 때 출력 이미지 형식(BMP, PNG, JPEG 등)을 지정할 수 있습니다.  
- **샘플을 실행하려면 라이선스가 필요합니까?** 평가용 무료 체험판으로도 실행할 수 있지만, 상용 환경에서는 상업용 라이선스가 필요합니다.  
- **BMP 대신 PDF나 PNG로 변환할 수 있나요?** 예 – `SaveFormat` 열거형을 `SaveFormat.Pdf` 또는 `SaveFormat.Png` 등으로 바꾸면 됩니다.  
- **지원되는 Java 버전은 무엇인가요?** Java 8 이상을 완전 지원합니다.  
- **대용량 문서에 대한 특별한 처리 방법이 있나요?** 메모리 사용량을 줄이기 위해 출력 스트리밍을 활용할 수 있습니다.

## What is “Image Save Options” in Aspose.Note?
`ImageSaveOptions` 클래스는 OneNote 페이지를 래스터 이미지로 렌더링하는 방식을 세밀하게 제어할 수 있게 해 줍니다. 이미지 형식, 해상도, 색 깊이 등을 설정할 수 있어 레거시 시스템용 BMP 파일이나 웹용 PNG/JPEG 파일을 손쉽게 생성할 수 있습니다.

## Prerequisites

시작하기 전에 다음이 준비되어 있는지 확인하세요:

1. Java 프로그래밍 언어에 대한 기본 지식.  
2. 머신에 JDK(Java Development Kit)가 설치되어 있음.  
3. Eclipse 또는 IntelliJ IDEA와 같은 IDE.  
4. Aspose.Note for Java 라이브러리 – [여기](https://releases.aspose.com/note/java/)에서 다운로드.

## Import Packages

먼저 필요한 Aspose.Note 클래스와 표준 Java I/O 유틸리티를 import합니다:

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Step 1: Load the OneNote Document

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";

// Load the document into Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

여기서는 소스 OneNote 파일(`Aspose.one`)이 들어 있는 폴더를 지정하고, 이를 `Document` 객체로 로드합니다. 이 객체를 통해 노트북 내 페이지, 섹션 및 기타 요소에 완전하게 접근할 수 있습니다.

## Step 2: Save the Document as a BMP Image

```java
dataDir = dataDir + "SaveToBmpImageUsingImageSaveOptions_out.bmp";

// Save the document.
oneFile.save(dataDir, new ImageSaveOptions(SaveFormat.Bmp));
```

출력 파일 이름을 연결한 뒤, **BMP**(`SaveFormat.Bmp`)로 설정된 `ImageSaveOptions` 인스턴스를 사용해 `save`를 호출합니다.  
PNG로 **OneNote 페이지를 저장**하고 싶다면 `SaveFormat.Bmp`를 `SaveFormat.Png`로 바꾸면 됩니다. 마찬가지로 `SaveFormat.Pdf`를 사용하면 **OneNote를 PDF**로 변환할 수 있습니다.

## Why Choose BMP?
- **무손실 품질** – BMP는 원시 픽셀 데이터를 그대로 저장하므로 원본 페이지의 정확한 모습을 유지합니다.  
- **호환성** – 오래된 Windows 애플리케이션이 BMP 파일을 요구하는 경우가 많습니다.  
- **단순성** – 압축 아티팩트가 없어서 추가 이미지 처리에 이상적입니다.

## Common Issues & Tips

- **파일 경로 오류** – `dataDir`이 적절한 파일 구분자(`/` 또는 `\`)로 끝나는지 확인하세요.  
- **대용량 노트북** – 매우 큰 OneNote 파일의 경우, 메모리 사용량을 낮추기 위해 페이지별로 개별 저장하는 것을 고려하세요.  
- **라이선스 예외** – 유효한 라이선스 없이 코드를 실행하면 생성된 이미지에 워터마크가 추가됩니다.

## Conclusion

이 가이드에서는 Aspose.Note for Java의 `ImageSaveOptions`를 활용해 **OneNote 문서를 BMP 이미지로 저장**하는 방법을 보여드렸습니다. `SaveFormat` 열거형을 교체하면 PNG, JPEG, PDF 등 다른 지원 포맷도 손쉽게 생성할 수 있어, 다양한 다운스트림 시나리오에 맞게 OneNote 콘텐츠를 유연하게 내보낼 수 있습니다.

## Frequently Asked Questions

**Q1: BMP 외에 다른 이미지 포맷으로 OneNote 문서를 저장할 수 있나요?**  
A: 네, `ImageSaveOptions`와 `SaveFormat.Png`, `SaveFormat.Jpeg`, `SaveFormat.Gif`, `SaveFormat.Tiff` 등을 사용해 해당 포맷으로 내보낼 수 있습니다.

**Q2: Aspose.Note for Java는 다양한 문서 포맷 간 변환을 지원하나요?**  
A: 물론입니다. 이미지 포맷 외에도 적절한 `SaveFormat`을 지정하면 OneNote 파일을 PDF, DOCX, HTML 등으로 변환할 수 있습니다.

**Q3: Aspose.Note for Java는 최신 OneNote 버전과 호환되나요?**  
A: 네, 라이브러리는 최신 OneNote 릴리스와 동기화되도록 정기적으로 업데이트됩니다.

**Q4: OneNote 문서의 내용을 프로그래밍 방식으로 조작할 수 있나요?**  
A: 예, API를 통해 페이지, 섹션, 텍스트, 이미지, 표 등 풍부한 콘텐츠를 추가, 편집, 삭제할 수 있습니다.

**Q5: Aspose.Note for Java는 기술 지원을 제공하나요?**  
A: 예, Aspose는 기술 지원 및 전용 포럼을 운영합니다. 도움이 필요하면 [Aspose.Note 포럼](https://forum.aspose.com/c/note/28)을 방문하세요.

---

**마지막 업데이트:** 2025-12-16  
**테스트 환경:** Aspose.Note for Java 24.12  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
