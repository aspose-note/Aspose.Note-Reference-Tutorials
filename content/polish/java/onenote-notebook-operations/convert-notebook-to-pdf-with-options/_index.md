---
title: Konwertuj notatnik na format PDF za pomocą opcji w programie OneNote - Aspose.Note
linktitle: Konwertuj notatnik na format PDF za pomocą opcji w programie OneNote - Aspose.Note
second_title: Aspose.Note API Java
description: łatwością dostosowuj i eksportuj notesy OneNote do formatu PDF! Aspose.Note dla Java obsługuje ciężkie podnoszenie. W zestawie instrukcja krok po kroku! #OneNote #Java #Aspose
type: docs
weight: 17
url: /pl/java/onenote-notebook-operations/convert-notebook-to-pdf-with-options/
---
## Wstęp

W tym samouczku zagłębimy się w świat konwersji notatników do formatu PDF z konfigurowalnymi opcjami przy użyciu Aspose.Note dla Java. Aspose.Note to potężny interfejs API Java, który umożliwia programistom programowe manipulowanie dokumentami Microsoft OneNote. Konwersja notatników do formatu PDF jest powszechnym wymaganiem w różnych aplikacjach, a dzięki Aspose.Note zadanie to staje się usprawnione i wydajne.

## Warunki wstępne

Zanim zaczniemy, upewnij się, że spełnione są następujące wymagania wstępne:

1. Zestaw Java Development Kit (JDK): Upewnij się, że masz zainstalowany pakiet JDK w swoim systemie.
2. Aspose.Note dla Java: Pobierz i zainstaluj Aspose.Note dla Java z[link do pobrania](https://releases.aspose.com/note/java/).
3. IDE (zintegrowane środowisko programistyczne): wybierz preferowane środowisko IDE do programowania w języku Java. Popularnymi wyborami są IntelliJ IDEA, Eclipse lub NetBeans.

## Importuj pakiety

Najpierw musisz zaimportować niezbędne pakiety do swojego projektu Java. Pakiety te udostępniają klasy i metody wymagane do pracy z dokumentami programu OneNote.

```java
import com.aspose.note.Notebook;
import java.io.IOException;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookPdfSaveOptions;
import com.aspose.note.PdfSaveOptions;
```

## Krok 1: Załaduj notatnik programu OneNote

Aby przekonwertować notatnik na format PDF, musisz najpierw załadować notatnik programu OneNote. Upewnij się, że ścieżka do pliku notatnika została poprawnie określona.

```java
String dataDir = "Your Document Directory";
// Załaduj notatnik programu OneNote
Notebook notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## Krok 2: Określ opcje zapisywania plików PDF

Aspose.Note zapewnia różne opcje dostosowywania wyjściowego pliku PDF. Możesz określić opcje, takie jak algorytmy podziału strony, ustawienia nagłówka/stopki i inne.

```java
// Określ opcje zapisywania plików PDF
NotebookPdfSaveOptions notebookSaveOptions = new NotebookPdfSaveOptions();
PdfSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();
documentSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm());
```

## Krok 3: Zapisz notatnik jako plik PDF

Po załadowaniu notatnika i określeniu opcji zapisywania nadszedł czas na zapisanie notatnika jako pliku PDF.

```java
dataDir = dataDir + "ExportNotebooktoPDFwithOptions_out.pdf";
// Zapisz notatnik
notebook.save(dataDir, notebookSaveOptions);
```

## Wniosek

W tym samouczku omówiliśmy, jak konwertować notesy OneNote do formatu PDF przy użyciu Aspose.Note dla Java. Wykonując te proste kroki, możesz efektywnie obsługiwać konwersje dokumentów w aplikacjach Java.

---

## Często zadawane pytania

### P1: Czy mogę dostosować wygląd pliku PDF?

O1: Tak, Aspose.Note zapewnia różne opcje dostosowywania wyjściowego pliku PDF, w tym ustawienia nagłówka/stopki, algorytmy podziału strony i inne.

### P2: Czy Aspose.Note jest kompatybilny ze wszystkimi wersjami OneNote?

O2: Aspose.Note obsługuje Microsoft OneNote 2010 i nowsze wersje.

### P3: Czy Aspose.Note oferuje bezpłatną wersję próbną?

 A3: Tak, możesz pobrać bezpłatną wersję próbną Aspose.Note z[Tutaj](https://releases.aspose.com/).

### P4: Gdzie mogę znaleźć dokumentację dla Aspose.Note?

 O4: Możesz znaleźć obszerną dokumentację dla Aspose.Note[Tutaj](https://reference.aspose.com/note/java/).

### P5: Jak mogę uzyskać wsparcie dla Aspose.Note?

 O5: Aby uzyskać pomoc techniczną lub zadać pytania, możesz odwiedzić forum pomocy technicznej Aspose.Note[Tutaj](https://forum.aspose.com/c/note/28).