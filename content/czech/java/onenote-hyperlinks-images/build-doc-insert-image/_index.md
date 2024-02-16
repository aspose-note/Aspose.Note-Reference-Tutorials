---
title: Vytvořte dokument a vložte obrázek do OneNotu pomocí Java
linktitle: Vytvořte dokument a vložte obrázek do OneNotu pomocí Java
second_title: Aspose.Note Java API
description: Naučte se vytvářet dokumenty OneNotu a vkládat obrázky pomocí Aspose.Note pro Java. Výukový program krok za krokem pro bezproblémovou integraci.
type: docs
weight: 12
url: /cs/java/onenote-hyperlinks-images/build-doc-insert-image/
---
## Úvod

V tomto tutoriálu prozkoumáme, jak používat Aspose.Note pro Java k vytváření dokumentů OneNotu a vkládání obrázků do nich. Aspose.Note je výkonné Java API, které umožňuje vývojářům pracovat se soubory Microsoft OneNote programově. Každý krok podrobně rozebereme, abychom vás tímto procesem provedli.

## Předpoklady

Než začneme, ujistěte se, že máte následující předpoklady:

1. Java Development Kit (JDK): Ujistěte se, že máte v systému nainstalovaný JDK.
2.  Aspose.Note pro knihovnu Java: Stáhněte a nainstalujte knihovnu Aspose.Note pro Java z[webová stránka](https://releases.aspose.com/note/java/).
3. IDE (Integrated Development Environment): Pro kódování použijte jakékoli IDE podporované Javou, jako je IntelliJ IDEA nebo Eclipse.

## Importujte balíčky

Začněte importováním potřebných balíčků do kódu Java:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## Krok 1: Nastavte dokument

Nejprve vytvořte nový dokument OneNotu a inicializujte potřebné objekty:

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

## Krok 2: Inicializujte Outline

Nastavte obrys pro dokument a zadejte vlastnosti odsazení:

```java
Outline outline = new Outline();
outline.setVerticalOffset(0);
outline.setHorizontalOffset(0);
```

## Krok 3: Přidejte obrázek

Načtěte obrázek a určete jeho zarovnání:

```java
Image image = new Image(null, dataDir + "Input.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## Krok 4: Přidejte obrázek do prvku obrysu

Připojte obrázek k prvku obrysu:

```java
OutlineElement outlineElem = new OutlineElement();
outlineElem.appendChildLast(image);
```

## Krok 5: Přidejte obrys a uzly stránky

Přidejte osnovu a uzly stránky do dokumentu:

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## Krok 6: Uložte dokument

Nakonec uložte dokument OneNotu:

```java
try {
    doc.save(dataDir + "NewOneNotedocument_out", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Závěr

Gratulujeme! Úspěšně jste se naučili, jak vytvářet dokumenty OneNotu a vkládat do nich obrázky pomocí Aspose.Note for Java. Pomocí těchto kroků můžete efektivně spravovat a manipulovat se soubory OneNotu v aplikacích Java.

## FAQ

### Q1: Kde najdu dokumentaci k Aspose.Note pro Java?

 A1: Máte přístup k dokumentaci[tady](https://reference.aspose.com/note/java/).

### Q2: Jak stáhnu Aspose.Note pro Java?

 A2: Aspose.Note pro Java si můžete stáhnout z[stránka ke stažení](https://releases.aspose.com/note/java/).

### Q3: Je k dispozici bezplatná zkušební verze pro Aspose.Note pro Java?

 A3: Ano, můžete získat bezplatnou zkušební verzi z[webová stránka](https://releases.aspose.com/).

### Q4: Kde mohu získat podporu pro Aspose.Note pro Java?

 A4: Pro podporu navštivte[Aspose.Note fórum](https://forum.aspose.com/c/note/28).

### Q5: Mohu získat dočasnou licenci pro Aspose.Note pro Java?

 A5: Ano, můžete požádat o dočasnou licenci[tady](https://purchase.aspose.com/temporary-license/).
