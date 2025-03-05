---
title: OneNote에서 루트 및 하위 페이지가 포함된 문서 만들기
linktitle: OneNote에서 루트 및 하위 페이지가 포함된 문서 만들기
second_title: Aspose.Note 자바 API
description: Aspose.Note for Java를 사용하여 OneNote에서 루트 및 하위 페이지가 포함된 문서를 만듭니다. 단계별 가이드에 따라 노트를 효율적으로 정리하세요.
type: docs
weight: 11
url: /ko/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
---
## 소개

이 튜토리얼에서는 Aspose.Note for Java를 사용하여 OneNote에서 루트 및 하위 페이지가 포함된 문서를 만드는 과정을 안내합니다. 다음 단계를 따르면 OneNote 문서를 계층 구조로 효율적으로 구성할 수 있습니다.

## 전제조건

시작하기 전에 다음 필수 구성 요소가 있는지 확인하세요.

1. JDK(Java Development Kit): 시스템에 JDK가 설치되어 있는지 확인하십시오.
2. Java용 Aspose.Note: 다음 사이트에서 Java용 Aspose.Note를 다운로드하고 설치하세요.[웹사이트](https://purchase.aspose.com/buy).
3. 통합 개발 환경(IDE): IntelliJ IDEA, Eclipse 또는 NetBeans와 같은 Java IDE를 선택합니다.

## 패키지 가져오기

Java 프로젝트에 필요한 패키지를 가져오는 것부터 시작하세요.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

## 1단계: 문서 디렉토리 설정

OneNote 문서를 저장할 디렉터리를 정의합니다.

```java
String dataDir = "Your Document Directory";
```

## 2단계: 문서 개체 만들기

 인스턴스화`Document` 물체:

```java
Document doc = new Document();
```

## 3단계: 페이지 생성

페이지 개체를 초기화하고 해당 수준을 설정합니다.

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## 4단계: 페이지에 노드 추가

### 첫 번째 페이지에 노드 추가

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text = new RichText().append("First page.");
text.setParagraphStyle(textStyle);

outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page1.appendChildLast(outline);
```

### 두 번째 페이지에 노드 추가

```java
Outline outline2 = new Outline();
OutlineElement outlineElem2 = new OutlineElement();
ParagraphStyle textStyle2 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text2 = new RichText().append("Second page.");
text2.setParagraphStyle(textStyle2);

outlineElem2.appendChildLast(text2);
outline2.appendChildLast(outlineElem2);
page2.appendChildLast(outline2);
```

### 세 번째 페이지에 노드 추가

```java
Outline outline3 = new Outline();
OutlineElement outlineElem3 = new OutlineElement();
ParagraphStyle textStyle3 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Broadway")
                                    .setFontSize(10);

RichText text3 = new RichText().append("Third page.");
text3.setParagraphStyle(textStyle3);

outlineElem3.appendChildLast(text3);
outline3.appendChildLast(outlineElem3);
page3.appendChildLast(outline3);
```

## 5단계: 문서에 페이지 추가

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## 6단계: 문서 저장

OneNote 문서를 저장합니다.

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // 예외 처리
}
```

축하해요! Java용 Aspose.Note를 사용하여 OneNote에서 루트 및 하위 페이지가 포함된 문서를 성공적으로 만들었습니다.

## 결론

더 나은 관리 및 탐색을 위해서는 OneNote 문서를 계층 구조로 구성하는 것이 필수적입니다. Aspose.Note for Java를 사용하면 루트 및 하위 페이지가 포함된 문서를 효율적으로 생성하여 노트에 명확하고 체계적인 레이아웃을 제공할 수 있습니다.

## FAQ

### Q1: Aspose.Note for Java를 사용하여 여러 수준의 하위 페이지를 만들 수 있나요?

A1: 예, 각 페이지에 적절한 수준을 설정하여 여러 수준의 하위 페이지를 만들 수 있습니다.

### Q2: Aspose.Note for Java는 다른 Java IDE와 호환됩니까?

A2: 예, Aspose.Note for Java는 IntelliJ IDEA, Eclipse, NetBeans 등 널리 사용되는 Java IDE와 호환됩니다.

### 질문 3: OneNote 문서의 텍스트 서식을 사용자 지정할 수 있나요?

A3: 예, Java의 서식 있는 텍스트 기능을 위한 Aspose.Note를 사용하여 글꼴, 색상, 크기 및 기타 서식 옵션을 사용자 정의할 수 있습니다.

### Q4: Java용 Aspose.Note는 다양한 형식의 문서 저장을 지원합니까?

A4: 예, Aspose.Note for Java는 BMP, PDF, PNG 등을 포함한 다양한 형식의 문서 저장을 지원합니다.

### Q5: Aspose.Note for Java에 사용할 수 있는 평가판이 있나요?

A5: 예, 웹사이트에서 Java용 Aspose.Note의 무료 평가판을 다운로드할 수 있습니다.