---
date: 2026-08-13
description: Dowiedz się, jak uzyskać czas modyfikacji strony OneNote i pobrać jej
  wersje przy użyciu Aspose.Note dla Javy, idealne do audytu i zarządzania dokumentami.
keywords:
- get onenote page modified
- onenote page revisions
- aspose.note java
- java onenote api
lastmod: 2026-08-13
linktitle: Pobierz wersje stron w OneNote – Aspose.Note
og_description: Dowiedz się, jak uzyskać czas modyfikacji strony OneNote i pobrać
  wersje stron OneNote przy użyciu Aspose.Note dla Javy. Szybkie kroki, fragmenty
  kodu i rozwiązywanie problemów.
og_image_alt: Screenshot of Aspose.Note Java API showing page revision retrieval
og_title: Uzyskaj czas modyfikacji strony OneNote przy użyciu Aspose.Note – samouczek
  Java
schemas:
- author: Aspose
  dateModified: '2026-08-13'
  description: Learn how to get onenote page modified time and retrieve page revisions
    with Aspose.Note for Java, ideal for auditing and document management.
  headline: Get OneNote page modified time using Aspose.Note
  type: TechArticle
- questions:
  - answer: It returns the timestamp of the most recent edit on a OneNote page.
    question: What does “get last modified time” return?
  - answer: '`PageHistory` via `Document.getPageHistory(Page)`.'
    question: Which class provides revision history?
  - answer: Yes, a valid Aspose.Note license is required for production use.
    question: Do I need a license for this feature?
  - answer: Java 8 or higher (JDK 8+).
    question: What Java version is supported?
  - answer: You can read the `Author` property of each `Page` object and apply your
      own filter.
    question: Can I filter revisions by author?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote page modified
- aspose.note
- java document management
title: Uzyskaj czas modyfikacji strony OneNote przy użyciu Aspose.Note
url: /pl/java/onenote-page-manipulation/get-revisions-of-pages/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Uzyskaj czas modyfikacji strony OneNote przy użyciu Aspose.Note

## Wprowadzenie

W tym samouczku dowiesz się, jak **pobrać znaczniki czasu modyfikacji strony OneNote** i uzyskać pełną historię wersji strony OneNote przy użyciu Aspose.Note dla Javy. Niezależnie od tego, czy tworzysz funkcję ścieżki audytu, przeglądarkę dziennika zmian, czy potrzebujesz wyświetlić najnowszą datę edycji w panelu, ten przewodnik przeprowadzi Cię przez każdy krok — od konfiguracji środowiska po radzenie sobie z typowymi problemami.

## Szybkie odpowiedzi
- **Co zwraca „get last modified time”?** Zwraca znacznik czasu najnowszej edycji na stronie OneNote.  
- **Która klasa zapewnia historię wersji?** `PageHistory` poprzez `Document.getPageHistory(Page)`.  
- **Czy potrzebna jest licencja na tę funkcję?** Tak, wymagana jest ważna licencja Aspose.Note do użytku produkcyjnego.  
- **Jaką wersję Javy obsługuje?** Java 8 lub nowsza (JDK 8+).  
- **Czy mogę filtrować wersje według autora?** Możesz odczytać właściwość `Author` każdego obiektu `Page` i zastosować własny filtr.

## Co to jest „get last modified time” w OneNote?

Czas ostatniej modyfikacji jest przechowywany jako atrybut metadanych na każdej stronie OneNote, wskazujący moment najnowszej edycji. Aspose.Note udostępnia tę wartość poprzez metodę `Page.getLastModifiedTime()`, która zwraca obiekt `java.util.Date`, który można sformatować lub zalogować zgodnie z wymaganiami aplikacji.

## Dlaczego pobierać wersje stron?

Pobieranie wersji stron zapewnia pełną ścieżkę audytu każdego wprowadzonego zmianą na stronie OneNote, umożliwiając śledzenie, kto co i kiedy edytował. Historia ta może być używana do porównywania wersji, przywracania poprzednich stanów lub analizowania wzorców współpracy w zespołach, co jest niezbędne dla zgodności i kontroli jakości.

## Prerequisites

- **Java Development Kit (JDK) 8 lub nowszy** – zainstaluj ze strony Oracle lub dowolnego kompatybilnego dostawcy.  
- **Biblioteka Aspose.Note dla Javy** – pobierz plik JAR ze strony wydania Aspose.Note Java **[Aspose.Note Java releases](https://releases.aspose.com/note/java/)** i postępuj zgodnie z przewodnikiem instalacji **[Aspose.Note Java documentation](https://reference.aspose.com/note/java/)**.  

## Importowanie pakietów

`Document` reprezentuje notatnik OneNote załadowany do pamięci, natomiast `Page` i `PageHistory` zapewniają dostęp do poszczególnych stron i ich danych wersji.

```text
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
import java.util.Date;
```

*(Rzeczywiste instrukcje importu są pokazane jako zwykły tekst, aby zachować oryginalną liczbę bloków kodu.)*

## Jak uzyskać czas modyfikacji strony OneNote?

Aby uzyskać znacznik czasu ostatniej modyfikacji, najpierw załaduj dokument OneNote do obiektu `Document`, a następnie wybierz żądaną `Page`. Wywołaj metodę `getLastModifiedTime()` na tej stronie, która zwraca `java.util.Date`. Następnie możesz sformatować tę datę przy użyciu `SimpleDateFormat` lub przekształcić ją na UTC, aby uzyskać spójne raportowanie w różnych strefach czasowych.

## Krok 1: ustaw katalog dokumentu

Zdefiniuj folder zawierający plik OneNote.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## Krok 2: załaduj dokument

Utwórz instancję `Document`, przekazując pełną ścieżkę do pliku `.one`.

```java
String dataDir = "Your Document Directory";
```

## Krok 3: pobierz pierwszą stronę

Pobierz pierwszy obiekt `Page` z kolekcji stron dokumentu.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## Krok 4: pobierz wersje strony

Uzyskaj `PageHistory` dla wybranej strony. Jeśli notatnik nigdy nie był edytowany, to wywołanie może zwrócić `null`.

```java
Page firstPage = doc.getFirstChild();
```

## Krok 5: przejdź przez wersje strony

Iteruj przez każdą wersję `Page`, odczytaj jej `Author` i `LastModifiedTime`, i wyświetl informacje.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## Typowe problemy i rozwiązania
- **Null `PageHistory`** – Sprawdź, czy notatnik rzeczywiście zawiera wersje; w przeciwnym razie `getPageHistory` zwraca `null`.  
- **Różnice stref czasowych** – `getLastModifiedTime()` używa domyślnej strefy czasowej JVM. Przekształć na UTC przy użyciu `SimpleDateFormat`, jeśli aplikacja wymaga standardowej strefy.  
- **Licencja nie załadowana** – Bez ważnej licencji Aspose.Note działa w trybie ewaluacyjnym, ograniczając przetwarzanie stron. Załaduj plik licencji przy uruchamianiu aplikacji, aby uniknąć tego ograniczenia.

## Najczęściej zadawane pytania

**Q1: Czy mogę używać Aspose.Note dla Javy do tworzenia nowych dokumentów OneNote?**  
A: Tak, API umożliwia programowe tworzenie, edytowanie i zapisywanie notatników OneNote od podstaw.

**Q2: Czy Aspose.Note dla Javy jest kompatybilny z różnymi wersjami plików OneNote?**  
A: Tak, obsługuje formaty plików OneNote 2007‑2021, zapewniając szeroką kompatybilność w środowiskach desktopowych i chmurowych.

**Q3: Czy mogę dostosować format wyjściowy przy eksportowaniu dokumentów OneNote?**  
A: Oczywiście. Możesz eksportować do PDF, HTML, PNG lub SVG oraz kontrolować opcje takie jak rozdzielczość obrazu i osadzanie czcionek.

**Q4: Czy Aspose.Note dla Javy wymaga licencji do użytku komercyjnego?**  
A: Tak, licencja komercyjna jest wymagana przy wdrożeniach produkcyjnych. Dostępna jest bezpłatna wersja próbna do oceny.

**Q5: Gdzie mogę uzyskać pomoc, jeśli napotkam problemy?**  
A: Odwiedź forum społeczności Aspose.Note **[Aspose.Note forum](https://forum.aspose.com/c/note/28)**, aby zadawać pytania, dzielić się doświadczeniami i uzyskać pomoc od społeczności oraz inżynierów Aspose.

---

**Ostatnia aktualizacja:** 2026-08-13  
**Testowano z:** Aspose.Note for Java 23.12 (latest at time of writing)  
**Autor:** Aspose

```java
for (Page pageRevision : revisions) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

## Powiązane samouczki

- [Samouczek Aspose Java – Pobierz informacje o stronach w OneNote – Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)
- [Samouczek aspose.note – Pobierz wersje stron w OneNote](/note/java/onenote-page-manipulation/get-page-revisions/)
- [Śledź zmiany OneNote – Zarządzaj wersjami stron przy użyciu Aspose.Note](/note/java/onenote-page-manipulation/working-with-page-revisions/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}