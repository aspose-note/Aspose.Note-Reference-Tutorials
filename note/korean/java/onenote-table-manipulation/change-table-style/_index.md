---
date: 2026-01-20
description: Aspose.Note for Java를 사용하여 OneNote에서 표 스타일을 변경하고 표 행 배경 색상을 설정하는 방법을
  배우세요. 배경 색상 적용, 굵은 텍스트 적용 및 OneNote 문서 저장을 위한 단계별 가이드를 따라보세요.
linktitle: Change Table Style in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Aspose.Note를 사용하여 OneNote에서 표 스타일 변경 방법
url: /ko/java/onenote-table-manipulation/change-table-style/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote에서 Aspose.Note을 사용하여 표 스타일 변경하는 방법

## 소개
OneNote 노트북에서, Aspose.Note for Java를 사용하면 손쉽게 할 수 있습니다. 이 튜토리얼에서는 OneNote 파일을 로드하고, 표 행 배경 색상을 설정하고, 굵게 및 기울임꼴 서식을 적용한 다음, 업데이트된 문서를 저장하는 전체 과정을 단계별로 안내합니다. 끝까지 진행하면 OneNote 표 서식에 익숙해지고, 행에 배경 색을 적용하는 방법을 알게 되며, 새로운 스타일을 적용한 OneNote 문서를 저장하는 방법을.  
-RowStyle`하게합니다- ** Library** – [download page](https://releases.aspose.com/note/java/)에서 다운로드합니다.  
- **Document Directory** – `.one` 파일이 위치할 폴더입니다.  

## 패키지 가져오기
Java 프로젝트에서 Aspose.Note와 작업하기 위해 필요한 패키지를 가져옵니다:
```java
import com.aspose.note.*;
import java.awt.Color;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.List;
```

## 단계 1: 문서 설정
OneNote 문서를 Aspose.Note에 로드하고 표 노드 목록을 가져옵니다.
```java
// Set up the document and get the list of table nodes
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "ChangeTableStyleIn.one");
List<Table> nodes = document.getChildNodes(Table.class);
```

## 단계 2: 행 스타일 설정
각 표를 순회하면서 각 행의 스타일을 설정하고, 헤더 다음 첫 번째 행을 강조합니다. 이는 **set table row background**와 **how to apply background color**를 보여줍니다.
```java
// Set row styles for each table in the document
for (Table table : nodes) {
    setRowStyle(table.getFirstChild(), Color.GRAY, true, true);
    // Highlight first row after the head.
    boolean flag = false;
    List<TableRow> rows = table.getChildren();
    for (int i = 1; i < rows.size(); ++i) {
        setRowStyle(rows.get(i), flag ? Color.lightGray : new java.awt.Color(-1, true), false, false);
        flag = !flag;
    }
}
```

## setRowStyle 메서드
헬퍼 메서드는 행의 모든 셀에 배경 색상, 굵게 및 기울임꼴 서식을 적용합니다. 여기서 **how to bold text in onenote**가 구현됩니다.
```java
    private static void setRowStyle(TableRow row, Color highlightColor, boolean bold, boolean italic) {
        for (TableCell cell: row)
        {
            cell.setBackgroundColor(highlightColor);
            for (RichText node: cell.getChildNodes(RichText.class))
            {
                node.getParagraphStyle().setBold(bold);
                node.getParagraphStyle().setItalic(italic);
                for (TextRun run: node.getTextRuns())
                {
                    run.getStyle().setBold(bold);
                    run.getStyle().setItalic(italic);
                }
            }
        }
    }
```

## 단계 3: 문서 저장
표에 스타일을 적용한 후, 수정된 문서를 저장합니다. 이는 새로운 서식이 적용된 **how to save onenote document**를 보여줍니다.
```java
// Save the modified document
document.save(Paths.get(dataDir, "ChangeTableStyleOut.one").toString());
```

## 결론
Aspose.Note for Java는 OneNote 파일을 조작하는 과정을 단순화합니다. 라이브러리의 기능을 활용하면 표 스타일을 쉽게 변경하고, 표 행 배경 색상을 설정하며, 텍스트를 굵게 하고, OneNote 문서를 저장할 수 있습니다—모두 몇 줄의 코드만으로 가능합니다.

## 자주 묻는 질문
### Aspose.Note for Java 문서는 어디에서 찾을 수 있나요?
포괄적인 가이드를 보려면 [documentation](https://reference.aspose.com/note/java/)을 방문하세요.

### Aspose.Note for Java 임시 라이선스를 어떻게 얻을 수 있나요?
임시 라이선스를 받으려면 이 [link](https://purchase.aspose.com/temporary-license/)를 따라가세요.

### Aspose.Note for Java 무료 체험판이 있나요?
예, [here](https://releases.aspose.com/)에서 무료 체험판을 다운로드할 수 있습니다.

### Aspose.Note for Java 지원은 어디서 받을 수 있나요?
커뮤니티로부터 도움을 받으려면 [Aspose.Note forum](https://forum.aspose.com/c/note/28)에 참여하세요.

### Aspose.Note for Java를 어떻게 구매하나요?
라이브러리는 [here](https://purchase.aspose.com/buy)에서 구매할 수 있습니다.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-20  
**Tested With:** Aspose.Note for Java 24.11  
**Author:** Aspose