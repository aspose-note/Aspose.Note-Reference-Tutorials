---
title: Dodaj węzeł tabeli ze znacznikiem w Aspose.Note
linktitle: Dodaj węzeł tabeli ze znacznikiem w Aspose.Note
second_title: Aspose.Note .NET API
description: Dowiedz się, jak dodawać tabele ze znacznikami w Aspose.Note dla .NET. Popraw swoje umiejętności programowego manipulowania dokumentami.
type: docs
weight: 11
url: /pl/net/tag-management/add-table-node-tag/
---
## Wstęp

W tym samouczku przeprowadzimy Cię przez proces dodawania węzła tabeli ze znacznikiem za pomocą Aspose.Note dla .NET. Aby to osiągnąć, wykonaj poniższe czynności.

## Importuj przestrzenie nazw

Zanim zaczniesz, pamiętaj o zaimportowaniu przestrzeni nazw niezbędnych do pracy z Aspose. Uwaga:

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using Aspose.Note.Examples.CSharp.Tables;
```

## Warunki wstępne

Przed kontynuowaniem upewnij się, że masz skonfigurowane następujące wymagania wstępne:

1.  Instalacja: Pobierz i zainstaluj bibliotekę Aspose.Note dla .NET z[Tutaj](https://releases.aspose.com/note/net/).
2.  Licencja: Zdobądź licencję lub użyj[licencja tymczasowa](https://purchase.aspose.com/temporary-license/) do korzystania z biblioteki.
3. Środowisko programistyczne: Skonfiguruj zgodne środowisko programistyczne, takie jak Visual Studio.

## Krok 1: Zainicjuj obiekty dokumentu i strony

 Zacznij od utworzenia instancji`Document` klasę i inicjowanie a`Page` obiekt:

```csharp
Document doc = new Document();
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## Krok 2: Utwórz obiekty tabeli, wiersza i komórki

 Zainicjuj`Table`, `TableRow` , I`TableCell` obiekty:

```csharp
TableRow row = new TableRow(doc);
TableCell cell = new TableCell(doc);
```

## Krok 3: Wstaw zawartość do komórki

 Dodaj zawartość do komórki za pomocą`AppendChildLast` metoda:

```csharp
cell.AppendChildLast(InsertTable.GetOutlineElementWithText(doc, "Single cell."));
```

## Krok 4: Zainicjuj węzeł tabeli

 Zainicjuj`Table` obiekt o określonych właściwościach:

```csharp
Table table = new Table(doc)
{
    IsBordersVisible = true,
    Columns = { new TableColumn { Width = 70 } }
};
```

## Krok 5: Dodaj wiersz do tabeli

Dodaj węzeł wiersza do tabeli:

```csharp
table.AppendChildLast(row);
```

## Krok 6: Dodaj tag do węzła tabeli

Dołącz tag dla węzła tabeli:

```csharp
table.Tags.Add(NoteTag.CreateQuestionMark());
```

## Krok 7: Dodaj węzeł tabeli do elementu konspektu

 Stworzyć`Outline` I`OutlineElement` aby dodać węzeł tabeli:

```csharp
Outline outline = new Outline(doc);
OutlineElement outlineElem = new OutlineElement(doc);
outlineElem.AppendChildLast(table);
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## Krok 8: Zapisz dokument

Zapisz dokument OneNote:

```csharp
string dataDir = "Your Document Directory";
dataDir = dataDir + "AddTableNodeWithTag_out.one";
doc.Save(dataDir);
Console.WriteLine("\nTable node with tag added successfully.\nFile saved at " + dataDir);
```

Po wykonaniu tych kroków powinieneś pomyślnie dodać węzeł tabeli ze znacznikiem przy użyciu Aspose.Note dla .NET.

## Wniosek

tym samouczku omówiliśmy proces dodawania węzła tabeli ze znacznikiem w Aspose.Note dla .NET. Wykonując te kroki, możesz efektywnie programowo manipulować dokumentami programu OneNote, zwiększając możliwości zarządzania dokumentami.

## Często zadawane pytania

### P1: Czy Aspose.Note jest kompatybilny ze wszystkimi wersjami .NET?

O1: Aspose.Note dla .NET obsługuje .NET Framework wersje 2.0 i nowsze, w tym .NET Core i .NET Standard.

### P2: Czy mogę wypróbować Aspose.Note przed zakupem licencji?

 A2: Tak, możesz uzyskać bezpłatną wersję próbną Aspose.Note od[Tutaj](https://releases.aspose.com/).

### P3: Jak zdobyć tymczasową licencję na Aspose.Note?

 A3: Możesz uzyskać tymczasową licencję od[ten link](https://purchase.aspose.com/temporary-license/), który jest ważny przez 30 dni.

### P4: Czy Aspose.Note obsługuje szyfrowanie dokumentów?

O4: Tak, Aspose.Note zapewnia obsługę szyfrowania dokumentów OneNote w celu zapewnienia bezpieczeństwa danych.

### P5: Czy dostępna jest pomoc techniczna dla użytkowników Aspose.Note?

 Odpowiedź 5: Tak, wsparcie techniczne jest zapewniane za pośrednictwem forów Aspose[Tutaj](https://forum.aspose.com/c/note/28), gdzie możesz zwrócić się o pomoc do ekspertów.