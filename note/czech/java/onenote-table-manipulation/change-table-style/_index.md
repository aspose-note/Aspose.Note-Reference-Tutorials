---
title: Změna stylu tabulky ve OneNotu - Aspose.Note
linktitle: Změna stylu tabulky ve OneNotu - Aspose.Note
second_title: Aspose.Note Java API
description: Vylepšete své tabulky OneNotu bez námahy pomocí Aspose.Note pro Java. Chcete-li změnit styly tabulek, postupujte podle našeho podrobného průvodce. Stáhněte si knihovnu nyní!
type: docs
weight: 10
url: /cs/java/onenote-table-manipulation/change-table-style/
---
## Úvod
Aspose.Note for Java je výkonná knihovna, která vývojářům umožňuje bez námahy manipulovat se soubory OneNote. V tomto tutoriálu se zaměříme na změnu stylu tabulky v dokumentu OneNote pomocí Aspose.Note pro Javu. Postupujte podle pokynů krok za krokem, abyste zvýšili vizuální přitažlivost svých stolů.
## Předpoklady
Než začnete, ujistěte se, že máte na svém místě následující:
- Vývojové prostředí Java: Ujistěte se, že máte na svém počítači nastavené vývojové prostředí Java.
-  Aspose.Note for Java Library: Stáhněte a nainstalujte knihovnu Aspose.Note for Java z[stránka ke stažení](https://releases.aspose.com/note/java/).
- Adresář dokumentů: Připravte adresář pro uložení dokumentů OneNotu.
## Importujte balíčky
Ve svém projektu Java importujte potřebné balíčky pro práci s Aspose. Poznámka:
```java
import com.aspose.note.*;
import java.awt.Color;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.List;
```
## Krok 1: Nastavte dokument
Načtěte dokument OneNotu do Aspose.Note a načtěte seznam uzlů tabulky
```java
// Nastavte dokument a získejte seznam uzlů tabulky
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "ChangeTableStyleIn.one");
List<Table> nodes = document.getChildNodes(Table.class);
```
## Krok 2: Nastavte styly řádků
Iterujte každou tabulku, nastavte styl pro každý řádek, včetně zvýraznění prvního řádku za záhlavím.

```java
// Nastavte styly řádků pro každou tabulku v dokumentu
for (Table table : nodes) {
    setRowStyle(table.getFirstChild(), Color.GRAY, true, true);
    // Zvýrazněte první řádek po hlavě.
    boolean flag = false;
    List<TableRow> rows = table.getChildren();
    for (int i = 1; i < rows.size(); ++i) {
        setRowStyle(rows.get(i), flag ? Color.lightGray : new java.awt.Color(-1, true), false, false);
        flag = !flag;
    }
}
```
## metoda setRowStyle
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
## Krok 3: Uložte dokument
Uložte upravený dokument s novými styly tabulek.
Pomocí těchto kroků můžete snadno změnit styl tabulky v dokumentu OneNotu pomocí Aspose.Note pro Java.

```java
// Uložte upravený dokument
document.save(Paths.get(dataDir, "ChangeTableStyleOut.one").toString());
```
## Závěr
Aspose.Note for Java zjednodušuje proces manipulace se soubory OneNotu. Využitím možností knihovny můžete bez námahy vylepšit vizuální prezentaci vašich stolů.

## Nejčastější dotazy
### Kde najdu dokumentaci k Aspose.Note pro Java?
 Navštivte[dokumentace](https://reference.aspose.com/note/java/) za komplexní návod.
### Jak mohu získat dočasnou licenci pro Aspose.Note pro Java?
 Postupujte podle tohoto[odkaz](https://purchase.aspose.com/temporary-license/) získat dočasnou licenci.
### Je k dispozici bezplatná zkušební verze pro Aspose.Note pro Java?
 Ano, můžete si stáhnout bezplatnou zkušební verzi z[tady](https://releases.aspose.com/).
### Kde mohu získat podporu pro Aspose.Note pro Java?
 Připojte se k[Aspose.Note fórum](https://forum.aspose.com/c/note/28) hledat pomoc od komunity.
### Jak koupím Aspose.Note pro Java?
 Knihovnu si můžete zakoupit[tady](https://purchase.aspose.com/buy).