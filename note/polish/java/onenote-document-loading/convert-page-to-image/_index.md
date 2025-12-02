---
date: 2025-11-29
description: „Dowiedz się, jak eksportować strony OneNote do obrazów przy użyciu Javy
  i odkryj, jak konwertować obrazy stron OneNote za pomocą Aspose.Note. Skorzystaj
  z naszego przewodnika krok po kroku, aby szybko zintegrować rozwiązanie.”
language: pl
linktitle: How to Export OneNote Page to Image Using Java
second_title: Aspose.Note Java API
title: Jak wyeksportować stronę OneNote do obrazu przy użyciu Javy
url: /java/onenote-document-loading/convert-page-to-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak wyeksportować stronę OneNote do obrazu przy użyciu Javy

## Introduction

W tym samouczku dowiesz się, **jak wyeksportować strony OneNote** do plików obrazu przy użyciu Javy i Aspose.Note. Konwertowanie strony OneNote na obraz jest przydatne, gdy musisz osadzić zawartość notatnika w raportach, udostępnić zrzuty ekranu użytkownikom nie‑korzystającym z OneNote lub wygenerować miniatury dla systemów zarządzania dokumentami. Przejdziemy krok po kroku, wyjaśnimy, dlaczego każda linia ma znaczenie, i pokażemy, jak dostosować wynik.

## Quick Answers
- **Jakiej biblioteki wymagana jest?** Aspose.Note for Java  
- **Czy mogę wybrać format obrazu?** Tak – JPEG, PNG, BMP itd. za pomocą `ImageSaveOptions`  
- **Czy potrzebna jest licencja do produkcji?** Wymagana jest ważna licencja Aspose.Note do użytku komercyjnego.  
- **Którą stronę mogę wyeksportować?** Dowolną stronę, ustawiając `PageIndex` (indeks zerowy).  
- **Jak długo trwa konwersja?** Zazwyczaj poniżej sekundy dla standardowej strony.

## Co oznacza eksportowanie stron OneNote do obrazów?

Eksportowanie stron OneNote oznacza renderowanie bogatej zawartości strony — tekstu, rysunków, tabel — do statycznego pliku obrazu (np. JPEG). Proces ten tworzy przenośną wizualną reprezentację, którą można wyświetlać wszędzie, nawet tam, gdzie nie zainstalowano klienta OneNote.

## Why use Aspose.Note for converting OneNote pages?

- **Pełna wierność** – zachowuje układ, czcionki i pociągnięcia atramentu.  
- **Brak zależności od Microsoft Office** – działa na każdej platformie obsługującej Javę.  
- **Precyzyjna kontrola** – wybierz format obrazu, jakość i konkretny indeks strony.  
- **Skalowalny** – odpowiedni do przetwarzania wsadowego wielu stron.

## Prerequisites

Zanim zaczniemy, upewnij się, że masz następujące wymagania wstępne:

1. **Java Development Kit (JDK)** – Zainstaluj JDK 11 lub nowszy. Możesz go pobrać ze [strony oficjalnej Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html), jeśli jeszcze tego nie zrobiłeś.  
2. **Aspose.Note for Java** – Pobierz najnowszą bibliotekę ze [strony pobierania Aspose.Note](https://releases.aspose.com/note/java/). Dodaj plik JAR do ścieżki klas swojego projektu.

## Import Packages

Najpierw zaimportujmy niezbędne pakiety, które dają dostęp do obsługi dokumentów i opcji zapisu obrazu.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Step 1: Load the OneNote Document

Zaczynamy od załadowania pliku `.one` do obiektu `Aspose.Note` `Document`.

```java
String dataDir = "Your Document Directory";
// Load the document into Aspose.Note
Document oneFile = new Document(dataDir + "Sample1.one");
```

> **Wskazówka:** Użyj ścieżki bezwzględnej lub strumienia zasobów, jeśli Twój plik znajduje się wewnątrz pliku JAR.

## Step 2: Initialize Image Save Options

Utwórz instancję `ImageSaveOptions`, aby określić format wyjściowy (w tym przykładzie JPEG). Możesz przełączyć się na PNG, BMP lub GIF, zmieniając `SaveFormat`.

```java
// Initialize ImageSaveOptions object
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
```

## Step 3: Specify the Page Index

Strony są indeksowane od zera, więc `1` wybiera **drugą** stronę. Dostosuj tę wartość, aby wyeksportować dowolną potrzebną stronę.

```java
// Specify second page for conversion
options.setPageIndex(1);
```

## Step 4: Save the Document as an Image

Teraz wywołujemy `save` na obiekcie `Document`, przekazując nazwę pliku docelowego oraz skonfigurowane opcje.

```java
// Save the document
oneFile.save(dataDir + "ConvertSpecificPageToImage_out.jpg", options);
```

## Step 5: Print Confirmation

Prosta wiadomość w konsoli potwierdza, że obraz został wygenerowany pomyślnie.

```java
// Print confirmation message
System.out.println("File saved: " + dataDir + "ConvertSpecificPageToImage_out.jpg");
```

## How to convert OneNote pages to images (alternative scenarios)

Jeśli potrzebujesz **konwertować pliki obrazu stron OneNote** masowo, po prostu umieść powyższy kod w pętli iterującej po `Document.getPages()`. Zmieniaj `options.setPageIndex(i)` dla każdej iteracji i opcjonalnie dostosuj `options.setQuality(90)`, aby kontrolować kompresję JPEG.

## Common Issues and Solutions

| Problem | Przyczyna | Rozwiązanie |
|---------|-----------|-------------|
| **Obraz jest pusty** | Indeks strony poza zakresem lub dokument nie został poprawnie załadowany. | Sprawdź, czy `options.setPageIndex` mieści się w przedziale `0 .. document.getPages().size() - 1`. |
| **Nieobsługiwany format** | Używasz starszej wersji Aspose.Note, która nie obsługuje niektórych formatów. | Zaktualizuj do najnowszej wersji Aspose.Note for Java. |
| **OutOfMemoryError** | Konwersja bardzo dużych stron na JVM z małą ilością pamięci. | Zwiększ rozmiar sterty (`-Xmx2g`) lub przetwarzaj strony pojedynczo. |

## Frequently Asked Questions

**P1: Czy mogę konwertować wiele stron na obrazy przy użyciu tej metody?**  
O: Tak. Umieść logikę zapisu w pętli i zmień `options.setPageIndex(i)` dla każdej strony, którą chcesz wyeksportować.

**P2: Czy Aspose.Note jest kompatybilny z różnymi wersjami plików OneNote?**  
O: Zdecydowanie. Aspose.Note obsługuje pliki .one z OneNote 2007, 2010, 2013 i nowszych wersji.

**P3: Czy mogę dostosować format obrazu i jakość podczas konwersji?**  
O: Tak. Wybierz `SaveFormat.Png`, `SaveFormat.Bmp` itp., oraz ustaw `options.setQuality(int)` dla jakości JPEG (0‑100).

**P4: Czy Aspose.Note oferuje wsparcie dla innych języków programowania?**  
O: Tak. Biblioteki są dostępne dla .NET, Pythona, C++ i innych.

**P5: Gdzie mogę znaleźć dodatkowe wsparcie lub pomoc?**  
O: Odwiedź [forum Aspose.Note](https://forum.aspose.com/c/note/28) lub zapoznaj się z oficjalną dokumentacją [tutaj](https://reference.aspose.com/note/java/).

---

**Ostatnia aktualizacja:** 2025-11-29  
**Testowano z:** Aspose.Note for Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}