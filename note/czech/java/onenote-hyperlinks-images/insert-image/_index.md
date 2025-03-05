---
title: Vložte obrázek do dokumentu OneNotu s Java
linktitle: Vložte obrázek do dokumentu OneNotu s Java
second_title: Aspose.Note Java API
description: Naučte se vkládat obrázky do dokumentů OneNotu pomocí Java s knihovnou Aspose.Note for Java. Postupujte podle našeho podrobného průvodce pro bezproblémovou integraci.
type: docs
weight: 16
url: /cs/java/onenote-hyperlinks-images/insert-image/
---
## Úvod

V tomto tutoriálu prozkoumáme, jak vložit obrázek do dokumentu OneNote pomocí Javy s pomocí Aspose.Note pro Javu. Aspose.Note for Java je výkonná knihovna, která umožňuje vývojářům pracovat se soubory Microsoft OneNote programově a umožňuje různé operace, jako je vytváření, čtení a manipulace s dokumenty OneNotu.

## Předpoklady

Než začneme, ujistěte se, že máte nastaveny následující předpoklady:

### 1. Java Development Kit (JDK)
Ujistěte se, že máte v systému nainstalovanou sadu Java Development Kit (JDK). JDK si můžete stáhnout a nainstalovat z webu Oracle.

### 2. Aspose.Note for Java Library
 Stáhněte a nastavte knihovnu Aspose.Note for Java podle pokynů v[dokumentace](https://reference.aspose.com/note/java/).

## Importujte balíčky

Začněte importováním potřebných balíčků do vašeho projektu Java. Tyto balíčky zahrnují knihovnu Aspose.Note a další požadované závislosti.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

Pojďme si proces vložení obrázku do dokumentu OneNotu rozdělit do několika kroků:

## Krok 1: Načtěte dokument OneNotu

Nejprve načtěte dokument OneNotu, do kterého chcete obrázek vložit.

```java
LoadOptions options = new LoadOptions();
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", options);
```

## Krok 2: Získejte stránku

Načtěte stránku v dokumentu, kam chcete vložit obrázek.

```java
Page page = oneFile.getFirstChild();
```

## Krok 3: Načtěte obrázek

Načtěte obrázek, který chcete vložit do dokumentu OneNotu.

```java
Image image = new Image(oneFile, dataDir + "Input.jpg");
```

## Krok 4: Přizpůsobte atributy obrázku (volitelné)

Volitelně můžete upravit velikost, umístění a zarovnání obrázku podle svých požadavků.

```java
image.setWidth(100);
image.setHeight(100);
image.setVerticalOffset(400);
image.setHorizontalOffset(100);
image.setAlignment(HorizontalAlignment.Right);
```

## Krok 5: Přidejte obrázek na stránku

Přidejte obrázek na stránku v dokumentu OneNotu.

```java
page.appendChildLast(image);
```

## Krok 6: Uložte dokument

Uložte upravený dokument včetně vloženého obrázku.

```java
try {
    oneFile.save(dataDir + "InsertanImage_out.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Závěr

V tomto tutoriálu jsme se naučili, jak vložit obrázek do dokumentu OneNote pomocí Javy s pomocí knihovny Aspose.Note for Java. Podle podrobného průvodce můžete bez námahy začlenit obrázky do dokumentů OneNotu programově.

## FAQ

### Q1: Mohu pomocí této metody vložit více obrázků do jednoho dokumentu OneNotu?

Odpověď 1: Ano, do jednoho dokumentu OneNotu můžete vložit více obrázků opakováním postupu popsaného v tomto kurzu pro každý obrázek.

### Q2: Je Aspose.Note for Java kompatibilní se všemi verzemi OneNotu?

Odpověď 2: Aspose.Note for Java podporuje práci se soubory OneNote vytvořenými v aplikaci Microsoft OneNote 2010 a novějších verzích.

### Otázka 3: Mohu do dokumentu OneNotu vložit obrázky různých formátů, jako je PNG nebo GIF?

Odpověď 3: Ano, Aspose.Note pro Java podporuje vkládání obrázků v různých formátech, včetně PNG, JPEG, GIF a dalších.

### Q4: Je k dispozici zkušební verze Aspose.Note pro Java pro účely testování?

Odpověď 4: Ano, z webové stránky si můžete stáhnout bezplatnou zkušební verzi Aspose.Note pro Java pro účely hodnocení.

### Q5: Jak mohu získat technickou podporu pro Aspose.Note pro Java?

 Odpověď 5: Technickou podporu pro Aspose.Note pro Java můžete získat na adrese[Fórum](https://forum.aspose.com/c/note/28) věnované produktům Aspose.Note.