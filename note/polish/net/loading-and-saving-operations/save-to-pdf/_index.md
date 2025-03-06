---
title: Zapisz w formacie PDF w Aspose.Note
linktitle: Zapisz w formacie PDF w Aspose.Note
second_title: Aspose.Note .NET API
description: Dowiedz się, jak zapisywać dokumenty Microsoft OneNote w formacie PDF przy użyciu Aspose.Note dla .NET. Samouczek krok po kroku z przykładami kodu dla układów stron Letter i A4.
weight: 26
url: /pl/net/loading-and-saving-operations/save-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zapisz w formacie PDF w Aspose.Note

## Wstęp

tym samouczku omówimy, jak zapisywać dokumenty w formacie PDF za pomocą Aspose.Note dla .NET. Aspose.Note to potężna biblioteka, która umożliwia programistom programową pracę z plikami Microsoft OneNote. Omówimy wymagania wstępne, zaimportujemy przestrzenie nazw i udostępnimy przewodniki krok po kroku dotyczące zapisywania dokumentów w formacie PDF w różnych układach stron.

## Warunki wstępne

Zanim zaczniemy, upewnij się, że masz następujące elementy:

- Program Visual Studio zainstalowany w systemie.
-  Pobrano i zainstalowano bibliotekę Aspose.Note dla .NET. Można go pobrać z[Tutaj](https://releases.aspose.com/note/net/).
- Podstawowa znajomość języka programowania C#.

## Importuj przestrzenie nazw

Najpierw zaimportujmy niezbędne przestrzenie nazw do naszego kodu C#:

```csharp
using System;
using System.IO;

using Aspose.Note.Saving;
```

Teraz, gdy mamy już spełnione wymagania wstępne i zaimportowane przestrzenie nazw, przejdźmy do zapisywania dokumentów w formacie PDF w różnych układach stron.

## Krok 1: Zapisz w formacie PDF, korzystając z ustawień strony listowej


```csharp
public static void SaveToPdfUsingLetterPageSettings()
{
    // Ścieżka do katalogu dokumentów.
    string dataDir = "Your Document Directory";

    // Załaduj dokument do Aspose.Note.
    Document oneFile = new Document(dataDir + "OneNote.one");

    var dst = Path.Combine(dataDir, "SaveToPdfUsingLetterPageSettings.pdf");

    // Zapisz dokument.
    oneFile.Save(dst, new PdfSaveOptions() { PageSettings = PageSettings.Letter });

    Console.WriteLine("\nOneNote document saved successfully.\nFile saved at " + dst);
}
```

### Wyjaśnienie:

- Ładujemy dokument OneNote do Aspose.Note.
- Określ ścieżkę docelową dla zapisanego pliku PDF.
-  Zapisz dokument w formacie PDF za pomocą`PdfSaveOptions` z`PageSettings` Ustawić`Letter`.

## Krok 2: Zapisz w formacie PDF przy użyciu ustawień strony A4 bez ograniczenia wysokości

```csharp
public static void SaveToPdfUsingA4PageSettingsWithoutHeightLimit()
{
    // Ścieżka do katalogu dokumentów.
    string dataDir = "Your Document Directory";

    // Załaduj dokument do Aspose.Note.
    Document oneFile = new Document(dataDir + "OneNote.one");

    var dst = Path.Combine(dataDir, "SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf");

    // Zapisz dokument.
    oneFile.Save(dst, new PdfSaveOptions() { PageSettings = PageSettings.A4NoHeightLimit });

    Console.WriteLine("\nOneNote document saved successfully.\nFile saved at " + dst);
}
```

### Wyjaśnienie:

- Podobnie jak w poprzednim kroku, ładujemy dokument OneNote do Aspose.Note.
- Określ ścieżkę docelową dla zapisanego pliku PDF.
-  Zapisz dokument w formacie PDF za pomocą`PdfSaveOptions` z`PageSettings` Ustawić`A4NoHeightLimit`.

## Wniosek

W tym samouczku nauczyliśmy się, jak zapisywać dokumenty w formacie PDF za pomocą Aspose.Note dla .NET. Omówiliśmy dwa różne układy strony: Letter i A4 bez ograniczenia wysokości. Dzięki Aspose.Note programiści mogą łatwo programowo manipulować plikami OneNote, zapewniając elastyczność i wydajność w zadaniach związanych z zarządzaniem dokumentami.

## Często zadawane pytania

### P1: Czy Aspose.Note obsługuje złożone pliki OneNote?

Odpowiedź 1: Tak, Aspose.Note obsługuje różne funkcje i funkcjonalności, aby skutecznie obsługiwać złożone pliki OneNote.

### P2: Czy Aspose.Note nadaje się do projektów komercyjnych?

 Odpowiedź 2: Oczywiście, Aspose.Note można z łatwością używać w projektach komercyjnych. Możesz kupić licencję[Tutaj](https://purchase.aspose.com/buy).

### P3: Czy Aspose.Note oferuje bezpłatną wersję próbną?

 Odpowiedź 3: Tak, możesz eksplorować Aspose.Note w ramach bezpłatnej wersji próbnej[Tutaj](https://releases.aspose.com/).

### P4: Gdzie mogę znaleźć dokumentację dla Aspose.Note?

 A4: Możesz znaleźć szczegółową dokumentację[Tutaj](https://reference.aspose.com/note/net/).

### P5: Potrzebujesz dalszej pomocy?

 A5: Zachęcamy do zadawania pytań lub szukania pomocy na forum Aspose.Note[Tutaj](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
