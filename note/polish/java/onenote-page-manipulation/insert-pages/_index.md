---
date: 2026-01-10
description: Dowiedz się, jak programowo wstawiać strony do dokumentów OneNote przy
  użyciu Aspose.Note for Java. Ten przewodnik pokazuje, jak wstawiać strony, dostosowywać
  styl strony oraz zapisywać OneNote jako PDF lub obraz.
linktitle: Insert Pages in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Jak wstawiać strony w OneNote – Aspose.Note
url: /pl/java/onenote-page-manipulation/insert-pages/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wstawianie stron w OneNote - Aspose.Note

## Wprowadzenie

W tym samouczku nauczymy się **jak wstawiać strony** do dokumentu OneNote przy użyciu Aspose.Note dla Javy. Po zakończeniu przewodnika będziesz w stanie dodać strony do pliku OneNote, dostosować styl strony oraz wyeksportować wynik do formatu PDF lub różnych formatów obrazu.

## Szybkie odpowiedzi
- **Jaki jest główny cel?** Wstawianie nowych stron do dokumentu OneNote programowo.  
- **Która biblioteka jest wymagana?** Aspose.Note dla Javy.  
- **Czy wynik można zapisać jako PDF?** Tak – użyj `SaveFormat.Pdf`.  
- **Jak uzyskać obrazy z OneNote?** Zapisz dokument w formatach obrazu takich jak BMP, PNG lub JPEG, aby **przekształcić OneNote na obraz**.  
- **Czy potrzebna jest licencja?** Wymagana jest ważna licencja Aspose.Note do użytku produkcyjnego.

## Jak wstawiać strony do OneNote
Ta sekcja bezpośrednio odnosi się do głównego słowa kluczowego i prowadzi Cię przez cały proces **wstawiania stron** oraz **dodawania stron do dokumentu OneNote** z dostosowanym stylem.

## Wymagania wstępne

1. Zainstalowany Java Development Kit (JDK) w systemie.  
2. Pobraną bibliotekę Aspose.Note dla Javy. Możesz ją pobrać [tutaj](https://releases.aspose.com/note/java/).  
3. Zainstalowane zintegrowane środowisko programistyczne (IDE), takie jak IntelliJ IDEA lub Eclipse.

## Importowanie pakietów

Najpierw musisz zaimportować niezbędne pakiety w swoim pliku Java:

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

## Krok 1: Utwórz obiekt Document

Zainicjalizuj obiekt `Document`:

```java
Document doc = new Document();
```

## Krok 2: Zainicjalizuj obiekty Page

Zainicjalizuj obiekty `Page` i ustaw ich poziomy:

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## Krok 3: Dodaj węzły do stron

Dla każdej strony dodaj węzły z żądaną treścią. Tutaj również **dostosowujemy styl strony OneNote** ustawiając kolor czcionki, nazwę i rozmiar:

```java
// Adding nodes to first Page
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

// Repeat similar steps for other pages
```

## Krok 4: Dodaj strony do dokumentu

Dodaj utworzone strony do dokumentu OneNote:

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## Krok 5: Zapisz dokument

Zapisz dokument w wybranych formatach. To pokazuje zarówno możliwość **zapisania OneNote jako PDF**, jak i **konwersji OneNote na obraz**:

```java
String dataDir = "Your Document Directory";

doc.save(dataDir + "InsertPages_out.bmp" , SaveFormat.Bmp);
doc.save(dataDir + "InsertPages_out.pdf", SaveFormat.Pdf);
doc.save(dataDir + "InsertPages_out.gif", SaveFormat.Gif);
doc.save(dataDir + "InsertPages_out.jpeg", SaveFormat.Jpeg);
doc.save(dataDir + "InsertPages_out.png", SaveFormat.Png);
doc.save(dataDir + "InsertPages_out.tiff", SaveFormat.Tiff);

System.out.println("Files Saved Successfully!");
```

## Zakończenie

W tym samouczku nauczyliśmy się **jak wstawiać strony** do dokumentu OneNote przy użyciu Aspose.Note dla Javy. Postępując zgodnie z podanymi krokami, możesz efektywnie manipulować dokumentami OneNote programowo, **dostosowywać styl strony OneNote** oraz **zapisywać OneNote jako PDF** lub pliki graficzne do dalszego przetwarzania.

## FAQ

### Q1: Czy mogę wstawiać obrazy do dokumentu OneNote przy użyciu Aspose.Note dla Javy?

A1: Tak, możesz wstawiać obrazy, korzystając z odpowiednich klas i metod udostępnionych przez Aspose.Note.

### Q2: Czy Aspose.Note jest kompatybilny z różnymi wersjami OneNote?

A2: Aspose.Note zapewnia kompatybilność z różnymi wersjami OneNote, zapewniając płynną integrację i funkcjonalność.

### Q3: Jak mogę obsługiwać błędy lub wyjątki podczas pracy z Aspose.Note?

A3: Możesz wdrożyć techniki obsługi błędów, takie jak bloki try-catch, aby zarządzać wyjątkami w sposób elegancki i utrzymać stabilność aplikacji.

### Q4: Czy Aspose.Note wspiera rozwój wieloplatformowy?

A4: Tak, możesz tworzyć aplikacje przy użyciu Aspose.Note dla Javy na różnych platformach, w tym Windows, Linux i macOS.

### Q5: Czy mogę dostosować wygląd wstawionych stron w OneNote?

A5: Zdecydowanie, Aspose.Note oferuje rozbudowane opcje dostosowywania układów stron, stylów i treści, aby spełnić Twoje konkretne wymagania.

## Najczęściej zadawane pytania

**P: Jak mogę programowo dodać więcej niż trzy strony?**  
A: Utwórz dodatkowe obiekty `Page`, ustaw ich poziomy, dodaj treść i dołącz je do `Document` tak jak w powyższych przykładach.

**P: Czy mogę zmienić kolor tła strony OneNote?**  
A: Tak, użyj metody `Page.setBackgroundColor()` (lub równoważnej właściwości) przed dołączeniem strony do dokumentu.

**P: Czy można połączyć wiele plików OneNote w jeden?**  
A: Możesz wczytać każdy plik do osobnego obiektu `Document`, a następnie skopiować ich strony do jednego docelowego dokumentu.

**P: Jakiego formatu powinienem używać dla obrazów wysokiej rozdzielczości?**  
A: Zapis w formacie PNG lub TIFF (`SaveFormat.Png` / `SaveFormat.Tiff`) zachowuje najwyższą jakość przy eksportach graficznych.

**P: Czy Aspose.Note obsługuje zaszyfrowane pliki OneNote?**  
A: Tak, możesz podać hasło podczas wczytywania zaszyfrowanego pliku, używając odpowiedniego przeciążenia konstruktora `Document`.

**Ostatnia aktualizacja:** 2026-01-10  
**Testowano z:** Aspose.Note dla Javy 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}