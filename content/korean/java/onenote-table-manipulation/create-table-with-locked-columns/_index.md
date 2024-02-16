---
title: OneNote에서 잠긴 열이 있는 테이블 만들기 - Aspose.Note
linktitle: OneNote에서 잠긴 열이 있는 테이블 만들기 - Aspose.Note
second_title: Aspose.Note 자바 API
description: Java용 Aspose.Note로 OneNote 경험을 향상하세요. 단계별 가이드를 사용하여 잠긴 열이 있는 테이블을 만드는 방법을 알아보세요. 지금 무료 평가판을 다운로드하세요!
type: docs
weight: 12
url: /ko/java/onenote-table-manipulation/create-table-with-locked-columns/
---
## 소개
OneNote는 정보를 정리하는 강력한 도구이며, Aspose.Note for Java는 잠긴 열이 있는 테이블을 생성하는 원활한 방법을 제공하여 기능을 향상시킵니다. 이 튜토리얼에서는 Java용 Aspose.Note를 사용하여 OneNote에서 잠긴 열이 있는 테이블을 만드는 과정을 안내합니다.
## 전제조건
시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.
- [JDK(자바 개발 키트)](https://www.oracle.com/java/technologies/javase-downloads.html)귀하의 컴퓨터에 설치되었습니다.
- [Java용 Aspose.Note](https://downloads.aspose.com/note/java) 라이브러리가 다운로드되어 프로젝트에 추가되었습니다.
## 패키지 가져오기
Java 프로젝트에서 Aspose.Note 작업에 필요한 패키지를 가져옵니다.
```java
import com.aspose.note.*;
import java.io.IOException;
```
## 1단계: 프로젝트 설정
새로운 Java 프로젝트를 생성하고 Aspose.Note 라이브러리를 클래스 경로에 추가하는 것부터 시작하세요. 프로젝트가 JDK를 사용하도록 구성되었는지 확인하세요.
## 2단계: 문서 및 페이지 개체 초기화
```java
// 문서 디렉터리의 경로입니다.
String dataDir = "Your Document Directory";
//Document 클래스의 객체 생성
Document doc = new Document();
// 페이지 클래스 객체 초기화
Page page = new Page();
```
## 3단계: 표 행 및 셀 만들기
```java
// TableRow 클래스 객체 초기화
TableRow row1 = new TableRow();
// TableCell 클래스 객체 초기화 및 텍스트 내용 설정
TableCell cell11 = new TableCell();
cell11.appendChildLast(InsertTable.GetOutlineElementWithText("Small text"));
row1.appendChildLast(cell11);
// TableRow 클래스 객체 초기화
TableRow row2 = new TableRow();
// TableCell 클래스 객체 초기화 및 텍스트 내용 설정
TableCell cell21 = new TableCell();
cell21.appendChildLast(InsertTable.GetOutlineElementWithText("Long   text    with    several   words and    spaces."));
row2.appendChildLast(cell21);
```
## 4단계: 테이블 생성 및 사용자 지정
```java
// 테이블 클래스 객체 초기화
Table table = new Table();
table.setBordersVisible(true);
TableColumn col = new TableColumn();
col.setWidth(200);
col.setLockedWidth(true);
table.getColumns().addItem(col);
// 행 추가
table.appendChildLast(row1);
table.appendChildLast(row2);
```
## 5단계: 개요 및 페이지에 표 추가
```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
// 테이블 노드 추가
outlineElem.appendChildLast(table);
// 개요 요소 노드 추가
outline.appendChildLast(outlineElem);
// 개요 노드 추가
page.appendChildLast(outline);
// 페이지 노드 추가
doc.appendChildLast(page);
```
## 6단계: 문서 저장
```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```
축하해요! Java용 Aspose.Note를 사용하여 OneNote에서 잠긴 열이 있는 테이블을 성공적으로 만들었습니다.
## 결론
이 튜토리얼에서는 잠긴 열이 있는 테이블을 생성하여 OneNote 경험을 향상시키기 위해 Java용 Aspose.Note를 활용하는 프로세스를 살펴보았습니다. 이 기능은 메모에 새로운 조직 및 구조 계층을 추가합니다.
## 자주 묻는 질문
### Aspose.Note for Java는 모든 Java 버전과 호환됩니까?
예, Java용 Aspose.Note는 Java 6 이상 버전과 호환됩니다.
### 테이블의 모양을 추가로 사용자 정의할 수 있나요?
전적으로! Aspose.Note for Java는 테두리 조정, 셀 간격 등과 같은 테이블 사용자 정의를 위한 광범위한 옵션을 제공합니다.
### 구매하기 전에 체험판을 사용할 수 있나요?
 그래 넌 할수있어[무료 평가판을 다운로드하세요](https://releases.aspose.com/) Java용 Aspose.Note의 기능을 탐색합니다.
### 추가 지원이나 커뮤니티 토론은 어디서 찾을 수 있나요?
 방문하다[Aspose.Note 포럼](https://forum.aspose.com/c/note/28) 지원 및 커뮤니티 토론을 위해.
### Aspose.Note for Java의 임시 라이선스를 어떻게 얻을 수 있나요?
 방문하다[이 링크](https://purchase.aspose.com/temporary-license/) 테스트 목적으로 임시 라이센스를 취득합니다.