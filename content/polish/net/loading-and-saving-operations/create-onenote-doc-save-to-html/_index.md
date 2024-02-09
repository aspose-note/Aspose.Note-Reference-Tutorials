---
title: Utwórz dokument OneNote i zapisz w formacie HTML w Aspose.Note
linktitle: Utwórz dokument OneNote i zapisz w formacie HTML w Aspose.Note
second_title: Aspose.Note .NET API
description: Dowiedz się, jak tworzyć i zapisywać dokumenty Microsoft OneNote w formacie HTML w aplikacjach .NET przy użyciu interfejsu API Aspose.Note. Skorzystaj z naszego obszernego samouczka z przykładami krok po kroku.
type: docs
weight: 14
url: /pl/net/loading-and-saving-operations/create-onenote-doc-save-to-html/
---
## Wstęp

Aspose.Note dla .NET to potężny interfejs API, który umożliwia programistom programową pracę z dokumentami Microsoft OneNote w aplikacjach .NET. Dzięki Aspose.Note możesz bez wysiłku tworzyć, manipulować i konwertować pliki OneNote. W tym samouczku przyjrzymy się, jak utworzyć dokument OneNote i zapisać go w formacie HTML, korzystając z różnych opcji udostępnianych przez interfejs API Aspose.Note dla .NET.

## Warunki wstępne

Zanim zaczniemy, upewnij się, że masz następujące wymagania wstępne:

- Podstawowa znajomość języka programowania C#.
- Program Visual Studio zainstalowany w systemie.
-  Aspose.Note dla .NET API zainstalowanego w Twoim projekcie. Można go pobrać z[Tutaj](https://releases.aspose.com/note/net/).
- Znajomość struktury dokumentów Microsoft OneNote.

## Importuj przestrzenie nazw

Zanim zagłębimy się w kodowanie, zaimportujmy niezbędne przestrzenie nazw:

```csharp
using System;
using System.Drawing;
using System.Globalization;
using System.IO;

using Aspose.Note.Saving;
using Aspose.Note.Saving.Html;

```

Teraz podzielmy każdy przykład na wiele kroków i zobaczmy, jak utworzyć dokument OneNote i zapisać go w formacie HTML za pomocą Aspose.Note dla .NET.

## Krok 1: Utwórz dokument OneNote z opcjami domyślnymi

```csharp
public static void CreateAndSaveToHTMLUsingDefaultOptions()
{
    // Zainicjuj dokument programu OneNote
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    // Domyślny styl całego tekstu w dokumencie.
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    // Zapisz w formacie HTML
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateOneNoteDocAndSaveToHTML_out.html");
    doc.Save(outputPath);

    Console.WriteLine("\nOneNote document created successfully.\nFile saved at " + outputPath);
}
```

Na tym etapie inicjujemy nowy dokument OneNote, dodajemy stronę z tytułem i zapisujemy ją w formacie HTML, korzystając z opcji domyślnych.

## Krok 2: Utwórz i zapisz określony zakres stron w formacie HTML

```csharp
public static void CreateAndSavePageRange()
{
    // Zainicjuj dokument programu OneNote
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    // Domyślny styl całego tekstu w dokumencie.
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    // Zapisz w formacie HTML
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateAndSavePageRange_out.html");
    doc.Save(outputPath, new HtmlSaveOptions { PageCount = 1, PageIndex = 0 });

    Console.WriteLine("\nOneNote document created successfully and saved as page range.\nFile saved at " + outputPath);
}
```

Tutaj pokazujemy, jak utworzyć dokument i zapisać określony zakres stron w formacie HTML.

## Krok 3: Zapisz jako HTML w strumieniu pamięci z osadzonymi zasobami

```csharp
public static void SaveAsHTMLToMemoryStreamWithEmbeddedResources()
{
    // Załaduj dokument programu OneNote
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Określ opcje zapisywania HTML
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportEmbedded,
        ExportFonts = ResourceExportType.ExportEmbedded,
        ExportImages = ResourceExportType.ExportEmbedded,
        FontFaceTypes = FontFaceType.Ttf
    };

    // Zapisz dokument w strumieniu pamięci
    var memoryStream = new MemoryStream();
    document.Save(memoryStream, options);
}
```

W tym kroku pokazano, jak zapisać dokument programu OneNote w formacie HTML z osadzonymi zasobami (CSS, czcionkami i obrazami) w strumieniu pamięci.

## Krok 4: Zapisz jako HTML do pliku z zasobami w oddzielnych plikach

```csharp
public static void SaveAsHTMLToFileWithResourcesInSeparateFiles()
{
    // Załaduj dokument programu OneNote
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Określ opcje zapisywania HTML
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportAsStream,
        ExportFonts = ResourceExportType.ExportAsStream,
        ExportImages = ResourceExportType.ExportAsStream,
        FontFaceTypes = FontFaceType.Ttf
    };

    //Zapisz dokument w pliku HTML z zasobami przechowywanymi w oddzielnych plikach
    document.Save(Path.Combine(dataDir, "document_out.html"), options);
}
```

Na tym etapie zapisujemy dokument OneNote w formacie HTML ze wszystkimi zasobami (CSS, czcionkami i obrazami) przechowywanymi w oddzielnych plikach.

## Krok 5: Zapisz jako HTML w strumieniu pamięci z wywołaniami zwrotnymi, aby zapisać zasoby

```csharp
public static void SaveAsHTMLToMemoryStreamWithCallBacksToSaveResources()
{
    // Określ zapisywanie konfiguracji wywołań zwrotnych
    var savingCallbacks = new UserSavingCallbacks()
    {
        RootFolder = "documentFolder",
        CssFolder = "css",
        KeepCssStreamOpened = true,
        ImagesFolder = "images",
        FontsFolder = "fonts"
    };

    // Określ opcje zapisywania HTML
    var options = new HtmlSaveOptions
    {
        FontFaceTypes = FontFaceType.Ttf,
        CssSavingCallback = savingCallbacks,
        FontSavingCallback = savingCallbacks,
        ImageSavingCallback = savingCallbacks
    };

    // Załaduj dokument programu OneNote
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Zapisz dokument w formacie HTML z zasobami zarządzanymi przez wywołania zwrotne zdefiniowane przez użytkownika
    using (var stream = File.Create(Path.Combine(savingCallbacks.RootFolder, "document.html")))
    {
        document.Save(stream, options);
    }

    // Ręcznie dołącz dane do strumienia CSS
    using (var writer = new StreamWriter(savingCallbacks.CssStream))
    {
        writer.WriteLine();
        writer.WriteLine("/* This line is appended to stream manually by user */");
    }
}
```

Tutaj pokazujemy, jak zapisać dokument OneNote w formacie HTML z zasobami zarządzanymi przez wywołania zwrotne zdefiniowane przez użytkownika.

## Wniosek

W tym artykule omówiliśmy, jak pracować z dokumentami OneNote i zapisywać je w formacie HTML przy użyciu Aspose.Note dla .NET. Postępując zgodnie z przewodnikiem krok po kroku, możesz to łatwo zrobić

 zintegruj tę funkcjonalność z aplikacjami .NET, umożliwiając efektywne manipulowanie plikami OneNote.

## Często zadawane pytania

### P1: Czy mogę dostosować wygląd zapisanego pliku HTML?

Odpowiedź 1: Tak, możesz dostosować wygląd, modyfikując arkusze stylów CSS wygenerowane podczas procesu konwersji.

### P2: Czy Aspose.Note obsługuje konwersję do innych formatów oprócz HTML?

Odpowiedź 2: Tak, Aspose.Note obsługuje konwersję do różnych formatów, takich jak PDF, obrazy i dokumenty Microsoft Word.

### P3: Czy Aspose.Note jest kompatybilny z aplikacjami .NET Core?

O3: Tak, Aspose.Note jest kompatybilny zarówno z aplikacjami .NET Framework, jak i .NET Core.

### P4: Czy mogę wyodrębnić tekst i obrazy z dokumentów OneNote za pomocą Aspose.Note?

O4: Tak, możesz wyodrębniać tekst i obrazy, a także wykonywać różne inne manipulacje za pomocą interfejsu API Aspose.Note.

### P5: Czy dostępna jest wersja próbna do testowania funkcji Aspose.Note?

 Odpowiedź 5: Tak, możesz pobrać bezpłatną wersję próbną ze strony[Tutaj](https://releases.aspose.com/).