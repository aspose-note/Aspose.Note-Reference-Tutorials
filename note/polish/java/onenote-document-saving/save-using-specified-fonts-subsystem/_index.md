---
date: 2025-12-18
description: Naucz się, jak **zapisować OneNote jako PDF** przy użyciu określonego
  podsystemu czcionek w Javie z Aspose.Note. Ten przewodnik pokazuje również, jak
  konwertować OneNote na PDF, ładować własne pliki czcionek i określać czcionki domyślne.
linktitle: Save OneNote as PDF Using Specified Fonts Subsystem
second_title: Aspose.Note Java API
title: Zapisz OneNote jako PDF przy użyciu określonego podsystemu czcionek
url: /pl/java/onenote-document-saving/save-using-specified-fonts-subsystem/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zapisz OneNote jako PDF przy użyciu określonego podsystemu czcionek

## Wprowadzenie

W wielu scenariuszach biznesowych musisz **zapisz OneNote jako PDF** zachowując dokładny wygląd oryginalnych stron. Aspose.Note for Java ułatwia to, pozwalając kontrolować podsystem czcionek podczas konwersji. W tym samouczku przeprowadzimy trzy praktyczne sposoby **konwersji OneNote do PDF**, obejmujące **ładowanie własnych plików czcionek**, **określenie domyślnej czcionki** oraz **użycie strumienia czcionki**, gdy czcionka nie jest dostępna na docelowym komputerze.

## Quick Answers
- **Co oznacza „save OneNote as PDF”?** Konwertuje plik .one do PDF, zachowując układ i styl.  
- **Które API obsługuje czcionki?** `DocumentFontsSubsystem` pozwala zdefiniować domyślną czcionkę lub załadować własny plik/strumień czcionki.  
- **Czy potrzebna jest licencja do produkcji?** Tak, komercyjna licencja Aspose.Note jest wymagana do użytku nie‑testowego.  
- **Czy mogę konwertować wiele plików jednocześnie?** Oczywiście – wystarczy pętla nad logiką ładowania i zapisywania `Document`.  
- **Jakiej wersji Javy wymaga?** Java 15 lub nowsza (przykład używa JDK 15).

## Co to jest „save OneNote as PDF” z podsystemem czcionek?

Zapisanie OneNote jako PDF z podsystemem czcionek oznacza, że podczas procesu konwersji Aspose.Note zastępuje brakujące glify czcionką, którą podasz. Gwarantuje to, że PDF wygląda identycznie na każdym urządzeniu, nawet gdy oryginalna czcionka nie jest zainstalowana.

## Dlaczego kontrolować podsystem czcionek przy **konwersji OneNote do PDF**?

- **Spójna identyfikacja wizualna** – dokumenty korporacyjne zachowują dokładny krój pisma.  
- **Niezawodność wieloplatformowa** – PDF-y renderują się tak samo na Windows, macOS, Linux i urządzeniach mobilnych.  
- **Mniej błędów** – ostrzeżenia o brakujących czcionkach znikają, co daje czysty wynik.

## Prerequisites

### 1. Java Development Kit (JDK)

Upewnij się, że masz zainstalowany Java Development Kit (JDK) na swoim systemie. Możesz go pobrać z [tutaj](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html), jeśli jeszcze tego nie zrobiłeś.

### 2. Biblioteka Aspose.Note for Java

Pobierz i skonfiguruj bibliotekę Aspose.Note for Java. Możesz ją pobrać ze [strony internetowej](https://releases.aspose.com/note/java/).

## Import Packages

Upewnij się, że zaimportowałeś niezbędne pakiety w swoim projekcie Java:

```java
import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
import com.aspose.note.fonts.DocumentFontsSubsystem;
import java.io.FileInputStream;
import java.io.IOException;
import java.io.InputStream;
import java.nio.file.Paths;
```

Teraz rozbijmy każdy przykład na kilka kroków, aby lepiej zrozumieć proces.

## Jak **zapisz OneNote jako PDF** używając Document Fonts Subsystem z domyślną czcionką

### Krok 1: Zapisz używając Document Fonts Subsystem z nazwą domyślnej czcionki

Ten krok demonstruje, jak **zapisz OneNote jako PDF** w prosty sposób, określając nazwę domyślnej czcionki.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName() throws IOException
{
    // Load the document into Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Specify the default font.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFont("Times New Roman"));

    // Save the document as PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf", options);
}
```

W tym kroku:
- Dokument OneNote jest ładowany przy użyciu Aspose.Note.
- **Domyślna czcionka** jest określona jako **"Times New Roman"**.
- Dokument jest zapisywany w formacie PDF z wybraną czcionką.

### Krok 2: Zapisz używając Document Fonts Subsystem z domyślną czcionką z pliku

Tutaj **ładujemy własny plik czcionki** i używamy go jako zapasowego przy konwersji do PDF.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile() throws IOException
{
    // Load the document into Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Specify the path to the font file.
    String fontFile = "geo_1.ttf";

    // Specify the default font from the file.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromFile(fontFile));

    // Save the document as PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf", options);
}
```

Kluczowe punkty:
- **Własny plik czcionki** `geo_1.ttf` jest **ładowany z dysku**.
- `usingDefaultFontFromFile` **określa domyślną czcionkę z pliku**, zapewniając, że PDF użyje tej czcionki, gdy oryginalna jest nieobecna.
- Powstały PDF zachowuje zamierzony wygląd.

### Krok 3: Zapisz używając Document Fonts Subsystem z domyślną czcionką ze strumienia

Czasami czcionka może być przechowywana w bazie danych lub otrzymywana przez sieć. Ten przykład pokazuje, jak **użyć strumienia czcionki**.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream() throws IOException
{
    // Load the document into Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Specify the path to the font file.
    String fontFile = "geo_1.ttf";

    // Load the font file as a stream.
    InputStream stream = new FileInputStream(fontFile);

    try
    {
        // Specify the default font from the stream.
        PdfSaveOptions options = new PdfSaveOptions();
        options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromStream(stream));

        // Save the document as PDF.
        oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf", options);
    }
    catch (Exception e)
    {
        stream.close();
    }
}
```

Co się tutaj dzieje:
- Plik czcionki jest otwierany jako **InputStream**, co jest przydatne, gdy czcionka znajduje się w źródle innym niż plik.
- `usingDefaultFontFromStream` **używa strumienia czcionki** do określenia czcionki zapasowej.
- Plik OneNote jest zapisywany jako PDF z czcionką opartą na strumieniu.

## Typowe problemy i rozwiązania

| Problem | Dlaczego się pojawia | Jak naprawić |
|-------|----------------|------------|
| **Ostrzeżenia o brakującej czcionce** | Plik .one odwołuje się do czcionki, której nie ma na komputerze. | Dostarcz domyślną czcionkę za pomocą `usingDefaultFont`, `usingDefaultFontFromFile` lub `usingDefaultFontFromStream`. |
| **Nie znaleziono pliku czcionki** | Nieprawidłowa ścieżka do pliku `.ttf`. | Użyj ścieżek bezwzględnych lub zweryfikuj ścieżkę względną względem katalogu roboczego. |
| **Strumień nie został zamknięty** | Wyjątek wystąpił przed wywołaniem `close()`. | Użyj try‑with‑resources (`try (InputStream stream = ...) { ... }`) aby automatycznie zamykać. |

## Najczęściej zadawane pytania

**P: Czy mogę określić różne czcionki dla różnych części dokumentu?**  
O: Tak, możesz zastosować własne ustawienia czcionki do poszczególnych elementów tekstu przy użyciu klasy `Font` w Aspose.Note.

**P: Czy Aspose.Note jest kompatybilny ze wszystkimi wersjami OneNote?**  
O: Aspose.Note obsługuje pliki OneNote z najnowszych wersji desktopowych i mobilnych, zapewniając szeroką kompatybilność.

**P: Jak mogę obsłużyć brakujące czcionki przy zapisywaniu dokumentów?**  
O: Użyj metod podsystemu czcionek pokazanych powyżej (`usingDefaultFont`, `usingDefaultFontFromFile`, `usingDefaultFontFromStream`), aby zapewnić zapasową czcionkę.

**P: Czy mogę dostosować właściwości czcionki, takie jak rozmiar i styl?**  
O: Oczywiście – API pozwala ustawić rozmiar, styl, kolor i inne atrybuty dla każdego fragmentu tekstu.

**P: Czy dostępna jest wersja próbna Aspose.Note for Java?**  
O: Tak, darmową wersję próbną można pobrać ze strony Aspose.

## Zakończenie

W tym samouczku nauczyliśmy się, jak **zapisz OneNote jako PDF** kontrolując podsystem czcionek w Javie przy użyciu Aspose.Note. Stosując trzy podejścia — określenie nazwy domyślnej czcionki, ładowanie własnego pliku czcionki lub użycie strumienia czcionki — możesz zapewnić spójną reprezentację czcionek na różnych platformach przy eksportowaniu lub zapisywaniu dokumentów OneNote.

---

**Last Updated:** 2025-12-18  
**Tested With:** Aspose.Note for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}