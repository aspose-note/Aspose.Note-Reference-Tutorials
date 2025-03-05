---
title: Az oldalak átdolgozása a OneNote-ban – Aspose.Note
linktitle: Az oldalak átdolgozása a OneNote-ban – Aspose.Note
second_title: Aspose.Note Java API
description: Ismerje meg, hogyan kérheti le a OneNote-dokumentumok oldalainak változatait az Aspose.Note Java használatával. Integrálja ezt Java-alkalmazásaiba a hatékony dokumentumkezelés érdekében.
type: docs
weight: 15
url: /hu/java/onenote-page-manipulation/get-revisions-of-pages/
---
## Bevezetés

Ebben az oktatóanyagban az Aspose.Note for Java képességeit mutatjuk be. Ez egy olyan hatékony könyvtár, amely lehetővé teszi, hogy zökkenőmentesen dolgozzon a Microsoft OneNote fájlokkal Java-alkalmazásaiban. Pontosabban arra fogunk összpontosítani, hogyan lehet lekérni az oldalak változatait egy OneNote-dokumentumban. Ennek az útmutatónak a végére birtokában lesz az oldalváltozatok hatékony kinyeréséhez szükséges ismereteknek, beleértve az olyan részleteket, mint az utolsó módosítás ideje, a létrehozási idő, a cím, a szint és a szerző.

## Előfeltételek

Mielőtt belevágna ebbe az oktatóanyagba, győződjön meg arról, hogy beállította a következő előfeltételeket:

### Java Development Kit (JDK) telepítve

Győződjön meg arról, hogy a Java Development Kit telepítve van a rendszerére. Letöltheti és telepítheti az Oracle webhelyéről, vagy csomagkezelőt használhat, ha Unix-alapú rendszert használ.

### Aspose.Note for Java Library

 Töltse le és telepítse az Aspose.Note for Java könyvtárat a webhelyről. A letöltési linket megtalálod[itt](https://releases.aspose.com/note/java/) . Kövesse a dokumentációban található telepítési utasításokat[itt](https://reference.aspose.com/note/java/).

## Csomagok importálása

Kezdésként importálja a szükséges csomagokat a Java projektbe. Ezek a csomagok lehetővé teszik az Aspose.Note for Java által biztosított funkciók kihasználását.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

Most bontsuk le a példakódot több lépésre, hogy megértsük az egyes összetevőket és azok funkcióit.

## 1. lépés: Állítsa be a dokumentumkönyvtárat

Határozza meg a könyvtárat, ahol a OneNote-dokumentum található.

```java
String dataDir = "Your Document Directory";
```

## 2. lépés: Töltse be a dokumentumot

Töltse be a OneNote-dokumentumot az Aspose.Note-ba.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## 3. lépés: Szerezze be az első oldalt

Keresse ki a dokumentum első oldalát.

```java
Page firstPage = doc.getFirstChild();
```

## 4. lépés: Szerezze be az oldalváltozatokat

Szerezze be az oldal felülvizsgálati előzményeit.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## 5. lépés: Járja be az oldalváltozatokat

Ismételje meg az oldalváltozatok listáját, és kérjen le releváns információkat.

```java
for (Page pageRevision : revisions) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

## Következtetés

Ebben az oktatóanyagban megvizsgáltuk, hogyan lehet lekérni egy OneNote-dokumentum oldalainak változatait az Aspose.Note for Java használatával. A lépésenkénti útmutató követésével és a mellékelt példakód felhasználásával könnyedén integrálhatja ezt a funkciót Java-alkalmazásaiba, lehetővé téve a OneNote-fájlok hatékony kezelését.

## GYIK

### 1. kérdés: Használhatom az Aspose.Note for Java programot új OneNote-dokumentumok létrehozására?

1. válasz: Igen, az Aspose.Note for Java átfogó támogatást nyújt a OneNote-dokumentumok programozott létrehozásához, olvasásához és kezeléséhez.

### 2. kérdés: Az Aspose.Note for Java kompatibilis a OneNote-fájlok különböző verzióival?

2. válasz: Igen, az Aspose.Note for Java támogatja a Microsoft OneNote-fájlok különféle verzióit, így biztosítja a kompatibilitást a különböző környezetekben.

### 3. kérdés: Testreszabhatom a kimeneti formátumot a OneNote-dokumentumok exportálásakor?

3. válasz: Az Aspose.Note for Java rugalmasságot kínál a OneNote-dokumentumok különböző formátumokba, például PDF-be, HTML-be és képekbe történő exportálásához, testreszabási lehetőségekkel.

### 4. kérdés: Az Aspose.Note for Java licencet igényel kereskedelmi használatra?

4. válasz: Igen, az Aspose.Note for Java kereskedelmi használatához érvényes licenc szükséges. A licencet az Aspose webhelyéről szerezheti be.

### 5. kérdés: Hol kérhetek segítséget, ha problémákat tapasztalok vagy kérdéseim vannak az Aspose.Note for Java-val kapcsolatban?

 5. válasz: Támogatásért és segítségért keresse fel az Aspose.Note fórumot[itt](https://forum.aspose.com/c/note/28)ahol kérdéseket tehet fel, megoszthatja tapasztalatait, és kapcsolatba léphet más felhasználókkal és szakértőkkel.