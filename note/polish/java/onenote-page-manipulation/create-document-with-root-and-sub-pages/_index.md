---
title: Utwórz dokument ze stronami głównymi i podrzędnymi w programie OneNote
linktitle: Utwórz dokument ze stronami głównymi i podrzędnymi w programie OneNote
second_title: Aspose.Note API Java
description: Utwórz dokument ze stronami głównymi i podrzędnymi w OneNote, używając Aspose.Note dla Java. Postępuj zgodnie z przewodnikiem krok po kroku, aby sprawnie organizować notatki.
type: docs
weight: 11
url: /pl/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
---
## Wstęp

W tym samouczku przeprowadzimy Cię przez proces tworzenia dokumentu ze stronami głównymi i podstronami w OneNote przy użyciu Aspose.Note dla Java. Wykonując poniższe kroki, będziesz w stanie efektywnie organizować dokumenty programu OneNote w oparciu o strukturę hierarchiczną.

## Warunki wstępne

Zanim zaczniesz, upewnij się, że masz następujące wymagania wstępne:

1. Zestaw Java Development Kit (JDK): Upewnij się, że w systemie jest zainstalowany pakiet JDK.
2. Aspose.Note dla Java: Pobierz i zainstaluj Aspose.Note dla Java z[strona internetowa](https://purchase.aspose.com/buy).
3. Zintegrowane środowisko programistyczne (IDE): wybierz środowisko Java IDE, takie jak IntelliJ IDEA, Eclipse lub NetBeans.

## Importuj pakiety

Zacznij od zaimportowania niezbędnych pakietów do projektu Java:

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

## Krok 1: Skonfiguruj katalog dokumentów

Zdefiniuj katalog, w którym chcesz zapisać dokument OneNote:

```java
String dataDir = "Your Document Directory";
```

## Krok 2: Utwórz obiekt dokumentu

 Utwórz instancję a`Document` obiekt:

```java
Document doc = new Document();
```

## Krok 3: Utwórz strony

Zainicjuj obiekty strony i ustaw ich poziomy:

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

### Dodawanie węzłów do strony trzeciej

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

Zapisz dokument OneNote:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Obsłuż wyjątek
}
```

Gratulacje! Pomyślnie utworzyłeś dokument ze stronami głównymi i podrzędnymi w OneNote przy użyciu Aspose.Note dla Java.

## Wniosek

Organizowanie dokumentów programu OneNote w sposób hierarchiczny jest niezbędne do lepszego zarządzania i nawigacji. Dzięki Aspose.Note dla Java możesz efektywnie tworzyć dokumenty ze stronami głównymi i podstronami, zapewniając przejrzysty i zorganizowany układ notatek.

## Często zadawane pytania

### P1: Czy mogę utworzyć wiele poziomów podstron za pomocą Aspose.Note dla Java?

Odpowiedź 1: Tak, możesz utworzyć wiele poziomów podstron, ustawiając odpowiedni poziom dla każdej strony.

### P2: Czy Aspose.Note dla Java jest kompatybilny z różnymi środowiskami IDE Java?

O2: Tak, Aspose.Note dla Java jest kompatybilny z popularnymi środowiskami IDE Java, takimi jak IntelliJ IDEA, Eclipse i NetBeans.

### Pyt. 3: Czy mogę dostosować formatowanie tekstu w dokumencie programu OneNote?

O3: Tak, możesz dostosować czcionkę, kolor, rozmiar i inne opcje formatowania za pomocą Aspose.Note dla funkcji tekstu sformatowanego Java.

### P4: Czy Aspose.Note dla Java obsługuje zapisywanie dokumentów w różnych formatach?

O4: Tak, Aspose.Note dla Java obsługuje zapisywanie dokumentów w różnych formatach, w tym BMP, PDF, PNG i innych.

### P5: Czy dostępna jest wersja próbna Aspose.Note dla Java?

O5: Tak, możesz pobrać bezpłatną wersję próbną Aspose.Note dla Java ze strony internetowej.