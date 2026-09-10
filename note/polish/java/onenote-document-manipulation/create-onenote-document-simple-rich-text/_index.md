---
date: 2026-08-18
description: Dowiedz się, jak wyeksportować OneNote do PDF, ustawić formatowanie akapitu
  w Javie oraz zapisać OneNote jako PDF przy użyciu Aspose.Note dla Javy.
keywords:
- export onenote to pdf
- save onenote as pdf
- paragraph formatting java
- rich text formatting java
- aspose note java
lastmod: 2026-08-18
linktitle: Ustaw formatowanie akapitu podczas tworzenia dokumentu OneNote w Javie
og_description: Eksportuj OneNote do PDF i ustaw formatowanie akapitu w Javie przy
  użyciu Aspose.Note. Postępuj zgodnie z tym przewodnikiem krok po kroku, aby łatwo
  tworzyć dopracowane pliki PDF.
og_image_alt: Screenshot of Java code exporting OneNote to PDF with styled paragraphs
og_title: Eksportuj OneNote do PDF z formatowaniem akapitu w Javie (58 znaków)
schemas:
- author: Aspose
  dateModified: '2026-08-18'
  description: Learn how to export OneNote to PDF, set paragraph formatting in Java,
    and save OneNote as PDF using Aspose.Note for Java.
  headline: How to export OneNote to PDF with paragraph style in Java
  type: TechArticle
- description: Learn how to export OneNote to PDF, set paragraph formatting in Java,
    and save OneNote as PDF using Aspose.Note for Java.
  name: How to export OneNote to PDF with paragraph style in Java
  steps:
  - name: set document directory
    text: Define where the generated files will be saved. Replace `"Your Document
      Directory"` with an absolute or relative path on your machine.
  - name: initialize document object
    text: Create the root `Document` that represents the OneNote file. **Definition
      anchor:** `Document` is Aspose.Note’s top‑level object that holds one or more
      pages in memory.
  - name: initialize page object
    text: A OneNote file consists of one or more pages; we start with a single page.
      **Definition anchor:** `Page` represents a single OneNote page, containing outlines,
      images, and other elements.
  - name: initialize outline object
    text: Outlines act as containers for outline elements (think of them as sections).
      **Definition anchor:** `Outline` groups related `OutlineElement` objects and
      defines their visual hierarchy.
  - name: initialize outline element object
    text: Here we **add outline element** that will hold our rich text. **Definition
      anchor:** `OutlineElement` is a leaf node inside an `Outline` that can contain
      text, images, or other media.
  - name: set text style (set paragraph style)
    text: '`ParagraphStyle` defines the font family, size, color, and other typographic
      attributes for a paragraph. The `ParagraphStyle` instance defines the font,
      size, and color—this is where we **set paragraph style** for the upcoming text
      node.'
  - name: initialize rich text object
    text: '`RichText` is the node that stores styled text within an `OutlineElement`.
      We create a `RichText` node, insert a simple string, and attach the previously
      defined style.'
  - name: add rich text node to outline element
    text: Now the styled text lives inside the outline element.
  - name: add outline element node to outline
    text: The outline now contains the element that holds our paragraph.
  - name: add outline node to page
    text: We place the outline onto the page.
  type: HowTo
- questions:
  - answer: Yes, the API supports tables, images, hyperlinks, and advanced layout
      features in addition to plain text.
    question: Can Aspose.Note handle complex formatting such as tables or images?
  - answer: Direct conversion isn’t provided, but you can extract PDF content and
      rebuild a OneNote document using the API.
    question: Is it possible to convert a OneNote PDF back to a OneNote file?
  - answer: Absolutely. Aspose.Note for Java is platform‑independent; just ensure
      a compatible JDK is installed.
    question: Does the library work on Linux/macOS environments?
  - answer: Create additional `Page` and `Outline` objects, then append them to the
      `Document` just like the single‑page example.
    question: How do I add multiple pages or outlines?
  - answer: The official Aspose.Note documentation and the [support forum](https://forum.aspose.com/c/note/28)
      contain many code samples and real‑world scenarios.
    question: Where can I find more examples?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- export onenote
- aspose.note
- java document processing
title: Jak wyeksportować OneNote do PDF z formatowaniem akapitu w Javie
url: /pl/java/onenote-document-manipulation/create-onenote-document-simple-rich-text/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ustaw styl akapitu podczas tworzenia dokumentu OneNote w Javie

## Wprowadzenie

Programowe eksportowanie OneNote do PDF jest powszechnym wymaganiem dla silników raportujących, usług automatycznego notowania oraz potoków konwersji dokumentów. W tym samouczku nauczysz się, jak **eksportować OneNote do PDF**, zastosować niestandardowe formatowanie akapitu i zapisać plik OneNote — wszystko przy użyciu Aspose.Note dla Javy. Po zakończeniu będziesz mieć gotowy fragment kodu Java, który generuje elegancki PDF o dokładnie określonym wyglądzie.

## Szybkie odpowiedzi
- **Co oznacza „set paragraph style”?** Stosuje czcionkę, rozmiar, kolor i inne atrybuty formatowania do akapitu tekstu.  
- **Czy mogę wyeksportować wynik do PDF?** Tak – przewodnik kończy się zapisem pliku OneNote jako PDF.  
- **Czy potrzebuję licencji na Aspose.Note?** Darmowa wersja próbna działa w celach oceny; licencja komercyjna jest wymagana do użytku produkcyjnego.  
- **Jakie IDE są obsługiwane?** Dowolne IDE Java – Eclipse, IntelliJ IDEA, NetBeans itp.  
- **Jak długo trwa implementacja?** Około 10‑15 minut dla podstawowego dokumentu.

## Jak wyeksportować OneNote do PDF w Javie?

`Document` reprezentuje plik OneNote zawierający strony, konspekty i inne elementy. Załaduj swój dokument OneNote przy pomocy `new Document()` (lub utwórz nowy) i wywołaj `document.save("output.pdf", SaveFormat.Pdf)`. Aspose.Note zapisuje PDF w jednym przebiegu, zachowując style, obrazy i konspekty bez potrzeby instalacji Microsoft OneNote. To bezpośrednie podejście działa na Windows, Linux i macOS z dowolnym JDK 1.8+.

## Co to jest „set paragraph style” w Aspose.Note?

`ParagraphStyle` jest klasą, która przechowuje nazwę czcionki, rozmiar, kolor, wyrównanie i inne ustawienia typograficzne dla akapitu. Dołączając instancję `ParagraphStyle` do węzła `RichText`, kontrolujesz dokładnie, jak ten akapit będzie wyglądał na końcowej stronie OneNote i w wyeksportowanym PDF.

## Dlaczego eksportować OneNote do PDF?

Eksportowanie OneNote do PDF zapewnia spójną identyfikację wizualną poprzez zachowanie firmowych czcionek i kolorów, poprawia czytelność dzięki utrzymaniu dokładnego układu przy drukowaniu lub archiwizacji oraz zapewnia dostęp wieloplatformowy, dzięki czemu odbiorcy mogą przeglądać dokument na dowolnym urządzeniu bez potrzeby posiadania OneNote. Dodatkowo oferuje korzyści wydajnościowe, umożliwiając szybkie przetwarzanie dużych dokumentów.

## Wymagania wstępne

1. **Java Development Kit (JDK) 1.8+** – dowolny aktualny JDK będzie działał.  
2. **Aspose.Note for Java** – pobierz najnowszy JAR ze [Strony pobierania Aspose.Note](https://releases.aspose.com/note/java/).  
3. **IDE** (Eclipse, IntelliJ IDEA lub NetBeans) do kompilacji i uruchamiania przykładu.  

> **Wskazówka:** Dodaj plik JAR Aspose.Note do ścieżki klas projektu za pomocą Maven (`<dependency>`) lub ręcznie odwołując się do JAR w IDE.

## Importuj pakiety

Najpierw zaimportuj wymagane przestrzenie nazw. Ten blok pozostaje niezmieniony.

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

> Klasa `ParagraphStyle` jest kluczem do **set paragraph style** później w samouczku.

## Przewodnik krok po kroku

Poniżej znajduje się zwięzły opis każdej operacji. Bloki kodu są dokładnie takie, jak w oryginalnym przykładzie; dodajemy jedynie tekst wyjaśniający.

### Krok 1: ustaw katalog dokumentu
Zdefiniuj, gdzie zostaną zapisane wygenerowane pliki.

```java
String dataDir = "Your Document Directory";
```

Zastąp `"Your Document Directory"` ścieżką bezwzględną lub względną na swoim komputerze.

### Krok 2: zainicjalizuj obiekt dokumentu
Utwórz główny obiekt `Document`, który reprezentuje plik OneNote.

```java
Document doc = new Document();
```

**Definicja:** `Document` jest obiektem najwyższego poziomu w Aspose.Note, który przechowuje jedną lub więcej stron w pamięci.

### Krok 3: zainicjalizuj obiekt strony
Plik OneNote składa się z jednej lub więcej stron; zaczynamy od jednej strony.

```java
Page page = new Page();
```

**Definicja:** `Page` reprezentuje pojedynczą stronę OneNote, zawierającą konspekty, obrazy i inne elementy.

### Krok 4: zainicjalizuj obiekt konspektu
Konspekty działają jako kontenery dla elementów konspektu (pomyśl o nich jako o sekcjach).

```java
Outline outline = new Outline();
```

**Definicja:** `Outline` grupuje powiązane obiekty `OutlineElement` i definiuje ich hierarchię wizualną.

### Krok 5: zainicjalizuj obiekt elementu konspektu
Tutaj **add outline element**, który będzie przechowywał nasz tekst sformatowany.

```java
OutlineElement outlineElem = new OutlineElement();
```

**Definicja:** `OutlineElement` jest węzłem liścia wewnątrz `Outline`, który może zawierać tekst, obrazy lub inne media.

### Krok 6: ustaw styl tekstu (set paragraph style)

`ParagraphStyle` definiuje rodzinę czcionki, rozmiar, kolor i inne atrybuty typograficzne dla akapitu.

```java
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```

Instancja `ParagraphStyle` określa czcionkę, rozmiar i kolor — to miejsce, w którym **set paragraph style** jest stosowany do nadchodzącego węzła tekstowego.

### Krok 7: zainicjalizuj obiekt RichText

`RichText` jest węzłem, który przechowuje stylowany tekst w obrębie `OutlineElement`.

```java
RichText text = new RichText().append("Hello OneNote text!");
text.setParagraphStyle(textStyle);
```

Tworzymy węzeł `RichText`, wstawiamy prosty ciąg znaków i dołączamy wcześniej zdefiniowany styl.

### Krok 8: dodaj węzeł RichText do elementu konspektu

```java
outlineElem.appendChildLast(text);
```

Teraz stylowany tekst znajduje się wewnątrz elementu konspektu.

### Krok 9: dodaj węzeł elementu konspektu do konspektu

```java
outline.appendChildLast(outlineElem);
```

Konspekt teraz zawiera element, który przechowuje nasz akapit.

### Krok 10: dodaj węzeł konspektu do strony

```java
page.appendChildLast(outline);
```

Umieszczamy konspekt na stronie.

### Krok 11: dodaj węzeł strony do dokumentu

```java
doc.appendChildLast(page);
```

Dokument ma teraz jedną stronę ze stylowanym tekstem.

### Krok 12: zapisz dokument (eksportuj OneNote do PDF)

```java
doc.save(dataDir + "CreateOneNoteDocumentWithSimpleRichText_out.pdf", SaveFormat.Pdf);
```

Metoda `save` zapisuje plik OneNote i **exports OneNote to PDF** w jednym kroku. Możesz także zapisać jako `.one`, używając `SaveFormat.One`, jeśli potrzebny jest format natywny.

## Typowe problemy i rozwiązania

| Problem | Powód | Rozwiązanie |
|-------|--------|-----|
| **Plik nie znaleziony** | `dataDir` wskazuje na nieistniejący folder. | Upewnij się, że katalog istnieje lub utwórz go programowo (`new File(dataDir).mkdirs();`). |
| **Pusty PDF** | Nie dodano żadnej treści przed zapisem. | Sprawdź, czy węzeł `RichText` został dołączony i styl został ustawiony. |
| **Nieobsługiwana czcionka** | Nazwa czcionki nie jest zainstalowana w systemie. | Użyj popularnej czcionki, takiej jak "Arial", lub osadź czcionkę w projekcie. |

## Najczęściej zadawane pytania

**Q: Czy Aspose.Note obsługuje złożone formatowanie, takie jak tabele lub obrazy?**  
A: Tak, API obsługuje tabele, obrazy, hiperłącza i zaawansowane funkcje układu oprócz zwykłego tekstu.

**Q: Czy można przekonwertować PDF OneNote z powrotem na plik OneNote?**  
A: Bezpośrednia konwersja nie jest dostępna, ale możesz wyodrębnić zawartość PDF i odtworzyć dokument OneNote przy użyciu API.

**Q: Czy biblioteka działa w środowiskach Linux/macOS?**  
A: Absolutnie. Aspose.Note for Java jest niezależny od platformy; wystarczy zapewnić kompatybilny JDK.

**Q: Jak dodać wiele stron lub konspektów?**  
A: Utwórz dodatkowe obiekty `Page` i `Outline`, a następnie dołącz je do `Document` tak samo, jak w przykładzie jednosktronicowym.

**Q: Gdzie mogę znaleźć więcej przykładów?**  
A: Oficjalna dokumentacja Aspose.Note oraz [forum wsparcia](https://forum.aspose.com/c/note/28) zawierają liczne przykłady kodu i scenariusze z życia wzięte.

## Podsumowanie

Widzisz już, jak **set paragraph style**, **add outline element** i **export OneNote to PDF** przy użyciu Aspose.Note dla Javy. Wczesne zastosowanie stylowanego tekstu zapewnia profesjonalny wygląd końcowego PDF, a jednorazowe wywołanie `save` efektywnie obsługuje konwersję. Rozbuduj tę bazę o obrazy, tabele lub własne metadane, aby spełnić specyficzne potrzeby swojej aplikacji.

---

**Ostatnia aktualizacja:** 2026-08-18  
**Testowano z:** Aspose.Note for Java 26.5 (najnowsze wydanie)  
**Autor:** Aspose

## Powiązane samouczki

- [Jak zapisać OneNote jako PDF przy użyciu Aspose.Note dla Javy](/note/java/onenote-document-loading/load-save-format/)
- [Naucz się konwertować OneNote do PDF przy użyciu Aspose.Note i PdfSaveOptions](/note/java/onenote-document-loading/load-pdf-save-options/)
- [Ustaw domyślny styl akapitu w OneNote - Aspose.Note](/note/java/onenote-styles/set-default-paragraph-style/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}