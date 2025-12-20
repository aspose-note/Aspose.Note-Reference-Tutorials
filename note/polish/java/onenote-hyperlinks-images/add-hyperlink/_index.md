---
date: 2025-12-20
description: Dowiedz się, jak zapisać OneNote jako PDF i dodać hiperłącze w OneNote
  przy użyciu Javy oraz biblioteki Aspose.Note. Generuj PDF z OneNote bez wysiłku.
linktitle: Save OneNote as PDF and Add Hyperlink in OneNote with Java
second_title: Aspose.Note Java API
title: Zapisz OneNote jako PDF i dodaj hiperłącze w OneNote przy użyciu Javy
url: /pl/java/onenote-hyperlinks-images/add-hyperlink/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zapisz OneNote jako PDF i dodaj hiperłącze w OneNote przy użyciu Java

## Wprowadzenie

Dodawanie hiperłączy do dokumentów OneNote oraz jednoczesne zapisywanie ich jako PDF może znacząco poprawić interaktywność notatek i ułatwić udostępnianie. W tym samouczku nauczysz się **jak zapisać OneNote jako PDF** i osadzić klikalny link przy użyciu Java oraz biblioteki Aspose.Note. Przejdźmy razem przez kolejne kroki!

## Szybkie odpowiedzi
- **Czy mogę zapisać OneNote jako PDF przy użyciu Java?** Tak, Aspose.Note for Java udostępnia pojedyncze wywołanie `save`, które generuje plik PDF.
- **Jak dodać hiperłącze?** Użyj `TextStyle.setHyperlinkAddress` na segmencie `RichText`.
- **Jakie są wymagania wstępne?** JDK 8+ oraz biblioteka Aspose.Note for Java.
- **Jakie formaty wyjściowe są obsługiwane?** PDF, DOCX, XPS i inne.
- **Czy wymagana jest licencja do użytku produkcyjnego?** Tak, do użytku nie‑ewaluacyjnego potrzebna jest licencja komercyjna.

## Co to jest „save onenote as pdf”?

Zapisanie notesu OneNote jako PDF tworzy przenośną, tylko‑do‑odczytu wersję notatek, którą można otworzyć na dowolnym urządzeniu bez aplikacji OneNote. Jest to szczególnie przydatne do archiwizacji, drukowania lub udostępniania osobom, które nie mają OneNote.

## Dlaczego generować PDF z OneNote przy użyciu Aspose.Note Java?

- **Pełna wierność:** Zachowuje formatowanie, obrazy i hiperłącza.
- **Kontrola programowa:** Automatyzuj konwersje wsadowe w usługach backendowych.
- **Wieloplatformowość:** Działa na Windows, Linux i macOS.
- **Bogate API:** Łatwo dodawaj lub modyfikuj zawartość przed zapisem.

## Wymagania wstępne

Zanim zaczniemy, upewnij się, że masz zainstalowane i skonfigurowane następujące elementy:

### Java Development Kit (JDK)

Upewnij się, że masz zainstalowany Java Development Kit (JDK). Możesz pobrać i zainstalować JDK ze [strony Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).

### Biblioteka Aspose.Note for Java

Pobierz i zainstaluj bibliotekę Aspose.Note for Java. Dokumentację oraz link do pobrania znajdziesz [tutaj](https://reference.aspose.com/note/java/).

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

## Krok 1: Konfiguracja struktury dokumentu

Najpierw utwórz nowy dokument i stronę, na której będzie znajdować się zawartość.

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
Title title = new Title();
```

## Krok 2: Definicja domyślnego stylu tekstu

Zdefiniuj domyślny styl akapitu, który zostanie zastosowany do większości elementów tekstowych.

```java
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                            .setFontName("Arial")
                                            .setFontSize(10)
                                            .setFontColor(java.awt.Color.GRAY);
```

## Krok 3: Ustawienie tekstu tytułu

Utwórz tytuł strony i zastosuj domyślny styl.

```java
RichText titleText = new RichText().append("Title");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
page.setTitle(title);
```

## Krok 4: Utworzenie konturu i elementów konturu

Kontury działają jak kontenery dla akapitów i innych elementów.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## Krok 5: Definicja stylu tekstu dla hiperłącza

Tutaj definiujemy styl w kolorze czerwonym, który zostanie użyty dla klikalnej części.

```java
TextStyle textStyleRed = new TextStyle()
                                    .setFontName("Arial")
                                    .setFontSize(10)
                                    .setFontColor(java.awt.Color.red);
```

## Krok 6: Dodanie tekstu z hiperłączem

Teraz budujemy obiekt `RichText`, który miesza zwykły tekst i hiperłącze.  
Metoda `setHyperlinkAddress` informuje Aspose.Note, że ten segment ma być klikalny.

```java
RichText text = new RichText()
                            .append("This is ", textStyleRed)
                            .append("hyperlink", new TextStyle().setHyperlinkAddress("www.google.com"))
                            .append(". This text is not a hyperlink.", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
outlineElem.appendChildLast(text);
```

## Krok 7: Dodanie konturu do strony i strony do dokumentu

Dołącz element konturu do konturu, kontur do strony, a na końcu stronę do dokumentu.

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## Krok 8: Zapisanie dokumentu jako PDF

Ostatnim krokiem jest zapisanie dokumentu OneNote jako plik PDF. To właśnie tutaj wkracza główne słowo kluczowe **save onenote as pdf**.

```java
doc.save(dataDir + "AddHyperlink_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "AddHyperlink_out.pdf");
```

## Podsumowanie

Gratulacje! Pomyślnie **zapisano OneNote jako PDF** i dodano hiperłącze do dokumentu przy użyciu Java oraz biblioteki Aspose.Note. Dzięki temu możesz tworzyć interaktywne, łatwe do udostępniania pliki PDF bezpośrednio z zawartości OneNote.

## FAQ

### Pytanie 1: Czy Aspose.Note jest kompatybilny ze wszystkimi wersjami Java?

Odpowiedź 1: Tak, Aspose.Note for Java obsługuje wszystkie główne wersje Java, w tym JDK 8 i wyższe.

### Pytanie 2: Czy mogę dodać wiele hiperłączy w jednym dokumencie przy użyciu Aspose.Note?

Odpowiedź 2: Oczywiście! Możesz dodać dowolną liczbę hiperłączy w dokumencie OneNote przy użyciu Aspose.Note for Java.

### Pytanie 3: Czy Aspose.Note oferuje wsparcie dla innych języków programowania?

Odpowiedź 3: Tak, Aspose.Note udostępnia biblioteki dla różnych języków programowania, w tym .NET, Python i Android.

### Pytanie 4: Czy Aspose.Note jest łatwy do integracji w istniejących projektach Java?

Odpowiedź 4: Tak, integracja Aspose.Note w projektach Java jest prosta i dobrze udokumentowana, co ułatwia szybki start.

### Pytanie 5: Gdzie mogę znaleźć więcej pomocy i zasobów dotyczących Aspose.Note?

Odpowiedź 5: Rozbudowaną dokumentację, samouczki i wsparcie społeczności znajdziesz na [forum Aspose.Note](https://forum.aspose.com/c/note/28).

## Frequently Asked Questions

**Q: Jak mogę dostosować wygląd hiperłącza?**  
A: Użyj właściwości `TextStyle`, takich jak `setFontColor`, `setUnderline` lub `setFontName`, przed wywołaniem `setHyperlinkAddress`.

**Q: Czy mogę zapisać dokument w formatach innych niż PDF?**  
A: Tak, Aspose.Note obsługuje DOCX, XPS, HTML oraz kilka innych formatów eksportu.

**Q: Co zrobić, jeśli muszę dodać hiperłącze do istniejącego pliku OneNote?**  
A: Załaduj istniejący plik przy pomocy `new Document("input.one")`, zmodyfikuj zawartość jak pokazano, a następnie wywołaj `save` z żądanym formatem.

**Q: Czy istnieje sposób, aby otworzyć hiperłącze programowo po wygenerowaniu PDF?**  
A: Przeglądarka PDF automatycznie obsłuży klikalne linki; nie jest wymagany dodatkowy kod.

**Q: Czy potrzebna jest licencja do użytku deweloperskiego?**  
A: Tymczasowa licencja ewaluacyjna wystarczy do rozwoju i testów, ale pełna licencja jest wymagana przy wdrożeniach produkcyjnych.

---

**Ostatnia aktualizacja:** 2025-12-20  
**Testowano z:** Aspose.Note for Java 23.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}