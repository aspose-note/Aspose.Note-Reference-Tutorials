---
date: 2025-12-18
description: Aspose.Note for Java를 사용하여 OneNote 페이지를 PDF로 내보내는 방법을 배워보세요. 분할 알고리즘을
  선택하고 페이지 분할을 설정하여 PDF 파일을 쉽게 생성할 수 있습니다.
linktitle: Export OneNote Pages with Splitting Algorithm Method – Aspose.Note
second_title: Aspose.Note Java API
title: 분할 알고리즘 방법으로 OneNote 페이지 내보내기 – Aspose.Note
url: /ko/java/onenote-document-saving/use-splitting-algorithm-method/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 분할 알고리즘 방법을 사용하여 OneNote 페이지에 있었습니다 – Aspose.Note

## 소개

프로그래밍 방식으로 **OneNote 페이지 내보내기**를 PDF 문서로 처리해야 하는 경우 Aspose.Note for Java를 사용하면 매우 간단합니다. 이 튜토리얼에서는 분할 알고리즘 방법을 좀 더 살펴보며, 페이지만 콘텐츠가 어떻게 작동하는지 제어하여 명확하게 알기 쉬운 PDF 출력을 만들 수 있습니다. PDF 저장 옵션을 설정하고, 적절한 페이지 분할 목록을 선택하고, 몇 가지 Java 코드만 PDF 파일을 생성하는 과정을 표시해 드립니다.

##빠른 답변
- **분할 알고리즘은 무엇을 방해합니까?** OneNote 페이지를 PDF로 내보낼 때 페이지 경계를 어떻게 처리할지를 결정합니다.
- **필요한 클래스는?** Aspose.Note for Java (공식 Aspose 사이트에서 다운로드).
- **라이선스가 필요합니까?** 무료 체험판을 이용하실 수 있습니다.
- **대용량 OneNote 노트북을 내보낼 수 있습니까?** 예 – 도서관은 조직 파일을 처리하며 페이지 분할 규칙을 접근할 수 있습니다.
- **지원되는 출력 형식은?** PDF, JPEG, PNG, XPS 등; 이 가이드는 PDF에 응답해야 합니다.

## **onenote 페이지 내보내기**란 무엇인가요?
OneNote 페이지를 내보낸다는 것은 기본적으로 `.one` 파일 형식을 PDF와 동일하게 휴대성이 높은 형식으로 변환하는 것을 의미합니다. OneNote는 콘텐츠를 공유할 수 없으며, 보관하거나 인쇄할 때 유용합니다.

## **onenote 페이지 내보내기**에 분할 알고리즘을 사용하는 이유
이 버섯을 사용하면 끌어들이는(표, 이미지, 그림)가 페이지를 어떻게 처리하는지 처리할 수 있습니다. 적절한 선택을 하면 다음을 수행할 수 있습니다:

* 각 페이지의 표시 내용을 유지합니다.
* 잘려드리는 것을 방지합니다.
* 이를 다음 페이지로 깔끔하게 이동하여 생성될 페이지를 줄 수 있습니다.

##조건

시작하기 전에 다음 조건을 확인하세요:

1. Java Development Kit (JDK): 시스템에 JDK가 설치되어 있어야 합니다. [웹사이트](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)에서 다운로드할 수 있습니다.
2. Aspose.Note for Java 라이브러리: [다운로드 링크](https://releases.aspose.com/note/java/)에서 Aspose.Note for Java 라이브러리를 다운로드하고 설치합니다.

## 패키지 가져오기

Java 프로젝트에서 Aspose.Note 기능을 활용하기 위해 필요한 부품을 가져옵니다.

```java
import java.io.IOException;
import com.aspose.note.AlwaysSplitObjectsAlgorithm;
import com.aspose.note.Document;
import com.aspose.note.KeepPartAndCloneSolidObjectToNextPageAlgorithm;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.PdfSaveOptions;
```

## 1단계: 문서 디렉터리 정의

OneNote 문서가 위치한 디렉터리를 설정합니다.

```java
String dataDir = "Your Document Directory";
```

## 2단계: OneNote 문서 불러오기

Aspose.Note의 `Document` 클래스를 사용하여 OneNote 문서를 로드합니다.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## 3단계: PDF 저장 옵션 설정

`PdfSaveOptions` 인스턴스를 생성하여 문서를 PDF로 저장할 때의 옵션을 지정합니다. 여기서 **set page splitting** 동작 및 기타 PDF 관련 설정을 정의합니다.

```java
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
```

## 4단계: 페이지 분할 알고리즘 설정

요구 사항에 맞는 적절한 splitting 알고리즘을 선택합니다. 여기서는 `KeepPartAndCloneSolidObjectToNextPageAlgorithm`을 사용합니다. 이 알고리즘은 객체의 일부를 현재 페이지에 남기고 나머지를 다음 페이지에 복제합니다.

```java
pdfSaveOptions.setPageSplittingAlgorithm(new KeepPartAndCloneSolidObjectToNextPageAlgorithm(100));
```

## 5단계: 문서 저장

지정한 PDF 저장 옵션으로 문서를 저장합니다. 이 단계에서는 **generates PDF onenote** 출력물이 생성되어 열거나, 공유하거나, 인쇄할 수 있습니다.

```java
try {
    doc.save(dataDir + "UsingSplittingAlgorithmMethod_out.Jpeg", pdfSaveOptions);
} catch (Exception ex) {
    System.out.println("Exception: " + ex.getMessage());
}
```

## 일반적인 문제 및 해결 방법

| 문제 | 해결 |
|-------|----------|
| **개체는 페이지 경계에서 잘립니다** | `AlwaysSplitObjectsAlgorithm`과 같은 다른 것을 시도하거나 `KeepPartAndCloneSolidObjectToNextPageAlgorithm`의 젊은 값을 높이세요. |
| **출력 PDF가 비어 있습니다** | 원본 `.one` 파일이 손상되지 않았는지, `dataDir`이 제대로 작동하지 않을지 확인하세요. |
| **대형 노트북에서는 성능이 느림** | `pdfSaveOptions.setCompressImages(true)`를 쪼이는 메모리 분수를 참고, 노트북을 더 작은 섹션으로 나누어 처리하는 것을 고려하세요. |

## 자주 묻는 질문

**Q: Aspose.Note for Java를 다른 프로그래밍 언어와 함께 사용할 수 있나요?**
A: 예, Aspose.Note는 .NET, C++, Python에서도 사용할 수 있습니다.

**Q: Aspose.Note는 대용량 OneNote 파일 처리에 적합합니까?**
A: 물론입니다. 이 라이브러리는 게이밍 노트북을 위해 처리하도록 최적화되어 있습니다.

**Q: Aspose.Note에 대한 추가 리소스와 지원은 어디서 찾을 수 있나요?**
A: 지원 및 가이드를 위해 [문서](https://reference.aspose.com/note/java/) 및 [포럼](https://forum.aspose.com/c/note/28)을 참고하세요.

**Q: 구매하기 전에 Aspose.Note를 사용해 볼 수 있나요?**
A: 예, [무료 평가판](https://releases.aspose.com/)을 통해 기능을 체험한 후 구매를 결정할 수 있습니다.

**Q: Aspose.Note의 임시 라이선스를 어떻게 얻을 수 있나요?**
A: 제품을 평가할 수 있도록 [임시 라이선스](https://purchase.aspose.com/temporary-license/)를 요청해 주세요.

---

**최종 업데이트:** 2025년 12월 18일
**테스트 환경:** Aspose.Note 26.4 for Java
**개발자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}