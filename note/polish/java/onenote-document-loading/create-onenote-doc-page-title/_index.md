---
date: 2025-12-02
description: Dowiedz się, jak utworzyć stronę OneNote z tytułem w języku Java przy
  użyciu Aspose.Note for Java. Ten przewodnik pokazuje, jak ustawić tytuł strony OneNote
  i dostosować czcionkę tytułu.
linktitle: How to Create OneNote Page with Title - Java
second_title: Aspose.Note Java API
title: Jak utworzyć stronę OneNote z tytułem – Java
url: /pl/java/onenote-document-loading/create-onenote-doc-page-title/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak utworzyć stronę OneNote z tytułem - Java

## Wprowadzenie

Jeśli potrzebujesz **jak utworzyć stronę OneNote** programowo, Aspose.Note for Java ułatwia to. W tym samouczku dowiesz się, jak wygenerować plik OneNote, ustawić tytuł strony i nawet dostosować czcionkę tytułu — wszystko w kodzie Java. Po zakończeniu będziesz mieć gotowy dokument OneNote, który możesz zintegrować z dowolną aplikacją Java.

## Szybkie odpowiedzi
- **Jakiej biblioteki wymaga?** Aspose.Note for Java.
- **Czy mogę ustawić własną czcionkę dla tytułu?** Tak – użyj `ParagraphStyle`, aby określić nazwę czcionki, rozmiar i kolor.
- **Która wersja Javy jest obsługiwana?** Dowolny JDK 8+ (API jest kompatybilne wstecz).
- **Czy potrzebna jest licencja do rozwoju?** Darmowa wersja próbna działa do testów; licencja jest wymagana w produkcji.
- **Gdzie zapisywany jest wynik?** Ścieżkę definiujesz w zmiennej `dataDir`.

## Co to jest tytuł strony OneNote?
Tytuł strony OneNote to nagłówek wyświetlany u góry każdej strony. Zazwyczaj zawiera nazwę strony, datę utworzenia i godzinę. Ustawienie tego tytułu programowo pomaga tworzyć spójne, dobrze zorganizowane notatniki.

## Dlaczego ustawiać tytuł strony OneNote programowo?
- **Automatyzacja:** Generuj raporty lub notatki ze spotkań bez ręcznej edycji.  
- **Spójność:** Wymuszaj konwencję nazewnictwa we wszystkich stronach.  
- **Integracja:** Łącz OneNote z innymi systemami (np. CRM, narzędzia do zarządzania projektami).  

## Prerequisites

- **Java Development Kit (JDK)** – wersja 8 lub wyższa.  
- **Aspose.Note for Java** – pobierz ze strony oficjalnej **[tutaj](https://releases.aspose.com/note/java/)**.  
- **IDE** – IntelliJ IDEA, Eclipse lub NetBeans (według wyboru).

## Importowanie pakietów

Najpierw zaimportuj klasy, których będziemy potrzebować z biblioteki Aspose.Note.

```java
import com.aspose.note.*;
import java.awt.*;
import java.io.IOException;
import java.util.Calendar;
```

### Krok 1: Ustaw katalog dokumentu  
Określ, gdzie zostanie zapisany wygenerowany plik OneNote.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
```

### Krok 2: Utwórz obiekt Document  
Utwórz nowy `Document` – reprezentuje on plik OneNote, który będziesz budować.

```java
// Create an object of the Document class
Document doc = new Document();
```

### Krok 3: Zainicjuj obiekt Page  
Utwórz obiekt `Page`, który będzie zawierał tytuł i dowolną treść.

```java
// Initialize Page class object
Page page = new Page();
```

### Krok 4: Ustaw domyślny styl tekstu  
Zdefiniuj domyślny `ParagraphStyle`, który zostanie zastosowany do tekstu tytułu. To miejsce, w którym **dostosowujemy czcionkę tytułu OneNote**.

```java
// Default style for all text in the document.
ParagraphStyle textStyle = new ParagraphStyle()
                            .setFontColor(Color.BLACK)
                            .setFontName("Arial")
                            .setFontSize(10);
```

### Krok 5: Ustaw właściwości tytułu strony  
Tutaj **ustawiamy szczegóły tytułu strony OneNote** – tekst tytułu, datę i godzinę. Śmiało modyfikuj łańcuchy, aby dopasować je do swojego przypadku.

```java
// Set page title properties
Title title = new Title();

RichText titleText = new RichText().append("Title text.");
titleText.setParagraphStyle(textStyle);
title.setTitleText(titleText);

Calendar cal = Calendar.getInstance();
cal.set(2018, 04, 03);
RichText titleDate = new RichText().append(cal.getTime().toString());
titleDate.setParagraphStyle(textStyle);
title.setTitleDate(titleDate);

RichText titleTime = new RichText().append("12:34");
titleTime.setParagraphStyle(textStyle);
title.setTitleText(titleTime);
```

### Krok 6: Przypisz tytuł do strony  
Teraz **dodajemy tytuł do OneNote** łącząc obiekt `Title` ze `Page`.

```java
page.setTitle(title);
```

### Krok 7: Dodaj stronę do dokumentu  
Dodaj skonfigurowaną stronę do struktury dokumentu.

```java
doc.appendChildLast(page);
```

### Krok 8: Zapisz dokument OneNote  
Określ nazwę pliku wyjściowego i zapisz notatnik. To kończy proces **java create onenote file**.

```java
dataDir = dataDir + "load//CreateDocWithPageTitle_out.one";

// Save OneNote document
doc.save(dataDir);
```

## Częste problemy i wskazówki

| Issue | Solution |
|-------|----------|
| **Nieprawidłowa ścieżka pliku** | Upewnij się, że `dataDir` kończy się właściwym separatorem (`/` lub `\\`) i że folder istnieje. |
| **Tytuł niewidoczny** | Sprawdź, czy `ParagraphStyle` jest zastosowany do każdego elementu `RichText`. |
| **Wyjątek licencyjny** | Użyj licencji próbnej do testów; zastosuj pełną licencję przed wdrożeniem. |
| **Data wyświetla niewłaściwy miesiąc** | Miesiące w Javie są zerowo‑indeksowane; `cal.set(2018, 04, 03)` faktycznie ustawia maj. Dostosuj odpowiednio. |

## Najczęściej zadawane pytania

**Q:** Czy Aspose.Note for Java jest kompatybilny z różnymi wersjami Javy?  
**A:** Tak, biblioteka działa z Java 8 i nowszymi, zapewniając elastyczność w różnych środowiskach.

**Q:** Czy mogę dostosować styl i rozmiar czcionki tytułu strony?  
**A:** Oczywiście! Użyj `ParagraphStyle` (jak pokazano w Kroku 4), aby ustawić dowolną nazwę czcionki, rozmiar i kolor.

**Q:** Jak dodać więcej treści (np. akapity, obrazy) do strony?  
**A:** Utwórz dodatkowe obiekty `RichText` lub `Image`, ustaw ich style i dodaj je do `Page` za pomocą `page.appendChildLast(yourObject)`.

**Q:** Czy dostępna jest wersja próbna Aspose.Note for Java?  
**A:** Tak, możesz pobrać darmową wersję próbną ze strony Aspose, aby ocenić wszystkie funkcje.

**Q:** Gdzie mogę uzyskać wsparcie, jeśli napotkam problemy?  
**A:** Odwiedź [forum Aspose.Note](https://forum.aspose.com/c/note/28) w celu uzyskania pomocy od społeczności lub otwórz zgłoszenie wsparcia w Aspose.

---

**Last Updated:** 2025-12-02  
**Testowane z:** Aspose.Note for Java 24.12 (najnowsza w momencie pisania)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}