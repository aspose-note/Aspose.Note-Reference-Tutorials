---
title: Java를 사용하여 OneNote에서 문서 작성 및 이미지 삽입
linktitle: Java를 사용하여 OneNote에서 문서 작성 및 이미지 삽입
second_title: Aspose.Note 자바 API
description: OneNote 문서를 작성하고 Java용 Aspose.Note를 사용하여 이미지를 삽입하는 방법을 알아보세요. 원활한 통합을 위한 단계별 튜토리얼입니다.
weight: 12
url: /ko/java/onenote-hyperlinks-images/build-doc-insert-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java를 사용하여 OneNote에서 문서 작성 및 이미지 삽입

## 소개

이 튜토리얼에서는 Java용 Aspose.Note를 사용하여 OneNote 문서를 작성하고 여기에 이미지를 삽입하는 방법을 살펴보겠습니다. Aspose.Note는 개발자가 Microsoft OneNote 파일을 프로그래밍 방식으로 작업할 수 있게 해주는 강력한 Java API입니다. 각 단계를 자세히 분석하여 프로세스를 안내해 드리겠습니다.

## 전제조건

시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

1. JDK(Java Development Kit): 시스템에 JDK가 설치되어 있는지 확인하세요.
2.  Aspose.Note for Java 라이브러리: Aspose.Note for Java 라이브러리를 다운로드하여 설치하세요.[웹사이트](https://releases.aspose.com/note/java/).
3. IDE(통합 개발 환경): IntelliJ IDEA 또는 Eclipse와 같은 Java 지원 IDE를 사용하여 코딩합니다.

## 패키지 가져오기

Java 코드에 필요한 패키지를 가져오는 것부터 시작하세요.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## 1단계: 문서 설정

먼저 새 OneNote 문서를 만들고 필요한 개체를 초기화합니다.

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

## 2단계: 개요 초기화

문서의 윤곽선을 설정하고 오프셋 속성을 지정합니다.

```java
Outline outline = new Outline();
outline.setVerticalOffset(0);
outline.setHorizontalOffset(0);
```

## 3단계: 이미지 추가

이미지를 로드하고 정렬을 지정합니다.

```java
Image image = new Image(null, dataDir + "Input.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## 4단계: 개요 요소에 이미지 추가

개요 요소에 이미지를 첨부합니다.

```java
OutlineElement outlineElem = new OutlineElement();
outlineElem.appendChildLast(image);
```

## 5단계: 개요 및 페이지 노드 추가

문서에 개요 및 페이지 노드를 추가합니다.

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## 6단계: 문서 저장

마지막으로 OneNote 문서를 저장합니다.

```java
try {
    doc.save(dataDir + "NewOneNotedocument_out", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## 결론

축하해요! OneNote 문서를 작성하고 Java용 Aspose.Note를 사용하여 이미지를 삽입하는 방법을 성공적으로 배웠습니다. 다음 단계를 수행하면 Java 응용 프로그램에서 OneNote 파일을 효율적으로 관리하고 조작할 수 있습니다.

## FAQ

### Q1: Aspose.Note for Java 설명서는 어디서 찾을 수 있나요?

 A1: 문서에 액세스할 수 있습니다.[여기](https://reference.aspose.com/note/java/).

### Q2: Java용 Aspose.Note를 어떻게 다운로드하나요?

 A2: 다음에서 Java용 Aspose.Note를 다운로드할 수 있습니다.[다운로드 페이지](https://releases.aspose.com/note/java/).

### Q3: Aspose.Note for Java에 대한 무료 평가판이 있습니까?

 A3: 예, 다음 사이트에서 무료 평가판을 받을 수 있습니다.[웹사이트](https://releases.aspose.com/).

### Q4: Java용 Aspose.Note에 대한 지원은 어디서 받을 수 있나요?

 A4: 지원을 받으려면[Aspose.Note 포럼](https://forum.aspose.com/c/note/28).

### Q5: Aspose.Note for Java에 대한 임시 라이선스를 얻을 수 있나요?

 A5: 네, 임시 라이센스를 요청할 수 있습니다.[여기](https://purchase.aspose.com/temporary-license/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
