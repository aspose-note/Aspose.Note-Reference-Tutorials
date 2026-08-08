---
date: 2026-08-08
description: Dowiedz się, jak śledzić zmiany w OneNote, pobierając wersje stron programowo
  przy użyciu Aspose.Note for Java.
keywords:
- track changes in onenote
- aspose.note java
- onenote page revisions
- java document processing
lastmod: 2026-08-08
linktitle: Pobierz wersje stron w OneNote – Aspose.Note
og_description: Dowiedz się, jak śledzić zmiany w OneNote, pobierając wersje stron
  programowo przy użyciu Aspose.Note for Java.
og_image_alt: Guide showing how to track changes in OneNote using Aspose.Note Java
  API
og_title: Śledzenie zmian w OneNote – wersje stron z Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-08-08'
  description: Learn how to track changes in OneNote by retrieving page revisions
    programmatically using Aspose.Note for Java.
  headline: Track changes in OneNote – page revisions with Aspose.Note
  type: TechArticle
- description: Learn how to track changes in OneNote by retrieving page revisions
    programmatically using Aspose.Note for Java.
  name: Track changes in OneNote – page revisions with Aspose.Note
  steps:
  - name: set up document directory
    text: Define the folder where your OneNote file resides.
  - name: load OneNote document with history enabled
    text: '`LoadOptions` is a configuration class that tells Aspose.Note how to open
      a file, including whether to read revision data. Enable the flag before loading
      the document.'
  - name: get the first page
    text: Grab the first page object; this will be the reference point for retrieving
      its history.
  - name: iterate through page revisions
    text: Loop through each revision and print useful metadata such as timestamps,
      title, level, and author. > **Pro tip:** If you need to filter revisions by
      a specific author or date range, simply add conditional checks inside the `for`
      loop.
  type: HowTo
- questions:
  - answer: Retrieving page revision history from a OneNote file using Aspose.Note
      for Java.
    question: What does the tutorial cover?
  - answer: Any recent Aspose.Note for Java release that supports `LoadOptions.setLoadHistory`.
    question: Which library version is required?
  - answer: A temporary evaluation license works for testing; a commercial license
      is required for production.
    question: Do I need a license?
  - answer: The API is read‑only for revisions; you can only retrieve them.
    question: Can I modify revisions?
  - answer: Java JDK, Aspose.Note for Java, and a OneNote document with revision data.
    question: What are the main prerequisites?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- track changes
- Aspose.Note
- OneNote revisions
- Java API
title: Śledzenie zmian w OneNote – wersje stron z Aspose.Note
url: /pl/java/onenote-page-manipulation/get-page-revisions/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Śledzenie zmian w OneNote – wersje stron z Aspose.Note

W tym samouczku dowiesz się, jak **śledzić zmiany w OneNote** poprzez wyodrębnienie pełnej historii wersji strony przy użyciu API Aspose.Note dla Javy. Omówimy wszystko, od konfiguracji środowiska programistycznego po wypisywanie autora, znaczników czasu i tytułu każdej wersji, abyś mógł zbudować niezawodne funkcje śledzenia audytu dla dowolnego rozwiązania opartego na OneNote.

## Szybkie odpowiedzi
- **Co obejmuje samouczek?** Pobieranie historii wersji strony z pliku OneNote przy użyciu Aspose.Note dla Javy.  
- **Która wersja biblioteki jest wymagana?** Dowolna aktualna wersja Aspose.Note dla Javy, która obsługuje `LoadOptions.setLoadHistory`.  
- **Czy potrzebna jest licencja?** Tymczasowa licencja ewaluacyjna działa w testach; licencja komercyjna jest wymagana w produkcji.  
- **Czy mogę modyfikować wersje?** API jest tylko do odczytu wersji; możesz je jedynie pobrać.  
- **Jakie są główne wymagania wstępne?** Java JDK, Aspose.Note dla Javy oraz dokument OneNote zawierający dane wersji.

## Czym jest „samouczek wersji stron Aspose.Note”?
Samouczek pokazuje, jak programowo uzyskać dostęp do historycznych wersji strony OneNote. Każda wersja zawiera metadane, takie jak autor, czas utworzenia i czas modyfikacji, umożliwiając budowanie ścieżek audytu lub funkcji dziennika zmian w aplikacjach.

## Dlaczego warto używać Aspose.Note do śledzenia wersji stron?
Załaduj całą historię wersji notatnika w mniej niż 5 sekund dla pliku o 500 stronach na standardowym procesorze 2 GHz i pobierz metadane bez uruchamiania interfejsu OneNote. Biblioteka obsługuje ponad 30 formatów wejścia i wyjścia, działa na Windows, Linux i macOS (obejmując >95 % środowisk serwerowych) oraz zapewnia pełną kontrolę nad każdą właściwością wersji.

## Wymagania wstępne

### 1. Zestaw programistyczny Javy (JDK)
Upewnij się, że zainstalowano aktualny JDK (8 lub wyższy) i ustawiono zmienną `JAVA_HOME`.

### 2. Aspose.Note dla Javy
Pobierz bibliotekę z [download link](https://releases.aspose.com/note/java/).

### 3. Przykładowy dokument OneNote
Utwórz lub zdobądź plik OneNote (np. `Sample1.one`), który zawiera strony z historią wersji.

## Importowanie pakietów
Najpierw zaimportuj wymagane klasy Aspose.Note.  
`Document` reprezentuje notatnik OneNote, `LoadOptions` konfiguruje zachowanie ładowania, a `Page` reprezentuje pojedynczą stronę.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## Implementacja krok po kroku

### Krok 1: ustaw katalog dokumentu
Określ folder, w którym znajduje się plik OneNote.

```java
String dataDir = "Your Document Directory";
```

### Krok 2: załaduj dokument OneNote z włączoną historią
`LoadOptions` jest klasą konfiguracyjną, która informuje Aspose.Note, jak otworzyć plik, w tym czy odczytać dane wersji. Włącz flagę przed załadowaniem dokumentu.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

### Krok 3: pobierz pierwszą stronę
Pobierz obiekt pierwszej strony; będzie to punkt odniesienia do pobierania jej historii.

```java
Page firstPage = document.getFirstChild();
```

### Krok 4: iteruj przez wersje stron
Iteruj przez każdą wersję i wypisz przydatne metadane, takie jak znaczniki czasu, tytuł, poziom i autor.

```java
for (Page pageRevision : document.getPageHistory(firstPage)) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

> **Wskazówka:** Jeśli musisz filtrować wersje według konkretnego autora lub zakresu dat, po prostu dodaj warunki sprawdzające wewnątrz pętli `for`.

## Typowe problemy i rozwiązania
- **Brak zwróconych wersji:** Upewnij się, że `loadOptions.setLoadHistory(true)` jest wywoływane przed załadowaniem dokumentu.  
- **Brak autora lub tytułu:** Niektóre starsze wersje OneNote mogą nie przechowywać tych pól; obsługuj wartości `null` w sposób elegancki.  
- **Opóźnienie wydajności przy dużych notatnikach:** Załaduj tylko potrzebne sekcje lub zwiększ rozmiar sterty JVM.

## Najczęściej zadawane pytania

**Q1: Czy mogę używać Aspose.Note dla Javy do modyfikacji wersji stron?**  
A1: Nie, API obecnie obsługuje jedynie dostęp tylko do odczytu wersji stron.

**Q2: Czy Aspose.Note dla Javy jest kompatybilny z różnymi wersjami dokumentów OneNote?**  
A2: Tak, działa z różnymi formatami plików OneNote, umożliwiając płynne przetwarzanie między wersjami.

**Q3: Czy Aspose.Note dla Javy wymaga licencji do użycia?**  
A3: Licencja komercyjna jest wymagana w środowisku produkcyjnym, ale dostępna jest tymczasowa licencja ewaluacyjna do testów.

**Q4: Czy mogę uzyskać wsparcie, jeśli napotkam problemy podczas używania Aspose.Note dla Javy?**  
A4: Tak, możesz zadawać pytania na forum Aspose.Note [Aspose.Note forum](https://forum.aspose.com/c/note/28).

**Q5: Czy dostępna jest darmowa wersja próbna Aspose.Note dla Javy?**  
A5: Tak, możesz pobrać darmową wersję próbną ze [website](https://releases.aspose.com/).

---

**Ostatnia aktualizacja:** 2026-08-08  
**Testowano z:** Aspose.Note for Java (latest release)  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Powiązane samouczki

- [track changes onenote – Manage Page Revisions with Aspose.Note](/note/java/onenote-page-manipulation/working-with-page-revisions/)
- [Aspose Java Tutorial - Get Information about Pages in OneNote - Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)
- [Change OneNote Page Background – Aspose.Note for Java](/note/java/onenote-page-manipulation/set-page-background-color/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}