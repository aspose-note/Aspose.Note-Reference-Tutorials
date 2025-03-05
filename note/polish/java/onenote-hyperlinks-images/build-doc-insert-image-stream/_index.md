---
title: Utwórz dokument i wstaw obraz za pomocą strumienia w programie OneNote — Java
linktitle: Utwórz dokument i wstaw obraz za pomocą strumienia w programie OneNote — Java
second_title: Aspose.Note API Java
description: Dowiedz się, jak bez wysiłku integrować obrazy z dokumentami OneNote za pomocą Aspose.Note dla Java. Samouczek krok po kroku dla programistów Java.
type: docs
weight: 13
url: /pl/java/onenote-hyperlinks-images/build-doc-insert-image-stream/
---
## Wstęp

Witamy w naszym kompleksowym samouczku na temat używania Aspose.Note dla Java do tworzenia dokumentów i wstawiania obrazów przy użyciu strumieni obrazów w OneNote! W tym samouczku przeprowadzimy Cię przez proces krok po kroku, upewniając się, że dobrze rozumiesz każdy etap. Na koniec będziesz mógł bez wysiłku integrować obrazy z dokumentami programu OneNote przy użyciu języka Java.

## Warunki wstępne

Zanim przejdziemy do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:

### Zestaw programistyczny Java (JDK)

Upewnij się, że w systemie jest zainstalowany zestaw Java Development Kit (JDK). Można go pobrać ze strony internetowej Oracle.

### Aspose.Note dla biblioteki Java

 Pobierz i zainstaluj bibliotekę Aspose.Note dla Java z dostarczonego oprogramowania[połączyć](https://releases.aspose.com/note/java/).

### Konfiguracja IDE

Skonfiguruj zintegrowane środowisko programistyczne (IDE) za pomocą konfiguracji niezbędnych do pracy z projektami Java.

## Importuj pakiety

Aby rozpocząć, zaimportuj wymagane pakiety do projektu Java. Pakiety te zapewniają funkcjonalność niezbędną do pracy z dokumentami i obrazami programu OneNote.

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

## Krok 1: Skonfiguruj katalog dokumentów

 Zdefiniuj katalog, w którym znajdują się dokumenty i obrazy. Zastępować`"Your Document Directory"` ze ścieżką do swojego katalogu.

```java
String dataDir = "Your Document Directory";
```

## Krok 2: Utwórz obiekt dokumentu

 Zainicjuj instancję`Document` class, aby rozpocząć pracę z dokumentem programu OneNote.

```java
Document doc = new Document();
```

## Krok 3: Zainicjuj obiekt strony

 Stwórz`Page` obiekt reprezentujący stronę w dokumencie.

```java
Page page = new Page();
```

## Krok 4: Utwórz konspekt

 Zainicjuj`Outline` obiekt służący do strukturyzowania zawartości strony.

```java
Outline outline1 = new Outline();
outline1.setVerticalOffset(600);
outline1.setHorizontalOffset(0);
```

## Krok 5: Utwórz element konspektu

 Stworzyć`OutlineElement` aby przytrzymać obraz i określić jego położenie.

```java
OutlineElement outlineElem1 = new OutlineElement();
```

## Krok 6: Załaduj strumień obrazu

 Załaduj strumień obrazu za pomocą`FileInputStream` dla żądanego obrazu.

```java
InputStream fs = null;
try {
    fs = new FileInputStream(dataDir + "image.jpg");
} catch (FileNotFoundException e) {
    e.printStackTrace();
}
```

## Krok 7: Wstaw obraz

 Wstaw obraz do dokumentu, tworząc plik`Image` obiektu i ustawienie jego wyrównania.

```java
Image image = new Image(null, dataDir + "image1.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## Krok 8: Dołącz obraz do elementu konspektu

Dołącz obraz do elementu konturu.

```java
outlineElem1.appendChildLast(image);
```

## Krok 9: Dołącz element konspektu do konspektu

Dodaj element konturu do konturu.

```java
outline1.appendChildLast(outlineElem1);
```

## Krok 10: Dołącz konspekt do strony

Dodaj kontur do strony.

```java
page.appendChildLast(outline1);
```

## Krok 11: Dołącz stronę do dokumentu

Na koniec dołącz stronę do dokumentu.

```java
doc.appendChildLast(page);
```

## Krok 12: Zapisz dokument

Zapisz zmodyfikowany dokument, określając żądany format (np. PDF).

```java
try {
    doc.save("D://Aspose_JavaProjects//OneNote//out3.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

Wykonując te kroki, możesz bez wysiłku tworzyć dokumenty i wstawiać obrazy przy użyciu strumieni obrazów w OneNote przy użyciu Aspose.Note dla Java.

## Wniosek

Podsumowując, opanowanie integracji obrazów z dokumentami programu OneNote przy użyciu języka Java może znacząco usprawnić proces tworzenia dokumentów. Dzięki Aspose.Note dla Java masz do dyspozycji potężne narzędzie, które pozwala bezproblemowo wykonać to zadanie.

## Często zadawane pytania

### P1: Czy Aspose.Note dla Java jest kompatybilny ze wszystkimi wersjami OneNote?

O1: Aspose.Note dla Java obsługuje różne wersje OneNote, zapewniając kompatybilność w różnych środowiskach.

### P2: Czy mogę dostosować wygląd wstawionych obrazów w dokumentach OneNote przy użyciu Aspose.Note dla Java?

Odpowiedź 2: Tak, możesz dostosować różne aspekty wstawianych obrazów, takie jak wyrównanie, rozmiar i orientacja, aby spełnić Twoje specyficzne wymagania.

### P3: Czy Aspose.Note dla Java zapewnia obsługę innych formatów dokumentów oprócz PDF?

O3: Tak, Aspose.Note dla Java obsługuje szeroką gamę formatów dokumentów, w tym DOCX, HTML i inne, zapewniając elastyczność w zadaniach związanych z zarządzaniem dokumentami.

### P4: Gdzie mogę znaleźć dodatkowe zasoby i wsparcie dla Aspose.Note dla Java?

O4: Możesz uzyskać dostęp do dokumentacji, linków do pobrania, forów wsparcia i tymczasowych licencji dla Aspose.Note dla Java za pomocą podanych linków.

### P5: Czy dostępna jest wersja próbna Aspose.Note dla Java?

Odpowiedź 5: Tak, możesz uzyskać bezpłatną wersję próbną Aspose.Note dla Java, aby poznać jej funkcje i możliwości przed podjęciem decyzji o zakupie.
