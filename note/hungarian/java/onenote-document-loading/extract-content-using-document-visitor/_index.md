---
date: 2025-12-04
description: Tanulja meg, hogyan lehet képeket kinyerni a OneNote‑fájlokból, és hogyan
  konvertálhatja a OneNote‑ot szöveggé Java‑ban az Aspose.Note segítségével. Lépésről‑lépésre
  útmutató kódrészletekkel.
linktitle: Extract Images from OneNote using Document Visitor - Java
second_title: Aspose.Note Java API
title: Képek kinyerése a OneNote-ból a Document Visitor használatával – Java
url: /hu/java/onenote-document-loading/extract-content-using-document-visitor/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Képek kinyerése a OneNote-ból Dokumentum Látogatóval – Java

## Bevezetés

Aspose.Note for Java megkönnyíti a **képek kinyerését a OneNote** jegyzetfüzetekből, valamint a mögöttes `.one` fájl olvasását Java-ban. Ebben az útmutatóban lépésről lépésre bemutatunk egy komplett, gyakorlati példát, amely megmutatja, hogyan töltsünk be egy OneNote fájlt, járjuk be a struktúráját egy egyedi `DocumentVisitor` segítségével, és nyerjük ki a képeket és a sima szöveget. A végére megtanulod, hogyan **konvertálj OneNote-ot szöveggé**, ha csak a szöveges tartalomra van szükséged.

## Gyors válaszok
- **Milyen könyvtárra van szükségem?** Aspose.Note for Java (letölthető alább).  
- **Kinyerhetek csak képeket?** Igen – implementáld a `VisitImageStart` metódust egy `DocumentVisitor`-ban.  
- **Hogyan olvassak be egy .one fájlt Java-ban?** Használd a `new Document(path, new LoadOptions())`-t.  
- **Szükség van licencre a termeléshez?** Kereskedelmi licenc szükséges a nem‑próba használathoz.  
- **Mely Java verzió támogatott?** JDK 8 vagy újabb.

## Előfeltételek

Mielőtt elkezdenéd, győződj meg róla, hogy rendelkezel:

1. Java Development Kit (JDK) 8 vagy újabb telepítve.  
2. Aspose.Note for Java könyvtár letöltve. Letöltheted **[itt](https://releases.aspose.com/note/java/)**.  
3. Egy OneNote dokumentum (`.one` fájl), amelyből képeket szeretnél kinyerni vagy szöveggé konvertálni.

## Csomagok importálása

Először importáld a szükséges osztályokat az Aspose.Note API-ból.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.DocumentVisitor;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.OutlineGroup;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.Title;
```

## 1. lépés: Egyedi Document Visitor beállítása

Hozz létre egy osztályt, amely kiterjeszti a `DocumentVisitor`-t. Ez az osztály minden egyes csomópontnál meghívódik a OneNote dokumentumban, lehetővé téve a **képek kinyerését a OneNote-ból** és opcionálisan a szöveg összegyűjtését.

```java
public class ExtractOneNoteContentUsingDocumentvisitor extends DocumentVisitor {
    
    final private StringBuilder mBuilder;
    final private boolean mIsSkipText;
    private int nodecount;

    public ExtractOneNoteContentUsingDocumentvisitor() {
        nodecount = 0;
        mIsSkipText = false;
        mBuilder = new StringBuilder();
    }
    
    // Other methods will be implemented here
}
```

## 2. lépés: Látogató metódusok implementálása

Adj hozzá felülírásokat a számodra fontos csomóponttípusokhoz. Az alábbiakban a gazdag szöveget, képeket, címeket, oldalakat, vázlatokat és vázlat elemeket kezeljük. A `VisitImageStart` metódusban történik a képek kinyerése.

```java
// Visitor methods for different types of nodes

public /* override */ void VisitRichTextStart(RichText run) {
    ++nodecount;
    AppendText(run.getText());
}

public /* override */ void VisitDocumentStart(Document document) {
    ++nodecount;
}

public /* override */ void VisitPageStart(Page page) {
    ++nodecount;
}

public /* override */ void VisitTitleStart(Title title) {
    ++nodecount;
}

public /* override */ void VisitImageStart(Image image) {
    ++nodecount;
    // Here you could save the image to disk or process it further
    System.out.println("Found image with size: " + image.getData().length + " bytes");
}

public /* override */ void VisitOutlineGroupStart(OutlineGroup outlineGroup) {
    ++nodecount;
}

public void VisitOutlineStart(Outline outline) {
    ++nodecount;
}

public void VisitOutlineElementStart(OutlineElement outlineElement) {
    ++nodecount;
}
```

### Miért implementáljuk ezeket a metódusokat?

- **Képek kinyerése a OneNote-ból:** A `VisitImageStart` közvetlen hozzáférést biztosít a nyers kép bájtokhoz.  
- **OneNote konvertálása szöveggé:** A `VisitRichTextStart` összegyűjti a szöveges tartalmat, lehetővé téve egy egyszerű **OneNote szöveggé konvertálás** műveletet.  
- **.one fájl olvasása Java-ban:** A látogató minta elvonja a mögöttes `.one` fájl struktúráját, így nem kell magadnak a bináris formátumot elemezni.

## 3. lépés: A látogató futtatása a fő metódusból

Töltsd be a `.one` fájlt, példányosítsd a látogatót, és indítsd el a bejárást.

```java
public static void main(String[] args) throws IOException {
    // Open the document we want to convert.
    String dataDir = "Your Document Directory";
    Document doc = new Document(dataDir + "Sample1.one", new LoadOptions());
    
    // Create an object that inherits from the DocumentVisitor class.
    ExtractOneNoteContentUsingDocumentvisitor myConverter = new ExtractOneNoteContentUsingDocumentvisitor();
    
    // Accept the visitor to start the visiting process.
    doc.accept(myConverter);
    
    // Retrieve the result of the operation.
    System.out.println(myConverter.GetText());   // Text extracted from the notebook
    System.out.println(myConverter.NodeCount()); // Total nodes visited
}
```

## Általános felhasználási esetek

- **Automatizált jelentéskészítés:** Képek és szöveg kinyerése egy OneNote megbeszélés jegyzetfüzetből PDF vagy HTML összefoglaló generálásához.  
- **Tartalom migráció:** Régi OneNote archívumok konvertálása egyszerű szövegfájlokká indexel vagy keresőmotorok számára.  
- **Digitális eszközök kinyerése:** Beágyazott képernyőképek, diagramok vagy fényképek gyűjtése más alkalmazásokban való újrahasználathoz.

## Hibakeresés és tippek

- **Nagy jegyzetfüzetek:** Ha memória problémákba ütközöl, dolgozd fel az oldalakat egyenként a `VisitPageStart` ellenőrzésével, és tölts be oldal‑szintű erőforrásokat csak szükség esetén.  
- **Képformátumok:** Az `Image` objektum nyers bájtokat ad vissza; a mentés előtt esetleg fel kell ismerned a formátumot (PNG, JPEG).  
- **Licenc hibák:** Győződj meg róla, hogy beállítottad az Aspose licencet (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`) a dokumentum betöltése előtt a termelésben.

## Gyakran Ismételt Kérdések

**K: Kinyerhetek specifikus típusú tartalmat a OneNote dokumentumból?**  
V: Igen – csak azokat a látogató metódusokat felülírva, amelyekre szükséged van (pl. `VisitImageStart` képekhez, `VisitRichTextStart` szöveghez).

**K: Az Aspose.Note for Java kompatibilis a OneNote dokumentumok különböző verzióival?**  
V: Teljesen. A könyvtár támogatja az összes főbb OneNote fájlverziót, így nyugodtan **.one fájl Java** projekteket olvashatsz, függetlenül a forrás OneNote verziótól.

**K: Integrálhatom ezt a kinyerési folyamatot a Java alkalmazásomba?**  
V: Igen. A látogató minta zökkenőmentesen működik bármely Java kódbázisban; csak add hozzá a könyvtár JAR-át és hívd meg a fenti példát.

**K: Az Aspose.Note for Java támogatja a komplex OneNote dokumentumok kezelését?**  
V: Igen. A beágyazott vázlatok, beágyazott média és egyedi adatok mind elérhetők a látogató API-n keresztül.

**K: Van valamilyen korlát a feldolgozható OneNote dokumentum méretére?**  
V: Nincs szigorú korlát, de rendkívül nagy jegyzetfüzetek több heap memóriát igényelhetnek; fontold meg az oldalonkénti feldolgozást.

**K: Hogyan konvertáljam a kinyert szöveget egyszerű szövegfájlba?**  
V: Miután a `myConverter.GetText()` egy `String`-et ad vissza, írd ki egy fájlba a szokásos Java I/O-val (`Files.write(Paths.get("output.txt"), text.getBytes());`).

---  

**Last Updated:** 2025-12-04  
**Tested With:** Aspose.Note for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}