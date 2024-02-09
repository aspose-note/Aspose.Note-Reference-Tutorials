---
title: Uzyskaj informacje o obrazach w Aspose.Note
linktitle: Uzyskaj informacje o obrazach w Aspose.Note
second_title: Aspose.Note .NET API
description: Dowiedz się, jak wyodrębnić informacje o obrazie z plików Microsoft OneNote za pomocą Aspose.Note dla .NET. Postępuj zgodnie z naszym przewodnikiem krok po kroku, aby uzyskać efektywny rozwój.
type: docs
weight: 13
url: /pl/net/images/get-info-of-images/
---
## Wstęp

W świecie programowania .NET Aspose.Note zapewnia potężny zestaw narzędzi do pracy z plikami Microsoft OneNote. Jednym z typowych zadań, przed którymi często stają programiści, jest wyodrębnianie informacji z obrazów osadzonych w tych notatkach. Niezależnie od tego, czy chodzi o uzyskiwanie wymiarów, nazw plików czy czasów modyfikacji, Aspose.Note upraszcza ten proces.

## Warunki wstępne

Zanim zajmiemy się wyodrębnianiem informacji o obrazie za pomocą Aspose.Note, upewnij się, że masz następujące elementy:

1. Podstawowa znajomość języka C#: Znajomość języka programowania C# jest niezbędna do zrozumienia przykładów kodu.
2.  Zainstalowano Aspose.Note dla .NET: Upewnij się, że masz zainstalowaną bibliotekę Aspose.Note w swoim środowisku programistycznym. Możesz go pobrać[Tutaj](https://releases.aspose.com/note/net/).

## Importuj przestrzenie nazw

Zanim zaczniemy, zaimportujmy niezbędne przestrzenie nazw:

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System;
```

## Krok 1: Załaduj dokument

Najpierw załaduj docelowy dokument OneNote do Aspose.Note:

```csharp
// Ścieżka do katalogu dokumentów.
string dataDir = "Your Document Directory";

// Załaduj dokument do Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

 Zastępować`"Your Document Directory"` ze ścieżką do pliku OneNote.

## Krok 2: Pobierz informacje o obrazie

Następnie pobierz wszystkie węzły obrazu z dokumentu:

```csharp
// Pobierz wszystkie węzły obrazu
IList<Aspose.Note.Image> images = oneFile.GetChildNodes<Aspose.Note.Image>();
```

Ten fragment kodu pobiera wszystkie węzły obrazu w załadowanym dokumencie programu OneNote.

## Krok 3: Iteruj po obrazach

Przejdźmy teraz przez każdy węzeł obrazu, aby wyodrębnić jego metadane:

```csharp
foreach (Aspose.Note.Image image in images)
{
    Console.WriteLine("Width: {0}", image.Width);
    Console.WriteLine("Height: {0}", image.Height);
    Console.WriteLine("OriginalWidth: {0}", image.OriginalWidth);
    Console.WriteLine("OriginalHeight: {0}", image.OriginalHeight);
    Console.WriteLine("FileName: {0}", image.FileName);
    Console.WriteLine("LastModifiedTime: {0}", image.LastModifiedTime);
    Console.WriteLine();
}
```

Ta pętla wypisuje różne atrybuty każdego obrazu, takie jak szerokość, wysokość, oryginalne wymiary, nazwa pliku i czas ostatniej modyfikacji.

## Wniosek

Dzięki Aspose.Note dla .NET wyodrębnianie informacji o obrazie z dokumentów OneNote staje się płynnym procesem. Wykonując kroki opisane w tym samouczku, programiści mogą efektywnie pobierać metadane z osadzonych obrazów, co umożliwia im tworzenie niezawodnych aplikacji.

## Często zadawane pytania

### P1: Czy Aspose.Note jest kompatybilny ze wszystkimi wersjami Microsoft OneNote?

O1: Aspose.Note obsługuje różne formaty plików OneNote, w tym .one, .onepkg i .onetoc2, zapewniając kompatybilność w różnych wersjach.

### P2: Czy mogę modyfikować właściwości obrazu za pomocą Aspose.Note?

O2: Tak, Aspose.Note pozwala programowo manipulować właściwościami obrazu, takimi jak wymiary, nazwy plików i czasy modyfikacji.

### P3: Czy Aspose.Note oferuje wsparcie dla .NET Core?

O3: Tak, Aspose.Note zapewnia obsługę .NET Core, umożliwiając tworzenie aplikacji na wielu platformach.

### P4: Czy dostępna jest bezpłatna wersja próbna Aspose.Note?

Odpowiedź 4: Tak, możesz uzyskać dostęp do bezpłatnej wersji próbnej Aspose.Note, aby zapoznać się z jego funkcjami przed dokonaniem zakupu.

### P5: Gdzie mogę znaleźć dodatkowe wsparcie lub pomoc dotyczącą Aspose.Note?

 O5: W przypadku jakichkolwiek pytań lub pomocy możesz odwiedzić forum Aspose.Note[Tutaj](https://forum.aspose.com/c/note/28).