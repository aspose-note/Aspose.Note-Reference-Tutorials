---
date: 2026-03-19
description: Dowiedz się, jak dodać obraz do OneNote przy użyciu Aspose.Note dla Javy.
  Ten przewodnik krok po kroku pokazuje, jak tworzyć dokumenty OneNote, wstawiać obrazy
  do OneNote i zapisywać OneNote jako PDF.
linktitle: How to add picture to OneNote using Java – Build Document and Insert Image
second_title: Aspose.Note Java API
title: Jak dodać obraz do OneNote przy użyciu Javy – Tworzenie dokumentu i wstawianie
  obrazu
url: /pl/java/onenote-hyperlinks-images/build-doc-insert-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak dodać obraz do OneNote przy użyciu Javy – Tworzenie dokumentu i wstawianie obrazu

## Wprowadzenie

W tym samouczku dowiesz się **jak dodać obraz do OneNote** przy użyciu Aspose.Note Java API. Przeprowadzimy Cię przez tworzenie dokumentu OneNote od podstaw, wstawianie obrazu i zapisywanie wyniku jako PDF. Niezależnie od tego, czy tworzysz narzędzie raportujące, automatyzujesz notowanie, czy po prostu potrzebujesz programowo osadzać grafiki, ten przewodnik zapewnia jasną, praktyczną ścieżkę.

## Szybkie odpowiedzi
- **Jakiej biblioteki potrzebuję?** Aspose.Note for Java.  
- **Czy mogę wstawić dowolny format obrazu?** Obsługiwane są JPEG, PNG, BMP, GIF i inne.  
- **Jakie formaty wyjściowe są dostępne?** Możesz zapisać jako OneNote, PDF, XPS, HTML itp.  
- **Czy potrzebna jest licencja do produkcji?** Tak, wymagana jest licencja komercyjna do użytku nie‑testowego.  
- **Czy kod jest wieloplatformowy?** Absolutnie – Java działa na Windows, Linux i macOS.

## Jak dodać obraz do OneNote przy użyciu Javy

Dodanie obrazu do OneNote oznacza programowe osadzenie pliku graficznego na stronie OneNote, tak aby pojawił się obok tekstu, konturów lub innych elementów. API Aspose.Note abstrahuje format pliku OneNote, pozwalając skupić się na treści, a nie na leżącej u podstaw strukturze XML.

### Dlaczego osadzać obraz w OneNote?

- **Automatyzacja:** Automatyczne generowanie protokołów spotkań ze zrzutami ekranu.  
- **Spójność:** Zapewnienie, że każda strona ma ten sam układ i branding.  
- **Integracja:** Łączenie danych z innych systemów (np. wykresów) bezpośrednio w notatnikach OneNote.  
- **Wieloplatformowość:** Java pozwala uruchamiać ten sam kod na dowolnym serwerze lub komputerze.

## Wymagania wstępne

Zanim zaczniemy, upewnij się, że masz następujące elementy:

1. **Java Development Kit (JDK)** – dowolna aktualna wersja (8 lub nowsza).  
2. **Biblioteka Aspose.Note for Java** – pobierz ją ze [strony internetowej](https://releases.aspose.com/note/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse lub dowolny edytor kompatybilny z Javą, który preferujesz.  

## Importowanie pakietów

Zacznij od zaimportowania niezbędnych klas w swoim pliku źródłowym Java:

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

### Krok 1: Przygotowanie dokumentu

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

Załaduj obraz, który chcesz osadzić i wyrównaj go do prawej strony strony. To jest miejsce, w którym faktycznie **dodajemy obraz do OneNote**. Konstruktor `Image` pokazuje, jak **załadować plik obrazu w Javie** w kodzie.

```java
Image image = new Image(null, dataDir + "Input.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

### Krok 4: Dołączenie obrazu do elementu Outline

Umieść obraz wewnątrz `OutlineElement`. Ten krok łączy obiekt wizualny z hierarchią konturu dokumentu i skutecznie **wstawia obraz do OneNote**.

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

Zachowaj dokument na dysku. W tym przykładzie eksportujemy do PDF, co pokazuje, jak **zapisać OneNote jako PDF** lub **przekonwertować OneNote na PDF**. Możesz także zapisać jako natywny plik OneNote (`.one`), zmieniając `SaveFormat`.

```java
try {
    doc.save(dataDir + "NewOneNotedocument_out", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Typowe problemy i rozwiązania

| Problem | Dlaczego się pojawia | Rozwiązanie |
|-------|----------------|-----|
| **Obraz nie wyświetla się** | Nieprawidłowa ścieżka pliku lub nieobsługiwany format. | Zweryfikuj, że `dataDir` wskazuje na właściwy folder i użyj obsługiwanego typu obrazu (JPEG, PNG itp.). |
| **Dokument zapisany jako pusty PDF** | Nieprawidłowo ustawione przesunięcia outline. | Upewnij się, że wywołano `setVerticalOffset(0)` i `setHorizontalOffset(0)`, lub dostosuj przesunięcia, aby umieścić zawartość w granicach strony. |
| **IOException przy zapisie** | Folder docelowy nie istnieje lub brakuje uprawnień do zapisu. | Utwórz folder wcześniej lub uruchom program z odpowiednimi uprawnieniami. |

## Najczęściej zadawane pytania

**P1: Gdzie mogę znaleźć dokumentację Aspose.Note for Java?**  
O1: Dokumentację możesz znaleźć [tutaj](https://reference.aspose.com/note/java/).

**P2: Jak pobrać Aspose.Note for Java?**  
O2: Aspose.Note for Java możesz pobrać ze [strony pobierania](https://releases.aspose.com/note/java/).

**P3: Czy dostępna jest darmowa wersja próbna Aspose.Note for Java?**  
O3: Tak, darmową wersję próbną możesz uzyskać ze [strony internetowej](https://releases.aspose.com/).

**P4: Gdzie mogę uzyskać wsparcie dla Aspose.Note for Java?**  
O4: Wsparcie znajdziesz na [forum Aspose.Note](https://forum.aspose.com/c/note/28).

**P5: Czy mogę uzyskać tymczasową licencję dla Aspose.Note for Java?**  
O5: Tak, tymczasową licencję możesz zamówić [tutaj](https://purchase.aspose.com/temporary-license/).

**P6: Czy mogę użyć tego kodu do **zapisania OneNote jako PDF** na serwerze Linux?**  
O6: Absolutnie. Biblioteka Aspose.Note jest niezależna od platformy, więc ten sam kod działa na Windows, Linux i macOS.

**P7: Czy API obsługuje **osadzanie obrazu w OneNote** z przezroczystymi PNG?**  
O7: Tak, pliki PNG z kanałami alfa są w pełni obsługiwane i zachowują przezroczystość po wstawieniu.

---

**Ostatnia aktualizacja:** 2026-03-19  
**Testowano z:** Aspose.Note for Java 24.12 (najnowsza)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}