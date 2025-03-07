---
title: Zapisz w obrazie TIFF przy użyciu opcji zapisywania obrazu w programie OneNote
linktitle: Zapisz w obrazie TIFF przy użyciu opcji zapisywania obrazu w programie OneNote
second_title: Aspose.Note API Java
description: Konwertuj dokumenty OneNote do formatu TIFF i kontroluj rozmiar i jakość plików! Wybierz kompresję Jpeg, PackBits lub Fax w Javie. Pobierz przykłady kodu i dowiedz się, jak to zrobić! #OneNote #Java #Aspose
weight: 21
url: /pl/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zapisz w obrazie TIFF przy użyciu opcji zapisywania obrazu w programie OneNote

## Wstęp

W tym samouczku dowiesz się, jak zapisać dokument w formacie obrazu TIFF przy użyciu różnych metod kompresji w Aspose.Note dla Java. Omówimy wymagania wstępne, importowanie pakietów i zapewnimy przewodnik krok po kroku dla każdej metody kompresji.

## Warunki wstępne

Zanim zaczniesz, upewnij się, że masz następujące elementy:

- Zestaw Java Development Kit (JDK) zainstalowany w systemie.
- Pobrano i skonfigurowano bibliotekę Aspose.Note dla Java.
- Podstawowa znajomość języka programowania Java.

## Importuj pakiety

Najpierw musisz zaimportować niezbędne pakiety do pliku Java:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Krok 1: Zapisz w formacie TIFF przy użyciu kompresji JPEG

```java
public static void SaveToTiffUsingJpegCompression() throws IOException {
    // Ścieżka do katalogu dokumentów.
    String dataDir = "Your Document Directory";

    // Załaduj dokument do Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.Jpeg);
    options.setQuality(93);

    oneFile.save(Paths.get(dataDir,"SaveToTiffUsingJpegCompression.tiff").toString(), options);
}
```

-  Załaduj dokument za pomocą`Document` klasa.
-  Utwórz instancję`ImageSaveOptions` i określ typ kompresji TIFF jako JPEG.
- Ustaw żądaną jakość (opcjonalnie).
- Zapisz dokument w formacie TIFF, korzystając z określonych opcji.

## Krok 2: Zapisz w formacie TIFF przy użyciu kompresji PackBits

```java
public static void SaveToTiffUsingPackBitsCompression() throws IOException {
    // Ścieżka do katalogu dokumentów.
    String dataDir = "Your Document Directory";

    // Załaduj dokument do Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.PackBits);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingPackBitsCompression.tiff").toString(), options);
}
```

-  Załaduj dokument za pomocą`Document` klasa.
-  Utwórz instancję`ImageSaveOptions` i określ typ kompresji TIFF jako PackBits.
- Zapisz dokument w formacie TIFF, korzystając z określonych opcji.

## Krok 3: Zapisz w formacie TIFF przy użyciu kompresji faksów CCITT Group 3

```java
public static void SaveToTiffUsingCcitt3Compression() throws IOException {
    // Ścieżka do katalogu dokumentów.
    String dataDir = "Your Document Directory";

    // Załaduj dokument do Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setColorMode(ColorMode.BlackAndWhite);
    options.setTiffCompression(TiffCompression.Ccitt3);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingCcitt3Compression.tiff").toString(), options);
}
```

-  Załaduj dokument za pomocą`Document` klasa.
-  Utwórz instancję`ImageSaveOptions` i określ typ kompresji TIFF jako faks CCITT Group 3.
- Ustaw tryb koloru na czarno-biały.
- Zapisz dokument w formacie TIFF, korzystając z określonych opcji.

## Wniosek

W tym samouczku nauczyłeś się, jak zapisać dokument w formacie obrazu TIFF przy użyciu różnych metod kompresji w Aspose.Note dla Java. Postępując zgodnie z przewodnikiem krok po kroku, możesz efektywnie wykorzystać możliwości Aspose.Note, aby spełnić Twoje wymagania.

## Często zadawane pytania

### P1: Czy mogę używać Aspose.Note dla Java do konwersji innych formatów dokumentów na TIFF?

O1: Tak, Aspose.Note dla Java obsługuje konwersję różnych formatów dokumentów do TIFF, w tym dokumentów OneNote.

### P2: Jakie znaczenie ma określenie typu kompresji podczas zapisywania w formacie TIFF?

Odpowiedź 2: Określenie typu kompresji pozwala kontrolować jakość obrazu i rozmiar pliku. Różne metody kompresji oferują kompromis między jakością a stopniem kompresji.

### P3: Czy Aspose.Note dla Java nadaje się do wsadowego przetwarzania dokumentów?

O3: Tak, Aspose.Note dla Java udostępnia interfejsy API do przetwarzania wsadowego, umożliwiając wydajną automatyzację zadań konwersji dokumentów.

### P4: Czy mogę bardziej dostosować ustawienia kompresji?

O4: Tak, możesz dostosować parametry, takie jak jakość, rozdzielczość i metoda kompresji, aby dostosować wydruk do swoich wymagań.

### P5: Czy Aspose.Note dla Java oferuje wsparcie techniczne?

Odpowiedź 5: Tak, Aspose zapewnia kompleksowe wsparcie techniczne za pośrednictwem forów i systemów opartych na biletach.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
