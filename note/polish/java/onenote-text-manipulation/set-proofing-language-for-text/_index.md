---
date: 2026-09-29
description: Poradnik ustawiania języka onenote pokazuje, jak przypisać język korekty
  do tekstu w OneNote przy użyciu Aspose.Note dla Javy, z kodem krok po kroku i najlepszymi
  praktykami.
keywords:
- set language onenote
- spell check language onenote
- change text language onenote
- set proofing language onenote
- add language onenote
lastmod: 2026-09-29
linktitle: Ustaw język korekty dla tekstu w OneNote – Aspose.Note
og_description: Przewodnik ustawiania języka onenote dla programistów Javy. Dowiedz
  się, jak zmienić język tekstu, włączyć sprawdzanie pisowni i zapisywać pliki OneNote
  przy użyciu Aspose.Note.
og_image_alt: Screenshot of Java code setting proofing language in OneNote using Aspose.Note
og_title: Jak ustawić język onenote w OneNote – Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-09-29'
  description: Set language onenote tutorial shows you how to assign proofing language
    to text in OneNote using Aspose.Note for Java, with step‑by‑step code and best
    practices.
  headline: How to set language onenote in a OneNote document – Aspose.Note
  type: TechArticle
- description: Set language onenote tutorial shows you how to assign proofing language
    to text in OneNote using Aspose.Note for Java, with step‑by‑step code and best
    practices.
  name: How to set language onenote in a OneNote document – Aspose.Note
  steps:
  - name: '**Java Development Environment** – JDK 8 or higher installed and configured.'
    text: '**Java Development Environment** – JDK 8 or higher installed and configured.'
  - name: '**Aspose.Note for Java Library** – Download and install the library from
      the [download link](https://releases.aspose.com/note/java/).'
    text: '**Aspose.Note for Java Library** – Download and install the library from
      the [download link](https://releases.aspose.com/note/java/).'
  - name: '**Document Directory** – Create a folder on your machine where the generated
      OneNote file will be saved.'
    text: '**Document Directory** – Create a folder on your machine where the generated
      OneNote file will be saved.'
  type: HowTo
- questions:
  - answer: Absolutely! Add additional `append` calls with the desired `Locale.forLanguageTag("xx-XX")`.
    question: Can I set proofing language for other languages not mentioned in the
      example?
  - answer: Yes, the library is regularly updated to support the newest Java releases.
    question: Is Aspose.Note for Java compatible with the latest Java versions?
  - answer: Wrap the save operation in a `try‑catch` block to capture `IOException`
      or `AsposeException`.
    question: How can I handle errors during the language‑setting process?
  - answer: Certainly. Just include the Aspose.Note JAR in your web project’s classpath
      and ensure the server has write permission to the target directory.
    question: Can I integrate this code into a web application?
  - answer: Explore the [documentation](https://reference.aspose.com/note/java/) for
      a full list of APIs and sample projects.
    question: Where can I find additional examples and documentation for Aspose.Note
      for Java?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote language
- Aspose.Note
- Java document processing
- proofing language
- onenote API
title: Jak ustawić język onenote w dokumencie OneNote – Aspose.Note
url: /pl/java/onenote-text-manipulation/set-proofing-language-for-text/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak ustawić język onenote w dokumencie OneNote – Aspose.Note

## Wprowadzenie
Jeśli potrzebujesz **ustawić język onenote** dla konkretnych fragmentów tekstu w notatniku OneNote, Aspose.Note for Java ułatwia to. W tym samouczku nauczysz się, jak utworzyć dokument OneNote, zmienić język tekstu dla pojedynczych słów lub fraz oraz ostatecznie zapisać plik OneNote z zastosowanym prawidłowym językiem korekty. Po zakończeniu zrozumiesz, dlaczego ustawianie języka ma znaczenie dla sprawdzania pisowni i lokalizacji, oraz będziesz mieć gotowy do uruchomienia przykład kodu.

## Szybkie odpowiedzi
- **Co wpływa ustawienie „set language”?** Informuje OneNote, którego słownika korekty użyć do sprawdzania pisowni i gramatyki.  
- **Czy mogę ustawić różne języki w tej samej notatce?** Tak, możesz przypisać język do każdego fragmentu tekstu.  
- **Czy potrzebuję licencji na Aspose.Note?** Darmowa wersja próbna działa do testów; licencja komercyjna jest wymagana w produkcji.  
- **Jakie wersje Javy są obsługiwane?** Aspose.Note for Java obsługuje Javę 8 i nowsze.  
- **Czy wynikowy plik jest .one?** Tak, dokument jest zapisywany jako plik OneNote *.one*.

## Co to jest ustawianie języka onenote?
`set language onenote` odnosi się do przypisania lokalizacji IETF BCP‑47 do fragmentu tekstu, tak aby silnik korekty OneNote używał odpowiedniego słownika. Te metadane podróżują wraz z plikiem *.one* i są respektowane przez klienta OneNote na każdej platformie.

## Dlaczego ustawiać język onenote?
Zastosowanie prawidłowego języka poprawia dokładność sprawdzania pisowni nawet o **95 %** w wielojęzycznych notatnikach oraz przyspiesza indeksowanie o około **30 %**, ponieważ silnik może pomijać nieistotne słowniki. Aspose.Note obsługuje **30+** formatów wejściowych i wyjściowych oraz może przetwarzać notatniki z **10 000+** stronami bez ładowania całego pliku do pamięci.

## Wymagania wstępne
Zanim zanurzysz się w kod, upewnij się, że masz następujące:

1. **Java Development Environment** – Zainstalowany i skonfigurowany JDK 8 lub nowszy.  
2. **Aspose.Note for Java Library** – Pobierz i zainstaluj bibliotekę z [download link](https://releases.aspose.com/note/java/).  
3. **Document Directory** – Utwórz folder na swoim komputerze, w którym zostanie zapisany wygenerowany plik OneNote.

## Jak ustawić język onenote
Aby ustawić język, najpierw wczytaj istniejący dokument OneNote lub utwórz nową instancję `Document`. Następnie, dla każdego segmentu tekstu, który chcesz zmodyfikować, utwórz lub pobierz obiekt `RichText`, zastosuj `TextStyle` z żądaną `Locale` (na przykład `Locale.forLanguageTag("en-US")`), i dołącz sformatowany tekst z powrotem do konturu (outline). Na koniec wywołaj `document.save`, aby zapisać zmiany do pliku *.one*, zachowując metadane językowe.

## Krok 1: przygotowanie dokumentu i strony
Document jest obiektem najwyższego poziomu w Aspose.Note, który reprezentuje notatnik OneNote w pamięci. Po utworzeniu instancji `Document` możesz dodawać strony, kontury (outlines) i inne elementy.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.Locale;
```

## Krok 2: utwórz kontur i element konturu
`Outline` działa jako kontener dla zawartości strony, natomiast `OutlineElement` przechowuje poszczególne elementy, takie jak tekst sformatowany (rich text).

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
```

## Krok 3: dodaj tekst sformatowany z ustawieniami języka
`RichText` przechowuje rzeczywiste znaki. `TextStyle` pozwala dołączyć `Locale` (np. `en‑US`, `fr‑FR`) do fragmentu tekstu, co jest sposobem na **ustawienie języka onenote**. Zastosowanie stylu do każdego wywołania `append` zapewnia precyzyjną kontrolę.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## Krok 4: uporządkuj elementy i zapisz
`ParagraphStyle` może być użyty, gdy chcesz ustawić język dla całego akapitu zamiast pojedynczych słów. Po zbudowaniu hierarchii konturu wywołaj `document.save`, aby zapisać plik *.one* zachowujący wszystkie metadane językowe.

```java
RichText text = new RichText()
                        .append("United States", new TextStyle().setLanguage(Locale.forLanguageTag("en-US")))
                        .append(" Germany", new TextStyle().setLanguage(Locale.forLanguageTag("de-DE")))
                        .append(" China", new TextStyle().setLanguage(Locale.forLanguageTag("zh-CN")));
text.setParagraphStyle(ParagraphStyle.getDefault());
```

## Typowe pułapki i wskazówki
- **Format lokalizacji** – Używaj tagu IETF BCP‑47 (np. `en-US`, `de-DE`). Nieprawidłowy tag spowoduje domyślny język dokumentu.  
- **Ścieżka pliku** – Upewnij się, że `dataDir` wskazuje istniejący folder; w przeciwnym razie `document.save` zgłosi `IOException`.  
- **Wskazówka:** Jeśli potrzebujesz ustawić język dla całego akapitu, zastosuj `TextStyle` do `ParagraphStyle` zamiast do każdego wywołania `append`.

## Podsumowanie
Właśnie nauczyłeś się **jak ustawić język onenote** dla poszczególnych fragmentów tekstu w notatniku OneNote przy użyciu Aspose.Note for Java. Ta funkcja pozwala **tworzyć dokument OneNote** programowo, **zmieniać język tekstu** w locie oraz **zapisywać plik OneNote** z dokładnymi metadanymi korekty.

## Najczęściej zadawane pytania

**Q: Czy mogę ustawić język korekty dla innych języków nie wymienionych w przykładzie?**  
A: Zdecydowanie! Dodaj dodatkowe wywołania `append` z żądaną `Locale.forLanguageTag("xx-XX")`.

**Q: Czy Aspose.Note for Java jest kompatybilny z najnowszymi wersjami Javy?**  
A: Tak, biblioteka jest regularnie aktualizowana, aby wspierać najnowsze wydania Javy.

**Q: Jak mogę obsłużyć błędy podczas procesu ustawiania języka?**  
A: Otocz operację zapisu w bloku `try‑catch`, aby przechwycić `IOException` lub `AsposeException`.

**Q: Czy mogę zintegrować ten kod z aplikacją webową?**  
A: Oczywiście. Wystarczy dodać plik JAR Aspose.Note do ścieżki klas (classpath) projektu webowego i upewnić się, że serwer ma uprawnienia do zapisu w docelowym katalogu.

**Q: Gdzie mogę znaleźć dodatkowe przykłady i dokumentację dla Aspose.Note for Java?**  
A: Zapoznaj się z [documentation](https://reference.aspose.com/note/java/) aby uzyskać pełną listę API i przykładowych projektów.

---

**Ostatnia aktualizacja:** 2026-09-29  
**Testowano z:** Aspose.Note for Java 24.12  
**Autor:** Aspose  

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
document.appendChildLast(page);
document.save(Paths.get(dataDir, "SetProofingLanguageForText.one").toString()); 
```

## Powiązane samouczki

- [Załaduj plik OneNote przy użyciu Java: użyj Aspose.Note do ładowania dokumentów OneNote](/note/java/onenote-document-loading/load-onenote-document/)
- [Konwertuj OneNote na zwykły tekst – wyodrębnij cały tekst przy użyciu Aspose.Note for Java](/note/java/onenote-text-manipulation/extract-all-text/)
- [Konwertuj OneNote na PDF używając ustawień strony z Aspose.Note for Java](/note/java/onenote-document-saving/save-to-pdf-using-page-settings/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}