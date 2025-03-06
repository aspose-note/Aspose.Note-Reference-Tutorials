---
title: Az oldalváltozatok kezelése a OneNote-ban – Aspose.Note
linktitle: Az oldalváltozatok kezelése a OneNote-ban – Aspose.Note
second_title: Aspose.Note Java API
description: Ismerje meg, hogyan kezelheti az oldalváltozatokat a OneNote-dokumentumokban az Aspose.Note for Java használatával. Lépésről lépésre nyújt útmutatót a hatékony revíziókövetéshez és együttműködéshez.
weight: 21
url: /hu/java/onenote-page-manipulation/working-with-page-revisions/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Az oldalváltozatok kezelése a OneNote-ban – Aspose.Note

## Bevezetés

A OneNote egy hatékony eszköz a jegyzetek rendszerezéséhez és kezeléséhez, de időnként a módosításokkal kell dolgoznia a változások nyomon követéséhez és a hatékony együttműködéshez. Az Aspose.Note for Java segítségével egyszerűen, programozottan kezelheti a OneNote-dokumentumok oldalváltozatait. Ez az oktatóanyag lépésről lépésre végigvezeti a folyamaton.

## Előfeltételek

Mielőtt elkezdené, győződjön meg arról, hogy rendelkezik a következőkkel:

### Java fejlesztői környezet

Győződjön meg arról, hogy a Java Development Kit (JDK) telepítve van a rendszerén.

### Aspose.Note for Java Library

Töltse le és telepítse az Aspose.Note for Java könyvtárat innen[itt](https://releases.aspose.com/note/java/).

### OneNote-dokumentum

Készítsen egy minta OneNote-dokumentumot teszteléshez.

## Csomagok importálása

Java-projektjében importálja a szükséges csomagokat az Aspose.Note for Java programhoz.

```java
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.RevisionSummary;
import java.io.IOException;
import java.util.Calendar;
```

Bontsuk fel a megadott példát több lépésre az egyértelmű megértés érdekében.

## 1. lépés: Töltse be a OneNote-dokumentumot

Először töltse be a OneNote-dokumentumot, és szerezze be az első gyermekoldalt.

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
Page page = document.getFirstChild();
```

## 2. lépés: Olvassa el az oldal felülvizsgálatának összefoglalóját

Olvassa el az oldal tartalmi felülvizsgálatának összefoglalóját.

```java
RevisionSummary pageRevisionInfo = page.getPageContentRevisionSummary();
System.out.println(String.format("Author:\t%s\nModified:\t%s",
        pageRevisionInfo.getAuthorMostRecent(),
        pageRevisionInfo.getLastModifiedTime().toString()));
```

## 3. lépés: Frissítse az oldal felülvizsgálatának összegzését

Frissítse az oldal felülvizsgálati összefoglalóját az új szerzővel és a módosított dátummal.

```java
pageRevisionInfo.setAuthorMostRecent("New Author");
Calendar modifiedDate = Calendar.getInstance();
pageRevisionInfo.setLastModifiedTime(modifiedDate.getTime());
document.save(dataDir + "WorkingWithPageRevisions_out.one");
```

## Következtetés

A OneNote-dokumentumok oldalváltozatainak programozott kezelése leegyszerűsíthető az Aspose.Note for Java segítségével. Az oktatóanyagban ismertetett lépések követésével hatékonyan dolgozhat az oldalváltozatokkal a változások nyomon követése és a zökkenőmentes együttműködés érdekében.

## GYIK

### 1. kérdés: Használhatom az Aspose.Note for Java-t más Java könyvtárakkal?

V: Igen, az Aspose.Note for Java integrálható más Java-könyvtárakba a funkcionalitás javítása érdekében.

### 2. kérdés: Az Aspose.Note for Java támogatja a OneNote dokumentumok összes verzióját?

V: Az Aspose.Note for Java a OneNote dokumentumok különféle verzióit támogatja, beleértve a régebbi verziókat is.

### 3. kérdés: Az Aspose.Note for Java alkalmas vállalati szintű alkalmazásokhoz?

V: Természetesen az Aspose.Note for Java úgy lett kialakítva, hogy megfeleljen a vállalati szintű alkalmazások igényeinek robusztus szolgáltatásokkal és skálázhatósággal.

### 4. kérdés: Testreszabhatom az oldalváltozatokat az Aspose.Note for Java segítségével?

V: Igen, az Aspose.Note for Java segítségével testreszabhatja az oldalváltozatokat igényei szerint.

### 5. kérdés: Hol kaphatok támogatást az Aspose.Note for Java számára?

 V: Az Aspose.Note for Java támogatást a következő webhelyen kaphatja meg[Aspose.Note fórum](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
