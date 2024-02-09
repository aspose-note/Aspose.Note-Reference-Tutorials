---
title: Załaduj dokument OneNote do Aspose.Note
linktitle: Załaduj dokument OneNote do Aspose.Note
second_title: Aspose.Note .NET API
description: Dowiedz się, jak programowo ładować, szyfrować i odszyfrowywać dokumenty OneNote w .NET przy użyciu Aspose.Note.
type: docs
weight: 16
url: /pl/net/loading-and-saving-operations/load-onenote-document/
---
## Wstęp

Aspose.Note dla .NET to potężny interfejs API, który umożliwia programistom programową pracę z plikami Microsoft OneNote w aplikacjach .NET. Niezależnie od tego, czy chcesz ładować, manipulować czy konwertować dokumenty OneNote, Aspose.Note dla .NET zapewnia wszechstronną funkcjonalność usprawniającą przepływ pracy.

## Warunki wstępne

Przed przystąpieniem do samouczka upewnij się, że spełniasz następujące wymagania wstępne:

1. Visual Studio: Zainstaluj Visual Studio, kompleksowe zintegrowane środowisko programistyczne (IDE) do programowania w środowisku .NET.
2.  Aspose.Note dla .NET: Pobierz i zainstaluj Aspose.Note dla .NET z[strona pobierania](https://releases.aspose.com/note/net/).
3. Podstawowa znajomość języka C#: Znajomość podstaw języka programowania C# jest niezbędna do zrozumienia i wdrożenia przykładów podanych w tym samouczku.

## Importuj przestrzenie nazw

Zanim zaczniesz pracować z Aspose.Note dla .NET, pamiętaj o zaimportowaniu wymaganych przestrzeni nazw do swojego projektu C#:

```csharp
using System;
using System.IO;
```

Podzielmy każdy przykład na wiele kroków:

## Załaduj dokument OneNote do Aspose.Note

### Krok 1: Proste ładowanie notebooka:
   -  Rozpocznij od utworzenia nowej instancji pliku`Notebook` class, przekazując ścieżkę do dokumentu OneNote.
   - Wykonaj iterację po węzłach podrzędnych notesu, używając pętli foreach.
   - Wyświetl nazwę wyświetlaną każdego węzła podrzędnego.
   - Wykonaj określone działania w zależności od tego, czy węzeł podrzędny jest dokumentem, czy innym notatnikiem.

```csharp
public static void SimpleLoadNotebook()
{
    // Ścieżka do katalogu dokumentów.
    string dataDir = "Your Document Directory";
    string fileName = "Open Notebook.onetoc2";
    try
    {
        var notebook = new Notebook(Path.Combine(dataDir, fileName));
        foreach (var notebookChildNode in notebook)
        {
            Console.WriteLine(notebookChildNode.DisplayName);
            if (notebookChildNode is Document)
            {
                // Zrób coś z dokumentem podrzędnym
            }
            else if (notebookChildNode is Notebook)
            {
                // Zrób coś z notatnikiem dziecka
            }
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine(ex.Message);
    }
}
```

### Krok 2: Sprawdź, czy dokument jest zaszyfrowany i załaduj:
   - Sprawdź, czy dokument OneNote jest zaszyfrowany, wywołując metodę`Document.IsEncrypted` metodę, przekazując nazwę pliku.
   - Jeśli nie jest zaszyfrowany, kontynuuj przetwarzanie dokumentu.
   - Jeśli są zaszyfrowane, poproś użytkownika o podanie hasła do odszyfrowania.

```csharp
public static void Document_CheckIfEncryptedAndLoad()
{
    // Ścieżka do katalogu dokumentów.
    string dataDir = "Your Document Directory";
    string fileName = Path.Combine(dataDir, "Aspose.one");

    Document document;
    if (!Document.IsEncrypted(fileName, out document))
    {
        Console.WriteLine("The document is loaded and ready to be processed.");
    }
    else
    {
        Console.WriteLine("The document is encrypted. Provide a password.");
    }
}
```

### Krok 3: Sprawdź, czy dokument jest zaszyfrowany hasłem i załaduj:
   - Podobnie jak w poprzednim kroku, sprawdź, czy dokument jest zaszyfrowany określonym hasłem.
   - Jeśli jest zaszyfrowany i podano prawidłowe hasło, kontynuuj przetwarzanie dokumentu.
   - Jeśli hasło zostało zaszyfrowane, ale podano nieprawidłowe hasło, poproś użytkownika o podanie nieprawidłowego hasła.

```csharp
public static void Document_CheckIfEncryptedByPasswordAndLoad()
{
    // Ścieżka do katalogu dokumentów.
    string dataDir = "Your Document Directory";
    string fileName = Path.Combine(dataDir, "Aspose.one");

    Document document;
    if (Document.IsEncrypted(fileName, "VerySecretPassword", out document))
    {
        if (document != null)
        {
            Console.WriteLine("The document is decrypted. It is loaded and ready to be processed.");
        }
        else
        {
            Console.WriteLine("The document is encrypted. Invalid password was provided.");
        }
    }
    else
    {
        Console.WriteLine("The document is NOT encrypted. It is loaded and ready to be processed.");
    }
}
```

### Krok 4: Obsługa nieobsługiwanego formatu OneNote 2007:
   - Spróbuj załadować dokument OneNote w formacie 2007.
   -  Jeśli format nie jest obsługiwany, złap`UnsupportedFileFormatException` i obsłużyć się z nim odpowiednio, informując użytkownika o nieobsługiwanym formacie.

```csharp
public static void Document_OneNote2007_Is_NotSupported()
{
    // Ścieżka do katalogu dokumentów.
    string dataDir = "Your Document Directory";
    string fileName = Path.Combine(dataDir, "OneNote2007.one");

    try
    {
        new Document(fileName);
    }
    catch (UnsupportedFileFormatException e)
    {
        if (e.FileFormat == FileFormat.OneNote2007)
        {
            Console.WriteLine("It looks like the provided file is in OneNote 2007 format that is not supported.");
        }
        else
            throw;
    }
}
```

## Wniosek

tym samouczku omówiliśmy, jak ładować dokumenty OneNote w Aspose.Note dla .NET przy użyciu różnych metod. Postępując zgodnie z tymi szczegółowymi instrukcjami, możesz bezproblemowo zintegrować możliwości przetwarzania dokumentów programu OneNote z aplikacjami .NET.

## Często zadawane pytania

### P1: Czy Aspose.Note dla .NET jest kompatybilny ze wszystkimi wersjami Microsoft OneNote?

O1: Aspose.Note dla .NET obsługuje różne wersje OneNote. Mogą jednak występować ograniczenia w przypadku starszych formatów, takich jak OneNote 2007.

### P2: Czy mogę programowo szyfrować i odszyfrowywać dokumenty OneNote za pomocą Aspose.Note dla .NET?

Odpowiedź 2: Tak, możesz sprawdzić, czy dokument jest zaszyfrowany i odszyfrować go za pomocą Aspose.Note dla .NET.

### P3: Gdzie mogę znaleźć więcej zasobów i wsparcia dla Aspose.Note dla .NET?

 A3: Możesz odwiedzić[Aspose.Note dla dokumentacji .NET](https://reference.aspose.com/note/net/) obszerne przewodniki i przykłady. Dodatkowo możesz zwrócić się o pomoc do[Aspose.Note dla forum .NET](https://forum.aspose.com/c/note/28).

### P4: Czy dostępna jest bezpłatna wersja próbna Aspose.Note dla .NET?

 Odpowiedź 4: Tak, możesz pobrać bezpłatną wersję próbną ze strony[Strona Aspose](https://releases.aspose.com/).

### P5: Jak mogę uzyskać tymczasową licencję na Aspose.Note dla .NET?

 Odpowiedź 5: Możesz poprosić o licencję tymczasową od[Strona zakupu Aspose](https://purchase.aspose.com/temporary-license/).