---
title: Převést dokument OneNotu na obrázek – Java
linktitle: Převést dokument OneNotu na obrázek – Java
second_title: Aspose.Note Java API
description: Naučte se převádět OneNote na obrázek pomocí Aspose.Note pro Java. Postupujte podle jednoduchých kroků, načtěte dokument, inicializujte možnosti a uložte jako PNG.
type: docs
weight: 14
url: /cs/java/onenote-document-loading/convert-to-image/
---
## Úvod

V tomto tutoriálu vás provedeme procesem použití Aspose.Note pro Java k převodu dokumentu OneNotu na obrázek. Každý krok rozdělíme do snadno pochopitelných pokynů.

## Předpoklady

Než začneme, ujistěte se, že máte následující:

1. Java Development Kit (JDK) nainstalovaný ve vašem systému.
2.  Aspose.Note pro knihovnu Java. Můžete si jej stáhnout z[tady](https://releases.aspose.com/note/java/).

## Importujte balíčky

Nejprve importujte potřebné balíčky do kódu Java:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

Nyní rozdělíme poskytnutý příklad kódu do několika kroků:

## Krok 1: Nastavte adresář dokumentů

Definujte adresář, kde se nachází váš dokument OneNotu:

```java
String dataDir = "Your Document Directory";
```

 Nahradit`"Your Document Directory"` s cestou k vašemu dokumentu OneNotu.

## Krok 2: Vložte dokument

Načtěte dokument OneNotu do Aspose.Note:

```java
Document oneFile = new Document(dataDir + "Sample1.one");
```

 Zajistit`"Sample1.one"` odpovídá názvu souboru dokumentu OneNotu.

## Krok 3: Inicializujte ImageSaveOptions

 Inicializujte`ImageSaveOptions` objekt pro určení formátu uložení:

```java
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
```

Zde dokument ukládáme jako obrázek PNG. V případě potřeby si můžete vybrat jiné formáty jako JPEG nebo BMP.

## Krok 4: Uložte dokument jako obrázek

Uložte načtený dokument jako obrázek:

```java
oneFile.save(dataDir + "ConvertToImage_out.png", options);
```

Tento řádek uloží dokument jako obrázek PNG se zadanými možnostmi.

## Krok 5: Vytiskněte potvrzení

Vytiskněte zprávu pro potvrzení uložení souboru:

```java
System.out.println("File saved: " + dataDir + "ConvertToImage_out.png");
```

Tento řádek vás upozorní na úspěšný převod a umístění uloženého souboru obrázku.

## Závěr

Podle výše uvedených kroků můžete bez námahy převést dokument OneNotu na obrázek pomocí Aspose.Note for Java. Je to jednoduchý a efektivní způsob, jak zvládnout převod dokumentů ve vašich aplikacích Java.

## FAQ

### Q1: Mohu převést více dokumentů OneNotu najednou?

Odpověď 1: Ano, můžete procházet seznam dokumentů a provádět převod pro každý dokument.

### Q2: Podporuje Aspose.Note jiné výstupní formáty kromě obrázků?

Odpověď 2: Ano, Aspose.Note podporuje různé výstupní formáty, jako jsou PDF, HTML a formáty Microsoft Word.

### Q3: Je Aspose.Note kompatibilní se všemi verzemi souborů OneNotu?

A3: Aspose.Note nabízí kompatibilitu se soubory OneNote vytvořenými v různých verzích Microsoft OneNote.

### Q4: Mohu přizpůsobit rozlišení výstupních obrázků?

A4: Ano, můžete upravit rozlišení a další parametry pomocí možností dostupných v Aspose.Note.

### Q5: Vyžaduje Aspose.Note připojení k internetu pro převod dokumentů?

A5: Ne, Aspose.Note funguje místně bez nutnosti připojení k internetu.