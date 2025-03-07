---
title: Táblázatstílus módosítása a OneNote-ban – Aspose.Note
linktitle: Táblázatstílus módosítása a OneNote-ban – Aspose.Note
second_title: Aspose.Note Java API
description: Az Aspose.Note for Java segítségével könnyedén javíthatja OneNote-táblázatait. Kövesse lépésenkénti útmutatónkat a táblázatstílusok megváltoztatásához. Töltse le a könyvtárat most!
weight: 10
url: /hu/java/onenote-table-manipulation/change-table-style/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Táblázatstílus módosítása a OneNote-ban – Aspose.Note

## Bevezetés
Az Aspose.Note for Java egy hatékony könyvtár, amely lehetővé teszi a fejlesztők számára, hogy könnyedén kezeljék a OneNote fájlokat. Ebben az oktatóanyagban a táblázatstílus megváltoztatására összpontosítunk egy OneNote-dokumentumban az Aspose.Note for Java használatával. Kövesse a lépésről lépésre szóló útmutatót, hogy javítsa asztalai megjelenését.
## Előfeltételek
Mielőtt elkezdené, győződjön meg arról, hogy a következők vannak a helyükön:
- Java fejlesztői környezet: Győződjön meg arról, hogy be van állítva Java fejlesztői környezet a gépén.
-  Aspose.Note for Java Library: Töltse le és telepítse az Aspose.Note for Java könyvtárat a[letöltési oldal](https://releases.aspose.com/note/java/).
- Dokumentumkönyvtár: Készítsen könyvtárat a OneNote-dokumentumok tárolására.
## Csomagok importálása
Java-projektjében importálja a szükséges csomagokat az Aspose használatához.Megjegyzés:
```java
import com.aspose.note.*;
import java.awt.Color;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.List;
```
## 1. lépés: Állítsa be a dokumentumot
Töltse be a OneNote-dokumentumot az Aspose.Note-ba, és kérje le a táblacsomópontok listáját
```java
// Állítsa be a dokumentumot, és szerezze be a táblázat csomópontjainak listáját
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "ChangeTableStyleIn.one");
List<Table> nodes = document.getChildNodes(Table.class);
```
## 2. lépés: Állítsa be a sorstílusokat
Ismételje meg az egyes táblázatokat, állítsa be az egyes sorok stílusát, beleértve a fejléc utáni első sor kiemelését.

```java
// Állítsa be a sorstílusokat a dokumentum minden táblájához
for (Table table : nodes) {
    setRowStyle(table.getFirstChild(), Color.GRAY, true, true);
    // Jelölje ki a fej utáni első sort.
    boolean flag = false;
    List<TableRow> rows = table.getChildren();
    for (int i = 1; i < rows.size(); ++i) {
        setRowStyle(rows.get(i), flag ? Color.lightGray : new java.awt.Color(-1, true), false, false);
        flag = !flag;
    }
}
```
## setRowStyle módszer
```java
    private static void setRowStyle(TableRow row, Color highlightColor, boolean bold, boolean italic) {
        for (TableCell cell: row)
        {
            cell.setBackgroundColor(highlightColor);
            for (RichText node: cell.getChildNodes(RichText.class))
            {
                node.getParagraphStyle().setBold(bold);
                node.getParagraphStyle().setItalic(italic);
                for (TextRun run: node.getTextRuns())
                {
                    run.getStyle().setBold(bold);
                    run.getStyle().setItalic(italic);
                }
            }
        }
    }
```
## 3. lépés: Mentse el a dokumentumot
Mentse el a módosított dokumentumot az új táblázatstílusokkal.
Ha követi ezeket a lépéseket, az Aspose.Note for Java segítségével könnyedén módosíthatja a táblázat stílusát a OneNote-dokumentumokban.

```java
// Mentse el a módosított dokumentumot
document.save(Paths.get(dataDir, "ChangeTableStyleOut.one").toString());
```
## Következtetés
Az Aspose.Note for Java leegyszerűsíti a OneNote-fájlok kezelésének folyamatát. A könyvtár lehetőségeinek kiaknázásával könnyedén javíthatja asztalai vizuális megjelenítését.

## GYIK
### Hol találom az Aspose.Note for Java dokumentációját?
 Meglátogatni a[dokumentáció](https://reference.aspose.com/note/java/) átfogó útmutatásért.
### Hogyan szerezhetek ideiglenes licencet az Aspose.Note for Java számára?
 Kövesd ezt[link](https://purchase.aspose.com/temporary-license/) ideiglenes engedély megszerzésére.
### Elérhető az Aspose.Note for Java ingyenes próbaverziója?
 Igen, letölthet egy ingyenes próbaverziót a webhelyről[itt](https://releases.aspose.com/).
### Hol kaphatok támogatást az Aspose.Note for Java számára?
 Csatlakozz a[Aspose.Note fórum](https://forum.aspose.com/c/note/28) segítséget kérni a közösségtől.
### Hogyan vásárolhatom meg az Aspose.Note for Java-t?
 Megvásárolhatja a könyvtárat[itt](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
