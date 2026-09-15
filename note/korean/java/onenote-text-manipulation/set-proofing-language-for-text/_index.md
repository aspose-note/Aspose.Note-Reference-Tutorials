---
date: 2026-03-29
description: Aspose.Note for Java를 사용하여 OneNote에서 텍스트의 언어를 설정하는 방법을 배워보세요. 이 단계별 가이드는
  OneNote 문서를 만들고, 텍스트 언어를 변경하며, OneNote 파일을 효율적으로 저장하는 방법을 보여줍니다.
linktitle: Set Proofing Language for Text in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: OneNote에서 텍스트 언어 설정 방법 – Aspose.Note
url: /ko/java/onenote-text-manipulation/set-proofing-language-for-text/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote에서 텍스트 언어 설정 방법 – Aspose.Note

## 소개
OneNote 노트북 안의 특정 텍스트에 **how to set language**를 설정해야 한다면, Aspose.Note for Java가 이를 간단하게 만들어 줍니다. 이 튜토리얼에서는 OneNote 문서를 생성하고, 개별 단어나 구절의 텍스트 언어를 변경한 뒤, 올바른 교정 언어가 적용된 OneNote 파일을 저장하는 방법을 배웁니다. 끝까지 읽으면 언어 설정이 맞춤법 검사와 현지화에 왜 중요한지 이해하고, 바로 실행할 수 있는 코드 샘플을 얻게 됩니다.

## 빠른 답변
- **“set language”가 무엇에 영향을 줍니까?** OneNote에 어떤 교정 사전을 사용할지 알려줍니다(맞춤법 검사 및 문법).
- **같은 노트에서 다른 언어를 설정할 수 있나요?** 예, 각 텍스트 실행에 언어를 지정할 수 있습니다.
- **Aspose.Note에 라이선스가 필요합니까?** 무료 체험판으로 테스트할 수 있지만, 상용 환경에서는 상업용 라이선스가 필요합니다.
- **지원되는 Java 버전은 무엇입니까?** Aspose.Note for Java는 Java 8 및 그 이후 버전을 지원합니다.
- **.one 파일이 출력됩니까?** 예, 문서는 OneNote *.one* 파일로 저장됩니다.

## 전제 조건
코드에 들어가기 전에 다음 항목을 준비하십시오:

1. **Java Development Environment** – JDK 8 or higher installed and configured.  
2. **Aspose.Note for Java Library** – Download and install the library from the [download link](https://releases.aspose.com/note/java/).  
3. **Document Directory** – Create a folder on your machine where the generated OneNote file will be saved.

## OneNote에서 텍스트 언어를 설정해야 하는 이유
교정 언어를 설정하면 맞춤법 검사, 문법 제안 및 검색 인덱싱이 다국어 콘텐츠에 대해 올바르게 작동합니다. 이는 특히 다음과 같은 경우에 유용합니다:

- **Global teams** collaborating on a single notebook. 단일 노트북에서 협업하는 글로벌 팀.
- **Localized documentation** where each section may be in a different language. 각 섹션이 다른 언어일 수 있는 현지화된 문서.
- **Data‑driven applications** that generate notes programmatically for users worldwide. 전 세계 사용자에게 프로그램matically 노트를 생성하는 데이터 기반 애플리케이션.

## 패키지 가져오기
필요한 Aspose.Note 클래스와 Java 유틸리티를 가져오는 것으로 시작합니다.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.Locale;
```

## 단계 1: 문서 및 페이지 설정
새로운 OneNote 문서와 콘텐츠를 담을 페이지를 생성합니다. 이 단계에서는 **create OneNote document**도 시연합니다.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
```

## 단계 2: 개요 및 개요 요소 생성
개요는 노트북 콘텐츠를 담는 컨테이너입니다. 여기서는 이후에 언어별 텍스트를 포함할 구조를 구축합니다.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## 단계 3: 언어 설정이 포함된 서식 있는 텍스트 추가
이제 각 텍스트 세그먼트에 특정 `Locale`을 가진 `TextStyle`을 연결하여 **change text language**를 수행합니다. 이는 **set language for text**를 시연합니다.

```java
RichText text = new RichText()
                        .append("United States", new TextStyle().setLanguage(Locale.forLanguageTag("en-US")))
                        .append(" Germany", new TextStyle().setLanguage(Locale.forLanguageTag("de-DE")))
                        .append(" China", new TextStyle().setLanguage(Locale.forLanguageTag("zh-CN")));
text.setParagraphStyle(ParagraphStyle.getDefault());
```

## 단계 4: 요소 정리 및 저장
개요 계층 구조를 조립하고 페이지에 첨부한 뒤, 언어 설정이 적용된 **save OneNote file**를 최종적으로 수행합니다.

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
document.appendChildLast(page);
document.save(Paths.get(dataDir, "SetProofingLanguageForText.one").toString()); 
```

## 일반적인 함정 및 팁
- **Locale format** – Use the IETF BCP‑47 tag (e.g., `en-US`, `de-DE`). An incorrect tag will default to the document’s language. IETF BCP‑47 태그(e.g., `en-US`, `de-DE`)를 사용하십시오. 잘못된 태그는 문서의 언어로 기본 설정됩니다.
- **File path** – Ensure `dataDir` points to an existing folder; otherwise `document.save` will throw an `IOException`. `dataDir`이 기존 폴더를 가리키는지 확인하십시오; 그렇지 않으면 `document.save`가 `IOException`을 발생시킵니다.
- **Pro tip:** If you need to set the language for an entire paragraph, apply the `TextStyle` to the `ParagraphStyle` instead of each `append` call. 전체 단락에 언어를 설정해야 하는 경우, 각 `append` 호출 대신 `ParagraphStyle`에 `TextStyle`을 적용하십시오.

## 결론
여러분은 이제 Aspose.Note for Java를 사용하여 OneNote 노트북의 개별 텍스트 조각에 **how to set language**를 설정하는 방법을 배웠습니다. 이 기능을 통해 **create OneNote document**를 프로그래밍 방식으로 생성하고, **change text language**를 실시간으로 변경하며, 정확한 교정 메타데이터와 함께 **save OneNote file**를 할 수 있습니다.

## 자주 묻는 질문

**Q: 예제에 언급되지 않은 다른 언어에 대한 교정 언어를 설정할 수 있나요?**  
A: 물론입니다! 원하는 `Locale.forLanguageTag("xx-XX")`를 사용하여 추가 `append` 호출을 추가하십시오.

**Q: Aspose.Note for Java가 최신 Java 버전과 호환됩니까?**  
A: 예, 라이브러리는 최신 Java 릴리스를 지원하도록 정기적으로 업데이트됩니다.

**Q: 언어 설정 과정 중 오류를 어떻게 처리할 수 있나요?**  
A: 저장 작업을 `try‑catch` 블록으로 감싸 `IOException` 또는 `AsposeException`을 포착하십시오.

**Q: 이 코드를 웹 애플리케이션에 통합할 수 있나요?**  
A: 물론입니다. Aspose.Note JAR를 웹 프로젝트의 클래스패스에 포함하고, 서버가 대상 디렉터리에 대한 쓰기 권한을 가지고 있는지 확인하십시오.

**Q: Aspose.Note for Java에 대한 추가 예제와 문서는 어디에서 찾을 수 있나요?**  
A: 전체 API 목록 및 샘플 프로젝트를 보려면 [documentation](https://reference.aspose.com/note/java/)을 살펴보십시오.

---

**마지막 업데이트:** 2026-03-29  
**테스트 대상:** Aspose.Note for Java 24.12  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}