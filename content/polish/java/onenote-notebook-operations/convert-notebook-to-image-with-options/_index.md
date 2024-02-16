---
title: Konwertuj notatnik na obraz za pomocą opcji w programie OneNote — Aspose.Note
linktitle: Konwertuj notatnik na obraz za pomocą opcji w programie OneNote — Aspose.Note
second_title: Aspose.Note API Java
description: Dowiedz się, jak przekonwertować Notatnik na obraz za pomocą opcji przy użyciu Aspose.Note dla Java. Postępuj zgodnie z naszym samouczkiem krok po kroku, aby uzyskać bezproblemową integrację z aplikacjami Java.
type: docs
weight: 14
url: /pl/java/onenote-notebook-operations/convert-notebook-to-image-with-options/
---
## Wstęp

W tym samouczku zagłębimy się w proces konwersji Notatnika na obraz za pomocą różnych opcji przy użyciu Aspose.Note dla Java. Aspose.Note to potężny interfejs API Java, który umożliwia programistom programową pracę z plikami Microsoft OneNote, umożliwiając bezproblemową integrację z ich aplikacjami Java.

## Warunki wstępne

Zanim zaczniemy, upewnij się, że spełnione są następujące wymagania wstępne:

1. Zestaw Java Development Kit (JDK): Upewnij się, że masz zainstalowany pakiet JDK w swoim systemie.
2. Aspose.Note dla plików Java JAR: Pobierz bibliotekę Aspose.Note dla Java z[Tutaj](https://releases.aspose.com/note/java/) i umieść go w ścieżce klas swojego projektu.

## Importuj pakiety

Najpierw zaimportujmy niezbędne pakiety dla naszej aplikacji Java:

```java
import java.io.IOException;

import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Krok 1: Załaduj notatnik

Na początek musimy załadować notatnik OneNote, który chcemy przekonwertować na obraz.

```java
String dataDir = "Your Document Directory";
// Załaduj notatnik programu OneNote
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

## Krok 2: Ustaw opcje zapisywania

Następnie zdefiniujemy opcje zapisywania obrazu, w tym żądany format (PNG, JPEG itp.) i rozdzielczość.

```java
NotebookImageSaveOptions notebookSaveOptions = new NotebookImageSaveOptions(SaveFormat.Png);

ImageSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();

documentSaveOptions.setResolution(400);
```

## Krok 3: Zapisz notatnik jako obraz

Teraz zapiszemy notatnik jako obraz z określonymi opcjami.

```java
dataDir = dataDir + "ExportNotebooktoImagewithOptions_out.png";

// Zapisz notatnik
notebook.save(dataDir, notebookSaveOptions);
```

## Wniosek

W tym samouczku nauczyliśmy się, jak przekonwertować Notatnik na obraz za pomocą różnych opcji przy użyciu Aspose.Note dla Java. Wykonując poniższe kroki, możesz bezproblemowo zintegrować tę funkcję z aplikacjami Java, otwierając możliwości programowego manipulowania plikami OneNote.

## Często zadawane pytania

### P1: Czy Aspose.Note obsługuje złożone pliki OneNote?

Odpowiedź 1: Tak, Aspose.Note może efektywnie obsługiwać złożone pliki OneNote, umożliwiając programowe wykonywanie na nich różnych operacji.

### P2: Czy Aspose.Note dla Java można łatwo zintegrować z istniejącymi projektami?

A2: Absolutnie! Aspose.Note dla Java zapewnia proste API, które można łatwo zintegrować z projektami Java, oszczędzając czas i wysiłek.

### P3: Czy mogę dostosować wyjściowy obraz podczas konwersji notebooka?

O3: Tak, Aspose.Note umożliwia dostosowanie wyjściowego obrazu poprzez określenie opcji, takich jak rozdzielczość, format i inne.

### P4: Czy Aspose.Note oferuje wsparcie dla programistów?

Odpowiedź 4: Tak, Aspose zapewnia doskonałe wsparcie dla programistów za pośrednictwem forów i dokumentacji, zapewniając płynną integrację i rozwiązywanie problemów.

### P5: Czy dostępna jest bezpłatna wersja próbna Aspose.Note dla Java?

 O5: Tak, możesz skorzystać z bezpłatnej wersji próbnej Aspose.Note dla Java z[Tutaj](https://releases.aspose.com/).