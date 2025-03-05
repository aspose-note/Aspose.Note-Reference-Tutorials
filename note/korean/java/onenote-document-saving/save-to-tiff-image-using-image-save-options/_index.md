---
title: OneNote의 이미지 저장 옵션을 사용하여 TIFF 이미지에 저장
linktitle: OneNote의 이미지 저장 옵션을 사용하여 TIFF 이미지에 저장
second_title: Aspose.Note 자바 API
description: OneNote 문서를 TIFF로 변환하고 파일 크기와 품질을 제어하세요! Java에서 Jpeg, PackBits 또는 팩스 압축을 선택합니다. 코드 예제를 받고 방법을 알아보세요! #OneNote #Java #Aspose
type: docs
weight: 21
url: /ko/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
---
## 소개

이 튜토리얼에서는 Java용 Aspose.Note에서 다양한 압축 방법을 사용하여 문서를 TIFF 이미지 형식으로 저장하는 방법을 배웁니다. 전제 조건, 패키지 가져오기를 다루고 각 압축 방법에 대한 단계별 가이드를 제공합니다.

## 전제조건

시작하기 전에 다음 사항이 있는지 확인하세요.

- 시스템에 JDK(Java Development Kit)가 설치되어 있습니다.
- 다운로드 및 구성된 Java 라이브러리용 Aspose.Note입니다.
- Java 프로그래밍 언어에 대한 기본 이해.

## 패키지 가져오기

먼저 필요한 패키지를 Java 파일로 가져와야 합니다.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## 1단계: JPEG 압축을 사용하여 TIFF에 저장

```java
public static void SaveToTiffUsingJpegCompression() throws IOException {
    // 문서 디렉터리의 경로입니다.
    String dataDir = "Your Document Directory";

    // 문서를 Aspose.Note에 로드합니다.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.Jpeg);
    options.setQuality(93);

    oneFile.save(Paths.get(dataDir,"SaveToTiffUsingJpegCompression.tiff").toString(), options);
}
```

-  다음을 사용하여 문서를 로드합니다.`Document` 수업.
-  인스턴스 만들기`ImageSaveOptions` TIFF 압축 유형을 JPEG로 지정합니다.
- 원하는 품질을 설정합니다(선택 사항).
- 지정된 옵션을 사용하여 문서를 TIFF 형식으로 저장합니다.

## 2단계: PackBits 압축을 사용하여 TIFF에 저장

```java
public static void SaveToTiffUsingPackBitsCompression() throws IOException {
    // 문서 디렉터리의 경로입니다.
    String dataDir = "Your Document Directory";

    // 문서를 Aspose.Note에 로드합니다.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.PackBits);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingPackBitsCompression.tiff").toString(), options);
}
```

-  다음을 사용하여 문서를 로드합니다.`Document` 수업.
-  인스턴스 만들기`ImageSaveOptions` TIFF 압축 유형을 PackBits로 지정합니다.
- 지정된 옵션을 사용하여 문서를 TIFF 형식으로 저장합니다.

## 3단계: CCITT 그룹 3 팩스 압축을 사용하여 TIFF에 저장

```java
public static void SaveToTiffUsingCcitt3Compression() throws IOException {
    // 문서 디렉터리의 경로입니다.
    String dataDir = "Your Document Directory";

    // 문서를 Aspose.Note에 로드합니다.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setColorMode(ColorMode.BlackAndWhite);
    options.setTiffCompression(TiffCompression.Ccitt3);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingCcitt3Compression.tiff").toString(), options);
}
```

-  다음을 사용하여 문서를 로드합니다.`Document` 수업.
-  인스턴스 만들기`ImageSaveOptions` TIFF 압축 유형을 CCITT 그룹 3 팩스로 지정합니다.
- 색상 모드를 흑백으로 설정하세요.
- 지정된 옵션을 사용하여 문서를 TIFF 형식으로 저장합니다.

## 결론

이 튜토리얼에서는 Java용 Aspose.Note에서 다양한 압축 방법을 사용하여 문서를 TIFF 이미지 형식으로 저장하는 방법을 배웠습니다. 단계별 가이드를 따르면 Aspose.Note의 기능을 효율적으로 활용하여 요구 사항을 충족할 수 있습니다.

## FAQ

### Q1: Aspose.Note for Java를 사용하여 다른 문서 형식을 TIFF로 변환할 수 있나요?

A1: 예, Java용 Aspose.Note는 OneNote 문서를 포함하여 다양한 문서 형식에서 TIFF로의 변환을 지원합니다.

### Q2: TIFF로 저장할 때 압축 유형을 지정하는 것은 무엇을 의미합니까?

A2: 압축 유형을 지정하면 이미지 품질과 파일 크기를 제어할 수 있습니다. 다양한 압축 방법은 품질과 압축 비율 간의 균형을 제공합니다.

### Q3: Aspose.Note for Java가 문서 일괄 처리에 적합합니까?

A3: 예, Aspose.Note for Java는 일괄 처리용 API를 제공하여 문서 변환 작업을 효율적으로 자동화할 수 있습니다.

### Q4: 압축 설정을 추가로 사용자 정의할 수 있습니까?

A4: 예, 품질, 해상도, 압축 방법 등의 매개변수를 조정하여 요구 사항에 따라 출력을 맞춤화할 수 있습니다.

### Q5: Aspose.Note for Java는 기술 지원을 제공합니까?

A5: 네, Aspose는 포럼과 티켓 기반 시스템을 통해 포괄적인 기술 지원을 제공합니다.