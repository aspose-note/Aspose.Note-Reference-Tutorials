---
date: 2025-12-02
description: Naučte se, jak exportovat písma při ukládání OneNote jako HTML pomocí
  Aspose.Note pro Javu. Tento průvodce vám ukáže, jak programově vytvořit OneNote
  a vložit písma, CSS a obrázky.
language: cs
linktitle: How to Export Fonts When Saving OneNote as HTML – Java
second_title: Aspose.Note Java API
title: Jak exportovat písma při ukládání OneNote do HTML – Java
url: /java/onenote-document-loading/create-onenote-save-to-html/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak exportovat písma při ukládání OneNote jako HTML – Java

## Úvod

V tomto tutoriálu se dozvíte **jak exportovat písma**, když **uložíte OneNote jako HTML** pomocí Aspose.Note pro Java. Provedeme vás vytvořením OneNote dokumentu programově, nastavením možností uložení HTML a vložením potřebných souborů písem, aby výsledné HTML vypadalo přesně jako původní stránky OneNote. Tento přístup je ideální, pokud potřebujete zachovat vizuální věrnost obsahu OneNote ve webově přátelském formátu.

## Rychlé odpovědi
- **Jaká knihovna provádí export?** Aspose.Note for Java  
- **Lze písma vložit do HTML?** Ano – nastavte `ExportFonts` na `ExportEmbedded`  
- **Potřebuji licenci pro produkci?** Platná licence Aspose.Note je vyžadována pro komerční použití  
- **Jaká verze Javy je podporována?** Java 8 nebo vyšší  
- **Je možné uložit zdroje do samostatných souborů?** Rozhodně – nakonfigurujte `ResourceExportType` podle potřeby  

## Co znamená „jak exportovat písma“ v kontextu konverze OneNote do HTML?

Když převádíte notebook OneNote do HTML, vizuální vzhled závisí na CSS, obrázcích a zejména na písmech použitých v původních stránkách. **Exportování písem** znamená vložení souborů písem (např. TTF) přímo do balíčku HTML, aby prohlížeče mohly vykreslit text přesně tak, jak se zobrazuje v OneNote, i když uživatel nemá tato písma nainstalována lokálně.

## Proč vytvářet OneNote programově a ukládat jej jako HTML?

- **Automatizace:** Generujte zprávy, dokumentaci nebo články znalostní báze z OneNote bez ručního kopírování.  
- **Konzistence:** Zachovejte rozvržení, stylování a vlastní písma napříč zařízeními.  
- **Přenositelnost:** HTML je univerzálně zobrazitelné – není potřeba klient OneNote.  

## Předpoklady

1. Nainstalovaný Java Development Kit (JDK) 8 nebo novější.  
2. Knihovna Aspose.Note pro Java – stáhněte ji z [here](https://releases.aspose.com/note/java/).  
3. Ukázkový soubor OneNote (`.one`) k načtení, nebo můžete vytvořit nový programově.  

## Import balíčků

Nejprve importujte požadované třídy do svého Java projektu:

```java
import java.io.ByteArrayOutputStream;
import java.io.File;
import java.io.FileOutputStream;
import java.io.IOException;
import java.io.OutputStream;
import java.io.OutputStreamWriter;
import java.nio.file.Paths;
import com.aspose.note.CssSavingArgs;
import com.aspose.note.Document;
import com.aspose.note.FontFaceType;
import com.aspose.note.FontSavingArgs;
import com.aspose.note.HtmlSaveOptions;
import com.aspose.note.ICssSavingCallback;
import com.aspose.note.IFontSavingCallback;
import com.aspose.note.IImageSavingCallback;
import com.aspose.note.ImageSavingArgs;
import com.aspose.note.ResourceExportType;
```

## Jak exportovat písma při ukládání OneNote jako HTML?

Níže je krok za krokem průvodce, který vám ukáže **jak exportovat písma** a další zdroje.

### Krok 1: Vytvořit OneNote dokument programově  

```java
Document document = new Document("Path_to_your_sample_one_file");
```

Tento řádek načte existující soubor `.one`. Pokud potřebujete **vytvořit OneNote programově**, můžete vytvořit novou instanci objektu `Document` a přidat sekce/stránky pomocí API (není zde ukázáno, aby byl zachován hlavní důraz na exportování písem).

### Krok 2: Uložit do paměťového proudu s vloženými písmy  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

- `setExportFonts(ResourceExportType.ExportEmbedded)` říká Aspose.Note, aby **exportoval písma** přímo do HTML balíčku.  
- `setFontFaceTypes(FontFaceType.Ttf)` zajišťuje použití TrueType písem, která mají širokou podporu v prohlížečích.

### Krok 3: Uložit jako HTML se samostatnými soubory zdrojů (stále exportuje písma)  

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

I když jsou CSS a obrázky vloženy, můžete změnit `ResourceExportType` na `ExportExternal`, pokud dáváte přednost samostatným souborům pro snadnější cachování. Klíčová část – **exportování písem** – zůstává nezměněna.

### Krok 4: Použít zpětné volání pro kontrolu, kam se každý zdroj uloží  

```java
Document document = new Document("Path_to_your_sample_one_file");

UserSavingCallbacks savingCallbacks = new UserSavingCallbacks();
savingCallbacks.setRootFolder("documentFolder");
savingCallbacks.setCssFolder("css");
savingCallbacks.setKeepCssStreamOpened(true);
savingCallbacks.setImagesFolder("images");
savingCallbacks.setFontsFolder("fonts");

HtmlSaveOptions options = new HtmlSaveOptions();
options.setFontFaceTypes(FontFaceType.Ttf);
options.setCssSavingCallback(savingCallbacks);
options.setImageSavingCallback(savingCallbacks);
options.setFontSavingCallback(savingCallbacks);
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);

File dir = new File(savingCallbacks.getRootFolder());
if (!dir.exists()) {
    dir.mkdir();
}

document.save(Paths.get(savingCallbacks.getRootFolder(), "document.html").toString(), options);
```

Třída `UserSavingCallbacks` (budete muset implementovat `ICssSavingCallback`, `IImageSavingCallback` a `IFontSavingCallback`) vám poskytuje plnou kontrolu nad strukturou složek, což vám umožní uchovávat písma v samostatném adresáři `fonts`, přičemž **exportování písem** bude stále správně.

## Časté problémy a tipy

- **Chybějící písma ve výstupu:** Ověřte, že je nastaveno `setExportFonts(ResourceExportType.ExportEmbedded)` a že zdrojový soubor OneNote skutečně používá vložená písma.  
- **Velké HTML soubory:** Vkládání písem může zvýšit velikost. Pokud je šířka pásma problém, přepněte `ExportFonts` na `ExportExternal` a hostujte písma na CDN.  
- **Chyby v implementaci zpětných volání:** Ujistěte se, že vaše třídy zpětných volání správně zapisují proud a uzavírají zdroje, aby nedošlo k poškození souboru.  

## Často kladené otázky

**Q: Mohu převést více OneNote dokumentů do HTML najednou?**  
A: Ano, projděte každou instanci `Document` a použijte stejné `HtmlSaveOptions`.

**Q: Podporuje Aspose.Note pro Java další výstupní formáty kromě HTML?**  
A: Rozhodně. Můžete exportovat do PDF, DOCX, PNG, JPEG a dalších pomocí příslušných možností uložení.

**Q: Je k dispozici zkušební verze Aspose.Note pro Java?**  
A: Ano, stáhněte si bezplatnou zkušební verzi z [here](https://releases.aspose.com/).

**Q: Kde mohu získat podporu pro Aspose.Note pro Java?**  
A: Navštivte [Aspose.Note forum](https://forum.aspose.com/c/note/28) pro komunitní a oficiální pomoc.

**Q: Jak mohu zakoupit licenci pro Aspose.Note pro Java?**  
A: Licence jsou k dispozici na [Aspose website](https://purchase.aspose.com/buy).

## Závěr

Nyní víte **jak exportovat písma**, když **ukládáte OneNote jako HTML** pomocí Aspose.Note pro Java. Konfigurací `HtmlSaveOptions` a volitelným použitím zpětných volání můžete zachovat přesný vzhled vašich OneNote stránek – včetně vlastních písem – při jejich publikaci na webu. Klidně experimentujte s různými nastaveními `ResourceExportType`, aby vyhovovaly výkonu a požadavkům na úložiště vašeho projektu.

---

**Last Updated:** 2025-12-02  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
