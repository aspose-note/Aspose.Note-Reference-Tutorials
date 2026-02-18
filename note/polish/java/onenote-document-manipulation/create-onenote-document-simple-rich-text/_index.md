---
date: 2026-02-18
description: Naucz się ustawiać styl akapitu i dodawać element konspektu podczas tworzenia
  dokumentów OneNote w Javie przy użyciu Aspose.Note. Eksportuj OneNote do PDF, zapisz
  OneNote jako PDF i generuj pliki OneNote bez wysiłku.
linktitle: Set Paragraph Style while Creating OneNote Document in Java
second_title: Aspose.Note Java API
title: Eksportuj OneNote do PDF – Ustaw styl akapitu podczas tworzenia dokumentu OneNote
  w Javie
url: /pl/java/onenote-document-manipulation/create-onenote-document-simple-rich-text/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ustaw styl akapitu podczas tworzenia dokumentu OneNote w Javie

## Wprowadzenie

W dzisiejszym dynamicznie rozwijającym się środowisku programistycznym możliwość **eksportowania OneNote do PDF** w sposób programowy jest niezbędna do tworzenia dopracowanych, gotowych do udostępnienia dokumentów. Ten samouczek przeprowadzi Cię przez tworzenie pliku OneNote, zastosowanie własnego stylu akapitu oraz ostateczne **eksportowanie OneNote do PDF** przy użyciu Aspose.Note dla Javy. Niezależnie od tego, czy budujesz silnik raportowania, zautomatyzowane rozwiązanie do notowania, czy usługę konwersji dokumentów, techniki przedstawione tutaj pomogą Ci **zapisać OneNote jako PDF** z precyzyjną kontrolą formatowania.

## Szybkie odpowiedzi
- **Co oznacza „ustaw styl akapitu”?** Nakłada czcionkę, rozmiar, kolor i inne formatowanie na akapit tekstu.  
- **Czy mogę wyeksportować wynik do PDF?** Tak – samouczek kończy się zapisem pliku OneNote jako PDF.  
- **Czy potrzebna jest licencja na Aspose.Note?** Darmowa wersja próbna wystarczy do oceny; licencja jest wymagana w środowisku produkcyjnym.  
- **Jakie IDE są obsługiwane?** Dowolne IDE Java – Eclipse, IntelliJ IDEA, NetBeans itp.  
- **Jak długo trwa implementacja?** Około 10‑15 minut dla podstawowego dokumentu.

## Czym jest „ustaw styl akapitu” w Aspose.Note?
Ustawianie stylu akapitu odnosi się do konfigurowania obiektu `ParagraphStyle` (nazwa czcionki, rozmiar, kolor itp.) i dołączania go do węzła `RichText`. Daje to pełną kontrolę nad tym, jak tekst wygląda na stronie OneNote.

## Jak ustawić styl akapitu w OneNote?
Zastosowanie stylu jest tak proste, jak stworzenie instancji `ParagraphStyle`, dostosowanie jej właściwości i przypisanie jej elementowi `RichText`. API umożliwia wykonanie tej operacji w jednej linii, gdy obiekt stylu jest gotowy.

## Dlaczego eksportować OneNote do PDF?
- **Spójna identyfikacja wizualna:** Zachowuje firmowe czcionki i kolory przy udostępnianiu notatek na zewnątrz.  
- **Czytelność:** PDF utrzymuje dokładny układ, co czyni go idealnym do drukowania lub archiwizacji.  
- **Dostępność na wszystkich platformach:** Odbiorcy mogą otworzyć PDF na dowolnym urządzeniu bez potrzeby posiadania OneNote.  

## Wymagania wstępne

Przed rozpoczęciem upewnij się, że masz:

1. **Java Development Kit (JDK) 1.8+** – dowolny aktualny JDK będzie działał.  
2. **Aspose.Note for Java** – pobierz najnowszy plik JAR ze [strony pobierania Aspose.Note](https://releases.aspose.com/note/java/).  
3. **IDE** (Eclipse, IntelliJ IDEA lub NetBeans) do kompilacji i uruchomienia przykładu.  

> **Pro tip:** Dodaj plik JAR Aspose.Note do ścieżki klas projektu za pomocą Maven lub ręcznie odwołując się do JAR w swoim IDE.

## Importowanie pakietów

Najpierw zaimportuj klasy, które będą potrzebne. Ten blok pozostaje niezmieniony.

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

> Klasa `ParagraphStyle` jest kluczem do **ustawienia stylu akapitu** później w samouczku.

## Przewodnik krok po kroku

Poniżej znajduje się zwięzły opis każdej operacji. Bloki kodu są dokładnie takie, jak w oryginalnym przykładzie; dodajemy jedynie tekst wyjaśniający.

### Krok 1: Ustaw katalog dokumentu
Zdefiniuj, gdzie zostaną zapisane wygenerowane pliki.

```java
String dataDir = "Your Document Directory";
```

Zastąp `"Your Document Directory"` ścieżką bezwzględną lub względną na swoim komputerze.

### Krok 2: Zainicjalizuj obiekt Document
Utwórz główny obiekt `Document`, który reprezentuje plik OneNote.

```java
Document doc = new Document();
```

### Krok 3: Zainicjalizuj obiekt Page
Plik OneNote składa się z jednej lub wielu stron; zaczynamy od jednej strony.

```java
Page page = new Page();
```

### Krok 4: Zainicjalizuj obiekt Outline
Outlines działają jako kontenery dla elementów outline (pomyśl o nich jako sekcjach).

```java
Outline outline = new Outline();
```

### Krok 5: Zainicjalizuj obiekt OutlineElement
Tutaj **dodajemy element outline**, który będzie zawierał nasz tekst sformatowany.

```java
OutlineElement outlineElem = new OutlineElement();
```

### Krok 6: Ustaw styl tekstu (Ustaw styl akapitu)

```java
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```

Instancja `ParagraphStyle` definiuje czcionkę, rozmiar i kolor — to miejsce, w którym **ustawiamy styl akapitu** dla nadchodzącego węzła tekstowego.

### Krok 7: Zainicjalizuj obiekt RichText

```java
RichText text = new RichText().append("Hello OneNote text!");
text.setParagraphStyle(textStyle);
```

Tworzymy węzeł `RichText`, wstawiamy prosty ciąg znaków i dołączamy wcześniej zdefiniowany styl.

### Krok 8: Dodaj węzeł RichText do OutlineElement

```java
outlineElem.appendChildLast(text);
```

Teraz sformatowany tekst znajduje się wewnątrz elementu outline.

### Krok 9: Dodaj węzeł OutlineElement do Outline

```java
outline.appendChildLast(outlineElem);
```

Outline zawiera teraz element, który przechowuje nasz akapit.

### Krok 10: Dodaj węzeł Outline do Page

```java
page.appendChildLast(outline);
```

Umieszczamy outline na stronie.

### Krok 11: Dodaj węzeł Page do Document

```java
doc.appendChildLast(page);
```

Dokument ma już jedną stronę ze sformatowanym tekstem.

### Krok 12: Zapisz dokument (Eksportuj OneNote do PDF)

```java
doc.save(dataDir + "CreateOneNoteDocumentWithSimpleRichText_out.pdf", SaveFormat.Pdf);
```

Metoda `save` zapisuje plik OneNote i **eksportuje OneNote PDF** w jednym kroku. Możesz także zapisać jako `.one`, używając `SaveFormat.One`, jeśli potrzebny jest natywny format.

## Typowe problemy i rozwiązania

| Problem | Powód | Rozwiązanie |
|---------|-------|-------------|
| **Plik nie znaleziony** | `dataDir` wskazuje na nieistniejący folder. | Upewnij się, że katalog istnieje lub utwórz go programowo (`new File(dataDir).mkdirs();`). |
| **Pusty PDF** | Nie dodano żadnej treści przed zapisem. | Sprawdź, czy węzeł `RichText` został dołączony i czy styl został ustawiony. |
| **Nieobsługiwana czcionka** | Nazwa czcionki nie jest zainstalowana w systemie. | Użyj popularnej czcionki, np. `"Arial"`, lub osadź czcionkę w projekcie. |

## Najczęściej zadawane pytania

**P: Czy Aspose.Note obsługuje złożone formatowanie, takie jak tabele lub obrazy?**  
O: Tak, API wspiera tabele, obrazy, hiperłącza i bardziej zaawansowane funkcje układu.

**P: Czy istnieje możliwość **konwersji OneNote PDF** z powrotem do pliku OneNote?**  
O: Bezpośrednia konwersja nie jest udostępniona, ale możesz wyodrębnić zawartość PDF i odtworzyć dokument OneNote przy użyciu API.

**P: Czy biblioteka działa w środowiskach Linux/macOS?**  
O: Oczywiście. Aspose.Note for Java jest niezależny od platformy; wystarczy mieć zainstalowany JDK.

**P: Jak dodać wiele stron lub outline?**  
O: Utwórz dodatkowe obiekty `Page` i `Outline`, a następnie dołącz je do `Document` tak samo, jak w przykładzie z jedną stroną.

**P: Gdzie mogę znaleźć więcej przykładów?**  
O: Oficjalna dokumentacja Aspose.Note oraz [forum wsparcia](https://forum.aspose.com/c/note/28) zawierają liczne przykłady kodu.

## Podsumowanie

Widzisz teraz, jak **ustawić styl akapitu**, **dodać element outline** i **wygenerować plik OneNote**, który może być **wyeksportowany do PDF** przy użyciu Aspose.Note dla Javy. Wczesne zastosowanie stylowanego tekstu zapewnia, że końcowy dokument wygląda profesjonalnie, a każda kolejna operacja **konwersji OneNote PDF** zachowuje formatowanie. Śmiało rozbudowuj tę bazę o obrazy, tabele lub własne metadane, aby spełnić wymagania swojego projektu.

---

**Last Updated:** 2026-02-18  
**Tested With:** Aspose.Note for Java 24.11 (latest release)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}