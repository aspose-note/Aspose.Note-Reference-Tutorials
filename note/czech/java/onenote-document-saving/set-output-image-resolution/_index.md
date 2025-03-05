---
title: Nastavte výstupní rozlišení obrazu ve OneNotu - Aspose.Note
linktitle: Nastavte výstupní rozlišení obrazu ve OneNotu - Aspose.Note
second_title: Aspose.Note Java API
description: Přečtěte si, jak upravit rozlišení obrázků v dokumentech OneNotu pomocí Aspose.Note pro Java. Pro snadnou implementaci postupujte podle našeho podrobného průvodce
type: docs
weight: 23
url: /cs/java/onenote-document-saving/set-output-image-resolution/
---
## Úvod

Chcete manipulovat s rozlišením obrázků v dokumentech OneNotu pomocí Javy? Aspose.Note for Java nabízí robustní řešení pro takové úkoly. V tomto tutoriálu si projdeme kroky k nastavení výstupního rozlišení obrazu pomocí Aspose.Note.

## Předpoklady

Než začneme, ujistěte se, že máte následující předpoklady:

1. Java Development Kit (JDK): Nainstalujte JDK do svého systému.
2. Aspose.Note for Java: Stáhněte a nainstalujte Aspose.Note for Java z[webová stránka](https://releases.aspose.com/note/java/).
3. Integrované vývojové prostředí (IDE): Vyberte si preferované IDE, jako je Eclipse nebo IntelliJ IDEA.

## Importujte balíčky

Ve svém projektu Java importujte potřebné balíčky Aspose.Note:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Krok 1: Načtěte dokument OneNotu

Začněte načtením dokumentu OneNotu do aplikace Java:

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```

 Nahradit`"Your Document Directory"` se skutečným adresářem, kde se nachází váš dokument OneNotu.

## Krok 2: Nastavte možnosti uložení obrázku

Definujte možnosti uložení obrázku a určete požadované rozlišení:

```java
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Jpeg);
imageSaveOptions.setResolution(120);
```

 Zde nastavíme rozlišení na`120 dpi`. Tuto hodnotu můžete upravit podle svých požadavků.

## Krok 3: Uložte dokument s upraveným rozlišením

Uložte dokument s aktualizovaným rozlišením obrázku:

```java
doc.save(dataDir + "SetOutputImageResolution_out.jpeg", imageSaveOptions);
```

Tím se upravený dokument uloží se zadaným rozlišením.

## Závěr

V tomto tutoriálu jsme prozkoumali, jak nastavit výstupní rozlišení obrazu v dokumentech OneNotu pomocí Aspose.Note pro Java. Pomocí těchto jednoduchých kroků můžete efektivně manipulovat s rozlišením obrázků tak, aby vyhovovaly požadavkům vaší aplikace.


## FAQ

### Q1: Mohu upravit rozlišení obrázku na hodnotu vyšší než 120 dpi?

A1: Ano, rozlišení můžete nastavit na libovolnou požadovanou hodnotu podle vašich potřeb.

### Q2: Podporuje Aspose.Note jiné obrazové formáty kromě JPEG?

Odpověď 2: Ano, Aspose.Note podporuje různé formáty obrázků, jako je PNG, BMP, GIF atd.

### Q3: Je Aspose.Note kompatibilní se všemi verzemi Java?

A3: Aspose.Note je kompatibilní s Java 1.6 nebo novějšími verzemi.

### Q4: Mohu manipulovat s jinými aspekty obrázků v dokumentech OneNotu pomocí Aspose.Note?

Odpověď 4: Ano, Aspose.Note poskytuje komplexní funkce pro manipulaci s obrázky, včetně změny velikosti, oříznutí a otočení.

### Q5: Kde mohu získat podporu pro dotazy související s Aspose.Note?

 A5: Můžete požádat o pomoc z fóra komunity Aspose.Note[tady](https://forum.aspose.com/c/note/28).