---
date: 2025-12-20
description: Aspose.Note for Java를 사용하여 OneNote에 그림을 추가하는 방법을 배워보세요. OneNote 문서를 만들고
  이미지를 프로그래밍 방식으로 삽입하는 단계별 가이드.
linktitle: How to add picture to OneNote using Java – Build Document and Insert Image
second_title: Aspose.Note Java API
title: Java를 사용하여 OneNote에 사진 추가하기 – 문서 만들기 및 이미지 삽입
url: /ko/java/onenote-hyperlinks-images/build-doc-insert-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java를 사용하여 OneNote에 그림 추가 – 문서 만들기 및 이미지 삽입

## 소개

이 튜토리얼에서는 **Aspose.Note Java API**를 사용하여 **OneNote에 그림을 추가하는 방법**을 배웁니다. 처음부터 OneNote 문서를 생성하고, 이미지를 삽입한 뒤, 결과를 PDF로 저장하는 과정을 단계별로 안내합니다. 보고서 도구를 구축하든, 노트 자동화를 하든, 혹은 프로그래밍 방식으로 그래픽을 삽입해야 하든, 이 가이드는 명확하고 실용적인 경로를 제공합니다.

## 빠른 답변
- **필요한 라이브러리는?** Aspose.Note for Java.
- **모든 이미지 형식을 삽입할 수 있나요?** JPEG, PNG, BMP, GIF 등 다양한 형식을 지원합니다.
- **어떤 출력 형식을 사용할 수 있나요?** OneNote, PDF, XPS, HTML 등으로 저장할 수 있습니다.
- **프로덕션에서 라이선스가 필요한가요?** 예, 비시험용으로는 상용 라이선스가 필요합니다.
- **코드가 크로스 플랫폼인가요?** 물론입니다 – Java는 Windows, Linux, macOS에서 실행됩니다.

## “OneNote에 그림 추가”란 무엇인가요?
OneNote에 그림을 추가한다는 것은 이미지 파일을 프로그래밍 방식으로 OneNote 페이지에 삽입하여 텍스트, 개요, 기타 요소와 함께 표시되도록 하는 것을 의미합니다. Aspose.Note API는 OneNote 파일 형식을 추상화하여 XML 구조에 신경 쓰지 않고 콘텐츠에 집중할 수 있게 해줍니다.

## Java로 OneNote에 그림을 추가해야 하는 이유
- **자동화:** 스크린샷을 자동으로 포함한 회의록을 생성합니다.
- **일관성:** 모든 페이지가 동일한 레이아웃과 브랜딩을 유지하도록 합니다.
- **통합:** 다른 시스템(예: 차트)에서 데이터를 직접 OneNote 노트북에 삽입합니다.
- **크로스 플랫폼:** Java를 사용하면 동일한 코드를 서버든 데스크톱이든 어느 환경에서든 실행할 수 있습니다.

## 사전 요구 사항

시작하기 전에 다음 항목을 준비하세요:

1. **Java Development Kit (JDK)** – 최신 버전(8 이상) 중 하나.  
2. **Aspose.Note for Java 라이브러리** – [웹사이트](https://releases.aspose.com/note/java/)에서 다운로드합니다.  
3. **IDE** – IntelliJ IDEA, Eclipse 또는 선호하는 Java 호환 편집기.  

## 패키지 가져오기

Java 소스 파일에 필요한 클래스를 가져옵니다:

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

## 단계별 가이드

### 단계 1: 문서 설정

새 OneNote 문서와 페이지 컨테이너를 생성합니다.

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

### 단계 2: 개요 초기화

*개요*는 텍스트와 이미지 같은 요소를 담는 컨테이너 역할을 합니다. 오프셋을 0으로 설정해 내용이 페이지 좌상단에서 시작하도록 합니다.

```java
Outline outline = new Outline();
outline.setVerticalOffset(0);
outline.setHorizontalOffset(0);
```

### 단계 3: 이미지 로드 및 정렬

삽입할 그림을 로드하고 페이지 오른쪽에 정렬합니다. 여기서 실제로 **OneNote에 그림을 추가**합니다.

```java
Image image = new Image(null, dataDir + "Input.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

### 단계 4: 이미지와 개요 요소 연결

이미지를 `OutlineElement` 안에 감싸서 문서의 개요 계층에 시각 객체를 연결합니다.

```java
OutlineElement outlineElem = new OutlineElement();
outlineElem.appendChildLast(image);
```

### 단계 5: 문서 구조 조립

개요 요소를 개요에 추가하고, 개요를 페이지에 연결한 뒤, 페이지를 문서에 추가합니다.

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

### 단계 6: OneNote 문서 저장

문서를 디스크에 저장합니다. 예제에서는 PDF로 내보내지만, `SaveFormat`을 변경하면 네이티브 OneNote 파일(`.one`)로도 저장할 수 있습니다.

```java
try {
    doc.save(dataDir + "NewOneNotedocument_out", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## 일반적인 문제와 해결 방법

| 문제 | 발생 원인 | 해결 방법 |
|------|-----------|-----------|
| **이미지가 표시되지 않음** | 파일 경로가 잘못되었거나 지원되지 않는 형식. | `dataDir`가 올바른 폴더를 가리키는지 확인하고, JPEG, PNG 등 지원되는 이미지 형식을 사용합니다. |
| **빈 PDF로 저장됨** | 개요 오프셋이 잘못 설정됨. | `setVerticalOffset(0)` 및 `setHorizontalOffset(0)` 호출을 확인하거나, 페이지 경계 내에 내용이 배치되도록 오프셋을 조정합니다. |
| **저장 시 IOException** | 대상 폴더가 없거나 쓰기 권한이 없음. | 폴더를 미리 생성하거나 적절한 권한으로 프로그램을 실행합니다. |

## 자주 묻는 질문

**Q1: Aspose.Note for Java 문서는 어디서 찾을 수 있나요?**  
A1: 문서는 [여기](https://reference.aspose.com/note/java/)에서 확인할 수 있습니다.

**Q2: Aspose.Note for Java를 어떻게 다운로드하나요?**  
A2: [다운로드 페이지](https://releases.aspose.com/note/java/)에서 받을 수 있습니다.

**Q3: Aspose.Note for Java 무료 체험판이 있나요?**  
A3: 예, [웹사이트](https://releases.aspose.com/)에서 무료 체험판을 받을 수 있습니다.

**Q4: Aspose.Note for Java 지원은 어디서 받을 수 있나요?**  
A4: 지원은 [Aspose.Note 포럼](https://forum.aspose.com/c/note/28)에서 받을 수 있습니다.

**Q5: Aspose.Note for Java 임시 라이선스를 받을 수 있나요?**  
A5: 예, [여기](httpshttps://purchase.aspose.com/temporary-license/)에서 임시 라이선스를 요청할 수 있습니다.

---

**마지막 업데이트:** 2025-12-20  
**테스트 환경:** Aspose.Note for Java 24.12 (최신)  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}