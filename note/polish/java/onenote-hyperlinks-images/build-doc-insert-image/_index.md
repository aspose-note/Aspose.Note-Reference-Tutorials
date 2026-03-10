---
date: 2025-12-20
description: Dowiedz się, jak dodać obraz do OneNote przy użyciu Aspose.Note dla Javy.
  Przewodnik krok po kroku, jak tworzyć dokumenty OneNote i wstawiać obrazy programowo.
linktitle: How to add picture to OneNote using Java – Build Document and Insert Image
second_title: Aspose.Note Java API
title: Jak dodać obraz do OneNote przy użyciu Javy – Utwórz dokument i wstaw obraz
url: /pl/java/onenote-hyperlinks-images/build-doc-insert-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak dodać obraz do OneNote przy użyciu Java – Tworzenie dokumentu i wstawianie obrazu

## Wprowadzenie

W tym samouczku dowiesz się **jak dodać obraz do OneNote** przy użyciu Aspose.Note Java API. Przeprowadzimy Cię przez tworzenie dokumentu OneNote od podstaw, wstawianie obrazu i zapisywanie wyniku jako PDF. Niezależnie od tego, czy tworzysz narzędzie raportujące, automatyzujesz notowanie, czy po prostu potrzebujesz programowo osadzać grafiki, ten przewodnik zapewnia jasną, praktyczną ścieżkę.

## Szybkie odpowiedzi
- **Jakiej biblioteki potrzebuję?** Aspose.Note for Java.
- **Czy mogę wstawić dowolny format obrazu?** Obsługiwane są JPEG, PNG, BMP, GIF i inne.
- **Jakie formaty wyjściowe są dostępne?** Możesz zapisać jako OneNote, PDF, XPS, HTML itp.
- **Czy potrzebna jest licencja do produkcji?** Tak, wymagana jest licencja komercyjna do użytku nie‑trial.
- **Czy kod jest wieloplatformowy?** Absolutnie – Java działa na Windows, Linux i macOS.

## Co oznacza „dodawanie obrazu do OneNote”?
Dodanie obrazu do OneNote oznacza programowe osadzenie pliku graficznego na stronie OneNote, tak aby pojawił się obok tekstu, konturów lub innych elementów. API Aspose.Note abstrahuje format pliku OneNote, pozwalając skupić się na treści, a nie na leżącej u podstaw strukturze XML.

## Dlaczego dodawać obraz do OneNote przy użyciu Java?
- **Automatyzacja:** Automatyczne generowanie protokołów spotkań ze zrzutami ekranu.
- **Spójność:** Zapewnienie, że każda strona ma ten sam układ i identyfikację wizualną.
- **Integracja:** Łączenie danych z innych systemów (np. wykresów) bezpośrednio w notatnikach OneNote.
- **Wieloplatformowość:** Java pozwala uruchamiać ten sam kod na dowolnym serwerze lub komputerze stacjonarnym.

## Wymagania wstępne

Zanim zaczniemy, upewnij się, że masz następujące elementy:

1. **Java Development Kit (JDK)** – dowolna aktualna wersja (8 lub nowsza).  
2. **Biblioteka Aspose.Note for Java** – pobierz ją ze [strony internetowej](https://releases.aspose.com/note/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse lub dowolny edytor kompatybilny z Java, którego preferujesz.  

## Importowanie pakietów

Rozpocznij od zaimportowania niezbędnych klas w swoim pliku źródłowym Java:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## Przewodnik krok po kroku

### Krok 1: Utworzenie dokumentu

Utwórz nowy dokument OneNote oraz kontener strony, w którym będzie znajdować się zawartość.

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

### Krok 2: Inicjalizacja konturu (Outline)

*Outline* działa jak kontener dla elementów takich jak tekst i obrazy. Ustawiamy jego przesunięcia na zero, aby zawartość zaczynała się w lewym górnym rogu.

```java
Outline outline = new Outline();
outline.setVerticalOffset(0);
outline.setHorizontalOffset(0);
```

### Krok 3: Załadowanie i wyrównanie obrazu

Załaduj obraz, który chcesz osadzić, i wyrównaj go do prawej strony strony. To jest miejsce, w którym faktycznie **dodajemy obraz do OneNote**.

```java
Image image = new Image(null, dataDir + "Input.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

### Krok 4: Dołączenie obrazu do elementu outline

Umieść obraz wewnątrz `OutlineElement`. Ten krok łączy obiekt wizualny z hierarchią outline dokumentu.

```java
OutlineElement outlineElem = new OutlineElement();
outlineElem.appendChildLast(image);
```

### Krok 5: Zbudowanie struktury dokumentu

Dodaj element outline do outline, następnie dołącz outline do strony i na końcu dodaj stronę do dokumentu.

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

### Krok 6: Zapisanie dokumentu OneNote

Zapisz dokument na dysku. W tym przykładzie eksportujemy do PDF, ale możesz również zapisać jako natywny plik OneNote (`.one`), zmieniając `SaveFormat`.

```java
try {
    doc.save(dataDir + "NewOneNotedocument_out", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Częste problemy i rozwiązania

| Problem | Dlaczego się pojawia | Rozwiązanie |
|-------|----------------|-----|
| **Obraz się nie wyświetla** | Nieprawidłowa ścieżka pliku lub nieobsługiwany format. | Zweryfikuj, że `dataDir` wskazuje na właściwy folder i użyj obsługiwanego typu obrazu (JPEG, PNG itp.). |
| **Dokument zapisany jako pusty PDF** | Nieprawidłowo ustawione przesunięcia outline. | Upewnij się, że wywołano `setVerticalOffset(0)` i `setHorizontalOffset(0)`, lub dostosuj przesunięcia, aby umieścić zawartość w granicach strony. |
| **IOException przy zapisie** | Folder docelowy nie istnieje lub brakuje uprawnień do zapisu. | Utwórz folder wcześniej lub uruchom program z odpowiednimi uprawnieniami. |

## Najczęściej zadawane pytania

**Q1: Gdzie mogę znaleźć dokumentację Aspose.Note dla Java?**  
A1: Dokumentację można znaleźć [tutaj](https://reference.aspose.com/note/java/).

**Q2: Jak pobrać Aspose.Note dla Java?**  
A2: Aspose.Note dla Java można pobrać ze [strony pobierania](https://releases.aspose.com/note/java/).

**Q3: Czy dostępna jest darmowa wersja próbna Aspose.Note dla Java?**  
A3: Tak, darmową wersję próbną można uzyskać na [stronie internetowej](https://releases.aspose.com/).

**Q4: Gdzie mogę uzyskać wsparcie dla Aspose.Note dla Java?**  
A4: Wsparcie można uzyskać, odwiedzając [forum Aspose.Note](https://forum.aspose.com/c/note/28).

**Q5: Czy mogę uzyskać tymczasową licencję dla Aspose.Note dla Java?**  
A5: Tak, tymczasową licencję można zamówić [tutaj](https://purchase.aspose.com/temporary-license/).

---

**Ostatnia aktualizacja:** 2025-12-20  
**Testowano z:** Aspose.Note for Java 24.12 (latest)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}