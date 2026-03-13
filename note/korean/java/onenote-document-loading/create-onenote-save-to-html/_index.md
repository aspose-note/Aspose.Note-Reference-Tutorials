---
date: 2026-02-07
description: Aspose.Note for Java를 사용하여 OneNote를 HTML로 저장하면서 글꼴을 내보내는 방법을 배웁니다. 이
  가이드는 프로그래밍 방식으로 OneNote를 생성하고 글꼴, CSS 및 이미지를 삽입하는 방법을 보여줍니다.
linktitle: How to Export Fonts When Saving OneNote as HTML – Java
second_title: Aspose.Note Java API
title: OneNote를 HTML로 저장할 때 글꼴을 내보내는 방법 – Java
url: /ko/java/onenote-document-loading/create-onenote-save-to-html/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote를 HTML로 저장할 때 글꼴 내보내는 방법 – Java

## 소개

이 튜토리얼에서는 Aspose.Note for Java를 사용하여 **OneNote를 HTML로 저장할 때 글꼴을 내보내는 방법**을 알아봅니다. OneNote 문서를 프로그래밍 방식으로 생성하고, HTML 저장 옵션을 구성하며, 필요한 글꼴 파일을 임베드하여 결과 HTML이 원본 OneNote 페이지와 정확히 동일하게 보이도록 하는 과정을 단계별로 안내합니다. 웹 친화적인 형식으로 OneNote 콘텐츠의 시각적 충실도를 유지해야 할 때 이 방법이 최적입니다.

## 빠른 답변
- **어떤 라이브러리가 내보내기를 담당하나요?** Aspose.Note for Java  
- **HTML에 글꼴을 임베드할 수 있나요?** 예 – `ExportFonts`를 `ExportEmbedded`로 설정하면 됩니다.  
- **프로덕션에서 라이선스가 필요합니까?** 상업적 사용을 위해서는 유효한 Aspose.Note 라이선스가 필요합니다.  
- **지원되는 Java 버전은 무엇인가요?** Java 8 이상  
- **리소스를 별도 파일로 저장할 수 있나요?** 물론 – `ResourceExportType`을 적절히 구성하면 됩니다.  

## “글꼴 내보내기”가 OneNote HTML 변환에서 의미하는 바는 무엇인가요?

OneNote 노트북을 HTML로 변환할 때 시각적 모습은 CSS, 이미지, 그리고 특히 원본 페이지에서 사용된 글꼴에 따라 달라집니다. **글꼴 내보내기**란 글꼴 파일(TTF 등)을 HTML 패키지에 직접 포함시켜, 사용자가 해당 글꼴을 로컬에 설치하지 않아도 브라우저가 OneNote와 동일하게 텍스트를 렌더링하도록 하는 것을 의미합니다.

## 왜 OneNote를 프로그래밍 방식으로 생성하고 HTML로 저장하나요?

- **자동화:** OneNote에서 수동 복사·붙여넣기 없이 보고서, 문서, 지식베이스 기사를 생성합니다.  
- **일관성:** 레이아웃, 스타일, 사용자 정의 글꼴을 기기 간에 동일하게 유지합니다.  
- **이식성:** HTML은 어디서든 볼 수 있어 OneNote 클라이언트가 필요 없습니다.  

## 전제 조건

1. Java Development Kit (JDK) 8 이상 설치  
2. Aspose.Note for Java 라이브러리 – [여기](https://releases.aspose.com/note/java/)에서 다운로드  
3. 로드할 샘플 OneNote 파일(`.one`) 또는 프로그래밍 방식으로 새 파일을 생성할 수 있음  

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

아래 단계별 가이드를 통해 **글꼴을 내보내는 방법**과 기타 리소스 처리 방법을 확인하세요.

### 단계 1: OneNote 문서를 프로그래밍 방식으로 생성  

```java
Document document = new Document("Path_to_your_sample_one_file");
```

이 코드는 기존 `.one` 파일을 로드합니다. **프로그래밍 방식으로 OneNote를 생성**하려면 `Document` 객체를 새로 인스턴스화하고 API를 통해 섹션·페이지를 추가하면 됩니다(여기서는 글꼴 내보내기에 집중하기 위해 생략).

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

- `setExportFonts(ResourceExportType.ExportEmbedded)`은 Aspose.Note가 **글꼴을 직접 HTML 패키지에 내보내도록** 지정합니다.  
- `setFontFaceTypes(FontFaceType.Ttf)`는 브라우저 호환성이 높은 TrueType 글꼴을 사용하도록 보장합니다.

### 단계 3: 별도 리소스 파일로 HTML 저장 (글꼴 내보내기 유지)

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

CSS와 이미지는 임베드되지만, `ResourceExportType`을 `ExportExternal`으로 변경하면 캐싱을 위해 파일을 별도로 저장할 수 있습니다. 핵심인 **글꼴 내보내기**는 그대로 유지됩니다.

### 단계 4: 콜백을 사용해 각 리소스 저장 위치 제어  

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

`UserSavingCallbacks` 클래스( `ICssSavingCallback`, `IImageSavingCallback`, `IFontSavingCallback` 구현 필요)를 활용하면 폴더 구조를 자유롭게 지정할 수 있습니다. 이를 통해 글꼴을 전용 `fonts` 디렉터리에 저장하면서도 **글꼴을 올바르게 내보내기**할 수 있습니다.

## OneNote를 HTML로 변환할 때 사용자 정의 글꼴을 임베드하는 방법

사용자 정의 글꼴을 임베드하면 해당 글꼴이 설치되지 않은 장치에서도 HTML 렌더링이 원본 OneNote 레이아웃과 일치합니다. `ExportEmbedded`와 `FontFaceType.Ttf`를 함께 사용하면 TrueType 파일이 Base‑64 인코딩되어 생성된 CSS에 직접 삽입되므로 외부 글꼴 호스팅이 필요 없습니다.

## ResourceExportType을 사용해 리소스 내보내기 제어

`ResourceExportType`을 통해 CSS, 이미지, 글꼴을 **HTML 파일 내부에**(`ExportEmbedded`) 저장하거나 **외부 파일**(`ExportExternal`)로 저장할지 선택할 수 있습니다. 단일 파일 솔루션이 필요하면 `ExportEmbedded`를, 대용량 자산에 대해 브라우저 캐싱을 활용하고 싶다면 `ExportExternal`을 선택하세요.

## HTML 내보내기를 위해 OneNote를 프로그래밍 방식으로 생성하기

처음부터 코드를 사용해 OneNote 문서를 만들고 섹션·페이지·리치 텍스트를 추가한 뒤 앞서 소개한 `HtmlSaveOptions`를 적용하면 됩니다. 이렇게 하면 데이터 생성부터 스타일이 적용된 HTML 출력(사용자 정의 글꼴 임베드 포함)까지 전 과정을 자동화할 수 있습니다.

## 일반적인 문제 및 팁

- **출력에 글꼴이 누락됨:** `setExportFonts(ResourceExportType.ExportEmbedded)`가 설정되어 있는지, 원본 OneNote 파일에 임베드된 글꼴이 실제로 사용되었는지 확인하세요.  
- **HTML 파일 크기 증가:** 글꼴을 임베드하면 파일 크기가 커집니다. 대역폭이 우려된다면 `ExportFonts`를 `ExportExternal`로 전환하고 CDN에 글꼴을 호스팅하세요.  
- **콜백 구현 오류:** 콜백 클래스가 스트림을 올바르게 쓰고 리소스를 닫는지 확인하여 파일 손상을 방지하세요.  

## 자주 묻는 질문

**Q: 여러 OneNote 문서를 한 번에 HTML로 변환할 수 있나요?**  
A: 예, 각 `Document` 인스턴스를 순회하면서 동일한 `HtmlSaveOptions`를 적용하면 됩니다.  

**Q: Aspose.Note for Java가 HTML 외에 다른 출력 형식을 지원하나요?**  
A: 물론입니다. PDF, DOCX, PNG, JPEG 등 다양한 포맷으로 저장할 수 있는 전용 저장 옵션이 제공됩니다.  

**Q: Aspose.Note for Java의 체험판을 받을 수 있나요?**  
A: 예, [여기](https://releases.aspose.com/)에서 무료 체험판을 다운로드하세요.  

**Q: Aspose.Note for Java에 대한 지원은 어디서 받을 수 있나요?**  
A: [Aspose.Note 포럼](https://forum.aspose.com/c/note/28)에서 커뮤니티와 공식 지원을 받을 수 있습니다.  

**Q: Aspose.Note for Java 라이선스는 어떻게 구매하나요?**  
A: 라이선스는 [Aspose 웹사이트](https://purchase.aspose.com/buy)에서 구매할 수 있습니다.  

## 결론

이제 Aspose.Note for Java를 사용해 **OneNote를 HTML로 저장하면서 글꼴을 내보내는 방법**을 알게 되었습니다. `HtmlSaveOptions`를 적절히 구성하고 필요에 따라 콜백을 활용하면 OneNote 페이지의 정확한 모양—사용자 정의 글꼴 포함—을 웹에 그대로 전달할 수 있습니다. 프로젝트의 성능 및 저장 요구에 맞게 `ResourceExportType` 설정을 자유롭게 실험해 보세요.

---

**Last Updated:** 2026-02-07  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}