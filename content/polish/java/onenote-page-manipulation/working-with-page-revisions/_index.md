---
title: Praca z wersjami stron w programie OneNote — Aspose.Note
linktitle: Praca z wersjami stron w programie OneNote — Aspose.Note
second_title: Aspose.Note API Java
description: Dowiedz się, jak zarządzać wersjami stron w dokumentach OneNote za pomocą Aspose.Note dla Java. Zawiera przewodnik krok po kroku dotyczący skutecznego śledzenia wersji i współpracy.
type: docs
weight: 21
url: /pl/java/onenote-page-manipulation/working-with-page-revisions/
---
## Wstęp

OneNote to potężne narzędzie do organizowania notatek i zarządzania nimi, ale czasami trzeba pracować z wersjami, aby śledzić zmiany i efektywnie współpracować. Dzięki Aspose.Note dla Java możesz łatwo programowo zarządzać wersjami stron w dokumentach OneNote. Ten samouczek przeprowadzi Cię przez proces krok po kroku.

## Warunki wstępne

Zanim zaczniesz, upewnij się, że masz następujące elementy:

### Środowisko programistyczne Java

Upewnij się, że w systemie jest zainstalowany zestaw Java Development Kit (JDK).

### Aspose.Note dla biblioteki Java

Pobierz i zainstaluj bibliotekę Aspose.Note dla Java z[Tutaj](https://releases.aspose.com/note/java/).

### Dokument OneNota

Przygotuj przykładowy dokument programu OneNote do celów testowych.

## Importuj pakiety

W swoim projekcie Java zaimportuj niezbędne pakiety do pracy z Aspose.Note for Java.

```java
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.RevisionSummary;
import java.io.IOException;
import java.util.Calendar;
```

Dla lepszego zrozumienia podzielmy podany przykład na wiele kroków.

## Krok 1: Załaduj dokument OneNote

Najpierw załaduj dokument OneNote i uzyskaj pierwszą stronę podrzędną.

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
Page page = document.getFirstChild();
```

## Krok 2: Przeczytaj podsumowanie wersji strony

Przeczytaj podsumowanie wersji treści strony.

```java
RevisionSummary pageRevisionInfo = page.getPageContentRevisionSummary();
System.out.println(String.format("Author:\t%s\nModified:\t%s",
        pageRevisionInfo.getAuthorMostRecent(),
        pageRevisionInfo.getLastModifiedTime().toString()));
```

## Krok 3: Zaktualizuj podsumowanie wersji strony

Zaktualizuj podsumowanie wersji strony, podając nowego autora i datę modyfikacji.

```java
pageRevisionInfo.setAuthorMostRecent("New Author");
Calendar modifiedDate = Calendar.getInstance();
pageRevisionInfo.setLastModifiedTime(modifiedDate.getTime());
document.save(dataDir + "WorkingWithPageRevisions_out.one");
```

## Wniosek

Programowe zarządzanie wersjami stron w dokumentach OneNote można uprościć za pomocą Aspose.Note dla Java. Wykonując kroki opisane w tym samouczku, możesz efektywnie pracować z wersjami stron, aby śledzić zmiany i bezproblemowo współpracować.

## Często zadawane pytania

### P1: Czy mogę używać Aspose.Note dla Java z innymi bibliotekami Java?

O: Tak, Aspose.Note for Java można zintegrować z innymi bibliotekami Java w celu zwiększenia funkcjonalności.

### P2: Czy Aspose.Note dla Java obsługuje wszystkie wersje dokumentów OneNote?

Odp.: Aspose.Note for Java obsługuje różne wersje dokumentów OneNote, w tym starsze wersje.

### P3: Czy Aspose.Note dla Java nadaje się do aplikacji na poziomie przedsiębiorstwa?

O: Oczywiście, Aspose.Note dla Java został zaprojektowany, aby zaspokoić potrzeby aplikacji na poziomie korporacyjnym, oferując solidne funkcje i skalowalność.

### P4: Czy mogę dostosować wersje strony za pomocą Aspose.Note dla Java?

O: Tak, możesz dostosować wersje strony zgodnie ze swoimi wymaganiami, używając Aspose.Note dla Java.

### P5: Gdzie mogę uzyskać pomoc dotyczącą Aspose.Note dla Java?

 Odp.: Możesz uzyskać wsparcie dla Aspose.Note dla Java z[Forum Aspose.Note](https://forum.aspose.com/c/note/28).