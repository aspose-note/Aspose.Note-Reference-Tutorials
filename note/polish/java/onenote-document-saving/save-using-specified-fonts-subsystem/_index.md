---
title: Zapisz, używając określonego podsystemu czcionek w programie OneNote
linktitle: Zapisz, używając określonego podsystemu czcionek w programie OneNote
second_title: Aspose.Note API Java
description: Dowiedz się, jak zapisywać dokumenty OneNote przy użyciu określonego podsystemu czcionek w Javie za pomocą Aspose.Note. Bez wysiłku zapewnij spójną reprezentację czcionek na różnych platformach.
weight: 22
url: /pl/java/onenote-document-saving/save-using-specified-fonts-subsystem/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zapisz, używając określonego podsystemu czcionek w programie OneNote

## Wstęp

Aspose.Note dla Java zapewnia solidne możliwości pracy z dokumentami OneNote. Jednym z powszechnych wymagań podczas pracy z takimi dokumentami jest zapewnienie prawidłowego utrzymania czcionek, zwłaszcza jeśli dokument ma zostać wyeksportowany lub zapisany w różnych formatach, takich jak PDF. Ten samouczek przeprowadzi Cię przez proces zapisywania dokumentów programu OneNote przy określaniu podsystemu czcionek, zapewniając spójną i dokładną reprezentację tekstu na różnych platformach.

## Warunki wstępne

Zanim przejdziemy do samouczka, upewnij się, że masz skonfigurowane następujące wymagania wstępne:

### 1. Zestaw programistyczny Java (JDK)

 Upewnij się, że w systemie jest zainstalowany zestaw Java Development Kit (JDK). Można go pobrać z[Tutaj](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html) jeśli jeszcze tego nie zrobiłeś.

### 2. Aspose.Note dla biblioteki Java

 Pobierz i skonfiguruj bibliotekę Aspose.Note dla Java. Można go pobrać z[strona internetowa](https://releases.aspose.com/note/java/).

## Importuj pakiety

Pamiętaj, aby zaimportować niezbędne pakiety do swojego projektu Java:

```java
import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
import com.aspose.note.fonts.DocumentFontsSubsystem;
import java.io.FileInputStream;
import java.io.IOException;
import java.io.InputStream;
import java.nio.file.Paths;
```

Podzielmy teraz każdy przykład na wiele kroków, aby lepiej zrozumieć proces.

## Krok 1: Zapisz przy użyciu podsystemu czcionek dokumentu z domyślną nazwą czcionki

W tym kroku pokazano, jak zapisać dokument w formacie PDF przy użyciu określonej domyślnej nazwy czcionki.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName() throws IOException
{
    // Załaduj dokument do Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Określ domyślną czcionkę.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFont("Times New Roman"));

    // Zapisz dokument w formacie PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf", options);
}
```

W tym kroku:
- Dokument OneNote jest ładowany przy użyciu Aspose.Note.
- Domyślną czcionką jest „Times New Roman”.
- Dokument zapisywany jest w formacie PDF z określoną czcionką.

## Krok 2: Zapisz przy użyciu podsystemu czcionek dokumentów z domyślną czcionką z pliku

W tym kroku pokazano, jak zapisać dokument w formacie PDF przy użyciu domyślnej czcionki załadowanej z pliku.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile() throws IOException
{
    // Załaduj dokument do Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Określ ścieżkę do pliku czcionki.
    String fontFile = "geo_1.ttf";

    // Określ domyślną czcionkę z pliku.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromFile(fontFile));

    // Zapisz dokument w formacie PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf", options);
}
```

W tym kroku:
- Załadowany zostanie plik czcionki „geo_1.ttf”.
- Domyślna czcionka jest określona na podstawie załadowanego pliku czcionki.
- Dokument zapisywany jest w formacie PDF z określoną czcionką.

## Krok 3: Zapisz przy użyciu podsystemu czcionek dokumentów z domyślną czcionką ze strumienia

tym kroku pokazano, jak zapisać dokument w formacie PDF przy użyciu domyślnej czcionki załadowanej ze strumienia.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream() throws IOException
{
    // Załaduj dokument do Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Określ ścieżkę do pliku czcionki.
    String fontFile = "geo_1.ttf";

    // Załaduj plik czcionki jako strumień.
    InputStream stream = new FileInputStream(fontFile);

    try
    {
        // Określ domyślną czcionkę ze strumienia.
        PdfSaveOptions options = new PdfSaveOptions();
        options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromStream(stream));

        // Zapisz dokument w formacie PDF.
        oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf", options);
    }
    catch (Exception e)
    {
        stream.close();
    }
}
```

W tym kroku:
- Plik czcionki „geo_1.ttf” jest ładowany jako strumień.
- Domyślna czcionka jest określona na podstawie załadowanego strumienia.
- Dokument zapisywany jest w formacie PDF z określoną czcionką.

## Wniosek

W tym samouczku nauczyliśmy się, jak zapisywać dokumenty OneNote przy użyciu określonego podsystemu czcionek w Javie przy użyciu Aspose.Note. Wykonując poniższe kroki, możesz zapewnić spójną reprezentację czcionek na różnych platformach podczas eksportowania lub zapisywania dokumentów.

## Często zadawane pytania

### P1: Czy mogę określić różne czcionki dla różnych części dokumentu?

O1: Tak, możesz określić różne czcionki dla różnych części dokumentu, używając Aspose.Note dla Java.

### P2: Czy Aspose.Note jest kompatybilny ze wszystkimi wersjami OneNote?

O2: Aspose.Note obsługuje różne wersje OneNote, zapewniając kompatybilność w różnych środowiskach.

### P3: Jak mogę sobie poradzić z brakującymi czcionkami podczas zapisywania dokumentów?

O3: Aspose.Note udostępnia opcje umożliwiające określenie domyślnych czcionek w celu skutecznej obsługi brakujących czcionek podczas zapisywania dokumentu.

### P4: Czy mogę dostosować właściwości czcionki, takie jak rozmiar i styl?

O4: Tak, możesz dostosować właściwości czcionki, takie jak rozmiar, styl i kolor, używając Aspose.Note dla Java.

### P5: Czy dostępna jest wersja próbna Aspose.Note dla Java?

Odpowiedź 5: Tak, możesz pobrać bezpłatną wersję próbną Aspose.Note dla Java ze strony internetowej.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
