---
title: Zapisz, używając określonych czcionek w Aspose.Note
linktitle: Zapisz, używając określonych czcionek w Aspose.Note
second_title: Aspose.Note .NET API
description: Dowiedz się, jak zapisywać dokumenty z określonymi czcionkami w Aspose.Note dla .NET. Z łatwością dostosowuj ustawienia czcionek, aby uzyskać spójne formatowanie dokumentu.
type: docs
weight: 28
url: /pl/net/loading-and-saving-operations/save-using-specified-fonts/
---
## Wstęp

W tym samouczku nauczymy się, jak zapisywać dokumenty przy użyciu określonych czcionek w Aspose.Note dla .NET. Krok po kroku przeanalizujemy różne metody osiągnięcia tego celu.

## Warunki wstępne

Zanim zaczniemy, upewnij się, że masz następujące elementy:

1.  Aspose.Note dla .NET: Upewnij się, że zainstalowałeś Aspose.Note dla .NET. Można go pobrać z[Tutaj](https://releases.aspose.com/note/net/).

2. Środowisko programistyczne: Potrzebujesz środowiska programistycznego skonfigurowanego do programowania .NET.

## Importuj przestrzenie nazw

Najpierw zaimportujmy niezbędne przestrzenie nazw:

```csharp
using System;
using System.IO;

using Aspose.Note.Fonts;
using Aspose.Note.Saving;

```

## Krok 1: Zapisywanie z domyślną nazwą czcionki

W tym kroku zapiszemy dokument przy użyciu określonej domyślnej nazwy czcionki.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName()
{
    // Ścieżka do katalogu dokumentów.
    string dataDir = "Your Document Directory";

    // Załaduj dokument do Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Zapisz dokument w formacie PDF z określoną czcionką domyślną.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFont("Times New Roman")
                          });
}
```

## Krok 2: Zapisywanie z domyślną czcionką z pliku

Następnie zapiszmy dokument przy użyciu domyślnej czcionki załadowanej z pliku.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile()
{
    // Ścieżka do katalogu dokumentów.
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    // Załaduj dokument do Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Zapisz dokument w formacie PDF z domyślną czcionką załadowaną z pliku.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromFile(fontFile)
                          });
}
```

## Krok 3: Zapisywanie z domyślną czcionką ze strumienia

Na koniec zapiszmy dokument przy użyciu domyślnej czcionki załadowanej ze strumienia.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream()
{
    // Ścieżka do katalogu dokumentów.
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    // Załaduj dokument do Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Zapisz dokument w formacie PDF z domyślną czcionką załadowaną ze strumienia.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf";

    using (var stream = File.Open(fontFile, FileMode.Open, FileAccess.Read, FileShare.Read))
    {
        oneFile.Save(dataDir, new PdfSaveOptions()
                              {
                                  FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromStream(stream)
                              });
    }
}
```

## Wniosek

W tym samouczku omówiliśmy, jak zapisywać dokumenty przy użyciu określonych czcionek w Aspose.Note dla .NET. Wykonując poniższe kroki, możesz dostosować ustawienia czcionek zgodnie ze swoimi wymaganiami, upewniając się, że dokumenty są sformatowane zgodnie z oczekiwaniami.

## Często zadawane pytania

### P1: Czy mogę używać dowolnej czcionki do zapisywania dokumentów w Aspose.Note?

O1: Tak, możesz określić dowolną czcionkę do zapisywania dokumentów. Upewnij się tylko, że plik czcionki jest dostępny i poprawnie załadowany.

### P2: Czy Aspose.Note jest kompatybilny z różnymi formatami dokumentów?

Odpowiedź 2: Aspose.Note działa głównie z dokumentami OneNote, ale udostępnia opcje zapisywania w różnych formatach, w tym w formacie PDF.

### P3: Jak mogę sobie poradzić z brakującymi czcionkami podczas zapisywania dokumentów?

O3: Aspose.Note oferuje opcje użycia domyślnych czcionek w przypadku braku określonej czcionki, zapewniając spójne formatowanie dokumentu.

### P4: Czy Aspose.Note obsługuje osadzanie czcionek w dokumentach wyjściowych?

O4: Tak, Aspose.Note umożliwia osadzanie czcionek, aby zapewnić przenośność dokumentów i spójne renderowanie na różnych platformach.

### P5: Gdzie mogę uzyskać dalszą pomoc dotyczącą Aspose.Note?

 O5: Aby uzyskać dalszą pomoc lub wsparcie techniczne, odwiedź stronę[Forum Aspose.Note](https://forum.aspose.com/c/note/28).