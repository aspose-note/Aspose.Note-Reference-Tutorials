---
title: Wstaw chińską listę numerów w tekście Aspose.Note
linktitle: Wstaw chińską listę numerów w tekście Aspose.Note
second_title: Aspose.Note .NET API
description: Dowiedz się, jak bez wysiłku wstawiać chińskie listy numerów w dokumentach Aspose.Note dla .NET. Podnieś swoje umiejętności formatowania dokumentów dzięki temu przewodnikowi krok po kroku.
type: docs
weight: 20
url: /pl/net/text-manipulation/insert-chinese-number-list/
---
## Wstęp
Czy chcesz ulepszyć swoje umiejętności Aspose.Note for .NET poprzez włączenie chińskich list numerów do swoich dokumentów? Jeśli tak, jesteś we właściwym miejscu! W tym samouczku przeprowadzimy Cię przez proces wstawiania chińskich list numerów za pomocą Aspose.Note dla .NET. Ta potężna biblioteka umożliwia płynne manipulowanie dokumentami programu OneNote.
## Warunki wstępne
Zanim przejdziemy do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:
- Podstawowa znajomość programowania w języku C#.
-  Zainstalowany Aspose.Note dla .NET. Możesz go pobrać[Tutaj](https://releases.aspose.com/note/net/).
## Importuj przestrzenie nazw
Aby rozpocząć, zaimportuj niezbędne przestrzenie nazw do swojego projektu:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## Krok 1: Zainicjuj dokument OneNote
```csharp
string dataDir = "Your Document Directory";
Aspose.Note.Document doc = new Aspose.Note.Document();
```
## Krok 2: Zainicjuj stronę OneNote
```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
Outline outline = new Outline(doc);
```
## Krok 3: Zastosuj ustawienia stylu tekstu
```csharp
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## Krok 4: Utwórz elementy konspektu
Utwórzmy teraz trzy elementy konspektu z chińskimi listami liczbowymi:
### Krok 4.1: Pierwszy element
```csharp
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
```
### Krok 4.2: Drugi element
```csharp
OutlineElement outlineElem2 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text2 = new RichText(doc) { Text = "Second", ParagraphStyle = defaultStyle };
outlineElem2.AppendChildLast(text2);
```
### Krok 4.3: Trzeci element
```csharp
OutlineElement outlineElem3 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text3 = new RichText(doc) { Text = "Third", ParagraphStyle = defaultStyle };
outlineElem3.AppendChildLast(text3);
```
## Krok 5: Dołącz elementy do konspektu
```csharp
outline.AppendChildLast(outlineElem1);
outline.AppendChildLast(outlineElem2);
outline.AppendChildLast(outlineElem3);
```
## Krok 6: Dołącz konspekt do strony
```csharp
page.AppendChildLast(outline);
```
## Krok 7: Dołącz stronę do dokumentu
```csharp
doc.AppendChildLast(page);
```
## Krok 8: Zapisz dokument OneNote
```csharp
dataDir = dataDir + "InsertChineseNumberList_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nChinese number list inserted successfully.\nFile saved at " + dataDir);
```
Gratulacje! Pomyślnie wstawiłeś chińskie listy numerów do swojego dokumentu Aspose.Note przy użyciu biblioteki .NET.
## Wniosek
W tym samouczku omówiliśmy krok po kroku proces włączania chińskich list numerów do dokumentów Aspose.Note dla .NET. Dzięki tym technikom rozwiń swoje umiejętności formatowania dokumentów i zwiększ atrakcyjność treści.
## Często zadawane pytania
### P: Czy mogę dostosować formatowanie chińskich list numerów?
 Odp.: Tak, możesz dostosować formatowanie, dostosowując parametry w pliku`NumberList` konstruktor.
### P: Czy Aspose.Note jest kompatybilny z najnowszą wersją .NET?
O: Tak, Aspose.Note jest regularnie aktualizowany, aby obsługiwał najnowsze wersje .NET.
### P: Gdzie mogę znaleźć dodatkowe przykłady i dokumentację?
O: Poznaj kompleksowość[Dokumentacja Aspose.Note](https://reference.aspose.com/note/net/).
### P: Jak mogę uzyskać tymczasową licencję na Aspose.Note?
 Odp.: Uzyskaj tymczasową licencję[Tutaj](https://purchase.aspose.com/temporary-license/).
### P: Gdzie mogę szukać pomocy lub omówić zapytania związane z Aspose.Note?
 O: Odwiedź[Forum wsparcia Aspose.Note](https://forum.aspose.com/c/note/28) za wsparcie społeczności.