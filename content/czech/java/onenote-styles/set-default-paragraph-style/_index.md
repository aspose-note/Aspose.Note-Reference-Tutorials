---
title: Nastavit výchozí styl odstavce ve OneNotu – Aspose.Note
linktitle: Nastavit výchozí styl odstavce ve OneNotu – Aspose.Note
second_title: Aspose.Note Java API
description: Přečtěte si, jak nastavit výchozí styly odstavců ve OneNotu pomocí Aspose.Note pro Java. Postupujte podle našeho podrobného průvodce pro efektivní formátování textu ve vašich aplikacích Java.
type: docs
weight: 11
url: /cs/java/onenote-styles/set-default-paragraph-style/
---
## Úvod

Aspose.Note for Java nabízí výkonné možnosti pro manipulaci s formátováním textu, včetně nastavení výchozích stylů odstavců. Tento kurz vás provede procesem nastavení výchozích stylů odstavců ve OneNotu pomocí Aspose.Note.

## Předpoklady

Než začnete, ujistěte se, že máte následující:

1. Java Development Kit (JDK): Ujistěte se, že máte v systému nainstalovaný JDK.
2.  Aspose.Note for Java Library: Stáhněte a nainstalujte Aspose.Note for Java z[stránka ke stažení](https://releases.aspose.com/note/java/).
3. Integrované vývojové prostředí (IDE): Pro usnadnění kódování byste měli mít nainstalované IDE, jako je Eclipse nebo IntelliJ IDEA.

## Importujte balíčky

Nejprve naimportujte potřebné balíčky, abyste mohli začít kódovat:

```java
import com.aspose.note.*;

import java.awt.*;
import java.io.FileInputStream;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.List;
```

Nyní si ukázkový kód rozdělíme do několika kroků:

## Krok 1: Inicializujte dokument, stránku a osnovu

```java
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
Outline outline = new Outline();
```

## Krok 2: Vytvořte prvek obrysu

```java
OutlineElement outlineElem = new OutlineElement();
```

## Krok 3: Definujte výchozí styl odstavce

```java
ParagraphStyle defaultStyle = new ParagraphStyle()
										.setFontName("Courier New")
										.setFontSize(20);
```

## Krok 4: Vytvořte formátovaný text s výchozím stylem

```java
RichText text = new RichText()
					.append("DefaultParagraphFontAndSize")
					.append(System.lineSeparator())
					.append("OnlyDefaultParagraphFont", new TextStyle().setFontSize(14))
					.append(System.lineSeparator())
					.append("OnlyDefaultParagraphFontSize", new TextStyle().setFontName("Verdana"));
text.setParagraphStyle(defaultStyle);
```

## Krok 5: Připojte formátovaný text k prvku obrysu

```java
outlineElem.appendChildLast(text);
```

## Krok 6: Připojte prvek obrysu k obrysu

```java
outline.appendChildLast(outlineElem);
```

## Krok 7: Připojte obrys na stránku

```java
page.appendChildLast(outline);
```

## Krok 8: Připojte stránku k dokumentu

```java
document.appendChildLast(page);
```

## Krok 9: Uložte dokument

```java
document.save(Paths.get(dataDir, "SetDefaultParagraphStyle.one").toString());
```

Tento kód nastaví výchozí styl odstavce ve OneNotu pomocí Aspose.Note pro Java.

## Závěr

Nastavení výchozích stylů odstavců ve OneNotu programově lze efektivně dosáhnout pomocí Aspose.Note pro Java. Podle kroků uvedených v tomto kurzu můžete tuto funkci bez problémů integrovat do svých aplikací Java.

## FAQ

### Q1: Mohu dále upravit výchozí styl odstavce?

A1: Ano, můžete upravit různé parametry, jako je název písma, velikost, barva a zarovnání, aby vyhovovaly vašim požadavkům.

### Q2: Podporuje Aspose.Note další operace formátování textu?

A2: Absolutně, Aspose.Note poskytuje rozsáhlou podporu pro manipulaci s formátováním textu, včetně stylů písem, odrážek a odsazení.

### Q3: Je Aspose.Note kompatibilní se všemi verzemi OneNotu?

Odpověď 3: Aspose.Note je navržen pro práci se soubory Microsoft OneNote v různých verzích a zajišťuje širokou kompatibilitu.

### Q4: Mohu integrovat Aspose.Note do mého stávajícího projektu Java?

A4: Ano, Aspose.Note můžete snadno integrovat do svých projektů Java přidáním nezbytných závislostí a importem požadovaných balíčků.

### Q5: Je k dispozici zkušební verze pro Aspose.Note?

 A5: Ano, máte přístup k bezplatné zkušební verzi Aspose.Note z[webová stránka](https://releases.aspose.com/).