---
title: OneNote의 옵션을 사용하여 노트북을 이미지로 변환 - Aspose.Note
linktitle: OneNote의 옵션을 사용하여 노트북을 이미지로 변환 - Aspose.Note
second_title: Aspose.Note 자바 API
description: Aspose.Note for Java를 사용하여 옵션을 사용하여 노트북을 이미지로 변환하는 방법을 알아보세요. Java 애플리케이션에 원활하게 통합하려면 단계별 튜토리얼을 따르십시오.
type: docs
weight: 14
url: /ko/java/onenote-notebook-operations/convert-notebook-to-image-with-options/
---
## 소개

이번 튜토리얼에서는 Aspose.Note for Java를 사용하여 노트북을 다양한 옵션으로 이미지로 변환하는 과정을 살펴보겠습니다. Aspose.Note는 개발자가 Microsoft OneNote 파일을 프로그래밍 방식으로 작업하여 Java 애플리케이션에 원활하게 통합할 수 있도록 하는 강력한 Java API입니다.

## 전제조건

시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

1. JDK(Java Development Kit): 시스템에 JDK가 설치되어 있는지 확인하세요.
2. Java JAR 파일용 Aspose.Note: 다음 위치에서 Java용 Aspose.Note 라이브러리를 다운로드하세요.[여기](https://releases.aspose.com/note/java/) 프로젝트의 클래스 경로에 포함시킵니다.

## 패키지 가져오기

먼저 Java 애플리케이션에 필요한 패키지를 가져옵니다.

```java
import java.io.IOException;

import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## 1단계: 노트북 로드

시작하려면 이미지로 변환하려는 OneNote 노트북을 로드해야 합니다.

```java
String dataDir = "Your Document Directory";
// OneNote 전자 필기장 로드
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

## 2단계: 저장 옵션 설정

다음으로 원하는 형식(PNG, JPEG 등)과 해상도를 포함한 이미지 저장 옵션을 정의하겠습니다.

```java
NotebookImageSaveOptions notebookSaveOptions = new NotebookImageSaveOptions(SaveFormat.Png);

ImageSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();

documentSaveOptions.setResolution(400);
```

## 3단계: 노트북을 이미지로 저장

이제 지정된 옵션을 사용하여 노트북을 이미지로 저장하겠습니다.

```java
dataDir = dataDir + "ExportNotebooktoImagewithOptions_out.png";

// 노트북 저장
notebook.save(dataDir, notebookSaveOptions);
```

## 결론

이 튜토리얼에서는 Aspose.Note for Java를 사용하여 다양한 옵션을 사용하여 노트북을 이미지로 변환하는 방법을 배웠습니다. 다음 단계를 수행하면 이 기능을 Java 응용 프로그램에 원활하게 통합하여 OneNote 파일을 프로그래밍 방식으로 조작할 수 있는 가능성이 열립니다.

## FAQ

### Q1: Aspose.Note가 복잡한 OneNote 파일을 처리할 수 있나요?

A1: 예, Aspose.Note는 복잡한 OneNote 파일을 효율적으로 처리할 수 있으므로 프로그래밍 방식으로 다양한 작업을 수행할 수 있습니다.

### Q2: Aspose.Note for Java는 기존 프로젝트에 쉽게 통합됩니까?

A2: 물론이죠! Aspose.Note for Java는 Java 프로젝트에 쉽게 통합할 수 있는 간단한 API를 제공하여 시간과 노력을 절약해 줍니다.

### Q3: 노트북을 변환할 때 이미지 출력을 사용자 정의할 수 있나요?

A3: 예, Aspose.Note를 사용하면 해상도, 형식 등과 같은 옵션을 지정하여 이미지 출력을 사용자 정의할 수 있습니다.

### Q4: Aspose.Note는 개발자를 지원합니까?

A4: 예, Aspose는 포럼과 문서를 통해 개발자에게 탁월한 지원을 제공하여 원활한 통합과 문제 해결을 보장합니다.

### Q5: Aspose.Note for Java에 대한 무료 평가판이 있습니까?

 A5: 예, 다음에서 Aspose.Note for Java 무료 평가판을 이용할 수 있습니다.[여기](https://releases.aspose.com/).