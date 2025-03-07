---
title: Utwórz listę numerowaną w programie OneNote — Aspose.Note
linktitle: Utwórz listę numerowaną w programie OneNote — Aspose.Note
second_title: Aspose.Note API Java
description: Dowiedz się, jak bez wysiłku utworzyć listę numerowaną w programie OneNote za pomocą Aspose.Note dla języka Java. Pobierz bezpłatną wersję próbną i zanurz się w świecie programowania Java!
weight: 14
url: /pl/java/onenote-text-manipulation/create-numbered-list/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Utwórz listę numerowaną w programie OneNote — Aspose.Note

## Wstęp
Aspose.Note dla Java umożliwia programistom Java płynną pracę z plikami Microsoft OneNote. W tym samouczku przeprowadzimy Cię przez proces tworzenia listy numerowanej w programie OneNote przy użyciu zaawansowanej biblioteki Aspose.Note dla języka Java.
## Warunki wstępne
Przed przystąpieniem do samouczka upewnij się, że spełnione są następujące wymagania wstępne:
- Zainstalowano zestaw Java Development Kit (JDK) na komputerze.
-  Aspose.Note dla biblioteki Java pobranej z[Tutaj](https://releases.aspose.com/note/java/).
## Importowanie pakietów
Najpierw zaimportujmy niezbędne pakiety do Twojego projektu Java, aby w pełni wykorzystać funkcjonalność Aspose.Note. Dołącz następujący kod do swojego projektu:
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
## Krok 1: Inicjowanie obiektów dokumentu, strony i konspektu
```java
// Twój katalog dokumentów
String dataDir = "Your Document Directory";
// Twórz obiekty Dokument, Strona i Konspekt
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
// Ustaw domyślny styl tekstu
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
```
## Krok 2: Ustawianie domyślnego stylu tekstu
```java
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
```
## Krok 3: Tworzenie elementów konspektu
Teraz utwórzmy elementy listy numerowanej.
```java
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10));
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
// Powtórz dla pozostałych elementów (outlineElem2 i konturElem3)
```
## Krok 4: Dodawanie elementów konspektu do konspektu
```java
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```
## Krok 5: Dodawanie konspektu do strony
```java
page.appendChildLast(outline);
```
## Krok 6: Zapisywanie dokumentu
```java
doc.appendChildLast(page);
doc.save(dataDir + "CreateNumberedList_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "CreateNumberedList_out.pdf");
```
Wykonaj dokładnie te kroki, a bez wysiłku utworzysz listę numerowaną w OneNote przy użyciu Aspose.Note dla Java.
## Wniosek
tym samouczku omówiliśmy bezproblemowy proces tworzenia listy numerowanej w programie OneNote przy użyciu programu Aspose.Note dla języka Java. Solidne funkcje biblioteki czynią ją nieocenionym narzędziem dla programistów Java pracujących z plikami Microsoft OneNote.
## Często Zadawane Pytania
### P: Czy mogę dostosować format numeracji na liście programu OneNote?
Odp.: Absolutnie! Możesz dostosować format numerowania, korzystając z klasy NumberList udostępnionej przez Aspose.Note dla Java.
### P: Czy dostępna jest wersja próbna Aspose.Note dla Java?
 Odp.: Tak, możesz pobrać bezpłatną wersję próbną[Tutaj](https://releases.aspose.com/).
### P: Jak mogę uzyskać wsparcie dla Aspose.Note dla Java?
 O: Odwiedź[Aspose.Note na forum Java](https://forum.aspose.com/c/note/28) za wsparcie społeczności.
### P: Gdzie mogę znaleźć szczegółową dokumentację Aspose.Note dla Java?
 Odp.: Patrz[dokumentacja](https://reference.aspose.com/note/java/) w celu uzyskania wyczerpujących informacji.
### P: Jak kupić licencję na Aspose.Note dla Java?
 Odpowiedź: Możesz kupić licencję[Tutaj](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
