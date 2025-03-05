---
title: Uložit do obrázku BMP pomocí možností uložení obrázku ve OneNotu
linktitle: Uložit do obrázku BMP pomocí možností uložení obrázku ve OneNotu
second_title: Aspose.Note Java API
description: Naučte se ukládat dokumenty OneNotu do obrázků BMP programově pomocí Aspose.Note pro Java. Podrobný průvodce s příklady kódu.
type: docs
weight: 16
url: /cs/java/onenote-document-saving/save-to-bmp-image-using-image-save-options/
---
## Úvod

Aspose.Note for Java je výkonná knihovna, která umožňuje vývojářům Java pracovat se soubory Microsoft OneNote programově. S Aspose.Note pro Java můžete bezproblémově vytvářet, manipulovat a převádět dokumenty OneNotu. V tomto tutoriálu se ponoříme do toho, jak uložit dokument OneNote do obrázku BMP pomocí možností uložení obrázku, které poskytuje Aspose.Note pro Java.

## Předpoklady

Než budete pokračovat v tomto návodu, ujistěte se, že máte následující:

1. Základní znalost programovacího jazyka Java.
2. Nainstalovaný JDK (Java Development Kit) ve vašem systému.
3. Integrované vývojové prostředí (IDE), jako je Eclipse nebo IntelliJ IDEA.
4.  Aspose.Note pro knihovnu Java. Můžete si jej stáhnout z[tady](https://releases.aspose.com/note/java/).

## Importujte balíčky

Nejprve musíte importovat potřebné balíčky z Aspose.Note pro Java, abyste mohli využívat jeho funkce. Přidejte do svého souboru Java následující příkaz pro import:

```java
import com.aspose.note.*;
import java.io.IOException;
```

Nyní si uvedený příklad rozdělíme do několika kroků:

## Krok 1: Vložte dokument

```java
// Cesta k adresáři dokumentů.
String dataDir = "Your Document Directory";

// Vložte dokument do Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

 tomto kroku určíme cestu k adresáři, kde se nachází náš dokument OneNotu. Poté načteme dokument pomocí`Document` třídy poskytované Aspose.Note pro Javu.

## Krok 2: Uložte do obrázku BMP

```java
dataDir = dataDir + "SaveToBmpImageUsingImageSaveOptions_out.bmp";

// Uložte dokument.
oneFile.save(dataDir, new ImageSaveOptions(SaveFormat.Bmp));
```

 V tomto kroku určíme výstupní cestu pro obrázek BMP, který bude vygenerován z dokumentu OneNote. Používáme`save` metoda`Document` třídy k uložení dokumentu jako obrázku BMP s uvedením výstupní cesty a instance`ImageSaveOptions` s požadovaným`SaveFormat` (v tomto případě,`SaveFormat.Bmp`).

## Závěr

V tomto tutoriálu jsme se naučili, jak uložit dokument OneNote do obrázku BMP pomocí Aspose.Note pro Java. Pokud budete postupovat podle podrobného průvodce, můžete tuto funkci bez problémů integrovat do svých aplikací Java, což vám umožní snadno manipulovat s dokumenty OneNotu.

## FAQ

### Q1: Mohu uložit dokumenty OneNotu do jiných obrazových formátů kromě BMP?

Odpověď 1: Ano, pomocí Aspose.Note pro Java můžete ukládat dokumenty OneNotu do různých obrazových formátů, jako jsou JPEG, PNG, GIF a TIFF.

### Q2: Podporuje Aspose.Note for Java převod mezi různými formáty dokumentů?

Odpověď 2: Ano, Aspose.Note pro Java podporuje převod mezi dokumenty OneNote a dalšími formáty, jako jsou PDF, DOCX, HTML a další.

### Q3: Je Aspose.Note for Java kompatibilní s nejnovějšími verzemi OneNotu?

Odpověď 3: Ano, Aspose.Note pro Java je pravidelně aktualizován, aby byla zajištěna kompatibilita s nejnovějšími verzemi OneNotu.

### Q4: Mohu programově manipulovat s obsahem dokumentů OneNotu pomocí Aspose.Note for Java?

Odpověď 4: Ano, můžete manipulovat s obsahem, strukturou a formátováním dokumentů OneNotu programově pomocí Aspose.Note for Java.

### Q5: Poskytuje Aspose.Note pro Java technickou podporu?

 A5: Ano, Aspose poskytuje technickou podporu pro své produkty. Můžete navštívit[Aspose.Note fórum](https://forum.aspose.com/c/note/28) pro pomoc.