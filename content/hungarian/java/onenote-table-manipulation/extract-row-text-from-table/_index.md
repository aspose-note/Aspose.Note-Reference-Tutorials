---
title: Sorszöveg kibontása a OneNote-dokumentum táblázatából – Aspose.Note
linktitle: Sorszöveg kibontása a OneNote-dokumentum táblázatából – Aspose.Note
second_title: Aspose.Note Java API
description: Az Aspose.Note for Java segítségével megtanulhatja, hogyan bontsa ki könnyedén sorszövegeket OneNote-táblázatokból. Kövesse lépésenkénti útmutatónkat a zökkenőmentes integráció érdekében.
type: docs
weight: 13
url: /hu/java/onenote-table-manipulation/extract-row-text-from-table/
---
## Bevezetés
Üdvözöljük ebben az átfogó oktatóanyagban, amely az Aspose.Note for Java segítségével sorszöveg kinyerésére szolgál a OneNote dokumentumok táblázataiból. Az Aspose.Note egy hatékony Java-könyvtár, amely lehetővé teszi a fejlesztők számára, hogy zökkenőmentesen dolgozzanak a Microsoft OneNote fájlokkal. Ebben az oktatóanyagban lépésről lépésre végigvezetjük a folyamaton, bemutatva, hogyan lehet hatékonyan kinyerni a sorok szövegét a OneNote-dokumentumok táblázataiból.
## Előfeltételek
Mielőtt belevágnánk az oktatóanyagba, győződjön meg arról, hogy a következő előfeltételek teljesülnek:
-  Aspose.Note for Java Library: Győződjön meg arról, hogy telepítve van az Aspose.Note for Java könyvtár. Letöltheti a[letöltési link](https://releases.aspose.com/note/java/).
- Java fejlesztői környezet: Győződjön meg arról, hogy be van állítva Java fejlesztői környezet a gépén.
- OneNote-dokumentum: Készítsen egy minta OneNote-dokumentumot (pl. "Sample1.one"), amely azokat a táblázatokat tartalmazza, amelyekből ki szeretné bontani a sor szövegét.
## Csomagok importálása
Java-projektjében importálja a szükséges Aspose.Note csomagokat. Ez biztosítja, hogy hozzáférjen a OneNote-dokumentumok kezeléséhez szükséges osztályokhoz és metódusokhoz.
```java
import java.io.IOException;
import java.util.List;
import java.util.stream.Collectors;
import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.RichText;
import com.aspose.note.Table;
import com.aspose.note.TableRow;
```
## 1. lépés: Állítsa be a dokumentumkönyvtárat
```java
// A dokumentumok könyvtárának elérési útja.
String dataDir = "Your Document Directory";
```
## 2. lépés: Töltse be a OneNote-dokumentumot
```java
// Töltse be a dokumentumot az Aspose.Note-ba.
Document document = new Document(dataDir + "Sample1.one", new LoadOptions());
```
## 3. lépés: Szerezze be a táblázat csomópontjait
```java
// Szerezze meg a táblázat csomópontjainak listáját
List<Table> nodes = (List<Table>) document.getChildNodes(Table.class);
```
## 4. lépés: Ismétlés táblázatokon és sorokon keresztül
```java
// Sorszám beállítása
int rowCount = 0;
for (Table table : nodes) {
    // Iteráció a táblázat sorain keresztül
    for (TableRow row : table) {
        rowCount++;
        // Szöveg lekérése
        List<RichText> textNodes = (List<RichText>) row.getChildNodes(RichText.class);
        StringBuilder text = new StringBuilder();
        for (RichText richText : textNodes) {
            text = text.append(richText.getText().toString());
        }
        // Szöveg nyomtatása a kimeneti képernyőn
        System.out.println(text);
    }
}
```
Ismételje meg ezeket a lépéseket a OneNote-dokumentum minden táblájához, és sikeresen kibontja a sor szövegét.
## Következtetés
Gratulálunk! Megtanulta, hogyan vonhat ki sorszöveget a OneNote-dokumentumok táblázataiból az Aspose.Note for Java segítségével. Ez az oktatóanyag alapot nyújt az Aspose.Note hatékony képességeinek kiaknázásához a Java-alkalmazásokban.
## Gyakran Ismételt Kérdések
### Az Aspose.Note kompatibilis a Microsoft OneNote legújabb verziójával?
 Az Aspose.Note a OneNote különféle verzióit támogatja, beleértve a legújabbat is. Utal[dokumentáció](https://reference.aspose.com/note/java/) a kompatibilitási részletekért.
### Kipróbálhatom az Aspose.Note for Java programot vásárlás előtt?
Igen, felfedezheti az Aspose.Note ingyenes próbaverzióját a címen[ez a link](https://releases.aspose.com/).
### Hol találhatok további támogatást és segítséget?
 Meglátogatni a[Aspose.Note fórum](https://forum.aspose.com/c/note/28) közösségi támogatásra és beszélgetésekre.
### Hogyan szerezhetek ideiglenes licencet az Aspose.Note számára?
 Szerezzen ideiglenes engedélyt innen[ez a link](https://purchase.aspose.com/temporary-license/).
### Vannak speciális rendszerkövetelmények az Aspose.Note for Java használatához?
A részletes rendszerkövetelményeket a dokumentációban találja.