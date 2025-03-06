---
title: Utwórz chińską listę numerowaną w programie OneNote — Aspose.Note
linktitle: Utwórz chińską listę numerowaną w programie OneNote — Aspose.Note
second_title: Aspose.Note API Java
description: Usprawnij tworzenie dokumentów w Javie dzięki Aspose.Note. Dowiedz się krok po kroku, jak utworzyć chińską listę numerowaną w programie OneNote. Poznaj zaawansowane funkcje Aspose.Note.
weight: 13
url: /pl/java/onenote-text-manipulation/create-chinese-numbered-list/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Utwórz chińską listę numerowaną w programie OneNote — Aspose.Note

## Wstęp
Jeśli chcesz zwiększyć możliwości tworzenia dokumentów w Javie, Aspose.Note jest rozwiązaniem dla Ciebie. W tym samouczku przeprowadzimy Cię przez proces tworzenia chińskiej listy numerowanej w programie OneNote przy użyciu programu Aspose.Note dla języka Java. Ta potężna biblioteka umożliwia programowe manipulowanie dokumentami programu OneNote, zapewniając pełną kontrolę nad ich strukturą i zawartością.
## Warunki wstępne
Zanim przejdziesz do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:
1. Środowisko programistyczne Java: Upewnij się, że na komputerze jest skonfigurowane środowisko programistyczne Java.
2.  Biblioteka Aspose.Note: Pobierz i zainstaluj bibliotekę Aspose.Note. Możesz znaleźć link do pobrania[Tutaj](https://releases.aspose.com/note/java/).
## Importuj pakiety
Rozpocznij od zaimportowania niezbędnych pakietów do projektu Java. Pakiety te są niezbędne do wykorzystania funkcji Aspose.Note dla Java. Oto przykładowy fragment kodu:
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NumberFormat;
import com.aspose.note.NumberList;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.ParagraphStyle;
```
Podzielmy teraz kod na poszczególne kroki:
## Krok 1: Utwórz obiekt dokumentu
```java
// Ścieżka do katalogu dokumentów.
String dataDir = "Your Document Directory";
// utwórz obiekt klasy Dokument
Document doc = new Document();
```
## Krok 2: Zainicjuj obiekt strony
```java
// zainicjuj obiekt klasy Page
Page page = new Page();
```
## Krok 3: Zainicjuj obiekt konspektu
```java
// zainicjuj obiekt klasy Outline
Outline outline = new Outline();
```
## Krok 4: Zainicjuj obiekt TextStyle
```java
// zainicjuj obiekt klasy TextStyle i ustaw właściwości formatowania
ParagraphStyle defaultStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```
## Krok 5: Zainicjuj obiekty OutlineElement i zastosuj numerację
```java
// zainicjuj obiekty klasy OutlineElement i zastosuj numerację
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10));
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
OutlineElement outlineElem2 = new OutlineElement();
outlineElem2.setNumberList(new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10));
RichText text2 = new RichText().append("Second");
text2.setParagraphStyle(defaultStyle);
outlineElem2.appendChildLast(text2);
OutlineElement outlineElem3 = new OutlineElement();
outlineElem3.setNumberList(new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10));
RichText text3 = new RichText().append("Third");
text3.setParagraphStyle(defaultStyle);
outlineElem3.appendChildLast(text3);
```
## Krok 6: Dodaj elementy konspektu
```java
// dodaj elementy konturu
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```
## Krok 7: Dodaj węzeł konspektu do strony
```java
// dodaj węzeł Kontur
page.appendChildLast(outline);
```
## Krok 8: Dodaj węzeł strony do dokumentu
```java
// dodaj węzeł strony
doc.appendChildLast(page);
```
## Krok 9: Zapisz dokument
```java
// zapisz dokument
doc.save(dataDir + "CreateChineseNumberedList_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "CreateChineseNumberedList_out.pdf");
```
Teraz pomyślnie utworzyłeś chińską listę numerowaną w OneNote przy użyciu Aspose.Note dla Java!
## Wniosek
W tym samouczku omówiliśmy proces wykorzystania Aspose.Note dla języka Java do generowania chińskiej listy numerowanej w programie OneNote. Dzięki swoim zaawansowanym funkcjom Aspose.Note umożliwia programistom programowe manipulowanie i ulepszanie zawartości dokumentów.
## Często Zadawane Pytania
### Czy Aspose.Note jest kompatybilny z różnymi środowiskami Java?
Tak, Aspose.Note jest kompatybilny z popularnymi środowiskami Java IDE, takimi jak Eclipse i IntelliJ IDEA.
### Czy mogę dostosować formatowanie listy numerowanej?
Absolutnie. Jak pokazano w samouczku, możesz dostosować czcionkę, kolor i rozmiar, aby spełnić Twoje specyficzne wymagania.
### Czy dostępna jest wersja próbna Aspose.Note?
 Tak, możesz skorzystać z wersji próbnej[Tutaj](https://releases.aspose.com/).
### Gdzie mogę znaleźć szczegółową dokumentację Aspose.Note?
 Zapoznaj się z dokumentacją[Tutaj](https://reference.aspose.com/note/java/).
### Jak mogę uzyskać wsparcie dla Aspose.Note?
 Odwiedź forum pomocy[Tutaj](https://forum.aspose.com/c/note/28) w celu uzyskania pomocy lub pytań.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
