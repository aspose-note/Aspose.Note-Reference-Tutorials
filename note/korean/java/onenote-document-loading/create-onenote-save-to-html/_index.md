---
date: 2025-12-02
description: Aspose.Note for Java를 사용하여 OneNote를 HTML로 저장하면서 글꼴을 내보내는 방법을 배웁니다. 이
  가이드는 프로그래밍 방식으로 OneNote를 생성하고 글꼴, CSS 및 이미지를 삽입하는 방법을 보여줍니다.
language: ko
linktitle: How to Export Fonts When Saving OneNote as HTML – Java
second_title: Aspose.Note Java API
title: OneNote를 HTML로 저장할 때 글꼴 내보내는 방법 – Java
url: /java/onenote-document-loading/create-onenote-save-to-html/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote를 HTML로 저장할 때 글꼴 내보내는 방법 – Java

## 소개

이 튜토리얼에서는 Aspose.Note for Java를 사용하여 **OneNote를 HTML로 저장할 때 글꼴을 내보내는 방법**을 알아봅니다. 프로그래밍 방식으로 OneNote 문서를 생성하고, HTML 저장 옵션을 구성하며, 필요한 글꼴 파일을 포함시켜 결과 HTML이 원본 OneNote 페이지와 정확히 동일하게 보이도록 하는 과정을 단계별로 안내합니다. 이 방법은 OneNote 콘텐츠의 시각적 일관성을 웹 친화적인 형식으로 보존해야 할 때 완벽합니다.

## 빠른 답변
- **어떤 라이브러리가 내보내기를 처리합니까?** Aspose.Note for Java  
- **HTML에 글꼴을 포함시킬 수 있나요?** 예 – `ExportFonts`를 `ExportEmbedded`로 설정  
- **프로덕션에 라이선스가 필요합니까?** 상업적 사용을 위해서는 유효한 Aspose.Note 라이선스가 필요합니다  
- **지원되는 Java 버전은?** Java 8 이상  
- **리소스를 별도 파일로 저장할 수 있나요?** 물론 – `ResourceExportType`을 적절히 구성하면 됩니다  

## OneNote HTML 변환 맥락에서 “글꼴 내보내기”란 무엇인가요?

OneNote 노트북을 HTML로 변환하면 시각적 모양이 CSS, 이미지 및 특히 원본 페이지에서 사용된 글꼴에 의존합니다. **글꼴 내보내기**란 글꼴 파일(TTF 등)을 HTML 패키지에 직접 포함시켜 브라우저가 사용자의 로컬에 해당 글꼴이 설치되어 있지 않더라도 OneNote와 동일하게 텍스트를 렌더링하도록 하는 것을 의미합니다.

## 왜 OneNote를 프로그래밍 방식으로 생성하고 HTML로 저장하나요?

- **자동화:** OneNote에서 보고서, 문서, 혹은 지식베이스 기사를 수동 복사‑붙여넣기 없이 생성합니다.  
- **일관성:** 레이아웃, 스타일링 및 사용자 정의 글꼴을 장치 간에 유지합니다.  
- **이식성:** HTML은 보편적으로 볼 수 있어 OneNote 클라이언트가 필요 없습니다.  

## 전제 조건

1. Java Development Kit (JDK) 8 이상 설치  
2. Aspose.Note for Java 라이브러리 – [here](https://releases.aspose.com/note/java/)에서 다운로드  
3. 로드할 샘플 OneNote 파일(`.one`) 또는 프로그래밍 방식으로 새 파일을 생성할 수 있습니다.  

## 패키지 가져오기

먼저 Java 프로젝트에 필요한 클래스를 가져옵니다:

```java
import java.io.ByteArrayOutputStream;
import java.io.File;
import java.io.FileOutputStream;
import java.io.IOException;
import java.io.OutputStream;
import java.io.OutputStreamWriter;
import java.nio.file.Paths;
import com.aspose.note.CssSavingArgs;
import com.aspose.note.Document;
import com.aspose.note.FontFaceType;
import com.aspose.note.FontSavingArgs;
import com.aspose.note.HtmlSaveOptions;
import com.aspose.note.ICssSavingCallback;
import com.aspose.note.IFontSavingCallback;
import com.aspose.note.IImageSavingCallback;
import com.aspose.note.ImageSavingArgs;
import com.aspose.note.ResourceExportType;
```

## OneNote를 HTML로 저장하면서 글꼴을 내보내는 방법

아래 단계별 가이드는 **글꼴을 내보내는 방법**과 기타 리소스를 보여줍니다.

### 단계 1: OneNote 문서를 프로그래밍 방식으로 생성  

```java
Document document = new Document("Path_to_your_sample_one_file");
```

이 코드는 기존 `.one` 파일을 로드합니다. **프로그래밍 방식으로 OneNote를 생성**해야 하는 경우, 새 `Document` 객체를 인스턴스화하고 API를 통해 섹션/페이지를 추가할 수 있습니다(여기서는 글꼴 내보내기에 집중하기 위해 생략).

### 단계 2: 임베디드 글꼴로 메모리 스트림에 저장  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

- `setExportFonts(ResourceExportType.ExportEmbedded)`는 Aspose.Note에 **글꼴을** HTML 패키지에 직접 **내보내**도록 지시합니다.  
- `setFontFaceTypes(FontFaceType.Ttf)`는 브라우저 호환성이 넓은 TrueType 글꼴을 사용하도록 보장합니다.

### 단계 3: 별도 리소스 파일로 HTML 저장 (여전히 글꼴 내보내기)  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

CSS와 이미지가 임베드되어 있더라도, 캐시 효율성을 위해 별도 파일을 원한다면 `ResourceExportType`을 `ExportExternal`로 변경할 수 있습니다. 핵심인 **글꼴 내보내기**는 그대로 유지됩니다.

### 단계 4: 콜백을 사용하여 각 리소스 저장 위치 제어  

```java
Document document = new Document("Path_to_your_sample_one_file");

UserSavingCallbacks savingCallbacks = new UserSavingCallbacks();
savingCallbacks.setRootFolder("documentFolder");
savingCallbacks.setCssFolder("css");
savingCallbacks.setKeepCssStreamOpened(true);
savingCallbacks.setImagesFolder("images");
savingCallbacks.setFontsFolder("fonts");

HtmlSaveOptions options = new HtmlSaveOptions();
options.setFontFaceTypes(FontFaceType.Ttf);
options.setCssSavingCallback(savingCallbacks);
options.setImageSavingCallback(savingCallbacks);
options.setFontSavingCallback(savingCallbacks);
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);

File dir = new File(savingCallbacks.getRootFolder());
if (!dir.exists()) {
    dir.mkdir();
}

document.save(Paths.get(savingCallbacks.getRootFolder(), "document.html").toString(), options);
```

`UserSavingCallbacks` 클래스(`ICssSavingCallback`, `IImageSavingCallback`, `IFontSavingCallback` 구현 필요)는 폴더 구조를 완전히 제어할 수 있게 해 주며, 글꼴을 전용 `fonts` 디렉터리에 보관하면서도 **글꼴을 올바르게 내보내**도록 합니다.

## 일반적인 문제 및 팁

- **출력에 글꼴이 누락된 경우:** `setExportFonts(ResourceExportType.ExportEmbedded)`가 설정되어 있고 원본 OneNote 파일이 실제로 임베디드 글꼴을 사용하는지 확인하십시오.  
- **대용량 HTML 파일:** 글꼴을 임베드하면 크기가 증가할 수 있습니다. 대역폭이 문제라면 `ExportFonts`를 `ExportExternal`로 전환하고 CDN에 글꼴을 호스팅하십시오.  
- **콜백 구현 오류:** 콜백 클래스가 스트림을 올바르게 쓰고 리소스를 닫아 파일 손상을 방지하도록 하십시오.  

## 자주 묻는 질문

**Q: 한 번에 여러 OneNote 문서를 HTML로 변환할 수 있나요?**  
A: 예, 각 `Document` 인스턴스를 순회하면서 동일한 `HtmlSaveOptions`를 적용하면 됩니다.  

**Q: Aspose.Note for Java가 HTML 외에 다른 출력 형식을 지원하나요?**  
A: 물론입니다. 적절한 저장 옵션을 사용하면 PDF, DOCX, PNG, JPEG 등 다양한 형식으로 내보낼 수 있습니다.  

**Q: Aspose.Note for Java용 체험판이 있나요?**  
A: 예, [here](https://releases.aspose.com/)에서 무료 체험판을 다운로드하십시오.  

**Q: Aspose.Note for Java에 대한 지원은 어디서 받을 수 있나요?**  
A: 커뮤니티 및 공식 지원을 위해 [Aspose.Note forum](https://forum.aspose.com/c/note/28)을 방문하십시오.  

**Q: Aspose.Note for Java 라이선스는 어떻게 구매하나요?**  
A: 라이선스는 [Aspose website](https://purchase.aspose.com/buy)에서 구매할 수 있습니다.  

## 결론

이제 Aspose.Note for Java를 사용하여 **OneNote를 HTML로 저장하면서 글꼴을 내보내는 방법**을 알게 되었습니다. `HtmlSaveOptions`를 구성하고 필요에 따라 콜백을 활용하면 웹에 제공할 때도 OneNote 페이지의 정확한 모양—맞춤 글꼴 포함—을 유지할 수 있습니다. 프로젝트의 성능 및 저장 요구에 맞게 다양한 `ResourceExportType` 설정을 실험해 보세요.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2025-12-02  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose  

---