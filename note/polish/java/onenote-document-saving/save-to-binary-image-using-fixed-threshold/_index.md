---
title: Zapisz w obrazie binarnym przy użyciu stałego progu w programie OneNote
linktitle: Zapisz w obrazie binarnym przy użyciu stałego progu w programie OneNote
second_title: Aspose.Note API Java
description: Bez wysiłku zapisuj dokumenty Microsoft OneNote jako obrazy binarne, korzystając ze stałego progu w Aspose.Note Java. Zwiększ swoje możliwości manipulowania plikami OneNote.
weight: 14
url: /pl/java/onenote-document-saving/save-to-binary-image-using-fixed-threshold/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zapisz w obrazie binarnym przy użyciu stałego progu w programie OneNote

## Wstęp

Aspose.Note dla Java to potężny interfejs API, który umożliwia programistom programową pracę z plikami Microsoft OneNote. W tym samouczku omówimy, jak zapisać dokument jako obraz binarny przy użyciu stałego progu. Aby to osiągnąć, wykonaj poniższe czynności.

## Warunki wstępne

Zanim zaczniesz, upewnij się, że masz następujące elementy:

1. Zestaw Java Development Kit (JDK) zainstalowany w systemie.
2.  Pobrano bibliotekę Aspose.Note dla Java. Można go pobrać z[Tutaj](https://releases.aspose.com/note/java/).
3. Podstawowa znajomość programowania w języku Java.

## Importuj pakiety

Najpierw zaimportuj niezbędne pakiety do pliku Java.

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Krok 1: Załaduj dokument

Załaduj dokument OneNote za pomocą interfejsu API Aspose.Note.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Krok 2: Ustaw opcje binaryzacji

Zdefiniuj opcje binaryzacji w celu zapisania dokumentu jako obrazu binarnego.

```java
dataDir = dataDir + "SaveToBinaryImageUsingFixedThreshold_out.png";
ImageBinarizationOptions binarizationOptions = new ImageBinarizationOptions();
binarizationOptions.setBinarizationMethod(BinarizationMethod.FixedThreshold);
binarizationOptions.setBinarizationThreshold(123);
```

## Krok 3: Ustaw opcje zapisywania obrazu

Ustaw opcje zapisywania obrazu, w tym tryb koloru i opcje binaryzacji.

```java
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.BlackAndWhite);
options.setBinarizationOptions(binarizationOptions);
```

## Krok 4: Zapisz dokument

Zapisz dokument jako obraz binarny z określonymi opcjami.

```java
oneFile.save(dataDir, options);
```

## Wniosek

tym samouczku nauczyliśmy się, jak zapisać dokument jako obraz binarny przy użyciu stałego progu w Aspose.Note dla Java. Wykonując poniższe kroki, można łatwo programowo manipulować plikami programu OneNote.

## Często zadawane pytania

### P1: Czy mogę dostosować wartość progową dla binaryzacji?

 A1: Tak, możesz dostosować wartość progową zgodnie ze swoimi wymaganiami, modyfikując`setBinarizationThreshold()` parametr metody.

### P2: Czy Aspose.Note dla Java jest kompatybilny ze wszystkimi wersjami Microsoft OneNote?

O2: Aspose.Note dla Java obsługuje różne wersje Microsoft OneNote, w tym 2010, 2013 i 2016.

### P3: Czy istnieją jakieś ograniczenia dotyczące rozmiaru dokumentów, które można przetwarzać?

O3: Aspose.Note dla Java nie ma ograniczeń co do rozmiaru dokumentów, które można przetworzyć, co pozwala efektywnie obsługiwać duże pliki.

### P4: Czy mogę jednocześnie konwertować wiele dokumentów programu OneNote?

O4: Tak, możesz przetwarzać wsadowo wiele dokumentów OneNote, iterując po każdym pliku i wykonując niezbędne operacje.

### P5: Czy dostępna jest pomoc techniczna dla Aspose.Note dla Java?

 Odpowiedź 5: Tak, pomoc techniczna jest dostępna za pośrednictwem[Forum Aspose.Note](https://forum.aspose.com/c/note/28), gdzie możesz zadawać pytania i szukać pomocy ekspertów.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
