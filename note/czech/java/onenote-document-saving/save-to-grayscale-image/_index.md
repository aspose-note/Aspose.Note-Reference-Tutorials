---
title: Uložit do obrázku ve stupních šedi ve OneNotu – Aspose.Note
linktitle: Uložit do obrázku ve stupních šedi ve OneNotu – Aspose.Note
second_title: Aspose.Note Java API
description: Přečtěte si, jak uložit dokument jako obrázek ve stupních šedi ve OneNotu pomocí Aspose.Note pro Java. Programově snadno manipulujte s dokumenty Microsoft OneNote.
type: docs
weight: 17
url: /cs/java/onenote-document-saving/save-to-grayscale-image/
---
## Úvod

V tomto kurzu prozkoumáme, jak uložit dokument jako obrázek ve stupních šedi ve OneNotu pomocí Aspose.Note pro Java. Obrázky ve stupních šedi jsou monochromatické obrázky, kde jsou barevné informace reprezentovány pouze odstíny šedé. Aspose.Note je výkonné Java API, které umožňuje manipulaci s dokumenty Microsoft OneNote programově.

## Předpoklady

Než začneme, ujistěte se, že máte následující:

1. Java Development Kit (JDK) nainstalovaný ve vašem systému.
2.  Aspose.Note pro knihovnu Java. Můžete si jej stáhnout z[tady](https://releases.aspose.com/note/java/).
3. Základní znalost programování v Javě.

## Importujte balíčky

Chcete-li začít, importujte potřebné balíčky:

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## Krok 1: Vložte dokument

 Nejprve načtěte dokument do Aspose.Note. Nahradit`"Your Document Directory"` s cestou k adresáři dokumentů a`"Aspose.one"` s názvem vašeho dokumentu OneNotu.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Krok 2: Nastavte výstupní cestu a možnosti

Definujte výstupní cestu pro obraz ve stupních šedi a určete možnosti uložení. Barevný režim nastavíme na stupně šedi.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## Krok 3: Uložte dokument

Nakonec uložte dokument jako obrázek ve stupních šedi pomocí zadaných možností.

```java
oneFile.save(dataDir, options);
```

## Závěr

Gratulujeme! Úspěšně jste se naučili, jak uložit dokument jako obrázek ve stupních šedi ve OneNotu pomocí Aspose.Note pro Java. To může být neuvěřitelně užitečné pro různé aplikace, kde jsou vyžadovány obrázky ve stupních šedi.

## FAQ

### Q1: Mohu uložit obrázek ve stupních šedi v jiném formátu?

 A1: Ano, můžete. Jednoduše změňte`SaveFormat` parametr v`ImageSaveOptions` konstruktoru do požadovaného formátu.

### Q2: Je Aspose.Note kompatibilní se všemi verzemi dokumentů OneNotu?

Odpověď 2: Aspose.Note podporuje Microsoft OneNote 2010 a vyšší.

### Q3: Vyžaduje Aspose.Note licenci k použití?

Odpověď 3: Ano, k použití Aspose.Note v produkčním prostředí potřebujete platnou licenci. Můžete však získat dočasnou licenci pro testovací účely.

### Q4: Mohu manipulovat s jinými aspekty dokumentu, než jej uložím jako obrázek?

A4: Rozhodně! Aspose.Note poskytuje širokou škálu funkcí pro programovou úpravu dokumentů OneNotu.

### Q5: Kde najdu podporu, pokud narazím na problémy?

A5: Podporu najdete na fóru Aspose.Note[tady](https://forum.aspose.com/c/note/28).