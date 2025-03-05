---
title: Převést konkrétní stránku na obrázek PNG ve OneNotu - Java
linktitle: Převést konkrétní stránku na obrázek PNG ve OneNotu - Java
second_title: Aspose.Note Java API
description: Naučte se používat Aspose.Note pro Java, převod stránky OneNotu na PNG. Postupujte podle jednoduchých kroků, načtěte dokument a nastavte možnosti. Vylepšete aplikace Java o tuto funkci.
type: docs
weight: 13
url: /cs/java/onenote-document-loading/convert-page-to-png-image/
---
## Úvod

V tomto kurzu se naučíte, jak používat Aspose.Note pro Java k převodu konkrétní stránky z dokumentu OneNotu na obrázek PNG. Tento proces rozdělíme do snadno srozumitelných kroků, které vám pomohou hladce integrovat tuto funkci do vaší Java aplikace.

## Předpoklady

Než začnete, ujistěte se, že máte následující:

1. Java Development Kit (JDK): Ujistěte se, že máte v systému nainstalovaný JDK.
2.  Aspose.Note for Java Library: Stáhněte a nainstalujte knihovnu Aspose.Note for Java z[webová stránka](https://releases.aspose.com/note/java/).
3. Dokument OneNotu: Připravte si dokument OneNotu, ze kterého chcete převést konkrétní stránku na PNG.

## Importujte balíčky

Nejprve je třeba importovat potřebné balíčky do souboru Java:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.LoadOptions;
import com.aspose.note.SaveFormat;
```

## Krok 1: Načtěte dokument OneNotu

```java
// Vložte dokument do Aspose.Note.
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", new LoadOptions());
```

 V tomto kroku načteme dokument OneNote pomocí Aspose.Note's`Document` třída.

## Krok 2: Inicializujte objekt ImageSaveOptions

```java
// Inicializujte objekt ImageSaveOptions
ImageSaveOptions opts = new ImageSaveOptions(SaveFormat.Png);
```

 Zde inicializujeme`ImageSaveOptions` objekt a zadejte formát uložení jako PNG.

## Krok 3: Nastavte index stránky

```java
// nastavit index stránky
opts.setPageIndex(0);
```

Nastavte index stránky, kterou chcete převést. Všimněte si, že indexování stránek začíná od 0.

## Krok 4: Uložte dokument jako PNG

```java
// Uložte dokument jako PNG.
oneFile.save(dataDir + "ConvertSpecificPageToPngImage_out.png", opts);
```

Nakonec uložte dokument se zadanou stránkou převedenou na obrázek PNG.

## Závěr

Gratulujeme! Úspěšně jste se naučili, jak převést konkrétní stránku z dokumentu OneNotu na obrázek PNG pomocí Aspose.Note for Java. Integrace této funkce do vašich aplikací Java vám umožní programově manipulovat s dokumenty OneNote, zvýší vaši produktivitu a rozšíří možnosti vašeho softwaru.

## FAQ

### Q1: Mohu pomocí Aspose.Note pro Java převést více stránek na obrázky PNG najednou?

Odpověď 1: Ano, můžete dosáhnout dávkového převodu procházením stránek a jejich ukládáním jednotlivě.

### Q2: Podporuje Aspose.Note pro Java jiné formáty obrázků kromě PNG?

Odpověď 2: Ano, Aspose.Note podporuje různé formáty obrázků, jako jsou JPEG, GIF, BMP a TIFF.

### Q3: Je k dispozici bezplatná zkušební verze pro Aspose.Note pro Java?

 A3: Ano, máte přístup k bezplatné zkušební verzi z[webová stránka](https://releases.aspose.com/).

### Q4: Mohu získat technickou pomoc, pokud narazím na nějaké problémy s Aspose.Note pro Java?

 A4: Rozhodně můžete požádat o podporu na fóru komunity Aspose[tady](https://forum.aspose.com/c/note/28).

### Q5: Kde si mohu zakoupit licenci pro Aspose.Note pro Java?

 A5: Můžete si koupit licenci od[nákupní stránku](https://purchase.aspose.com/buy).