---
date: 2026-03-29
description: Dowiedz się, jak ustawić język tekstu w OneNote przy użyciu Aspose.Note
  dla Javy. Ten przewodnik krok po kroku pokazuje, jak utworzyć dokument OneNote,
  zmienić język tekstu i efektywnie zapisać plik OneNote.
linktitle: Set Proofing Language for Text in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Jak ustawić język dla tekstu w OneNote – Aspose.Note
url: /pl/java/onenote-text-manipulation/set-proofing-language-for-text/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak ustawić język dla tekstu w OneNote – Aspose.Note

## Wprowadzenie
Jeśli potrzebujesz **how to set language** dla konkretnych fragmentów tekstu w notesie OneNote, Aspose.Note for Java ułatwia to. W tym samouczku dowiesz się, jak utworzyć dokument OneNote, zmienić język tekstu dla pojedynczych słów lub fraz oraz ostatecznie zapisać plik OneNote z zastosowanym prawidłowym językiem korekty. Po zakończeniu zrozumiesz, dlaczego ustawianie języka ma znaczenie dla sprawdzania pisowni i lokalizacji, oraz będziesz mieć gotowy do uruchomienia przykład kodu.

## Szybkie odpowiedzi
- **What does “set language” affect?** Informuje OneNote, którego słownika korekty używać do sprawdzania pisowni i gramatyki.
- **Can I set different languages in the same note?** Tak, możesz przypisać język do każdego fragmentu tekstu.
- **Do I need a license for Aspose.Note?** Darmowa wersja próbna działa do testów; licencja komercyjna jest wymagana w środowisku produkcyjnym.
- **Which Java versions are supported?** Aspose.Note for Java obsługuje Java 8 i nowsze.
- **Is the output a .one file?** Tak, dokument jest zapisywany jako plik OneNote *.one*.

## Wymagania wstępne
Zanim zagłębisz się w kod, upewnij się, że masz następujące:

1. **Java Development Environment** – Zainstalowany i skonfigurowany JDK 8 lub nowszy.  
2. **Aspose.Note for Java Library** – Pobierz i zainstaluj bibliotekę z [download link](https://releases.aspose.com/note/java/).  
3. **Document Directory** – Utwórz folder na swoim komputerze, w którym zostanie zapisany wygenerowany plik OneNote.

## Dlaczego ustawiać język dla tekstu w OneNote?
Ustawienie języka korekty zapewnia, że sprawdzanie pisowni, sugestie gramatyczne i indeksowanie wyszukiwania działają poprawnie dla treści wielojęzycznych. Jest to szczególnie przydatne dla:

- **Global teams** współpracujących nad jednym notesem.  
- **Localized documentation**, w której każda sekcja może być w innym języku.  
- **Data‑driven applications** generujące notatki programowo dla użytkowników na całym świecie.

## Importowanie pakietów
Zacznij od zaimportowania niezbędnych klas Aspose.Note i narzędzi Java.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.Locale;
```

## Krok 1: Konfiguracja dokumentu i strony
Utwórz nowy dokument OneNote oraz stronę, która będzie zawierać Twoją treść. Ten krok również demonstruje **create OneNote document**.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
```

## Krok 2: Utwórz kontur i element konturu
Kontur (outline) jest kontenerem dla zawartości notesu. Tutaj budujemy strukturę, która później będzie zawierać tekst specyficzny dla języka.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## Krok 3: Dodaj tekst sformatowany z ustawieniami języka
Teraz **change text language** poprzez dołączenie `TextStyle` z określonym `Locale` do każdego segmentu tekstu. To demonstruje **set language for text**.

```java
RichText text = new RichText()
                        .append("United States", new TextStyle().setLanguage(Locale.forLanguageTag("en-US")))
                        .append(" Germany", new TextStyle().setLanguage(Locale.forLanguageTag("de-DE")))
                        .append(" China", new TextStyle().setLanguage(Locale.forLanguageTag("zh-CN")));
text.setParagraphStyle(ParagraphStyle.getDefault());
```

## Krok 4: Organizacja elementów i zapis
Złóż hierarchię konturu, dołącz ją do strony i ostatecznie **save OneNote file** z zastosowanymi ustawieniami języka.

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
document.appendChildLast(page);
document.save(Paths.get(dataDir, "SetProofingLanguageForText.one").toString()); 
```

## Typowe pułapki i wskazówki
- **Locale format** – Użyj znacznika IETF BCP‑47 (np. `en-US`, `de-DE`). Nieprawidłowy znacznik spowoduje użycie domyślnego języka dokumentu.  
- **File path** – Upewnij się, że `dataDir` wskazuje istniejący folder; w przeciwnym razie `document.save` zgłosi `IOException`.  
- **Pro tip:** Jeśli potrzebujesz ustawić język dla całego akapitu, zastosuj `TextStyle` do `ParagraphStyle` zamiast do każdego wywołania `append`.

## Podsumowanie
Właśnie nauczyłeś się **how to set language** dla poszczególnych fragmentów tekstu w notesie OneNote przy użyciu Aspose.Note for Java. Ta funkcja pozwala **create OneNote document** programowo, **change text language** w locie oraz **save OneNote file** z dokładnymi metadanymi korekty.

## Najczęściej zadawane pytania

**Q: Can I set proofing language for other languages not mentioned in the example?**  
A: Zdecydowanie! Dodaj dodatkowe wywołania `append` z żądanym `Locale.forLanguageTag("xx-XX")`.

**Q: Is Aspose.Note for Java compatible with the latest Java versions?**  
A: Tak, biblioteka jest regularnie aktualizowana, aby obsługiwać najnowsze wersje Java.

**Q: How can I handle errors during the language‑setting process?**  
A: Umieść operację zapisu w bloku `try‑catch`, aby przechwycić `IOException` lub `AsposeException`.

**Q: Can I integrate this code into a web application?**  
A: Oczywiście. Po prostu dołącz plik JAR Aspose.Note do ścieżki klas swojego projektu webowego i upewnij się, że serwer ma uprawnienia do zapisu w docelowym katalogu.

**Q: Where can I find additional examples and documentation for Aspose.Note for Java?**  
A: Przeglądaj [documentation](https://reference.aspose.com/note/java/) aby uzyskać pełną listę interfejsów API i przykładowych projektów.

---

**Ostatnia aktualizacja:** 2026-03-29  
**Testowano z:** Aspose.Note for Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}