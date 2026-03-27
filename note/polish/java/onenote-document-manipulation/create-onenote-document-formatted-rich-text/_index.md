---
date: 2026-02-18
description: Dowiedz się, jak tworzyć dokumenty OneNote, formatować tekst sformatowany
  i zapisywać je jako PDF w Javie przy użyciu Aspose.Note. Przewodnik krok po kroku
  dla płynnej automatyzacji.
linktitle: Create OneNote document and save as PDF in Java
second_title: Aspose.Note Java API
title: Utwórz dokument OneNote i zapisz go jako PDF w Javie
url: /pl/java/onenote-document-manipulation/create-onenote-document-formatted-rich-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Utwórz dokument OneNote i zapisz jako PDF w Javie

## Wprowadzenie

Jeśli potrzebujesz **utworzyć dokument onenote** i **zapisać OneNote jako PDF** zachowując formatowanie tekstu sformatowanego, trafiłeś we właściwe miejsce. W tym samouczku przeprowadzimy Cię przez tworzenie dokumentu OneNote, stosowanie niestandardowych stylów i eksportowanie go bezpośrednio do PDF przy użyciu Aspose.Note for Java. Po zakończeniu będziesz mieć gotowy fragment kodu, który możesz wkleić do dowolnego projektu Java, aby zautomatyzować eleganckie konwersje OneNote‑do‑PDF.

## Szybkie odpowiedzi
- **Co ten samouczek uczy?** Jak utworzyć dokument OneNote ze stylowanym tekstem i zapisać go jako PDF.  
- **Jakiej biblioteki wymaga?** Aspose.Note for Java (do pobrania ze strony oficjalnej).  
- **Czy potrzebuję licencji?** Tymczasowa licencja działa w testach; pełna licencja jest wymagana w produkcji.  
- **Jakiego IDE mogę używać?** Dowolne IDE Java — IntelliJ IDEA, Eclipse lub NetBeans.  
- **Czy mogę zmienić format wyjściowy?** Tak, Aspose.Note obsługuje PDF, HTML, PNG i inne.

## Co to jest „save onenote pdf”?
Zapisanie OneNote jako PDF oznacza konwersję struktury strony OneNote — w tym tekstu, obrazów i formatowania — do statycznego pliku PDF, który może być wyświetlany na dowolnej platformie bez potrzeby posiadania OneNote.

## Dlaczego formatować sformatowany tekst w Javie?
Stosowanie **format rich text** bezpośrednio w Javie pozwala generować dokumenty, które wyglądają profesjonalnie i spełniają wytyczne Twojej marki bez ręcznej edycji.

## Wymagania wstępne

1. **Java Development Kit (JDK)** – dowolna aktualna wersja (8 lub wyższa).  
2. **Aspose.Note for Java JAR** – pobierz go z [download link](https://releases.aspose.com/note/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse lub dowolny edytor, którego preferujesz.  

## Importowanie pakietów

Zanim zaczniemy, zaimportuj niezbędne klasy do swojego pliku Java:

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

## Jak utworzyć dokument OneNote – przewodnik krok po kroku

### Krok 1: Konfiguracja dokumentu i strony

Zainicjalizuj obiekty `Document` i `Page`, które będą przechowywać całą zawartość:

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

### Krok 2: Utwórz tytuł z formatowaniem

Dodaj element tytułu i zastosuj **set paragraph style**, aby kontrolować jego wygląd:

```java
Title title = new Title();
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);

RichText titleText = new RichText().append("Title!");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
```

### Krok 3: Utwórz sformatowany tekst

Tutaj budujemy zawartość sformatowanego tekstu przy użyciu kilku obiektów `TextStyle`, aby zademonstrować **rich text formatting**:

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();

TextStyle textStyleForHelloWord = new TextStyle()
                                        .setFontColor(Color.red)
                                        .setFontName("Arial")
                                        .setFontSize(10);

TextStyle textStyleForOneNoteWord = new TextStyle()
                                        .setFontColor(Color.green)
                                        .setFontName("Calibri")
                                        .setFontSize(10)
                                        .setItalic(true);

TextStyle textStyleForTextWord = new TextStyle()
                                        .setFontColor(Color.blue)
                                        .setFontName("Arial")
                                        .setFontSize(15)
                                        .setBold(true)
                                        .setItalic(true);

RichText text = new RichText()
        .append("Hello", textStyleForHelloWord)
        .append(" OneNote", textStyleForOneNoteWord)
        .append(" text", textStyleForTextWord)
        .append("!", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
```

### Krok 4: Dodaj elementy do strony i dokumentu

Połącz tytuł i sformatowany tekst w hierarchii strony:

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.setTitle(title);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

### Krok 5: Zapisz dokument – eksportuj onenote pdf

Na koniec wyeksportuj dokument OneNote jako plik PDF:

```java
doc.save(dataDir + "CreateOneNoteDocument_out.pdf", SaveFormat.Pdf);
```

## Typowe problemy i rozwiązania

| Problem | Rozwiązanie |
|---------|-------------|
| **Plik nie znaleziony** | Sprawdź, czy `dataDir` wskazuje istniejący folder i masz uprawnienia do zapisu. |
| **Brakujące czcionki** | Upewnij się, że czcionki, które odwołujesz (np. *Calibri*), są zainstalowane na komputerze. |
| **Licencja nie zastosowana** | Wczytaj licencję Aspose przed utworzeniem `Document`, aby uniknąć znaków wodnych wersji ewaluacyjnej. |

## Najczęściej zadawane pytania

**P: Czy mogę dalej dostosować style czcionek?**  
O: Tak, możesz dostosować dodatkowe właściwości, takie jak podkreślenie, przekreślenie i wyrównanie tekstu, za pomocą klas `TextStyle` i `ParagraphStyle`.

**P: Czy Aspose.Note for Java jest kompatybilny ze wszystkimi IDE Java?**  
O: Zdecydowanie. O ile IDE obsługuje standardowy rozwój w Javie, możesz dodać plik JAR Aspose.Note do ścieżki klas projektu.

**P: Czy mogę zintegrować tę funkcjonalność z aplikacjami webowymi?**  
O: Tak, ten sam kod działa w aplikacjach opartych na servletach lub Spring Boot, umożliwiając dynamiczne generowanie OneNote‑do‑PDF po stronie serwera.

**P: Czy istnieją wymagania licencyjne dotyczące używania Aspose.Note for Java?**  
O: Licencja komercyjna jest wymagana do użytku produkcyjnego. Licencja tymczasowa jest dostępna do oceny i testów.

**P: Czy Aspose.Note for Java obsługuje inne formaty dokumentów oprócz OneNote?**  
O: Obsługuje PDF, HTML, PNG, JPEG i kilka innych formatów eksportu, dając Ci elastyczność konwersji stron OneNote do potrzebnego formatu.

## Zakończenie

W tym przewodniku pokazaliśmy, jak **utworzyć dokument OneNote**, zastosować **formatowanie tekstu sformatowanego** oraz **zapisać OneNote jako PDF** przy użyciu Aspose.Note for Java. Postępując zgodnie z instrukcjami krok po kroku, możesz zautomatyzować tworzenie eleganckich dokumentów OneNote i konwertować je do PDF w dowolnym rozwiązaniu opartym na Javie.

---

**Ostatnia aktualizacja:** 2026-02-18  
**Testowano z:** Aspose.Note for Java 24.11 (najnowsza w momencie pisania)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}