---
date: 2025-12-21
description: Dowiedz się, jak tworzyć dokumenty OneNote w Javie i bez wysiłku wstawiać
  obrazy przy użyciu Aspose.Note dla Javy. Przewodnik krok po kroku dla programistów
  Java.
linktitle: How to create onenote document java – Build Doc and Insert Image with Stream
second_title: Aspose.Note Java API
title: Jak utworzyć dokument OneNote w Javie – budowanie dokumentu i wstawianie obrazu
  przy użyciu strumienia
url: /pl/java/onenote-hyperlinks-images/build-doc-insert-image-stream/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak utworzyć dokument OneNote w Java – Budowanie dokumentu i wstawianie obrazu za pomocą strumienia

## Wprowadzenie

Witamy! W tym samouczku **utworzysz dokument OneNote w Java** od podstaw i nauczysz się wstawiać obrazy przy użyciu strumienia obrazu. Przejdziemy przez każdy krok, wyjaśnimy, dlaczego każdy element ma znaczenie, i podamy praktyczne wskazówki, abyś mógł zastosować tę technikę w rzeczywistych projektach. Po zakończeniu będziesz w stanie programowo generować strony OneNote i osadzać obrazy dokładnie tam, gdzie ich potrzebujesz.

## Szybkie odpowiedzi
- **Jakiej biblioteki potrzebuję?** Aspose.Note for Java  
- **Czy mogę wstawiać obrazy ze strumienia?** Tak – wystarczy przekazać `InputStream` do konstruktora `Image`.  
- **Do jakiego formatu mogę eksportować?** Każdy format obsługiwany przez Aspose.Note, np. PDF, DOCX, HTML.  
- **Czy potrzebuję licencji do rozwoju?** Darmowa licencja tymczasowa działa w trybie ewaluacji; pełna licencja jest wymagana w produkcji.  
- **Jaka wersja Java jest wymagana?** Java 8 lub wyższa.

## Co to jest „utworzyć dokument OneNote w Java”?

Tworzenie dokumentu OneNote w Java oznacza użycie API Aspose.Note do programowego budowania struktury notatnika — stron, konturów i elementów — bez otwierania aplikacji OneNote na komputerze. Takie podejście jest idealne do automatycznego generowania raportów, przetwarzania partii notatek lub integrowania treści OneNote w większych aplikacjach Java.

## Dlaczego używać Aspose.Note for Java do tworzenia dokumentu OneNote w Java?

- **Pełna kontrola** nad układem strony, pozycjonowaniem konturów i stylizacją elementów.  
- **Brak interfejsu COM** – działa na każdym systemie operacyjnym obsługującym Java.  
- **Bogate opcje eksportu** – konwertuj ten sam dokument do PDF, DOCX, HTML itp. jednym wywołaniem.  
- **Przyjazny dla strumieni** – możesz ładować obrazy bezpośrednio z pamięci, sieci lub przechowywania w chmurze.

## Wymagania wstępne

Zanim zaczniemy, upewnij się, że masz przygotowane następujące elementy:

### Java Development Kit (JDK)

Najnowszy JDK (8 lub nowszy) zainstalowany na Twoim komputerze.

### Biblioteka Aspose.Note for Java

Pobierz bibliotekę ze strony oficjalnej wersji Aspose: [https://releases.aspose.com/note/java/](https://releases.aspose.com/note/java/).

### Konfiguracja IDE

Skonfiguruj swoje ulubione IDE (IntelliJ IDEA, Eclipse, VS Code), aby uwzględniało pliki JAR Aspose.Note w ścieżce klas projektu.

## Importowanie pakietów

Na początek zaimportuj wymagane klasy Java i Aspose.Note. Te importy dają dostęp do tworzenia dokumentów, obsługi stron, zarządzania konturami i wstawiania obrazów.

```java
import java.io.FileInputStream;
import java.io.FileNotFoundException;
import java.io.IOException;
import java.io.InputStream;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## Krok 1: Ustaw katalog dokumentu

Zdefiniuj folder zawierający obrazy źródłowe oraz miejsce, w którym zostanie zapisany plik wyjściowy. Zamień symbol zastępczy na rzeczywistą ścieżkę na swoim komputerze.

```java
String dataDir = "Your Document Directory";
```

## Krok 2: Utwórz obiekt Document

Utwórz nowy obiekt `Document`. Ten obiekt reprezentuje notatnik OneNote, który budujesz.

```java
Document doc = new Document();
```

## Krok 3: Zainicjuj obiekt Page

Utwórz `Page`, który będzie zawierał wszystkie kontury i elementy dla tej strony notatnika.

```java
Page page = new Page();
```

## Krok 4: Utwórz Outline

`Outline` działa jak kontener dla rozmieszczonych elementów. Tutaj ustawiamy pionowe i poziome przesunięcia, aby umieścić kontur na stronie.

```java
Outline outline1 = new Outline();
outline1.setVerticalOffset(600);
outline1.setHorizontalOffset(0);
```

## Krok 5: Utwórz Outline Element

`OutlineElement` będzie zawierał obraz, który zamierzamy wstawić.

```java
OutlineElement outlineElem1 = new OutlineElement();
```

## Krok 6: Załaduj strumień obrazu

Otwórz plik obrazu jako strumień. Użycie strumienia pozwala odczytać obraz z dowolnego źródła (system plików, sieć, baza danych) bez konieczności wcześniejszego zapisywania go na dysku.

```java
InputStream fs = null;
try {
    fs = new FileInputStream(dataDir + "image.jpg");
} catch (FileNotFoundException e) {
    e.printStackTrace();
}
```

## Krok 7: Wstaw obraz

Utwórz obiekt `Image`. Pierwszy argument może być `null`, gdy później podasz strumień, ale dla uproszczenia odwołujemy się tutaj do ścieżki pliku i ustawiamy wyrównanie po prawej stronie strony.

```java
Image image = new Image(null, dataDir + "image1.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## Krok 8: Dodaj obraz do Outline Element

Dodaj obraz do elementu konturu, aby stał się częścią wizualnej hierarchii strony.

```java
outlineElem1.appendChildLast(image);
```

## Krok 9: Dodaj Outline Element do Outline

Teraz dołącz element konturu (zawierający obraz) do kontenera Outline.

```java
outline1.appendChildLast(outlineElem1);
```

## Krok 10: Dodaj Outline do Page

Umieść kontur na stronie.

```java
page.appendChildLast(outline1);
```

## Krok 11: Dodaj Page do Document

Dodaj w pełni zbudowaną stronę do obiektu dokumentu.

```java
doc.appendChildLast(page);
```

## Krok 12: Zapisz dokument

Na koniec zapisz dokument OneNote w potrzebnym formacie. W tym przykładzie eksportujemy do PDF, ale możesz wybrać dowolny format obsługiwany przez Aspose.Note.

```java
try {
    doc.save("D://Aspose_JavaProjects//OneNote//out3.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

Postępując zgodnie z tymi krokami, pomyślnie **utworzyłeś dokument OneNote w Java** i osadziłeś obraz przy użyciu strumienia wejściowego.

## Typowe pułapki i wskazówki

- **Strumień nie został zamknięty** – W środowisku produkcyjnym zawsze zamykaj `InputStream` w bloku `finally` lub używaj try‑with‑resources.  
- **Nieprawidłowa ścieżka pliku** – Sprawdź dwukrotnie, czy `dataDir` kończy się odpowiednim separatorem (`/` lub `\`).  
- **Wyrównanie obrazu** – Jeśli obraz pojawia się poza ekranem, dostosuj wartości `VerticalOffset`/`HorizontalOffset` konturu.  
- **Wyjątki licencyjne** – Korzystanie z wersji ewaluacyjnej może dodać znak wodny do wyniku; zastosuj ważną licencję, aby go usunąć.

## Najczęściej zadawane pytania

### Q1: Czy Aspose.Note for Java jest kompatybilny ze wszystkimi wersjami OneNote?

A1: Aspose.Note for Java obsługuje różne formaty plików OneNote, zapewniając kompatybilność z wersjami desktop, online i mobilnymi.

### Q2: Czy mogę dostosować wygląd wstawianych obrazów w dokumentach OneNote przy użyciu Aspose.Note for Java?

A2: Tak, możesz modyfikować wyrównanie, rozmiar, obrót, a nawet przycinać obraz, używając odpowiednich właściwości obiektu `Image`.

### Q3: Czy Aspose.Note for Java zapewnia obsługę innych formatów dokumentów poza PDF?

A3: Zdecydowanie. API może eksportować do DOCX, HTML, XPS i kilku innych formatów, dając elastyczność w udostępnianiu lub archiwizacji notatek.

### Q4: Gdzie mogę znaleźć dodatkowe zasoby i wsparcie dla Aspose.Note for Java?

A4: Oficjalna strona Aspose oferuje obszerną dokumentację, przykłady kodu, fora oraz tymczasowe licencje do ewaluacji.

### Q5: Czy dostępna jest wersja próbna Aspose.Note for Java?

A5: Tak, możesz pobrać darmową wersję próbną ze strony wydania Aspose, aby przetestować wszystkie funkcje przed zakupem.

---

**Ostatnia aktualizacja:** 2025-12-21  
**Testowano z:** Aspose.Note for Java 24.12 (najnowsza w momencie pisania)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}