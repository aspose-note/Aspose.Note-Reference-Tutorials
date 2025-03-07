---
title: Információk a OneNote oldalairól – Aspose.Note
linktitle: Információk a OneNote oldalairól – Aspose.Note
second_title: Aspose.Note Java API
description: Fedezze fel az oldaltitkokat a OneNote-dokumentumokban! Az Aspose.Note segítségével kivonhatja a revíziókat, a létrehozási időket és egyebeket. Lépésről lépésre útmutató és kód mellékelve! #OneNote #Java #Aspose
weight: 12
url: /hu/java/onenote-page-manipulation/get-information-about-pages/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Információk a OneNote oldalairól – Aspose.Note

## Bevezetés

Ebben az oktatóanyagban végigvezetjük a OneNote-ban lévő oldalak információinak Aspose.Note for Java segítségével történő kinyerésének folyamatán. Az Aspose.Note egy hatékony API, amely lehetővé teszi a Microsoft OneNote dokumentumok programozott kezelését. Akár oldalváltozatokhoz, létrehozási időpontokhoz, címekhez vagy szerzőkhöz kell hozzáférnie, az Aspose.Note intuitív kezelőfelületével leegyszerűsíti a feladatot.

## Előfeltételek

Mielőtt elkezdené, győződjön meg arról, hogy rendelkezik a következőkkel:

1. Java Development Kit (JDK): Győződjön meg arról, hogy a JDK telepítve van a rendszeren.
2.  Aspose.Note for Java: Töltse le és telepítse az Aspose.Note for Java könyvtárat. Beszerezheti a[weboldal](https://purchase.aspose.com/buy).
3. Minta OneNote-dokumentum: Készítsen egy minta OneNote-dokumentumot, amelyből információkat kérhet le.

## Csomagok importálása

Először is importálnia kell a szükséges csomagokat az Aspose.Note használatához a Java projektben.

```java
import java.io.IOException;
import java.util.List;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## 1. lépés: Töltse be a OneNote-dokumentumot

Először töltse be a OneNote-dokumentumot az Aspose.Note használatával.

```java
String dataDir = "Your Document Directory";
// Töltse be a dokumentumot az Aspose.Note-ba
LoadOptions options = new LoadOptions();
Document doc = new Document(dataDir + "Sample1.one", options);
```

 Cserélje ki`"Your Document Directory"` a OneNote-dokumentum elérési útjával.

## 2. lépés: Az oldal információinak lekérése

Ezután kérjen le információkat a OneNote-dokumentum oldalairól.

```java
// Szerezzen be oldalváltozatokat
List<Page> pages = doc.getChildNodes(Page.class);

// Lapok listájának bejárása
for (Page pageRevision : pages) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
}
```

Ez a kódrészlet végighalad a dokumentum minden oldalán, és kinyomtatja az olyan információkat, mint az utolsó módosítás ideje, a létrehozás ideje, címe, szintje és szerzője.

## Következtetés

Ebben az oktatóanyagban megtanulta, hogyan kérhet le információkat a OneNote oldalairól az Aspose.Note for Java segítségével. A fent vázolt lépések követésével zökkenőmentesen integrálhatja az Aspose.Note-ot Java-alkalmazásaiba, így értékes adatokat nyerhet ki a OneNote-dokumentumokból.

## GYIK

### 1. kérdés: Használhatom az Aspose.Note for Java programot OneNote-dokumentumok szerkesztéséhez?

1. válasz: Igen, az Aspose.Note a szolgáltatások átfogó készletét kínálja a OneNote-dokumentumok programozott szerkesztéséhez és kezeléséhez.

### 2. kérdés: Az Aspose.Note kompatibilis a OneNote összes verziójával?

2. válasz: Az Aspose.Note a OneNote különféle verzióit támogatja, biztosítva a kompatibilitást a különböző környezetekben.

### 3. kérdés: Átalakíthatom a OneNote dokumentumokat más formátumokba az Aspose.Note segítségével?

3. válasz: Az Aspose.Note segítségével könnyedén konvertálhat OneNote-dokumentumokat PDF-, HTML- és képek formátumba.

### 4. kérdés: Az Aspose.Note kínál technikai támogatást a fejlesztőknek?

4. válasz: Igen, az Aspose speciális technikai támogatást nyújt a fejlesztőknek az Aspose.Note használata során felmerülő problémák megoldásához.

### 5. kérdés: Elérhető az Aspose.Note for Java próbaverziója?

 5. válasz: Igen, letöltheti az Aspose.Note for Java ingyenes próbaverzióját a webhelyről[itt](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
