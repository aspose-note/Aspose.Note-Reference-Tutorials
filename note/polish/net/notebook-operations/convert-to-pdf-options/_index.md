---
title: Konwertuj notesy do formatu PDF za pomocą opcji w Aspose Note .NET
linktitle: Konwertuj notesy do formatu PDF za pomocą opcji w Aspose Note .NET
second_title: Aspose.Note .NET API
description: Dowiedz się, jak konwertować notesy Microsoft OneNote do formatu PDF przy użyciu biblioteki Aspose.Note dla .NET z konfigurowalnymi opcjami.
weight: 16
url: /pl/net/notebook-operations/convert-to-pdf-options/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konwertuj notesy do formatu PDF za pomocą opcji w Aspose Note .NET

## Wstęp

W tym samouczku omówimy proces konwersji notatników do formatu PDF przy użyciu biblioteki Aspose.Note dla .NET. Aspose.Note dla .NET zapewnia potężny zestaw funkcji do programowej pracy z plikami Microsoft OneNote.

## Warunki wstępne

Zanim zaczniemy, upewnij się, że masz następujące wymagania wstępne:

### 1. Aspose.Note dla biblioteki .NET
 Upewnij się, że pobrałeś i zainstalowałeś bibliotekę Aspose.Note dla .NET. Można go pobrać z[strona internetowa](https://releases.aspose.com/note/net/).

### 2. Środowisko programistyczne
Należy mieć skonfigurowane środowisko programistyczne, takie jak Visual Studio, z zainstalowanym niezbędnym środowiskiem .NET.

## Importuj przestrzenie nazw

Zanim zaczniemy używać Aspose.Note for .NET w naszym projekcie, zaimportujmy wymagane przestrzenie nazw:

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Collections.Generic;
```

Podzielmy teraz proces konwersji notatników do formatu PDF z opcjami na kilka kroków:

## Krok 1: Załaduj notatnik

Najpierw musimy załadować notatnik OneNote, który chcemy przekonwertować na plik PDF.

```csharp
// Ścieżka do katalogu dokumentów.
string dataDir = "Your Document Directory";

// Załaduj notatnik programu OneNote
var notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## Krok 2: Określ opcje zapisywania plików PDF

Następnie określimy opcje zapisywania notatnika jako pliku PDF. Możemy dostosować różne ustawienia, takie jak algorytm podziału strony, marginesy i rozmiar strony.

```csharp
var notebookSaveOptions = new NotebookPdfSaveOptions();
var documentSaveOptions = notebookSaveOptions.DocumentSaveOptions;

documentSaveOptions.PageSplittingAlgorithm = new KeepSolidObjectsAlgorithm();
```

## Krok 3: Zapisz notatnik jako plik PDF

Teraz zapiszemy notatnik jako plik PDF, korzystając z określonych opcji.

```csharp
dataDir = dataDir + "ConvertToPDF_out.pdf";

// Zapisz notatnik
notebook.Save(dataDir, notebookSaveOptions);
```

## Krok 4: Zweryfikuj konwersję

Na koniec sprawdźmy, czy konwersja przebiegła pomyślnie i wydrukujmy lokalizację, w której zapisany jest plik PDF.

```csharp
Console.WriteLine("\nNoteBook document converted to pdf successfully with save options.\nFile saved at " + dataDir);
```

## Wniosek

W tym samouczku nauczyliśmy się konwertować notesy OneNote do formatu PDF przy użyciu biblioteki Aspose.Note dla .NET. Wykonując kroki opisane powyżej, możesz łatwo zintegrować tę funkcjonalność z aplikacjami .NET.

## Często zadawane pytania

### P1: Czy Aspose.Note dla .NET jest kompatybilny ze wszystkimi wersjami Microsoft OneNote?

O1: Tak, Aspose.Note dla .NET obsługuje różne wersje Microsoft OneNote, w tym formaty .one i .onetoc2.

### P2: Czy mogę dostosować wygląd pliku PDF?

O2: Tak, możesz określić różne opcje, takie jak rozmiar strony, marginesy i algorytm podziału strony, aby dostosować wygląd pliku PDF.

### P3: Czy Aspose.Note dla .NET zapewnia obsługę innych formatów plików?

O3: Tak, Aspose.Note dla .NET obsługuje konwersję do różnych innych formatów, takich jak obrazy, HTML i dokumenty Microsoft Word.

### P4: Czy dostępna jest bezpłatna wersja próbna Aspose.Note dla .NET?

Odpowiedź 4: Tak, możesz pobrać bezpłatną wersję próbną Aspose.Note dla .NET ze strony internetowej, aby ocenić jego funkcje przed dokonaniem zakupu.

### P5: Jak mogę uzyskać pomoc techniczną dla Aspose.Note dla .NET?

 O5: Możesz uzyskać pomoc techniczną dla Aspose.Note dla .NET odwiedzając stronę[Forum Aspose.Note](https://forum.aspose.com/c/note/28) lub skontaktuj się bezpośrednio z zespołem wsparcia Aspose.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
