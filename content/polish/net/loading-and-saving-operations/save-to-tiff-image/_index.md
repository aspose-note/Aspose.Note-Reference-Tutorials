---
title: Zapisz w obrazie TIFF w Aspose.Note
linktitle: Zapisz w obrazie TIFF w Aspose.Note
second_title: Aspose.Note .NET API
description: Dowiedz się, jak zapisywać dokumenty OneNote jako obrazy TIFF przy użyciu różnych metod kompresji przy użyciu Aspose.Note dla .NET.
type: docs
weight: 27
url: /pl/net/loading-and-saving-operations/save-to-tiff-image/
---
## Wstęp

W tym samouczku omówimy, jak zapisywać dokumenty jako obrazy w formacie TIFF przy użyciu Aspose.Note dla .NET. Aspose.Note to potężny interfejs API, który umożliwia programistom programową pracę z plikami Microsoft OneNote. Zapisywanie dokumentów programu OneNote jako obrazów TIFF może być przydatne w różnych zastosowaniach, takich jak archiwizacja, udostępnianie lub drukowanie.

## Warunki wstępne

Zanim zaczniemy, upewnij się, że masz następujące elementy:

1.  Aspose.Note dla .NET: Upewnij się, że zainstalowałeś Aspose.Note dla .NET. Można go pobrać z[Tutaj](https://releases.aspose.com/note/net/).

2. Środowisko programistyczne: skonfiguruj środowisko programistyczne w programie Visual Studio lub dowolnym innym środowisku .NET IDE.

3. Dokument OneNote: Przygotuj przykładowy dokument OneNote, który chcesz przekonwertować do formatu TIFF.

## Importuj przestrzenie nazw

Najpierw musisz zaimportować niezbędne przestrzenie nazw do swojego projektu:

```csharp
using System;
using System.IO;

using Aspose.Note.Saving;

```

## Krok 1: Zapisz w formacie TIFF przy użyciu kompresji JPEG

Kompresja JPEG jest powszechnie stosowaną metodą zmniejszania rozmiaru obrazów przy jednoczesnym zachowaniu jakości. Oto jak zapisać dokument programu OneNote jako obraz TIFF z kompresją JPEG:

```csharp
public static void SaveToTiffUsingJpegCompression()
{
    // Załaduj dokument do Aspose.Note.
    Document oneFile = new Document("Path_to_your_OneNote_document");

    // Ustaw ścieżkę docelową dla obrazu TIFF.
    var dst = "Destination_path_for_TIFF_image";

    // Zapisz dokument jako obraz TIFF z kompresją JPEG.
    oneFile.Save(dst, new ImageSaveOptions(SaveFormat.Tiff)
    {
        TiffCompression = TiffCompression.Jpeg,
        Quality = 93 // Dostosuj jakość według potrzeb
    });

    Console.WriteLine("\nOneNote document converted successfully to image in TIFF format using JPEG compression.\nFile saved at " + dst);
}
```

## Krok 2: Zapisz w formacie TIFF przy użyciu kompresji PackBits

Kompresja PackBits to prosty i wydajny algorytm kompresji powszechnie stosowany w obrazach TIFF. Oto jak zapisać dokument OneNote jako obraz TIFF z kompresją PackBits:

```csharp
public static void SaveToTiffUsingPackBitsCompression()
{
    // Załaduj dokument do Aspose.Note.
    Document oneFile = new Document("Path_to_your_OneNote_document");

    // Ustaw ścieżkę docelową dla obrazu TIFF.
    var dst = "Destination_path_for_TIFF_image";

    // Zapisz dokument jako obraz TIFF z kompresją PackBits.
    oneFile.Save(dst, new ImageSaveOptions(SaveFormat.Tiff)
    {
        TiffCompression = TiffCompression.PackBits
    });

    Console.WriteLine("\nOneNote document converted successfully to image in TIFF format using PackBits compression.\nFile saved at " + dst);
}
```

## Krok 3: Zapisz w formacie TIFF przy użyciu kompresji CCITT Group 3

Kompresja CCITT Group 3, znana również jako kompresja faksu, jest odpowiednia dla obrazów czarno-białych. Oto jak zapisać dokument OneNote jako obraz TIFF z kompresją CCITT Group 3:

```csharp
public static void SaveToTiffUsingCcitt3Compression()
{
    // Załaduj dokument do Aspose.Note.
    Document oneFile = new Document("Path_to_your_OneNote_document");

    // Ustaw ścieżkę docelową dla obrazu TIFF.
    var dst = "Destination_path_for_TIFF_image";

    // Zapisz dokument jako obraz TIFF z kompresją CCITT Group 3.
    oneFile.Save(dst, new ImageSaveOptions(SaveFormat.Tiff)
    {
        ColorMode = ColorMode.BlackAndWhite,
        TiffCompression = TiffCompression.Ccitt3
    });

    Console.WriteLine("\nOneNote document converted successfully to image in TIFF format using CCITT Group 3 fax compression.\nFile saved at " + dst);
}
```

Wykonując poniższe kroki, możesz łatwo zapisać dokumenty OneNote jako obrazy TIFF z różnymi opcjami kompresji przy użyciu Aspose.Note dla .NET.

## Wniosek

W tym samouczku nauczyliśmy się, jak zapisywać dokumenty OneNote jako obrazy TIFF przy użyciu różnych metod kompresji w Aspose.Note dla .NET. Niezależnie od tego, czy potrzebujesz kompresji JPEG, PackBits czy CCITT Group 3, Aspose.Note zapewnia elastyczność pozwalającą efektywnie obsługiwać różne wymagania.

## Często zadawane pytania

### P1: Czy mogę dostosować jakość kompresji JPEG?

O1: Tak, możesz dostosować parametr jakości podczas zapisywania z kompresją JPEG, aby zrównoważyć jakość obrazu i rozmiar pliku.

### P2: Czy program Aspose.Note jest kompatybilny z Visual Studio?

Odpowiedź 2: Tak, Aspose.Note można bezproblemowo zintegrować z Visual Studio do programowania .NET.

### P3: Czy istnieją ograniczenia dotyczące rozmiaru dokumentów programu OneNote, które można konwertować?

O3: Aspose.Note może obsługiwać duże dokumenty OneNote bez znaczących problemów z wydajnością.

### P4: Czy mogę zautomatyzować proces konwersji wielu dokumentów?

O4: Tak, możesz zautomatyzować proces konwersji za pomocą przetwarzania wsadowego za pomocą interfejsów API Aspose.Note.

### P5: Czy dostępna jest wersja próbna Aspose.Note?

 O5: Tak, możesz uzyskać bezpłatną wersję próbną Aspose.Note od[Tutaj](https://releases.aspose.com/).