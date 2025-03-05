---
title: OneNote에서 글머리 기호 목록 만들기 - Aspose.Note
linktitle: OneNote에서 글머리 기호 목록 만들기 - Aspose.Note
second_title: Aspose.Note 자바 API
description: Java용 Aspose.Note를 사용하여 OneNote에서 글머리 기호 목록을 만드는 방법에 대한 단계별 가이드를 살펴보세요. 쉽게 문서 작성 수준을 높이세요.
type: docs
weight: 12
url: /ko/java/onenote-text-manipulation/create-bulleted-list/
---
## 소개
Java 개발의 역동적인 환경에서는 매력적이고 체계적인 문서를 만드는 것이 필수적입니다. Aspose.Note for Java는 문서 생성 프로세스를 향상시키는 강력한 도구 세트를 제공합니다. 이 튜토리얼은 Java용 Aspose.Note를 사용하여 OneNote에서 글머리 기호 목록을 만드는 과정을 안내합니다. 자세한 내용을 살펴보겠습니다.
## 전제조건
시작하기 전에 다음 필수 구성 요소가 있는지 확인하세요.
- Java 프로그래밍에 대한 기본 지식.
-  Java 라이브러리용 Aspose.Note가 설치되었습니다. 다음에서 다운로드할 수 있습니다.[Java 문서에 대한 Aspose.Note](https://reference.aspose.com/note/java/).
- 컴퓨터에 설치된 Java IDE(통합 개발 환경).
## 패키지 가져오기
필요한 패키지를 Java 프로젝트로 가져오는 것부터 시작하세요. 이렇게 하면 Java 기능용 Aspose.Note에 액세스할 수 있습니다.
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NumberList;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.ParagraphStyle;
// Java 패키지용 Aspose.Note 가져오기
```
## 1단계: 문서 및 페이지 초기화
Document 클래스의 객체를 생성하고 Page 클래스 객체를 초기화합니다.
```java
String dataDir = "Your Document Directory";
// Document 클래스의 객체 생성
Document doc = new Document();
// 페이지 클래스 객체 초기화
Page page = new Page();
```
## 2단계: 개요 및 텍스트 스타일 초기화
이제 서식 지정 속성을 사용하여 아웃라인 클래스 객체와 TextStyle 클래스 객체를 초기화합니다.
```java
// 개요 클래스 객체 초기화
Outline outline = new Outline();
// TextStyle 클래스 객체를 초기화하고 형식 지정 속성을 설정합니다.
ParagraphStyle defaultStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```
## 3단계: 글머리 기호 목록 요소 만들기
OutlineElement 클래스 개체를 만들고 글머리 기호를 적용하여 글머리 기호 목록을 만듭니다.
```java
// OutlineElement 클래스 객체 초기화 및 글머리 기호 적용
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("*", "Arial", 10));
// RichText 클래스 객체 초기화 및 텍스트 스타일 적용
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
```
글머리 기호 목록의 각 요소에 대해 위 단계를 반복합니다.
## 4단계: 개요에 개요 요소 추가
생성된 OutlineElement 개체를 개요에 추가합니다.
```java
// 개요 요소 추가
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```
## 5단계: 페이지에 개요 추가 및 저장
페이지에 개요 노드를 추가한 다음 문서에 페이지 노드를 추가합니다. 마지막으로 문서를 저장합니다.
```java
// 개요 노드 추가
page.appendChildLast(outline);
// 페이지 노드 추가
doc.appendChildLast(page);
// 문서를 저장하다
doc.save(dataDir + "CreateBulletedList_out.pdf");
```
축하해요! Java용 Aspose.Note를 사용하여 OneNote에서 글머리 기호 목록을 성공적으로 만들었습니다.
## 결론
Aspose.Note for Java는 올바른 형식의 문서를 만드는 과정을 단순화합니다. 이 자습서에서는 OneNote에서 글머리 기호 목록을 만드는 단계를 안내했습니다. Aspose.Note로 더 많은 가능성을 탐색하여 문서 작성 경험을 향상하세요.
## 자주 묻는 질문
### Aspose.Note for Java는 모든 Java IDE와 호환됩니까?
예, Aspose.Note for Java는 Eclipse 및 IntelliJ IDEA와 같은 널리 사용되는 Java 통합 개발 환경과 호환됩니다.
### 글머리 기호 목록의 형식을 사용자 정의할 수 있나요?
전적으로! 기본 설정에 따라 글머리 기호 목록 요소의 글꼴, 색상 및 크기를 수정할 수 있습니다.
### Java용 Aspose.Note에 대한 추가 지원은 어디서 찾을 수 있나요?
 방문하다[Java 지원 포럼에 대한 Aspose.Note](https://forum.aspose.com/c/note/28) 지역 사회의 도움을 요청합니다.
### Aspose.Note for Java에 대한 무료 평가판이 있습니까?
 예, 무료 평가판을 사용해 볼 수 있습니다[여기](https://releases.aspose.com/).
### Aspose.Note for Java의 임시 라이선스를 어떻게 얻을 수 있나요?
 임시 라이센스 받기[여기](https://purchase.aspose.com/temporary-license/).