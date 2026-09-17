---
date: 2026-02-10
description: Dowiedz się, jak konwertować OneNote na tekst i wyodrębniać obrazy za
  pomocą Aspose.Note dla Javy. Poradnik pokazuje, jak odczytać plik .one w Javie i
  wykonać ekstrakcję tekstu z OneNote.
linktitle: Convert OneNote to Text and Extract Images using Document Visitor - Java
second_title: Aspose.Note Java API
title: Konwertuj OneNote na tekst i wyodrębnij obrazy przy użyciu Document Visitor
  – Java
url: /pl/java/onenote-document-loading/extract-content-using-document-visitor/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konwertuj program OneNote na tekst i wyodrębnij obrazy przy użyciu programu Document Visitor - Java

## Wstęp

Aspose.Note dla Java ułatwia **konwertowanie OneNote na tekst** oraz **wyodrębnianie obrazów z notatników OneNote**. W tym samouczku przeprowadziliśmy Cię przez, praktyczny przykład, który występuje, jak za użytkownika pliku OneNote, przejście po jego składniku przy użyciu własnego `DocumentVisitor` i Standardowe obrazy, jak i zwykły tekst. Na koniec wiesz także, jak **czytać pliki .one w Javie** oraz dlaczego jest to idealne rozwiązanie, jeśli chodzi o treść lub raportowania.

## Szybkie odpowiedzi
- **Jakiej biblioteki dostępne?** Aspose.Note for Java (link do pobrania poniżej).
- **Czy można wyodrębnić tylko obrazy?** Tak – zaimplementuj `VisitImageStart` w `DocumentVisitor`.
- **Jak odczytać plik .one w Javie?** użyj `new Document(path, new LoadOptions())`.
- **Czy dostępna jest wersja do produkcji?** Licencja komercyjna jest wymagana przy użyciu bez wersji próbnej.
- **Jaka wersja Javy obsługuje?** JDK8lub wyższy.

## Co to jest konwersja programu OneNote na tekst?

Konwersja OneNote oznacza tekst wyodrębniony surowej treści tekstowej z notatnika `.one` i zapisanie jej jako zwykłego tekstu Unicode. Jest to konieczne, gdy są potrzebne przeszukiwane archiwa, lekkie funkcje danych lub proste podsumowanie bez konieczności formatowania OneNote.

## Dlaczego warto używać narzędzia Document Visitor Aspose.Note do wyodrębniania tekstu w OneNote?

- **Kontrola szczegółowa:** Wzorzec odwiedzający pozwala dokładnie określić, które węzły (strony, kontury, obrazy, tekst sformatowany) mają być kontrolowane.
- **Wykonanie:** Unikasz obciążenia całego dokumentu pamięci jako jeden blok; Każdy węzeł jest odwiedzany przez użytkownika.
- **Wszechstronność:** Ten sam odwiedzający może być rozszerzony o wyodrębnione obrazy, tabele lub narzędzia metadanych, co tworzy kompleksowy element istniejący dla **konwertuj jedną notatkę na tekst**, jak i **jak wyodrębnić obrazy**.

## Warunki wstępne

Zanim udałosz się, udało się, że masz:

1. Zainstalowany Java Development Kit (JDK)8lub nowszy.
2. Biblioteka Aspose.Note for Java pobraną. Możesz ją zabrać **[tutaj](https://releases.aspose.com/note/java/)**.
3. Dokument OneNote („.one”), z którego chcesz wyodrębnić obrazy lub przekonwertować na tekst.

## Importuj pakiety

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

## Krok 1: Skonfiguruj niestandardową metodę odwiedzania dokumentu

Utwórz klasę, która rozszerza `DocumentVisitor`. Klasa ta będzie wywoływana dla każdego węzła w dokumencie OneNote, umożliwiając **wyodrębnianie obrazów OneNote** i opcjonalne zbieranie tekstu.

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

## Krok 2: Implementacja metod dla metody odwiedzającego

Dodaj nadpisania dla typów węzłów, które Cię interesują. Poniżej obsługujemy tekst sformatowany, obrazy, tytuły, strony, kontury i elementy konturów. Metoda `VisitImageStart` to miejsce, w którym odbywa się wyodrębnianie obrazu.

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

### Po co implementować te metody?

- **Extract images from OneNote:** `VisitImageStart` daje bezpośredni dostęp do surowych bajtów obrazu.  
- **Convert OneNote to text:** `VisitRichTextStart` zbiera treść tekstową, umożliwiając prostą operację **convert OneNote to text**.  
- **Read .one file Java:** Wzorzec odwiedzającego abstrahuje strukturę pliku `.one`, więc nie musisz samodzielnie parsować formatu binarnego.

## Krok 3: Uruchom metodę odwiedzającego z metody głównej

Załaduj plik `.one`, utwórz instancję swojego odwiedzającego i rozpocznij traversację.

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

## Typowe przypadki użycia

- **Automatyczne raportowanie:** Pobieraj obrazy i tekst z notatnika spotkań OneNote, aby wygenerować podsumowanie w formacie PDF lub HTML.
- **Migracja zawartości:** Konwertuj starsze archiwa OneNote na pliki tekstowe dla indeksowania lub pierwotne do wyszukiwarek.
- **Ekstrakcja zasobów cyfrowych:** Zbieraj osadzone zrzuty ekranu, diagramy lub zdjęcia do funkcji użytkowych w innych aplikacjach.

## Rozwiązywanie problemów i wskazówki

- **Duże notesy:** Jeśli wystąpią problemy z pamięcią, analizj stronę pojedynczo, sprawdzając `VisitPageStart` i ładując zasoby na poziomie strony tylko w razie potrzeby.
- **Formaty obrazów:** Obiekt `Image` zwrot surowe bajty; Może być konieczne wykrycie formatu (PNG, JPEG) przed zapisem.
- **Błędy licencji:** nastąpiło, że ustawiłeś obciążenie Aspose (`Licencja licencji = nowa licencja(); licencja.setLicense("Aspose.Note.Java.lic");`) przed uruchomieniem dokumentu w środowisku produkcyjnym.
- **Jak efektywnie wyodrębnić obrazy:** Filtruj węzły w `VisitImageStart` według własnego lub formatu, jeśli tylko występują konsekwencje obrazów.

## Często zadawane pytania

**Q: Czy mogę wyodrębnić konkretne typy treści z dokumentu OneNote?**  
A: Tak – poprzez nadpisanie tylko tych metod odwiedzających, które są potrzebne (np. `VisitImageStart` dla obrazów, `VisitRichTextStart` dla tekstu).

**Q: Czy Aspose.Note for Java jest kompatybilny z różnymi wersjami dokumentów OneNote?**  
A: Absolutnie. Biblioteka obsługuje wszystkie główne wersje plików OneNote, więc możesz bezpiecznie **read .one file java** projekty niezależnie od wersji źródłowego OneNote.

**Q: Czy mogę zintegrować ten proces wyodrębniania z moją aplikacją Java?**  
A: Tak. Wzorzec odwiedzającego działa płynnie w dowolnym kodzie Java; wystarczy dodać plik JAR biblioteki i wywołać przykład przedstawiony powyżej.

**Q: Czy Aspose.Note for Java zapewnia wsparcie przy obsłudze złożonych dokumentów OneNote?**  
A: Tak. Zagnieżdżone kontury, osadzone media i własne dane są udostępniane poprzez API odwiedzającego.

**Q: Czy istnieje limit rozmiaru dokumentu OneNote, który można przetworzyć?**  
A: Nie ma sztywnego limitu, ale bardzo duże notatniki mogą wymagać większej pamięci heap; rozważ przetwarzanie ich strona po stronie.

**Q: Jak przekonwertować wyodrębniony tekst na plik tekstowy?**  
A: Po tym, jak `myConverter.GetText()` zwróci `String`, zapisz go do pliku używając standardowego I/O Javy (`Files.write(Paths.get("output.txt"), text.getBytes());`).

---
**Last Updated:** 2026-02-10  
**Tested With:** Aspose.Note for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}