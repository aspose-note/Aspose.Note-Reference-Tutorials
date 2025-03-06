---
title: Zapisz zakres stron jako plik PDF w Aspose.Note
linktitle: Zapisz zakres stron jako plik PDF w Aspose.Note
second_title: Aspose.Note .NET API
description: Dowiedz się, jak zapisać zakres stron z dokumentów OneNote jako pliki PDF przy użyciu Aspose.Note dla .NET. W zestawie tutorial krok po kroku.
weight: 21
url: /pl/net/loading-and-saving-operations/save-range-pages-as-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zapisz zakres stron jako plik PDF w Aspose.Note

## Wstęp

W dziedzinie programowania .NET Aspose.Note wyróżnia się jako wszechstronne narzędzie do łatwej i wydajnej obsługi dokumentów OneNote. Wśród mnóstwa funkcji jedną z najbardziej poszukiwanych jest możliwość zapisywania zakresu stron w formacie PDF. Ten samouczek poprowadzi Cię krok po kroku przez proces, zapewniając bezproblemową integrację tej funkcji ze swoimi projektami.

## Warunki wstępne

Zanim przejdziesz do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:

1.  Biblioteka Aspose.Note dla .NET: Upewnij się, że pobrałeś i zainstalowałeś bibliotekę Aspose.Note dla .NET. Można go nabyć od[ten link](https://releases.aspose.com/note/net/).
   
2. Podstawowa znajomość języka C#: Zapoznaj się z podstawami języka programowania C#, ponieważ w tym samouczku używana będzie składnia języka C#.
   
3. Środowisko programistyczne: skonfiguruj preferowane środowisko programistyczne, niezależnie od tego, czy jest to Visual Studio, czy inne IDE kompatybilne z programowaniem .NET.

## Importuj przestrzenie nazw

Aby rozpocząć, musisz zaimportować niezbędne przestrzenie nazw do swojego kodu C#. Umożliwi to dostęp do klas i metod udostępnianych przez bibliotekę Aspose.Note.

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
```

## Zapisz zakres stron jako plik PDF w Aspose.Note

Podzielmy teraz proces zapisywania zakresu stron jako pliku PDF przy użyciu Aspose.Note na kilka kroków:

### Krok 1: Załaduj dokument

Najpierw musisz załadować dokument OneNote, który chcesz zapisać w formacie PDF.

```csharp
// Ścieżka do katalogu dokumentów.
string dataDir = "Your Document Directory";

// Załaduj dokument do Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

### Krok 2: Zainicjuj obiekt PdfSaveOptions

 Następnie zainicjuj instancję`PdfSaveOptions` class, która udostępnia opcje zapisania dokumentu w formacie PDF.

```csharp
// Zainicjuj obiekt PdfSaveOptions
PdfSaveOptions opts = new PdfSaveOptions
{
    // Ustaw indeks pierwszej strony, która ma zostać zapisana
    PageIndex = 0,

    // Ustaw liczbę stron
    PageCount = 1,
};
```

### Krok 3: Zapisz dokument w formacie PDF

Teraz zapisz załadowany dokument jako plik PDF, korzystając z wcześniej zainicjowanych opcji.

```csharp
// Zapisz dokument w formacie PDF
dataDir = dataDir + "SaveRangeOfPagesAsPDF_out.pdf";
oneFile.Save(dataDir, opts);
```

## Wniosek

Gratulacje! Pomyślnie nauczyłeś się, jak zapisać zakres stron z dokumentu OneNote jako plik PDF przy użyciu Aspose.Note dla .NET. Zintegrowanie tej funkcji z projektami .NET umożliwi wydajne zarządzanie dokumentami programu OneNote zgodnie z konkretnymi wymaganiami.

## Często zadawane pytania

### P1: Czy mogę zapisać wiele zakresów stron jako osobne pliki PDF przy użyciu Aspose.Note?

Odpowiedź 1: Tak, możesz to osiągnąć, powtarzając proces dla każdego zakresu stron, które chcesz zapisać, dostosowując`PageIndex` I`PageCount` odpowiednio.
   
### P2: Czy Aspose.Note obsługuje zapisywanie dokumentów w formatach innych niż PDF?

O2: Tak, Aspose.Note obsługuje zapisywanie dokumentów w różnych formatach, takich jak między innymi pliki obrazów (JPEG, PNG itp.), Microsoft Word i HTML.
   
### P3: Czy Aspose.Note jest kompatybilny zarówno z .NET Framework, jak i .NET Core?

O3: Tak, Aspose.Note obsługuje środowiska .NET Framework i .NET Core, zapewniając elastyczność programistom.
   
### P4: Czy mogę dostosować wygląd zapisanych plików PDF?

A4: Absolutnie! Aspose.Note oferuje rozbudowane opcje dostosowywania wyglądu plików PDF, w tym rozmiaru strony, orientacji, marginesów i innych.
   
### P5: Gdzie mogę znaleźć dodatkowe wsparcie i zasoby dla Aspose.Note?

 Odpowiedź 5: Aby uzyskać dodatkowe wsparcie, dokumentację i interakcję ze społecznością, możesz odwiedzić stronę[Forum Aspose.Note](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
