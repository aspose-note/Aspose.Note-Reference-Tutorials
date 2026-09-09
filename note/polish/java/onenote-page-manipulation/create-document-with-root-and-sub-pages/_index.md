---
description: Dowiedz się, jak zapisać plik PDF z OneNote i dodać podstrony w OneNote
  przy użyciu Aspose.Note dla Javy. Postępuj zgodnie z tym przewodnikiem krok po kroku,
  aby efektywnie organizować swoje notatki.
linktitle: How to Save OneNote PDF and Add Sub Pages
second_title: Aspose.Note Java API
title: Jak zapisać PDF z OneNote i dodać podstrony
url: /pl/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak zapisać OneNote PDF i dodać podstrony

## Wprowadzenie

W tym samouczku dowiesz się **jak zapisać OneNote PDF**, tworząc dokument zawierający zarówno strony główne, jak i podstrony przy użyciu Aspose.Note for Java. Organizowanie notatników OneNote w przejrzystej hierarchii ułatwia nawigację, a możliwość eksportu do PDF zapewnia udostępnianie notatek w uniwersalnym formacie. Pokażemy również, jak **dodać podstrony w stylu onenote**, aby z łatwością budować struktury wielopoziomowe.

## Szybkie odpowiedzi
- **Co oznacza główne słowo kluczowe?** Odnosi się do eksportowania notatnika OneNote do PDF przy użyciu Aspose.Note.  
- **Jakie API jest używane?** Aspose.Note for Java.  
- **Czy mogę tworzyć hierarchiczne strony?** Tak – ustaw poziom strony, aby zbudować strony główne i podstrony.  
- **Czy potrzebna jest licencja?** Dostępna jest bezpłatna wersja próbna; licencja komercyjna jest wymagana w produkcji.  
- **Jakie formaty wyjściowe są obsługiwane?** BMP, PDF, PNG i inne.

## Co to jest „jak zapisać OneNote PDF”?
Zapisywanie OneNote jako PDF konwertuje strony notatnika na dokument o stałym układzie, zachowujący formatowanie, obrazy i hierarchię. Jest to idealne rozwiązanie do udostępniania, archiwizacji lub drukowania notatek.

## Dlaczego dodawać podstrony w OneNote?
Dodawanie podstron pozwala grupować powiązane treści pod stroną nadrzędną, odzwierciedlając strukturę podobną do folderów. Poprawia organizację notatek, przyspiesza wyszukiwanie i zwiększa komfort czytania po wyeksportowaniu notatnika do PDF.

## Wymagania wstępne

Zanim rozpoczniesz, upewnij się, że masz następujące elementy:

1. Java Development Kit (JDK): Upewnij się, że masz zainstalowany JDK w systemie.  
2. Aspose.Note for Java: Pobierz i zainstaluj Aspose.Note for Java ze [strony internetowej](https://purchase.aspose.com/buy).  
3. Zintegrowane środowisko programistyczne (IDE): Wybierz IDE Java, takie jak IntelliJ IDEA, Eclipse lub NetBeans.

## Importowanie pakietów

Rozpocznij od zaimportowania niezbędnych pakietów w swoim projekcie Java:

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

## Krok 1: Ustaw katalog dokumentu

Zdefiniuj katalog, w którym chcesz zapisać dokument OneNote:

```java
String dataDir = "Your Document Directory";
```

## Krok 2: Utwórz obiekt Document

Utwórz instancję obiektu `Document`:

```java
Document doc = new Document();
```

## Krok 3: Utwórz strony

Zainicjuj obiekty stron i ustaw ich poziomy. Ustawienie poziomu określa, czy strona jest stroną główną, czy podstroną:

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## Krok 4: Dodaj węzły do stron

### Dodawanie węzłów do pierwszej strony

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text = new RichText().append("First page.");
text.setParagraphStyle(textStyle);

outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page1.appendChildLast(outline);
```

### Dodawanie węzłów do drugiej strony

```java
Outline outline2 = new Outline();
OutlineElement outlineElem2 = new OutlineElement();
ParagraphStyle textStyle2 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text2 = new RichText().append("Second page.");
text2.setParagraphStyle(textStyle2);

outlineElem2.appendChildLast(text2);
outline2.appendChildLast(outlineElem2);
page2.appendChildLast(outline2);
```

### Dodawanie węzłów do trzeciej strony

```java
Outline outline3 = new Outline();
OutlineElement outlineElem3 = new OutlineElement();
ParagraphStyle textStyle3 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Broadway")
                                    .setFontSize(10);

RichText text3 = new RichText().append("Third page.");
text3.setParagraphStyle(textStyle3);

outlineElem3.appendChildLast(text3);
outline3.appendChildLast(outlineElem3);
page3.appendChildLast(outline3);
```

## Krok 5: Dodaj strony do dokumentu

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## Krok 6: Zapisz dokument

Zapisz dokument OneNote jako PDF (lub BMP w tym przykładzie). Zmiana `SaveFormat` umożliwia eksport do PDF, co spełnia wymaganie „jak zapisać OneNote PDF”:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Handle exception
}
```

> **Wskazówka:** Aby wyeksportować bezpośrednio do PDF, zamień `SaveFormat.Bmp` na `SaveFormat.Pdf`.

Gratulacje! Pomyślnie utworzyłeś dokument OneNote z stronami głównymi i podstronami oraz nauczyłeś się **jak zapisać OneNote PDF** przy użyciu Aspose.Note for Java.

## Dlaczego to ma znaczenie

- **Hierarchiczna organizacja:** Strony główne i podstrony pozwalają na odzwierciedlenie struktury folderów w OneNote.  
- **Bezproblemowy eksport do PDF:** Po zorganizowaniu, eksport do PDF zachowuje hierarchię, co sprawia, że końcowy dokument jest łatwy do czytania i udostępniania.  
- **Automatyzacja:** Kod może być zintegrowany z większymi aplikacjami Java, umożliwiając masową kreację strukturalnych notatników.

## Typowe pułapki i jak ich unikać

| Problem | Przyczyna | Rozwiązanie |
|-------|-------|----------|
| Strony pojawiają się na tym samym poziomie | Nieprawidłowa wartość `setLevel` | Użyj `setLevel((byte) 1)` dla stron głównych i `setLevel((byte) 2)` (lub wyższego) dla podstron. |
| Wyjście PDF jest puste | Brak `SaveFormat.Pdf` lub nieprawidłowa ścieżka pliku | Sprawdź, czy katalog istnieje i użyj `SaveFormat.Pdf`. |
| Czcionka nie została zastosowana | Nieprawidłowa nazwa czcionki lub brak czcionki w systemie | Upewnij się, że czcionka (np. „David Transparent”) jest zainstalowana na komputerze uruchamiającym kod. |

## Najczęściej zadawane pytania

**Q: Czy mogę tworzyć wiele poziomów podstron przy użyciu Aspose.Note for Java?**  
A: Tak, możesz tworzyć głębsze hierarchie, ustawiając wyższe numery poziomów (np. `setLevel((byte) 3)` dla podstrony trzeciego poziomu).

**Q: Czy Aspose.Note for Java jest kompatybilny z różnymi IDE Java?**  
A: Absolutnie. Działa z IntelliJ IDEA, Eclipse, NetBeans i każdym innym IDE obsługującym rozwój w Javie.

**Q: Czy mogę dostosować formatowanie tekstu w moim dokumencie OneNote?**  
A: Tak. Użyj `ParagraphStyle`, aby ustawić nazwę czcionki, rozmiar, kolor i inne atrybuty dla każdego elementu `RichText`.

**Q: Czy Aspose.Note for Java obsługuje zapisywanie dokumentów w formatach innych niż BMP?**  
A: Tak. Obsługiwane formaty to m.in. PDF, PNG, JPEG, DOCX i inne. Zmieniaj odpowiednio wartość enum `SaveFormat`.

**Q: Czy dostępna jest wersja próbna Aspose.Note for Java?**  
A: Tak, możesz pobrać bezpłatną wersję próbną ze strony Aspose.

## Podsumowanie

Organizowanie notatników OneNote w przejrzystej strukturze hierarchicznej oraz ich eksport jako PDF sprawia, że notatki są bardziej dostępne i łatwiejsze do udostępniania. Postępując zgodnie z powyższymi krokami, teraz wiesz **jak zapisać OneNote PDF** oraz **dodać podstrony w stylu onenote** programowo przy użyciu Aspose.Note for Java.

**Ostatnia aktualizacja:** 2026-01-07  
**Testowano z:** Aspose.Note for Java 24.11 (latest)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}