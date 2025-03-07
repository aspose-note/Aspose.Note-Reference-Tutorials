---
title: Konwertuj notatnik na spłaszczony obraz w programie OneNote — Aspose.Note
linktitle: Konwertuj notatnik na spłaszczony obraz w programie OneNote — Aspose.Note
second_title: Aspose.Note API Java
description: Dowiedz się, jak przekonwertować notatnik na spłaszczony obraz w programie OneNote przy użyciu programu Aspose.Note dla języka Java. Zachowaj wszystkie elementy w jednym pliku obrazu bez wysiłku.
weight: 13
url: /pl/java/onenote-notebook-operations/convert-notebook-to-flattened-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konwertuj notatnik na spłaszczony obraz w programie OneNote — Aspose.Note

## Wstęp

tym samouczku przeprowadzimy Cię przez proces konwertowania notatnika na spłaszczony obraz w programie OneNote przy użyciu programu Aspose.Note dla języka Java. Dzięki temu możesz zapisać notatnik jako plik obrazu, zapewniając zachowanie wszystkich elementów w jednym formacie obrazu.

## Warunki wstępne

Zanim zaczniemy, upewnij się, że masz następujące elementy:

1. Zestaw Java Development Kit (JDK) zainstalowany w systemie.
2.  Biblioteka Aspose.Note dla Java pobrana i skonfigurowana w projekcie Java. Bibliotekę możesz pobrać ze strony[Tutaj](https://releases.aspose.com/note/java/).
3. Podstawowa znajomość programowania w języku Java.

## Importuj pakiety

Aby rozpocząć, musisz zaimportować niezbędne pakiety z Aspose.Note dla Java:

```java
import java.io.IOException;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Krok 1: Skonfiguruj katalog dokumentów

Najpierw zdefiniuj katalog, w którym znajduje się plik notatnika:

```java
String dataDir = "Your Document Directory";
```

 Zastępować`"Your Document Directory"` ze ścieżką do pliku notatnika.

## Krok 2: Załaduj notatnik

 Następnie załaduj plik notatnika za pomocą`Notebook` klasa:

```java
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

 Pamiętaj o wymianie`"test.onetoc2"` z nazwą pliku notatnika.

## Krok 3: Ustaw opcje zapisywania obrazu

Teraz skonfiguruj opcje zapisywania notatnika jako obrazu. Określimy format zapisu jako PNG i ustawimy rozdzielczość na 400 DPI:

```java
NotebookImageSaveOptions saveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
ImageSaveOptions documentSaveOptions = saveOptions.getDocumentSaveOptions();
documentSaveOptions.setResolution(400);
```

Możesz dostosować rozdzielczość zgodnie ze swoimi wymaganiami.

## Krok 4: Spłaszcz notatnik

Aby mieć pewność, że wszystkie elementy zostaną spłaszczone w jeden obraz, ustaw opcję`flatten` opcja`true`:

```java
saveOptions.setFlatten(true);
```

Dzięki temu uzyskany obraz zachowa układ notatnika.

## Krok 5: Zapisz obraz

Na koniec zapisz notatnik jako spłaszczony obraz:

```java
notebook.save(dataDir + "ExportImageasFlattenedNotebook_out.png", saveOptions);
```

 Zastępować`"ExportImageasFlattenedNotebook_out.png"` z żądaną nazwą pliku wyjściowego.

## Wniosek

Podsumowując, używając Aspose.Note dla Java, możesz łatwo przekonwertować swój notatnik na spłaszczony obraz w OneNote. Proces ten zapewnia zachowanie wszystkich elementów w jednym formacie obrazu, co ułatwia udostępnianie i przeglądanie.

## Często zadawane pytania

### P1: Czy mogę dostosować rozdzielczość obrazu wyjściowego?

 Odpowiedź 1: Tak, możesz dostosować rozdzielczość do swoich wymagań, modyfikując plik`setResolution` parametr metody.

### P2: Czy Aspose.Note obsługuje inne formaty obrazów do eksportu?

O2: Tak, Aspose.Note obsługuje różne formaty obrazów, takie jak PNG, JPEG, BMP itp., do eksportowania notatników.

### P3: Czy mogę bardziej dostosować obraz wyjściowy?

O3: Tak, Aspose.Note zapewnia szerokie możliwości dostosowywania obrazu wyjściowego, w tym rozmiaru strony, orientacji i ustawień jakości.

### P4: Czy dostępna jest wersja próbna Aspose.Note dla Java?

 Odpowiedź 4: Tak, możesz uzyskać bezpłatną wersję próbną od[Tutaj](https://releases.aspose.com/).

### P5: Gdzie mogę znaleźć wsparcie dla Aspose.Note dla Java?

 O5: Możesz znaleźć wsparcie i zasoby na forum Aspose.Note[Tutaj](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
