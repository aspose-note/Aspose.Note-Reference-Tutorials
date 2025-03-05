---
title: Uložit do obrázku TIFF pomocí možností uložení obrázku ve OneNotu
linktitle: Uložit do obrázku TIFF pomocí možností uložení obrázku ve OneNotu
second_title: Aspose.Note Java API
description: Převeďte dokumenty OneNote na TIFF a ovládejte velikost a kvalitu souboru! Vyberte kompresi Jpeg, PackBits nebo Fax v Javě. Získejte příklady kódu a zjistěte, jak na to! #OneNote #Java #Aspose
type: docs
weight: 21
url: /cs/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
---
## Úvod

V tomto tutoriálu se naučíte, jak uložit dokument do obrazového formátu TIFF pomocí různých metod komprese v Aspose.Note pro Javu. Pokryjeme předpoklady, import balíčků a poskytneme podrobného průvodce pro každou metodu komprese.

## Předpoklady

Než začnete, ujistěte se, že máte následující:

- Java Development Kit (JDK) nainstalovaný ve vašem systému.
- Aspose.Note pro knihovnu Java staženou a nakonfigurovanou.
- Základní znalost programovacího jazyka Java.

## Importujte balíčky

Nejprve je třeba importovat potřebné balíčky do souboru Java:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Krok 1: Uložte do TIFF pomocí komprese JPEG

```java
public static void SaveToTiffUsingJpegCompression() throws IOException {
    // Cesta k adresáři dokumentů.
    String dataDir = "Your Document Directory";

    // Vložte dokument do Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.Jpeg);
    options.setQuality(93);

    oneFile.save(Paths.get(dataDir,"SaveToTiffUsingJpegCompression.tiff").toString(), options);
}
```

-  Vložte dokument pomocí`Document` třída.
-  Vytvořte instanci`ImageSaveOptions` a zadejte typ komprese TIFF jako JPEG.
- Nastavte požadovanou kvalitu (volitelné).
- Uložte dokument do formátu TIFF pomocí zadaných možností.

## Krok 2: Uložte do TIFF pomocí komprese PackBits

```java
public static void SaveToTiffUsingPackBitsCompression() throws IOException {
    // Cesta k adresáři dokumentů.
    String dataDir = "Your Document Directory";

    // Vložte dokument do Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.PackBits);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingPackBitsCompression.tiff").toString(), options);
}
```

-  Vložte dokument pomocí`Document` třída.
-  Vytvořte instanci`ImageSaveOptions` a zadejte typ komprese TIFF jako PackBits.
- Uložte dokument do formátu TIFF pomocí zadaných možností.

## Krok 3: Uložte do TIFF pomocí CCITT Group 3 Fax Compression

```java
public static void SaveToTiffUsingCcitt3Compression() throws IOException {
    // Cesta k adresáři dokumentů.
    String dataDir = "Your Document Directory";

    // Vložte dokument do Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setColorMode(ColorMode.BlackAndWhite);
    options.setTiffCompression(TiffCompression.Ccitt3);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingCcitt3Compression.tiff").toString(), options);
}
```

-  Vložte dokument pomocí`Document` třída.
-  Vytvořte instanci`ImageSaveOptions` a zadejte typ komprese TIFF jako CCITT Group 3 Fax.
- Nastavte barevný režim na černobílý.
- Uložte dokument do formátu TIFF pomocí zadaných možností.

## Závěr

V tomto tutoriálu jste se naučili, jak uložit dokument do formátu obrázku TIFF pomocí různých metod komprese v Aspose.Note pro Java. Budete-li se řídit podrobným průvodcem, můžete efektivně využívat možnosti Aspose.Note ke splnění vašich požadavků.

## FAQ

### Q1: Mohu použít Aspose.Note pro Java k převodu jiných formátů dokumentů na TIFF?

Odpověď 1: Ano, Aspose.Note pro Java podporuje převod z různých formátů dokumentů do TIFF, včetně dokumentů OneNote.

### Q2: Jaký význam má určení typu komprese při ukládání do TIFF?

A2: Určení typu komprese vám umožní ovládat kvalitu obrazu a velikost souboru. Různé kompresní metody nabízejí kompromisy mezi kvalitou a kompresním poměrem.

### Q3: Je Aspose.Note pro Java vhodný pro dávkové zpracování dokumentů?

Odpověď 3: Ano, Aspose.Note for Java poskytuje rozhraní API pro dávkové zpracování, což vám umožňuje efektivně automatizovat úlohy převodu dokumentů.

### Q4: Mohu dále upravit nastavení komprese?

A4: Ano, můžete upravit parametry, jako je kvalita, rozlišení a metoda komprese, abyste přizpůsobili výstup podle svých požadavků.

### Q5: Nabízí Aspose.Note for Java technickou podporu?

A5: Ano, Aspose poskytuje komplexní technickou podporu prostřednictvím fór a systémů založených na lístcích.