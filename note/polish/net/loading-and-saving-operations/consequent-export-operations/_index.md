---
title: Konsekwentne operacje eksportowe w Aspose.Note
linktitle: Konsekwentne operacje eksportowe w Aspose.Note
second_title: Aspose.Note .NET API
description: Dowiedz się, jak wykonywać kolejne operacje eksportu w Aspose.Note dla .NET, aby efektywnie zapisywać dokumenty OneNote w różnych formatach.
type: docs
weight: 10
url: /pl/net/loading-and-saving-operations/consequent-export-operations/
---
## Wstęp

W tym samouczku zagłębimy się w wykonywanie kolejnych operacji eksportu przy użyciu Aspose.Note dla .NET. Aspose.Note to potężna biblioteka, która umożliwia programistom programową pracę z plikami Microsoft OneNote. Eksportowanie dokumentów do różnych formatów jest powszechnym wymaganiem, a Aspose.Note skutecznie upraszcza to zadanie. Przyjrzyjmy się krok po kroku, jak zapisać dokument w różnych formatach.

## Warunki wstępne

Przed kontynuowaniem tego samouczka upewnij się, że posiadasz następujące elementy:

1. Podstawowa znajomość języka programowania C#.
2. Program Visual Studio zainstalowany w systemie.
3. Biblioteka Aspose.Note dla .NET zintegrowana z Twoim projektem.

## Importuj przestrzenie nazw

Na początek pamiętaj o zaimportowaniu niezbędnych przestrzeni nazw do kodu C#:

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Drawing;
using System.Globalization;
```

## Krok 1: Zainicjuj dokument

 Po pierwsze, zainicjuj nowy`Document` obiekt z wyłączonym automatycznym wykrywaniem zmian układu:

```csharp
Document doc = new Document() { AutomaticLayoutChangesDetectionEnabled = false };
```

## Krok 2: Zainicjuj nową stronę

 Stwórz nowy`Page`obiekt i określ jego właściwości:

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## Krok 3: Ustaw tytuł strony

Zdefiniuj tytuł strony wraz z informacją o dacie i godzinie:

```csharp
ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
page.Title = new Title(doc)
{
    TitleText = new RichText(doc) { Text = "Title text.", ParagraphStyle = textStyle },
    TitleDate = new RichText(doc) { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
    TitleTime = new RichText(doc) { Text = "12:34", ParagraphStyle = textStyle }
};
```

## Krok 4: Dołącz węzeł strony

Dodaj węzeł strony do dokumentu:

```csharp
doc.AppendChildLast(page);
```

## Krok 5: Zapisz dokument w różnych formatach

Teraz zapisz dokument OneNote w różnych formatach:

```csharp
string dataDir = "Your Document Directory";
doc.Save(dataDir + "ConsequentExportOperations_out.html");            
doc.Save(dataDir + "ConsequentExportOperations_out.pdf");            
doc.Save(dataDir + "ConsequentExportOperations_out.jpg");            
textStyle.FontSize = 11;           
doc.DetectLayoutChanges();            
doc.Save(dataDir + "ConsequentExportOperations_out.bmp");
```

## Wniosek

Podsumowując, nauczyliśmy się wykonywać kolejne operacje eksportu za pomocą Aspose.Note dla .NET. Wykonując czynności opisane w tym samouczku, możesz bezproblemowo zapisywać dokumenty programu OneNote w różnych formatach, zwiększając w ten sposób wszechstronność aplikacji.

## Często zadawane pytania

### P1: Czy mogę bardziej dostosować tytuł strony?

O1: Tak, przed zapisaniem dokumentu możesz zmodyfikować tekst tytułu, datę i godzinę zgodnie ze swoimi wymaganiami.

### P2: Jak radzić sobie z wykrywaniem zmian w układzie?

 O2: Jak pokazano, możesz ręcznie wykryć zmiany układu za pomocą`DetectLayoutChanges()` metoda dostarczona przez Aspose.Note.

### P3: Czy Aspose.Note obsługuje inne formaty eksportu oprócz wymienionych?

O3: Tak, Aspose.Note obsługuje szeroką gamę formatów eksportu, w tym DOCX, PNG, TIFF i inne.

### P4: Czy Aspose.Note jest kompatybilny z .NET Core?

O4: Tak, Aspose.Note jest kompatybilny zarówno ze środowiskami .NET Framework, jak i .NET Core.

### P5: Gdzie mogę znaleźć więcej zasobów i wsparcia dla Aspose.Note?

Odpowiedź 5: Możesz odwiedzić dokumentację i forum Aspose.Note, aby uzyskać wyczerpujące przewodniki, samouczki i wsparcie społeczności.