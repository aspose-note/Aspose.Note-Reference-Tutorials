---
date: 2025-12-17
description: Naucz się eksportować OneNote, zapisując dokument jako szarobury obraz
  PNG przy użyciu Aspose.Note dla Javy. Zawiera kroki ładowania dokumentu OneNote
  i tworzenia obrazu w odcieniach szarości.
linktitle: How to Export OneNote as Grayscale Image – Aspose.Note
second_title: Aspose.Note Java API
title: Jak wyeksportować OneNote jako obraz w odcieniach szarości – Aspose.Note
url: /pl/java/onenote-document-saving/save-to-grayscale-image/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zapisz jako obraz w odcieniach szarości w OneNote - Aspose.Note

## Introduction

W tym samouczku pokażemy, **jak wyeksportować onenote** przez zapisanie dokumentu jako obraz w odcieniach szarości przy użyciu Aspose.Note dla Java. Obrazy w odcieniach szarości to monochromatyczne zdjęcia zawierające tylko odcienie szarości, co może być przydatne przy drukowaniu, archiwizacji lub zmniejszaniu rozmiaru pliku. Przejdziemy przez ładowanie dokumentu OneNote, konfigurowanie opcji zapisu, aby **utworzyć obraz w odcieniach szarości**, i w końcu **zapisz dokument jako PNG**.

## Quick Answers
- **Co oznacza „how to export onenote”?** Odnosi się do konwertowania pliku OneNote na inny format, np. obraz, programowo.  
- **Jaki format jest najlepszy dla wyjścia w odcieniach szarości?** PNG sprawdza się dobrze, ponieważ zachowuje jakość bezstratną i obsługuje tryb kolorów w odcieniach szarości.  
- **Czy potrzebna jest licencja?** Wymagana jest ważna licencja Aspose.Note do użytku produkcyjnego; tymczasowa licencja próbna jest dostępna do testów.  
- **Jaka wersja Javy jest wymagana?** Zalecana jest Java 8 lub nowsza.  
- **Czy mogę zmienić rozmiar obrazu?** Tak, możesz dostosować właściwości `ImageSaveOptions`, takie jak `Resolution` lub `PageSize`, przed zapisem.

## What is “how to export onenote”?

Eksportowanie OneNote oznacza programowe konwertowanie pliku OneNote `.one` na inną reprezentację — taką jak PDF, HTML lub obraz. W tym przewodniku skupiamy się na eksporcie do **obrazu PNG w odcieniach szarości**, co jest częstym wymogiem w dokumentacji lub procesach drukowania.

## Why export OneNote as a grayscale image?

- **Zmniejszony rozmiar pliku** – PNG w odcieniach szarości są zazwyczaj mniejsze niż obrazy pełnokolorowe.  
- **Lepsza czytelność** – W raportach drukowanych odcienie szarości często zapewniają wyraźniejszy kontrast.  
- **Kompatybilność** – PNG jest szeroko wspierany w przeglądarkach, edytorach i urządzeniach mobilnych.  

## Prerequisites

Zanim zaczniemy, upewnij się, że masz następujące elementy:

1. Zainstalowany Java Development Kit (JDK) na twoim systemie.  
2. Biblioteka Aspose.Note for Java. Możesz ją pobrać [tutaj](https://releases.aspose.com/note/java/).  
3. Podstawowa znajomość programowania w Javie.  

## Import Packages

Aby rozpocząć, zaimportuj niezbędne pakiety:

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## Step 1: Load the OneNote Document

Najpierw **load onenote document** do Aspose.Note. Zastąp `"Your Document Directory"` ścieżką do lokalnego folderu i `"Aspose.one"` nazwą pliku OneNote.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Step 2: Set Output Path and Options

Zdefiniuj ścieżkę wyjściową dla obrazu w odcieniach szarości i określ opcje zapisu. Ustawimy `ColorMode` na `GrayScale` i użyjemy formatu **save document as png**.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## Step 3: Save the Document

Na koniec zapisz dokument jako obraz PNG w odcieniach szarości, używając skonfigurowanych opcji.

```java
oneFile.save(dataDir, options);
```

## Common Issues and Solutions
- **FileNotFoundException** – Sprawdź, czy `dataDir` wskazuje na właściwy folder i czy plik `.one` istnieje.  
- **LicenseException** – Upewnij się, że zastosowano ważną licencję Aspose.Note przed wywołaniem `save`.  
- **Niska rozdzielczość wyjścia** – Dostosuj `options.setResolution(300)`, aby zwiększyć DPI w razie potrzeby.

## Frequently Asked Questions

**Q1: Czy mogę zapisać obraz w odcieniach szarości w innym formacie?**  
A1: Tak, po prostu zmień parametr `SaveFormat` w konstruktorze `ImageSaveOptions` na `Jpeg`, `Bmp` itp.

**Q2: Czy Aspose.Note jest kompatybilny ze wszystkimi wersjami dokumentów OneNote?**  
A2: Aspose.Note obsługuje Microsoft OneNote 2010 i późniejsze wersje.

**Q3: Czy Aspose.Note wymaga licencji do użycia?**  
A3: Wymagana jest ważna licencja do użytku produkcyjnego, ale tymczasowa licencja próbna może być uzyskana do oceny.

**Q4: Czy mogę modyfikować inne elementy dokumentu przed zapisaniem go jako obraz?**  
A4: Oczywiście! Aspose.Note udostępnia rozbudowane API do edycji sekcji, stron i treści przed eksportem.

**Q5: Gdzie mogę znaleźć wsparcie, jeśli napotkam problemy?**  
A5: Wsparcie można znaleźć na forum Aspose.Note [tutaj](https://forum.aspose.com/c/note/28).

## Conclusion

Teraz wiesz, **jak wyeksportować onenote**, ładując plik OneNote, konfigurując opcje zapisu, aby **utworzyć obraz w odcieniach szarości**, i **zapisując dokument jako PNG**. Ta technika jest przydatna do generowania lekkich, gotowych do druku wizualizacji z notatników OneNote. Śmiało eksperymentuj z innymi ustawieniami `ColorMode` lub formatami obrazu, aby dopasować je do potrzeb projektu.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Ostatnia aktualizacja:** 2025-12-17  
**Testowano z:** Aspose.Note 24.12 for Java  
**Autor:** Aspose