---
date: 2025-12-17
description: Java에서 TIFF JPEG 압축, PackBits 또는 CCITT Group 3 Fax를 사용하여 OneNote 문서를
  TIFF 파일로 저장하는 방법을 배웁니다. Aspose.Note를 사용하여 이미지 품질, 파일 크기 및 색상 모드를 제어하세요.
linktitle: Save to TIFF Image Using TIFF JPEG Compression in OneNote
second_title: Aspose.Note Java API
title: OneNote에서 TIFF JPEG 압축을 사용하여 TIFF 이미지 저장
url: /ko/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# TIFF JPEG 압축을 사용하여 OneNote에서 TIFF 이미지 저장

## 소개

이 튜토리얼에서는 **TIFF JPEG 압축을 사용하여 OneNote 문서를 TIFF 파일로 저장하는 방법**과 두 가지 다른 일반적인 압축 방식을 소개합니다. 필요한 설정 과정을 살펴보고, 필요한 Java 패키지를 가져오며, 각 압축 옵션에 대한 명확한 단계별 코드를 제공합니다. 튜토리얼을 마치면 **TIFF 이미지 품질**을 제어하고 파일 크기를 줄이며, 팩스 스타일 출력용 흑백 TIFF도 생성할 수 있게 됩니다.

## 빠른 답변
- **TIFF JPEG 압축이란?** 시각적 품질을 유지하면서 TIFF 파일 크기를 줄이는 손실 압축 방식입니다.  
- **변환을 담당하는 라이브러리는?** Aspose.Note for Java.  
- **라이선스가 필요한가요?** 테스트용 무료 체험판을 사용할 수 있지만, 프로덕션에서는 라이선스가 필요합니다.  
- **이미지 품질을 변경할 수 있나요?** 예, `ImageSaveOptions`의 `quality` 속성을 설정하면 됩니다.  
- **배치 변환이 가능한가요?** 물론입니다 – 문서를 반복 처리하고 동일한 옵션을 적용하면 됩니다.

## TIFF JPEG 압축이란?
TIFF JPEG 압축은 이미지 데이터를 TIFF 컨테이너에 저장하면서 JPEG의 손실 알고리즘을 적용해 파일을 축소합니다. 웹이나 아카이브 시나리오처럼 **tiff 이미지 품질**과 작은 파일 크기의 균형이 필요할 때 이상적입니다.

## 다양한 TIFF 압축 유형을 사용하는 이유
- **JPEG** – 사진에 적합하며 품질을 조정할 수 있습니다.  
- **PackBits** – 단순한 무손실 런‑길이 인코딩; 넓은 균일 영역을 가진 그래픽에 유용합니다.  
- **CCITT Group 3 Fax** – 흑백 전용; 스캔 문서와 팩스 전송에 최적입니다.  

적절한 압축 방식을 선택하면 저장 용량 제한을 만족하면서도 애플리케이션에 필요한 시각적 충실도를 유지할 수 있습니다.

## 전제 조건

- Java Development Kit (JDK) 설치 완료.  
- 프로젝트에 Aspose.Note for Java 라이브러리 추가 (Maven/Gradle 또는 수동 JAR).  
- Java 문법에 대한 기본적인 이해.

## 패키지 가져오기

먼저, 필요한 Aspose.Note 클래스를 Java 파일에 포함합니다:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## 단계 1: TIFF JPEG 압축을 사용하여 TIFF 저장

아래는 OneNote 파일을 로드하고 JPEG 압축을 적용해 TIFF로 저장하는 전체 메서드입니다. `quality` 값(0‑100)을 조정하여 **tiff 이미지 품질**을 제어하세요.

```java
public static void SaveToTiffUsingJpegCompression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.Jpeg);
    options.setQuality(93);

    oneFile.save(Paths.get(dataDir,"SaveToTiffUsingJpegCompression.tiff").toString(), options);
}
```

**설명**

- `ImageSaveOptions`는 Aspose.Note에 TIFF 파일을 출력하도록 지시합니다.  
- `setTiffCompression(TiffCompression.Jpeg)`은 JPEG 압축을 선택합니다.  
- `setQuality(93)`(선택 사항)은 이미지 품질을 미세 조정합니다; 값이 낮을수록 파일이 작아집니다.

### Java에서 JPEG 압축으로 TIFF 저장하는 방법
1. `dataDir`을 `.one` 파일이 들어 있는 폴더 경로로 지정합니다.  
2. 메인 메서드 또는 서비스에서 `SaveToTiffUsingJpegCompression()`을 호출합니다.  
3. 결과 `.tiff` 파일이 동일한 디렉터리에 생성됩니다.

## 단계 2: PackBits 압축을 사용하여 TIFF 저장

무손실 옵션이 필요하다면 PackBits는 단순한 런‑길이 알고리즘으로, 단색 영역이 많은 그래픽에 적합합니다.

```java
public static void SaveToTiffUsingPackBitsCompression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.PackBits);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingPackBitsCompression.tiff").toString(), options);
}
```

**설명**

- `setTiffCompression(TiffCompression.PackBits)`가 압축 방식을 전환합니다.  
- PackBits는 무손실이므로 품질 설정이 필요하지 않습니다.

## 단계 3: CCITT Group 3 Fax 압축(흑백 TIFF) 사용하여 TIFF 저장

팩스 스타일 문서에는 **흑백 TIFF**가 흔히 필요합니다. CCITT Group 3은 단색 이미지에 높은 압축률을 제공합니다.

```java
public static void SaveToTiffUsingCcitt3Compression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setColorMode(ColorMode.BlackAndWhite);
    options.setTiffCompression(TiffCompression.Ccitt3);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingCcitt3Compression.tiff").toString(), options);
}
```

**설명**

- `setColorMode(ColorMode.BlackAndWhite)`가 흑백 출력을 강제합니다.  
- `setTiffCompression(TiffCompression.Cc3)`이 팩스 전용 압축을 적용합니다.

## 일반적인 문제 및 팁

| 문제 | 해결책 |
|-------|----------|
| **출력 파일이 예상보다 큼** | JPEG `quality` 값을 낮추거나, 무손실이 가능하다면 PackBits로 전환해 보세요. |
| **색상이 흐릿하게 나옴** | 컬러가 필요한 경우 `ColorMode.BlackAndWhite`가 설정되지 않았는지 확인하세요. |
| **지원되지 않는 이미지 형식 오류** | 최신 버전의 Aspose.Note를 사용하고 있는지 확인하세요; 오래된 빌드에서는 일부 압축 열거형이 없을 수 있습니다. |
| **런타임에 LicenseException 발생** | 유효한 Aspose.Note 라이선스를 설치합니다 (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`). |

## 자주 묻는 질문

**Q: 다른 문서 형식(PDF, DOCX 등)도 이 옵션으로 TIFF로 변환할 수 있나요?**  
A: 예. Aspose.Note는 OneNote 파일에 중점을 두지만, Aspose의 다른 라이브러리(PDF, Words 등)에서도 각 형식에 맞는 `ImageSaveOptions`를 제공하여 유사하게 변환할 수 있습니다.

**Q: TIFF JPEG 압축은 일반 JPEG 파일과 어떻게 다른가요?**  
A: 이미지 데이터가 TIFF 컨테이너 안에 저장되어 메타데이터를 보존하고 다중 페이지를 지원하지만, 압축 알고리즘 자체는 JPEG과 동일합니다.

**Q: 많은 `.one` 파일을 배치 처리할 수 있나요?**  
A: 물론 가능합니다. 폴더를 순회하면서 파일당 원하는 메서드 중 하나를 호출하고 결과 TIFF를 수집하면 됩니다.

**Q: 출력 TIFF의 DPI/해상도를 제어할 수 있나요?**  
A: 예. 저장 전에 `options.setResolution(int dpi)`를 사용하면 됩니다.

**Q: Aspose.Note가 비동기 처리를 지원하나요?**  
A: API 자체는 동기식이지만, Java의 `CompletableFuture`나 스레드 풀을 활용해 호출을 병렬화할 수 있습니다.

## 결론

이제 **java tiff conversion** 툴킷을 완전히 갖추었습니다. JPEG, PackBits, CCITT Group 3 Fax 압축을 사용해 OneNote 문서를 TIFF 파일로 저장할 수 있습니다. 품질, 색상 모드, 해상도를 조정해 **tiff 이미지 품질** 요구 사항을 만족하고, 배치 워크플로에 통합해 생산성을 극대화하세요.

---

**마지막 업데이트:** 2025-12-17  
**테스트 환경:** Aspose.Note for Java 23.12 (작성 시 최신 버전)  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}