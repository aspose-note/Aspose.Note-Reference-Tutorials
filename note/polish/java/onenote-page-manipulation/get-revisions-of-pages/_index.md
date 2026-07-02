---
date: 2026-01-10
description: Dowiedz się, jak uzyskać czas ostatniej modyfikacji i pobrać wersje stron
  OneNote przy użyciu Aspose.Note dla Javy. Zintegruj to w swoich aplikacjach Java,
  aby efektywnie zarządzać dokumentami.
linktitle: Get Revisions of Pages in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Jak uzyskać czas ostatniej modyfikacji stron OneNote – Aspose.Note
url: /pl/java/onenote-page-manipulation/get-revisions-of-pages/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Uzyskiwanie wersji stron w OneNote - Aspose.Note

## Wprowadzenie

W tym samouczku **pobierzesz czas ostatniej modyfikacji** stron w dokumencie OneNote i dowiesz się, jak uzyskać pełną historię wersji przy użyciu Aspose.Note dla Javy. Niezależnie od tego, czy tworzysz system zarządzania dokumentami, audytujesz zmiany, czy po prostu potrzebujesz wyświetlić, kiedy strona była ostatnio edytowana, ten przewodnik pokaże Ci dokładnie, jak programowo wydobyć te informacje.

## Szybkie odpowiedzi
- **Co zwraca „get last modified time”?** Znacznik czasu najnowszej edycji na stronie OneNote.  
- **Która klasa zapewnia historię wersji?** `PageHistory` poprzez `Document.getPageHistory(Page)`.  
- **Czy potrzebna jest licencja do tej funkcji?** Tak, do użycia w środowisku produkcyjnym wymagana jest ważna licencja Aspose.Note.  
- **Jaką wersję Javy obsługuje?** Java 8 lub nowsza (JDK 8+).  
- **Czy mogę filtrować wersje według autora?** Możesz odczytać właściwość `Author` każdego obiektu `Page` i zastosować własny filtr.

## Co to jest „get last modified time” w OneNote?

**Czas ostatniej modyfikacji** to pole metadanych przechowywane przy każdej stronie, które rejestruje, kiedy strona została ostatnio zmieniona. Aspose.Note udostępnia tę wartość poprzez metodę `Page.getLastModifiedTime()`, co ułatwia wyświetlanie lub rejestrowanie dat zmian.

## Dlaczego pobierać wersje stron?

- **Ścieżki audytu:** Zachowaj rejestr, kto co i kiedy zmienił.  
- **Porównanie wersji:** Twórz funkcje porównujące dwie wersje obok siebie.  
- **Wgląd w współpracę użytkowników:** Zrozum wzorce edycji w udostępnionych notatnikach.  

## Wymagania wstępne

Zanim rozpoczniesz, upewnij się, że masz następujące elementy:

### Zainstalowany Java Development Kit (JDK)

Zainstaluj JDK 8 lub nowszy ze strony Oracle lub za pomocą preferowanego menedżera pakietów.

### Biblioteka Aspose.Note dla Javy

Pobierz bibliotekę z oficjalnej strony. Link do pobrania znajdziesz **[tutaj](https://releases.aspose.com/note/java/)**. Postępuj zgodnie z instrukcjami instalacji w dokumentacji **[tutaj](https://reference.aspose.com/note/java/)**.

## Importowanie pakietów

Aby rozpocząć, zaimportuj niezbędne pakiety do swojego projektu Java. Pakiety te umożliwią korzystanie z funkcjonalności dostarczanej przez Aspose.Note dla Javy.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

Teraz rozbijmy dostarczony przykład kodu na kilka kroków, aby zrozumieć każdy element i jego funkcjonalność.

## Jak uzyskać czas ostatniej modyfikacji strony OneNote

### Krok 1: Ustaw katalog dokumentu

Zdefiniuj katalog, w którym znajduje się Twój dokument OneNote.

```java
String dataDir = "Your Document Directory";
```

### Krok 2: Załaduj dokument

Załaduj dokument OneNote do Aspose.Note.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

### Krok 3: Pobierz pierwszą stronę

Pobierz pierwszą stronę z dokumentu.

```java
Page firstPage = doc.getFirstChild();
```

### Krok 4: Pobierz wersje strony

Uzyskaj historię wersji strony.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

### Krok 5: Przeglądaj wersje strony

Iteruj przez listę wersji strony i pobierz odpowiednie informacje, w tym **czas ostatniej modyfikacji**.

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

## Typowe problemy i rozwiązania
- **Null `PageHistory`:** Upewnij się, że dokument rzeczywiście zawiera wersje; w przeciwnym razie `getPageHistory` może zwrócić `null`.  
- **Różnice stref czasowych:** `getLastModifiedTime()` zwraca `java.util.Date` w domyślnej strefie czasowej systemu. W razie potrzeby skonwertuj do UTC.  
- **Licencja niezaładowana:** Bez ważnej licencji Aspose.Note może działać w trybie ewaluacyjnym, ograniczając liczbę przetwarzanych stron.

## Najczęściej zadawane pytania

### Q1: Czy mogę używać Aspose.Note dla Javy do tworzenia nowych dokumentów OneNote?
A1: Tak, Aspose.Note dla Javy zapewnia pełne wsparcie do tworzenia, odczytywania i manipulowania dokumentami OneNote programowo.

### Q2: Czy Aspose.Note dla Javy jest kompatybilny z różnymi wersjami plików OneNote?
A2: Tak, Aspose.Note dla Javy obsługuje różne wersje plików Microsoft OneNote, zapewniając kompatybilność w różnych środowiskach.

### Q3: Czy mogę dostosować format wyjściowy przy eksportowaniu dokumentów OneNote?
A3: Oczywiście, Aspose.Note dla Javy oferuje elastyczność przy eksportowaniu dokumentów OneNote do różnych formatów, takich jak PDF, HTML i obrazy, z opcjami dostosowania.

### Q4: Czy Aspose.Note dla Javy wymaga licencji do użytku komercyjnego?
A4: Tak, do komercyjnego użycia Aspose.Note dla Javy wymagana jest ważna licencja. Licencję można uzyskać na stronie Aspose.

### Q5: Gdzie mogę uzyskać pomoc, jeśli napotkam problemy lub będę miał pytania dotyczące Aspose.Note dla Javy?
A5: W celu uzyskania wsparcia i pomocy możesz odwiedzić forum Aspose.Note **[tutaj](https://forum.aspose.com/c/note/28)**, gdzie możesz zadawać pytania, dzielić się doświadczeniami i współpracować z innymi użytkownikami oraz ekspertami.

---

**Ostatnia aktualizacja:** 2026-01-10  
**Testowano z:** Aspose.Note for Java 23.12 (najnowsza w momencie pisania)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}