---
title: OneNote에서 기본 단락 스타일 설정 - Aspose.Note
linktitle: OneNote에서 기본 단락 스타일 설정 - Aspose.Note
second_title: Aspose.Note 자바 API
description: Java용 Aspose.Note를 사용하여 OneNote에서 기본 단락 스타일을 설정하는 방법을 알아보세요. Java 애플리케이션에서 효율적인 텍스트 형식 지정을 위한 단계별 가이드를 따르세요.
weight: 11
url: /ko/java/onenote-styles/set-default-paragraph-style/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote에서 기본 단락 스타일 설정 - Aspose.Note

## 소개

Aspose.Note for Java는 기본 단락 스타일 설정을 포함하여 텍스트 서식을 조작하는 강력한 기능을 제공합니다. 이 튜토리얼은 Aspose.Note를 사용하여 OneNote에서 기본 단락 스타일을 설정하는 과정을 안내합니다.

## 전제조건

시작하기 전에 다음 사항이 있는지 확인하세요.

1. JDK(Java Development Kit): 시스템에 JDK가 설치되어 있는지 확인하세요.
2.  Aspose.Note for Java 라이브러리: 다음에서 Aspose.Note for Java를 다운로드하고 설치하세요.[다운로드 페이지](https://releases.aspose.com/note/java/).
3. 통합 개발 환경(IDE): 코딩 편의를 위해 Eclipse 또는 IntelliJ IDEA와 같은 IDE가 설치되어 있어야 합니다.

## 패키지 가져오기

먼저 코딩을 시작하는 데 필요한 패키지를 가져옵니다.

```java
import com.aspose.note.*;

import java.awt.*;
import java.io.FileInputStream;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.List;
```

이제 예제 코드를 여러 단계로 나누어 보겠습니다.

## 1단계: 문서, 페이지, 개요 초기화

```java
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
Outline outline = new Outline();
```

## 2단계: 개요 요소 생성

```java
OutlineElement outlineElem = new OutlineElement();
```

## 3단계: 기본 단락 스타일 정의

```java
ParagraphStyle defaultStyle = new ParagraphStyle()
										.setFontName("Courier New")
										.setFontSize(20);
```

## 4단계: 기본 스타일을 사용하여 서식 있는 텍스트 만들기

```java
RichText text = new RichText()
					.append("DefaultParagraphFontAndSize")
					.append(System.lineSeparator())
					.append("OnlyDefaultParagraphFont", new TextStyle().setFontSize(14))
					.append(System.lineSeparator())
					.append("OnlyDefaultParagraphFontSize", new TextStyle().setFontName("Verdana"));
text.setParagraphStyle(defaultStyle);
```

## 5단계: 개요 요소에 서식 있는 텍스트 추가

```java
outlineElem.appendChildLast(text);
```

## 6단계: 개요에 개요 요소 추가

```java
outline.appendChildLast(outlineElem);
```

## 7단계: 페이지에 개요 추가

```java
page.appendChildLast(outline);
```

## 8단계: 문서에 페이지 추가

```java
document.appendChildLast(page);
```

## 9단계: 문서 저장

```java
document.save(Paths.get(dataDir, "SetDefaultParagraphStyle.one").toString());
```

이 코드는 Java용 Aspose.Note를 사용하여 OneNote에서 기본 단락 스타일을 설정합니다.

## 결론

OneNote에서 프로그래밍 방식으로 기본 단락 스타일을 설정하는 것은 Aspose.Note for Java를 사용하여 효율적으로 수행할 수 있습니다. 이 튜토리얼에 설명된 단계를 따르면 이 기능을 Java 애플리케이션에 원활하게 통합할 수 있습니다.

## FAQ

### Q1: 기본 단락 스타일을 추가로 사용자 정의할 수 있습니까?

A1: 예. 글꼴 이름, 크기, 색상, 정렬 등 다양한 매개변수를 요구 사항에 맞게 조정할 수 있습니다.

### Q2: Aspose.Note는 다른 텍스트 서식 작업을 지원합니까?

A2: 물론 Aspose.Note는 글꼴 스타일, 글머리 기호 및 들여쓰기를 포함하여 텍스트 서식을 조작하기 위한 광범위한 지원을 제공합니다.

### Q3: Aspose.Note는 모든 버전의 OneNote와 호환됩니까?

A3: Aspose.Note는 다양한 버전의 Microsoft OneNote 파일과 작동하도록 설계되어 광범위한 호환성을 보장합니다.

### Q4: Aspose.Note를 기존 Java 프로젝트에 통합할 수 있나요?

A4: 예, 필요한 종속성을 추가하고 필요한 패키지를 가져와서 Aspose.Note를 Java 프로젝트에 쉽게 통합할 수 있습니다.

### Q5: Aspose.Note에 사용할 수 있는 평가판이 있습니까?

 A5: 예, Aspose의 무료 평가판에 액세스할 수 있습니다.[웹사이트](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
