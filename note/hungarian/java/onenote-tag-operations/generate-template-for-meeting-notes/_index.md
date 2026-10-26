---
date: 2026-10-26
description: Ismerje meg, hogyan adhat hozzá checkboxokat a OneNote-hoz egy meeting
  notes sablon generálása közben az Aspose.Note for Java segítségével, és hogyan szabhatja
  testre a font style-ot a OneNote-ban egyszerűen.
keywords:
- add checkboxes onenote
- generate meeting notes template
- customize font style onenote
- create outline onenote
lastmod: 2026-10-26
linktitle: Meeting Notes sablon generálása az Aspose.Note for Java-val – Vázlat létrehozása
  a OneNote-ban
og_description: Ismerje meg, hogyan adhat hozzá checkboxokat a OneNote-hoz egy meeting
  notes sablon generálása közben az Aspose.Note for Java segítségével, és hogyan szabhatja
  testre a font style-ot a OneNote-ban egyszerűen.
og_image_alt: 'Developer guide: add checkboxes onenote and generate meeting notes
  template using Aspose.Note for Java'
og_title: Checkboxok hozzáadása a OneNote-hoz és jegyzet sablon létrehozása Java-ban
schemas:
- author: Aspose
  dateModified: '2026-10-26'
  description: Learn how to add checkboxes onenote while generating a meeting notes
    template with Aspose.Note for Java, and customize font style onenote easily.
  headline: Add checkboxes onenote and create notes template in Java
  type: TechArticle
- questions:
  - answer: You can create a bulleted list and manually mark items, but using `NoteCheckBox`
      provides interactive checkboxes that sync with OneNote’s UI.
    question: How do I add a checklist to OneNote without using checkboxes?
  - answer: Absolutely. Just change the date formatting or pass a custom title string
      to reuse the same structure for each week.
    question: Can I use this template to create a meeting agenda template for weekly
      repeats?
  - answer: Define `ParagraphStyle` objects with your corporate font name, size, and
      color, then apply them to each `RichText` element as shown in Step 1.
    question: What is the best way to customize font style onenote for branding?
  - answer: Yes. After saving the OneNote file, you can load it with Aspose.Note and
      export to PDF using `Document.save("output.pdf", SaveFormat.Pdf)`.
    question: Does Aspose.Note support exporting the outline to PDF?
  - answer: You can set the checkbox state by adding a `NoteCheckBox` tag with the
      `Checked` property set to `true`.
    question: Is there a way to programmatically mark a checkbox as completed?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote
- Aspose.Note
- Java
- meeting notes template
- checkboxes
title: Checkboxok hozzáadása a OneNote-hoz és jegyzet sablon létrehozása Java-ban
url: /hu/java/onenote-tag-operations/generate-template-for-meeting-notes/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jelölőnégyzetek hozzáadása OneNote-hoz és jegyzet sablon létrehozása Java-ban

## Bevezetés
A modern együttműködő környezetekben a **add checkboxes onenote** gyorsan lehetővé teszi egy kifinomult megbeszélés jegyzet sablon generálását manuális formázás nélkül. Az Aspose.Note for Java teljes irányítást ad az oldalcímek, hierarchikus vázlatok, betűstílusok és interaktív jelölőnégyzetek felett, így másodpercek alatt létrehozhat egy újrahasználható napirendet. Ez az útmutató minden lépésen végigvezet – az szükséges osztályok importálásától a végleges OneNote fájl mentéséig – hogy Ön a megbeszélés tartalmára koncentrálhasson, ne pedig a fáradságos UI munkára.

## Gyors válaszok
- **Mi jelent a “add checkboxes onenote”?** Azt jelenti, hogy programozottan interaktív jelölőnégyzeteket szúrunk be egy OneNote vázlatba, akárcsak a felhasználói felület teszi.  
- **Melyik könyvtár segít ebben?** Az Aspose.Note for Java biztosítja a teljes API-t.  
- **Hozzáadhatok jelölőnégyzeteket a vázlathoz?** Igen – használja a `NoteCheckBox.createBlueCheckBox()` vagy más színváltozatokat.  
- **Szükségem van licencre?** Egy ingyenes próba verzió fejlesztéshez működik; a gyártási használathoz kereskedelmi licenc szükséges.  
- **Melyik Java verzió támogatott?** Java 8 és későbbi.

## Mi az a add checkboxes onenote?
Az add checkboxes onenote egy `NoteCheckBox` címkét szúr be egy `RichText` elembe, egy normál szövegsort interaktív jelölőnégyzetté alakítva, amelyet a felhasználók közvetlenül a OneNote felhasználói felületén bejelölhetnek vagy törölhetnek, megőrizve a jelölőnégyzet állapotát az eszközök között és biztosítva a konzisztenciát.

## Miért használja az Aspose.Note-ot egy megbeszélés jegyzet sablon generálásához?
Az Aspose.Note **50+ bemeneti és kimeneti formátumot** dolgoz fel, és képes **akár 500 soros** oldalakat kezelni anélkül, hogy a teljes dokumentumot a memóriába töltené, gyors és memóriahatékony nagy napirendek generálását biztosítva. Emellett folyékony API-t kínál a stílusozáshoz, támogatja a Unicode karaktereket, és zökkenőmentesen integrálódik más Aspose könyvtárakkal, így ideális vállalati szintű megbeszélés dokumentációs munkafolyamatokhoz.

## Előfeltételek
- Alapvető Java programozási ismeretek.  
- Az Aspose.Note for Java könyvtár telepítve van. **Letöltheti az Aspose.Note for Java** a hivatalos Aspose.Note for Java kiadási oldalról: [Aspose.Note for Java kiadási oldal](https://releases.aspose.com/note/java/).  
- Egy IDE, például Eclipse vagy IntelliJ IDEA.  

## Csomagok importálása
A `Document`, `Outline`, `ParagraphStyle`, `RichText` és `NoteCheckBox` osztályok a fő építőelemek.

`Document` a teljes OneNote fájlt reprezentálja a memóriában, lehetővé téve oldalak és tartalom hozzáadását vagy módosítását.  
`Outline` modellezi a OneNote-ban megjelenő hierarchikus lista struktúrát, lehetővé téve a beágyazott felsorolásjeleket és a számozást.  
`ParagraphStyle` újrahasználható betű- és bekezdésattribútumokat definiál, amelyeket több `RichText` elemre is alkalmazhat.  
`RichText` a bekezdés tényleges szövegtartalmát tárolja, és tartalmazhat címkéket, például `NoteCheckBox`.  
`NoteCheckBox` interaktív jelölőnégyzet címkét hoz létre, amely egy `RichText` bekezdéshez csatolható.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.text.DateFormat;
import java.time.Instant;
import java.util.Date;
import java.util.Locale;
```

## 1. lépés: dokumentum struktúra létrehozása
Először példányosítson egy `Document`-ot, állítson be egy oldalcímet, és definiáljon két újrahasználható `ParagraphStyle` objektumot – egyet a címsorokhoz és egyet a törzsszöveghez.

A `ParagraphStyle` objektumok lehetővé teszik, hogy ugyanazt a betűcsaládot, méretet és színt több bekezdésre alkalmazza a kód ismétlése nélkül.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Create an object of the Document class
ParagraphStyle headerStyle = new ParagraphStyle()
                                    .setFontName("Calibri")
                                    .setFontSize(16);
ParagraphStyle bodyStyle = new ParagraphStyle()
                                    .setFontName("Calibri")
                                    .setFontSize(12);
DateFormat dateFormat = DateFormat.getDateInstance(DateFormat.SHORT, Locale.US);
Document d = new Document();
boolean restartFlag = true;
RichText titleText = new RichText().append(String.format("Weekly meeting %s", dateFormat.format(Date.from(Instant.now()))));
titleText.setParagraphStyle(ParagraphStyle.getDefault());
Title title = new Title();
title.setTitleText(titleText);
Page page = new Page();
page.setTitle(title);
d.appendChildLast(page);
```

*Mit tettünk:*  
- Definiálta a `headerStyle`-t a címsorokhoz és a `bodyStyle`-t a normál szöveghez.  
- Létrehozott egy `Document`-ot és hozzáadott egy `Title`-t, amely tartalmazza a mai dátumot, így az oldal egyértelmű címet kap.

## 2. lépés: fontos pontok vázlatának elkészítése
Ezután adjon egy `Outline` objektumot az oldalhoz, és töltse fel olyan szakaszokkal, mint az „Agenda”, a „Discussion Items” és az „Action Items”.

Az `Outline` objektum a OneNote-ban látható hierarchikus listát reprezentálja. A `createListNumberingStyle` használatával számozott listát generálunk, amely minden új szakaszhoz újraindítható.

```java
Outline outline = page.appendChildLast(new Outline());
outline.setVerticalOffset(30);
outline.setHorizontalOffset(30);
RichText richText = outline.appendChildLast(new OutlineElement()).appendChildLast(new RichText());
richText.append("Important");
richText.setParagraphStyle(headerStyle);
for (String e: new String[] { "First", "Second", "Third" })
{
    OutlineElement outlineElement = outline.appendChildLast(new OutlineElement());
    outlineElement.setNumberList(createListNumberingStyle(bodyStyle, restartFlag));
    richText = outlineElement.appendChildLast(new RichText());
    richText.append(e);
    richText.setParagraphStyle(bodyStyle);
    restartFlag = false;
}
```

*Miért fontos ez:*  
- A vázlat hierarchia tükrözi azt a manuális struktúrát, amelyet a OneNote-ban beírna, biztosítva a konzisztenciát az összes generált oldalon.  
- A számozási stílusok rendezetten és könnyen követhetően tartják az egyes napirendi szakaszokat.

## 3. lépés: akcióelemek kiemelése (hogyan adjunk hozzá jelölőnégyzeteket)
Az akcióelemeknek vizuális jelzésre van szükségük. Egy `NoteCheckBox` címke minden `RichText` elemhez való csatolásával közvetlenül a vázlatban engedélyezi a **add checkboxes onenote** funkciót.

`NoteCheckBox.createBlueCheckBox()` egy kék jelölt dobozt hoz létre; más színek is elérhetők a márkázáshoz.

```java
richText = outline.appendChildLast(new OutlineElement()).appendChildLast(new RichText());
richText.append("TO DO");
richText.setParagraphStyle(headerStyle);
richText.setSpaceBefore(15);
restartFlag = true;
for (String e: new String[] { "First", "Second", "Third" })
{
    OutlineElement outlineElement = outline.appendChildLast(new OutlineElement());
    outlineElement.setNumberList(createListNumberingStyle(bodyStyle, restartFlag));
    richText = outlineElement.appendChildLast(new RichText());
    richText.append(e);
    richText.setParagraphStyle(bodyStyle);
    richText.getTags().add(NoteCheckBox.createBlueCheckBox());
    restartFlag = false;
}
```

*Pro tip:* Használja a `NoteCheckBox.createBlueCheckBox()`-t egy kék jelölődobozhoz; más színek is elérhetők, ha más vizuális stílusra van szüksége.

## 4. lépés: betűstílus testreszabása OneNote-ban
A megbeszélés jegyzeteinek márkás megjelenéséhez alkalmazza a korábban definiált `ParagraphStyle` objektumokat minden `RichText` elemre.

A `FontName`, `FontSize` és `FontColor` tulajdonságok beállítása biztosítja, hogy a generált oldal megfeleljen a vállalati stílus útmutatónak.

```java
// Save OneNote document
d.save(Paths.get(dataDir, "meetingNotes.one").toString());
```

## 5. lépés: dokumentum mentése
Végül írja a OneNote fájlt a lemezre. A fájl közvetlenül megnyitható a OneNote asztali alkalmazásban, és később szükség esetén PDF‑re is konvertálható.

*Közvetlen válasz:* Hívja a `document.save("MeetingTemplate.one")` metódust – az API egy teljesen kompatibilis OneNote fájlt ír, amely azonnal megnyílik a OneNote kliensben.

## Gyakori problémák és megoldások
| Probléma | Megoldás |
|----------|----------|
| **A jelölőnégyzetek nem jelennek meg** | Győződjön meg arról, hogy a bekezdésstílus beállítása után hívta a `richText.getTags().add(NoteCheckBox.createBlueCheckBox())`-t. |
| **A betűk másként jelennek meg a OneNote-ban** | Ellenőrizze, hogy a betűtípus neve (pl. „Calibri”) telepítve van-e azon a gépen, ahol a OneNote megnyitja a fájlt. |
| **A vázlat nincs behúzva** | Állítsa be a `setVerticalOffset` és `setHorizontalOffset` értékeket az `Outline` objektumon. |
| **A számozás váratlanul újraindul** | Helyesen használja a `restartFlag`-et; állítsa `true`‑ra csak az új szakasz első listájánál. |

## Gyakran ismételt kérdések
### Hogyan adhatok hozzá jelölőnégyzeteket OneNote-hoz?
Töltsön be egy `RichText` elemet, majd hívja a `richText.getTags().add(NoteCheckBox.createBlueCheckBox())` metódust. A címke a sort interaktív jelölőnégyzetté alakítja, amelyet a felhasználók a OneNote-ban bejelölhetnek.

### Testreszabhatom a betűstílusokat a megbeszélés jegyzeteimben?
Igen. Hozzon létre `ParagraphStyle` objektumokat a kívánt `FontName`, `FontSize` és `FontColor` értékekkel, majd rendelje őket minden `RichText` elemhez, ahogyan az az 1. lépésben látható.

### Az Aspose.Note kompatibilis más Java könyvtárakkal?
Az Aspose.Note együtt működik más Aspose termékekkel (PDF, Cells, Slides) és a szabványos Java könyvtárakkal, lehetővé téve műveletek láncolását, például a generált OneNote fájl PDF‑re konvertálását.

### Hogyan adhatok hozzá további szakaszokat a megbeszélés jegyzeteimhez?
Használja újra ugyanazt a mintát: hozzon létre egy új `Outline` csomópontot, alkalmazzon egy `ParagraphStyle`-t, és opcionálisan adjon hozzá jelölőnégyzeteket. Az API teljesen ismételhető tetszőleges számú szakaszhoz.

### Vannak licencelési szempontok az Aspose.Note esetében?
A teljes licencelési részletekért tekintse meg az [Aspose.Note dokumentációt](https://reference.aspose.com/note/java/). Az ingyenes próba elegendő fejlesztéshez; a gyártási környezethez kereskedelmi licenc szükséges.

### Elérhető próba verzió az Aspose.Note-hoz?
Igen, elérheti a **ingyenes Aspose.Note próba letöltési oldalt**: [Aspose.Note próba letöltési oldal](https://releases.aspose.com/).

## GYIK
**Q: Hogyan adhatok hozzá ellenőrzőlistát OneNote-hoz anélkül, hogy jelölőnégyzeteket használnék?**  
A: Létrehozhat egy felsorolást és manuálisan jelölheti meg az elemeket, de a `NoteCheckBox` használata interaktív jelölőnégyzeteket biztosít, amelyek szinkronizálódnak a OneNote felhasználói felületével.

**Q: Használhatom ezt a sablont heti ismétlődő megbeszélés napirend sablon létrehozásához?**  
A: Természetesen. Csak módosítsa a dátumformátumot vagy adjon át egy egyedi címkarakterláncot, hogy ugyanazt a struktúrát minden héten újra felhasználja.

**Q: Mi a legjobb módja a betűstílus testreszabásának OneNote-ban a márkázáshoz?**  
A: Definiáljon `ParagraphStyle` objektumokat a vállalati betűtípus nevével, méretével és színével, majd alkalmazza őket minden `RichText` elemre, ahogyan az az 1. lépésben látható.

**Q: Támogatja az Aspose.Note a vázlat PDF‑be exportálását?**  
A: Igen. A OneNote fájl mentése után betöltheti az Aspose.Note segítségével, és PDF‑be exportálhatja a `Document.save("output.pdf", SaveFormat.Pdf)` metódussal.

**Q: Van mód programozottan bejelölni egy jelölőnégyzetet befejezettként?**  
A: Beállíthatja a jelölőnégyzet állapotát egy `NoteCheckBox` címke hozzáadásával, ahol a `Checked` tulajdonság `true`‑ra van állítva.

---

**Utolsó frissítés:** 2026-10-26  
**Tesztelve a következővel:** Aspose.Note for Java 24.11 (latest at time of writing)  
**Szerző:** Aspose

## Kapcsolódó oktatóanyagok

- [Címkék hozzáadása OneNote-hoz – Címkézett OneNote dokumentum létrehozása Aspose.Note segítségével](/note/java/onenote-tag-operations/)
- [Hogyan testreszabjuk a OneNote stílusokat Aspose.Note for Java segítségével](/note/java/onenote-styles/)
- [OneNote dokumentum létrehozása Java-ban – Aspose Note Java oktatóanyag](/note/java/onenote-document-manipulation/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}