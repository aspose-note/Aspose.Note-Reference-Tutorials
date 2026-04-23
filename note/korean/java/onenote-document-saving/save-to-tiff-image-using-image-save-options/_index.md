---
date: 2026-03-14
description: Java에서 TIFF JPEG 압축, TIFF PackBits 압축 또는 CCITT Group 3 Fax를 사용하여 OneNote
  문서를 TIFF 파일로 저장하는 방법을 배웁니다. Aspose.Note를 사용하여 이미지 품질, 파일 크기 및 색상 모드를 제어하세요.
linktitle: Save to TIFF Image Using TIFF JPEG Compression in OneNote
second_title: Aspose.Note Java API
title: OneNote에서 TIFF JPEG 압축을 사용하여 TIFF 이미지로 저장
url: /ko/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

/products/products-backtop-button >}}

All placeholders unchanged.

Now ensure markdown formatting preserved.

Let's construct final output.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote에서 TIFF JPEG 압축을 사용하여 TIFF 이미지 저장

## 소개

이 튜토리얼에서는 **TIFF JPEG 압축**을 사용하여 OneNote 문서를 TIFF 파일로 저장하는 방법과 다른 두 가지 인기 있는 압축 방법을 알아봅니다. 필요한 설정 과정을 안내하고, 필요한 Java 패키지를 가져오며, 각 압축 옵션에 대한 명확한 단계별 코드를 제공합니다. 끝까지 진행하면 **TIFF 이미지 품질**을 제어하고 파일 크기를 줄이며 팩스 스타일 출력용 흑백 TIFF도 생성할 수 있습니다.

## 빠른 답변
- **TIFF JPEG 압축이란?** 시각적 품질을 유지하면서 TIFF 파일 크기를 줄이는 손실 압축 방식입니다.  
- **변환을 처리하는 라이브러리는?** Aspose.Note for Java.  
- **라이선스가 필요합니까?** 테스트용으로는 무료 체험판을 사용할 수 있으며, 프로덕션에서는 라이선스가 필요합니다.  
- **이미지 품질을 변경할 수 있나요?** 예, `ImageSaveOptions`의 `quality` 속성을 설정하면 됩니다.  
- **배치 변환이 가능한가요?** 물론입니다 – 문서를 순회하면서 동일한 옵션을 적용하면 됩니다.

## TIFF JPEG 압축이란?

TIFF JPEG 압축은 이미지 데이터를 TIFF 컨테이너에 저장하면서 JPEG의 손실 알고리즘을 적용해 파일을 축소합니다. 특히 웹이나 아카이브 시나리오에서 **tiff 이미지 품질**과 작은 파일 크기의 균형이 필요할 때 이상적입니다.

## 다양한 TIFF 압축 유형을 사용하는 이유는?

- **JPEG** – 사진에 적합하며, 조정 가능한 품질을 제공합니다.  
- **PackBits** – 단순한 무손실 런-길이 인코딩으로, 넓은 균일 영역을 가진 그래픽에 유용합니다.  
- **CCITT Group 3 Fax** – 흑백 전용이며, 스캔 문서와 팩스 전송에 최적입니다.

올바른 압축 방식을 선택하면 애플리케이션에 필요한 시각적 충실도를 손상시키지 않으면서 저장 제한을 충족할 수 있습니다.

## Aspose.Note를 사용하여 OneNote를 TIFF로 변환

목표가 **OneNote를 TIFF로 변환**하는 것이라면, 아래 세 가지 방법이 가장 일반적인 시나리오를 다룹니다. 각 방법은 `.one` 파일을 로드하고 `ImageSaveOptions`를 구성한 뒤 결과를 `.tiff` 파일로 저장합니다.

## 전제 조건

- Java Development Kit (JDK) 설치  
- 프로젝트에 Aspose.Note for Java 라이브러리 추가 (Maven/Gradle 또는 수동 JAR).  
- Java 구문에 대한 기본적인 이해.

## 패키지 가져오기

먼저, 필요한 Aspose.Note 클래스를 Java 파일에 가져옵니다:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## 1단계: TIFF JPEG 압축을 사용하여 TIFF 저장

아래는 OneNote 파일을 로드하고 JPEG 압축을 사용하여 TIFF로 저장하는 전체 메서드입니다. `quality` 값(0‑100)을 조정하여 **tiff 이미지 품질**을 제어하세요.

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
- `setQuality(93)`(선택 사항)은 이미지 품질을 미세 조정합니다; 낮은 값은 파일을 더 작게 만듭니다.

### Java에서 JPEG 압축으로 TIFF 저장하는 방법
1. `dataDir`을 `.one` 파일이 들어 있는 폴더로 지정합니다.  
2. 메인 메서드나 서비스에서 `SaveToTiffUsingJpegCompression()`을 호출합니다.  
3. 생성된 `.tiff` 파일이 동일한 디렉터리에 나타납니다.

## TIFF PackBits 압축 개요

PackBits는 큰 단색 영역을 가진 이미지에 가장 적합한 무손실 압축 알고리즘입니다. 문서에서는 종종 **tiff packbits compression**이라고 언급됩니다.

## 2단계: PackBits 압축을 사용하여 TIFF 저장

무손실 옵션이 필요하다면, PackBits는 단색 그래픽에 잘 작동하는 간단한 런-길이 알고리즘입니다.

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

- `setTiffCompression(TiffCompression.PackBits)`는 압축 방식을 전환합니다.  
- PackBits는 무손실이므로 품질 설정이 필요하지 않습니다.

## 3단계: CCITT Group 3 Fax 압축(흑백 TIFF) 사용하여 TIFF 저장

팩스 스타일 문서에서는 종종 **흑백 TIFF**가 필요합니다. CCITT Group 3은 단색 이미지에 높은 압축률을 제공합니다.

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

- `setColorMode(ColorMode.BlackAndWhite)`는 단색 출력을 강제합니다.  
- `setTiffCompression(TiffCompression.Ccitt3)`는 팩스 전용 압축을 적용합니다.

## 일반적인 문제 및 팁

| Issue | Solution |
|-------|----------|
| **출력 파일이 예상보다 큽니다** | JPEG `quality` 값을 낮추거나 무손실이 허용된다면 PackBits로 전환해 보세요. |
| **색상이 흐릿하게 보입니다** | `ColorMode.BlackAndWhite`를 전체 색상이 필요할 때 실수로 설정하지 않았는지 확인하세요. |
| **지원되지 않는 이미지 형식 오류** | 최신 버전의 Aspose.Note를 사용하고 있는지 확인하세요; 오래된 빌드에서는 일부 압축 열거형이 없을 수 있습니다. |
| **런타임에서 LicenseException** | 유효한 Aspose.Note 라이선스를 설치하세요 (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`). |

## 자주 묻는 질문

**Q: 이러한 옵션으로 다른 문서 유형(예: PDF, DOCX)을 TIFF로 변환할 수 있나요?**  
A: 예. Aspose.Note는 OneNote 파일에 중점을 두지만, Aspose.PDF, Aspose.Words 및 기타 라이브러리도 해당 형식에 대해 유사한 `ImageSaveOptions`를 제공합니다.

**Q: TIFF JPEG 압축은 일반 JPEG 파일과 어떻게 다릅니까?**  
A: JPEG 알고리즘은 동일하지만 이미지 데이터가 TIFF 컨테이너 안에 들어 있어 여러 페이지와 풍부한 메타데이터를 포함할 수 있습니다.

**Q: 많은 `.one` 파일을 배치 처리할 수 있나요?**  
A: 물론입니다. 디렉터리를 순회하면서 각 파일에 대해 세 가지 방법 중 하나를 호출하고 결과 TIFF를 수집하면 됩니다.

**Q: 출력 TIFF의 DPI/해상도를 제어할 수 있나요?**  
A: 예. 저장하기 전에 `options.setResolution(int dpi)`를 사용하세요.

**Q: Aspose.Note가 비동기 처리를 지원하나요?**  
A: API 자체는 동기식이지만, Java의 `CompletableFuture`나 스레드 풀로 호출을 감싸면 병렬 실행이 가능합니다.

## 결론

이제 JPEG, PackBits 또는 CCITT Group 3 Fax 압축을 사용하여 OneNote 문서를 TIFF 파일로 저장할 수 있는 완전한 **java tiff conversion** 툴킷을 갖추었습니다. 품질, 색상 모드 및 해상도를 조정하여 특정 **tiff 이미지 품질** 요구 사항을 충족하고, 이러한 메서드를 배치 워크플로에 통합하여 생산성을 극대화하세요.

---

**마지막 업데이트:** 2026-03-14  
**테스트 환경:** Aspose.Note for Java 23.12 (latest at time of writing)  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}