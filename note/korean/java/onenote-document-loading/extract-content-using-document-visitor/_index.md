---
date: 2025-12-04
description: Aspose.Note를 사용하여 Java에서 OneNote 파일에서 이미지를 추출하고 OneNote를 텍스트로 변환하는 방법을
  배웁니다. 코드 예제가 포함된 단계별 가이드.
language: ko
linktitle: Extract Images from OneNote using Document Visitor - Java
second_title: Aspose.Note Java API
title: Document Visitor를 사용하여 OneNote에서 이미지 추출 - Java
url: /java/onenote-document-loading/extract-content-using-document-visitor/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Document Visitor를 사용하여 OneNote에서 이미지 추출 - Java

## 소개

Aspose.Note for Java를 사용하면 **OneNote** 노트북에서 이미지를 쉽게 **추출**하고, Java에서 기본 `.one` 파일을 읽을 수 있습니다. 이 튜토리얼에서는 OneNote 파일을 로드하고, 사용자 정의 `DocumentVisitor`로 구조를 순회하며 이미지와 일반 텍스트를 추출하는 전체 예제를 단계별로 안내합니다. 마지막으로 텍스트 내용만 필요할 경우 **OneNote를 텍스트로 변환**하는 방법도 알려드립니다.

## 빠른 답변
- **필요한 라이브러리는?** Aspose.Note for Java (아래 다운로드 링크).  
- **이미지만 추출할 수 있나요?** 예 – `DocumentVisitor`에서 `VisitImageStart` 메서드를 구현하면 됩니다.  
- **Java에서 .one 파일을 읽는 방법은?** `new Document(path, new LoadOptions())`를 사용합니다.  
- **프로덕션에 라이선스가 필요합니까?** 비트라이얼 사용이 아닌 경우 상용 라이선스가 필요합니다.  
- **지원되는 Java 버전은?** JDK 8 이상.

## 사전 요구 사항

시작하기 전에 다음을 준비하십시오:

1. Java Development Kit (JDK) 8 이상 설치.  
2. Aspose.Note for Java 라이브러리 다운로드. **[여기](https://releases.aspose.com/note/java/)**에서 받을 수 있습니다.  
3. 이미지 추출 또는 텍스트 변환을 원하는 OneNote 문서(`.one` 파일).

## 패키지 가져오기

먼저 Aspose.Note API에서 필요한 클래스를 가져옵니다.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.DocumentVisitor;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.OutlineGroup;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.Title;
```

## 1단계: 사용자 정의 Document Visitor 설정

`DocumentVisitor`를 상속하는 클래스를 만들고, 이 클래스가 OneNote 문서의 각 노드에 대해 호출되어 **OneNote에서 이미지 추출** 및 선택적으로 텍스트를 수집하도록 합니다.

```java
public class ExtractOneNoteContentUsingDocumentvisitor extends DocumentVisitor {
    
    final private StringBuilder mBuilder;
    final private boolean mIsSkipText;
    private int nodecount;

    public ExtractOneNoteContentUsingDocumentvisitor() {
        nodecount = 0;
        mIsSkipText = false;
        mBuilder = new StringBuilder();
    }
    
    // Other methods will be implemented here
}
```

## 2단계: Visitor 메서드 구현

관심 있는 노드 유형에 대한 오버라이드를 추가합니다. 아래 예제에서는 리치 텍스트, 이미지, 제목, 페이지, 아웃라인 및 아웃라인 요소를 처리합니다. 이미지 추출은 `VisitImageStart` 메서드에서 이루어집니다.

```java
// Visitor methods for different types of nodes

public /* override */ void VisitRichTextStart(RichText run) {
    ++nodecount;
    AppendText(run.getText());
}

public /* override */ void VisitDocumentStart(Document document) {
    ++nodecount;
}

public /* override */ void VisitPageStart(Page page) {
    ++nodecount;
}

public /* override */ void VisitTitleStart(Title title) {
    ++nodecount;
}

public /* override */ void VisitImageStart(Image image) {
    ++nodecount;
    // Here you could save the image to disk or process it further
    System.out.println("Found image with size: " + image.getData().length + " bytes");
}

public /* override */ void VisitOutlineGroupStart(OutlineGroup outlineGroup) {
    ++nodecount;
}

public void VisitOutlineStart(Outline outline) {
    ++nodecount;
}

public void VisitOutlineElementStart(OutlineElement outlineElement) {
    ++nodecount;
}
```

### 왜 이러한 메서드를 구현하나요?

- **OneNote에서 이미지 추출:** `VisitImageStart`를 통해 원시 이미지 바이트에 직접 접근할 수 있습니다.  
- **OneNote를 텍스트로 변환:** `VisitRichTextStart`가 텍스트 내용을 수집하므로 간단한 **OneNote를 텍스트로 변환** 작업이 가능합니다.  
- **Java에서 .one 파일 읽기:** Visitor 패턴이 `.one` 파일 구조를 추상화하므로 바이너리 포맷을 직접 파싱할 필요가 없습니다.

## 3단계: Main 메서드에서 Visitor 실행

`.one` 파일을 로드하고, Visitor 인스턴스를 생성한 뒤 순회를 시작합니다.

```java
public static void main(String[] args) throws IOException {
    // Open the document we want to convert.
    String dataDir = "Your Document Directory";
    Document doc = new Document(dataDir + "Sample1.one", new LoadOptions());
    
    // Create an object that inherits from the DocumentVisitor class.
    ExtractOneNoteContentUsingDocumentvisitor myConverter = new ExtractOneNoteContentUsingDocumentvisitor();
    
    // Accept the visitor to start the visiting process.
    doc.accept(myConverter);
    
    // Retrieve the result of the operation.
    System.out.println(myConverter.GetText());   // Text extracted from the notebook
    System.out.println(myConverter.NodeCount()); // Total nodes visited
}
```

## 일반적인 사용 사례

- **자동 보고:** OneNote 회의 노트북에서 이미지와 텍스트를 추출해 PDF 또는 HTML 요약본을 생성.  
- **콘텐츠 마이그레이션:** 레거시 OneNote 아카이브를 평문 파일로 변환해 인덱싱 또는 검색 엔진에 활용.  
- **디지털 자산 추출:** 삽입된 스크린샷, 다이어그램, 사진 등을 다른 애플리케이션에서 재사용하도록 수집.

## 문제 해결 및 팁

- **대용량 노트북:** 메모리 문제가 발생하면 `VisitPageStart`를 확인하고 페이지별로 필요한 리소스만 로드하도록 처리합니다.  
- **이미지 포맷:** `Image` 객체가 반환하는 원시 바이트를 저장하기 전에 포맷(PNG, JPEG 등)을 감지해야 할 수 있습니다.  
- **라이선스 오류:** 프로덕션 환경에서 문서를 로드하기 전에 Aspose 라이선스를 설정했는지 확인합니다(`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`).

## 자주 묻는 질문

**Q: OneNote 문서에서 특정 유형의 콘텐츠만 추출할 수 있나요?**  
A: 예 – 필요한 Visitor 메서드만 오버라이드하면 됩니다(`VisitImageStart`는 이미지, `VisitRichTextStart`는 텍스트).

**Q: Aspose.Note for Java가 다양한 버전의 OneNote 문서를 지원하나요?**  
A: 네. 주요 OneNote 파일 버전을 모두 지원하므로 **Java에서 .one 파일 읽기** 프로젝트에서 원본 OneNote 버전에 관계없이 안전하게 사용할 수 있습니다.

**Q: 이 추출 과정을 내 Java 애플리케이션에 통합할 수 있나요?**  
A: 가능합니다. Visitor 패턴은 어떤 Java 코드베이스에서도 원활히 동작하므로 라이브러리 JAR를 추가하고 위 예제를 호출하면 됩니다.

**Q: 복잡한 OneNote 문서를 처리할 수 있는 지원이 있나요?**  
A: 있습니다. 중첩된 아웃라인, 임베디드 미디어, 사용자 정의 데이터 모두 Visitor API를 통해 접근할 수 있습니다.

**Q: 처리 가능한 OneNote 문서 크기에 제한이 있나요?**  
A: 명확한 제한은 없지만 매우 큰 노트북은 더 많은 힙 메모리를 요구할 수 있으니 페이지 단위로 처리하는 것을 권장합니다.

**Q: 추출한 텍스트를 평문 파일로 저장하려면 어떻게 하나요?**  
A: `myConverter.GetText()`가 반환한 `String`을 표준 Java I/O(`Files.write(Paths.get("output.txt"), text.getBytes());`)를 사용해 파일에 기록하면 됩니다.

---  

**마지막 업데이트:** 2025-12-04  
**테스트 환경:** Aspose.Note for Java 24.10  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}