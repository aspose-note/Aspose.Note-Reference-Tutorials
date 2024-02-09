---
title: Generovat dokument ze šablony v Aspose.Note
linktitle: Generovat dokument ze šablony v Aspose.Note
second_title: Aspose.Note .NET API
description: Vytvářejte dynamické dokumenty bez námahy s Aspose.Note pro .NET. Postupujte podle našeho podrobného průvodce vytvářením personalizovaných dokumentů založených na datech.
type: docs
weight: 18
url: /cs/net/text-manipulation/generate-document-from-template/
---
## Úvod
V neustále se vyvíjejícím prostředí tvorby dokumentů vyniká Aspose.Note for .NET jako výkonný nástroj pro snadné generování dynamických dokumentů. Ať už se zabýváte zprávami, fakturami nebo personalizovanými dokumenty, tento tutoriál vás provede procesem generování dokumentu ze šablony pomocí Aspose.Note pro .NET.
## Předpoklady
Než se ponoříte do podrobného průvodce, ujistěte se, že máte splněny následující předpoklady:
1.  Aspose.Note for .NET Library: Stáhněte a nainstalujte knihovnu z[Aspose.Note pro dokumentaci .NET](https://reference.aspose.com/note/net/).
2. Šablona dokumentu: Připravte šablonu dokumentu ve formátu OneNote (s příponou .one). To bude sloužit jako základ pro váš dynamicky generovaný dokument.
## Importovat jmenné prostory
Nezapomeňte do projektu zahrnout potřebné jmenné prostory:
```csharp
    using System;
    using System.Collections.Generic;
    using System.IO;
```
Nyní si rozeberme jednotlivé kroky průvodce.
## Krok 1: Definujte svůj adresář dokumentů
```csharp
string dataDir = "Your Document Directory";
```
Nahraďte "Adresář vašich dokumentů" cestou, kam chcete uložit vygenerovaný dokument.
## Krok 2: Vytvořte slovník s náhradními hodnotami
```csharp
var templateData = new Dictionary<string, string>
{
    { "Company", "Atlas Shrugged Ltd" },
    { "CandidateName", "John Galt" },
    { "JobTitle", "Chief Entrepreneur Officer" },
    { "Department", "Sales" },
    { "Salary", "123456 USD" },
    { "Vacation", "30" },
    { "StartDate", "29 Feb 2024" },
    { "YourName", "Ayn Rand" }
};
```
Definujte slovník, kde jsou klíče ve vaší šabloně zástupné symboly a hodnoty jsou data, kterými je chcete nahradit.

## Krok 3: Načtěte dokument šablony
```csharp
var templateDocument = new Document(Path.Combine(dataDir, "JobOffer.one"));
```
Načtěte dokument šablony OneNote do Aspose.Note.

## Krok 4: Nahraďte slova šablony dynamickými daty
```csharp
foreach (var paragraph in templateDocument.GetChildNodes<RichText>())
{
    foreach (var replacement in templateData)
    {
        paragraph.Replace($"${{{replacement.Key}}}", replacement.Value);
    }
}
```
Iterujte každý odstavec v šabloně a nahraďte zástupné symboly dynamickými daty.

## Krok 5: Uložte vygenerovaný dokument
```csharp
templateDocument.Save(Path.Combine(dataDir, "JobOffer_out.one"));
```
Uložte dynamicky generovaný dokument do určeného adresáře.

## Závěr
Gratulujeme! Úspěšně jste vygenerovali dynamický dokument pomocí Aspose.Note pro .NET. Tento proces otevírá svět možností pro bezproblémové vytváření personalizovaných dokumentů založených na datech.

## Často kladené otázky
### Mohu použít Aspose.Note pro .NET s jinými formáty dokumentů?
Ano, Aspose.Note pro .NET se primárně zabývá dokumenty OneNote, ale Aspose poskytuje různé knihovny pro různé formáty.
### Je k dispozici bezplatná zkušební verze pro Aspose.Note pro .NET?
 Ano, můžete prozkoumat možnosti Aspose.Note pro .NET pomocí bezplatné zkušební verze. Návštěva[tady](https://releases.aspose.com/) Pro více informací.
### Jak mohu získat podporu pro Aspose.Note pro .NET?
 Navštivte[Aspose.Note pro .NET fórum](https://forum.aspose.com/c/note/28) získat pomoc od komunity a odborníků.
### Jsou k dispozici dočasné licence pro Aspose.Note pro .NET?
 Ano, můžete získat dočasnou licenci[tady](https://purchase.aspose.com/temporary-license/) pro účely testování a hodnocení.
### Kde najdu komplexní dokumentaci k Aspose.Note pro .NET?
 Odkazovat na[dokumentace](https://reference.aspose.com/note/net/) pro podrobné informace o používání Aspose.Note pro .NET.