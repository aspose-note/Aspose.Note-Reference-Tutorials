---
title: OneNote에서 노트북을 평면 이미지로 변환 - Aspose.Note
linktitle: OneNote에서 노트북을 평면 이미지로 변환 - Aspose.Note
second_title: Aspose.Note 자바 API
description: Java용 Aspose.Note를 사용하여 OneNote에서 노트북을 평면화된 이미지로 변환하는 방법을 알아보세요. 단일 이미지 파일의 모든 요소를 손쉽게 보존하세요.
weight: 13
url: /ko/java/onenote-notebook-operations/convert-notebook-to-flattened-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote에서 노트북을 평면 이미지로 변환 - Aspose.Note

## 소개

이 튜토리얼에서는 Aspose.Note for Java를 사용하여 OneNote에서 노트북을 평면화된 이미지로 변환하는 과정을 안내합니다. 이를 통해 노트북을 이미지 파일로 저장할 수 있어 모든 요소가 단일 이미지 형식으로 보존됩니다.

## 전제조건

시작하기 전에 다음 사항이 있는지 확인하세요.

1. 시스템에 JDK(Java Development Kit)가 설치되어 있습니다.
2.  Java 프로젝트에 다운로드 및 설정된 Java 라이브러리용 Aspose.Note입니다. 다음에서 라이브러리를 다운로드할 수 있습니다.[여기](https://releases.aspose.com/note/java/).
3. Java 프로그래밍에 대한 기본 지식.

## 패키지 가져오기

시작하려면 Aspose.Note for Java에서 필요한 패키지를 가져와야 합니다.

```java
import java.io.IOException;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## 1단계: 문서 디렉토리 설정

먼저 노트북 파일이 있는 디렉터리를 정의합니다.

```java
String dataDir = "Your Document Directory";
```

 바꾸다`"Your Document Directory"` 노트북 파일의 경로와 함께.

## 2단계: 노트북 로드

 다음으로, 다음을 사용하여 노트북 파일을 로드합니다.`Notebook` 수업:

```java
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

 반드시 교체하세요`"test.onetoc2"` 노트북 파일 이름으로.

## 3단계: 이미지 저장 옵션 설정

이제 노트북을 이미지로 저장하기 위한 옵션을 설정합니다. 저장 형식을 PNG로 지정하고 해상도를 400DPI로 설정하겠습니다.

```java
NotebookImageSaveOptions saveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
ImageSaveOptions documentSaveOptions = saveOptions.getDocumentSaveOptions();
documentSaveOptions.setResolution(400);
```

요구 사항에 따라 해상도를 조정할 수 있습니다.

## 4단계: 노트북 편평화

모든 요소가 단일 이미지로 병합되도록 하려면`flatten` 옵션`true`:

```java
saveOptions.setFlatten(true);
```

이렇게 하면 결과 이미지가 노트북의 레이아웃을 유지하게 됩니다.

## 5단계: 이미지 저장

마지막으로 노트북을 평면화된 이미지로 저장합니다.

```java
notebook.save(dataDir + "ExportImageasFlattenedNotebook_out.png", saveOptions);
```

 바꾸다`"ExportImageasFlattenedNotebook_out.png"` 원하는 출력 파일 이름으로.

## 결론

결론적으로 Java용 Aspose.Note를 사용하면 OneNote에서 노트북을 평면화된 이미지로 쉽게 변환할 수 있습니다. 이 프로세스를 통해 모든 요소가 단일 이미지 형식으로 보존되므로 쉽게 공유하고 볼 수 있습니다.

## FAQ

### Q1: 출력 이미지의 해상도를 조정할 수 있나요?

 A1: 예, 요구 사항에 따라 해상도를 수정하여 해상도를 조정할 수 있습니다.`setResolution` 메소드 매개변수.

### Q2: Aspose.Note는 내보내기를 위해 다른 이미지 형식을 지원합니까?

A2: 예, Aspose.Note는 노트북 내보내기를 위해 PNG, JPEG, BMP 등과 같은 다양한 이미지 형식을 지원합니다.

### Q3: 출력 이미지를 추가로 사용자 정의할 수 있나요?

A3: 예, Aspose.Note는 페이지 크기, 방향 및 품질 설정을 포함하여 출력 이미지를 사용자 정의하기 위한 광범위한 옵션을 제공합니다.

### Q4: Aspose.Note for Java에 사용할 수 있는 평가판이 있습니까?

 A4: 예, 다음 사이트에서 무료 평가판을 구할 수 있습니다.[여기](https://releases.aspose.com/).

### Q5: Java용 Aspose.Note에 대한 지원은 어디서 찾을 수 있나요?

 A5: Aspose.Note 포럼에서 지원과 리소스를 찾을 수 있습니다.[여기](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
