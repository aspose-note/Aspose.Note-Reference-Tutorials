---
title: Push aktuální verzi stránky ve OneNotu - Aspose.Note
linktitle: Push aktuální verzi stránky ve OneNotu - Aspose.Note
second_title: Aspose.Note Java API
description: Udržujte obsah OneNotu aktuální! Naučte se aktualizovat historii stránek a spravovat verze, včetně podrobného průvodce a kódu. #OneNote #Java #Aspose
weight: 18
url: /cs/java/onenote-page-manipulation/push-current-page-version/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Push aktuální verzi stránky ve OneNotu - Aspose.Note

## Úvod

V tomto tutoriálu prozkoumáme, jak využít Aspose.Note pro Javu k vložení aktuální verze stránky do OneNotu. Aspose.Note je výkonná Java knihovna, která umožňuje vývojářům pracovat s dokumenty Microsoft OneNote programově a umožňuje různé operace, jako je vytváření, manipulace a převod souborů OneNote.

## Předpoklady

Než začneme, ujistěte se, že máte následující předpoklady:
1. Základní znalost programovacího jazyka Java.
2. Nainstalovaný Java Development Kit (JDK) ve vašem systému.
3.  Aspose.Note pro knihovnu Java. Můžete si jej stáhnout z[tady](https://releases.aspose.com/note/java/).
4. Ukázkový dokument OneNotu pro práci.

## Importujte balíčky

Nejprve musíte do svého projektu Java importovat potřebné balíčky, abyste mohli používat funkce Aspose.Note.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## Krok 1: Načtěte dokument OneNotu

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
```

 Tady,`dataDir` by měl ukazovat na adresář, kde se nachází váš dokument OneNotu. Nahradit`"Sample1.one"` s názvem vašeho souboru OneNotu.

## Krok 2: Získejte aktuální stránku a její historii

```java
Page page = document.getFirstChild();
PageHistory pageHistory = document.getPageHistory(page);
```

 První stránku dokumentu načteme pomocí`getFirstChild()` a poté získat jeho historii pomocí`getPageHistory()`.

## Krok 3: Stiskněte aktuální verzi stránky

```java
pageHistory.addItem(page.deepClone());
```

Zde přidáme aktuální verzi stránky do její historie tak, že ji naklonujeme a přidáme jako novou položku.

## Krok 4: Uložte dokument

```java
document.save(dataDir + "PushCurrentPageVersion_out.one");
```

Nakonec upravený dokument uložíme s aktualizovanou historií stránek.

## Závěr

V tomto kurzu jsme se naučili, jak vložit aktuální verzi stránky do OneNotu pomocí Aspose.Note pro Javu. Pomocí těchto kroků můžete efektivně spravovat správu verzí dokumentů OneNotu programově.

## FAQ

### Q1: Mohu použít Aspose.Note pro Java k práci se zašifrovanými soubory OneNotu?

Odpověď 1: Ano, Aspose.Note pro Java podporuje práci se šifrovanými i nešifrovanými soubory OneNote.

### Q2: Je Aspose.Note for Java kompatibilní s nejnovější verzí OneNotu?

Odpověď 2: Aspose.Note for Java se snaží zachovat kompatibilitu s nejnovějšími verzemi dokumentů OneNotu.

### Q3: Mohu manipulovat s textem a obrázky v dokumentech OneNotu pomocí Aspose.Note pro Java?

Odpověď 3: Absolutně, Aspose.Note pro Java poskytuje rozsáhlé funkce pro manipulaci s textem, obrázky a dalšími prvky v souborech OneNotu.

### Q4: Podporuje Aspose.Note pro Java převod souborů OneNotu do jiných formátů?

Odpověď 4: Ano, Aspose.Note pro Java podporuje převod souborů OneNote do různých formátů, jako jsou PDF, HTML a obrazové formáty.

### Q5: Kde mohu získat podporu pro Aspose.Note pro Java, pokud narazím na nějaké problémy?

 A5: Můžete navštívit[Aspose.Note fórum](https://forum.aspose.com/c/note/28) požádat o pomoc komunitu nebo přímo kontaktovat podporu Aspose.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
