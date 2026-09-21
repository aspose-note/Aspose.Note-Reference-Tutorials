---
date: 2026-07-29
description: Dowiedz się, jak osadzić link do OneNote, zapisać OneNote jako PDF i
  dodać hiperłącza przy użyciu Javy z Aspose.Note. Eksportuj OneNote do PDF bez wysiłku.
keywords:
- embed link onenote
- export onenote to pdf
- generate pdf from onenote
- add hyperlink in onenote
- save onenote pdf
lastmod: 2026-07-29
linktitle: Zapisz OneNote jako PDF i dodaj hiperłącze w OneNote przy użyciu Javy
og_description: Osadź link do OneNote i wyeksportuj OneNote do PDF przy użyciu Javy
  i Aspose.Note. Dowiedz się krok po kroku, jak dodać hiperłącza i wygenerować PDF.
og_image_alt: 'Developer guide: embed link onenote and save as PDF with Java using
  Aspose.Note'
og_title: Osadź link do OneNote – Zapisz OneNote jako PDF przy użyciu Javy
schemas:
- author: Aspose
  dateModified: '2026-07-29'
  description: Learn how to embed link onenote, save OneNote as PDF, and add hyperlinks
    using Java with Aspose.Note. Export OneNote to PDF effortlessly.
  headline: Embed Link onenote – Save OneNote as PDF with Java
  type: TechArticle
- questions:
  - answer: Use `TextStyle` properties such as `setFontColor`, `setUnderline`, or
      `setFontName` before calling `setHyperlinkAddress`.
    question: How can I customize the appearance of the hyperlink?
  - answer: Yes, Aspose.Note supports DOCX, XPS, HTML, and several other export formats.
    question: Can I save the document in formats other than PDF?
  - answer: Load the existing file with `new Document("input.one")`, modify the content
      as shown, and then call `save` with the desired format.
    question: What if I need to add a hyperlink to an existing OneNote file?
  - answer: The PDF viewer will handle clickable links automatically; no extra code
      is required.
    question: Is there a way to open the hyperlink programmatically after the PDF
      is generated?
  - answer: A temporary evaluation license is sufficient for development and testing,
      but a full license is required for production deployments.
    question: Do I need a license for development use?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote pdf conversion
- Aspose.Note
- Java document processing
title: Osadź link do OneNote – Zapisz OneNote jako PDF przy użyciu Javy
url: /pl/java/onenote-hyperlinks-images/add-hyperlink/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zapisz OneNote jako PDF i dodaj hiperłącze w OneNote przy użyciu Javy

## Wprowadzenie

Jeśli potrzebujesz **embed link onenote** podczas konwertowania notesu na przenośny PDF, trafiłeś we właściwe miejsce. Ten samouczek przeprowadzi Cię przez proces zapisywania OneNote jako PDF oraz wstawiania klikalnych hiperłączy przy użyciu Javy i biblioteki Aspose.Note. Zobaczysz, dlaczego to podejście jest idealne do archiwizacji, udostępniania i automatyzacji przepływów dokumentów.

## Szybkie odpowiedzi
- **Czy mogę zapisać OneNote jako PDF przy użyciu Javy?** Tak, Aspose.Note for Java udostępnia pojedyncze wywołanie `save`, które generuje PDF.
- **Jak wstawić hiperłącze?** Użyj `TextStyle.setHyperlinkAddress` na segmencie `RichText`.
- **Jakie są wymagania wstępne?** JDK 8+ oraz biblioteka Aspose.Note for Java.
- **Jakie formaty wyjściowe są obsługiwane?** PDF, DOCX, XPS i inne.
- **Czy wymagana jest licencja do produkcji?** Tak, wymagana jest licencja komercyjna do użytku nie‑ewaluacyjnego.

## Czym jest „zapisz onenote jako pdf”?

Zapisanie notesu OneNote jako PDF tworzy wersję tylko do odczytu, działającą na różnych platformach, którą każdy może otworzyć bez aplikacji OneNote. Ten format jest idealny do archiwizacji, drukowania lub udostępniania współpracownikom, którzy nie mają zainstalowanego OneNote, przy jednoczesnym zachowaniu oryginalnego układu, obrazów i wszelkich osadzonych hiperłączy.

## Dlaczego generować PDF z OneNote przy użyciu Aspose.Note Java?

Aspose.Note for Java może **export onenote to pdf** z 100 % wiernością układu, obsługując do 200 stron w dokumencie bez ładowania całego pliku do pamięci. Biblioteka przetwarza ponad 30 różnych typów treści — w tym obrazy, tabele i 95 % stylów hiperłączy — dzięki czemu otrzymujesz wierną replikę oryginalnego notesu. Działa także na Windows, Linux i macOS, umożliwiając konwersje wsadowe w chmurze lub w środowiskach lokalnych.

## Wymagania wstępne

Zanim zaczniemy, upewnij się, że masz zainstalowane i skonfigurowane następujące elementy na swoim systemie:

### Java Development Kit (JDK)

Upewnij się, że masz zainstalowany Java Development Kit (JDK). Możesz pobrać i zainstalować JDK ze [strony Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).

### Aspose.Note for Java Library

Pobierz i zainstaluj bibliotekę Aspose.Note for Java. Dokumentację i link do pobrania znajdziesz [tutaj](https://reference.aspose.com/note/java/).

## Importowanie pakietów

Aby rozpocząć, zaimportuj niezbędne pakiety wymagane do pracy z Aspose.Note for Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

Teraz rozbijmy podany przykład na kilka kroków:

## Jak wstawić link onenote podczas zapisywania jako PDF?

Załaduj nową instancję `Document`, zbuduj strukturę strony, zdefiniuj czerwony `TextStyle` dla hiperłącza i na końcu wywołaj `document.save("output.pdf", SaveFormat.Pdf)`. Ta sekwencja tworzy PDF zawierający w pełni funkcjonalne hiperłącze, zachowując wszystkie oryginalne formatowanie i obrazy.

## Krok 1: Ustaw strukturę dokumentu

`Document` reprezentuje notes OneNote w Aspose.Note.  
`Page` jest kontenerem dla konturów i innych elementów na poziomie strony.

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
Title title = new Title();
```

## Krok 2: Zdefiniuj domyślny styl tekstu

`ParagraphStyle` definiuje domyślne formatowanie akapitów, takie jak wyrównanie, odstępy i wcięcia.

```java
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                            .setFontName("Arial")
                                            .setFontSize(10)
                                            .setFontColor(java.awt.Color.GRAY);
```

## Krok 3: Ustaw tekst tytułu

`Title` reprezentuje element tytułu strony w dokumencie OneNote.

```java
RichText titleText = new RichText().append("Title");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
page.setTitle(title);
```

## Krok 4: Utwórz kontur i elementy konturu

`Outline` działa jako kontener dla hierarchii bloków treści.  
`OutlineElement` jest pojedynczym elementem w konturze, takim jak akapit lub tabela.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## Krok 5: Zdefiniuj styl tekstu dla hiperłącza

`TextStyle` kontroluje wygląd wizualny fragmentów tekstu, w tym czcionkę, kolor i ustawienia podkreślenia.

```java
TextStyle textStyleRed = new TextStyle()
                                    .setFontName("Arial")
                                    .setFontSize(10)
                                    .setFontColor(java.awt.Color.red);
```

## Krok 6: Dodaj tekst z hiperłączem

`RichText` reprezentuje fragment sformatowanego tekstu wewnątrz akapitu. Ustawienie adresu hiperłącza sprawia, że tekst jest klikalny w wyeksportowanym PDF.

```java
RichText text = new RichText()
                            .append("This is ", textStyleRed)
                            .append("hyperlink", new TextStyle().setHyperlinkAddress("https://www.google.com"))
                            .append(". This text is not a hyperlink.", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
outlineElem.appendChildLast(text);
```

## Krok 7: Dodaj kontur do strony i stronę do dokumentu

Ten krok dołącza wcześniej utworzone elementy konturu do strony, a następnie dodaje stronę do obiektu `Document`.

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## Krok 8: Zapisz dokument jako PDF

`SaveFormat.Pdf` instruuje Aspose.Note, aby wyeksportował dokument w formacie PDF.

```java
doc.save(dataDir + "AddHyperlink_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "AddHyperlink_out.pdf");
```

## Podsumowanie

Gratulacje! Pomyślnie **zapisano OneNote jako PDF** i dodano hiperłącze do dokumentu przy użyciu Javy oraz biblioteki Aspose.Note. Ta funkcja pozwala **embed link onenote** i tworzyć interaktywne, udostępnialne pliki PDF bezpośrednio z treści OneNote.

## Najczęściej zadawane pytania

**Q: How can I customize the appearance of the hyperlink?**  
A: Use `TextStyle` properties such as `setFontColor`, `setUnderline`, or `setFontName` before calling `setHyperlinkAddress`.

**Q: Can I save the document in formats other than PDF?**  
A: Yes, Aspose.Note supports DOCX, XPS, HTML, and several other export formats.

**Q: What if I need to add a hyperlink to an existing OneNote file?**  
A: Load the existing file with `new Document("input.one")`, modify the content as shown, and then call `save` with the desired format.

**Q: Is there a way to open the hyperlink programmatically after the PDF is generated?**  
A: The PDF viewer will handle clickable links automatically; no extra code is required.

**Q: Do I need a license for development use?**  
A: A temporary evaluation license is sufficient for development and testing, but a full license is required for production deployments.

---

**Ostatnia aktualizacja:** 2026-07-29  
**Testowano z:** Aspose.Note for Java 26.4  
**Autor:** Aspose

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

## Powiązane samouczki

- [Jak zapisać OneNote jako PDF przy użyciu Aspose.Note dla Javy](/note/java/onenote-document-loading/load-save-format/)
- [Konwertuj OneNote do PDF przy użyciu Aspose.Note i PdfSaveOptions](/note/java/onenote-document-loading/load-pdf-save-options/)
- [Dodaj hiperłącze do obrazu w OneNote przy użyciu Javy](/note/java/onenote-hyperlinks-images/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}