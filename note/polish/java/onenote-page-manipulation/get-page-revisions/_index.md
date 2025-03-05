---
title: Pobierz wersje strony w programie OneNote — Aspose.Note
linktitle: Pobierz wersje strony w programie OneNote — Aspose.Note
second_title: Aspose.Note API Java
description: Dowiedz się, jak pobrać wersje stron w programie OneNote przy użyciu programu Aspose.Note dla języka Java. Postępuj zgodnie z naszym przewodnikiem krok po kroku, aby skutecznie śledzić zmiany.
type: docs
weight: 14
url: /pl/java/onenote-page-manipulation/get-page-revisions/
---
## Wstęp

OneNote to potężne narzędzie do porządkowania notatek i zarządzania nimi, ale czasami trzeba śledzić zmiany i poprawki wprowadzone na stronach. Dzięki Aspose.Note dla Java możesz łatwo programowo pobierać wersje stron. W tym samouczku przeprowadzimy Cię przez proces uzyskiwania wersji stron w programie OneNote przy użyciu programu Aspose.Note dla języka Java.

## Warunki wstępne

Zanim zaczniemy, upewnij się, że spełnione są następujące wymagania wstępne:

### 1. Zestaw programistyczny Java (JDK)

Upewnij się, że w systemie jest zainstalowany zestaw Java Development Kit (JDK). Możesz pobrać i zainstalować JDK ze strony internetowej Oracle.

### 2. Aspose.Note dla Javy

Pobierz i zainstaluj Aspose.Note dla Java z pliku[link do pobrania](https://releases.aspose.com/note/java/).

### 3. Przykładowy dokument OneNote

Przygotuj przykładowy dokument OneNote (`Sample1.one`) zawierający strony, z których chcesz pobrać wersje.

## Importuj pakiety

Najpierw musisz zaimportować niezbędne pakiety z Aspose.Note dla Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

Podzielmy teraz podany przykład na kilka kroków:

## Krok 1: Skonfiguruj katalog dokumentów

Zdefiniuj ścieżkę katalogu, w którym znajduje się dokument programu OneNote.

```java
String dataDir = "Your Document Directory";
```

## Krok 2: Załaduj dokument OneNote

 Załaduj dokument OneNote za pomocą`LoadOptions` aby włączyć historię ładowania.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

## Krok 3: Zdobądź pierwszą stronę

Pobierz pierwszą stronę z załadowanego dokumentu.

```java
Page firstPage = document.getFirstChild();
```

## Krok 4: Iteruj po wersjach strony

Przeglądaj każdą wersję strony i pobieraj istotne informacje, takie jak czas ostatniej modyfikacji, czas utworzenia, tytuł, poziom i autor.

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

## Wniosek

W tym samouczku nauczyliśmy się, jak pobierać wersje stron w programie OneNote przy użyciu programu Aspose.Note dla języka Java. Wykonując te kroki, możesz efektywnie śledzić zmiany wprowadzane na stronach programu OneNote w sposób programowy.

## Często zadawane pytania

### P1: Czy mogę używać Aspose.Note dla Java do modyfikowania wersji stron?

O1: Nie, Aspose.Note dla Java obsługuje obecnie pobieranie wersji stron, ale nie umożliwia ich modyfikowania.

### P2: Czy Aspose.Note dla Java jest kompatybilny z różnymi wersjami dokumentów OneNote?

Odpowiedź 2: Tak, Aspose.Note dla Java obsługuje różne wersje dokumentów OneNote, umożliwiając płynną pracę z różnymi formatami plików.

### P3: Czy Aspose.Note dla Java wymaga licencji?

O3: Tak, musisz kupić licencję, aby używać Aspose.Note dla Java w projektach komercyjnych. Można jednak również uzyskać licencję tymczasową do celów testowych.

### P4: Czy mogę zwrócić się o pomoc, jeśli napotkam jakiekolwiek problemy podczas korzystania z Aspose.Note dla Java?

 O4: Tak, możesz szukać pomocy na forum Aspose.Note[Tutaj](https://forum.aspose.com/c/note/28).

### P5: Czy dostępna jest bezpłatna wersja próbna Aspose.Note dla Java?

 O5: Tak, możesz uzyskać dostęp do bezpłatnej wersji próbnej Aspose.Note dla Java z poziomu[strona internetowa](https://releases.aspose.com/).