---
title: Konwertuj określony zakres stron na plik PDF w programie OneNote za pomocą języka Java
linktitle: Konwertuj określony zakres stron na plik PDF w programie OneNote za pomocą języka Java
second_title: Aspose.Note API Java
description: Dowiedz się, jak bezproblemowo konwertować określone zakresy stron z OneNote do formatu PDF za pomocą Aspose.Note dla Java. Bez problemu zachowaj formatowanie i układ.
type: docs
weight: 11
url: /pl/java/onenote-document-loading/convert-page-range-to-pdf/
---
## Wstęp

OneNote to potężne narzędzie do porządkowania notatek, ale czasami może być konieczne wyeksportowanie określonych zakresów stron do pliku PDF w celu udostępnienia lub archiwizacji. W tym samouczku przeprowadzimy Cię przez proces konwersji określonego zakresu stron do formatu PDF za pomocą Aspose.Note dla Java.

## Warunki wstępne

Zanim zaczniemy, upewnij się, że masz następujące wymagania wstępne:

1. Zestaw Java Development Kit (JDK): Upewnij się, że w systemie jest zainstalowana Java.
2.  Aspose.Note dla Java: Pobierz i zainstaluj Aspose.Note dla Java z[Tutaj](https://releases.aspose.com/note/java/).
3. Przykładowy dokument OneNote: Przygotuj przykładowy dokument OneNote, z którego chcesz wyodrębnić określony zakres stron.

## Importuj pakiety

W swoim projekcie Java zaimportuj pakiety niezbędne do korzystania z Aspose.Uwaga:

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
```

## Krok 1: Załaduj dokument OneNote

Załaduj dokument OneNote za pomocą Aspose.Note:

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one");
```

## Krok 2: Zainicjuj opcje zapisywania plików PDF

Zainicjuj obiekt PdfSaveOptions i określ indeks i liczbę stron:

```java
PdfSaveOptions opts = new PdfSaveOptions();
opts.setPageIndex(2);  // Indeks strony początkowej
opts.setPageCount(3);  // Liczba stron do uwzględnienia
```

## Krok 3: Zapisz jako plik PDF

Zapisz określony zakres stron jako plik PDF:

```java
oneFile.save(dataDir + "ConvertSpecificPageRangeToPdf_out.pdf", opts);
System.out.println("File saved: " + dataDir + "ConvertSpecificPageRangeToPdf_out.pdf");
```

Gratulacje! Pomyślnie przekonwertowałeś określony zakres stron z dokumentu OneNote na plik PDF przy użyciu Aspose.Note dla Java.

## Wniosek

W tym samouczku nauczyliśmy się, jak przekonwertować określony zakres stron z dokumentu OneNote na format PDF za pomocą Aspose.Note dla Java. Funkcjonalność ta może być przydatna do różnych celów, takich jak udostępnianie wybranych informacji lub tworzenie kopii archiwalnych.

## Często zadawane pytania

### P1: Czy mogę określić wiele nieciągłych zakresów stron do konwersji?

Odpowiedź 1: Niestety, Aspose.Note dla Java obsługuje obecnie konwersję tylko sąsiadujących zakresów stron do formatu PDF.

### P2: Czy Aspose.Note dla Java zachowuje formatowanie oryginalnego dokumentu OneNote?

O2: Tak, Aspose.Note zapewnia zachowanie formatowania i układu oryginalnego dokumentu OneNote w wygenerowanym pliku PDF.

### P3: Czy można konwertować dokumenty OneNote chronione hasłem do formatu PDF?

O3: Aspose.Note dla Java nie obsługuje bezpośredniej konwersji dokumentów OneNote chronionych hasłem. Przed konwersją należy usunąć zabezpieczenie hasłem.

### P4: Czy mogę dostosować wygląd wygenerowanego pliku PDF?

O4: Tak, możesz dostosować różne aspekty, takie jak rozmiar strony, orientacja i ustawienia nagłówka/stopki, korzystając z opcji zapisywania plików PDF Aspose.Note.

### P5: Czy Aspose.Note dla Java obsługuje wsadową konwersję wielu dokumentów OneNote?

O5: Tak, możesz zbiorczo konwertować wiele dokumentów OneNote do formatu PDF, przeglądając każdy dokument w pętli i stosując proces konwersji.