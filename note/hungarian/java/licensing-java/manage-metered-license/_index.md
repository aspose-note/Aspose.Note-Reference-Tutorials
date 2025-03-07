---
title: A OneNote mérőszámos licencének kezelése Java-ban
linktitle: A OneNote mérőszámos licencének kezelése Java-ban
second_title: Aspose.Note Java API
description: Ismerje meg, hogyan kezelheti a OneNote fizetős licenceit Java-ban az Aspose.Note könyvtár használatával. Irányítsd a felhasználást, figyeld a krediteket, és hatékonyan optimalizáld a költségeket.
weight: 10
url: /hu/java/licensing-java/manage-metered-license/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# A OneNote mérőszámos licencének kezelése Java-ban

## Bevezetés

Ebben az oktatóanyagban megtudjuk, hogyan kezelheti a OneNote mérőlicenceit az Aspose.Note for Java használatával. A mért licencelés lehetővé teszi a felhasználás kreditek alapján történő nyomon követését és ellenőrzését, rugalmas és költséghatékony megoldást biztosítva.

## Előfeltételek

Mielőtt elkezdené, győződjön meg arról, hogy rendelkezik a következő előfeltételekkel:

1.  Java Development Kit (JDK): Győződjön meg arról, hogy a JDK telepítve van a rendszeren. Letöltheti innen[itt](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
   
2. Aspose.Note for Java Library: rendelkeznie kell az Aspose.Note for Java könyvtárral. Letöltheti a[weboldal](https://releases.aspose.com/note/java/).

## Csomagok importálása

Először importálja a szükséges csomagokat a Java projektbe:

```java
import com.aspose.note.Document;
import com.aspose.note.Metered;



import java.nio.file.Paths;
```

## 1. lépés: Állítsa be a mért licencet

```java
Metered metered = new Metered();
metered.setMeteredKey("MyPublicKey", "MyPrivateKey");
```

 Ebben a lépésben inicializáljuk a`Metered` osztályba, és állítsa be a mért kulcsot az Aspose által biztosított nyilvános és privát kulcsokkal.

## 2. lépés: Töltse be a dokumentumot és hajtsa végre a műveleteket

```java
String dataDir = "Your Document Directory";
Document doc = new Document(Paths.get(dataDir,"Sample1.one").toString());
doc.save(Paths.get(dataDir,"MeteredLicense.pdf").toString());
```

 Itt betöltjük a OneNote dokumentumot a megadott könyvtárból, és elmentjük PDF fájlként. Biztosítsa a cserét`"Your Document Directory"` a tényleges könyvtár elérési útjával.

## 3. lépés: Ellenőrizze a fogyasztást

```java
System.out.println(String.format("Credit before operation: %.02f", Metered.getConsumptionCredit()));
System.out.println(String.format("Consumption quantity before operation: %.02f", Metered.getConsumptionQuantity()));
```

Ez a lépés lekéri és kinyomtatja a jóváírást és a fogyasztási mennyiséget a művelet előtt és után.

## Következtetés

Ebben az oktatóanyagban megtanultuk, hogyan kezelheti a OneNote mérőlicencét Javaban az Aspose.Note könyvtár használatával. A mért licencelés rugalmasságot és ellenőrzést biztosít a használat felett, biztosítva a költséghatékonyságot és a hatékony erőforrás-gazdálkodást.

## GYIK

### 1. kérdés: Mi az a mérsékelt licenc?

1. válasz: A mért licenc lehetővé teszi, hogy figyelje és szabályozza egy API vagy szolgáltatás használatát a kreditek alapján.
   
### 2. kérdés: Hogyan szerezhetek mérős kulcsot az Aspose termékekhez?

2. válasz: A mérőkulcsot az Aspose webhelyén vásárolt licenc megvásárlásával vagy értékelési célú ideiglenes licenc kérésével szerezheti be.
   
### 3. kérdés: Használhatok fizetős licencet több alkalmazáshoz?

3. válasz: Igen, a mért licenc több alkalmazáson keresztül is használható, de a fogyasztás összesítve lesz.
   
### 4. kérdés: Elérhető az Aspose.Note for Java ingyenes próbaverziója?

 4. válasz: Igen, letölthet egy ingyenes próbaverziót a webhelyről[itt](https://releases.aspose.com/).
   
### 5. kérdés: Hol kaphatok támogatást az Aspose.Note for Java számára?

 5. válasz: Támogatást kaphat az Aspose közösségi fórumokon[itt](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
