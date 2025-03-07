---
title: Az aktuális oldalverzió leküldése a OneNote-ban – Aspose.Note
linktitle: Az aktuális oldalverzió leküldése a OneNote-ban – Aspose.Note
second_title: Aspose.Note Java API
description: Tartsa frissen a OneNote tartalmát! Ismerje meg az oldalelőzmények frissítését és a verziók kezelését, lépésről lépésre útmutatót és kódot mellékelve. #OneNote #Java #Aspose
weight: 18
url: /hu/java/onenote-page-manipulation/push-current-page-version/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Az aktuális oldalverzió leküldése a OneNote-ban – Aspose.Note

## Bevezetés

Ebben az oktatóanyagban megvizsgáljuk, hogyan használhatja az Aspose.Note for Java alkalmazást az aktuális oldalverzió OneNote-ban való megjelenítéséhez. Az Aspose.Note egy hatékony Java-könyvtár, amely lehetővé teszi a fejlesztők számára, hogy programozottan dolgozzanak Microsoft OneNote-dokumentumokkal, lehetővé téve különféle műveleteket, például OneNote-fájlok létrehozását, kezelését és konvertálását.

## Előfeltételek

Mielőtt elkezdené, győződjön meg arról, hogy rendelkezik a következő előfeltételekkel:
1. Java programozási nyelv alapismerete.
2. Java Development Kit (JDK) telepítve a rendszerére.
3.  Aspose.Note a Java könyvtárhoz. Letöltheti innen[itt](https://releases.aspose.com/note/java/).
4. Egy minta OneNote-dokumentum, amellyel dolgozni.

## Csomagok importálása

Először is importálnia kell a szükséges csomagokat a Java projektbe az Aspose.Note funkciók használatához.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## 1. lépés: Töltse be a OneNote-dokumentumot

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
```

 Itt,`dataDir` arra a könyvtárra kell mutatnia, ahol a OneNote-dokumentum található. Cserélje ki`"Sample1.one"` a OneNote-fájl nevével.

## 2. lépés: Szerezze be az aktuális oldalt és előzményeit

```java
Page page = document.getFirstChild();
PageHistory pageHistory = document.getPageHistory(page);
```

 A dokumentum első oldalát a segítségével lekérjük`getFirstChild()` majd a használatával szerezze be az előzményeket`getPageHistory()`.

## 3. lépés: Nyomja meg az aktuális oldalverziót

```java
pageHistory.addItem(page.deepClone());
```

Itt hozzáadjuk az oldal aktuális verzióját az előzményekhez úgy, hogy klónozzuk, és új elemként adjuk hozzá.

## 4. lépés: Mentse el a dokumentumot

```java
document.save(dataDir + "PushCurrentPageVersion_out.one");
```

Végül elmentjük a módosított dokumentumot a frissített oldaltörténettel.

## Következtetés

Ebben az oktatóanyagban megtanultuk, hogyan töltheti le az aktuális oldalverziót a OneNote-ban az Aspose.Note for Java használatával. Az alábbi lépések követésével hatékonyan kezelheti a OneNote-dokumentumok verziószámát programozottan.

## GYIK

### 1. kérdés: Használhatom az Aspose.Note for Java programot titkosított OneNote-fájlokkal való együttműködéshez?

1. válasz: Igen, az Aspose.Note for Java támogatja mind a titkosított, mind a titkosítatlan OneNote-fájlokkal való munkát.

### 2. kérdés: Az Aspose.Note for Java kompatibilis a OneNote legújabb verziójával?

2. válasz: Az Aspose.Note for Java igyekszik fenntartani a kompatibilitást a OneNote dokumentumok legújabb verzióival.

### 3. kérdés: manipulálhatok szöveget és képeket a OneNote-dokumentumokban az Aspose.Note for Java segítségével?

3. válasz: Az Aspose.Note for Java kiterjedt funkciókat kínál a szövegek, képek és egyéb elemek kezeléséhez a OneNote-fájlokon belül.

### 4. kérdés: Az Aspose.Note for Java támogatja a OneNote-fájlok más formátumokba konvertálását?

4. válasz: Igen, az Aspose.Note for Java támogatja a OneNote-fájlok konvertálását különféle formátumokba, például PDF-, HTML- és képformátumokba.

### 5. kérdés: Hol kaphatok támogatást az Aspose.Note for Java-hoz, ha problémákat tapasztalok?

 A5: Meglátogathatja a[Aspose.Note fórum](https://forum.aspose.com/c/note/28) segítséget kérni a közösségtől, vagy közvetlenül kapcsolatba lépni az Aspose ügyfélszolgálatával.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
