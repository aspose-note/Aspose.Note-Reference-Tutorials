---
title: Dark Theme Transformation s Aspose.Note pro .NET
linktitle: Použijte tmavý motiv na text v Aspose.Note
second_title: Aspose.Note .NET API
description: Transformujte své dokumenty OneNote pomocí Aspose.Note pro .NET! Bez námahy naneste elegantní tmavý motiv. Stáhněte si nyní a vylepšete svůj zážitek z psaní poznámek.
type: docs
weight: 11
url: /cs/net/text-manipulation/apply-dark-theme-text/
---
## Úvod
Vítejte v našem podrobném průvodci aplikací tmavého motivu na text v Aspose.Note pro .NET. Aspose.Note je výkonné rozhraní .NET API, které umožňuje vývojářům pracovat se soubory Microsoft OneNote programově. V tomto kurzu prozkoumáme, jak dodat dokumentům OneNote elegantní a moderní vzhled použitím tmavého motivu na text.
## Předpoklady
Než se pustíme do výukového programu, ujistěte se, že máte splněny následující předpoklady:
-  Aspose.Note pro .NET: Ujistěte se, že máte nainstalovaný Aspose.Note pro .NET. Pokud ne, můžete si jej stáhnout z[Aspose.Note dokumentaci](https://reference.aspose.com/note/net/).
- Vývojové prostředí: Nastavte si preferované vývojové prostředí .NET, jako je Visual Studio.
- Adresář dokumentů: Připravte adresář, kde se nachází váš dokument OneNotu.
## Import jmenných prostorů
Ve svém projektu .NET importujte potřebné jmenné prostory pro práci s Aspose. Poznámka:
```csharp
    using System;
    using System.Drawing;
    using System.IO;
```
## Krok 1: Načtěte dokument OneNotu
Načtěte dokument OneNotu do Aspose.Note pomocí následujícího kódu:
```csharp
// Cesta k adresáři dokumentů.
string dataDir = "Your Document Directory";
// Vložte dokument do Aspose.Note.
Document doc = new Document(Path.Combine(dataDir, "Aspose.one"));
```
## Krok 2: Nastavte barvu pozadí
Nastavte barvu pozadí každé stránky na černou:
```csharp
foreach (var page in doc)
{
    page.BackgroundColor = Color.Black;
}
```
## Krok 3: Upravte barvu textu
Pro lepší viditelnost upravte barvu písma textu na bílou:
```csharp
foreach (var node in doc.GetChildNodes<RichText>())
{
    var c = node.ParagraphStyle.FontColor;
    if (c.IsEmpty || Math.Abs(c.R - Color.Black.R) + Math.Abs(c.G - Color.Black.G) + Math.Abs(c.B - Color.Black.B) <= 30)
    {
        node.ParagraphStyle.FontColor = Color.White;
    }
}
```
## Krok 4: Uložte dokument
Uložte upravený dokument OneNotu jako PDF:
```csharp
doc.Save(Path.Combine(dataDir, "AsposeDarkTheme.pdf"));
```
## Závěr
Gratulujeme! Úspěšně jste použili tmavý motiv na text v dokumentu Aspose.Note. Toto jednoduché, ale účinné vylepšení může dát vašim souborům OneNote sofistikovanější vzhled.
## Často kladené otázky
### Mohu použít tmavý motiv na konkrétní části mého dokumentu OneNotu?
Ano, kód můžete přizpůsobit tak, aby cílil na konkrétní stránky nebo sekce v dokumentu.
### Podporuje Aspose.Note jiné exportní formáty kromě PDF?
Absolutně! Aspose.Note podporuje různé formáty exportu, včetně obrázků a Microsoft Word.
### Existuje nějaké omezení velikosti dokumentu, které Aspose.Note zvládne?
Aspose.Note dokáže zpracovat dokumenty různých velikostí a jeho výkon je optimalizován pro efektivitu.
### Mohu se po použití tmavého motivu vrátit k původnímu motivu?
Ano, kód můžete upravit a přepínat mezi motivy na základě vašich preferencí.
### Kde mohu získat podporu pro dotazy související s Aspose.Note?
 Pro jakoukoli pomoc navštivte[Aspose.Note fórum](https://forum.aspose.com/c/note/28) nebo prozkoumat[dokumentace](https://reference.aspose.com/note/net/).