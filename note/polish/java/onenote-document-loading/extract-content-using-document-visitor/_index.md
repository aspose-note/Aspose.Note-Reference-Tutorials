---
date: 2025-12-03
description: „Dowiedz się, jak konwertować OneNote na tekst przy użyciu Aspose.Note
  dla Javy. Przewodnik krok po kroku obejmujący wyodrębnianie tekstu, wyodrębnianie
  obrazów oraz odczytywanie plików OneNote.”
language: pl
linktitle: Convert OneNote to Text with Document Visitor – Java
second_title: Aspose.Note Java API
title: Konwertuj OneNote na tekst przy użyciu Document Visitor – Java
url: /java/onenote-document-loading/extract-content-using-document-visitor/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konwertuj OneNote na Tekst przy użyciu Document Visitor – Java

## Wprowadzenie

W tym samouczku dowiesz się **jak konwertować OneNote na tekst** przy użyciu Document Visitor w Aspose.Note for Java. Niezależnie od tego, czy potrzebujesz programowo odczytać pliki OneNote, wyodrębnić czysty tekst, czy wyciągnąć osadzone obrazy, Document Visitor daje precyzyjną kontrolę nad każdym węzłem w dokumencie .one.

## Szybkie odpowiedzi
- **Co oznacza „konwertować OneNote na tekst”?** Oznacza to wyodrębnienie reprezentacji tekstowej (opcjonalnie obrazów) z pliku .one.  
- **Która biblioteka to umożliwia?** Aspose.Note for Java udostępnia API `DocumentVisitor`.  
- **Czy potrzebna jest licencja?** Darmowa wersja próbna wystarczy do oceny; licencja płatna jest wymagana w środowisku produkcyjnym.  
- **Czy mogę także wyodrębniać obrazy?** Tak – zaimplementuj metodę `VisitImageStart`, aby pobrać obrazy.  
- **Jakie są wymagania wstępne?** Java JDK 8+, Aspose.Note for Java JAR oraz plik .one do przetworzenia.

## Co to jest „konwertować OneNote na tekst”?
Konwersja OneNote na tekst oznacza programowe odczytanie pliku OneNote (.one) i pobranie jego treści tekstowej, tytułów oraz innych elementów bez użycia interfejsu OneNote. Jest to przydatne przy indeksowaniu wyszukiwania, raportowaniu lub migracji treści na inne platformy.

## Dlaczego używać Document Visitor do **czytania plików OneNote**?
Document Visitor realizuje wzorzec projektowy Visitor, umożliwiając przejście przez każdy element (strony, kontury, obrazy, fragmenty Rich‑Text itp.) w dokumencie OneNote. W porównaniu z ładowaniem całego dokumentu do pamięci i ręcznym parsowaniem, podejście oparte na odwiedzaniu jest:

* **Efektywne pamięciowo** – przetwarza węzły pojedynczo.  
* **Rozszerzalne** – możesz dodać własną logikę dla dowolnego typu węzła (np. wyodrębniać obrazy).  
* **Precyzyjne** – zachowuje oryginalną hierarchię, dzięki czemu nie pomijasz ukrytych treści.

## Wymagania wstępne

Zanim rozpoczniesz, upewnij się, że masz:

1. **Java Development Kit (JDK) 8 lub nowszy** zainstalowany.  
2. **Bibliotekę Aspose.Note for Java** pobraną ze strony oficjalnej – [pobierz tutaj](https://releases.aspose.com/note/java/).  
3. Dokument **OneNote** (`.one`), który chcesz skonwertować na tekst.  

## Krok 1: Importowanie pakietów

Najpierw zaimportuj klasy potrzebne do pracy z Aspose.Note for Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.DocumentVisitor;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.OutlineGroup;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.Title;
```

## Krok 2: Utworzenie klasy Document Visitor

Utwórz klasę, która rozszerza `DocumentVisitor`. Ten niestandardowy odwiedzający będzie zbierał tekst, liczył węzły i (jeśli chcesz) przechowywał obrazy.

```java
public class ExtractOneNoteContentUsingDocumentvisitor extends DocumentVisitor {
    
    final private StringBuilder mBuilder;
    final private boolean mIsSkipText;
    private int nodecount;

    public ExtractOneNoteContentUsingDocumentvisitor() {
        nodecount = 0;
        mIsSkipText = false;
        mBuilder = new StringBuilder();
    }
    
    // Other methods will be implemented here
}
```

## Krok 3: Implementacja metod odwiedzających  

Tutaj implementujemy wywołania zwrotne dla interesujących nas typów węzłów. Metody zwiększają licznik węzłów oraz, w przypadku `RichText`, dopisują rzeczywisty tekst do naszego `StringBuilder`. Możesz także dodać logikę **wyodrębniania obrazów z OneNote** obsługując `VisitImageStart`.

```java
// Visitor methods for different types of nodes

public /* override */ void VisitRichTextStart(RichText run) {
    ++nodecount;
    AppendText(run.getText());
}

public /* override */ void VisitDocumentStart(Document document) {
    ++nodecount;
}

public /* override */ void VisitPageStart(Page page) {
    ++nodecount;
}

public /* override */ void VisitTitleStart(Title title) {
    ++nodecount;
}

public /* override */ void VisitImageStart(Image image) {
    ++nodecount;
    // Pro tip: you can save the image stream here if you need to extract images.
}

public /* override */ void VisitOutlineGroupStart(OutlineGroup outlineGroup) {
    ++nodecount;
}

public void VisitOutlineStart(Outline outline) {
    ++nodecount;
}

public void VisitOutlineElementStart(OutlineElement outlineElement) {
    ++nodecount;
}
```

## Krok 4: Metoda main – uruchomienie odwiedzającego

Metoda `main` wczytuje plik OneNote, tworzy instancję naszego niestandardowego odwiedzającego i rozpoczyna przeglądanie. Po zakończeniu wypisuje wyodrębniony tekst oraz całkowitą liczbę węzłów.

```java
public static void main(String[] args) throws IOException {
    // Open the document we want to convert.
    String dataDir = "Your Document Directory";
    Document doc = new Document(dataDir + "Sample1.one", new LoadOptions());
    
    // Create an object that inherits from the DocumentVisitor class.
    ExtractOneNoteContentUsingDocumentvisitor myConverter = new ExtractOneNoteContentUsingDocumentvisitor();
    
    // Accept the visitor to start the visiting process.
    doc.accept(myConverter);
    
    // Retrieve the result of the operation.
    System.out.println(myConverter.GetText());
    System.out.println(myConverter.NodeCount());
}
```

## Typowe scenariusze użycia – **wyodrębnianie obrazów z OneNote**

* **Indeksowanie wyszukiwania** – Konwertuj notatniki OneNote na czysty tekst dla silników wyszukiwania pełnotekstowego.  
* **Migracja treści** – Przenieś notatki do systemu CMS lub portalu dokumentacji.  
* **Analiza danych** – Pobierz tekst i obrazy do przetwarzania języka naturalnego lub analizy obrazów.  

## Typowe problemy i rozwiązania

| Problem | Rozwiązanie |
|-------|----------|
| **NullPointerException przy odczycie pliku .one** | Upewnij się, że ścieżka do pliku (`dataDir`) kończy się separatorem ścieżki (`/` lub `\\`) i że plik istnieje. |
| **Obrazy nie są wyodrębniane** | Zaimplementuj logikę wewnątrz `VisitImageStart`, aby zapisać `image.getImageData()` do pliku lub strumienia. |
| **Duże notatniki powodują wysokie zużycie pamięci** | Przetwarzaj dokument strona po stronie lub użyj dostępnych API strumieniowych. |

## Najczęściej zadawane pytania

**P: Czy mogę wyodrębnić konkretne typy treści z dokumentu OneNote?**  
O: Tak, implementując tylko potrzebne metody odwiedzające (np. `VisitRichTextStart` dla tekstu, `VisitImageStart` dla obrazów).

**P: Czy Aspose.Note for Java jest kompatybilny z różnymi wersjami plików OneNote?**  
O: Absolutnie. Biblioteka obsługuje pliki .one tworzone przez najnowsze wersje Microsoft OneNote.

**P: Czy mogę zintegrować ten proces wyodrębniania z moją aplikacją Java?**  
O: Tak. Pokazany kod jest samodzielnym przykładem, który możesz wstawić bezpośrednio do dowolnego projektu Java.

**P: Czy Aspose.Note for Java radzi sobie ze złożonymi strukturami OneNote?**  
O: Tak. Wzorzec Visitor pozwala na nawigację po zagnieżdżonych konturach, grupach i osadzonych obiektach bez utraty hierarchii.

**P: Czy istnieje limit rozmiaru dokumentu OneNote, który można przetworzyć?**  
O: Nie ma sztywnego limitu, ale bardzo duże notatniki mogą wymagać większej pamięci heap; rozważ przetwarzanie ich partiami.

**P: Jak wyodrębnić obrazy z OneNote?**  
O: Zaimplementuj metodę `VisitImageStart`, aby uzyskać dostęp do `image.getImageData()` i zapisać bajty do pliku.

---

**Ostatnia aktualizacja:** 2025-12-03  
**Testowane z:** Aspose.Note for Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}