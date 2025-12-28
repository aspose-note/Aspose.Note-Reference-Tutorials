---
date: 2025-12-28
description: Dowiedz się, jak eksportować OneNote do PDF z pełną kontrolą przy użyciu
  Aspose.Note dla Javy. Zawiera opcje eksportu notatnika OneNote do PDF oraz przewodnik
  konwersji notatnika do PDF w Javie.
linktitle: How to Export OneNote to PDF with Options – Convert Notebook to PDF using
  Aspose.Note
second_title: Aspose.Note Java API
title: Jak wyeksportować OneNote do PDF z opcjami – konwertuj notatnik do PDF przy
  użyciu Aspose.Note
url: /pl/java/onenote-notebook-operations/convert-notebook-to-pdf-with-options/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak wyeksportować OneNote do PDF z opcjami – Aspose.Note Java API

## Introduction

W tym samouczku dowiesz się, **jak wyeksportować OneNote do PDF** z konfigurowalnymi opcjami przy użyciu Aspose.Note dla Javy. Konwersja notatnika OneNote do PDF jest częstym wymaganiem — niezależnie od tego, czy musisz udostępnić notatki ze spotkania, zarchiwizować dokumentację, czy wygenerować raporty do druku. Z Aspose.Note proces jest prosty, w pełni programowalny i daje precyzyjną kontrolę nad powstałym plikiem PDF.

## Quick Answers
- **Co robi API?** Ładuje notatnik OneNote i zapisuje go jako PDF z opcjonalnymi ustawieniami.  
- **Jakiego języka użyto?** Java – idealna do aplikacji po stronie serwera lub na pulpit.  
- **Czy potrzebna jest licencja?** Darmowa wersja próbna działa w środowisku deweloperskim; licencja komercyjna jest wymagana w produkcji.  
- **Czy mogę kontrolować układ strony?** Tak, możesz ustawić algorytmy dzielenia stron, nagłówki, stopki i inne.  
- **Czy przykład kodu jest uruchamialny?** Oczywiście — wystarczy zamienić ścieżkę zastępczą na lokalizację swojego notatnika.

## What is “how to export onenote to pdf”?

Eksportowanie OneNote do PDF oznacza przekształcenie natywnego notatnika OneNote (`*.onetoc2` i powiązanych plików sekcji) w przenośny dokument PDF o stałym układzie. Ta konwersja zachowuje formatowanie, obrazy i osadzone obiekty, jednocześnie umożliwiając wyświetlanie zawartości na dowolnym urządzeniu bez wymogu posiadania OneNote.

## Why use Aspose.Note for Java?

- **Brak zależności od Microsoft Office** – działa na każdej platformie obsługującej Javę.  
- **Bogate opcje PDF** – kontrola dzielenia stron, nagłówków/stopki i obsługi obiektów.  
- **Wysoka wierność** – wynikowy PDF bardzo przypomina oryginalny wygląd OneNote.  
- **Skalowalny** – odpowiedni do przetwarzania w partiach tysięcy notatników.

## Prerequisites

Zanim zaczniemy, upewnij się, że masz:

1. **Java Development Kit (JDK)** – wersja 8 lub wyższa.  
2. **Aspose.Note for Java** – pobierz z [download link](https://releases.aspose.com/note/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse lub NetBeans (według wyboru).  
4. **Notatnik OneNote**, który chcesz skonwertować (np. `Notizbuch öffnen.onetoc2`).

## Import Packages

Najpierw zaimportuj klasy zapewniające obsługę notatnika i funkcjonalność zapisu PDF.

```java
import com.aspose.note.Notebook;
import java.io.IOException;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookPdfSaveOptions;
import com.aspose.note.PdfSaveOptions;
```

## Step 1: Load the OneNote Notebook

### Krok 1: Załaduj notatnik OneNote

Załaduj plik notatnika z dysku. Zamień `Your Document Directory` na rzeczywisty folder zawierający plik `.onetoc2`.

```java
String dataDir = "Your Document Directory";
// Load a OneNote Notebook
Notebook notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## Step 2: Specify PDF Save Options

### Krok 2: Określ opcje zapisu PDF

Tutaj definiujesz, jak ma być generowany PDF. Przykład ustawia algorytm dzielenia stron, który utrzymuje spójne obiekty razem, co jest przydatne przy diagramach lub tabelach, które muszą pozostać na tej samej stronie.

```java
// Specify PDF save options
NotebookPdfSaveOptions notebookSaveOptions = new NotebookPdfSaveOptions();
PdfSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();
documentSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm());
```

## Step 3: Save the Notebook as PDF

### Krok 3: Zapisz notatnik jako PDF

Na koniec zapisz notatnik jako plik PDF. Ścieżka wyjściowa może być dowolnym wybranym przez Ciebie miejscem.

```java
dataDir = dataDir + "ExportNotebooktoPDFwithOptions_out.pdf";
// Save the Notebook
notebook.save(dataDir, notebookSaveOptions);
```

## Common Issues and Solutions

### Typowe problemy i rozwiązania

| Problem | Dlaczego się pojawia | Rozwiązanie |
|---------|----------------------|-------------|
| **Plik nie znaleziony** | Nieprawidłowy `dataDir` lub nazwa pliku. | Sprawdź ponownie ścieżkę i upewnij się, że plik notatnika istnieje. |
| **Brakujące czcionki** | Renderowanie PDF wymaga tych samych czcionek co OneNote. | Zainstaluj wymagane czcionki na serwerze lub osadź je przy użyciu dodatkowych opcji Aspose. |
| **Duże notatniki powodują OutOfMemoryError** | Cały notatnik jest ładowany do pamięci. | Przetwarzaj sekcje pojedynczo lub zwiększ rozmiar sterty JVM (`-Xmx`). |

## Conclusion

Przeszliśmy przez **proces eksportu OneNote do PDF** przy użyciu Aspose.Note dla Javy, obejmując ładowanie notatnika, konfigurowanie opcji PDF i zapisywanie wyniku. Postępując zgodnie z tymi krokami, możesz zintegrować konwersję notatnika do PDF w dowolnej aplikacji Java, niezależnie od tego, czy jest to narzędzie desktopowe, usługa internetowa, czy backend przetwarzający partie.

## FAQ's

### Q1: Czy mogę dostosować wygląd wyjściowego PDF?

**A1:** Tak, Aspose.Note oferuje różne opcje dostosowywania wyjściowego PDF, w tym ustawienia nagłówka/stopki, algorytmy dzielenia stron i inne.

### Q2: Czy Aspose.Note jest kompatybilny ze wszystkimi wersjami OneNote?

**A2:** Aspose.Note obsługuje Microsoft OneNote 2010 i późniejsze wersje.

### Q3: Czy Aspose.Note oferuje darmową wersję próbną?

**A3:** Tak, możesz pobrać darmową wersję próbną Aspose.Note z [here](https://releases.aspose.com/).

### Q4: Gdzie mogę znaleźć dokumentację Aspose.Note?

**A4:** Kompleksową dokumentację Aspose.Note znajdziesz [here](https://reference.aspose.com/note/java/).

### Q5: Jak mogę uzyskać wsparcie dla Aspose.Note?

**A5:** W przypadku pomocy technicznej lub pytań, możesz odwiedzić forum wsparcia Aspose.Note [here](https://forum.aspose.com/c/note/28).

## Additional Frequently Asked Questions

**P: Jak wyeksportować notatnik OneNote do PDF bez utraty obrazów?**  
**O:** Upewnij się, że `KeepSolidObjectsAlgorithm` jest ustawiony (jak pokazano) i że pliki obrazów źródłowego notatnika są dostępne w tym samym katalogu.

**P: Czy mogę konwertować wiele notatników jednocześnie w jednym uruchomieniu?**  
**O:** Tak. Przejdź pętlą przez listę ścieżek notatników, utwórz `Notebook` dla każdego, zastosuj te same `NotebookPdfSaveOptions` i wywołaj `save()`.

**P: Czy istnieje sposób ustawienia metadanych PDF (autor, tytuł) podczas konwersji?**  
**O:** Użyj `PdfSaveOptions.setMetadata()`, aby określić autora, tytuł, temat i słowa kluczowe przed zapisem.

**P: Czy API obsługuje PDF zabezpieczone hasłem?**  
**O:** Możesz ustawić hasło w `PdfSaveOptions` za pomocą `setEncryptionPassword()` po skonfigurowaniu pozostałych opcji.

**P: Jakiej wersji Aspose.Note użyto w tym samouczku?**  
**O:** Kod został przetestowany z Aspose.Note for Java 23.12.

---

**Last Updated:** 2025-12-28  
**Tested With:** Aspose.Note for Java 23.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}