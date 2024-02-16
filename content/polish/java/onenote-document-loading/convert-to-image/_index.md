---
title: Konwertuj dokument programu OneNote na obraz — Java
linktitle: Konwertuj dokument programu OneNote na obraz — Java
second_title: Aspose.Note API Java
description: Dowiedz się, jak przekonwertować OneNote na obraz za pomocą Aspose.Note dla Java. Wykonaj proste kroki, załaduj dokument, zainicjuj opcje i zapisz jako PNG.
type: docs
weight: 14
url: /pl/java/onenote-document-loading/convert-to-image/
---
## Wstęp

W tym samouczku przeprowadzimy Cię przez proces używania Aspose.Note dla Java do konwersji dokumentu OneNote na obraz. Podzielimy każdy krok na łatwe do wykonania instrukcje.

## Warunki wstępne

Zanim zaczniemy, upewnij się, że masz następujące elementy:

1. Zestaw Java Development Kit (JDK) zainstalowany w systemie.
2.  Aspose.Note dla biblioteki Java. Można go pobrać z[Tutaj](https://releases.aspose.com/note/java/).

## Importuj pakiety

Najpierw zaimportuj niezbędne pakiety do kodu Java:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

Podzielmy teraz dostarczony przykładowy kod na kilka kroków:

## Krok 1: Skonfiguruj katalog dokumentów

Zdefiniuj katalog, w którym znajduje się dokument programu OneNote:

```java
String dataDir = "Your Document Directory";
```

 Zastępować`"Your Document Directory"` ze ścieżką do dokumentu OneNote.

## Krok 2: Załaduj dokument

Załaduj dokument OneNote do Aspose.Note:

```java
Document oneFile = new Document(dataDir + "Sample1.one");
```

 Zapewnić`"Sample1.one"` odpowiada nazwie pliku dokumentu programu OneNote.

## Krok 3: Zainicjuj opcje ImageSaveOptions

 Zainicjuj`ImageSaveOptions` obiekt, aby określić format zapisu:

```java
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
```

Tutaj zapisujemy dokument jako obraz PNG. W razie potrzeby możesz wybrać inne formaty, takie jak JPEG lub BMP.

## Krok 4: Zapisz dokument jako obraz

Zapisz załadowany dokument jako obraz:

```java
oneFile.save(dataDir + "ConvertToImage_out.png", options);
```

Ta linia zapisuje dokument jako obraz PNG z określonymi opcjami.

## Krok 5: Wydrukuj potwierdzenie

Wydrukuj wiadomość potwierdzającą zapisanie pliku:

```java
System.out.println("File saved: " + dataDir + "ConvertToImage_out.png");
```

Ta linia informuje o pomyślnej konwersji i lokalizacji zapisanego pliku obrazu.

## Wniosek

Wykonując kroki opisane powyżej, możesz bez wysiłku przekonwertować dokument OneNote na obraz za pomocą Aspose.Note dla Java. Jest to prosty i skuteczny sposób obsługi konwersji dokumentów w aplikacjach Java.

## Często zadawane pytania

### P1: Czy mogę przekonwertować wiele dokumentów programu OneNote za jednym razem?

Odpowiedź 1: Tak, możesz przeglądać listę dokumentów i wykonywać operację konwersji dla każdego dokumentu.

### P2: Czy Aspose.Note obsługuje inne formaty wyjściowe oprócz obrazów?

O2: Tak, Aspose.Note obsługuje różne formaty wyjściowe, takie jak formaty PDF, HTML i Microsoft Word.

### P3: Czy Aspose.Note jest kompatybilny ze wszystkimi wersjami plików OneNote?

O3: Aspose.Note oferuje kompatybilność z plikami OneNote utworzonymi w różnych wersjach Microsoft OneNote.

### P4: Czy mogę dostosować rozdzielczość obrazów wyjściowych?

O4: Tak, możesz dostosować rozdzielczość i inne parametry, korzystając z opcji dostępnych w Aspose.Note.

### P5: Czy Aspose.Note wymaga połączenia z Internetem do konwersji dokumentów?

Odpowiedź 5: Nie, Aspose.Note działa lokalnie, bez konieczności połączenia z Internetem.