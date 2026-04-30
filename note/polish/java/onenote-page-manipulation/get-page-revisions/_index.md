---
date: 2026-01-10
description: Poznaj samouczek aspose.note dotyczący wersji stron w Javie – pobieraj
  wersje stron OneNote programowo przy użyciu Aspose.Note. Postępuj zgodnie z naszym
  przewodnikiem krok po kroku.
linktitle: Get Page Revisions in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: aspose.note – samouczek wersji stron – Pobieranie wersji stron w OneNote
url: /pl/java/onenote-page-manipulation/get-page-revisions/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Pobieranie wersji stron w OneNote - Aspose.Note

OneNote jest potężną platformą do tworzenia notatek, a gdy potrzebujesz audytować zmiany, **aspose.note page revisions tutorial** pokazuje dokładnie, jak pobrać historię wersji przy użyciu kilku linii kodu Java. W tym przewodniku przeprowadzimy Cię przez wszystko, czego potrzebujesz — od konfiguracji środowiska po wypisanie szczegółów każdej wersji — abyś mógł łatwo śledzić edycje, wkład autorów i znaczniki czasu.

## Szybkie odpowiedzi
- **Co obejmuje tutorial?** Pobieranie historii wersji stron z pliku OneNote przy użyciu Aspose.Note dla Javy.  
- **Jakiej wersji biblioteki wymaga?** Dowolna aktualna wersja Aspose.Note dla Javy, która obsługuje `LoadOptions.setLoadHistory`.  
- **Czy potrzebna jest licencja?** Tymczasowa licencja ewaluacyjna działa w testach; licencja komercyjna jest wymagana w produkcji.  
- **Czy mogę modyfikować wersje?** API jest tylko do odczytu wersji; możesz je jedynie pobierać.  
- **Jakie są główne wymagania wstępne?** Java JDK, Aspose.Note dla Javy oraz dokument OneNote z danymi wersji.

## Co to jest „aspose.note page revisions tutorial”?
Tutorial pokazuje, jak programowo uzyskać dostęp do historycznych wersji strony OneNote. Każda wersja zawiera metadane, takie jak autor, czas utworzenia i czas modyfikacji, co umożliwia budowanie ścieżek audytu lub funkcji dziennika zmian w aplikacjach.

## Dlaczego warto używać Aspose.Note do śledzenia wersji stron?
- **Brak zależności od UI** – działa w pełni w kodzie, idealny dla usług backendowych.  
- **Cross‑platform** – Java działa na Windows, Linux i macOS.  
- **Pełna kontrola** – pobiera wszystkie właściwości wersji bez ręcznego otwierania OneNote.  
- **Wydajność** – ładowanie historii jest zoptymalizowane, więc nawet duże notatniki są przetwarzane szybko.

## Wymagania wstępne

### 1. Java Development Kit (JDK)
Upewnij się, że zainstalowano aktualny JDK (8 lub wyższy) i ustawiono zmienną `JAVA_HOME`.

### 2. Aspose.Note dla Javy
Pobierz bibliotekę z [download link](https://releases.aspose.com/note/java/).

### 3. Przykładowy dokument OneNote
Utwórz lub zdobądź plik OneNote (np. `Sample1.one`), który zawiera strony z historią wersji.

## Importowanie pakietów
Najpierw zaimportuj wymagane klasy Aspose.Note.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## Implementacja krok po kroku

### Krok 1: Ustaw katalog dokumentu
Zdefiniuj folder, w którym znajduje się Twój plik OneNote.

```java
String dataDir = "Your Document Directory";
```

### Krok 2: Załaduj dokument OneNote z włączoną historią
Włącz flagę `LoadOptions`, aby pobrać dane wersji.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

### Krok 3: Pobierz pierwszą stronę
Pobierz obiekt pierwszej strony; będzie to punkt odniesienia do pobierania jej historii.

```java
Page firstPage = document.getFirstChild();
```

### Krok 4: Iteruj przez wersje stron
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

> **Pro tip:** Jeśli potrzebujesz filtrować wersje według konkretnego autora lub zakresu dat, po prostu dodaj warunki sprawdzające wewnątrz pętli `for`.

## Typowe problemy i rozwiązania
- **Brak zwróconych wersji:** Upewnij się, że `loadOptions.setLoadHistory(true)` jest wywoływane przed załadowaniem dokumentu.  
- **Autor lub tytuł null:** Niektóre starsze wersje OneNote mogą nie przechowywać tych pól; obsługuj wartości `null` w sposób bezpieczny.  
- **Opóźnienia wydajności przy dużych notatnikach:** Ładuj tylko potrzebne sekcje lub zwiększ rozmiar sterty JVM.

## Najczęściej zadawane pytania

**Q1: Czy mogę używać Aspose.Note dla Javy do modyfikowania wersji stron?**  
A1: Nie, API obecnie obsługuje tylko dostęp do wersji w trybie tylko do odczytu.

**Q2: Czy Aspose.Note dla Javy jest kompatybilny z różnymi wersjami dokumentów OneNote?**  
A2: Tak, działa z różnymi formatami plików OneNote, umożliwiając płynne przetwarzanie między wersjami.

**Q3: Czy Aspose.Note dla Javy wymaga licencji do użycia?**  
A3: Licencja komercyjna jest wymagana w środowisku produkcyjnym, ale dostępna jest tymczasowa licencja ewaluacyjna do testów.

**Q4: Czy mogę uzyskać wsparcie, jeśli napotkam problemy podczas używania Aspose.Note dla Javy?**  
A4: Tak, możesz zadawać pytania na forum Aspose.Note [tutaj](https://forum.aspose.com/c/note/28).

**Q5: Czy dostępna jest darmowa wersja próbna Aspose.Note dla Javy?**  
A5: Tak, możesz pobrać darmową wersję próbną ze [strony internetowej](https://releases.aspose.com/).

---

**Ostatnia aktualizacja:** 2026-01-10  
**Testowano z:** Aspose.Note for Java (latest release)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}