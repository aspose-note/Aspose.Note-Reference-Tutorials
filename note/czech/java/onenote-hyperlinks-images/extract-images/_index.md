---
title: Extrahujte obrázky z dokumentu OneNote pomocí Java
linktitle: Extrahujte obrázky z dokumentu OneNote pomocí Java
second_title: Aspose.Note Java API
description: Naučte se, jak extrahovat obrázky z dokumentů OneNotu pomocí Java s knihovnou Aspose.Note. Postupujte podle našeho podrobného průvodce pro bezproblémovou extrakci obrázků.
weight: 14
url: /cs/java/onenote-hyperlinks-images/extract-images/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Extrahujte obrázky z dokumentu OneNote pomocí Java

## Úvod

V tomto tutoriálu vás provedeme procesem extrahování obrázků z dokumentu OneNote pomocí Javy s pomocí knihovny Aspose.Note.

## Předpoklady

Než začnete, ujistěte se, že máte následující:

1.  Java Development Kit (JDK): Ujistěte se, že máte v systému nainstalovanou Javu. Můžete si jej stáhnout a nainstalovat z[webová stránka](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).

2.  Knihovna Aspose.Note: Stáhněte si a zahrňte knihovnu Aspose.Note do svého projektu Java. Můžete to získat z[odkaz ke stažení](https://releases.aspose.com/note/java/).

## Importujte balíčky

Chcete-li začít, importujte potřebné balíčky:

```java
import java.io.IOException;
import java.nio.file.Files;
import java.nio.file.Paths;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.Image;
```

## Krok 1: Vložte dokument

Nejprve načtěte dokument OneNotu pomocí Aspose.Note:

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```

## Krok 2: Získejte všechny obrázky

Dále načtěte všechny obrázky z dokumentu:

```java
List<Image> list = doc.getChildNodes(Image.class);
System.out.printf("Total Images: %s\n\n", list.size());
```

## Krok 3: Extrahujte obrázky

Procházejte seznam obrázků a uložte každý obrázek do souboru:

```java
for (int i = 0; i < list.size(); i++) {
    Image image = list.get(i);
    String outputFile = "ExtractImages_out" + i + "_" + image.getFileName();
    byte[] buffer = image.getBytes();
    Files.write(Paths.get(dataDir + outputFile), buffer);
    System.out.printf("File saved: %s\n", dataDir);
}
```

## Závěr

Extrahování obrázků z dokumentu OneNote pomocí Javy lze hladce dosáhnout pomocí knihovny Aspose.Note. Podle kroků uvedených v tomto kurzu můžete bez námahy získat obrázky z dokumentů pro další zpracování nebo analýzu.

## FAQ

### Q1: Mohu extrahovat obrázky z dokumentů OneNotu chráněných heslem?

Odpověď 1: Ano, Aspose.Note podporuje také extrahování obrázků z dokumentů chráněných heslem.

### Q2: Je Aspose.Note kompatibilní s různými verzemi Java?

Odpověď 2: Aspose.Note je kompatibilní s různými verzemi Java, což zajišťuje flexibilitu pro vývojáře.

### Q3: Mohu extrahovat obrázky z více dokumentů OneNotu v jednom spuštění?

A3: Rozhodně můžete procházet více dokumenty a extrahovat obrázky z každého z nich pomocí Aspose.Note.

### Q4: Existují nějaká omezení velikosti pro dokumenty OneNotu?

A4: Aspose.Note zpracuje dokumenty různých velikostí efektivně a nezajistí žádná omezení velikosti dokumentu pro extrakci obrázků.

### Q5: Podporuje Aspose.Note extrahování jiných typů obsahu kromě obrázků?

A5: Ano, kromě obrázků umožňuje Aspose.Note extrahování textu, příloh a dalších typů obsahu z dokumentů OneNotu.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
