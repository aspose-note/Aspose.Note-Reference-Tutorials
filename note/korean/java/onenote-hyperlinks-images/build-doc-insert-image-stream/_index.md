---
date: 2025-12-21
description: Aspose.Note for Java를 사용하여 OneNote 문서를 Java로 만들고 이미지를 손쉽게 삽입하는 방법을 배우세요.
  Java 개발자를 위한 단계별 가이드.
linktitle: How to create onenote document java – Build Doc and Insert Image with Stream
second_title: Aspose.Note Java API
title: Java로 OneNote 문서 만들기 – 문서 빌드 및 스트림을 사용한 이미지 삽입
url: /ko/java/onenote-hyperlinks-images/build-doc-insert-image-stream/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java에서 OneNote 문서 만들기 – 문서 생성 및 스트림으로 이미지 삽입

## 소개

환영합니다! 이 튜토리얼에서는 **Java에서 OneNote 문서 만들기**를 처음부터 진행하고 이미지 스트림을 사용해 이미지를 삽입하는 방법을 배웁니다. 각 단계를 차근차근 살펴보고, 왜 해당 단계가 중요한지 설명하며, 실제 프로젝트에 적용할 수 있는 실용적인 팁을 제공합니다. 끝까지 따라오면 프로그래밍으로 OneNote 페이지를 생성하고 필요한 위치에 사진을 정확히 삽입할 수 있게 됩니다.

## 빠른 답변
- **필요한 라이브러리는?** Aspose.Note for Java  
- **스트림으로 이미지를 삽입할 수 있나요?** 예 – `Image` 생성자에 `InputStream`을 전달하면 됩니다.  
- **어떤 형식으로 내보낼 수 있나요?** Aspose.Note에서 지원하는 모든 형식, 예: PDF, DOCX, HTML.  
- **개발에 라이선스가 필요합니까?** 평가용으로는 무료 임시 라이선스로 충분하지만, 실제 운영 환경에서는 정식 라이선스가 필요합니다.  
- **필요한 Java 버전은?** Java 8 이상.

## “Java에서 OneNote 문서 만들기”란?

Java에서 OneNote 문서를 만든다는 것은 Aspose.Note API를 활용해 노트북 구조(페이지, 아웃라인, 요소 등)를 프로그래밍 방식으로 구축한다는 의미이며, OneNote 데스크톱 클라이언트를 열 필요가 없습니다. 이 방법은 자동화된 보고서 생성, 대량 노트 처리, 또는 OneNote 콘텐츠를 더 큰 Java 애플리케이션에 통합할 때 이상적입니다.

## 왜 Aspose.Note for Java를 사용해 Java에서 OneNote 문서를 만들까요?

- **전체 제어** – 페이지 레이아웃, 아웃라인 위치, 요소 스타일을 자유롭게 지정 가능.  
- **COM 인터옵 없음** – Java를 지원하는 모든 OS에서 동작합니다.  
- **다양한 내보내기 옵션** – 동일한 문서를 단 한 번의 호출로 PDF, DOCX, HTML 등으로 변환 가능.  
- **스트림 친화적** – 메모리, 네트워크, 클라우드 저장소 등에서 직접 이미지를 로드할 수 있습니다.

## 사전 준비 사항

진행하기 전에 아래 항목들을 준비하십시오.

### Java Development Kit (JDK)

머신에 최신 JDK(8 이상)가 설치되어 있어야 합니다.

### Aspose.Note for Java 라이브러리

공식 Aspose 릴리스 페이지에서 라이브러리를 다운로드합니다: [https://releases.aspose.com/note/java/](https://releases.aspose.com/note/java/).

### IDE 설정

선호하는 IDE(IntelliJ IDEA, Eclipse, VS Code 등)에 Aspose.Note JAR 파일을 프로젝트 클래스패스에 포함하도록 구성합니다.

## 패키지 가져오기

시작하려면 필요한 Java 및 Aspose.Note 클래스를 가져옵니다. 이러한 import 구문을 통해 문서 생성, 페이지 처리, 아웃라인 관리 및 이미지 삽입 기능을 사용할 수 있습니다.

```java
import java.io.FileInputStream;
import java.io.FileNotFoundException;
import java.io.IOException;
import java.io.InputStream;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## 1단계: 문서 디렉터리 설정

소스 이미지가 들어 있는 폴더와 출력 파일을 저장할 위치를 정의합니다. 플레이스홀더를 실제 머신 경로로 교체하십시오.

```java
String dataDir = "Your Document Directory";
```

## 2단계: Document 객체 생성

새 `Document`를 인스턴스화합니다. 이 객체가 여러분이 구축하고 있는 OneNote 노트북을 나타냅니다.

```java
Document doc = new Document();
```

## 3단계: Page 객체 초기화

이 노트북 페이지에 포함될 모든 아웃라인 및 요소를 담을 `Page`를 생성합니다.

```java
Page page = new Page();
```

## 4단계: Outline 생성

`Outline`은 위치 지정 요소를 담는 컨테이너 역할을 합니다. 여기서는 아웃라인을 페이지에 배치하기 위해 수직 및 수평 오프셋을 설정합니다.

```java
Outline outline1 = new Outline();
outline1.setVerticalOffset(600);
outline1.setHorizontalOffset(0);
```

## 5단계: Outline Element 생성

이미지를 삽입할 `OutlineElement`를 생성합니다.

```java
OutlineElement outlineElem1 = new OutlineElement();
```

## 6단계: 이미지 스트림 로드

이미지 파일을 스트림으로 엽니다. 스트림을 사용하면 파일 시스템, 네트워크, 데이터베이스 등 어떤 소스에서든 이미지를 읽어 디스크에 저장하지 않고 바로 처리할 수 있습니다.

```java
InputStream fs = null;
try {
    fs = new FileInputStream(dataDir + "image.jpg");
} catch (FileNotFoundException e) {
    e.printStackTrace();
}
```

## 7단계: 이미지 삽입

`Image` 객체를 생성합니다. 첫 번째 인자는 나중에 스트림을 제공할 경우 `null`로 할 수 있지만, 여기서는 간단히 파일 경로를 지정하고 페이지 오른쪽에 정렬하도록 설정합니다.

```java
Image image = new Image(null, dataDir + "image1.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## 8단계: 이미지를 Outline Element에 추가

이미지를 아웃라인 요소에 추가하여 페이지 시각 계층 구조의 일부가 되게 합니다.

```java
outlineElem1.appendChildLast(image);
```

## 9단계: Outline Element를 Outline에 추가

이제 이미지가 포함된 아웃라인 요소를 아웃라인 컨테이너에 연결합니다.

```java
outline1.appendChildLast(outlineElem1);
```

## 10단계: Outline을 Page에 추가

아웃라인을 페이지에 배치합니다.

```java
page.appendChildLast(outline1);
```

## 11단계: Page를 Document에 추가

완성된 페이지를 문서 객체에 추가합니다.

```java
doc.appendChildLast(page);
```

## 12단계: 문서 저장

마지막으로 필요한 형식으로 OneNote 문서를 저장합니다. 이 예제에서는 PDF로 내보내지만, Aspose.Note가 지원하는 모든 형식 중에서 선택할 수 있습니다.

```java
try {
    doc.save("D://Aspose_JavaProjects//OneNote//out3.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

위 단계를 따라 하면 **Java에서 OneNote 문서 만들기**와 입력 스트림을 이용한 이미지 삽입을 성공적으로 수행한 것입니다.

## 흔히 발생하는 문제 및 팁

- **스트림 미닫힘** – 실제 운영 환경에서는 `InputStream`을 `finally` 블록에서 닫거나 try‑with‑resources를 사용해 자동으로 닫아야 합니다.  
- **잘못된 파일 경로** – `dataDir`이 올바른 구분자(`/` 또는 `\`)로 끝나는지 반드시 확인하십시오.  
- **이미지 정렬** – 이미지가 화면 밖에 나타나면 아웃라인의 `VerticalOffset`/`HorizontalOffset` 값을 조정하십시오.  
- **라이선스 예외** – 평가 버전을 사용할 경우 출력에 워터마크가 추가될 수 있으니, 정식 라이선스를 적용해 제거하십시오.

## 자주 묻는 질문

### Q1: Aspose.Note for Java는 모든 버전의 OneNote와 호환되나요?

A1: Aspose.Note for Java는 다양한 OneNote 파일 형식을 지원하므로 데스크톱, 온라인, 모바일 버전 모두와 호환됩니다.

### Q2: Aspose.Note for Java를 사용해 삽입한 이미지의 모양을 커스터마이즈할 수 있나요?

A2: 예, `Image` 객체의 정렬, 크기, 회전 및 자르기 등 속성을 조정하여 이미지 모양을 자유롭게 변경할 수 있습니다.

### Q3: Aspose.Note for Java가 PDF 외에 다른 문서 형식도 지원하나요?

A3: 물론입니다. API는 DOCX, HTML, XPS 등 여러 형식으로 내보낼 수 있어 노트를 다양한 방식으로 공유하거나 보관할 수 있습니다.

### Q4: Aspose.Note for Java에 대한 추가 자료와 지원은 어디서 찾을 수 있나요?

A4: 공식 Aspose 웹사이트에서 풍부한 문서, 코드 예제, 포럼 및 평가용 임시 라이선스를 제공하고 있습니다.

### Q5: Aspose.Note for Java의 체험판을 다운로드할 수 있나요?

A5: 예, Aspose 릴리스 페이지에서 무료 체험판을 다운로드하여 모든 기능을 구매 전 미리 체험할 수 있습니다.

---

**최종 업데이트:** 2025-12-21  
**테스트 환경:** Aspose.Note for Java 24.12 (작성 시 최신 버전)  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}