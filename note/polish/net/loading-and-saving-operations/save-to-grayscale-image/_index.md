---
title: Zapisz w obrazie w skali szarości w Aspose.Note
linktitle: Zapisz w obrazie w skali szarości w Aspose.Note
second_title: Aspose.Note .NET API
description: Dowiedz się, jak zapisywać dokumenty OneNote jako obrazy w skali szarości przy użyciu Aspose.Note dla .NET. Skorzystaj z tego obszernego samouczka, aby efektywnie przetwarzać dokumenty.
weight: 24
url: /pl/net/loading-and-saving-operations/save-to-grayscale-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zapisz w obrazie w skali szarości w Aspose.Note

## Wstęp

W tym samouczku odkryjemy, jak wykorzystać Aspose.Note dla .NET do zapisania dokumentu jako obrazu w skali szarości. Aspose.Note to potężna biblioteka, która umożliwia programistom programową pracę z plikami Microsoft OneNote, zapewniając szeroki zakres funkcjonalności.

## Warunki wstępne

Zanim przejdziemy dalej, upewnij się, że spełniasz następujące wymagania wstępne:

- Podstawowa znajomość języka programowania C#.
- Program Visual Studio zainstalowany w systemie.
-  Zainstalowana biblioteka Aspose.Note dla .NET. Możesz go pobrać[Tutaj](https://releases.aspose.com/note/net/).
- Znajomość dostępu i manipulowania plikami przy użyciu platformy .NET.

## Importuj przestrzenie nazw

Zacznijmy od zaimportowania niezbędnych przestrzeni nazw:

```csharp
using System;

using Aspose.Note.Saving;

```

## Krok 1: Załaduj dokument

Najpierw załaduj dokument do Aspose.Note. 

```csharp
string dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Krok 2: Zapisz jako obraz w skali szarości

Następnie określ ścieżkę zapisu obrazu w skali szarości i odpowiednio zapisz dokument.

```csharp
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
oneFile.Save(dataDir, new ImageSaveOptions(SaveFormat.Png)
					  {
						  ColorMode = ColorMode.GrayScale
					  });
```

## Krok 3: Sprawdź i wyświetl wynik

Na koniec sprawdź i wyświetl komunikat o pomyślnej konwersji wraz ze ścieżką pliku.

```csharp
Console.WriteLine("\nOneNote document converted successfully to grayscale image.\nFile saved at " + dataDir);
```

## Wniosek

W tym samouczku nauczyliśmy się, jak używać Aspose.Note dla .NET do konwertowania dokumentu na obraz w skali szarości. Wykonując te proste kroki, programiści mogą skutecznie włączyć tę funkcjonalność do swoich aplikacji, zwiększając możliwości przetwarzania dokumentów.

## Często zadawane pytania

### P1: Czy Aspose.Note obsługuje złożone pliki OneNote?

Odpowiedź 1: Tak, Aspose.Note może wydajnie obsługiwać złożone pliki OneNote, zapewniając solidne funkcje do manipulowania dokumentami.

### P2: Czy Aspose.Note jest kompatybilny z różnymi formatami plików?

Odpowiedź 2: Oczywiście, Aspose.Note obsługuje różne formaty plików, zapewniając elastyczność w przetwarzaniu dokumentów.

### P3: Czy Aspose.Note oferuje wsparcie dla programistów?

Odpowiedź 3: Tak, programiści mogą uzyskać dostęp do kompleksowego wsparcia za pośrednictwem forum Aspose i dokumentacji.

### P4: Czy mogę wypróbować Aspose.Note przed zakupem?

A4: Tak, możesz eksplorować Aspose.Note w ramach bezpłatnej wersji próbnej dostępnej na ich stronie internetowej.

### P5: Jak mogę uzyskać tymczasową licencję na Aspose.Note?

A5: Możesz uzyskać tymczasową licencję na Aspose.Note, odwiedzając podany link i postępując zgodnie z instrukcjami.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
