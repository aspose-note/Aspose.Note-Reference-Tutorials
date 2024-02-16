---
title: Pobierz listę punktorów lub numerów w tekście Aspose.Note
linktitle: Pobierz listę punktorów lub numerów w tekście Aspose.Note
second_title: Aspose.Note .NET API
description: Odblokuj potencjał Aspose.Note dla .NET dzięki naszemu przewodnikowi krok po kroku na temat odzyskiwania list punktowanych lub numerowanych. Podnieś swoje umiejętności manipulowania dokumentami OneNote!
type: docs
weight: 23
url: /pl/net/text-manipulation/retrieve-bullet-number-list/
---
## Wstęp
Witamy w świecie Aspose.Note dla .NET, solidnej i wszechstronnej biblioteki, która umożliwia programistom bezproblemową obsługę dokumentów OneNote. W tym samouczku zagłębimy się w proces pobierania list punktowanych lub numerowanych za pomocą Aspose.Note dla .NET. Niezależnie od tego, czy jesteś doświadczonym programistą, czy entuzjastą kodowania, ten przewodnik wyposaży Cię w wiedzę niezbędną do poruszania się po zawiłościach pracy z listami w Aspose.Note.
## Warunki wstępne
Zanim wyruszymy w tę podróż kodowania, upewnij się, że spełniasz następujące wymagania wstępne:
-  Aspose.Note dla .NET: Upewnij się, że masz zainstalowaną bibliotekę Aspose.Note. Jeśli nie, możesz pobrać go ze strony[Aspose.Note dla dokumentacji .NET](https://reference.aspose.com/note/net/).
- Środowisko programistyczne: Przygotuj działające środowisko programistyczne, najlepiej Microsoft Visual Studio, na swoim komputerze.
- Podstawowa znajomość języka C#: Zapoznaj się z językiem C#, ponieważ ten samouczek jest napisany w tym języku.
## Importuj przestrzenie nazw
Aby móc współdziałać z Aspose.Note dla .NET, musisz zaimportować niezbędne przestrzenie nazw do swojego projektu. Na początku kodu umieść następujące przestrzenie nazw:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
```
A teraz przeanalizujmy krok po kroku proces odzyskiwania list punktowanych i numerowanych:
## Krok 1: Ustaw katalog dokumentów
```csharp
// Ścieżka do katalogu dokumentów.
string dataDir = "Your Document Directory";
```
 Zastępować`"Your Document Directory"` z rzeczywistą ścieżką, w której znajduje się dokument Aspose.Note.
## Krok 2: Załaduj dokument
```csharp
// Załaduj dokument do Aspose.Note.
Document oneFile = new Document(dataDir + "ApplyNumberingOnText.one");
```
 Upewnij się, że wymieniłeś`"ApplyNumberingOnText.one"` z nazwą konkretnego dokumentu OneNote.
## Krok 3: Pobierz kolekcję węzłów
```csharp
// Pobierz kolekcję węzłów elementu konspektu.
IList<OutlineElement> nodes = oneFile.GetChildNodes<OutlineElement>();
```
Ten krok pobiera kolekcję węzłów konspektu z załadowanego dokumentu.
## Krok 4: Iteruj przez każdy węzeł
```csharp
// Iteruj przez każdy węzeł.
foreach (OutlineElement node in nodes)
{
    if (node.NumberList != null)
    {
        NumberList list = node.NumberList;
        // Przejdź do kolejnych kroków...
    }
}
```
Dzięki tej pętli mamy do czynienia tylko z węzłami, które zawierają listę numerów.
## Krok 5: Pobierz informacje o czcionce
```csharp
// Pobierz nazwę czcionki
Console.WriteLine("Font Name: " + list.Font);
// Pobierz długość czcionki
Console.WriteLine("Font Length: " + list.Font.Length);
// Pobierz rozmiar czcionki
Console.WriteLine("Font Size: " + list.FontSize);
// Pobierz kolor czcionki
Console.WriteLine("Font Color: " + list.FontColor);
// Pobierz format
Console.WriteLine("Font format: " + list.Format);
// Zaznacz pogrubienie
Console.WriteLine("Is bold: " + list.IsBold);
// Sprawdź kursywę
Console.WriteLine("Is italic: " + list.IsItalic);
Console.WriteLine();
```
Te linie kodu wyodrębniają różne informacje związane z czcionkami z listy numerów.
## Wniosek
 Gratulacje! Pomyślnie nauczyłeś się, jak pobierać listy wypunktowane lub numerowane za pomocą Aspose.Note dla .NET. Kontynuując eksplorację, zapoznaj się z sekcją[dokumentacja](https://reference.aspose.com/note/net/) aby uzyskać bardziej szczegółowe informacje i funkcje.
## Często zadawane pytania
### Czy mogę używać Aspose.Note dla .NET z innymi językami programowania?
Aspose.Note obsługuje przede wszystkim .NET, ale istnieją inne wersje biblioteki dostosowane do różnych platform i języków.
### Czy Aspose.Note jest kompatybilny z najnowszymi formatami OneNote?
Tak, Aspose.Note obsługuje szeroką gamę formatów OneNote, zapewniając kompatybilność z najnowszymi wersjami.
### Jak mogę uzyskać tymczasową licencję na Aspose.Note?
 Odwiedzać[ten link](https://purchase.aspose.com/temporary-license/) w celu uzyskania tymczasowej licencji do celów ewaluacyjnych.
### Jakie opcje wsparcia są dostępne dla użytkowników Aspose.Note?
Możesz przeglądać i szukać pomocy w[Forum Aspose.Note](https://forum.aspose.com/c/note/28) w przypadku jakichkolwiek pytań lub problemów, które możesz napotkać.
### Czy istnieje bezpłatna wersja próbna Aspose.Note dla .NET?
 Tak, możesz uzyskać dostęp do bezpłatnej wersji próbnej Aspose.Note dla .NET[Tutaj](https://releases.aspose.com/).