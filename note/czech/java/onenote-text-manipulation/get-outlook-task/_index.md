---
title: Získejte Outlook úkol ve OneNotu - Aspose.Note
linktitle: Získejte Outlook úkol ve OneNotu - Aspose.Note
second_title: Aspose.Note Java API
description: Prozkoumejte potenciál Aspose.Note pro Java při extrahování podrobností úloh aplikace Outlook z dokumentů OneNotu bez námahy. Zvyšte svůj vývoj v Javě pomocí této robustní knihovny.
weight: 10
url: /cs/java/onenote-text-manipulation/get-outlook-task/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Získejte Outlook úkol ve OneNotu - Aspose.Note

## Úvod
Vítejte ve světě Aspose.Note for Java – výkonného nástroje, který umožňuje vývojářům Java hladce pracovat se soubory Microsoft OneNote. V tomto podrobném průvodci vás provedeme procesem extrahování informací o úkolu aplikace Outlook z dokumentu OneNote pomocí Aspose.Note for Java.
## Předpoklady
Než se pustíte do výukového programu, ujistěte se, že máte splněny následující předpoklady:
- Java Development Kit (JDK): Ujistěte se, že máte v systému nainstalovanou Javu.
-  Aspose.Note pro Java: Stáhněte a nainstalujte knihovnu Aspose.Note z[stránka ke stažení](https://releases.aspose.com/note/java/).
## Importujte balíčky
Začněte importováním potřebných balíčků do vašeho projektu Java. Na začátek souboru Java přidejte následující řádky:
```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.ITag;
import com.aspose.note.NoteTask;
import com.aspose.note.RichText;
```
## Krok 1: Nastavte svůj projekt
Vytvořte nový projekt Java a zahrňte knihovnu Aspose.Note do závislostí svého projektu. Ujistěte se, že struktura vašeho projektu je uspořádána a že máte vyhrazený adresář pro vaše dokumenty.
## Krok 2: Načtěte dokument OneNotu
K načtení dokumentu OneNote do Aspose.Note použijte následující kód:
```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```
Ujistěte se, že jste nahradili "Váš adresář dokumentů" cestou k vašemu dokumentu OneNotu.
## Krok 3: Načtení uzlů RichText
Extrahujte všechny uzly RichText z dokumentu pomocí následujícího kódu:
```java
List<RichText> nodes = (List<RichText>) doc.getChildNodes(RichText.class);
```
## Krok 4: Iterujte přes každý uzel
Projděte každý uzel RichText a zjistěte, zda obsahuje značku NoteTask:
```java
for (RichText richText : nodes) {
    for (ITag tag : richText.getTags()) {
        if (tag.getClass() == NoteTask.class) {
            // Váš kód pro zpracování NoteTask
        }
    }
}
```
## Krok 5: Načtěte vlastnosti úlohy
Načtěte a vytiskněte různé vlastnosti NoteTask, jako je čas dokončení, čas vytvoření, datum dokončení, stav a ikona:
```java
NoteTask noteTask = (NoteTask) tag;
System.out.println("Completed Time: " + noteTask.getCompletedTime());
System.out.println("Create Time: " + noteTask.getCreationTime());
System.out.println("Due Date: " + noteTask.getDueDate());
System.out.println("Status: " + noteTask.getStatus());
System.out.println("Icon: " + noteTask.getIcon());
```
Tento postup opakujte pro všechny uzly NoteTask v dokumentu.
## Závěr
Gratulujeme! Úspěšně jste se naučili, jak používat Aspose.Note pro Java k extrahování informací o úkolu aplikace Outlook z dokumentu OneNotu. Tato výkonná knihovna otevírá svět možností pro vývojáře v jazyce Java pracující se soubory Microsoft OneNote.
## Nejčastější dotazy
### Otázka: Mohu použít Aspose.Note pro Javu s jinými frameworky Java?
Odpověď: Ano, Aspose.Note for Java je kompatibilní s různými frameworky Java a poskytuje flexibilitu při integraci.
### Otázka: Je k dispozici bezplatná zkušební verze pro Aspose.Note pro Java?
 Odpověď: Ano, můžete prozkoumat bezplatnou zkušební verzi Aspose.Note pro Javu[tady](https://releases.aspose.com/).
### Otázka: Jak mohu získat podporu pro Aspose.Note pro Java?
 A: Navštivte[Fórum Aspose.Note](https://forum.aspose.com/c/note/28) pro podporu komunity nebo prozkoumejte možnosti prémiové podpory.
### Otázka: Kde najdu podrobnou dokumentaci k Aspose.Note pro Javu?
 A: Viz[Aspose.Poznámka pro dokumentaci Java](https://reference.aspose.com/note/java/) pro podrobné informace.
### Otázka: Jak získám dočasnou licenci pro Aspose.Note pro Java?
 A: Získejte dočasnou licenci[tady](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
