---
title: Práce s revizemi stránky ve OneNotu – Aspose.Note
linktitle: Práce s revizemi stránky ve OneNotu – Aspose.Note
second_title: Aspose.Note Java API
description: Přečtěte si, jak spravovat revize stránek v dokumentech OneNotu pomocí Aspose.Note pro Java. Poskytuje průvodce krok za krokem pro efektivní sledování revizí a spolupráci.
weight: 21
url: /cs/java/onenote-page-manipulation/working-with-page-revisions/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Práce s revizemi stránky ve OneNotu – Aspose.Note

## Úvod

OneNote je výkonný nástroj pro organizaci a správu poznámek, ale někdy je potřeba pracovat s revizemi, abyste mohli sledovat změny a efektivně spolupracovat. S Aspose.Note pro Java můžete snadno programově spravovat revize stránek v dokumentech OneNotu. Tento tutoriál vás provede procesem krok za krokem.

## Předpoklady

Než začnete, ujistěte se, že máte následující:

### Vývojové prostředí Java

Ujistěte se, že máte v systému nainstalovanou sadu Java Development Kit (JDK).

### Aspose.Note pro Java Library

Stáhněte a nainstalujte knihovnu Aspose.Note pro Java z[tady](https://releases.aspose.com/note/java/).

### Dokument OneNotu

Připravte si vzorový dokument OneNotu pro testovací účely.

## Importujte balíčky

Ve svém projektu Java importujte potřebné balíčky pro práci s Aspose.Note for Java.

```java
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.RevisionSummary;
import java.io.IOException;
import java.util.Calendar;
```

Rozdělme si poskytnutý příklad do několika kroků pro jasné pochopení.

## Krok 1: Načtěte dokument OneNotu

Nejprve načtěte dokument OneNotu a získejte první podřízenou stránku.

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
Page page = document.getFirstChild();
```

## Krok 2: Přečtěte si souhrn revizí stránky

Přečtěte si souhrn revize obsahu stránky.

```java
RevisionSummary pageRevisionInfo = page.getPageContentRevisionSummary();
System.out.println(String.format("Author:\t%s\nModified:\t%s",
        pageRevisionInfo.getAuthorMostRecent(),
        pageRevisionInfo.getLastModifiedTime().toString()));
```

## Krok 3: Aktualizujte souhrn revizí stránky

Aktualizujte souhrn revize stránky novým autorem a datem změny.

```java
pageRevisionInfo.setAuthorMostRecent("New Author");
Calendar modifiedDate = Calendar.getInstance();
pageRevisionInfo.setLastModifiedTime(modifiedDate.getTime());
document.save(dataDir + "WorkingWithPageRevisions_out.one");
```

## Závěr

Programovou správu revizí stránek v dokumentech OneNotu lze zjednodušit pomocí Aspose.Note pro Java. Podle kroků uvedených v tomto kurzu můžete efektivně pracovat s revizemi stránek, abyste mohli sledovat změny a bezproblémově spolupracovat.

## FAQ

### Q1: Mohu použít Aspose.Note pro Java s jinými Java knihovnami?

Odpověď: Ano, Aspose.Note for Java lze integrovat s jinými knihovnami Java pro vylepšení funkčnosti.

### Q2: Podporuje Aspose.Note pro Java všechny verze dokumentů OneNotu?

Odpověď: Aspose.Note pro Java podporuje různé verze dokumentů OneNote, včetně starších verzí.

### Q3: Je Aspose.Note for Java vhodný pro aplikace na podnikové úrovni?

Odpověď: Rozhodně, Aspose.Note pro Java je navržen tak, aby vyhovoval potřebám podnikových aplikací s robustními funkcemi a škálovatelností.

### Q4: Mohu přizpůsobit revize stránek pomocí Aspose.Note pro Java?

Odpověď: Ano, pomocí Aspose.Note pro Java si můžete upravit revize stránek podle svých požadavků.

### Q5: Kde mohu získat podporu pro Aspose.Note pro Java?

 Odpověď: Podporu pro Aspose.Note pro Javu můžete získat z[Aspose.Note fórum](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
