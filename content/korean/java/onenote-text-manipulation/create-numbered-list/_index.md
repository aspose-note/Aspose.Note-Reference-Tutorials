---
title: OneNote에서 번호 매기기 목록 만들기 - Aspose.Note
linktitle: OneNote에서 번호 매기기 목록 만들기 - Aspose.Note
second_title: Aspose.Note 자바 API
description: Java용 Aspose.Note를 사용하여 OneNote에서 번호 매기기 목록을 쉽게 만드는 방법을 알아보세요. 무료 평가판을 다운로드하고 Java 개발의 세계에 빠져보세요!
type: docs
weight: 14
url: /ko/java/onenote-text-manipulation/create-numbered-list/
---
## 소개
Aspose.Note for Java는 Java 개발자가 Microsoft OneNote 파일을 원활하게 사용할 수 있도록 지원합니다. 이 자습서에서는 강력한 Java용 Aspose.Note 라이브러리를 사용하여 OneNote에서 번호 매기기 목록을 작성하는 과정을 안내합니다.
## 전제조건
튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.
- 컴퓨터에 JDK(Java Development Kit)를 설치했습니다.
-  Aspose.Note에서 다운로드한 Java 라이브러리용[여기](https://releases.aspose.com/note/java/).
## 패키지 가져오기
먼저 Aspose.Note 기능을 최대한 활용하기 위해 Java 프로젝트에 필요한 패키지를 가져옵니다. 프로젝트에 다음 코드를 포함합니다.
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NumberFormat;
import com.aspose.note.NumberList;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.ParagraphStyle;
```
## 1단계: 문서, 페이지 및 개요 개체 초기화
```java
// 귀하의 문서 디렉토리
String dataDir = "Your Document Directory";
// 문서, 페이지 및 개요 개체 만들기
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
// 기본 텍스트 스타일 설정
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
```
## 2단계: 기본 텍스트 스타일 설정
```java
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
```
## 3단계: 개요 요소 생성
이제 번호가 매겨진 목록의 요소를 만들어 보겠습니다.
```java
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10));
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
// 다른 요소(outlineElem2 및outlineElem3)에 대해 반복합니다.
```
## 4단계: 개요에 개요 요소 추가
```java
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```
## 5단계: 페이지에 개요 추가
```java
page.appendChildLast(outline);
```
## 6단계: 문서 저장
```java
doc.appendChildLast(page);
doc.save(dataDir + "CreateNumberedList_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "CreateNumberedList_out.pdf");
```
다음 단계를 꼼꼼하게 수행하면 Java용 Aspose.Note를 사용하여 OneNote에서 번호가 매겨진 목록을 쉽게 만들 수 있습니다.
## 결론
이 튜토리얼에서는 Java용 Aspose.Note를 사용하여 OneNote에서 번호 매기기 목록을 만드는 원활한 프로세스를 살펴보았습니다. 라이브러리의 강력한 기능은 Microsoft OneNote 파일을 사용하는 Java 개발자에게 매우 귀중한 도구입니다.
## 자주 묻는 질문
### Q: OneNote 목록에서 번호 매기기 형식을 사용자 지정할 수 있나요?
답: 물론이죠! Aspose.Note for Java에서 제공하는 NumberList 클래스를 사용하여 번호 매기기 형식을 사용자 정의할 수 있습니다.
### Q: Aspose.Note for Java에 사용할 수 있는 평가판이 있나요?
 A: 예, 무료 평가판을 다운로드할 수 있습니다.[여기](https://releases.aspose.com/).
### Q: Java용 Aspose.Note에 대한 지원을 어떻게 받을 수 있나요?
 답: 다음을 방문하세요.[Aspose.Note for Java 포럼](https://forum.aspose.com/c/note/28) 지역 사회 지원을 위해.
### Q: Aspose.Note for Java에 대한 자세한 문서는 어디서 찾을 수 있나요?
 답: 다음을 참조하세요.[선적 서류 비치](https://reference.aspose.com/note/java/) 포괄적인 정보를 얻으려면.
### Q: Aspose.Note for Java 라이선스는 어떻게 구매하나요?
 A: 라이센스를 구입할 수 있습니다.[여기](https://purchase.aspose.com/buy).