---
title: Dodaj węzeł tekstowy ze znacznikiem w programie OneNote — Aspose.Note
linktitle: Dodaj węzeł tekstowy ze znacznikiem w programie OneNote — Aspose.Note
second_title: Aspose.Note API Java
description: Dowiedz się, jak dodawać węzły tekstowe ze znacznikami w programie OneNote przy użyciu Aspose.Note dla języka Java. Łatwe, wydajne i przyjazne dla programistów. Pobierz bibliotekę teraz!
type: docs
weight: 13
url: /pl/java/onenote-tag-operations/add-text-node-with-tag/
---
## Wstęp
W tym samouczku omówimy, jak dodać węzeł tekstowy ze znacznikiem w programie OneNote przy użyciu programu Aspose.Note dla języka Java. Aspose.Note to potężna biblioteka Java, która umożliwia programistom programową pracę z plikami Microsoft OneNote. Dodawanie węzłów tekstowych ze znacznikami jest częstym wymogiem w przetwarzaniu dokumentów, a Aspose.Note upraszcza to zadanie.
## Warunki wstępne
Zanim przejdziemy do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:
- Podstawowa znajomość programowania w języku Java.
-  Zainstalowana biblioteka Aspose.Note dla Java. Możesz go pobrać[Tutaj](https://releases.aspose.com/note/java/).
- Zintegrowane środowisko programistyczne (IDE) skonfigurowane do programowania w języku Java.
## Importuj pakiety
Rozpocznij od zaimportowania niezbędnych pakietów dla projektu Java. W swoim kodzie uwzględnij następujące importy:
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.TagIcon;
import com.aspose.note.ParagraphStyle;
```
## Krok 1: Utwórz obiekt dokumentu
Zainicjuj obiekt klasy Dokument, który będzie reprezentował dokument OneNote:
```java
// Ścieżka do katalogu dokumentów.
String dataDir = "Your Document Directory";
//Utwórz obiekt klasy Dokument
Document doc = new Document();
```
## Krok 2: Zainicjuj obiekt klasy strony
Zainicjuj obiekt klasy Page, który będzie reprezentował stronę w dokumencie:
```java
// Zainicjuj obiekt klasy Page
Page page = new Page();
```
## Krok 3: Zainicjuj obiekt klasy Outline
Zainicjuj obiekt klasy Outline, aby uporządkować zawartość strony:
```java
// Zainicjuj obiekt klasy Outline
Outline outline = new Outline();
```
## Krok 4: Zainicjuj obiekt klasy OutlineElement
Zainicjuj obiekt klasy OutlineElement, aby reprezentował element w konspekcie:
```java
// Zainicjuj obiekt klasy OutlineElement
OutlineElement outlineElem = new OutlineElement();
```
## Krok 5: Dostosuj styl tekstu
Skonfiguruj styl węzła tekstowego, taki jak kolor czcionki, nazwa i rozmiar:
```java
// Dostosuj styl tekstu
ParagraphStyle textStyle = new ParagraphStyle()
                                .setFontColor(Color.BLACK)
                                .setFontName("Arial")
                                .setFontSize(10);
```
## Krok 6: Utwórz obiekt RichText
Utwórz obiekt RichText i dołącz do niego żądany tekst:
```java
// Utwórz obiekt RichText
RichText text = new RichText().append("OneNote text.");
text.setParagraphStyle(textStyle);
```
## Krok 7: Dodaj znacznik notatki
Dodaj do tekstu znacznik notatki, na przykład żółtą gwiazdkę:
```java
// Dodaj znacznik notatki
NoteTag noteTag = NoteTag.createYellowStar();
text.getTags().add(noteTag);
```
## Krok 8: Dodaj węzeł tekstowy
Dodaj węzeł tekstowy do elementu konspektu:
```java
// Dodaj węzeł tekstowy
outlineElem.appendChildLast(text);
```
## Krok 9: Dodaj element konspektu do konspektu
Dodaj element konturu do konturu:
```java
// Dodaj węzeł elementu konspektu
outline.appendChildLast(outlineElem);
```
## Krok 10: Dodaj kontur do strony
Dodaj konspekt do strony:
```java
// Dodaj węzeł konspektu
page.appendChildLast(outline);
```
## Krok 11: Dodaj stronę do dokumentu
Dodaj stronę do dokumentu:
```java
// Dodaj węzeł strony
doc.appendChildLast(page);
```
## Krok 12: Zapisz dokument OneNote
Zapisz dokument programu OneNote w określonym katalogu:
```java
// Zapisz dokument programu OneNote
doc.save(dataDir + "AddTextNodeWithTag_out.one");
```
Gratulacje! Pomyślnie dodałeś węzeł tekstowy ze znacznikiem w OneNote przy użyciu Aspose.Note dla Java.
## Wniosek
W tym samouczku omówiliśmy krok po kroku proces dodawania węzła tekstowego ze znacznikiem w programie OneNote przy użyciu biblioteki Aspose.Note for Java. Ta potężna biblioteka upraszcza zadania przetwarzania dokumentów, ułatwiając programistom programowe manipulowanie plikami OneNote.
## Często Zadawane Pytania
### P: Czy mogę używać Aspose.Note dla Java z innymi bibliotekami Java?
O: Tak, Aspose.Note for Java można bezproblemowo zintegrować z innymi bibliotekami Java w celu zwiększenia możliwości przetwarzania dokumentów.
### P: Czy dostępna jest bezpłatna wersja próbna Aspose.Note dla Java?
 Odp.: Tak, możesz uzyskać dostęp do bezpłatnego okresu próbnego[Tutaj](https://releases.aspose.com/).
### P: Jak mogę uzyskać wsparcie dla Aspose.Note dla Java?
Odp.: Możesz zwrócić się o wsparcie do społeczności Aspose.Note[forum](https://forum.aspose.com/c/note/28).
### P: Czy dostępne są tymczasowe licencje dla Aspose.Note dla Java?
 Odpowiedź: Tak, możesz uzyskać licencje tymczasowe[Tutaj](https://purchase.aspose.com/temporary-license/).
### P: Gdzie mogę znaleźć dokumentację Aspose.Note dla Java?
 Odp.: Dokumentacja jest dostępna[Tutaj](https://reference.aspose.com/note/java/).