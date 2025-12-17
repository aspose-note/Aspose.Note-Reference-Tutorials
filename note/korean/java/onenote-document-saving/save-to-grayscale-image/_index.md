---
date: 2025-12-17
description: Aspose.Note for Java를 사용하여 문서를 그레이스케일 PNG 이미지로 저장해 OneNote를 내보내는 방법을
  배웁니다. OneNote 문서를 로드하고 그레이스케일 이미지를 만드는 단계가 포함됩니다.
linktitle: How to Export OneNote as Grayscale Image – Aspose.Note
second_title: Aspose.Note Java API
title: OneNote를 그레이스케일 이미지로 내보내는 방법 – Aspose.Note
url: /ko/java/onenote-document-saving/save-to-grayscale-image/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote에서 그레이스케일 이미지로 저장 - Aspose.Note

## 소개

이 튜토리얼에서는 Aspose.Note for Java를 사용하여 문서를 그레이스케일 이미지로 저장함으로써 **OneNote 내보내기 방법**을 보여드립니다. 그레이스케일 이미지는 회색 음영만 포함하는 단색 사진으로, 인쇄, 보관 또는 파일 크기 감소에 유용합니다. OneNote 문서를 로드하고, 저장 옵션을 **그레이스케일 이미지 생성**으로 구성한 다음, 최종적으로 **문서를 PNG로 저장**하는 과정을 단계별로 안내합니다.

## 빠른 답변
- **“OneNote 내보내기 방법”이란 무엇인가요?** 프로그램matically OneNote 파일을 이미지와 같은 다른 형식으로 변환하는 것을 의미합니다.  
- **그레이스케일 출력에 가장 적합한 형식은 무엇인가요?** PNG는 무손실 품질을 유지하고 그레이스케일 색상 모드를 지원하기 때문에 적합합니다.  
- **라이선스가 필요합니까?** 프로덕션 사용을 위해서는 유효한 Aspose.Note 라이선스가 필요하며, 테스트용 임시 체험 라이선스를 사용할 수 있습니다.  
- **필요한 Java 버전은 무엇인가요?** Java 8 이상을 권장합니다.  
- **이미지 크기를 변경할 수 있나요?** 예, 저장하기 전에 `ImageSaveOptions`의 `Resolution` 또는 `PageSize`와 같은 속성을 조정할 수 있습니다.

## “OneNote 내보내기 방법”이란?

OneNote를 내보낸다는 것은 OneNote `.one` 파일을 프로그램matically PDF, HTML 또는 이미지와 같은 다른 형태로 변환하는 것을 의미합니다. 이 가이드에서는 문서화 또는 인쇄 워크플로우에서 흔히 요구되는 **그레이스케일 PNG** 이미지로 내보내는 데 중점을 둡니다.

## 왜 OneNote를 그레이스케일 이미지로 내보내나요?

- **파일 크기 감소** – 그레이스케일 PNG는 일반적으로 전체 색상 이미지보다 작습니다.  
- **가독성 향상** – 인쇄된 보고서에서는 그레이스케일이 더 선명한 대비를 제공합니다.  
- **호환성** – PNG는 브라우저, 편집기 및 모바일 기기 전반에서 널리 지원됩니다.

## 사전 요구 사항

시작하기 전에 다음이 준비되어 있는지 확인하십시오:

1. 시스템에 Java Development Kit (JDK)가 설치되어 있어야 합니다.  
2. Aspose.Note for Java 라이브러리. [여기](https://releases.aspose.com/note/java/)에서 다운로드할 수 있습니다.  
3. Java 프로그래밍에 대한 기본 이해.

## 패키지 가져오기

시작하려면 필요한 패키지를 가져오세요:

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## 단계 1: OneNote 문서 로드

먼저, **OneNote 문서를** Aspose.Note에 **로드**합니다. `"Your Document Directory"`를 로컬 폴더 경로로, `"Aspose.one"`을 OneNote 파일 이름으로 바꾸세요.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## 단계 2: 출력 경로 및 옵션 설정

그레이스케일 이미지의 출력 경로를 정의하고 저장 옵션을 지정합니다. `ColorMode`를 `GrayScale`로 설정하고 **문서를 PNG 형식으로 저장**을 사용합니다.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## 단계 3: 문서 저장

마지막으로, 구성된 옵션을 사용하여 문서를 그레이스케일 PNG 이미지로 저장합니다.

```java
oneFile.save(dataDir, options);
```

## 일반적인 문제 및 해결책
- **FileNotFoundException** – `dataDir`가 올바른 폴더를 가리키고 `.one` 파일이 존재하는지 확인하십시오.  
- **LicenseException** – `save`를 호출하기 전에 유효한 Aspose.Note 라이선스를 적용했는지 확인하십시오.  
- **저해상도 출력** – 필요에 따라 `options.setResolution(300)`을 조정하여 DPI를 높이세요.

## 자주 묻는 질문

**Q1: 그레이스케일 이미지를 다른 형식으로 저장할 수 있나요?**  
A1: 예, `ImageSaveOptions` 생성자에서 `SaveFormat` 매개변수를 `Jpeg`, `Bmp` 등으로 변경하면 됩니다.

**Q2: Aspose.Note가 모든 버전의 OneNote 문서와 호환되나요?**  
A2: Aspose.Note는 Microsoft OneNote 2010 및 이후 버전을 지원합니다.

**Q3: Aspose.Note를 사용하려면 라이선스가 필요합니까?**  
A3: 프로덕션 사용을 위해서는 유효한 라이선스가 필요하지만, 평가용으로 임시 체험 라이선스를 받을 수 있습니다.

**Q4: 이미지를 저장하기 전에 문서의 다른 부분을 조작할 수 있나요?**  
A4: 물론입니다! Aspose.Note는 섹션, 페이지 및 콘텐츠를 편집하는 포괄적인 API를 제공하여 내보내기 전에 수정할 수 있습니다.

**Q5: 문제가 발생했을 때 어디에서 지원을 받을 수 있나요?**  
A5: Aspose.Note 포럼에서 지원을 받을 수 있습니다. [여기](https://forum.aspose.com/c/note/28).

## 결론

이제 OneNote 파일을 로드하고, 저장 옵션을 **그레이스케일 이미지 생성**으로 구성한 뒤, **문서를 PNG로 저장**함으로써 **OneNote 내보내기 방법**을 익혔습니다. 이 기술은 OneNote 노트북에서 가볍고 인쇄 준비가 된 시각 자료를 생성하는 데 유용합니다. 프로젝트 요구에 맞게 다른 `ColorMode` 설정이나 이미지 형식을 자유롭게 실험해 보세요.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**마지막 업데이트:** 2025-12-17  
**테스트 환경:** Aspose.Note 24.12 for Java  
**작성자:** Aspose