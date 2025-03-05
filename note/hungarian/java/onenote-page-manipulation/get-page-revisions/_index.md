---
title: Szerezzen be oldalváltozatokat a OneNote-ban – Aspose.Note
linktitle: Szerezzen be oldalváltozatokat a OneNote-ban – Aspose.Note
second_title: Aspose.Note Java API
description: Ismerje meg, hogyan kérheti le az oldalváltozatokat a OneNote-ban az Aspose.Note for Java használatával. Kövesse lépésenkénti útmutatónkat a változások hatékony nyomon követéséhez.
type: docs
weight: 14
url: /hu/java/onenote-page-manipulation/get-page-revisions/
---
## Bevezetés

A OneNote egy hatékony eszköz a jegyzetek rendszerezésére és kezelésére, de időnként nyomon kell követnie az oldalain végrehajtott változtatásokat és átdolgozásokat. Az Aspose.Note for Java segítségével könnyedén lekérheti az oldalváltozatokat programozottan. Ebben az oktatóanyagban végigvezetjük Önt a OneNote-ban az Aspose.Note for Java használatával oldalverziók beszerzésének folyamatán.

## Előfeltételek

Mielőtt elkezdené, győződjön meg arról, hogy a következő előfeltételek teljesülnek:

### 1. Java fejlesztőkészlet (JDK)

Győződjön meg arról, hogy a Java Development Kit (JDK) telepítve van a rendszerén. A JDK letölthető és telepíthető az Oracle webhelyéről.

### 2. Aspose.Note for Java

Töltse le és telepítse az Aspose.Note for Java programot a[letöltési link](https://releases.aspose.com/note/java/).

### 3. Minta OneNote-dokumentum

Készítsen egy minta OneNote dokumentumot (`Sample1.one`), amely azokat az oldalakat tartalmazza, amelyekről a revíziókat le szeretné kérni.

## Csomagok importálása

Először is importálnia kell a szükséges csomagokat az Aspose.Note for Java-ból.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

Most bontsuk fel a megadott példát több lépésre:

## 1. lépés: Állítsa be a dokumentumkönyvtárat

Határozza meg a könyvtár elérési útját, ahol a OneNote-dokumentum található.

```java
String dataDir = "Your Document Directory";
```

## 2. lépés: Töltse be a OneNote-dokumentumot

 Töltse be a OneNote-dokumentumot a segítségével`LoadOptions` a betöltési előzmények engedélyezéséhez.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

## 3. lépés: Szerezze be az első oldalt

Vegye ki az első oldalt a betöltött dokumentumból.

```java
Page firstPage = document.getFirstChild();
```

## 4. lépés: Ismétlés oldal-revíziókkal

Ismételje meg az egyes oldalváltozatokat, és kérjen le releváns információkat, például az utolsó módosítás idejét, a létrehozási időt, a címet, a szintet és a szerzőt.

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

## Következtetés

Ebben az oktatóanyagban megtanultuk, hogyan kérheti le az oldalváltozatokat a OneNote-ban az Aspose.Note for Java használatával. Az alábbi lépések követésével hatékonyan nyomon követheti a OneNote-oldalain végrehajtott módosításokat programozottan.

## GYIK

### 1. kérdés: Használhatom az Aspose.Note for Java-t az oldalváltozatok módosítására?

1. válasz: Nem, az Aspose.Note for Java jelenleg támogatja az oldalverziók lekérését, de nem módosítja azokat.

### 2. kérdés: Az Aspose.Note for Java kompatibilis a OneNote dokumentumok különböző verzióival?

2. válasz: Igen, az Aspose.Note for Java támogatja a OneNote-dokumentumok különféle verzióit, így zökkenőmentesen dolgozhat különböző fájlformátumokkal.

### 3. kérdés: Az Aspose.Note for Java használatához licenc szükséges?

3. válasz: Igen, licencet kell vásárolnia az Aspose.Note for Java kereskedelmi projektekben való használatához. Ugyanakkor kiértékelési célból ideiglenes engedélyt is szerezhet.

### 4. kérdés: Kérhetek-e támogatást, ha az Aspose.Note for Java használata során bármilyen problémát tapasztalok?

 4. válasz: Igen, kérhet támogatást az Aspose.Note fórumtól[itt](https://forum.aspose.com/c/note/28).

### 5. kérdés: Elérhető az Aspose.Note for Java ingyenes próbaverziója?

 5. válasz: Igen, elérheti az Aspose.Note for Java ingyenes próbaverzióját a webhelyről[weboldal](https://releases.aspose.com/).