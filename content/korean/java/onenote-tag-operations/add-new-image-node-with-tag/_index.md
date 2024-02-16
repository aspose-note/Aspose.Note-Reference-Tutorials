---
title: OneNote에서 태그가 포함된 새 이미지 노드 추가 - Aspose.Note
linktitle: OneNote에서 태그가 포함된 새 이미지 노드 추가 - Aspose.Note
second_title: Aspose.Note 자바 API
description: Java용 Aspose.Note를 사용하여 OneNote에서 태그가 있는 새 이미지 노드를 추가하는 방법을 알아보세요. Java 프로그래밍 기술을 손쉽게 향상시켜 보세요.
type: docs
weight: 10
url: /ko/java/onenote-tag-operations/add-new-image-node-with-tag/
---
## 소개
Java 프로그래밍 영역에서 Aspose.Note는 OneNote 문서를 쉽게 처리할 수 있는 강력한 도구로 돋보입니다. 기술을 향상시키고 Aspose.Note를 사용하여 OneNote에서 태그가 포함된 새 이미지 노드를 추가하는 방법을 배우고 싶다면 잘 찾아오셨습니다. 이 단계별 가이드는 각 개념을 철저하게 이해할 수 있도록 프로세스를 안내합니다.
## 전제조건
튜토리얼을 시작하기 전에 필요한 모든 것이 갖추어져 있는지 확인하십시오.
1.  Java용 Aspose.Note: Aspose.Note 라이브러리가 설치되어 있는지 확인하세요. 그렇지 않은 경우 다운로드할 수 있습니다.[여기](https://releases.aspose.com/note/java/).
2. Java 개발 환경: 컴퓨터에 작동 중인 Java 개발 환경이 설정되어 있는지 확인하세요.
이제 전제 조건이 준비되었으므로 다음 단계로 넘어가겠습니다.
## 패키지 가져오기
Java 프로젝트에서 필요한 패키지를 가져오는 것부터 시작하세요.
```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Image;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
import com.aspose.note.TagIcon;
```
## 1단계: 문서 개체 만들기
```java
// 문서 디렉터리의 경로입니다.
String dataDir = "Your Document Directory";
// Document 클래스의 객체 생성
Document doc = new Document();
```
## 2단계: 페이지 클래스 개체 초기화
```java
// 페이지 클래스 객체 초기화
Page page = new Page();
```
## 3단계: 개요 클래스 개체 초기화
```java
// 개요 클래스 객체 초기화
Outline outline = new Outline();
```
## 4단계: OutlineElement 클래스 객체 초기화
```java
// OutlineElement 클래스 객체 초기화
OutlineElement outlineElem = new OutlineElement();
```
## 5단계: 이미지 로드 및 삽입
```java
// 이미지 로드
Image image = new Image(null, dataDir + "Input.jpg");
// 문서 노드에 이미지 삽입
outlineElem.appendChildLast(image);
```
## 6단계: 이미지에 메모 태그 추가
```java
// 이미지에 노란색 별표 태그를 추가하세요.
NoteTag noteTag = NoteTag.createYellowStar();
image.getTags().add(noteTag);
```
## 7단계: 개요 요소 노드 추가
```java
// 개요 요소 노드 추가
outline.appendChildLast(outlineElem);
```
## 8단계: 개요 노드 추가
```java
// 개요 노드 추가
page.appendChildLast(outline);
```
## 9단계: 페이지 노드 추가
```java
// 페이지 노드 추가
doc.appendChildLast(page);
```
## 10단계: OneNote 문서 저장
```java
// OneNote 문서를 PDF로 저장
doc.save(dataDir + "AddNewImageNodeWithTag_out.pdf", SaveFormat.Pdf);
```
축하해요! Java용 Aspose.Note를 사용하여 OneNote에 태그가 포함된 새 이미지 노드를 성공적으로 추가했습니다.
## 결론
 Java용 Aspose.Note를 마스터하면 OneNote 문서 조작에 흥미로운 가능성이 열립니다. 이 튜토리얼을 따라하면 다양한 프로젝트에 적용할 수 있는 실용적인 기술을 습득하게 됩니다. Aspose.Note 문서를 계속 탐색하세요.[여기](https://reference.aspose.com/note/java/)더 많은 고급 기능과 가능성을 확인하세요.
## 자주 묻는 질문
### Aspose.Note 문서는 어디서 찾을 수 있나요?
 문서를 찾을 수 있습니다[여기](https://reference.aspose.com/note/java/).
### Java용 Aspose.Note를 어떻게 다운로드하나요?
 릴리스 페이지에서 다운로드할 수 있습니다.[여기](https://releases.aspose.com/note/java/).
### 무료 평가판이 제공되나요?
 예, 무료 평가판에 액세스할 수 있습니다[여기](https://releases.aspose.com/).
### Aspose.Note에 대한 지원은 어디서 받을 수 있나요?
 커뮤니티 포럼 방문[여기](https://forum.aspose.com/c/note/28) 지원을 위해.
### 임시 라이센스가 필요합니까?
 필요한 경우 임시 라이센스를 얻을 수 있습니다.[여기](https://purchase.aspose.com/temporary-license/).