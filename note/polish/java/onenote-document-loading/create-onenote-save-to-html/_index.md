---
title: Utwórz dokument OneNote i zapisz w formacie HTML — Java
linktitle: Utwórz dokument OneNote i zapisz w formacie HTML — Java
second_title: Aspose.Note API Java
description: Dowiedz się, jak tworzyć i zapisywać dokumenty OneNote w formacie HTML przy użyciu Aspose.Note dla Java. Integracja z aplikacjami Java w celu programowej obsługi plików OneNote.

type: docs
weight: 18
url: /pl/java/onenote-document-loading/create-onenote-save-to-html/
---
## Wstęp

Aspose.Note dla Java to potężna biblioteka, która umożliwia programistom programową pracę z plikami Microsoft OneNote. W tym samouczku przyjrzymy się, jak utworzyć dokument OneNote i zapisać go w formacie HTML za pomocą Aspose.Note dla Java.

## Warunki wstępne

Zanim zaczniemy, upewnij się, że masz następujące elementy:

1. Zestaw Java Development Kit (JDK) zainstalowany w systemie.
2.  Aspose.Note dla biblioteki Java. Można go pobrać z[Tutaj](https://releases.aspose.com/note/java/).
3. Podstawowa znajomość programowania w języku Java.

## Importuj pakiety

Najpierw zaimportuj niezbędne pakiety do swojego projektu Java:

```java
import java.io.ByteArrayOutputStream;
import java.io.File;
import java.io.FileOutputStream;
import java.io.IOException;
import java.io.OutputStream;
import java.io.OutputStreamWriter;
import java.nio.file.Paths;
import com.aspose.note.CssSavingArgs;
import com.aspose.note.Document;
import com.aspose.note.FontFaceType;
import com.aspose.note.FontSavingArgs;
import com.aspose.note.HtmlSaveOptions;
import com.aspose.note.ICssSavingCallback;
import com.aspose.note.IFontSavingCallback;
import com.aspose.note.IImageSavingCallback;
import com.aspose.note.ImageSavingArgs;
import com.aspose.note.ResourceExportType;
```

## Krok 1: Utwórz obiekt dokumentu OneNote

```java
Document document = new Document("Path_to_your_sample_one_file");
```

 Ten kod inicjuje a`Document` obiekt, ładując przykładowy plik programu OneNote.

## Krok 2: Zapisz jako HTML w strumieniu pamięci

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

Tutaj konfigurujemy opcje zapisywania HTML i zapisujemy dokument w strumieniu pamięci.

## Krok 3: Zapisz jako HTML z zasobami w oddzielnych plikach

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

Ten krok powoduje zapisanie dokumentu w formacie HTML z zasobami takimi jak CSS, czcionki i obrazy w oddzielnych plikach.

## Krok 4: Zapisz jako HTML w strumieniu pamięci z wywołaniami zwrotnymi, aby zapisać zasoby

```java
Document document = new Document("Path_to_your_sample_one_file");

UserSavingCallbacks savingCallbacks = new UserSavingCallbacks();
savingCallbacks.setRootFolder("documentFolder");
savingCallbacks.setCssFolder("css");
savingCallbacks.setKeepCssStreamOpened(true);
savingCallbacks.setImagesFolder("images");
savingCallbacks.setFontsFolder("fonts");

HtmlSaveOptions options = new HtmlSaveOptions();
options.setFontFaceTypes(FontFaceType.Ttf);
options.setCssSavingCallback(savingCallbacks);
options.setImageSavingCallback(savingCallbacks);
options.setFontSavingCallback(savingCallbacks);
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);

File dir = new File(savingCallbacks.getRootFolder());
if (!dir.exists()) {
    dir.mkdir();
}

document.save(Paths.get(savingCallbacks.getRootFolder(), "document.html").toString(), options);
```

Tutaj zapisujemy dokument jako HTML w strumieniu pamięci, używając wywołań zwrotnych do obsługi oszczędzania zasobów.

## Wniosek

Gratulacje! Nauczyłeś się, jak utworzyć dokument OneNote i zapisać go w formacie HTML przy użyciu Aspose.Note dla Java. Możesz teraz zintegrować tę funkcję z aplikacjami Java, aby programowo pracować z plikami OneNote.

## Często zadawane pytania

### P1: Czy mogę za jednym razem przekonwertować wiele dokumentów programu OneNote na format HTML?

Odpowiedź 1: Tak, możesz przeglądać wiele dokumentów i powtarzać proces zapisywania.

### P2: Czy Aspose.Note dla Java obsługuje inne formaty wyjściowe oprócz HTML?

O2: Tak, Aspose.Note dla Java obsługuje różne formaty wyjściowe, w tym PDF, DOCX i formaty obrazów.

### P3: Czy dostępna jest wersja próbna Aspose.Note dla Java?

Odpowiedź 3: Tak, możesz pobrać bezpłatną wersję próbną ze strony[Tutaj](https://releases.aspose.com/).

### P4: Gdzie mogę uzyskać pomoc dotyczącą Aspose.Note dla Java?

 Odpowiedź 4: Możesz uzyskać wsparcie od[Forum Aspose.Note](https://forum.aspose.com/c/note/28).

### P5: Jak mogę kupić licencję na Aspose.Note dla Java?

 Odpowiedź 5: Możesz kupić licencję w witrynie[Strona Aspose](https://purchase.aspose.com/buy).