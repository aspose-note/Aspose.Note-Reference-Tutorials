---
title: Zapisz w obrazie w skali szarości w programie OneNote — Aspose.Note
linktitle: Zapisz w obrazie w skali szarości w programie OneNote — Aspose.Note
second_title: Aspose.Note API Java
description: Dowiedz się, jak zapisać dokument jako obraz w skali szarości w programie OneNote przy użyciu programu Aspose.Note dla języka Java. Z łatwością programowo manipuluj dokumentami Microsoft OneNote.
type: docs
weight: 17
url: /pl/java/onenote-document-saving/save-to-grayscale-image/
---
## Wstęp

W tym samouczku omówimy, jak zapisać dokument jako obraz w skali szarości w programie OneNote przy użyciu programu Aspose.Note dla języka Java. Obrazy w skali szarości to obrazy monochromatyczne, w których informacja o kolorze jest reprezentowana jedynie przez odcienie szarości. Aspose.Note to potężny interfejs API Java, który umożliwia programową manipulację dokumentami Microsoft OneNote.

## Warunki wstępne

Zanim zaczniemy, upewnij się, że masz następujące elementy:

1. Zestaw Java Development Kit (JDK) zainstalowany w systemie.
2.  Aspose.Note dla biblioteki Java. Można go pobrać z[Tutaj](https://releases.aspose.com/note/java/).
3. Podstawowa znajomość programowania w języku Java.

## Importuj pakiety

Aby rozpocząć, zaimportuj niezbędne pakiety:

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## Krok 1: Załaduj dokument

 Najpierw załaduj dokument do Aspose.Note. Zastępować`"Your Document Directory"` ze ścieżką do katalogu dokumentów i`"Aspose.one"` z nazwą dokumentu OneNote.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Krok 2: Ustaw ścieżkę wyjściową i opcje

Zdefiniuj ścieżkę wyjściową obrazu w skali szarości i określ opcje zapisywania. Ustawimy tryb koloru na skalę szarości.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## Krok 3: Zapisz dokument

Na koniec zapisz dokument jako obraz w skali szarości, korzystając z określonych opcji.

```java
oneFile.save(dataDir, options);
```

## Wniosek

Gratulacje! Pomyślnie nauczyłeś się, jak zapisać dokument jako obraz w skali szarości w OneNote przy użyciu Aspose.Note dla Java. Może to być niezwykle przydatne w różnych zastosowaniach, w których wymagane są obrazy w skali szarości.

## Często zadawane pytania

### P1: Czy mogę zapisać obraz w skali szarości w innym formacie?

 A1: Tak, możesz. Po prostu zmień`SaveFormat` parametr w`ImageSaveOptions` konstruktor do żądanego formatu.

### P2: Czy Aspose.Note jest kompatybilny ze wszystkimi wersjami dokumentów OneNote?

O2: Aspose.Note obsługuje Microsoft OneNote 2010 i nowsze wersje.

### P3: Czy Aspose.Note wymaga licencji?

Odpowiedź 3: Tak, potrzebujesz ważnej licencji, aby używać Aspose.Note w środowiskach produkcyjnych. Można jednak uzyskać licencję tymczasową do celów testowych.

### P4: Czy mogę manipulować innymi aspektami dokumentu przed zapisaniem go jako obrazu?

A4: Absolutnie! Aspose.Note zapewnia szeroką gamę funkcji do programowej edycji dokumentów OneNote.

### P5: Gdzie mogę znaleźć pomoc, jeśli napotkam problemy?

O5: Możesz znaleźć pomoc na forum Aspose.Note[Tutaj](https://forum.aspose.com/c/note/28).