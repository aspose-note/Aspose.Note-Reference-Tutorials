---
title: Prześlij bieżącą wersję strony w programie OneNote — Aspose.Note
linktitle: Prześlij bieżącą wersję strony w programie OneNote — Aspose.Note
second_title: Aspose.Note API Java
description: Zachowaj świeżość zawartości programu OneNote! Dowiedz się, jak aktualizować historię strony i zarządzać wersjami. Zawiera przewodnik krok po kroku i kod. #OneNote #Java #Aspose
type: docs
weight: 18
url: /pl/java/onenote-page-manipulation/push-current-page-version/
---
## Wstęp

W tym samouczku omówimy, jak wykorzystać Aspose.Note dla języka Java do przesyłania bieżącej wersji strony do programu OneNote. Aspose.Note to potężna biblioteka Java, która umożliwia programistom programową pracę z dokumentami Microsoft OneNote, umożliwiając różne operacje, takie jak tworzenie, manipulowanie i konwertowanie plików OneNote.

## Warunki wstępne

Zanim zaczniemy, upewnij się, że masz następujące wymagania wstępne:
1. Podstawowa znajomość języka programowania Java.
2. Zainstalowano zestaw Java Development Kit (JDK) w systemie.
3.  Aspose.Note dla biblioteki Java. Można go pobrać z[Tutaj](https://releases.aspose.com/note/java/).
4. Przykładowy dokument programu OneNote do pracy.

## Importuj pakiety

Najpierw musisz zaimportować niezbędne pakiety do swojego projektu Java, aby móc korzystać z funkcjonalności Aspose.Note.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## Krok 1: Załaduj dokument OneNote

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
```

 Tutaj,`dataDir` powinien wskazywać katalog, w którym znajduje się dokument OneNote. Zastępować`"Sample1.one"` z nazwą pliku OneNote.

## Krok 2: Pobierz bieżącą stronę i jej historię

```java
Page page = document.getFirstChild();
PageHistory pageHistory = document.getPageHistory(page);
```

 Pobieramy pierwszą stronę dokumentu za pomocą`getFirstChild()` a następnie uzyskaj jego historię za pomocą`getPageHistory()`.

## Krok 3: Prześlij bieżącą wersję strony

```java
pageHistory.addItem(page.deepClone());
```

Tutaj dodajemy aktualną wersję strony do jej historii klonując ją i dodając jako nowy element.

## Krok 4: Zapisz dokument

```java
document.save(dataDir + "PushCurrentPageVersion_out.one");
```

Na koniec zapisujemy zmodyfikowany dokument ze zaktualizowaną historią stron.

## Wniosek

W tym samouczku nauczyliśmy się, jak przesyłać bieżącą wersję strony do programu OneNote przy użyciu programu Aspose.Note dla języka Java. Wykonując te kroki, możesz efektywnie zarządzać wersjonowaniem dokumentów programu OneNote w sposób programowy.

## Często zadawane pytania

### P1: Czy mogę używać Aspose.Note dla Java do pracy z zaszyfrowanymi plikami OneNote?

Odpowiedź 1: Tak, Aspose.Note dla Java obsługuje pracę zarówno z zaszyfrowanymi, jak i niezaszyfrowanymi plikami OneNote.

### P2: Czy Aspose.Note dla Java jest kompatybilny z najnowszą wersją OneNote?

O2: Aspose.Note for Java stara się zachować kompatybilność z najnowszymi wersjami dokumentów OneNote.

### P3: Czy mogę manipulować tekstem i obrazami w dokumentach OneNote przy użyciu Aspose.Note dla Java?

Odpowiedź 3: Oczywiście, Aspose.Note dla Java zapewnia rozbudowane funkcje do manipulowania tekstem, obrazami i innymi elementami w plikach OneNote.

### P4: Czy Aspose.Note dla Java obsługuje konwersję plików OneNote do innych formatów?

O4: Tak, Aspose.Note dla Java obsługuje konwersję plików OneNote do różnych formatów, takich jak PDF, HTML i formaty obrazów.

### P5: Gdzie mogę uzyskać pomoc dotyczącą Aspose.Note dla Java, jeśli napotkam jakiekolwiek problemy?

 A5: Możesz odwiedzić[Forum Aspose.Note](https://forum.aspose.com/c/note/28) aby zwrócić się o pomoc do społeczności lub skontaktować się bezpośrednio z pomocą techniczną Aspose.