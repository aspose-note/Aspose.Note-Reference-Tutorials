---
date: 2025-12-09
description: Dowiedz się, jak zapisać OneNote jako PDF z sformatowanym tekstem bogatym
  w Javie, używając Aspose.Note for Java. Postępuj zgodnie z naszym przewodnikiem
  krok po kroku, aby uzyskać płynną automatyzację dokumentów.
linktitle: Save OneNote as PDF with Formatted Rich Text in Java
second_title: Aspose.Note Java API
title: Zapisz OneNote jako PDF z sformatowanym tekstem bogatym w Java
url: /pl/java/onenote-document-manipulation/create-onenote-document-formatted-rich-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zapisz OneNote jako PDF z sformatowanym tekstem bogatym w Java

## Wprowadzenie

Jeśli potrzebujesz **zapisz OneNote jako PDF** zachowując formatowanie tekstu bogatego, trafiłeś we właściwe miejsce. W tym samouczku przeprowadzimy Cię przez tworzenie dokumentu OneNote, stosowanie niestandardowych stylów i eksportowanie go bezpośrednio do PDF przy użyciu Aspose.Note for Java. Na końcu będziesz mieć wielokrotnego użytku fragment kodu, który możesz wstawić do dowolnego projektu Java, aby zautomatyzować eleganckie konwersje OneNote‑do‑PDF.

## Szybkie odpowiedzi
- **Co uczy ten samouczek?** Jak stworzyć dokument OneNote ze stylowanym tekstem i zapisać go jako PDF.  
- **Jakiej biblioteki wymaga?** Aspose.Note for Java (do pobrania ze strony oficjalnej).  
- **Czy potrzebna jest licencja?** Tymczasowa licencja działa w testach; pełna licencja jest wymagana w produkcji.  
- **Jakie IDE mogę używać?** Dowolne IDE Java — IntelliJ IDEA, Eclipse lub NetBeans.  
- **Czy mogę zmienić format wyjściowy?** Tak, Aspose.Note obsługuje PDF, HTML, i inne.

## Co to jest „zapisz OneNote jako PDF”?
Zapisanie OneNote jako PDF oznacza konwersję struktury strony OneNote — w tym tekstu, obrazów i formatowania — do statycznego pliku PDF, który może być wyświetlany na dowolnej platformie bez potrzeby posiadania OneNote.

## Dlaczego formatować tekst bogaty w Java?
Stosowanie formatowania tekstu bogatego (czcionki, kolory, style) bezpośrednio w Javie pozwala generować dokumenty wyglądające profesjonalnie i zgodne z wytycznymi marki, bez ręcznej edycji.

## Wymagania wstępne

1. **Java Development Kit (JDK)** – dowolna aktualna wersja (8 lub wyższa).  
2. **Aspose.Note for Java JAR** – pobierz go z [download link](https://releases.aspose.com/note/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse lub dowolny edytor, który preferujesz.  

## Importowanie pakietów

Najpierw musisz zaimportować niezbędne pakiety do swojego projektu Java. Dodaj następujące instrukcje importu na początku pliku Java:

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

## Krok 1: Konfiguracja dokumentu i strony

Rozpocznijmy od zainicjowania obiektów `Document` i `Page`:

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

## Krok 2: Utwórz tytuł z formatowaniem

Teraz utwórzmy tytuł z sformatowanym tekstem:

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

## Krok 3: Utwórz tekst bogaty z formatowaniem

Następnie utwórzmy tekst bogaty z różnymi stylami formatowania:

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

## Krok 4: Dodaj elementy do strony i dokumentu

Teraz dodajmy tytuł i tekst bogaty do strony oraz elementów konspektu:

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.setTitle(title);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## Krok 5: Zapisz dokument

Na koniec zapisz utworzony dokument OneNote jako PDF:

```java
doc.save(dataDir + "CreateOneNoteDocument_out.pdf", SaveFormat.Pdf);
```

## Typowe problemy i rozwiązania

| Problem | Rozwiązanie |
|-------|----------|
| **File not found** | Zwfikuj, czy `dataDir` wskazuje istniejący folder i masz uprawnienia do zapisu. |
| **Missing fonts** | Upewnij się, że czcionki, które odwołujesz (np. *Calibri*), są zainstalowane na maszynie hosta. |
| **License not applied** | Załaduj licencję Aspose przed utworzeniem `Document`, aby uniknąć znaków wodnych wersji ewaluacyjnej. |

## Najczęściej zadawane pytania

**P: Czy mogę dalej dostosować style czcionek?**  
O: Tak, możesz dostosować dodatkowe właściwości, takie jak podkreślenie, przekreślenie i wyrównanie tekstu za pomocą klas `TextStyle` i `ParagraphStyle`.

**P: Czy Aspose.Note for Java jest kompatybilny ze wszystkimi IDE Java?**  
O: Zdecydowanie tak. O ile IDE obsługuje standardowy rozwój w Javie, możesz dodać plik JAR Aspose.Note do ścieżki klas projektu.

**P: Czy mogę zintegrować tę funkcjonalność z aplikacjami webowymi?**  
O: Tak, ten sam kod działa w aplikacjach opartych na servletach lub Spring Boot, umożliwiając dynamiczne generowanie OneNote‑do‑PDF po stronie serwera.

**P: Czy istnieją wymagania licencyjne dotyczące używania Aspose.Note for Java?**  
O: Licencja komercyjna jest wymagana do użytku produkcyjnego. Tymczasowa licencja jest dostępna do oceny i testów.

**P: Czy Aspose.Note for Java obsługuje inne formaty dokumentów oprócz OneNote?**  
O: Obsługuje PDF, HTML, PNG, JPEG i kilka innych formatów eksportu, dając Ci elastyczność konwersji stron OneNote do potrzebnego formatu.

## Podsumowanie

W tym przewodniku pokazaliśmy, jak **zapisz OneNote jako PDF** stosując formatowanie tekstu bogatego przy użyciu Aspose.Note for. Postępując zgodnie z instrukcjami krok po kroku, możesz zautomatyzować tworzenie eleganckich dokumentów OneNote i konwertować je do PDF w dowolnym rozwiązaniu opartym na Javie.

---

**Ostatnia aktualizacja:** 2025-12-09  
**Testowano z:** Aspose.Note for Java 24.11 (najnowsza w momencie pisania)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}