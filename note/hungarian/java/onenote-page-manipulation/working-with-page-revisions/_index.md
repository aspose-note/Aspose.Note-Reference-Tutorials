---
date: 2026-05-25
description: Ismerje meg, hogyan követheti nyomon a OneNote változásait, és kezelheti
  az oldalrevíziókat a OneNote dokumentumokban az Aspose.Note for Java segítségével.
  Tartalmaz egy revízió összefoglaló példát és azt, hogyan módosíthatja a revízió
  dátumát.
keywords:
- track changes onenote
- OneNote page revisions
- Aspose.Note Java
- revision summary example
- modify revision date
linktitle: Munka az oldalrevíziókkal a OneNote-ban – Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-05-25'
  description: Learn how to track changes onenote and manage page revisions in OneNote
    documents using Aspose.Note for Java. Includes a revision summary example and
    how to modify revision date.
  headline: track changes onenote – Manage Page Revisions with Aspose.Note
  type: TechArticle
- questions:
  - answer: It means detecting who edited a OneNote page and when the edit occurred.
    question: What does “track changes onenote” mean?
  - answer: Aspose.Note for Java supplies a full‑featured API for page‑revision handling.
    question: Which library provides this capability?
  - answer: Yes—use the `RevisionSummary` object to set a new author name and modified
      date.
    question: Can I change the author or date of a revision?
  - answer: A sample `.one` file is required; the API works with any OneNote 2010‑2021
      format.
    question: Do I need a OneNote file beforehand?
  - answer: A valid Aspose.Note license must be applied for commercial deployments.
    question: Is a license required for production use?
  type: FAQPage
second_title: Aspose.Note Java API
title: OneNote változások nyomon követése – Oldalrevíziók kezelése az Aspose.Note
  segítségével
url: /hu/java/onenote-page-manipulation/working-with-page-revisions/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote oldalrevíziók kezelése - Aspose.Note

## Bevezetés

Az OneNote egy erőteljes jegyzetkészítő platform, és amikor szükség van a **track changes onenote** funkcióra, az oldalrevíziók kezelése elengedhetetlen a hatékony együttműködéshez. Az Aspose.Note for Java segítségével programozottan leolvashatja, ki szerkesztett egy oldalt, lekérheti az időbélyegeket, sőt módosíthatja is azokat. Ez a bemutató végigvezet a dokumentum betöltésén, a revízióösszegzés kinyerésén, és a szerző vagy dátum információk frissítésén – mindezt anélkül, hogy manuálisan megnyitná a OneNote‑ot.

## Gyors válaszok
- **Mi jelent a “track changes onenote”?** Azt jelenti, hogy felismeri, ki szerkesztett egy OneNote oldalt és mikor történt a szerkesztés.  
- **Melyik könyvtár biztosítja ezt a képességet?** Az Aspose.Note for Java teljes körű API‑t kínál az oldalrevíziók kezeléséhez.  
- **Módosíthatom a revízió szerzőjét vagy dátumát?** Igen – használja a `RevisionSummary` objektumot egy új szerzőnév és módosított dátum beállításához.  
- **Szükségem van előre egy OneNote fájlra?** Egy `.one` mintafájl szükséges; az API bármely OneNote 2010‑2021 formátummal működik.  
- **Szükséges licenc a termelésben való használathoz?** Egy érvényes Aspose.Note licencet kell alkalmazni a kereskedelmi telepítésekhez.

## Mi a revízióösszegzés példája?

A *revision summary* egy könnyű metaadatblokk, amely tárolja a legutóbbi szerkesztő nevét, a pontos módosítási időt, és néhány további jelzőt. Lehetővé teszi, hogy megjelenítse a „last edited by John Doe on 2026‑04‑30 10:15 AM” szöveget anélkül, hogy az egész oldal tartalmát elemezné. Általában tartalmazza a szerkesztő megjelenített nevét, a változás pontos UTC időpontját, és egy egyedi revízióazonosítót, amely szinkronizáláshoz használható.

## Miért használjunk track changes onenote‑t az Aspose.Note‑dal?

Az Aspose.Note használata a változások nyomon követésére programozott módot biztosít a revízióadatok kinyerésére manuális ellenőrzés nélkül, lehetővé téve az automatizált jelentéstételt, megfelelőségi ellenőrzéseket és a CI csővezetékekbe való integrációt. Az API gyors, memóriahatékony hozzáférést nyújt a revízió metaadataihoz nagy jegyzetfüzetek esetén, és támogatja a tömeges feldolgozást több ezer oldalra.

## Előfeltételek

### Java fejlesztői környezet
Telepítse a JDK 17-et vagy újabbat, és állítsa be IDE‑jét (IntelliJ IDEA, Eclipse vagy VS Code) Java fejlesztéshez.

### Aspose.Note for Java könyvtár
Letöltse a legújabb Aspose.Note for Java csomagot [innen](https://releases.aspose.com/note/java/). Adja hozzá a JAR‑t a projekt osztályútvonalához.

### OneNote dokumentum
Készítsen egy `.one` fájlt, amely legalább egy olyan oldalt tartalmaz, amelyet meg szeretne vizsgálni vagy módosítani.

## Csomagok importálása

`Document` osztály egy OneNote fájlt képvisel, a `Page` egy egyedi oldalt, és a `RevisionSummary` metaadatokat biztosít a legújabb változásokról.

```java
import com.aspose.note.*;
import java.util.Date;
```

## Hogyan töltök be egy OneNote dokumentumot és érhetem el az első oldalt?

Az OneNote fájl betöltéséhez hozza létre a `Document` példányt a .one fájl elérési útjával. A `Document` objektum a fájl struktúráját elemzi UI megjelenítés nélkül. Ezután az első oldalt a `getPages().get_Item(0)` hívással kérheti le, amely egy `Page` objektumot ad vissza, amely az oldal tartalmát és metaadatait képviseli. Ez a megközelítés alacsony memóriahasználatot biztosít.

```java
Document oneNoteDoc = new Document("sample.one");
Page firstPage = oneNoteDoc.getPages().get_Item(0);
```

## Hogyan olvashatom el az oldal revízióösszegzését?

A revízió metaadataihoz a `Page` példányon a `getRevisionSummary()` hívással férhet hozzá. A visszaadott `RevisionSummary` objektum olyan mezőket tartalmaz, mint a szerző neve, az utolsó módosítás időbélyege és a revízióazonosító. Ezeket az értékeket a `getAuthor()`, `getLastModifiedTime()` és `getRevisionId()` metódusokkal olvashatja ki, hogy megjelenítse vagy naplózza a legújabb szerkesztési információkat.

```java
RevisionSummary revSummary = firstPage.getRevisionSummary();
System.out.println("Author: " + revSummary.getAuthor());
System.out.println("Last Modified: " + revSummary.getLastModifiedTime());
```

## Hogyan frissíthetem a revízióösszegzést új szerzővel és dátummal?

Hozzon létre vagy szerezze meg a meglévő `RevisionSummary` objektumot az oldalról, és módosítsa annak tulajdonságait. Használja a `setAuthor(String)` metódust egy új szerzőnév hozzárendeléséhez, és a `setLastModifiedTime(Date)`‑t a kívánt időbélyeg (UTC) beállításához. A módosítások után hívja meg a `document.save()`‑t, hogy az frissített revízióadatok visszaíródjanak a .one fájlba.

```java
revSummary.setAuthor("Jane Smith");
revSummary.setLastModifiedTime(new Date()); // sets to current time
oneNoteDoc.save("updated.one");
```

## Gyakori buktatók és tippek

- **Ne felejtse el meghívni a `save()`‑t** a `RevisionSummary` módosítása után; különben a változások csak a memóriában maradnak.  
- **Az időzónák fontosak:** a `Date` objektumok UTC‑ben tárolódnak. Konvertálja a helyi időket UTC‑re, ha következetes, régióközi jelentésre van szükség.  
- **Nagy jegyzetfüzetek:** 200 oldalnál nagyobb jegyzetfüzetek feldolgozásakor iteráljon az oldalakat kötegekben, hogy a memóriahasználat 100 MB alatt maradjon.

## Gyakran feltett kérdések

**Q:** *Használhatom az Aspose.Note for Java‑t más Java könyvtárakkal együtt?*  
**A:** Igen. Az API tiszta Java, és zökkenőmentesen működik olyan könyvtárakkal, mint az Apache POI, Jackson vagy Spring Boot.

**Q:** *Támogatja az Aspose.Note a régebbi OneNote fájlformátumokat?*  
**A:** Támogatja az összes OneNote formátumot 2007‑től kezdődően, több mint 30 év verziótörténetet lefedve.

**Q:** *Alkalmas-e az Aspose.Note vállalati méretű alkalmazásokra?*  
**A:** Teljes mértékben. Kezeli a több gigabájtos jegyzetfüzeteket, szálbiztos műveleteket kínál, és korlátlan termelési telepítéshez licencelt.

**Q:** *Testreszabhatom a revízió metaadatait a szerzőn és a dátumon túl?*  
**A:** A `RevisionSummary` további mezőket is elérhetővé tesz, például `RevisionId` és `IsDeleted`; ezeket igény szerint olvashatja vagy beállíthatja.

**Q:** *Hol kaphatok segítséget, ha problémába ütközöm?*  
**A:** Tegyen fel kérdéseket a hivatalos [Aspose.Note fórumon](https://forum.aspose.com/c/note/28), ahol az Aspose mérnökök és a közösség tagjai nyújtanak segítséget.

## Következtetés

Az Aspose.Note for Java használatával teljes mértékben **track changes onenote** funkciót valósíthat meg, kinyerheti a revízió részleteket, és programozottan módosíthatja a szerzőneveket vagy időbélyegeket. Ez a képesség egyszerűsíti az együttműködést, megfelel az auditkövetelményeknek, és lehetővé teszi az automatizált migrációs vagy takarító szkriptek használatát nagy OneNote tárolókhoz.

---

**Utoljára frissítve:** 2026-05-25  
**Tesztelve a következővel:** Aspose.Note for Java 24.12  
**Szerző:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
pageRevisionInfo.setAuthorMostRecent("New Author");
Calendar modifiedDate = Calendar.getInstance();
pageRevisionInfo.setLastModifiedTime(modifiedDate.getTime());
document.save(dataDir + "WorkingWithPageRevisions_out.one");
```

## Kapcsolódó bemutatók

- [aspose.note oldalrevíziók bemutató – Oldalrevíziók lekérése OneNote‑ban](/note/java/onenote-page-manipulation/get-page-revisions/)
- [Hogyan módosítsuk a OneNote oldal történetét az Aspose.Note‑val](/note/java/onenote-page-manipulation/modify-page-history/)
- [OneNote oldalszám lekérése Aspose.Note for Java‑val](/note/java/onenote-page-manipulation/get-page-count/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

```java
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.RevisionSummary;
import java.io.IOException;
import java.util.Calendar;
```

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
Page page = document.getFirstChild();
```

```java
RevisionSummary pageRevisionInfo = page.getPageContentRevisionSummary();
System.out.println(String.format("Author:\t%s\nModified:\t%s",
        pageRevisionInfo.getAuthorMostRecent(),
        pageRevisionInfo.getLastModifiedTime().toString()));
```