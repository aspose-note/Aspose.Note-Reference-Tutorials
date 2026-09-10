---
date: 2026-07-05
description: Tanulja meg, hogyan konvertálja a OneNote-ot PDF-be, és hogyan kezelje
  a mérő licencet Java-ban az Aspose.Note használatával. Ellenőrizze a használatot,
  figyelje a krediteket, és tartsa alacsonyan a költségeket.
keywords:
- convert onenote to pdf
- how to convert onenote
- convert notebook to pdf
linktitle: Mérő licenc kezelése a OneNote-hoz Java-ban
schemas:
- author: Aspose
  dateModified: '2026-07-05'
  description: Learn how to convert OneNote to PDF and manage a metered license in
    Java using Aspose.Note. Control usage, monitor credits, and keep costs low.
  headline: Convert OneNote to PDF and Manage Metered License in Java
  type: TechArticle
- description: Learn how to convert OneNote to PDF and manage a metered license in
    Java using Aspose.Note. Control usage, monitor credits, and keep costs low.
  name: Convert OneNote to PDF and Manage Metered License in Java
  steps:
  - name: Set Up the Metered License
    text: The `Metered` class activates metered‑license mode for all subsequent Aspose.Note
      operations. You must provide the public and private keys you received from your
      Aspose account. Here we create a `Metered` object and inject the public/private
      keys you received from Aspose. This step activates the met
  - name: Load the OneNote Document and Convert to PDF
    text: 'The `Document` class represents a OneNote notebook in memory. After instantiation,
      you can call `save` with a `.pdf` extension to trigger the conversion. SaveFormat
      is an enumeration that specifies the output format for the document, such as
      PDF. - **Load**: `Document` reads the `.one` file located '
  - name: Check Credit Consumption Before and After Conversion
    text: The `Metered` class also provides methods to query credit usage. These two
      lines print the remaining credit balance and the amount of credit used by the
      conversion. Metered.getConsumptionCredit() returns the remaining credit balance,
      while Metered.getConsumptionQuantity() returns the credits used by
  type: HowTo
- questions:
  - answer: A metered license lets you pay for API usage based on credits, giving
      you fine‑grained cost control.
    question: What is a metered license?
  - answer: Purchase a license from the Aspose website or request a temporary evaluation
      key via your account dashboard.
    question: How do I obtain a metered key for Aspose products?
  - answer: Yes, but all consumption is aggregated under the same key, so monitor
      total usage carefully.
    question: Can I use a metered license across multiple applications?
  - answer: Yes, you can download a free trial from [here](https://releases.aspose.com/).
    question: Is there a free trial for Aspose.Note for Java?
  - answer: Ask questions on the Aspose community forums [here](https://forum.aspose.com/c/note/28).
    question: Where can I get support for Aspose.Note for Java?
  type: FAQPage
second_title: Aspose.Note Java API
title: Konvertálja a OneNote-ot PDF-be, és kezelje a mérő licencet Java-ban
url: /hu/java/licensing-java/manage-metered-license/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote konvertálása PDF-re és a mérő licenc kezelése Java-ban

## Bevezetés

Ebben az útmutatóban megtudja, hogyan **konvertálja a OneNote-ot PDF-re** a metered licenc használatával az Aspose.Note for Java könyvtár segítségével. A mérő licenc lehetővé teszi a kreditfogyasztás valós időben történő nyomon követését, így csak azt fizeti, amit ténylegesen használ. Végigvezetjük a teljes folyamaton – a licenckulcsok beállításától a OneNote fájl betöltéséig, a PDF-re konvertálásig, és a kreditfelhasználás ellenőrzéséig.

## Gyors válaszok
- **Mi jelent a “convert OneNote to PDF”?** Átalakít egy `.one` jegyzetfüzet fájlt hordozható PDF dokumentummá, amely megőrzi a elrendezést, betűtípusokat és képeket.  
- **Melyik könyvtár végzi a konverziót?** Az Aspose.Note for Java egyszerű, nagy teljesítményű API-t biztosít ehhez a feladathoz.  
- **Szükségem van licencre a konvertáláshoz?** Igen, a metered licenc szükséges a termeléshez és a pontos kreditkövetéshez.  
- **Hogyan tudom nyomon követni a használatot?** Hívja a `Metered.getConsumptionCredit()` és `Metered.getConsumptionQuantity()` metódusokat a konverzió előtt és után.  
- **Szükséges-e további beállítás?** Csak egy Java JDK és az Aspose.Note JAR fájl; a Maven vagy Gradle is kezelheti a függőséget.

## Mi a “convert OneNote to PDF”?

**Közvetlen válasz:** A OneNote PDF-re konvertálása beolvassa a `.one` jegyzetfüzetet, minden oldalt egy rögzített elrendezésű PDF oldalra laposít, és az eredményt egy `.pdf` fájlba írja, amely bármely eszközön megnyitható OneNote nélkül. Ez a konverzió megőrzi a szövegformázást, beágyazott képeket, táblázatokat és vektorgrafikákat, így a PDF ideális megosztásra, nyomtatásra vagy archiválásra.

A konverziós folyamat teljesen a szerver oldalon történik, így nincs szükség kliensoldali renderelésre vagy harmadik féltől származó szoftverre.

## Miért használjunk mérő licencet ehhez a konverzióhoz?

**Közvetlen válasz:** A mérő licenc kreditenként számláz, lehetővé téve a használat fel- vagy lecsökkentését fix előfizetési díj nélkül. Másodpercenként jelentést készít a használatról, havonta akár 10 000 kreditet támogat kulcsonként, és automatikusan letiltja az API-t, ha a kreditek elfogynak, megakadályozva a váratlan többletköltségeket. Ez a modell tökéletes időszakos terhelésekhez vagy proof‑of‑concept projektekhez, ahol szigorú költségkontrollra van szükség.

## Előfeltételek

Mielőtt elkezdenénk, győződjön meg róla, hogy rendelkezik a következőkkel:

1. **Java Development Kit (JDK)** – bármely friss verzió (JDK 11+ ajánlott). Töltse le [innen](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.Note for Java library** – szerezze be a legújabb JAR-t a [hivatalos weboldalról](https://releases.aspose.com/note/java/).  

> **Pro tipp:** Adja hozzá az Aspose.Note JAR-t a projekt osztályútvonalához, vagy használjon építőeszközt, például Maven/Gradle-t a függőség kezeléséhez. Maven felhasználók a következő függőséget adhatják hozzá (cserélje le a `VERSION`-t a legújabbra):  

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-note</artifactId>
    <version>VERSION</version>
</dependency>
```

## Csomagok importálása

Az importálási utasítások az Aspose.Note osztályokat hozzák be a Java projektbe, így hozzáférhet a licenceléshez, dokumentumkezeléshez és konverziós API-khoz.

Először importálja a szükséges osztályokat. Tartsa ezt a blokkot pontosan úgy, ahogy látható – a kódban ne legyen változtatás.

```java
import com.aspose.note.Document;
import com.aspose.note.Metered;



import java.nio.file.Paths;
```

## Hogyan konvertáljuk a OneNote-ot PDF-re Java-ban?

**Közvetlen válasz:** Töltse be a OneNote fájlt a `new Document("input.one")` paranccsal, majd hívja a `document.save("output.pdf", SaveFormat.Pdf)` metódust. Ez a két soros szekvencia elvégzi a teljes konverziót, automatikusan megőrizve az oldalelrendezést, betűtípusokat és képeket. Mentés után lekérdezheti a mérő licencet, hogy hány kreditet fogyasztott a művelet.

### 1. lépés: A mérő licenc beállítása

A `Metered` osztály aktiválja a mérő licenc módot minden későbbi Aspose.Note művelethez. Meg kell adnia a nyilvános és privát kulcsokat, amelyeket az Aspose fiókjából kapott.

```java
Metered metered = new Metered();
metered.setMeteredKey("MyPublicKey", "MyPrivateKey");
```

Itt létrehozunk egy `Metered` objektumot, és beadjuk a nyilvános/privát kulcsokat, amelyeket az Aspose-tól kaptunk. Ez a lépés aktiválja a mérő licenc módot minden későbbi művelethez, beleértve a **convert OneNote to PDF** hívást.

### 2. lépés: A OneNote dokumentum betöltése és PDF-re konvertálása

A `Document` osztály egy OneNote jegyzetfüzetet ábrázol a memóriában. Létrehozás után meghívhatja a `save` metódust `.pdf` kiterjesztéssel a konverzió elindításához.

A SaveFormat egy felsorolás, amely meghatározza a dokumentum kimeneti formátumát, például PDF.

```java
String dataDir = "Your Document Directory";
Document doc = new Document(Paths.get(dataDir,"Sample1.one").toString());
doc.save(Paths.get(dataDir,"MeteredLicense.pdf").toString());
```

- **Betöltés**: A `Document` beolvassa a `dataDir`-ben található `.one` fájlt. Ez a klasszikus mód a **OneNote dokumentum betöltésére** a feldolgozáshoz.  
- **Konvertálás és mentés**: A `save` `.pdf` kiterjesztéssel automatikusan **convert .one to .pdf**. A művelet **PDF-et ment OneNote-ból** ugyanabban a mappában. Cserélje le a `"Your Document Directory"`-t a gépén lévő tényleges útvonalra.

### 3. lépés: Kreditfogyasztás ellenőrzése a konverzió előtt és után

A `Metered` osztály további metódusokat biztosít a kreditfelhasználás lekérdezéséhez. Ezek a két sor kiírják a megmaradt kredit egyenleget és a konverzió által felhasznált kredit mennyiségét.

A Metered.getConsumptionCredit() visszaadja a megmaradt kredit egyenleget, míg a Metered.getConsumptionQuantity() visszaadja az utolsó művelet által felhasznált krediteket.

```java
System.out.println(String.format("Credit before operation: %.02f", Metered.getConsumptionCredit()));
System.out.println(String.format("Consumption quantity before operation: %.02f", Metered.getConsumptionQuantity()));
```

A `save` művelet után ugyanazok a hívások futtatása megmutatja a frissített értékeket, lehetővé téve, hogy ellenőrizze, a mérő licenc helyesen követi a használatot.

{{< blocks/products/products-backtop-button >}}

## Gyakori problémák és megoldások

| Probléma | Miért fordul elő | Megoldás |
|----------|-------------------|----------|
| **Invalid metered keys** | A kulcsok el vannak gépelve vagy lejártak. | Ellenőrizze a kulcsokat az Aspose fiókjából; szükség esetén generáljon újat. |
| **File not found** | A `dataDir` útvonal helytelen. | Használjon abszolút útvonalat vagy ellenőrizze a relatív útvonalat a projekt gyökerétől. |
| **Insufficient credits** | Minden kredit felhasználásra került. | Vásároljon további krediteket, vagy váltson állandó licencre nagy mennyiségű terhelés esetén. |

## Gyakran ismételt kérdések

**Q: Mi az a mérő licenc?**  
A: A mérő licenc lehetővé teszi, hogy a kreditek alapján fizessen az API használatáért, finomhangolt költségkontrollt biztosítva.

**Q: Hogyan szerezhetek mérő kulcsot az Aspose termékekhez?**  
A: Vásároljon licencet az Aspose weboldaláról, vagy kérjen ideiglenes értékelő kulcsot a fiókjának irányítópultján keresztül.

**Q: Használhatok mérő licencet több alkalmazásban?**  
A: Igen, de minden fogyasztás ugyanazon kulcs alatt aggregálódik, ezért figyelje a teljes használatot.

**Q: Van ingyenes próba az Aspose.Note for Java-hoz?**  
A: Igen, letölthet egy ingyenes próbát [innen](https://releases.aspose.com/).

**Q: Hol kaphatok támogatást az Aspose.Note for Java-hoz?**  
A: Tegyen fel kérdéseket az Aspose közösségi fórumokon [itt](https://forum.aspose.com/c/note/28).

## Összegzés

Most már rendelkezik egy teljes, termelésre kész munkafolyamattal a **convert OneNote to PDF** feladathoz, miközben Java-ban kezeli a mérő licencet. A kreditfogyasztás ellenőrzésével a konverzió előtt és után biztosíthatja, hogy alkalmazása a költségvetésen belül marad és hatékonyan skálázódik. Nyugodtan fedezze fel az Aspose.Note további funkcióit, például egyedi oldalrenderelést, képek kinyerését és kötegelt feldolgozást, hogy tovább bővítse ezt a megoldást.

---

**Legutóbb frissítve:** 2026-07-05  
**Tesztelve a következővel:** Aspose.Note for Java 24.12 (legújabb a írás időpontjában)  
**Szerző:** Aspose

## Kapcsolódó útmutatók

- [Aspose.Note Licencelés Java-val – Hogyan monitorozzuk a krediteket](/note/java/licensing-java/)
- [convert onenote to pdf – Jegyzetfüzet konvertálása PDF-re az Aspose.Note segítségével](/note/java/onenote-notebook-operations/convert-notebook-to-pdf/)
- [Jegyzetfüzet konvertálása PDF-re opciókkal a OneNote-ban – Aspose.Note](/note/java/onenote-notebook-operations/convert-notebook-to-pdf-with-options/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}