---
title: Otevřít a zavřít projekty pomocí značek v Aspose.Note
linktitle: Otevřít a zavřít projekty pomocí značek v Aspose.Note
second_title: Aspose.Note .NET API
description: Naučte se, jak programově manipulovat se soubory Microsoft OneNote pomocí Aspose.Note pro .NET. Efektivně otevírejte a zavírejte projekty pomocí značek.
weight: 15
url: /cs/net/tag-management/open-close-projects-tags/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Otevřít a zavřít projekty pomocí značek v Aspose.Note

## Úvod

tomto tutoriálu se naučíme, jak používat Aspose.Note pro .NET k otevírání a zavírání projektů pomocí značek. Aspose.Note je výkonné rozhraní API, které umožňuje vývojářům pracovat se soubory Microsoft OneNote programově, což umožňuje úkoly, jako je manipulace s textem, obrázky a tagy v dokumentech.

## Předpoklady

Než začneme, ujistěte se, že máte nastaveny následující předpoklady:

## Import jmenných prostorů

```csharp
using System.IO;
using System.Linq;
```

Nyní si každý příklad rozdělíme do několika kroků:

## Krok 1: Vložte dokument

Nejprve musíme načíst dokument do Aspose.Note.

```csharp
string dataDir = "Your Document Directory";
var oneFile = new Document(Path.Combine(dataDir, "ProjectNotes.one"));
```

## Krok 2: Zavřete položky projektu C

Nyní zavřeme všechny položky zaškrtávacího políčka související s „Projektem C“.

```csharp
foreach (var node in oneFile.GetChildNodes<ITaggable>())
{
    foreach (var checkBox in node.Tags.OfType<CheckBox>())
    {
        if (checkBox.Label.Contains("Project C") && !checkBox.Checked)
        {
            checkBox.SetCompleted();
        }
    }
}
```

## Krok 3: Uložte uzavřené poznámky k projektu C

Uložte upravený dokument se zavřenými položkami „Projektu C“.

```csharp
oneFile.Save("Path to save the closed Project C notes");
```

## Krok 4: Otevřete položky Project C

Dále otevřeme všechny položky zaškrtávacího políčka související s „Projektem C“.

```csharp
var oneFile = new Document("Path to the closed Project C notes");

foreach (var node in oneFile.GetChildNodes<ITaggable>())
{
    foreach (var checkBox in node.Tags.OfType<CheckBox>())
    {
        if (checkBox.Label.Contains("Project C") && checkBox.Checked)
        {
            checkBox.SetOpen();
        }
    }
}
```

## Krok 5: Uložte poznámky Open Project C

Uložte upravený dokument s otevřenými položkami 'Projekt C'.

```csharp
oneFile.Save(Path.Combine(dataDir, "ProjectNoteWithOpenProjectC.one"));
```

Nyní jste se naučili, jak otevírat a zavírat projekty pomocí značek v Aspose.Note pomocí .NET.

## Závěr

Aspose.Note pro .NET poskytuje pohodlný způsob, jak programově manipulovat s dokumenty OneNotu. Podle tohoto kurzu můžete efektivně spravovat své projekty otevíráním a zavíráním položek pomocí značek.

## FAQ

### Q1: Je Aspose.Note kompatibilní se všemi verzemi OneNotu?

Odpověď 1: Aspose.Note podporuje Microsoft OneNote 2010 a novější verze.

### Q2: Mohu použít Aspose.Note pro komerční projekty?

 A2: Ano, Aspose.Note můžete použít pro osobní i komerční projekty. Návštěva[tady](https://purchase.aspose.com/buy) k zakoupení licence.

### Q3: Nabízí Aspose.Note bezplatnou zkušební verzi?

 A3: Ano, můžete získat bezplatnou zkušební verzi[tady](https://releases.aspose.com/).

### Q4: Kde najdu dokumentaci k Aspose.Note?

 A4: Můžete najít dokumentaci[tady](https://reference.aspose.com/note/net/).

### Q5: Kde mohu získat podporu pro Aspose.Note?

 A5: Pro podporu můžete navštívit Aspose.Note[Fórum](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
