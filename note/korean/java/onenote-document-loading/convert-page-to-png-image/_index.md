---
date: 2026-02-05
description: OneNote 페이지를 내보내고 이미지를 저장하는 방법을 배웁니다. 이 가이드는 .one 파일을 PNG로 변환하고, 페이지
  인덱스를 설정하며, Aspose.Note for Java를 사용하여 OneNote 페이지 이미지를 내보내는 방법을 보여줍니다.
linktitle: Export OneNote Page to PNG Image in Java
second_title: Aspose.Note Java API
title: Aspose.Note를 사용하여 Java에서 OneNote 페이지를 PNG 이미지로 내보내는 방법
url: /ko/java/onenote-document-loading/convert-page-to-png-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java에서 Aspose.Note를 사용하여 OneNote 페이지를 PNG 이미지로 내보내기

## 소개

이 튜토리얼에서는 Aspose.Note for Java 라이브러리를 사용하여 **OneNote 페이지를 PNG 이미지로 보는 방법**을 알아봅니다. **OneNote 페이지를 처리하는 방법**은 OneNote 관리 메모를 공유하거나, 의견에 삽입하거나, 이미지 처리 도구로 처리하고자 할 때 종종 필요합니다. 환경 설정부터 페이지를 보내십시오, 페이지 변환, 고품질 PNG 파일로 저장하는 전체 과정을 끝까지 안내합니다. 끝까지 따라오면 모든 Java 작곡에서 **OneNote 이미지로 작성**할 수 있습니다.

## 빠른 답변
- **어떤 라이브러리가 필요합니까?** Java용 Aspose.Note.
- **단일 페이지를 내보낼 수 있나요?** 예. 정확한 페이지를 타겟팅하려면 'setPageIndex'를 사용하세요.
- **지원되는 이미지 형식?** PNG, JPEG, GIF, BMP, TIFF(여기에는 PNG가 표시됨).
- **라이센스가 필요합니까?** 무료 평가판을 사용할 수 있습니다. 생산을 위해서는 라이센스가 필요합니다.
- **구현 시간은 얼마나 걸리나요?** 기본 변환의 경우 일반적으로 10분 미만이 소요됩니다.
- **.one을 png로 변환하는 방법은 무엇입니까?** `Document`를 사용하여 `.one` 파일을 로드하고 페이지 인덱스를 설정한 다음 `ImageSaveOptions`를 사용하여 저장합니다.

## 'OneNote 페이지 내보내기'란 무엇인가요?

OneNote 페이지를 내보낸다는 것은 `.one` 문서 안에 있는 특정 페이지를 관련인 이미지 파일(PNG)로 변환하는 것을 의미합니다. **OneNote 페이지를 이미지를 처리해야** 할 때, 공유, 삽입, 또는 이미지 기반 추가 분석을 위해 유용합니다.

## OneNote를 PNG로 변환하기 위해 Java용 Aspose.Note를 사용하는 이유는 무엇입니까?
- **Microsoft Office 종속성 없음** – Java를 실행하는 모든 플랫폼에서 작동합니다.
- **세밀한 제어** – `setPageIndex`를 통해 원하는 페이지를 선택할 수 있습니다.
- **고품질 출력** – PNG는 벡터 그래픽과 텍스트 선명도를 유지합니다.
- **일괄 처리 가능** – 대량 변환을 위해 페이지를 쉽게 순환할 수 있으므로 한 번에 여러 페이지에 대해 **onenote를 png로 변환**하는 것이 간단해집니다.

## 전제 조건

시작하기 전에 다음을 준비하세요:

1. **JDK(Java Development Kit)** – 버전 8 이상.
2. **Aspose.Note for Java** – 최신 JAR 파일을 [Aspose 웹사이트](https://releases.aspose.com/note/java/)에서 다운로드하세요.
3. **OneNote 문서**(`.one`) – 파일을 보내려고 합니다.

## 패키지 가져오기

먼저 필요한 Java 클래스를 가져옵니다:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.LoadOptions;
import com.aspose.note.SaveFormat;
```

이 import 문을 통해 문서 로드와 이미지 저장 옵션 설정 등 Aspose.Note 핵심 API에 접근할 수 있습니다.

## 단계별 가이드

### 1단계: OneNote 문서 불러오기

```java
// Load the document into Aspose.Note.
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", new LoadOptions());
```

`Document` 클래스를 사용해 디스크에 있는 OneNote 파일을 읽어옵니다. `LoadOptions` 객체를 통해 필요에 따라 로드 동작을 맞춤 설정할 수 있습니다. 이 단계는 **.one 파일을 png로 변환**하는 기반이 됩니다.

### 2단계: ImageSaveOptions 초기화

```java
// Initialize ImageSaveOptions object
ImageSaveOptions opts = new ImageSaveOptions(SaveFormat.Png);
```

`ImageSaveOptions`는 Aspose.Note에 출력 형식을 **PNG**로 지정하도록 알려줍니다. `SaveFormat`을 변경하면 JPEG, BMP 등 다른 포맷으로도 저장할 수 있습니다. 또한 DPI, 색 깊이 등 이미지‑특화 설정을 제어할 수 있습니다.

### 3단계: 페이지 색인 설정 (OneNote 페이지 변환 방법)

```java
// set page index
opts.setPageIndex(0);
```

`setPageIndex` 메서드는 내보낼 페이지를 선택합니다. 페이지 번호는 **0**부터 시작하므로 `0`은 첫 번째 페이지를 의미합니다. 이 값을 조정해 **다른 페이지를 내보내**거나, 여러 페이지를 순회하면서 **OneNote를 이미지로 저장**할 수 있습니다.

### 4단계: 문서를 PNG 파일로 저장 (OneNote 문서를 PNG로 저장)

```java
// Save the document as PNG.
oneFile.save(dataDir + "ConvertSpecificPageToPngImage_out.png", opts);
```

`save` 메서드를 호출하면 선택한 페이지가 PNG 파일로 디스크에 저장됩니다. 파일명 `ConvertSpecificPageToPngImage_out.png`는 예시이며, 원하는 이름으로 바꿀 수 있습니다. 이 최종 단계에서 **OneNote 페이지 이미지가 내보내져** 보고서, 웹 페이지, 혹은 추가 처리에 사용할 수 있게 됩니다.

## 일반적인 문제 및 팁

- **잘못된 페이지 인덱스** – 인덱스는 0부터 시작합니다. 빈 이미지가 표시되면 인덱스 값을 확인하세요.

- **Aspose.Note JAR 파일 누락** – JAR 파일이 클래스 경로에 있는지 확인하세요. 그렇지 않으면 `ClassNotFoundException` 오류가 발생합니다.

- **큰 페이지** – 페이지 크기가 매우 큰 경우, `OutOfMemoryError`를 방지하기 위해 JVM 힙 크기를 늘리는 것(`-Xmx`)을 고려하세요.

- **해상도 조정** – `save`를 호출하기 전에 `opts.setResolution(300)`(또는 필요한 DPI)을 사용하여 이미지 선명도를 높이세요.

## 자주 묻는 질문

### Q1: Aspose.Note for Java를 사용하여 여러 페이지를 한 번에 PNG 이미지로 변환할 수 있나요?

A1: 네, 문서의 페이지를 순회하면서 `opts.setPageIndex(i)`를 업데이트하고 각 페이지마다 `save`를 호출하면 됩니다.

### 질문 2: Aspose.Note for Java는 PNG 외에 다른 이미지 형식도 지원하나요?

답변 2: 네, 그렇습니다. `ImageSaveOptions`에서 `SaveFormat.Jpeg`, `SaveFormat.Gif`, `SaveFormat.Bmp`, 또는 `SaveFormat.Tiff`를 설정할 수 있습니다.

### 질문 3: Aspose.Note for Java의 무료 평가판을 사용할 수 있나요?

답변 3: 네, [웹사이트](https://releases.aspose.com/)에서 무료 평가판을 다운로드할 수 있습니다.

### 질문 4: Aspose.Note for Java 사용 중 문제가 발생하면 기술 지원을 받을 수 있나요?

답변 4: 네, Aspose 커뮤니티 포럼 [여기](https://forum.aspose.com/c/note/28)에서 지원을 받을 수 있습니다.

### 질문 5: Aspose.Note for Java 라이선스는 어디에서 구매할 수 있나요?

A5: [구매 페이지](https://purchase.aspose.com/buy)에서 라이선스를 구매할 수 있습니다.

### Q6: 이미지가 포함된 페이지를 어떻게 내보내나요?

A6: 포함된 이미지는 PNG 출력에 자동으로 렌더링되므로 추가 코드가 필요하지 않습니다.

### Q7: DPI 또는 이미지 해상도를 설정할 수 있나요?

A7: 네, `save`를 호출하기 전에 `opts.setResolution(int dpi)`를 사용하여 출력 품질을 제어할 수 있습니다.

---
**Last Updated:** 2026-02-05  
**Tested With:** Aspose.Note for Java 24.11 (latest)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}