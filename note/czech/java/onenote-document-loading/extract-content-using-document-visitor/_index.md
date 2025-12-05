---
date: 2025-12-04
description: Naučte se, jak extrahovat obrázky ze souborů OneNote a převést OneNote
  na text v Javě pomocí Aspose.Note. Podrobný průvodce krok za krokem s ukázkami kódu.
language: cs
linktitle: Extract Images from OneNote using Document Visitor - Java
second_title: Aspose.Note Java API
title: Extrahovat obrázky z OneNote pomocí Document Visitor – Java
url: /java/onenote-document-loading/extract-content-using-document-visitor/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Extrahování obrázků z OneNote pomocí Document Visitor - Java

## Úvod

Aspose.Note for Java usnadňuje **extrahování obrázků z OneNote** sešitů a také čtení podkladového souboru `.one` v Javě. V tomto tutoriálu vás provedeme kompletním praktickým příkladem, který ukazuje, jak načíst soubor OneNote, projít jeho strukturu pomocí vlastního `DocumentVisitor` a získat jak obrázky, tak prostý text. Na konci také budete vědět, jak **převést OneNote na text**, pokud potřebujete jen textový obsah.

## Rychlé odpovědi
- **Jakou knihovnu potřebuji?** Aspose.Note pro Java (odkaz ke stažení níže).  
- **Mohu extrahovat jen obrázky?** Ano – implementujte metodu `VisitImageStart` ve `DocumentVisitor`.  
- **Jak načíst soubor .one v Javě?** Použijte `new Document(path, new LoadOptions())`.  
- **Potřebuji licenci pro produkci?** Pro ne‑zkušební použití je vyžadována komerční licence.  
- **Jaká verze Javy je podporována?** JDK 8 nebo vyšší.

## Předpoklady

1. Nainstalovaný Java Development Kit (JDK) 8 nebo novější.  
2. Stažená knihovna Aspose.Note pro Java. Můžete ji stáhnout **[zde](https://releases.aspose.com/note/java/)**.  
3. Dokument OneNote (`.one` soubor), ze kterého chcete extrahovat obrázky nebo jej převést na text.

## Import balíčků

Nejprve importujte potřebné třídy z API Aspose.Note.

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

## Krok 1: Nastavení vlastního Document Visitor

Vytvořte třídu, která rozšiřuje `DocumentVisitor`. Tato třída bude volána pro každý uzel v dokumentu OneNote, což vám umožní **extrahovat obrázky z OneNote** a volitelně sbírat text.

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

## Krok 2: Implementace metod Visitor

Přidejte přepsání (overrides) proy uzlů, které vás zajímají. Níže zpracováváme rich‑text, obrázky, tituly, stránky, obrysy a elementy obrysu. Metoda `VisitImageStart` je místem, kde probíhá extrakce obrázku.

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
    // Here you could save the image to disk or process it further
    System.out.println("Found image with size: " + image.getData().length + " bytes");
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

### Proč implementovat tyto metody?

- **Extrahovat obrázky z OneNote:** `VisitImageStart` poskytuje přímý přístup k surovým bajtům obrázku.  
- **Převést OneNote na text:** `VisitRichTextStart` sbírá textový obsah, což umožňuje jednoduchou operaci **převodu OneNote na text**.  
- **Číst .one soubor v Javě:** Vzor Visitor abstrahuje podkladovou strukturu souboru `.one`, takže nemusíte sami parsovat binární formát.

## Krok 3: Spuštění Visitoru z hlavní metody

Načtěte soubor `.one`, vytvořte instanci vašeho visitoru a spusťte procházení.

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
    System.out.println(myConverter.GetText());   // Text extracted from the notebook
    System.out.println(myConverter.NodeCount()); // Total nodes visited
}
```

## Běžné případy použití

- **Automatizované reportování:** Vytažení obrázků a textu z OneNote sešitu schůzek pro vytvoření souhrnu v PDF nebo HTML.  
- **Migrace obsahu:** Převod starých archivů OneNote na soubory prostého textu pro indexaci nebo ingestování do vyhledávačů.  
- **Extrahování digitálních aktiv:** Sklízení vložených screenshotů, diagramů nebo fotografií pro opětovné použití v jiných aplikacích.

## Řešení problémů a tipy

- **Velké sešity:** Pokud narazíte na problémy s pamětí, zpracovávejte stránky jednotlivě kontrolou `VisitPageStart` a načítáním zdrojů na úrovni stránky jen podle potřeby.  
- **Formáty obrázků:** Objekt `Image` vrací surové bajty; může být nutné detekovat formát (PNG, JPEG) před uložením.  
- **Chyby licence:** Ujistěte se, že jste nastavili licenci Aspose (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`) před načtením dokumentu v produkci.

## Často kladené otázky

**Q: Můžu extrahovat konkrétní typy obsahu z dokumentu OneNote?**  
A: Ano – přepsáním (override) jen těch metod visitoru, které potřebujete (např. `VisitImageStart` pro obrázky, `VisitRichTextStart` pro text).

**Q: Je Aspose.Note pro Java kompatibilní s různými verzemi dokumentů OneNote?**  
A: Naprosto. Knihovna podporuje všechny hlavní verze souborů OneNote, takže můžete bezpečně **číst .one soubor v Javě** projekty bez ohledu na původní verzi OneNote.

**Q: Můžu integrovat tento proces extrakce do své Java aplikace?**  
A: Ano. Vzor Visitor funguje hladce v jakémkoli Java kódu; stačí přidat JAR knihovny a zavolat ukázkový kód výše.

**Q: Poskytuje Aspose.Note pro Java podporu pro práci se složitými dokumenty OneNote?**  
A: Ano. Vnořené obrysy, vložená média a vlastní data jsou všechny zpřístupněny přes API visitoru.

**Q: Existuje nějaký limit velikosti dokumentu OneNote, který lze zpracovat?**  
A: Neexistuje pevný limit, ale extrémně velké sešity mohou vyžadovat více paměti heap; zvažte jejich zpracování stránku po stránce.

**Q: Jak převést extrahovaný text do souboru prostého textu?**  
A: Po tom, co `myConverter.GetText()` vrátí `String`, zapište jej do souboru pomocí standardního Java I/O (`Files.write(Paths.get("output.txt"), text.getBytes());`).

---  

**Poslední aktualizace:** 2025-12-04  
**Testováno s:** Aspose.Note for Java 24.10  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}