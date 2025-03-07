---
title: OneNote 문서의 표에서 행 텍스트 추출 - Aspose.Note
linktitle: OneNote 문서의 표에서 행 텍스트 추출 - Aspose.Note
second_title: Aspose.Note 자바 API
description: Java용 Aspose.Note를 사용하여 OneNote 테이블에서 행 텍스트를 손쉽게 추출하는 방법을 알아보세요. 원활한 통합을 위한 단계별 가이드를 따르세요.
weight: 13
url: /ko/java/onenote-table-manipulation/extract-row-text-from-table/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote 문서의 표에서 행 텍스트 추출 - Aspose.Note

## 소개
Java용 Aspose.Note를 사용하여 OneNote 문서의 테이블에서 행 텍스트를 추출하는 방법에 대한 포괄적인 튜토리얼에 오신 것을 환영합니다. Aspose.Note는 개발자가 Microsoft OneNote 파일을 원활하게 사용할 수 있게 해주는 강력한 Java 라이브러리입니다. 이 자습서에서는 프로세스를 단계별로 안내하여 OneNote 문서의 테이블에서 행 텍스트를 효율적으로 추출하는 방법을 보여줍니다.
## 전제조건
튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.
-  Java 라이브러리용 Aspose.Note: Java 라이브러리용 Aspose.Note가 설치되어 있는지 확인하세요. 다음에서 다운로드할 수 있습니다.[다운로드 링크](https://releases.aspose.com/note/java/).
- Java 개발 환경: 컴퓨터에 Java 개발 환경이 설정되어 있는지 확인하십시오.
- OneNote 문서: 행 텍스트를 추출하려는 테이블이 포함된 샘플 OneNote 문서(예: "Sample1.one")를 준비합니다.
## 패키지 가져오기
Java 프로젝트에서 필요한 Aspose.Note 패키지를 가져옵니다. 이렇게 하면 OneNote 문서 작업에 필요한 클래스와 메서드에 액세스할 수 있습니다.
```java
import java.io.IOException;
import java.util.List;
import java.util.stream.Collectors;
import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.RichText;
import com.aspose.note.Table;
import com.aspose.note.TableRow;
```
## 1단계: 문서 디렉터리 설정
```java
// 문서 디렉터리의 경로입니다.
String dataDir = "Your Document Directory";
```
## 2단계: OneNote 문서 로드
```java
// 문서를 Aspose.Note에 로드합니다.
Document document = new Document(dataDir + "Sample1.one", new LoadOptions());
```
## 3단계: 테이블 노드 가져오기
```java
// 테이블 노드 목록 가져오기
List<Table> nodes = (List<Table>) document.getChildNodes(Table.class);
```
## 4단계: 테이블과 행 반복
```java
// 행 개수 설정
int rowCount = 0;
for (Table table : nodes) {
    // 테이블 행을 통해 반복
    for (TableRow row : table) {
        rowCount++;
        // 텍스트 검색
        List<RichText> textNodes = (List<RichText>) row.getChildNodes(RichText.class);
        StringBuilder text = new StringBuilder();
        for (RichText richText : textNodes) {
            text = text.append(richText.getText().toString());
        }
        // 출력 화면에 텍스트 인쇄
        System.out.println(text);
    }
}
```
OneNote 문서의 각 테이블에 대해 이 단계를 반복하면 행 텍스트가 성공적으로 추출됩니다.
## 결론
축하해요! Java용 Aspose.Note를 사용하여 OneNote 문서의 테이블에서 행 텍스트를 추출하는 방법을 배웠습니다. 이 튜토리얼은 Java 애플리케이션에서 Aspose.Note의 강력한 기능을 활용하기 위한 기반을 제공합니다.
## 자주 묻는 질문
### Aspose.Note는 최신 버전의 Microsoft OneNote와 호환됩니까?
 Aspose.Note는 최신 버전을 포함하여 다양한 OneNote 버전을 지원합니다. 다음을 참조하세요.[선적 서류 비치](https://reference.aspose.com/note/java/) 호환성 세부정보를 확인하세요.
### 구매하기 전에 Java용 Aspose.Note를 사용해 볼 수 있나요?
예, Aspose.Note의 무료 평가판을 탐색할 수 있습니다.[이 링크](https://releases.aspose.com/).
### 추가 지원 및 도움은 어디서 찾을 수 있나요?
 방문하다[Aspose.Note 포럼](https://forum.aspose.com/c/note/28) 커뮤니티 지원 및 토론을 위해.
### Aspose.Note의 임시 라이선스는 어떻게 얻나요?
 임시 라이센스를 받으십시오.[이 링크](https://purchase.aspose.com/temporary-license/).
### Aspose.Note for Java를 사용하기 위한 특정 시스템 요구 사항이 있나요?
자세한 시스템 요구 사항은 설명서를 참조하세요.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
