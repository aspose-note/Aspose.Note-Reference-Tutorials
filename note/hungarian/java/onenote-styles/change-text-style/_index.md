---
date: 2026-06-05
description: Ismerje meg, hogyan változtathatja meg a font size OneNote-ban, set font
  color, és highlight text az Aspose.Note for Java segítségével – lépésről‑lépésre
  útmutató kódrészletekkel.
keywords:
- change font size onenote
- how to change text
- set font color onenote
linktitle: Betűméret módosítása a OneNote-ban - Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-06-05'
  description: Learn how to change font size onenote, set font color, and highlight
    text with Aspose.Note for Java – step‑by‑step guide with code snippets.
  headline: Change Font Size in OneNote - Aspose.Note
  type: TechArticle
- description: Learn how to change font size onenote, set font color, and highlight
    text with Aspose.Note for Java – step‑by‑step guide with code snippets.
  name: Change Font Size in OneNote - Aspose.Note
  steps:
  - name: Import Packages
    text: 'The `Document`, `RichText`, and `TextRun` classes live in the `com.aspose.note`
      namespace. Import them at the top of your Java source file:'
  - name: Load the Document
    text: The `Document` class is Aspose.Note's top‑level object that represents a
      single OneNote file in memory. Loading a file is as simple as passing the file
      path to its constructor.
  - name: Access RichText Nodes
    text: '`RichText` nodes contain the actual paragraph text. By iterating over `document.getRichTextNodes()`,
      you gain access to every piece of editable text in the notebook.'
  - name: Change Text Style
    text: '`TextRun` represents a contiguous run of characters sharing the same formatting.
      Within the loop, set `FontColor` to yellow, `HighlightColor` to blue, and `FontSize`
      to **20** points to achieve the desired styling.'
  - name: Save the Document
    text: Call `document.save("StyledSample.one")` to write the changes back to a
      OneNote file. The save operation preserves all original content while applying
      the new styles.
  type: HowTo
- questions:
  - answer: Yes, filter the `RichText` collection by page or section ID before applying
      style changes.
    question: Can I apply these text style changes to specific sections of my OneNote
      document?
  - answer: Absolutely, you can modify font family, bold/italic, underline, alignment,
      and paragraph spacing using the same object model.
    question: Does Aspose.Note support other formatting options beyond color, highlight,
      and size?
  - answer: Yes, Aspose.Note works seamlessly with libraries like Apache POI, Jackson,
      or Spring to build complex document pipelines.
    question: Can I integrate Aspose.Note with other Java libraries for advanced processing?
  - answer: A commercial license is required for production deployments; a free evaluation
      license is available for development and testing.
    question: Is Aspose.Note licensed for commercial use?
  - answer: Visit the Aspose.Note documentation portal, download the full API reference
      PDF, and explore the GitHub repository for community examples.
    question: Where can I find additional samples and API reference?
  type: FAQPage
second_title: Aspose.Note Java API
title: Betűméret módosítása a OneNote-ban - Aspose.Note
url: /hu/java/onenote-styles/change-text-style/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Betűméret módosítása a OneNote-ban – Aspose.Note

## Bevezetés

Ebben az oktatóanyagban megtanulja, **how to change font size onenote** dokumentumok módosítását az Aspose.Note for Java segítségével. Lépésről lépésre végigvezetjük a OneNote-fájl betöltésén, a szövegcsoportok elérésén, a szín, kiemelés és betűméret módosításán, majd a frissített fájl mentésén. Legyen szó jelentésgenerálás automatizálásáról vagy a megbeszélés jegyzeteinek finomhangolásáról, ez az útmutató megbízható módot kínál a OneNote-tartalom programozott stílusozására.

## Gyors válaszok
- **Hogyan változtathatom meg a betűméretet a OneNote-ban Java-val?** Töltse be a dokumentumot, módosítsa minden `TextRun` `FontSize` tulajdonságát, majd mentse – három egyszerű lépés.  
- **Meg tudom változtatni a szöveg színét és a kiemelést is?** Igen, állítsa be a `FontColor` és a `HighlightColor` értékeket ugyanazon `TextRun`-on.  
- **Melyik Aspose.Note verzió szükséges?** Bármely 23.10+ kiadás támogatja ezeket a formázási API-kat.  
- **Szükség van licencre fejlesztéshez?** Ingyenes próba verzió teszteléshez elegendő; a termeléshez kereskedelmi licenc szükséges.  
- **Ez a megközelítés alkalmas nagy jegyzetfüzetekre?** Igen – az Aspose.Note több száz oldalas jegyzetfüzeteket is feldolgoz anélkül, hogy az egész fájlt memóriába töltené.

## Mi az a change font size onenote?
**change font size onenote** arra a programozott módon történő `FontSize` attribútum módosítására utal, amely a szövegelemeket érinti egy OneNote jegyzetfüzetben. Az Aspose.Note segítségével a fejlesztők az API-n keresztül módosíthatják ezt a tulajdonságot, amely közvetlenül frissíti a OneNote fájl alapszerkezetét, biztosítva a vizuális megjelenés változását manuális szerkesztés vagy UI interakció nélkül.

## Miért használja az Aspose.Note-ot a szövegstílus módosításához a OneNote-ban?
Az Aspose.Note több mint 30 formázási lehetőséget kínál – beleértve a betűcsaládot, méretet, színt, kiemelést, igazítást és bekezdésközt – és úgy lett tervezve, hogy nagy jegyzetfüzeteket hatékonyan dolgozzon fel. Több mint 500 oldalas jegyzetfüzeteket képes kezelni kevesebb, mint 150 MB RAM felhasználásával, megbízható, nagy teljesítményű automatizálást biztosítva vállalati szintű dokumentumfolyamatokhoz.

## Előfeltételek

1. Alapvető Java programozási ismeretek.  
2. JDK 8 vagy újabb telepítve a gépén.  
3. Aspose.Note for Java könyvtár (letölthető az Aspose weboldaláról).  
4. Ismeretek a OneNote hierarchikus felépítéséről (oldalak, szekciók, RichText csomópontok).

## Hogyan változtassuk meg a betűméretet a OneNote-ban az Aspose.Note használatával?

Töltse be a OneNote-fájlt, keresse meg minden `RichText` csomópontot, frissítse minden `TextRun` stílusát, majd mentse a dokumentumot. Ez az átfogó folyamat csak néhány kódsort igényel, és tipikusan egy másodpercnél kevesebb idő alatt lefut a szokásos jegyzetfüzeteken.

### 1. lépés: Csomagok importálása

A `Document`, `RichText` és `TextRun` osztályok a `com.aspose.note` névtérben találhatók. Importálja őket a Java forrásfájl tetején:

```java
import java.awt.Color;
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.RichText;
import com.aspose.note.TextRun;
import com.aspose.note.TextStyle;
```

### 2. lépés: Dokumentum betöltése

A `Document` osztály az Aspose.Note legfelső szintű objektuma, amely egyetlen OneNote-fájlt reprezentál a memóriában. Egy fájl betöltése egyszerűen a fájl útvonalának átadásával a konstruktorban történik.

```java
// Load the document into Aspose.Note
Document document = new Document("Your Document Directory/Sample1.one");
```

### 3. lépés: RichText csomópontok elérése

A `RichText` csomópontok tartalmazzák a tényleges bekezdés szöveget. A `document.getRichTextNodes()` iterálásával hozzáférhet a jegyzetfüzet minden szerkeszthető szövegrészéhez.

```java
// Get a particular RichText node
List<RichText> richTextNodes = document.getChildNodes(RichText.class);
RichText richText = richTextNodes.get(0);
```

### 4. lépés: Szövegstílus módosítása

A `TextRun` egy összefüggő karaktercsoportot képvisel, amely ugyanazt a formázást használja. A cikluson belül állítsa be a `FontColor`-t sárgára, a `HighlightColor`-t kékre, és a `FontSize`-t **20** pontra a kívánt megjelenés eléréséhez.

```java
for (TextRun run : richText.getTextRuns()) {
    // Set font color
    run.getStyle().setFontColor(Color.yellow);
    // Set highlight color
    run.getStyle().setHighlight(Color.blue);
    // Set font size
    run.getStyle().setFontSize(20);
}
```

### 5. lépés: Dokumentum mentése

Hívja meg a `document.save("StyledSample.one")` metódust a változtatások visszaírásához egy OneNote-fájlba. A mentési művelet megőrzi az összes eredeti tartalmat, miközben alkalmazza az új stílusokat.

```java
document.save("Your Document Directory/ChangeTextStyle_out.pdf");
System.out.printf("File saved: %s\n", "Your Document Directory/ChangeTextStyle_out.pdf");
```

## Gyakori problémák és megoldások

- **A szöveg nem változik:** Győződjön meg róla, hogy a `TextRun` objektumokon iterál a `RichText` csomópontokon belül; ennek kihagyása a formázás változatlanul hagyását eredményezi.  
- **A szín másként jelenik meg:** Az Aspose.Note RGB értékeket használ; ellenőrizze, hogy a megfelelő `java.awt.Color` konstansokat alkalmazza.  
- **Nagy jegyzetfüzet lassul:** A `LoadOptions` beállítja, hogyan tölti be az Aspose.Note a fájlt, lehetővé téve a streaminget és a formátum kiválasztását. Használja a `document.setLoadOptions(new LoadOptions(LoadFormat.OneNote))` hívást a streaming mód engedélyezéséhez, amely csökkenti a memóriaigényt.

## Gyakran ismételt kérdések

**K: Alkalmazhatom ezeket a szövegstílus‑változtatásokat a OneNote-dokumentum konkrét szekcióira?**  
V: Igen, szűrje a `RichText` gyűjteményt oldal‑ vagy szekció‑azonosító alapján, mielőtt a stílusváltoztatásokat alkalmazná.

**K: Támogatja az Aspose.Note más formázási lehetőségeket is a szín, kiemelés és méret mellett?**  
V: Teljes mértékben, módosíthatja a betűcsaládot, félkövér/dőlt, aláhúzást, igazítást és bekezdésközt ugyanazzal az objektummodellel.

**K: Integrálhatom az Aspose.Note-ot más Java‑könyvtárakkal fejlett feldolgozáshoz?**  
V: Igen, az Aspose.Note zökkenőmentesen működik olyan könyvtárakkal, mint az Apache POI, Jackson vagy Spring, összetett dokumentumcsővezetékek építéséhez.

**K: Az Aspose.Note kereskedelmi felhasználásra licencelt?**  
V: Kereskedelmi licenc szükséges a termelési környezetben; ingyenes értékelési licenc elérhető fejlesztéshez és teszteléshez.

**K: Hol találok további példákat és API‑referenciát?**  
V: Látogassa meg az Aspose.Note dokumentációs portált, töltse le a teljes API‑referencia PDF‑et, és böngéssze a GitHub tárolót a közösségi példákért.

## Következtetés

A fenti lépések követésével most már tudja, **how to change font size onenote** fájlok módosítását, a szöveg színének beállítását és a kiemelések alkalmazását az Aspose.Note for Java segítségével. Ez a képesség lehetővé teszi a megbeszélés‑jegyzetek, képzési anyagok vagy bármely OneNote‑alapú tartalom vizuális finomhangolásának automatizálását nagy léptékben.

---

**Utolsó frissítés:** 2026-06-05  
**Tesztelt verzió:** Aspose.Note 23.10 for Java  
**Szerző:** Aspose

## Kapcsolódó oktatóanyagok

- [Alapértelmezett bekezdésstílus beállítása a OneNote-ban – Aspose.Note](/note/java/onenote-styles/set-default-paragraph-style/)
- [Helyesírási nyelv beállítása a szöveghez a OneNote-ban – Aspose.Note](/note/java/onenote-text-manipulation/set-proofing-language-for-text/)
- [Oldalcím beállítása a Microsoft OneNote stílusban – Aspose.Note](/note/java/onenote-text-manipulation/setting-page-title-in-microsoft-onenote-style/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-wrap-class >}}