---
date: 2026-09-24
description: Ismerje meg, hogyan adhat hozzá címkét a OneNote-hoz, hozhat létre vázlatot
  a OneNote-ban, és exportálhatja a OneNote-ot PDF-be az Aspose.Note for Java segítségével.
keywords:
- add tag onenote
- how to add tag
- how to create outline
- export onenote pdf
- java convert onenote pdf
lastmod: 2026-09-24
linktitle: Hogyan adjunk hozzá címkét a OneNote-hoz és hozzunk létre vázlatot a OneNote-ban
og_description: Adjon hozzá címkét a OneNote-hoz és hozzon létre vázlatot a OneNote-ban
  az Aspose.Note for Java használatával, majd exportálja a jegyzetfüzetet PDF-be.
  Kövesse a lépésről‑lépésre kódot és a legjobb gyakorlatokat.
og_image_alt: Screenshot showing OneNote outline with tags created via Aspose.Note
  Java API
og_title: Címke hozzáadása a OneNote-hoz és vázlat létrehozása a OneNote-ban – Aspose.Note
  útmutató
schemas:
- author: Aspose
  dateModified: '2026-09-24'
  description: Learn how to add tag onenote, create outline in OneNote, and export
    OneNote to PDF using Aspose.Note for Java.
  headline: How to add tag onenote and create outline in OneNote
  type: TechArticle
- questions:
  - answer: Aspose.Note primarily targets Java, but equivalent libraries exist for
      .NET and other platforms.
    question: Can I use Aspose.Note for Java with other programming languages?
  - answer: Yes—its API is well‑documented, and the step‑by‑step approach in this
      guide is friendly for developers of any skill level.
    question: Is Aspose.Note suitable for beginners?
  - answer: You can get a temporary license from the **[temporary license page](https://purchase.aspose.com/temporary-license/)**.
    question: How do I obtain a temporary license for Aspose.Note for Java?
  - answer: Visit the **[Aspose.Note forum](https://forum.aspose.com/c/note/28)**
      for community help and official assistance.
    question: Where can I find additional support?
  - answer: Yes—download a trial version from the **[Aspose releases page](https://releases.aspose.com/)**.
    question: Is a free trial available?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote tagging
- Aspose.Note
- Java note processing
title: Hogyan adjunk hozzá címkét a OneNote-hoz és hozzunk létre vázlatot a OneNote-ban
url: /hu/java/onenote-tag-operations/add-tag/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hogyan adjon hozzá címkét a OneNote-hoz és hozza létre a vázlatot a OneNote-ban

## Bevezetés
Ebben az útmutatóban megtanulja, hogyan **add tag onenote** és hogyan építsen fel egy strukturált vázlatot egy OneNote jegyzetfüzetben az Aspose.Note for Java használatával. Lépésről lépésre végigvezetjük, elmagyarázzuk, miért fontos minden API hívás, és végül **exporting the notebook to PDF**-et hajtunk végre, hogy megoszthassa a csapattagokkal a kifinomult, kereshető dokumentumot.

## Gyors válaszok
- **Mit jelent a “create outline in OneNote”?** Hierarchikus fát épít a címsorokból és alrészekből, amelyet ki- és összecsukhat.  
- **Melyik osztály ad hozzá címkéket a OneNote-hoz?** Használja a `NoteTag` osztályt az Aspose.Note for Java-ból.  
- **Exportálhatom az eredményt PDF-be?** Igen – hívja meg a `doc.save("output.pdf", SaveFormat.Pdf)`-t.  
- **Szükségem van licencre a termeléshez?** Egy ideiglenes licenc elérhető teszteléshez; a kereskedelmi használathoz teljes licenc szükséges.  
- **Mik a fő előfeltételek?** JDK telepítve, Aspose.Note for Java könyvtár, és alapvető Java ismeretek.

## Mi a “create outline in OneNote”?
A vázlat létrehozása a OneNote-ban azt jelenti, hogy `Outline` és `OutlineElement` objektumokat adunk hozzá, amelyek fastruktúrát definiálnak a jegyzetekhez. Ez a hierarchia lehetővé teszi az információk összecsukását, kibontását és szervezését, akárcsak a dokumentumok címsorai. Emellett programozott navigációt tesz lehetővé, és támogatja a hierarchia exportálását olyan formátumokba, mint a PDF, ahol minden szint könyvjelzővé válhat.

## Miért adjunk címkét a OneNote-hoz?
A címke hozzáadása a OneNote-hoz vizuális jelzőt biztosít – például csillagot, jelölőnégyzetet vagy egyedi ikont –, amely azonnal felhívja a figyelmet, javítja a kereshetőséget, és segíti a csapatokat a feladatok priorizálásában. Az Aspose.Note segítségével programozottan csatolhat egy `NoteTag`-et bármely szövegrészhez, biztosítva a konzisztenciát számos oldalon.

## Az Aspose.Note mérhető előnyei
Az Aspose.Note **30+ bemeneti és kimeneti formátumot** támogat (beleértve a DOCX, PDF, HTML és képtípusokat), és képes **legfeljebb 500 oldalas** jegyzetfüzeteket feldolgozni anélkül, hogy az egész fájlt a memóriába töltené, így nagy teljesítményű konverziókat biztosít a szabványos szerverhardveren.

## Előfeltételek
- Java Development Kit (JDK) 8 vagy újabb.  
- Aspose.Note for Java könyvtár – töltse le a **[Aspose.Note for Java download page](https://releases.aspose.com/note/java/)** oldalról.  
- Alapvető ismeretek a Java szintaxisról és a Maven/Gradle projekt beállításáról.

## Csomagok importálása
A `Document`, `Page`, `Outline`, `OutlineElement`, `RichText` és `NoteTag` osztályok a `com.aspose.note` névtérben találhatók. Importálja őket a Java fájl tetején:

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.TagIcon;
import com.aspose.note.ParagraphStyle;
```

Törjük le az importálást lépésről lépésre.

## 1. lépés: Dokumentum és oldal beállítása
`Document` a teljes OneNote jegyzetfüzetet képviseli a memóriában, míg a `Page` egyetlen vászon a jegyzetfüzeten belül.  

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

A `Document` osztály a teljes OneNote fájlt reprezentálja a memóriában, míg a `Page` objektum a vászon, ahol a vázlatok és címkék elhelyezésre kerülnek.

## 2. lépés: Vázlat létrehozása
`Outline` egy tároló, amely a `OutlineElement` objektumok hierarchiáját tartalmazza, ezáltal a jegyzetfüzet szerkezeti fát alkotja.  

```java
Outline outline = new Outline();
```

A vázlatok biztosítják a szerkezeti gerincet, amely lehetővé teszi, hogy **create outline in OneNote**-t hajtson végre, és az információkat rendezett módon tartsa.

## 3. lépés: Outline element és bekezdésstílus inicializálása
`OutlineElement` egy egyedi csomópontot (címsort) képvisel a vázlatban, a `ParagraphStyle` pedig meghatározza a betűtípust, méretet és behúzást.  

```java
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                .setFontColor(Color.black)
                                .setFontName("Arial")
                                .setFontSize(10);
```

`OutlineElement` egyetlen csomópontot (címsort) jelent a vázlatban, a `ParagraphStyle` pedig szabályozza a betűtípust, méretet és a behúzást.

## 4. lépés: Rich text hozzáadása note tag-gel
`RichText` tárolja a tényleges szövegtartalmat, a `NoteTag` pedig egy vizuális címkét (ikont) csatol a szöveghez.  

```java
RichText text = new RichText().append("OneNote text.");
text.setParagraphStyle(textStyle);
NoteTag noteTag = NoteTag.createYellowStar();
text.getTags().add(noteTag);
```

`RichText` a tényleges szöveget tartalmazza, míg a `NoteTag` **adds tag to OneNote**-ként vizuális jelzést ad a szöveg mellett.

## 5. lépés: Vázlat struktúra felépítése
Adja hozzá a `RichText` csomópontot a `OutlineElement`-hez, majd adja az elemet a `Outline`-hoz, végül csatolja a vázlatot az oldalhoz.  

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

Ez a lépés befejezi a hierarchikus elrendezést, befejezve a **create outline in OneNote** munkafolyamatot.

## 6. lépés: Dokumentum mentése PDF-ként
`SaveFormat.Pdf` azt mondja az Aspose.Note-nak, hogy a jegyzetfüzetet PDF fájlként írja ki.  

```java
doc.save(dataDir + "AddTag_out.pdf", SaveFormat.Pdf);
System.out.printf("File Saved: %s\n", dataDir + "AddTag_out.pdf");
```

Az eredményül kapott PDF megőrzi a vázlat hierarchiáját és a vizuális címkéket, így kereshető és nyomtatható.

## Gyakori buktatók és hibaelhárítás
- **A címke nem jelenik meg:** Győződjön meg arról, hogy a `NoteTag`-et a `RichText` objektumhoz *előtt* adja hozzá, mielőtt a szöveget az outline elementhez csatolná.  
- **A vázlat nem csukható össze PDF-ben:** A PDF-megjelenítők nem támogatják a OneNote interaktív vázlatát; a hierarchia helyette könyvjelzőként marad meg.  
- **Nagy jegyzetfüzetek memória nyomást okoznak:** `Document.saveOptions.setLoadOnDemand(true)` használatával lazán dolgozhatja fel az oldalakat.

## Gyakran feltett kérdések

**K: Használhatom az Aspose.Note for Java-t más programozási nyelvekkel?**  
A: Az Aspose.Note elsősorban Java-ra van célozva, de ekvivalens könyvtárak léteznek .NET és más platformok számára.

**K: Alkalmas az Aspose.Note kezdőknek?**  
A: Igen – API-ja jól dokumentált, és ebben az útmutatóban a lépésről‑lépésre megközelítés minden szintű fejlesztő számára barátságos.

**K: Hogyan szerezhetek ideiglenes licencet az Aspose.Note for Java-hoz?**  
A: Ideiglenes licencet a **[temporary license page](https://purchase.aspose.com/temporary-license/)** oldalról kaphat.

**K: Hol találok további támogatást?**  
A: Látogassa meg a **[Aspose.Note fórumot](https://forum.aspose.com/c/note/28)** a közösségi segítségért és a hivatalos támogatásért.

**K: Elérhető ingyenes próba?**  
A: Igen – próbaverziót tölthet le a **[Aspose releases page](https://releases.aspose.com/)** oldalról.

**További kérdések és válaszok**

**K: Testreszabhatom a címke ikont?**  
A: Igen – az Aspose.Note előre definiált ikonokat biztosít a `TagIcon` enumon keresztül, és lehetővé teszi egyedi képek megadását is.

**K: Hogyan módosíthatom a PDF kimeneti beállításokat?**  
A: Használja a `PdfSaveOptions`-t a képminőség, tömörítés és biztonság beállításához, mielőtt meghívná a `doc.save`-ot.

**K: Lehetséges több címkét hozzáadni ugyanahhoz a szöveghez?**  
A: Természetesen. Hívja meg a `richText.getTags().add()`-t többször különböző `NoteTag` példányokkal.

---

## Kapcsolódó útmutatók

- [Címkék hozzáadása a OneNote-hoz – Címkézett OneNote dokumentum létrehozása az Aspose.Note segítségével](/note/java/onenote-tag-operations/)
- [Hogyan hozzunk létre OneNote dokumentumot – Szövegcsoport hozzáadása címkével az Aspose.Note használatával](/note/java/onenote-tag-operations/add-text-node-with-tag/)
- [Találkozó jegyzet sablon generálása az Aspose.Note for Java-val – Vázlat létrehozása a OneNote-ban](/note/java/onenote-tag-operations/generate-template-for-meeting-notes/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}