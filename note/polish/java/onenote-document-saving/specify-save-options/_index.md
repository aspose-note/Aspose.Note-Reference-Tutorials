---
date: 2025-12-18
description: Dowiedz się, jak zapisać wybrane strony jako PDF w OneNote przy użyciu
  Aspose.Note dla Javy, obejmując indeks strony, liczbę stron i kompresję. Łatwo konwertuj
  OneNote na PDF.
linktitle: Save Specific Pages PDF in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Zapisz określone strony PDF w OneNote – Aspose.Note
url: /pl/java/onenote-document-saving/specify-save-options/
weight: 24
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zapisz wybrane strony PDF w OneNote – Aspose.Note

## Wprowadzenie

W tym samouczku dowiesz się **jak zapisać wybrane strony PDF** z dokumentu OneNote przy użyciu Aspose.Note dla Javy. Niezależnie od tego, czy potrzebujesz **wyeksportować OneNote jako PDF**, **przekonwertować OneNote na PDF**, czy po prostu kontrolować zakres stron i kompresję, ten przewodnik przeprowadzi Cię przez każdy krok z jasnymi wyjaśnieniami i gotowym do uruchomienia kodem.

## Szybkie odpowiedzi
- **Co oznacza „zapisz wybrane strony PDF”?** Umożliwia wybranie podzbioru stron OneNote i wygenerowanie pliku PDF zawierającego tylko te strony.  
- **Która biblioteka obsługuje to?** Aspose.Note dla Javy udostępnia `PdfSaveOptions`, aby kontrolować indeks strony, liczbę stron oraz kompresję obrazów.  
- **Czy potrzebna jest licencja?** Darmowa wersja próbna działa w środowisku deweloperskim; licencja komercyjna jest wymagana w produkcji.  
- **Czy mogę ustawić indeks strony i liczbę stron?** Tak – użyj `setPageIndex()` i `setPageCount()` w `PdfSaveOptions`.  
- **Czy obsługiwana jest kompresja obrazów?** Oczywiście – wybierz JPEG, PNG lub inne formaty za pomocą `setImageCompression()`.

## Wymagania wstępne

Zanim rozpoczniesz, upewnij się, że masz:

1. Podstawową znajomość programowania w Javie.  
2. Zainstalowane JDK na swoim komputerze.  
3. Bibliotekę Aspose.Note dla Javy pobraną z oficjalnej strony – możesz ją pobrać **[tutaj](https://releases.aspose.com/note/java/)**.  

## Importowanie pakietów

Na początek zaimportuj klasy, które będą potrzebne:

```java
import com.aspose.note.Document;
import com.aspose.note.PdfImageCompression;
import com.aspose.note.PdfSaveOptions;
import java.io.IOException;
```

Przejdźmy przez proces krok po kroku.

## Jak zapisać wybrane strony PDF

### Krok 1: Załaduj dokument OneNote

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";

// Load the document into Aspose.Note.
Document doc = new Document(dataDir + "Aspose.one");
```

Tutaj wskazujemy folder zawierający plik źródłowy `.one` i ładujemy go do obiektu `Document`. Obiekt ten reprezentuje cały notes OneNote w pamięci.

### Krok 2: Zainicjalizuj `PdfSaveOptions`

```java
// Initialize PdfSaveOptions object
PdfSaveOptions opts = new PdfSaveOptions();
```

`PdfSaveOptions` zapewnia precyzyjną kontrolę nad procesem konwersji do PDF, w tym możliwość **ustawienia indeksu strony PDF** oraz **ustawienia liczby stron PDF**.

### Krok 3: Ustaw indeks strony i liczbę stron

```java
// Set page index
opts.setPageIndex(2);

// Set page count
opts.setPageCount(3);
```

Te dwa wywołania informują Aspose.Note, aby rozpoczął eksport od strony 2 (indeksowanie od zera) i uwzględnił kolejne trzy strony. To jest sedno **zapisywania wybranych stron PDF**.

### Krok 4: Określ ustawienia kompresji

```java
// Specify compression if required
opts.setImageCompression(PdfImageCompression.Jpeg);
opts.setJpegQuality(90);
```

Możesz kontrolować jakość obrazów w PDF. Kompresja JPEG o jakości 90 % zapewnia dobrą równowagę między rozmiarem pliku a jakością wizualną.

### Krok 5: Zapisz dokument z opcjami

```java
dataDir = dataDir + "Document.SaveWithOptions_out.pdf";
doc.save(dataDir, opts);
```

Metoda `save` zapisuje wybrane strony do nowego pliku PDF, wykorzystując skonfigurowane opcje. Wynikiem jest kompaktowy PDF zawierający tylko potrzebne Ci strony.

## Dlaczego to ma znaczenie

- **Wydajność:** Eksportowanie tylko wymaganych stron skraca czas przetwarzania i zużycie pamięci, szczególnie w przypadku dużych notesów.  
- **Rozmiar pliku:** Ograniczając zakres stron i stosując kompresję JPEG, otrzymany PDF jest znacznie mniejszy — idealny do załączników e‑mail lub przesyłania w sieci.  
- **Elastyczność:** Możesz łączyć `setPageIndex` i `setPageCount` z innymi opcjami (np. dodawanie znaków wodnych), aby tworzyć własne potoki eksportu.

## Typowe przypadki użycia

| Scenariusz | Jak funkcja pomaga |
|------------|--------------------|
| Generowanie raportu z jednego spotkania | Eksportuj tylko stronę spotkania zamiast całego notesu. |
| Archiwizowanie wybranych sekcji | Zapisz wybrane sekcje jako PDF w celu zgodności, nie ujawniając niepowiązanej treści. |
| Zmniejszanie zużycia pasma dla użytkowników mobilnych | Wyślij lekki PDF zawierający tylko potrzebne strony. |

## Rozwiązywanie problemów i wskazówki

- **Nieprawidłowy indeks strony:** Pamiętaj, że indeksowanie stron zaczyna się od 0. Jeśli ustawisz indeks większy niż całkowita liczba stron, Aspose.Note zgłosi `ArgumentOutOfRangeException`.  
- **Liczba stron równa zero:** Ustawienie `setPageCount(0)` skutkuje pustym PDF. Użyj liczby dodatniej.  
- **Artefakty kompresji:** Jeśli jakość JPEG jest zbyt niska, obrazy mogą być rozmyte. Dostosuj `setJpegQuality()` w razie potrzeby.  
- **Problemy ze ścieżką pliku:** Upewnij się, że katalog wyjściowy istnieje i masz uprawnienia do zapisu; w przeciwnym razie `doc.save()` zakończy się niepowodzeniem.

## Najczęściej zadawane pytania

**Q1: Czy Aspose.Note radzi sobie z dużymi dokumentami OneNote?**  
A1: Tak, Aspose.Note jest zaprojektowany do efektywnego przetwarzania dużych notesów i możesz dodatkowo zwiększyć wydajność, eksportując tylko potrzebne strony.

**Q2: Czy Aspose.Note jest kompatybilny z najnowszymi wersjami Javy?**  
A2: Absolutnie. Biblioteka działa z Javą 8 i nowszymi wersjami.

**Q3: Czy mogę konwertować dokumenty OneNote na inne formaty oprócz PDF?**  
A3: Tak, Aspose.Note obsługuje konwersję do DOCX, HTML, XPS i kilku formatów obrazów.

**Q4: Czy Aspose.Note zapewnia wsparcie dla szyfrowania i deszyfrowania dokumentów OneNote?**  
A4: Tak, API zawiera metody umożliwiające programowe szyfrowanie i deszyfrowanie plików OneNote.

**Q5: Czy Aspose.Note nadaje się do użytku komercyjnego?**  
A5: Tak, licencja komercyjna pozwala na użycie biblioteki w środowiskach produkcyjnych.

---

**Ostatnia aktualizacja:** 2025-12-18  
**Testowano z:** Aspose.Note for Java 24.12 (latest)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}