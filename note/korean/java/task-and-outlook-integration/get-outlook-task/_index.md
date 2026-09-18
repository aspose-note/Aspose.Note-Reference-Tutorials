---
date: 2026-04-01
description: Aspose.Note for Java를 사용하여 Outlook에서 OneNote로 작업을 추출하는 방법을 배우세요. 단계별
  가이드를 따라 작업 세부 정보를 빠르게 가져오세요.
keywords:
- how to extract tasks
- Aspose.Note Java
- Outlook task extraction
linktitle: Outlook 작업을 OneNote에 가져오기 - Aspose.Note
second_title: Aspose.Note Java API
title: Aspose.Note를 사용하여 OneNote에서 Outlook 작업을 추출하는 방법
url: /ko/java/task-and-outlook-integration/get-outlook-task/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Outlook 작업을 OneNote에서 가져오기 - Aspose.Note

## 소개
Outlook에서 OneNote 노트북에 있는 **작업을 추출하는 방법**에 대한 포괄적인 가이드에 오신 것을 환영합니다. Aspose.Note for Java를 사용합니다. 마이그레이션 도구를 구축하거나, 보고서를 생성하거나, 단순히 작업 데이터를 동기화해야 할 때, 이 튜토리얼은 OneNote 파일을 로드하는 단계부터 각 Outlook 작업의 속성을 읽는 단계까지 모든 과정을 안내합니다. 끝까지 진행하면 자체 프로젝트에 적용할 수 있는 사용 준비가 된 코드 스니펫을 얻게 됩니다.

## 빠른 답변
- **이 튜토리얼은 무엇을 다루나요?** Aspose.Note for Java를 사용하여 OneNote 문서에서 Outlook 작업 세부 정보를 추출합니다.  
- **어떤 API가 사용되나요?** Aspose.Note Java 라이브러리.  
- **라이선스가 필요합니까?** 무료 체험판은 개발에 사용할 수 있으며, 상용 환경에서는 상업용 라이선스가 필요합니다.  
- **구현에 얼마나 걸립니까?** 환경이 설정되면 약 10‑15분 정도 소요됩니다.  
- **여러 노트북을 처리할 수 있나요?** 예—파일을 반복하고 동일한 로직을 재사용하면 됩니다.

## 작업 추출이란?
작업 추출은 Outlook이 OneNote 페이지 내부에 `NoteTask` 태그로 저장하는 구조화된 작업 정보(예: 마감일, 상태, 아이콘)를 읽는 것을 의미합니다. 이를 통해 수동 복사 없이도 작업 메타데이터에 프로그래밍 방식으로 접근할 수 있습니다.

## 왜 Aspose.Note for Java를 사용하나요?
- **Microsoft Office 불필요** – Java 런타임이 있는 모든 플랫폼에서 작동합니다.  
- **전체 충실도** – 모든 OneNote 요소를 보존하면서 태그에 직접 접근할 수 있습니다.  
- **고성능** – 대형 노트북 및 배치 처리에 최적화되었습니다.  

## 사전 요구 사항
시작하기 전에 다음이 준비되어 있는지 확인하십시오:

- **Java 개발 환경** – JDK 8 이상이 설치되고 구성되어 있어야 합니다.  
- **Aspose.Note 라이브러리** – 공식 사이트에서 최신 Java 패키지를 다운로드하십시오 [here](https://releases.aspose.com/note/java/).  
- **샘플 OneNote 파일** – 튜토리얼은 `Sample1.one`을 사용합니다; Outlook 작업이 포함된任意의 노트북으로 교체할 수 있습니다.

## 패키지 가져오기
필요한 import를 Java 클래스에 추가하십시오. 이러한 클래스는 문서 모델과 Outlook 전용 `NoteTask` 태그에 접근할 수 있게 해줍니다.

```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.ITag;
import com.aspose.note.NoteTask;
import com.aspose.note.RichText;
```

## 단계별 가이드

### 1단계: 문서 디렉터리 설정
OneNote 파일이 저장된 폴더를 정의합니다. 절대 경로나 상대 경로를 사용할 수 있지만, 가독성을 위해 경로 문자열을 깔끔하게 유지하십시오.

```java
String dataDir = "Your Document Directory";
```

### 2단계: OneNote 문서 로드
`Document` 인스턴스를 `.one` 파일을 가리키도록 생성합니다. Aspose.Note는 파일을 탐색 가능한 DOM 유사 구조로 파싱합니다.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

### 3단계: 모든 RichText 노드 가져오기
Outlook 작업은 `RichText` 요소 내부에 저장됩니다. 모든 `RichText` 노드를 가져와 태그를 검사할 수 있습니다.

```java
List<RichText> nodes = (List<RichText>) doc.getChildNodes(RichText.class);
```

### 4단계: 각 노드 반복 처리
각 `RichText` 노드를 순회하면서 태그를 검사하고 `NoteTask`를 만나면 작업합니다. 아래 코드는 각 작업에 대한 가장 유용한 속성을 출력합니다.

```java
for (RichText richText : nodes) {
    for (ITag tag : richText.getTags()) {
        if (tag.getClass() == NoteTask.class) {
            NoteTask noteTask = (NoteTask) tag;
            
            // Retrieve properties
            System.out.println("Completed Time: " + noteTask.getCompletedTime());
            System.out.println("Create Time: " + noteTask.getCreationTime());
            System.out.println("Due Date: " + noteTask.getDueDate());
            System.out.println("Status: " + noteTask.getStatus());
            System.out.println("Icon: " + noteTask.getIcon());
        }
    }
}
```

**팁:** 속성 중 일부만 필요하면 다른 속성을 건너뛰어 대형 노트북을 처리할 때 성능을 향상시킬 수 있습니다.

### 일반적인 문제 및 해결책
- **작업을 찾을 수 없음:** OneNote 페이지에 실제로 Outlook 작업이 포함되어 있는지 확인하십시오. 작은 Outlook 아이콘이 있는 체크박스로 표시됩니다.  
- **Null 값:** `CompletedTime`과 같은 일부 작업 필드는 작업이 완료되지 않은 경우 `null`일 수 있습니다. 출력하기 전에 `null`을 확인하여 `NullPointerException`을 방지하십시오.  
- **파일을 찾을 수 없음:** `dataDir`이 OS에 맞는 경로 구분자(`/` 또는 `\\`)로 끝나는지 확인하십시오.

## 결론
축하합니다! Aspose.Note Java API를 사용하여 OneNote에서 Outlook 작업을 **추출하는 방법**을 배웠습니다. 이 접근 방식은 작업 데이터에 대한 완전한 프로그래밍 제어를 제공하여 맞춤형 보고 도구, 데이터베이스 또는 기타 비즈니스 워크플로와의 통합을 가능하게 합니다.

## 자주 묻는 질문

**Q: Aspose.Note가 모든 버전의 OneNote와 호환됩니까?**  
A: Aspose.Note는 Microsoft OneNote 2010 및 이후 버전을 지원합니다.

**Q: Aspose.Note를 개인 및 상업 프로젝트 모두에 사용할 수 있나요?**  
A: 예, Aspose.Note는 개인 및 상업 프로젝트 모두에 사용할 수 있습니다. 라이선스 옵션을 확인하려면 [here](https://purchase.aspose.com/buy) 를 방문하십시오.

**Q: Aspose.Note의 무료 체험판이 있나요?**  
A: 예, 무료 체험판은 [here](https://releases.aspose.com/) 에서 이용할 수 있습니다.

**Q: Aspose.Note에 대한 지원을 어떻게 받을 수 있나요?**  
A: [Aspose.Note 포럼](https://forum.aspose.com/c/note/28)에서 커뮤니티 지원을 받을 수 있습니다. 추가 지원이 필요하면 [temporary license](https://purchase.aspose.com/temporary-license/) 구매를 고려하십시오.

**Q: 테스트용 샘플 OneNote 문서가 있나요?**  
A: Aspose.Note 문서에서 샘플 문서를 [here](https://reference.aspose.com/note/java/) 에서 찾을 수 있습니다.

---

**마지막 업데이트:** 2026-04-01  
**테스트 환경:** Aspose.Note for Java 24.12 (작성 시 최신)  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}