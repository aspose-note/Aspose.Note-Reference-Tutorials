---
title: Zastosuj numerację tekstu w Aspose.Note
linktitle: Zastosuj numerację tekstu w Aspose.Note
second_title: Aspose.Note .NET API
description: Dzięki temu obszernemu samouczkowi dowiedz się, jak zastosować numerację tekstu w Aspose.Note dla .NET. Ulepsz formatowanie swojego dokumentu bez wysiłku.
weight: 12
url: /pl/net/text-manipulation/apply-numbering-on-text/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zastosuj numerację tekstu w Aspose.Note

## Wstęp
Aspose.Note dla .NET zapewnia potężne narzędzia do manipulacji dokumentami w aplikacjach C#. W tym samouczku omówimy proces stosowania numeracji tekstu za pomocą Aspose.Note. Postępuj zgodnie z tymi instrukcjami krok po kroku, aby bez wysiłku ulepszyć formatowanie dokumentu.
## Warunki wstępne
Zanim przejdziesz do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:
- Podstawowa znajomość języka programowania C#.
-  Zainstalowany Aspose.Note dla .NET. Możesz go pobrać[Tutaj](https://releases.aspose.com/note/net/).
- Zintegrowane środowisko programistyczne (IDE), takie jak Visual Studio.
## Importuj przestrzenie nazw
Aby rozpocząć, zaimportuj niezbędne przestrzenie nazw do swojego projektu C#:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## Krok 1: Skonfiguruj swój dokument
Rozpocznij od utworzenia nowego dokumentu i zainicjowania wymaganych obiektów:
```csharp
// Ścieżka do katalogu dokumentów.
string dataDir = "Your Document Directory";
//Utwórz obiekt klasy Dokument
Document doc = new Document();
// Zainicjuj obiekt klasy Page
Aspose.Note.Page page = new Aspose.Note.Page(doc);
// Zainicjuj obiekt klasy Outline
Outline outline = new Outline(doc);
```
## Krok 2: Zdefiniuj styl domyślny
Skonfiguruj domyślną stylizację tekstu za pomocą klasy ParagraphStyle:
```csharp
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## Krok 3: Zastosuj numerację
Zainicjuj obiekty klasy OutlineElement i zastosuj numerację do każdego elementu:
```csharp
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
OutlineElement outlineElem2 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text2 = new RichText(doc) { Text = "Second", ParagraphStyle = defaultStyle };
outlineElem2.AppendChildLast(text2);
OutlineElement outlineElem3 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text3 = new RichText(doc) { Text = "Third", ParagraphStyle = defaultStyle };
outlineElem3.AppendChildLast(text3);
```
## Krok 4: Dodaj elementy konspektu
Dołącz elementy konspektu do konspektu:
```csharp
outline.AppendChildLast(outlineElem1);
outline.AppendChildLast(outlineElem2);
outline.AppendChildLast(outlineElem3);
```
## Krok 5: Zapisz dokument
Zapisz dokument OneNote z zastosowaną numeracją:
```csharp
dataDir = dataDir + "ApplyNumberingOnText_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nNumbering applied successfully on a text.\nFile saved at " + dataDir); 
```
## Wniosek
Gratulacje! Pomyślnie nauczyłeś się, jak stosować numerację tekstu w Aspose.Note dla .NET. Eksperymentuj z różnymi opcjami formatowania, aby bez wysiłku tworzyć atrakcyjne wizualnie dokumenty.
## Często zadawane pytania
### 1. Czy mogę dostosować format numeracji?
Tak, klasa NumberList umożliwia dostosowanie formatu numeracji zgodnie z własnymi preferencjami.
### 2. Czy dostępne są inne opcje formatowania?
Aspose.Note zapewnia szeroką gamę opcji formatowania, w tym styl czcionki, kolor i inne.
### 3. Czy Aspose.Note jest kompatybilny z Visual Studio?
Absolutnie! Aspose.Note bezproblemowo integruje się z Visual Studio, zapewniając płynne środowisko programistyczne.
### 4. Czy mogę wypróbować Aspose.Note przed zakupem?
 Z pewnością! Możesz skorzystać z bezpłatnego okresu próbnego[Tutaj](https://releases.aspose.com/).
### 5. Gdzie mogę uzyskać pomoc dotyczącą Aspose.Note?
 Aby uzyskać pomoc lub zadać pytania, odwiedź stronę[Forum Aspose.Note](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
