---
title: Twórz dokumenty z katalogiem głównym i podstronami za pomocą Aspose.Note
linktitle: Twórz dokumenty z katalogiem głównym i podstronami za pomocą Aspose.Note
second_title: Aspose.Note .NET API
description: Dowiedz się, jak używać Aspose.Note dla .NET do tworzenia dynamicznych dokumentów OneNote o strukturach hierarchicznych.
weight: 11
url: /pl/net/note-manipulation/create-documents-root-sub-pages/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Twórz dokumenty z katalogiem głównym i podstronami za pomocą Aspose.Note

## Wstęp

Witamy w naszym samouczku na temat tworzenia dokumentów z katalogiem głównym i podstronami przy użyciu Aspose.Note dla .NET! Aspose.Note to potężna biblioteka, która umożliwia programistom programową pracę z plikami Microsoft OneNote, umożliwiając tworzenie, manipulowanie i konwersję dokumentów OneNote.

tym samouczku przeprowadzimy Cię krok po kroku przez proces tworzenia dokumentu OneNote z katalogiem głównym i stronami podrzędnymi. Dostarczymy szczegółowe wyjaśnienia i fragmenty kodu przy użyciu Aspose.Note dla .NET, co ułatwi ci śledzenie i wdrażanie we własnych projektach.

## Warunki wstępne

Zanim zaczniemy, upewnij się, że masz następujące wymagania wstępne:

1. Visual Studio: Aby pisać i kompilować kod .NET, będziesz potrzebować zainstalowanego programu Visual Studio w swoim systemie.
2.  Aspose.Note dla .NET: Pobierz i zainstaluj Aspose.Note dla .NET z[strona pobierania](https://releases.aspose.com/note/net/).
3. Podstawowa znajomość języka C#: Do zrozumienia i wdrożenia przykładów kodu wymagana jest znajomość języka programowania C#.

Teraz, gdy już wszystko skonfigurowałeś, przejdźmy do samouczka!

## Importuj przestrzenie nazw

Najpierw zaimportujmy niezbędne przestrzenie nazw do naszego projektu:

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using System.Drawing;
```

## Krok 1: Zainicjuj obiekt dokumentu

```csharp
//Utwórz obiekt klasy Dokument
Document doc = new Document();
```

## Krok 2: Utwórz stronę główną i strony podrzędne

```csharp
// Zainicjuj obiekty klasy Page i ustaw ich poziomy
Page page1 = new Page(doc) { Level = 1 };
Page page2 = new Page(doc) { Level = 2 };
Page page3 = new Page(doc) { Level = 1 };
```

### Dla strony 1:

```csharp
Outline outline1 = new Outline(doc);
OutlineElement outlineElem1 = new OutlineElement(doc);
ParagraphStyle textStyle1 = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text1 = new RichText(doc) { Text = "First page.", ParagraphStyle = textStyle1 };
outlineElem1.AppendChildLast(text1);
outline1.AppendChildLast(outlineElem1);
page1.AppendChildLast(outline1);
```

### Dla strony 2:

```csharp
Outline outline2 = new Outline(doc);
OutlineElement outlineElem2 = new OutlineElement(doc);
ParagraphStyle textStyle2 = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text2 = new RichText(doc) { Text = "Second page.", ParagraphStyle = textStyle2 };
outlineElem2.AppendChildLast(text2);
outline2.AppendChildLast(outlineElem2);
page2.AppendChildLast(outline2);
```

### Dla strony 3:

```csharp
Outline outline3 = new Outline(doc);
OutlineElement outlineElem3 = new OutlineElement(doc);
ParagraphStyle textStyle3 = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text3 = new RichText(doc) { Text = "Third page.", ParagraphStyle = textStyle3 };
outlineElem3.AppendChildLast(text3);
outline3.AppendChildLast(outlineElem3);
page3.AppendChildLast(outline3);
```

## Krok 4: Dodaj strony do dokumentu

```csharp
// Dodaj strony do dokumentu programu OneNote
doc.AppendChildLast(page1);
doc.AppendChildLast(page2);
doc.AppendChildLast(page3);
```

## Krok 5: Zapisz dokument

```csharp
// Zapisz dokument programu OneNote
string dataDir = "Your Document Directory";
dataDir = dataDir + "CreateDocWithRootAndSubPages_out.one";
doc.Save(dataDir);
```

## Wniosek

Gratulacje! Pomyślnie nauczyłeś się tworzyć dokumenty z katalogiem głównym i podstronami przy użyciu Aspose.Note dla .NET. Teraz możesz wykorzystać tę wiedzę do dynamicznego generowania złożonych dokumentów OneNote w swoich aplikacjach.

## Często zadawane pytania

### P1: Czy Aspose.Note obsługuje duże dokumenty OneNote?

Odpowiedź 1: Tak, Aspose.Note został zaprojektowany do wydajnej obsługi dużych dokumentów OneNote bez pogarszania wydajności.

### P2: Czy Aspose.Note jest kompatybilny z .NET Core?

Odpowiedź 2: Tak, Aspose.Note obsługuje .NET Core wraz z tradycyjnym .NET Framework.

### P3: Czy mogę konwertować dokumenty OneNote na inne formaty za pomocą Aspose.Note?

A3: Oczywiście, Aspose.Note zapewnia możliwości konwersji do różnych formatów, w tym PDF, DOCX, HTML i innych.

### P4: Czy Aspose.Note oferuje integrację z chmurą?

Odpowiedź 4: Aspose.Note koncentruje się głównie na programowaniu lokalnym, ale można go używać w środowiskach chmurowych po odpowiedniej konfiguracji.

### P5: Czy dostępna jest pomoc techniczna dla Aspose.Note?

Odpowiedź 5: Tak, Aspose zapewnia dedykowane wsparcie techniczne za pośrednictwem swojego forum, na którym możesz zadawać pytania i uzyskać pomoc.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
