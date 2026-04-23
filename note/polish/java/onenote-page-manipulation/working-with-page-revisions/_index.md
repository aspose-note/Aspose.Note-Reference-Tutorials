---
date: 2026-01-15
description: Dowiedz się, jak śledzić zmiany w OneNote i zarządzać wersjami stron
  w dokumentach OneNote przy użyciu Aspose.Note dla Javy. Zawiera przykład podsumowania
  wersji oraz instrukcję modyfikacji daty wersji.
linktitle: Working with Page Revisions in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Śledzenie zmian w OneNote – zarządzaj wersjami stron przy użyciu Aspose.Note
url: /pl/java/onenote-page-manipulation/working-with-page-revisions/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Praca z rewizjami stron w OneNote - Aspose.Note

## Wprowadzenie

OneNote jest potężnym narzędziem do organizowania notatek, a gdy potrzebujesz **track changes onenote**, zarządzanie rewizjami stron staje się niezbędne dla efektywnej współpracy. Dzięki Aspose.Note for Java możesz programowo obsługiwać rewizje, zobaczyć, kto edytował stronę, a nawet dostosować znaczniki czasu. Ten samouczek przeprowadzi Cię przez każdy krok, od wczytania dokumentu po aktualizację podsumowania rewizji.

## Szybkie odpowiedzi
- **Co oznacza „track changes onenote”?** Odnosi się do monitorowania, kto edytował stronę OneNote i kiedy.
- **Jakiej biblioteki wymaga się?** Aspose.Note for Java.
- **Czy mogę zmienić autora lub datę rewizji?** Tak, przy użyciu RevisionSummary API (`modify revision date`).
- **Czy potrzebuję pliku OneNote wcześniej?** Tak, wymagany jest przykładowy plik `.one`.
- **Czy licencja jest wymagana w produkcji?** Wymagana jest ważna licencja Aspose.Note do użytku komercyjnego.

## Czym jest przykład podsumowania rewizji?
*revision summary* dostarcza metadane o najnowszych zmianach na stronie — nazwę autora, czas ostatniej modyfikacji i inne szczegóły. W tym przewodniku pobierzemy i wyświetlimy te informacje, a następnie pokażemy, jak **modify revision date**.

## Dlaczego śledzić zmiany onenote przy użyciu Aspose.Note?
- **Collaboration:** Szybko zobacz, kto wprowadził najnowsze zmiany.
- **Auditing:** Zachowaj wiarygodną historię zmian dla zgodności.
- **Automation:** Zintegruj obsługę rewizji z usługami back‑end lub narzędziami migracyjnymi.

## Wymagania wstępne

### Java Development Environment
Upewnij się, że masz zainstalowany Java Development Kit (JDK) w swoim systemie.

### Aspose.Note for Java Library
Pobierz i zainstaluj bibliotekę Aspose.Note for Java z [tutaj](https://releases.aspose.com/note/java/).

### OneNote Document
Miej gotowy przykładowy dokument OneNote do celów testowych.

## Import Packages

W swoim projekcie Java zaimportuj niezbędne pakiety do pracy z Aspose.Note for Java.

```java
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.RevisionSummary;
import java.io.IOException;
import java.util.Calendar;
```

Rozbijmy podany przykład na kilka kroków, aby uzyskać jasne zrozumienie.

## Krok 1: Wczytaj dokument OneNote

Najpierw wczytaj dokument OneNote i pobierz pierwszą podstronę.

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
Page page = document.getFirstChild();
```

## Krok 2: Odczytaj podsumowanie rewizji strony

Odczytaj podsumowanie rewizji treści dla strony. To jest **revision summary example**, które pokazuje, kto ostatnio edytował stronę.

```java
RevisionSummary pageRevisionInfo = page.getPageContentRevisionSummary();
System.out.println(String.format("Author:\t%s\nModified:\t%s",
        pageRevisionInfo.getAuthorMostRecent(),
        pageRevisionInfo.getLastModifiedTime().toString()));
```

## Krok 3: Zaktualizuj podsumowanie rewizji strony

Zaktualizuj podsumowanie rewizji strony, podając nowego autora i nową datę modyfikacji. To pokazuje, jak programowo **modify revision date**.

```java
pageRevisionInfo.setAuthorMostRecent("New Author");
Calendar modifiedDate = Calendar.getInstance();
pageRevisionInfo.setLastModifiedTime(modifiedDate.getTime());
document.save(dataDir + "WorkingWithPageRevisions_out.one");
```

## Podsumowanie

Zarządzanie rewizjami stron w dokumentach OneNote programowo może być uproszczone dzięki Aspose.Note for Java. Postępując zgodnie z krokami opisanymi w tym samouczku, możesz skutecznie **track changes onenote**, przeglądać szczegóły rewizji i nawet **modify revision date**, aby dopasować je do swojego przepływu pracy.

## FAQ

### Q1: Czy mogę używać Aspose.Note for Java z innymi bibliotekami Java?
**A:** Tak, Aspose.Note for Java może być zintegrowany z innymi bibliotekami Java, aby zwiększyć funkcjonalność.

### Q2: Czy Aspose.Note for Java obsługuje wszystkie wersje dokumentów OneNote?
**A:** Aspose.Note for Java obsługuje różne wersje dokumentów OneNote, w tym starsze wersje.

### Q3: Czy Aspose.Note for Java jest odpowiedni dla aplikacji na poziomie przedsiębiorstwa?
**A:** Zdecydowanie, Aspose.Note for Java jest zaprojektowany, aby spełniać potrzeby aplikacji na poziomie przedsiębiorstwa, oferując solidne funkcje i skalowalność.

### Q4: Czy mogę dostosować rewizje stron przy użyciu Aspose.Note for Java?
**A:** Tak, możesz dostosować rewizje stron zgodnie z wymaganiami, używając Aspose.Note for Java.

### Q5: Gdzie mogę uzyskać wsparcie dla Aspose.Note for Java?
**A:** Wsparcie dla Aspose.Note for Java możesz uzyskać na [forum Aspose.Note](https://forum.aspose.com/c/note/28).

---

**Last Updated:** 2026-01-15  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}