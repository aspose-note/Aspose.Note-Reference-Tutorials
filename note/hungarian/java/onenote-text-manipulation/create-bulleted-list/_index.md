---
date: 2026-03-03
description: Tanulja meg, hogyan hozhat létre felsorolásos listát a OneNote-ban az
  Aspose.Note for Java segítségével, és hogyan mentheti el a OneNote dokumentumot
  PDF formátumban. Lépésről‑lépésre útmutató Java felsorolásokkal.
linktitle: Create Bulleted List OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Felsoroláslista létrehozása OneNote – Aspose.Note
url: /hu/java/onenote-text-manipulation/create-bulleted-list/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Pontozott lista létrehozása OneNote-ban – Aspose.Note

## Bevezetés
Ha programozott módon **pontozott listát szeretne létrehozni OneNote-ban**, az Aspose.Note for Java egy tiszta, folyékony API-t biztosít, amely a OneNote belső működését Ön helyett kezeli. Ebben az útmutatóban lépésről lépésre bemutatjuk, hogyan állíthat be felsorolásjeleket Java-ban, hogyan adhatja hozzá őket egy vázlathoz, és végül **mentse a OneNote dokumentumot PDF‑ként**. A végére egy használatra kész kódrészletet kap, amelyet bármely Java projektbe beilleszthet.

## Gyors válaszok
- **Mit csinál az Aspose.Note?** Lehetővé teszi OneNote fájlok létrehozását, szerkesztését és konvertálását OneNote telepítése nélkül.  
- **Beállíthatok felsorolásjeleket Java‑val?** Igen – használja a `NumberList`‑et a felsorolás stílusának meghatározásához.  
- **Hogyan exportálok PDF‑be?** Hívja a `doc.save(...".pdf")`‑t az oldal felépítése után.  
- **Szükségem van licencre a fejlesztéshez?** Egy ingyenes próba verzió teszteléshez elegendő; a termeléshez licenc szükséges.  
- **Mely IDE-k támogatottak?** Bármely Java IDE, például Eclipse, IntelliJ IDEA vagy VS Code.

## Mi az a „pontozott lista létrehozása OneNote-ban”?
A pontozott lista létrehozása OneNote-ban azt jelenti, hogy egy sor vázlelemhez hozzáadunk egy felsorolásjelet (pl. „*”). Ez a struktúra javítja az olvashatóságot és hasonló módon működik, mint amikor a felhasználók manuálisan adnak hozzá listákat a OneNote felületén.

## Miért használjuk az Aspose.Note for Java‑t a felsorolásjelek beállításához?
- **OneNote telepítése nélkül** – szervereken és CI pipeline‑okban is működik.  
- **Teljes stílusvezérlés** – a betűtípus, méret, szín és a felsorolásjel is konfigurálható.  
- **Közvetlen PDF export** – egy sorban generálhat PDF‑et, ami tökéletes jelentéshez vagy archiváláshoz.  

## Előfeltételek
- Alapvető Java programozási ismeretek.  
- Az Aspose.Note for Java könyvtár telepítve – töltse le a [Aspose.Note for Java Documentation](https://reference.aspose.com/note/java/) oldalról.  
- Java IDE (Eclipse, IntelliJ IDEA stb.) telepítve a gépén.

## Csomagok importálása
Kezdje a szükséges csomagok importálásával a Java projektjébe. Ez hozzáférést biztosít az összes, a továbbiakban használandó Aspose.Note osztályhoz.

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NumberList;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.ParagraphStyle;
// Import Aspose.Note for Java packages
```

## 1. lépés: Dokumentum és oldal inicializálása
Hozzon létre egy `Document` példányt és egy `Page`‑t, ahol a vázlat elhelyezkedik.

```java
String dataDir = "Your Document Directory";
// create an object of the Document class
Document doc = new Document();
// initialize Page class object
Page page = new Page();
```

## 2. lépés: Outline és TextStyle inicializálása (bullet points beállítása Java-ban)
Létrehozzuk az `Outline` konténert és definiálunk egy alapértelmezett `ParagraphStyle`‑t. Itt állítjuk be a **bullet points java**‑stílusú formázást.

```java
// initialize Outline class object
Outline outline = new Outline();
// initialize TextStyle class object and set formatting properties
ParagraphStyle defaultStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```

## 3. lépés: Pontozott listaelemek létrehozása
Hozzon létre egyedi `OutlineElement` objektumokat, csatoljon egy `NumberList`‑et, amely meghatározza a felsorolásjelet, és adja hozzá a szöveget.

```java
// initialize OutlineElement class objects and apply bullets
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("*", "Arial", 10));
// initialize RichText class object and apply text style
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
```

*Ismételje meg a fenti blokkot minden további felsoroláshoz, amelyre szüksége van (pl. `outlineElem2`, `outlineElem3`).*

## 4. lépés: Outline elemek hozzáadása az Outline‑hoz
Gyűjtse össze az összes felsorolás elemet a szülő `Outline`‑ba.

```java
// add outline elements
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```

## 5. lépés: Outline hozzáadása az oldalhoz és mentés (OneNote dokumentum mentése PDF‑ként)
Csatolja az `Outline`‑t a `Page`‑hez, adja hozzá az oldalt a `Document`‑hoz, és végül **mentse a OneNote dokumentumot PDF‑ként**.

```java
// add Outline node
page.appendChildLast(outline);
// add Page node
doc.appendChildLast(page);
// save the document
doc.save(dataDir + "CreateBulletedList_out.pdf");
```

Gratulálunk! Most már programozott módon **pontozott listát hozott létre OneNote-ban** és PDF‑be exportálta az Aspose.Note for Java segítségével.

## Gyakori problémák és megoldások
| Probléma | Megoldás |
|----------|----------|
| `outlineElem2` vagy `outlineElem3` nincs definiálva | Győződjön meg arról, hogy a 3. lépésből származó kódrészletet megismétli minden további felsoroláshoz, és a változókat ennek megfelelően átnevezi. |
| PDF fájl nem jött létre | Ellenőrizze, hogy a `dataDir` egy írható mappára mutat-e, és rendelkezik-e írási jogosultsággal. |
| A felsorolás stílusa másként jelenik meg | Állítsa be a `NumberList` konstruktor paramétereit (betűtípus, méret vagy karakter) a kívánt megjelenéshez. |

## Gyakran ismételt kérdések

**Q: Az Aspose.Note for Java kompatibilis minden Java IDE‑val?**  
A: Igen, működik Eclipse, IntelliJ IDEA, NetBeans és bármely, a szabványos Java projekteket támogató IDE‑val.

**Q: Testreszabhatom a pontozott lista formázását?**  
A: Természetesen! A betűtípust, színt, méretet, sőt egyedi Unicode szimbólumokat is használhat a `NumberList` paramétereinek módosításával.

**Q: Hol találok további támogatást az Aspose.Note for Java‑hoz?**  
A: Látogassa meg a [Aspose.Note for Java support forum](https://forum.aspose.com/c/note/28) oldalt a közösségi segítségért és a hivatalos támogatásért.

**Q: Van ingyenes próba verzió az Aspose.Note for Java‑hoz?**  
A: Igen, egy ingyenes próba verziót [itt](https://releases.aspose.com/) tekinthet meg.

**Q: Hogyan szerezhetek ideiglenes licencet az Aspose.Note for Java‑hoz?**  
A: Ideiglenes licencet [itt](https://purchase.aspose.com/temporary-license/) kaphat.

## Összegzés
Az Aspose.Note for Java egyszerűvé teszi a **pontozott lista létrehozását OneNote-ban**, minden felsorolás stílusának beállítását, és a **OneNote dokumentum PDF‑ként való mentését** néhány rövid lépésben. Nyugodtan kísérletezzen különböző felsorolásjelekkel, betűtípusokkal és színekkel, hogy illeszkedjenek az alkalmazás tervezési nyelvéhez. Fedezze fel az Aspose.Note további funkcióit, például táblázatokat, képeket és hiperhivatkozásokat, hogy gazdagabb OneNote tartalmat építsen.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-03-03  
**Tested With:** Aspose.Note for Java 24.11  
**Author:** Aspose