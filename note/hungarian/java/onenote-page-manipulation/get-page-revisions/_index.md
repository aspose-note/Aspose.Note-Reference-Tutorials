---
date: 2026-01-10
description: Ismerje meg az aspose.note oldalváltozatok oktatóját Java-hoz – programozottan
  szerezze be a OneNote oldalváltozatokat az Aspose.Note használatával. Kövesse lépésről
  lépésre útmutatónkat.
linktitle: Get Page Revisions in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: aspose.note oldalváltozatok útmutató – Oldalváltozatok lekérése a OneNote-ban
url: /hu/java/onenote-page-manipulation/get-page-revisions/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Oldalrevíziók lekérése a OneNote-ban – Aspose.Note

OneNote egy erőteljes jegyzetkészítő platform, és amikor a változások auditálására van szükség, a **aspose.note page revisions tutorial** pontosan megmutatja, hogyan lehet néhány Java kódsorral lekérni a revíziótörténetet. Ebben az útmutatóban végigvezetünk minden szükséges lépésen – a környezet beállításától az egyes revíziók részleteinek kiírásáig – hogy könnyedén nyomon követhesse a szerkesztéseket, a szerzői hozzájárulásokat és az időbélyegeket.

## Gyors válaszok
- **Mi a tutorial tartalma?** A OneNote fájlból történő oldalrevíziók történetének lekérése az Aspose.Note for Java használatával.  
- **Melyik könyvtárverzió szükséges?** Bármely, a `LoadOptions.setLoadHistory`-t támogató, legújabb Aspose.Note for Java kiadás.  
- **Szükségem van licencre?** Ideiglenes értékelő licenc teszteléshez megfelelő; a termeléshez kereskedelmi licenc szükséges.  
- **Módosíthatok revíziókat?** Az API csak olvasásra engedélyezi a revíziókat; csak lekérhetők.  
- **Mik a fő előfeltételek?** Java JDK, Aspose.Note for Java, és egy OneNote dokumentum revíziós adatokkal.

## Mi az a “aspose.note page revisions tutorial”?
A tutorial bemutatja, hogyan lehet programozottan hozzáférni egy OneNote oldal történeti verzióihoz. Minden revízió metaadatokat tartalmaz, például a szerzőt, a létrehozás időpontját és a módosítás időpontját, lehetővé téve audit nyomvonalak vagy változásnapló funkciók építését az alkalmazásokban.

## Miért használja az Aspose.Note-ot az oldalrevíziók nyomon követéséhez?
- **Nincs UI függőség** – teljesen kódból működik, tökéletes a háttérszolgáltatásokhoz.  
- **Keresztplatformos** – a Java fut Windows, Linux és macOS rendszereken.  
- **Teljes irányítás** – minden revízió tulajdonság lekérhető a OneNote manuális megnyitása nélkül.  
- **Teljesítmény** – a történelem betöltése optimalizált, így még nagy jegyzetfüzetek is gyorsan feldolgozhatók.

## Előfeltételek

### 1. Java fejlesztői csomag (JDK)
Győződjön meg róla, hogy egy naprakész JDK (8 vagy újabb) telepítve van, és a `JAVA_HOME` be van állítva.

### 2. Aspose.Note for Java
Töltse le a könyvtárat a [download link](https://releases.aspose.com/note/java/) címről.

### 3. Minta OneNote dokumentum
Hozzon létre vagy szerezzen be egy OneNote fájlt (pl. `Sample1.one`), amely tartalmaz revíziótörténettel rendelkező oldalakat.

## Csomagok importálása
Először importálja a szükséges Aspose.Note osztályokat.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## Lépésről‑lépésre megvalósítás

### 1. lépés: Dokumentum könyvtár beállítása
Adja meg azt a mappát, ahol a OneNote fájlja található.

```java
String dataDir = "Your Document Directory";
```

### 2. lépés: OneNote dokumentum betöltése a történelem engedélyezésével
Engedélyezze a `LoadOptions` jelzőt a revíziós adatok lekéréséhez.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

### 3. lépés: Az első oldal lekérése
Szerezze meg az első oldal objektumát; ez lesz a referenciapont a történelem lekéréséhez.

```java
Page firstPage = document.getFirstChild();
```

### 4. lépés: Az oldalrevíziók iterálása
Iteráljon minden revízión, és nyomtasson hasznos metaadatokat, például időbélyegeket, címet, szintet és szerzőt.

```java
for (Page pageRevision : document.getPageHistory(firstPage)) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

> **Pro tipp:** Ha egy adott szerző vagy dátumtartomány szerint szeretné szűrni a revíziókat, egyszerűen adjon hozzá feltételes ellenőrzéseket a `for` cikluson belül.

## Gyakori problémák és megoldások
- **Nem tér vissza revízió:** Ellenőrizze, hogy a `loadOptions.setLoadHistory(true)` hívás megtörtént-e a dokumentum betöltése előtt.  
- **Null szerző vagy cím:** Egyes régebbi OneNote verziók nem tárolhatják ezeket a mezőket; kezelje a `null` értékeket megfelelően.  
- **Teljesítménycsökkenés nagy jegyzetfüzeteknél:** Töltse be csak a szükséges szakaszokat, vagy növelje a JVM heap méretét.

## Gyakran ismételt kérdések

**Q1: Használhatom az Aspose.Note for Java-t az oldalrevíziók módosítására?**  
A1: Nem, az API jelenleg csak olvasás‑csak hozzáférést biztosít az oldalrevíziókhoz.

**Q2: Az Aspose.Note for Java kompatibilis a OneNote dokumentumok különböző verzióival?**  
A2: Igen, különböző OneNote fájlformátumokkal működik, lehetővé téve a zökkenőmentes feldolgozást a verziók között.

**Q3: Az Aspose.Note for Java használatához szükséges licenc?**  
A3: Kereskedelmi licenc szükséges a termeléshez, de ideiglenes értékelő licenc elérhető teszteléshez.

**Q4: Kaphatok támogatást, ha problémáim merülnek fel az Aspose.Note for Java használata során?**  
A4: Igen, kérdéseket tehet fel az Aspose.Note fórumon [itt](https://forum.aspose.com/c/note/28).

**Q5: Van ingyenes próba a Aspose.Note for Java-hoz?**  
A5: Igen, letölthet egy ingyenes próbaverziót a [weboldalról](https://releases.aspose.com/).

---

**Utolsó frissítés:** 2026-01-10  
**Tesztelve:** Aspose.Note for Java (legújabb kiadás)  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}