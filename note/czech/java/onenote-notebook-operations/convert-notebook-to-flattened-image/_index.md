---
title: Převést Poznámkový blok na sloučený obrázek ve OneNotu – Aspose.Note
linktitle: Převést Poznámkový blok na sloučený obrázek ve OneNotu – Aspose.Note
second_title: Aspose.Note Java API
description: Přečtěte si, jak převést poznámkový blok na sloučený obrázek ve OneNotu pomocí Aspose.Note pro Java. Zachovejte všechny prvky v jediném souboru obrázku bez námahy.
weight: 13
url: /cs/java/onenote-notebook-operations/convert-notebook-to-flattened-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převést Poznámkový blok na sloučený obrázek ve OneNotu – Aspose.Note

## Úvod

tomto kurzu vás provedeme procesem převodu poznámkového bloku na sloučený obrázek ve OneNotu pomocí Aspose.Note for Java. To vám umožní uložit poznámkový blok jako obrázkový soubor a zajistit, že všechny prvky budou zachovány v jediném formátu obrázku.

## Předpoklady

Než začneme, ujistěte se, že máte následující:

1. Java Development Kit (JDK) nainstalovaný ve vašem systému.
2.  Aspose.Note pro knihovnu Java staženou a nastavenou ve vašem projektu Java. Knihovnu si můžete stáhnout z[tady](https://releases.aspose.com/note/java/).
3. Základní znalost programování v Javě.

## Importujte balíčky

Chcete-li začít, musíte importovat potřebné balíčky z Aspose.Note pro Java:

```java
import java.io.IOException;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Krok 1: Nastavte adresář dokumentů

Nejprve definujte adresář, kde se nachází soubor vašeho notebooku:

```java
String dataDir = "Your Document Directory";
```

 Nahradit`"Your Document Directory"` s cestou k souboru vašeho notebooku.

## Krok 2: Načtěte notebook

 Dále načtěte soubor notebooku pomocí`Notebook` třída:

```java
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

 Zajistěte výměnu`"test.onetoc2"` s názvem souboru vašeho notebooku.

## Krok 3: Nastavte možnosti uložení obrázku

Nyní nastavte možnosti pro uložení poznámkového bloku jako obrázku. Formát uložení určíme jako PNG a nastavíme rozlišení na 400 DPI:

```java
NotebookImageSaveOptions saveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
ImageSaveOptions documentSaveOptions = saveOptions.getDocumentSaveOptions();
documentSaveOptions.setResolution(400);
```

Rozlišení můžete upravit podle svých požadavků.

## Krok 4: Zploštění notebooku

Chcete-li zajistit, aby byly všechny prvky sloučeny do jednoho obrázku, nastavte`flatten` možnost`true`:

```java
saveOptions.setFlatten(true);
```

Tím je zajištěno, že výsledný obrázek zachová rozložení vašeho notebooku.

## Krok 5: Uložte obrázek

Nakonec uložte zápisník jako sloučený obrázek:

```java
notebook.save(dataDir + "ExportImageasFlattenedNotebook_out.png", saveOptions);
```

 Nahradit`"ExportImageasFlattenedNotebook_out.png"` s požadovaným názvem výstupního souboru.

## Závěr

Závěrem lze říci, že pomocí Aspose.Note for Java můžete snadno převést svůj poznámkový blok na sloučený obrázek ve OneNotu. Tento proces zajišťuje zachování všech prvků v jediném formátu obrázku, což usnadňuje sdílení a prohlížení.

## FAQ

### Q1: Mohu upravit rozlišení výstupního obrazu?

 A1: Ano, můžete upravit rozlišení podle svých požadavků úpravou`setResolution` parametr metody.

### Q2: Podporuje Aspose.Note jiné formáty obrázků pro export?

Odpověď 2: Ano, Aspose.Note podporuje různé formáty obrázků, jako je PNG, JPEG, BMP atd., pro export poznámkových bloků.

### Q3: Mohu si výstupní obrázek dále přizpůsobit?

Odpověď 3: Ano, Aspose.Note poskytuje rozsáhlé možnosti přizpůsobení výstupního obrazu, včetně nastavení velikosti stránky, orientace a kvality.

### Q4: Je k dispozici zkušební verze pro Aspose.Note pro Java?

 A4: Ano, můžete získat bezplatnou zkušební verzi od[tady](https://releases.aspose.com/).

### Q5: Kde najdu podporu pro Aspose.Note pro Java?

 A5: Podporu a zdroje najdete na fóru Aspose.Note[tady](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
