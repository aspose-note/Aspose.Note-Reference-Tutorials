---
title: Adjon hozzá táblázatcsomópontot címkével az Aspose.Note-ban
linktitle: Adjon hozzá táblázatcsomópontot címkével az Aspose.Note-ban
second_title: Aspose.Note .NET API
description: Ismerje meg, hogyan adhat hozzá címkéket tartalmazó táblázatokat az Aspose.Note for .NET-hez. Programozottan javítsa dokumentumkezelési készségeit.
weight: 11
url: /hu/net/tag-management/add-table-node-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Adjon hozzá táblázatcsomópontot címkével az Aspose.Note-ban

## Bevezetés

Ebben az oktatóanyagban végigvezetjük Önt egy táblacsomópont hozzáadásának folyamatán az Aspose.Note for .NET használatával. Ennek eléréséhez kövesse az alábbi lépéseket.

## Névterek importálása

Mielőtt elkezdené, importálja a szükséges névtereket az Aspose használatához.Megjegyzés:

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using Aspose.Note.Examples.CSharp.Tables;
```

## Előfeltételek

A folytatás előtt győződjön meg arról, hogy beállította a következő előfeltételeket:

1.  Telepítés: Töltse le és telepítse az Aspose.Note for .NET könyvtárat innen[itt](https://releases.aspose.com/note/net/).
2.  Licenc: Szerezzen licencet vagy használja a[ideiglenes engedély](https://purchase.aspose.com/temporary-license/) a könyvtár használatához.
3. Fejlesztői környezet: legyen beállítva egy kompatibilis fejlesztői környezet, például a Visual Studio.

## 1. lépés: Inicializálja a dokumentum- és oldalobjektumokat

 Kezdje a példány létrehozásával a`Document` osztály és inicializálás a`Page` tárgy:

```csharp
Document doc = new Document();
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## 2. lépés: Hozzon létre táblázat-, sor- és cellaobjektumokat

 Inicializálja a`Table`, `TableRow` , és`TableCell` objektumok:

```csharp
TableRow row = new TableRow(doc);
TableCell cell = new TableCell(doc);
```

## 3. lépés: Szúrjon be tartalmat a cellába

 Adjon hozzá tartalmat a cellához a gombbal`AppendChildLast` módszer:

```csharp
cell.AppendChildLast(InsertTable.GetOutlineElementWithText(doc, "Single cell."));
```

## 4. lépés: Inicializálja a táblázat csomópontját

 Inicializálja a`Table` objektum meghatározott tulajdonságokkal:

```csharp
Table table = new Table(doc)
{
    IsBordersVisible = true,
    Columns = { new TableColumn { Width = 70 } }
};
```

## 5. lépés: Adjon hozzá sort a táblázathoz

Adja hozzá a sor csomópontját a táblázathoz:

```csharp
table.AppendChildLast(row);
```

## 6. lépés: Adjon hozzá címkét a táblázat csomópontjához

Tartalmazzon címkét a táblázat csomópontjához:

```csharp
table.Tags.Add(NoteTag.CreateQuestionMark());
```

## 7. lépés: Adjon hozzá táblázatcsomópontot a vázlatelemhez

 Hozzon létre egy`Outline` és`OutlineElement` a táblázat csomópontjának hozzáadásához:

```csharp
Outline outline = new Outline(doc);
OutlineElement outlineElem = new OutlineElement(doc);
outlineElem.AppendChildLast(table);
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## 8. lépés: Mentse el a dokumentumot

Mentse el a OneNote-dokumentumot:

```csharp
string dataDir = "Your Document Directory";
dataDir = dataDir + "AddTableNodeWithTag_out.one";
doc.Save(dataDir);
Console.WriteLine("\nTable node with tag added successfully.\nFile saved at " + dataDir);
```

A lépések végrehajtása után sikeresen hozzá kellett adnia egy táblacsomópontot egy címkével az Aspose.Note for .NET segítségével.

## Következtetés

Ebben az oktatóanyagban bemutattuk egy táblacsomópont hozzáadásának folyamatát címkével az Aspose.Note for .NET-hez. Az alábbi lépések követésével hatékonyan kezelheti a OneNote-dokumentumokat programozottan, javítva ezzel a dokumentumkezelési képességeket.

## GYIK

### 1. kérdés: Az Aspose.Note kompatibilis a .NET összes verziójával?

1. válasz: Az Aspose.Note for .NET támogatja a .NET-keretrendszer 2.0-s és újabb verzióit, beleértve a .NET Core-t és a .NET Standardot is.

### 2. kérdés: Kipróbálhatom az Aspose.Note-ot a licenc megvásárlása előtt?

 2. válasz: Igen, beszerezheti az Aspose.Note ingyenes próbaverzióját a webhelyről[itt](https://releases.aspose.com/).

### 3. kérdés: Hogyan szerezhetek ideiglenes licencet az Aspose.Note számára?

 V3: Ideiglenes licencet szerezhet be[ez a link](https://purchase.aspose.com/temporary-license/), amely 30 napig érvényes.

### 4. kérdés: Az Aspose.Note támogatja a dokumentumtitkosítást?

4. válasz: Igen, az Aspose.Note támogatja a OneNote-dokumentumok titkosítását az adatbiztonság érdekében.

### 5. kérdés: Rendelkezésre áll műszaki támogatás az Aspose.Note felhasználói számára?

 5. válasz: Igen, a technikai támogatást az Aspose fórumain keresztül biztosítjuk[itt](https://forum.aspose.com/c/note/28), ahol szakértőktől kérhet segítséget.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
