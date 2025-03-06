---
title: Ustaw rozdzielczość obrazu wyjściowego w programie OneNote - Aspose.Note
linktitle: Ustaw rozdzielczość obrazu wyjściowego w programie OneNote - Aspose.Note
second_title: Aspose.Note API Java
description: Dowiedz się, jak dostosować rozdzielczość obrazu w dokumentach OneNote przy użyciu Aspose.Note dla Java. Postępuj zgodnie z naszym przewodnikiem krok po kroku, aby ułatwić wdrożenie
weight: 23
url: /pl/java/onenote-document-saving/set-output-image-resolution/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ustaw rozdzielczość obrazu wyjściowego w programie OneNote - Aspose.Note

## Wstęp

Czy chcesz manipulować rozdzielczością obrazów w dokumentach programu OneNote przy użyciu języka Java? Aspose.Note dla Java oferuje solidne rozwiązanie do takich zadań. W tym samouczku omówimy kroki ustawiania rozdzielczości obrazu wyjściowego za pomocą Aspose.Note.

## Warunki wstępne

Zanim zaczniemy, upewnij się, że masz następujące wymagania wstępne:

1. Zestaw Java Development Kit (JDK): zainstaluj pakiet JDK w swoim systemie.
2. Aspose.Note dla Java: Pobierz i zainstaluj Aspose.Note dla Java z[strona internetowa](https://releases.aspose.com/note/java/).
3. Zintegrowane środowisko programistyczne (IDE): Wybierz preferowane środowisko IDE, takie jak Eclipse lub IntelliJ IDEA.

## Importuj pakiety

W projekcie Java zaimportuj niezbędne pakiety Aspose.Note:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Krok 1: Załaduj dokument OneNote

Zacznij od załadowania dokumentu OneNote do aplikacji Java:

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```

 Zastępować`"Your Document Directory"` z rzeczywistym katalogiem, w którym znajduje się dokument programu OneNote.

## Krok 2: Ustaw opcje zapisywania obrazu

Zdefiniuj opcje zapisywania obrazu i określ żądaną rozdzielczość:

```java
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Jpeg);
imageSaveOptions.setResolution(120);
```

 Tutaj ustawiamy rozdzielczość na`120 dpi`. Możesz dostosować tę wartość do swoich wymagań.

## Krok 3: Zapisz dokument ze zmienioną rozdzielczością

Zapisz dokument ze zaktualizowaną rozdzielczością obrazu:

```java
doc.save(dataDir + "SetOutputImageResolution_out.jpeg", imageSaveOptions);
```

Spowoduje to zapisanie zmodyfikowanego dokumentu w określonej rozdzielczości.

## Wniosek

W tym samouczku omówiliśmy, jak ustawić rozdzielczość obrazu wyjściowego w dokumentach OneNote przy użyciu Aspose.Note dla Java. Wykonując te proste kroki, możesz efektywnie manipulować rozdzielczością obrazów, aby spełnić wymagania aplikacji.


## Często zadawane pytania

### P1: Czy mogę ustawić rozdzielczość obrazu na wartość wyższą niż 120 dpi?

Odpowiedź 1: Tak, możesz ustawić dowolną rozdzielczość w zależności od potrzeb.

### P2: Czy Aspose.Note obsługuje inne formaty obrazów oprócz JPEG?

O2: Tak, Aspose.Note obsługuje różne formaty obrazów, takie jak PNG, BMP, GIF itp.

### P3: Czy Aspose.Note jest kompatybilny ze wszystkimi wersjami Java?

O3: Aspose.Note jest kompatybilny z wersją Java 1.6 lub nowszą.

### P4: Czy mogę manipulować innymi aspektami obrazów w dokumentach OneNote za pomocą Aspose.Note?

O4: Tak, Aspose.Note zapewnia kompleksowe funkcje do manipulacji obrazami, w tym zmianę rozmiaru, kadrowanie i obracanie.

### P5: Gdzie mogę uzyskać pomoc dotyczącą zapytań związanych z Aspose.Note?

 O5: Możesz zwrócić się o pomoc na forum społeczności Aspose.Note[Tutaj](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
