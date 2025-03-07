---
title: Twórz tabele za pomocą Aspose.Note
linktitle: Twórz tabele za pomocą Aspose.Note
second_title: Aspose.Note .NET API
description: Dowiedz się, jak tworzyć tabele strukturalne z zawartością tekstu sformatowanego przy użyciu Aspose.Note dla .NET. Bez wysiłku popraw organizację i czytelność dokumentów.
weight: 11
url: /pl/net/table-manipulation/compose-tables/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Twórz tabele za pomocą Aspose.Note

## Wstęp

Tabele są podstawowymi elementami dokumentów, umożliwiającymi uporządkowaną prezentację informacji. Aspose.Note dla .NET zapewnia niezawodne narzędzia do łatwego tworzenia tabel. W tym samouczku przeprowadzimy Cię przez proces tworzenia tabel z bogatą zawartością tekstową przy użyciu Aspose.Note.

## Warunki wstępne

Zanim zagłębisz się w tworzenie tabeli za pomocą Aspose.Note dla .NET, upewnij się, że spełniasz następujące wymagania wstępne:

1. Konfiguracja środowiska: Upewnij się, że masz skonfigurowane odpowiednie środowisko programistyczne z .NET Framework lub .NET Core.
2.  Instalacja: Pobierz i zainstaluj Aspose.Note dla .NET z[strona internetowa](https://releases.aspose.com/note/net/).
3. Podstawowa wiedza: Zapoznaj się z podstawowymi koncepcjami programowania w języku C# i manipulowania dokumentami.

## Importuj przestrzenie nazw

Zanim zaczniesz tworzyć tabele, pamiętaj o zaimportowaniu niezbędnych przestrzeni nazw:

```csharp
using System;
using System.Drawing;
using System.IO;
using System.Linq;
```

Podzielmy podany przykład na łatwe do wykonania kroki:

## Krok 1: Skonfiguruj katalog dokumentów

Przed utworzeniem tabeli określ katalog, w którym zostanie zapisany dokument.

```csharp
string dataDir = "Your Document Directory";
```

## Krok 2: Utwórz tekst nagłówka

Zdefiniuj tekst nagłówka za pomocą określonych stylów, takich jak rozmiar czcionki i pogrubienie.

```csharp
var headerText = new RichText() { ParagraphStyle = new ParagraphStyle() { FontSize = 18, IsBold = true }, Alignment = HorizontalAlignment.Center }
					.Append("Super contest for suppliers.");
```

## Krok 3: Utwórz stronę i konspekt

Zainicjuj stronę i konspekt, aby uporządkować zawartość.

```csharp
var page = new Page();
var outline = page.AppendChildLast(new Outline() { HorizontalOffset = 50 });
outline.AppendChildLast(new OutlineElement()).AppendChildLast(headerText);
```

## Krok 4: Dodaj tekst podsumowania

Umieść tekst podsumowujący przed tabelą.

```csharp
var bodyTextHeader = outline.AppendChildLast(new OutlineElement()).AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default });
bodyTextHeader.Append("This is the final ranking of proposals got from our suppliers.");
```

## Krok 5: Utwórz tabelę

Zainicjuj tabelę, aby uporządkować dane w wierszach i kolumnach.

```csharp
var ranking = outline.AppendChildLast(new OutlineElement()).AppendChildLast(new Table());
```

## Krok 6: Dodaj wiersz nagłówka

Wypełnij tabelę wierszem nagłówka zawierającym tytuły kolumn.

```csharp
var headerRow = ranking.AppendChildFirst(new TableRow());
foreach (var header in new[] { "Supplier", "Contacts", "Score A", "Score B", "Score C", "Final score", "Attached materials", "Comments" })
{
   ranking.Columns.Add(new TableColumn());
   headerRow.AppendChildLast(new TableCell() { BackgroundColor = backGroundColor })
			 .AppendChildLast(new OutlineElement())
			 .AppendChildLast(new RichText() { ParagraphStyle = headerStyle })
			 .Append(header);
}
```

## Krok 7: Dodaj puste wiersze

Wstaw puste wiersze, aby przygotować się do wstawienia danych.

```csharp
for (int i = 0; i < 5; i++)
{
   backGroundColor = backGroundColor.IsEmpty ? Color.LightGray : Color.Empty;
   var row = ranking.AppendChildLast(new TableRow());
   for (int j = 0; j < ranking.Columns.Count(); j++)
   {
	   row.AppendChildLast(new TableCell() { BackgroundColor = backGroundColor })
		  .AppendChildLast(new OutlineElement())
		  .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default });
   }
}
```

## Krok 8: Dodaj informacje kontaktowe

Wypełnij kolumnę „Kontakty” treścią szablonu.

```csharp
foreach (var row in ranking.Skip(1))
{
   var contactsCell = row.ElementAt(1);
   contactsCell.AppendChildLast(new OutlineElement())
			   .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default })
			   .Append("Web: ").Append("link", new TextStyle() { HyperlinkAddress = "www.link.com", IsHyperlink = true });
   contactsCell.AppendChildLast(new OutlineElement())
			   .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default })
			   .Append("E-mail: ").Append("mail", new TextStyle() { HyperlinkAddress = "mailto:hi@link.com", IsHyperlink = true });
}
```

## Krok 9: Zapisz dokument

Zapisz utworzony dokument tabeli.

```csharp
var d = new Document();
d.AppendChildLast(page);
d.Save(Path.Combine(dataDir, "ComposeTable_out.one"));
```

## Krok 10: Potwierdzenie

Potwierdź pomyślną kompozycję dokumentu.

```csharp
Console.WriteLine("\nThe document is composed successfully.");
```

## Wniosek

W tym samouczku omówiliśmy, jak tworzyć tabele z zawartością tekstu sformatowanego przy użyciu Aspose.Note dla .NET. Postępując zgodnie z tymi szczegółowymi instrukcjami, możesz skutecznie tworzyć w dokumentach uporządkowane tabele, poprawiając czytelność i organizację.

## Często zadawane pytania

### P1: Czy mogę dostosować styl elementów stołu?
   
O1: Tak, możesz dostosować różne aspekty, takie jak rozmiar czcionki, kolor i wyrównanie, do swoich wymagań.

### P2: Czy Aspose.Note jest kompatybilny z innymi bibliotekami .NET?
   
Odpowiedź 2: Aspose.Note bezproblemowo integruje się z innymi bibliotekami .NET, oferując dużą elastyczność w manipulowaniu dokumentami.

### P3: Czy Aspose.Note obsługuje eksportowanie tabel do różnych formatów?
   
O3: Oczywiście, Aspose.Note umożliwia eksportowanie tabel do różnych formatów, w tym PDF, DOCX i HTML.

### P4: Czy mogę dynamicznie wypełniać tabele danymi ze źródeł zewnętrznych?
   
O4: Tak, możesz dynamicznie wypełniać tabele, pobierając dane z baz danych, interfejsów API lub danych wejściowych użytkownika.

### P5: Czy dostępna jest pomoc techniczna dla użytkowników Aspose.Note?
   
Odpowiedź 5: Tak, Aspose zapewnia kompleksowe wsparcie techniczne za pośrednictwem swoich forów i dedykowanych kanałów wsparcia.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
