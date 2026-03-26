---
date: 2026-01-05
description: 기본 로케일 설정, OneNote 문서 로드, Aspose 라이선스 설정, OneNote를 PNG로 변환하고 Aspose.Note
  for Java를 사용하여 OneNote를 이미지로 저장하는 방법을 배웁니다.
linktitle: Working with Locales in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: OneNote에서 기본 로케일 설정 – Aspose.Note Java
url: /ko/java/onenote-notebook-operations/working-with-locales/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote에서 기본 로케일 설정 – Aspose.Note Java

## 소개

OneNote 파일을 처리하면서 **set default locale**이 필요하다면, Aspose.Note for Java가 손쉽게 도와줍니다. 이 튜토리얼에서는 제품 라이선스 설정부터 OneNote 문서 로드, 로케일 변경, 마지막으로 파일을 PNG 이미지로 변환하는 전체 과정을 단계별로 안내합니다. 끝까지 따라오면 몇 줄의 코드만으로 언어 설정을 맞춤화하고 로케일별 출력물을 생성할 수 있게 됩니다.

## 빠른 답변
- **“set default locale”은 무엇을 하나요?** Aspose.Note가 OneNote 파일을 읽거나 쓸 때 사용하는 언어 및 지역 형식을 정의합니다.  
- **라이선스가 필요합니까?** 예—전체 기능을 사용하려면 Aspose 라이선스를 설정하세요.  
- **필요한 Java 버전은?** JDK 8 이상이면 모두 지원됩니다.  
- **OneNote를 PNG로 변환할 수 있나요?** 물론입니다; API를 사용하면 페이지를 이미지로 저장할 수 있습니다.  
- **이 과정이 스레드‑안전한가요?** set default locale은 전역 설정이므로 애플리케이션 시작 시 한 번만 구성하면 됩니다.

## Aspose.Note에서 “set default locale”이란?

기본 로케일을 설정하면 Aspose.Note가 날짜, 숫자 및 텍스트를 구문 분석할 때 적용할 언어와 문화적 규칙을 지정합니다. 이는 다양한 사용자 로케일에 걸쳐 일관된 형식이 필요한 다지역 애플리케이션에 필수적입니다.

## OneNote 작업 시 기본 로케일을 설정해야 하는 이유

- **정확한 데이터 표현:** 대상 사용자에게 날짜와 숫자가 올바르게 표시됩니다.  
- **일관된 UI 문자열:** OneNote에서 추출한 텍스트가 언어 설정을 따릅니다.  
- **간소화된 변환:** 이후 OneNote 파일을 PNG 등으로 변환할 때 시각적 레이아웃이 기대하는 로케일에 맞게 표시됩니다.

## 전제 조건

- **Java 개발 환경:** JDK가 설치되어 있고 `JAVA_HOME`이 설정되어 있어야 합니다.  
- **Aspose.Note 라이브러리:** 최신 JAR를 [다운로드 링크](https://releases.aspose.com/note/java/)에서 다운로드하세요.  
- **유효한 Aspose 라이선스 파일** (무료 체험판으로 테스트 가능).

## 패키지 가져오기

코드를 작성하기 전에 필요한 기능을 제공하는 클래스를 가져와야 합니다.

```java
import java.io.IOException;
import java.nio.file.Path;
import java.util.Locale;
import com.aspose.note.Document;
import com.aspose.note.License;
import com.aspose.note.LocaleOptions;
```

## 단계 1: Aspose 라이선스 설정

```java
License license = new License();
license.setLicense("licenseFile");
```

Aspose 라이선스를 설정하면 로케일 처리와 이미지 변환을 포함한 모든 기능이 활성화됩니다.

## 단계 2: 기본 로케일 설정

```java
java.util.Locale.setDefault(new java.util.Locale("en", "rs"));
```

여기서는 언어 코드 `en`과 국가 코드 `rs`를 사용해 **set default locale**을 영어로 설정합니다. 대상 지역에 맞게 언어 및 국가 코드를 조정하세요.

## 단계 3: OneNote 문서 로드

```java
String inputFile = "Sample1.one";
Path inputPath = Paths.get(inputFile);

Document oneFile = new Document(inputPath.toString());
```

이 단계에서는 **load(s) OneNote document**를 `Document` 객체에 로드하여 내용에 접근할 수 있게 합니다.

## 단계 4: OneNote를 PNG로 변환 (OneNote 파일 변환)

```java
oneFile.save("sample.png");
```

`save` 메서드는 **onenote file conversion**을 수행하여 노트북(또는 특정 페이지)을 PNG 이미지로 내보냅니다—즉 **convert onenote to png** 및 **save onenote as image**와 같은 동작을 합니다.

## 일반적인 문제 및 팁

- **라이선스를 찾을 수 없음:** `licenseFile` 경로가 올바른지, 파일에 읽기 권한이 있는지 확인하세요.  
- **로케일이 적용되지 않음:** 문서를 로드하기 **전에** `Locale.setDefault`를 호출하세요.  
- **이미지 출력이 없음:** OneNote 파일에 실제로 렌더링 가능한 페이지가 있는지 확인하세요; 빈 노트북은 빈 PNG를 생성합니다.

## 자주 묻는 질문

**Q: Aspose.Note가 다양한 Java 버전과 호환되나요?**  
A: 예, Aspose.Note는 Java 8 이상을 지원하므로 다양한 개발 환경에서 폭넓게 호환됩니다.

**Q: Aspose.Note를 다른 Java 라이브러리와 통합할 수 있나요?**  
A: 물론입니다. API는 Apache POI, Jackson, Spring 등 인기 라이브러리와 원활하게 작동합니다.

**Q: Aspose.Note가 다양한 파일 형식을 지원하나요?**  
A: 핵심은 OneNote 파일이지만, 라이브러리는 PNG, JPEG, PDF 등 여러 이미지 형식으로 내보낼 수 있습니다.

**Q: Aspose.Note 사용자가 도움을 구하고 지식을 공유할 수 있는 커뮤니티 포럼이 있나요?**  
A: 네, Aspose 커뮤니티 포럼은 사용자가 전문가와 교류하고, 질문을 하고, 솔루션을 협업할 수 있는 플랫폼을 제공합니다. 도움을 원하시면 [지원 포럼](https://forum.aspose.com/c/note/28)을 방문하세요.

**Q: 구매 전에 Aspose.Note를 체험할 수 있나요?**  
A: 물론입니다. 웹사이트에서 제공하는 무료 체험판을 이용해 Aspose.Note의 기능을 살펴볼 수 있습니다.

## 결론

이 단계를 따라 하면 Aspose.Note for Java를 사용해 **set default locale**, **load OneNote document**, **set Aspose license**, 그리고 **convert OneNote to PNG**를 수행하는 방법을 배웠습니다. 이 워크플로우를 통해 전 세계 사용자를 위한 로케일 인식 보고서와 이미지를 생성할 수 있습니다.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**마지막 업데이트:** 2026-01-05  
**테스트 대상:** Aspose.Note 24.11 for Java  
**작성자:** Aspose