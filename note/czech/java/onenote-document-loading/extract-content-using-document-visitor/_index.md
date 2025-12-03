---
date: 2025-12-03
description: Naučte se, jak převést OneNote na text pomocí Aspose.Note pro Javu. Podrobný
  návod krok za krokem, který zahrnuje extrakci textu, extrakci obrázků a jak číst
  soubory OneNote.
language: cs
linktitle: Convert OneNote to Text with Document Visitor – Java
second_title: Aspose.Note Java API
title: Převod OneNote na text pomocí Document Visitor – Java
url: /java/onenote-document-loading/extract-content-using-document-visitor/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převod OneNote na text pomocí Document Visitor – Java

## Úvod

V tomto tutoriálu se naučíte **jak převést OneNote na text** pomocí Document Visitor z Aspose.Note for Java. Ať už potřebujete programově číst soubory OneNote, extrahovat čistý textový obsah nebo získat vložené obrázky, Document Visitor vám poskytuje detailní kontrolu nad každým uzlem v souboru .one.

## Rychlé odpovědi
- **Co znamená „převod OneNote na text“?** Znamená to extrahování čisté textové reprezentace (a volitelně obrázků) ze souboru .one.  
- **Která knihovna s tím pomáhá?** Aspose.Note for Java poskytuje API `DocumentVisitor`.  
- **Potřebuji licenci?** Bezplatná zkušební verze funguje pro hodnocení; pro produkční použití je vyžadována placená licence.  
- **Mohu také extrahovat obrázky?** Ano – implementujte metodu `VisitImageStart` pro získání obrázků.  
- **Jaké jsou předpoklady?** Java JDK 8+, Aspose.Note for Java JAR a soubor .one k zpracování.

## Co je „převod OneNote na text“?
Převod OneNote na text znamená programově číst soubor OneNote (.one) a získávat jeho textový obsah, nadpisy a další prvky bez původního uživatelského rozhraní OneNote. To je užitečné pro indexování vyhledávání, tvorbu reportů nebo migraci obsahu na jiné platformy.

## Proč použít Document Visitor k **čtení OneNote** souborům?
Document Visitor používá návrhový vzor Visitor, který vám umožňuje projít každý prvek (stránky, osnovy, obrázky, bloky formátovaného textu atd.) v dokumentu OneNote. Ve srovnání s načítáním celého dokumentu do paměti a ručním parsováním je přístup visitor:

* **Paměťově úsporný** – zpracovává uzly po jednom.  
* **Rozšiřitelný** – můžete přidat vlastní logiku pro jakýkoli typ uzlu (např. extrahovat obrázky).  
* **Přesný** – zachovává původní hierarchii, takže nevynecháte skrytý obsah.

## Předpoklady

Předtím, než začnete, ujistěte se, že máte:

1. **Java Development Kit (JDK) 8 nebo novější** nainstalovaný.  
2. **Aspose.Note for Java** knihovnu staženou z oficiální stránky – [download here](https://releases.aspose.com/note/java/).  
3. **OneNote dokument** (`.one` soubor), který chcete převést na text.

## Krok 1: Import balíčků

Nejprve importujte třídy, které budete potřebovat pro práci s Aspose.Note for Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.DocumentVisitor;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.OutlineGroup;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.Title;
```

## Krok 2: Nastavení třídy Document Visitor

Vytvořte třídu, která rozšiřuje `DocumentVisitor`. Tento vlastní visitor bude sbírat text, počítat uzly a (pokud chcete) ukládat obrázky.

```java
public class ExtractOneNoteContentUsingDocumentvisitor extends DocumentVisitor {
    
    final private StringBuilder mBuilder;
    final private boolean mIsSkipText;
    private int nodecount;

    public ExtractOneNoteContentUsingDocumentvisitor() {
        nodecount = 0;
        mIsSkipText = false;
        mBuilder = new StringBuilder();
    }
    
    // Other methods will be implemented here
}
```

## Krok 3: Implementace metod Visitor

Zde implementujeme zpětná volání pro typy uzlů, o které nám jde. Metody zvyšují čítač uzlů a pro `RichText` přidávají skutečný text do našeho `StringBuilder`. Můžete také přidat logiku pro **extrahování obrázků z OneNote** zpracováním `VisitImageStart`.

```java
// Visitor methods for different types of nodes

public /* override */ void VisitRichTextStart(RichText run) {
    ++nodecount;
    AppendText(run.getText());
}

public /* override */ void VisitDocumentStart(Document document) {
    ++nodecount;
}

public /* override */ void VisitPageStart(Page page) {
    ++nodecount;
}

public /* override */ void VisitTitleStart(Title title) {
    ++nodecount;
}

public /* override */ void VisitImageStart(Image image) {
    ++nodecount;
    // Pro tip: you can save the image stream here if you need to extract images.
}

public /* override */ void VisitOutlineGroupStart(OutlineGroup outlineGroup) {
    ++nodecount;
}

public void VisitOutlineStart(Outline outline) {
    ++nodecount;
}

public void VisitOutlineElementStart(OutlineElement outlineElement) {
    ++nodecount;
}
```

## Krok 4: Hlavní metoda – spuštění Visitoru

Metoda `main` načte soubor OneNote, vytvoří instanci našeho vlastního visitoru a spustí procházení. Po návštěvě vytiskne extrahovaný text a celkový počet uzlů.

```java
public static void main(String[] args) throws IOException {
    // Open the document we want to convert.
    String dataDir = "Your Document Directory";
    Document doc = new Document(dataDir + "Sample1.one", new LoadOptions());
    
    // Create an object that inherits from the DocumentVisitor class.
    ExtractOneNoteContentUsingDocumentvisitor myConverter = new ExtractOneNoteContentUsingDocumentvisitor();
    
    // Accept the visitor to start the visiting process.
    doc.accept(myConverter);
    
    // Retrieve the result of the operation.
    System.out.println(myConverter.GetText());
    System.out.println(myConverter.NodeCount());
}
```

## Běžné případy použití – **extrahování obrázků z OneNote**

* **Indexování vyhledávání** – Převést sešity OneNote na čistý text pro full‑textové vyhledávače.  
* **Migrace obsahu** – Přesunout poznámky do CMS nebo portálu dokumentace.  
* **Analýza dat** – Získat text a obrázky pro zpracování přirozeného jazyka nebo analýzu obrázků.  

## Běžné problémy a řešení

| Problém | Řešení |
|-------|----------|
| **NullPointerException při čtení souboru .one** | Ujistěte se, že cesta k souboru (`dataDir`) končí separátorem cesty (`/` nebo `\\`) a soubor existuje. |
| **Obrázky se neextrahují** | Implementujte logiku uvnitř `VisitImageStart`, která zapíše `image.getImageData()` do souboru nebo proudu. |
| **Velké sešity způsobují vysokou spotřebu paměti** | Zpracovávejte dokument stránku po stránce nebo použijte streamingové API, pokud jsou k dispozici. |

## Často kladené otázky

**Q: Mohu extrahovat konkrétní typy obsahu z dokumentu OneNote?**  
A: Ano, implementací pouze těch metod visitoru, které potřebujete (např. `VisitRichTextStart` pro text, `VisitImageStart` pro obrázky).

**Q: Je Aspose.Note for Java kompatibilní s různými verzemi souborů OneNote?**  
A: Rozhodně. Knihovna podporuje soubory .one vytvořené nedávnými verzemi Microsoft OneNote.

**Q: Mohu tento proces extrakce integrovat do své Java aplikace?**  
A: Ano. Ukázaný kód je samostatný příklad, který můžete vložit přímo do libovolného Java projektu.

**Q: Zvládá Aspose.Note for Java složité struktury OneNote?**  
A: Ano. Vzor Visitor vám umožňuje procházet vnořené osnovy, skupiny a vložené objekty bez ztráty hierarchie.

**Q: Existuje limit velikosti OneNote dokumentu, který lze zpracovat?**  
A: I když neexistuje pevný limit, extrémně velké sešity mohou vyžadovat více haldy; zvažte jejich zpracování po částech.

**Q: Jak extrahuji obrázky z OneNote?**  
A: Implementujte metodu `VisitImageStart`, která získá `image.getImageData()` a zapíše bajty do souboru.

---

**Poslední aktualizace:** 2025-12-03  
**Testováno s:** Aspose.Note for Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}