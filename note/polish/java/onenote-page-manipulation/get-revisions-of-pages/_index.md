---
title: Uzyskaj wersje stron w programie OneNote — Aspose.Note
linktitle: Uzyskaj wersje stron w programie OneNote — Aspose.Note
second_title: Aspose.Note API Java
description: Dowiedz się, jak pobierać wersje stron w dokumentach OneNote przy użyciu Aspose.Note Java. Zintegruj to z aplikacjami Java, aby efektywnie zarządzać dokumentami.
type: docs
weight: 15
url: /pl/java/onenote-page-manipulation/get-revisions-of-pages/
---
## Wstęp

tym samouczku zagłębimy się w możliwości Aspose.Note dla Java, potężnej biblioteki, która umożliwia płynną pracę z plikami Microsoft OneNote w aplikacjach Java. W szczególności skupimy się na sposobie pobierania wersji stron w dokumencie programu OneNote. Pod koniec tego przewodnika będziesz wyposażony w wiedzę niezbędną do skutecznego wyodrębniania wersji stron, w tym szczegółów, takich jak czas ostatniej modyfikacji, czas utworzenia, tytuł, poziom i autor.

## Warunki wstępne

Zanim zagłębisz się w ten samouczek, upewnij się, że masz skonfigurowane następujące wymagania wstępne:

### Zainstalowany zestaw programistyczny Java (JDK).

Upewnij się, że masz zainstalowany zestaw Java Development Kit w swoim systemie. Można go pobrać i zainstalować ze strony internetowej Oracle lub użyć menedżera pakietów, jeśli korzystasz z systemu opartego na systemie Unix.

### Aspose.Note dla biblioteki Java

 Pobierz i zainstaluj bibliotekę Aspose.Note for Java ze strony internetowej. Możesz znaleźć link do pobrania[Tutaj](https://releases.aspose.com/note/java/) . Postępuj zgodnie z instrukcjami instalacji podanymi w dokumentacji[Tutaj](https://reference.aspose.com/note/java/).

## Importuj pakiety

Aby rozpocząć, zaimportuj niezbędne pakiety do swojego projektu Java. Pakiety te pozwolą Ci wykorzystać funkcjonalność Aspose.Note dla Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

Podzielmy teraz dostarczony przykładowy kod na wiele kroków, aby zrozumieć każdy komponent i jego funkcjonalność.

## Krok 1: Ustaw katalog dokumentów

Zdefiniuj katalog, w którym znajduje się dokument programu OneNote.

```java
String dataDir = "Your Document Directory";
```

## Krok 2: Załaduj dokument

Załaduj dokument OneNote do Aspose.Note.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## Krok 3: Zdobądź pierwszą stronę

Pobierz pierwszą stronę z dokumentu.

```java
Page firstPage = doc.getFirstChild();
```

## Krok 4: Pobierz wersje strony

Uzyskaj historię zmian strony.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## Krok 5: Przeglądanie wersji strony

Przeglądaj listę wersji stron i pobieraj istotne informacje.

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

## Wniosek

W tym samouczku omówiliśmy, jak pobrać wersje stron w dokumencie OneNote za pomocą Aspose.Note dla Java. Postępując zgodnie ze szczegółowym przewodnikiem i korzystając z dostarczonego przykładowego kodu, możesz łatwo zintegrować tę funkcjonalność z aplikacjami Java, umożliwiając wydajne zarządzanie plikami OneNote.

## Często zadawane pytania

### P1: Czy mogę używać Aspose.Note dla Java do tworzenia nowych dokumentów OneNote?

O1: Tak, Aspose.Note dla Java zapewnia kompleksową obsługę programowego tworzenia, czytania i manipulowania dokumentami OneNote.

### P2: Czy Aspose.Note dla Java jest kompatybilny z różnymi wersjami plików OneNote?

Odpowiedź 2: Tak, Aspose.Note dla Java obsługuje różne wersje plików Microsoft OneNote, zapewniając kompatybilność w różnych środowiskach.

### P3: Czy mogę dostosować format wyjściowy podczas eksportowania dokumentów programu OneNote?

O3: Oczywiście, Aspose.Note dla Java oferuje elastyczność w eksportowaniu dokumentów OneNote do różnych formatów, takich jak PDF, HTML i obrazy, z opcjami dostosowywania.

### P4: Czy Aspose.Note dla Java wymaga licencji do użytku komercyjnego?

O4: Tak, do komercyjnego wykorzystania Aspose.Note dla Java wymagana jest ważna licencja. Licencję można uzyskać ze strony internetowej Aspose.

### P5: Gdzie mogę szukać pomocy, jeśli napotkam problemy lub mam pytania dotyczące Aspose.Note for Java?

 O5: Aby uzyskać wsparcie i pomoc, możesz odwiedzić forum Aspose.Note[Tutaj](https://forum.aspose.com/c/note/28)gdzie możesz zadawać pytania, dzielić się doświadczeniami i kontaktować się z innymi użytkownikami i ekspertami.