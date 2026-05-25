---
date: 2026-05-25
description: Tanulja meg, hogyan állíthatja vissza a korábbi OneNote verziót, és hogyan
  vonhatja vissza a OneNote oldalakat az Aspose.Note for Java használatával. Kövesse
  ezt a lépésről‑lépésre útmutatót a hatékony dokumentumkezeléshez.
keywords:
- restore previous onenote version
- how to roll back onenote
- read .one file java
- recover previous onenote page
linktitle: Hogyan állítsuk vissza a korábbi OneNote verziót – Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-05-25'
  description: Learn how to restore previous OneNote version and roll back OneNote
    pages using Aspose.Note for Java. Follow this step‑by‑step guide for efficient
    document management.
  headline: How to Restore Previous OneNote Version – Aspose.Note
  type: TechArticle
- description: Learn how to restore previous OneNote version and roll back OneNote
    pages using Aspose.Note for Java. Follow this step‑by‑step guide for efficient
    document management.
  name: How to Restore Previous OneNote Version – Aspose.Note
  steps:
  - name: '**Install Java Development Kit (JDK):** Grab the latest JDK from the Oracle
      website or your preferred package manager.'
    text: '**Install Java Development Kit (JDK):** Grab the latest JDK from the Oracle
      website or your preferred package manager.'
  - name: '**Configure Environment Variables:** Set `JAVA_HOME` and update `PATH`
      so the `java` and `javac` commands are reachable from the command line.'
    text: '**Configure Environment Variables:** Set `JAVA_HOME` and update `PATH`
      so the `java` and `javac` commands are reachable from the command line.'
  - name: '**Add Aspose.Note for Java:** Download the library from the [website](https://purchase.aspose.com/buy)
      and add the JAR to your project''s classpath.'
    text: '**Add Aspose.Note for Java:** Download the library from the [website](https://purchase.aspose.com/buy)
      and add the JAR to your project''s classpath.'
  type: HowTo
- questions:
  - answer: Restoring a page to a prior version saved in its history.
    question: What does “roll back” mean for OneNote?
  - answer: '`PageHistory` class in Aspose.Note for Java.'
    question: Which API handles the rollback?
  - answer: A valid Aspose.Note license is required for production use.
    question: Do I need a license?
  - answer: Yes – you can pick any entry from the page’s history list.
    question: Can I choose any previous version?
  - answer: Absolutely; the operation works on individual pages without loading the
      entire notebook into memory.
    question: Is this approach safe for large notebooks?
  type: FAQPage
second_title: Aspose.Note Java API
title: Hogyan állítsuk vissza a korábbi OneNote verziót – Aspose.Note
url: /hu/java/onenote-page-manipulation/roll-back-to-previous-page-version/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote korábbi verziójának visszaállítása – Aspose.Note

## Bevezetés

Ha megbízható, programozott módra van szükséged a **korábbi OneNote verzió visszaállításához**, amikor egy véletlen szerkesztés csúszik be, jó helyen vagy. Ebben az útmutatóban végigvezetünk az Aspose.Note for Java használatán, és pontosan megmutatjuk, hogyan lehet egy OneNote oldalt egy korábbi állapotra visszaállítani. Akár automatizált jegyzetkezelő szolgáltatást építesz, akár biztonsági hálót adsz a közös jegyzetfüzetekhez, az oldal visszaállításának képessége biztosítja, hogy a tartalom pontos, megbízható és auditálásra kész legyen.

## Gyors válaszok
- **Mi jelent a „visszagörgetés” a OneNote-ban?** Egy oldal visszaállítása egy korábbi, a történetben mentett verzióra.  
- **Melyik API kezeli a visszagörgetést?** A `PageHistory` osztály az Aspose.Note for Java-ban.  
- **Szükségem van licencre?** Egy érvényes Aspose.Note licenc szükséges a termelési használathoz.  
- **Kiválaszthatok bármely korábbi verziót?** Igen – bármely bejegyzést kiválaszthatod az oldal történeti listájából.  
- **Biztonságos ez a megközelítés nagy jegyzetfüzetek esetén?** Teljesen; a művelet egyedi oldalakon működik, anélkül, hogy a teljes jegyzetfüzetet betöltené a memóriába.

## Mi a „korábbi OneNote verzió visszaállítása”?
**`restore previous onenote version`** arra a folyamatra utal, amely egy OneNote oldal korábbi pillanatfelvételét hívja elő a belső verziótörténetből, és a jelenlegi oldal tartalmát ezzel a pillanatfelvételekkel helyettesíti. Ez a művelet teljes mértékben támogatott az Aspose.Note `PageHistory` API-jával, és nem igényel manuális visszavonási lépéseket.

## Miért használjuk az Aspose.Note-ot a OneNote oldalak visszagörgetéséhez?
Az Aspose.Note képes a jegyzetfüzeteket **ezrek oldalával** feldolgozni, miközben a memóriahasználat **50 MB** alatt marad, mivel oldalanként dolgozik. Támogat **30+ OneNote‑specifikus funkciót**, beleértve a `.one` fájlok olvasását, metaadatok kinyerését és bármely történeti bejegyzés visszaállítását. Ez ideálissá teszi vállalati szintű automatizáláshoz, ahol a megbízhatóság és a teljesítmény kritikus.

## Előfeltételek

Mielőtt a kódba merülnénk, győződj meg róla, hogy a következők készen állnak:

### Java fejlesztői környezet beállítása
1. **Telepítsd a Java Development Kit-et (JDK):** Szerezd be a legújabb JDK-t az Oracle weboldaláról vagy a kedvenc csomagkezelődből.  
2. **Állítsd be a környezeti változókat:** Állítsd be a `JAVA_HOME`-t és frissítsd a `PATH`-t, hogy a `java` és `javac` parancsok elérhetők legyenek a parancssorból.  
3. **Add Aspose.Note for Java:** Töltsd le a könyvtárat a [website](https://purchase.aspose.com/buy) oldalról, és add hozzá a JAR-t a projekted osztályútvonalához.

## Csomagok importálása

A OneNote fájlokkal való interakcióhoz importáld a szükséges Aspose.Note osztályokat:

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## Hogyan állíthatom vissza egy korábbi OneNote oldal verzióját?

Töltsd be a céljegyzetfüzetet, szerezd be a kívánt történeti bejegyzést a `PageHistory` segítségével, távolítsd el a jelenlegi oldalt, és fűzd vissza a kiválasztott verziót a dokumentumba – mindezt tíz Java sor alatt. Ez a megközelítés garantálja, hogy csak a konkrét oldal érintett, a jegyzetfüzet többi része érintetlen marad, és a memóriahasználat minimális.

## 1. lépés: OneNote dokumentum betöltése

`Document` az Aspose.Note legfelső szintű objektuma, amely egyetlen OneNote fájlt reprezentál a memóriában. Először a `.one` fájlt tartalmazó mappára mutatunk, és betöltjük egy `Document` példányba.

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
```
Először a `.one` fájlt tartalmazó mappára mutatunk, és betöltjük egy `Document` objektumba.

## 2. lépés: Oldaltörténet lekérése

`PageHistory` hozzáférést biztosít a kiválasztott oldal minden mentett verziójához, lehetővé téve a **korábbi OneNote verzió visszaállítása** képességet. A `getHistory()` hívásával egy listát kapsz, amelyet közvetlenül iterálhatsz vagy indexelhetsz.

```java
Page page = document.getFirstChild();
PageHistory pageHistory = document.getPageHistory(page);
```
`PageHistory` hozzáférést biztosít a kiválasztott oldal minden mentett verziójához, lehetővé téve a **korábbi OneNote verzió visszaállítása** képességet.

## 3. lépés: Jelenlegi oldal eltávolítása

`Page` egy egyedi oldalt képvisel egy OneNote jegyzetfüzetben. A jelenlegi oldal eltávolítása helyet teremt a visszahozni kívánt történeti verzió számára.

```java
document.removeChild(page);
```
A jelenlegi oldal eltávolításával helyet teremtünk a visszahozni kívánt verzió számára.

## 4. lépés: Korábbi oldalverzió hozzáfűzése

`appendChildLast` egy csomópontot ad a dokumentum gyermekgyűjteményének végéhez. Itt a legújabb történeti bejegyzést választjuk ki (az indexet módosíthatod, hogy bármely régebbi verziót célozz meg), és visszaadjuk a dokumentumba.

```java
document.appendChildLast(pageHistory.get_Item(pageHistory.size() - 1));
```
Itt a legújabb történeti bejegyzést választjuk ki (az indexet módosíthatod, hogy bármely régebbi verziót célozz meg), és visszaadjuk a dokumentumba.

## 5. lépés: Dokumentum mentése

A mentés visszaírja a módosított jegyzetfüzetet a lemezre, egy olyan fájlt hozva létre, amely most már tartalmazza a visszagörgetett oldalt. A művelet csak a módosított oldalt írja, így a nagy jegyzetfüzetek is gyorsan feldolgozhatók.

```java
document.save(dataDir + "RollBackToPreviousPageVersion_out.one");
```
Végül, tárold a módosított jegyzetfüzetet. A kimeneti fájl most már tartalmazza a visszagörgetett oldalt.

## Gyakori problémák és tippek
- **Üres történelem:** Ha a `pageHistory.size()` 0-t ad vissza, az oldalnak nincs mentett verziója – győződj meg róla, hogy a verziókövetés engedélyezve van a OneNote-ban.  
- **Index határon kívül:** Ne feledd, hogy a történelem lista nulláról indul. Állítsd be az indexet (`size() - 1`), hogy a szükséges pontos verziót célozd.  
- **Teljesítmény:** Egyetlen oldallal dolgozni elkerüli a teljes jegyzetfüzet memóriába töltését, így a művelet gyors marad még **10 000+ oldalas** jegyzetfüzetek esetén is.  
- **.one fájlok olvasása Java-ban:** Használd a `Document.load("path/to/file.one")` parancsot egy OneNote fájl beolvasásához; az Aspose.Note teljes mértékben támogatja a `.one` formátumot anélkül, hogy a Microsoft Office telepítve lenne.  
- **Korábbi OneNote oldal biztonságos visszaállítása:** Mindig készíts biztonsági másolatot az eredeti `.one` fájlról, mielőtt kötegelt visszagörgetéseket hajtasz végre, különösen sok jegyzetfüzet automatizálása esetén.

## Gyakran ismételt kérdések

**Q1: Visszagörgethetek több verziót egy oldalból?**  
A: Igen, hozzáférhetsz az egész oldal történetéhez, és bármely korábbi verziót visszaállíthatsz a megfelelő index kiválasztásával a `PageHistory` listából.

**Q2: Támogatja az Aspose.Note más programozási nyelveket is a Java mellett?**  
A: Igen, az Aspose.Note könyvtárakat biztosít .NET, C++ és Python számára is, lehetővé téve ugyanazoknak a visszagörgetési műveleteknek a végrehajtását különböző platformokon.

**Q3: Kompatibilis az Aspose.Note minden OneNote verzióval?**  
A: Az Aspose.Note támogatja az összes főbb OneNote fájlformátumot, beleértve a régi `.one` fájlokat és az újabb OneNote 2016/365 struktúrákat, biztosítva a széles körű kompatibilitást.

**Q4: Automatizálhatok más feladatokat is a OneNote-ban az Aspose.Note segítségével?**  
A: Teljesen. Az API lehetővé teszi, hogy programozottan hozzáadj, törölj és módosíts szekciókat, oldalakat és beágyazott erőforrásokat, így ideális tömeges migrációkhoz és egyedi jelentésekhez.

**Q5: Van közösségi fórum vagy támogatás az Aspose.Note-hoz?**  
A: Igen, meglátogathatod a [Aspose.Note fórumot](https://forum.aspose.com/c/note/28) a közösségi segítségért, vagy felveheted a kapcsolatot az Aspose dedikált támogatási csapatával kereskedelmi segítségért.

---

**Last Updated:** 2026-05-25  
**Tested With:** Aspose.Note for Java (latest release)  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Kapcsolódó útmutatók

- [Hogyan mentse a OneNote oldal verzióját – Aktuális oldal verziójának feltöltése a OneNote-ban - Aspose.Note](/note/java/onenote-page-manipulation/push-current-page-version/)
- [Aspose Java útmutató – Információk lekérése a OneNote oldalakról - Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)
- [OneNote oldal számának lekérése Aspose.Note for Java segítségével](/note/java/onenote-page-manipulation/get-page-count/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}