---
date: 2025-12-04
description: Dowiedz się, jak wyodrębniać obrazy z plików OneNote i konwertować OneNote
  na tekst w Javie przy użyciu Aspose.Note. Przewodnik krok po kroku z przykładami
  kodu.
language: pl
linktitle: Extract Images from OneNote using Document Visitor - Java
second_title: Aspose.Note Java API
title: Wyodrębnianie obrazów z OneNote przy użyciu Document Visitor – Java
url: /java/onenote-document-loading/extract-content-using-document-visitor/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wyodrębnianie obrazów z OneNote przy użyciu Document Visitor - Java

## Introduction

Aspose.Note for Java ułatwia **wyodrębnianie obrazów z OneNote** w zeszytach oraz odczytanie podstawowego pliku `.one` w Javie. W tym samouczku przeprowadzimy Cię przez kompletny, praktyczny przykład, który pokazuje, jak załadować plik OneNote, przejść po jego strukturze przy użyciu własnego `DocumentVisitor` i wyciągnąć zarówno obrazy, jak i zwykły tekst. Na koniec dowiesz się także, jak **przekształcić OneNote na tekst**, jeśli potrzebujesz tylko treści tekstowej.

## Quick Answers
- **Jakiej biblioteki potrzebuję?** Aspose.Note for Java (link do pobrania poniżej).  
- **Czy mogę wyodrębnić tylko obrazy?** Tak – zaimplementuj metodę `VisitImageStart` w `DocumentVisitor`.  
- **Jak odczytać plik .one w Javie?** Użyj `new Document(path, new LoadOptions())`.  
- **Czy potrzebna jest licencja do produkcji?** Wymagana jest licencja komercyjna do użytku nie‑testowego.  
- **Jakąję Javy obsługuje?** JDK 8 lub wyższą.

## Prerequisites

Zanim zaczniesz, upewnij się, że masz:

1. Java Development Kit (JDK) 8 lub nowszy zainstalowany.  
2. Aspose.Note for Java library downloaded. You can download it **[here](https://releases.aspose.com/note/java/)**.  
3. Dokument OneNote (`.one`), z którego chcesz wyodrębnić obrazy lub przekonwertować na tekst.

## Import Packages

Najpierw zaimportuj niezbędne klasy z API Aspose.Note.

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

## Step 1: Set Up a Custom Document Visitor

Utwórz klasę, która rozszerza `DocumentVisitor`. Ta klasa będzie wywoływana dla każdego węzła w dokumencie OneNote, umożliwiając **wyodrębnianie obrazów z OneNote** i opcjonalnie zbieranie tekstu.

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

## Step 2: Implement Visitor Methods

Dodaj nadpisania dla typów węzłów, które Cię interesują. Poniżej obsługujemy rich‑text, obrazy, tytuły, strony, kontury i elementy konturów. Metoda `VisitImageStart` to miejsce, w którym odbywa się wyodrębnianie obrazu.

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
    // Here you could save the image to disk or process it further
    System.out.println("Found image with size: " + image.getData().length + " bytes");
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

### Why implement these methods?

- **Wyodrębnianie obrazów z OneNote:** `VisitImageStart` zapewnia bezpośredni dostęp do surowych bajtów obrazu.  
- **Konwersja OneNote na tekst:** `VisitRichTextStart` zbiera treść tekstową, umożliwiając prostą operację **convert OneNote to text**.  
- **Odczyt pliku .one w Javie:** Wzorzec odwiedzającego abstrahuje strukturę podstawowego pliku `.one`, więc nie musisz samodzielnie parsować formatu binarnego.

## Step 3: Run the Visitor from Your Main Method

Załaduj plik `.one`, utwórz instancję swojego odwiedzającego i rozpocznij przeglądanie.

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
    System.out.println(myConverter.GetText());   // Text extracted from the notebook
    System.out.println(myConverter.NodeCount()); // Total nodes visited
}
```

## Common Use Cases

- **Automatyczne raportowanie:** Pobierz obrazy i tekst z zeszytu spotkania OneNote, aby wygenerować podsumowanie w PDF lub HTML.  
- **Migracja treści:** Przekształć archiwa OneNote w pliki tekstowe do indeksowania lub wprowadzania do wyszukiwarki.  
- **Ekstrakcja zasobów cyfrowych:** Zbierz osadzone zrzuty ekranu, diagramy lub zdjęcia do ponownego użycia w innych aplikacjach.

## Troubleshooting & Tips

- **Duże zeszyty:** Jeśli napotkasz problemy z pamięcią, przetwarzaj strony indywidualnie, sprawdzając `VisitPageStart` i ładując zasoby na poziomie strony tylko w razie potrzeby.  
- **Formaty obrazów:** Obiekt `Image` zwraca surowe bajty; może być konieczne wykrycie formatu (PNG, JPEG) przed zapisem.  
- **Błędy licencji:** Upewnij się, że ustawiłeś licencję Aspose (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`) przed załadowaniem dokumentu w środowisku produkcyjnym.

## Frequently Asked Questions

**Q: Czy mogę wyodrębnić określone typy treści z dokumentu OneNote?**  
A: Tak – poprzez nadpisanie tylko tych metod odwiedzającego, które są potrzebne (np. `VisitImageStart` dla obrazów, `VisitRichTextStart` dla tekstu).

**Q: Czy Aspose.Note for Java jest kompatybilny z różnymi wersjami dokumentów OneNote?**  
A: Absolutnie. Biblioteka obsługuje wszystkie główne wersje plików OneNote, więc możesz bezpiecznie **read .one file Java** projekty niezależnie od wersji pochodzącego dokumentu OneNote.

**Q: Czy mogę zintegrować ten proces wyodrębniania w mojej aplikacji Java?**  
A: Tak. Wzorzec odwiedzającego działa płynnie w dowolnym kodzie Java; wystarczy dodać plik JAR biblioteki i wywołać przykład pokazany powyżej.

**Q: Czy Aspose.Note for Java zapewnia wsparcie przy obsłudze złożonych dokumentów OneNote?**  
A: Tak. Zagnieżdżone kontury, osadzone media i dane niestandardowe są udostępniane poprzez API odwiedzającego.

**Q: Czy istnieje jakiś limit rozmiaru dokumentu OneNote, który można przetworzyć?**  
A: Nie ma sztywnego limitu, ale bardzo duże zeszyty mogą wymagać większej pamięci sterty; rozważ przetwarzanie ich strona po stronie.

**Q: Jak przekonwertować wyodrębniony tekst do pliku tekstowego?**  
A: Po tym, jak `myConverter.GetText()` zwróci `String`, zapisz go do pliku używając standardowego I/O Javy (`Files.write(Paths.get("output.txt"), text.getBytes());`).

---  

**Last Updated:** 2025-12-04  
**Tested With:** Aspose.Note for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}