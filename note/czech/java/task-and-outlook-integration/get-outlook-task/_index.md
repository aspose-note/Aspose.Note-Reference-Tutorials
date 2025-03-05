---
title: Získejte Outlook úkol ve OneNotu - Aspose.Note
linktitle: Získejte Outlook úkol ve OneNotu - Aspose.Note
second_title: Aspose.Note Java API
description: Prozkoumejte sílu Aspose.Note pro Java při extrahování úloh aplikace Outlook z OneNotu bez námahy. Postupujte podle našeho podrobného průvodce a vylepšete své možnosti zpracování dokumentů.
type: docs
weight: 10
url: /cs/java/task-and-outlook-integration/get-outlook-task/
---
## Úvod
Vítejte v našem komplexním průvodci používáním Aspose.Note pro Java k bezproblémovému načítání úloh Outlooku ve OneNotu. Aspose.Note je výkonné Java API, které umožňuje vývojářům bez námahy pracovat se soubory Microsoft OneNote. V tomto kurzu vás krok za krokem provedeme procesem extrahování úloh aplikace Outlook z dokumentu OneNotu.
## Předpoklady
Než se pustíme do výukového programu, ujistěte se, že máte splněny následující předpoklady:
- Vývojové prostředí Java: Ujistěte se, že máte na svém počítači nastavené vývojové prostředí Java.
-  Knihovna Aspose.Note: Stáhněte a nainstalujte knihovnu Aspose.Note for Java. Knihovnu najdete[tady](https://releases.aspose.com/note/java/).
## Importujte balíčky
Chcete-li začít, importujte potřebné balíčky do svého projektu Java. Přidejte do kódu následující řádky:
```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.ITag;
import com.aspose.note.NoteTask;
import com.aspose.note.RichText;

```
Nyní si tento proces rozdělíme na zvládnutelné kroky:
## Krok 1: Nastavte adresář dokumentů
Definujte adresář, kde se nachází váš dokument OneNotu:
```java
String dataDir = "Your Document Directory";
```
## Krok 2: Načtěte dokument OneNotu
Načtěte dokument OneNotu pomocí Aspose.Note:
```java
Document doc = new Document(dataDir + "Sample1.one");
```
## Krok 3: Získejte všechny uzly RichText
Načíst všechny uzly RichText z dokumentu:
```java
List<RichText> nodes = (List<RichText>) doc.getChildNodes(RichText.class);
```
## Krok 4: Iterujte přes každý uzel
Iterujte každý uzel RichText a zkontrolujte značky NoteTask:
```java
for (RichText richText : nodes) {
    for (ITag tag : richText.getTags()) {
        if (tag.getClass() == NoteTask.class) {
            NoteTask noteTask = (NoteTask) tag;
            
            // Načíst vlastnosti
            System.out.println("Completed Time: " + noteTask.getCompletedTime());
            System.out.println("Create Time: " + noteTask.getCreationTime());
            System.out.println("Due Date: " + noteTask.getDueDate());
            System.out.println("Status: " + noteTask.getStatus());
            System.out.println("Icon: " + noteTask.getIcon());
        }
    }
}
```
## Závěr
Gratulujeme! Úspěšně jste se naučili používat Aspose.Note pro Java k načítání úloh Outlooku ve OneNotu. Toto výkonné API zjednodušuje proces, činí jej efektivním a přívětivým pro vývojáře.
## Nejčastější dotazy
### Je Aspose.Note kompatibilní se všemi verzemi OneNotu?
Aspose.Note podporuje Microsoft OneNote 2010 a novější verze.
### Mohu používat Aspose.Note pro osobní i komerční projekty?
 Ano, Aspose.Note lze použít pro osobní i komerční projekty. Návštěva[tady](https://purchase.aspose.com/buy) prozkoumat možnosti licencování.
### Je k dispozici bezplatná zkušební verze pro Aspose.Note?
 Ano, máte přístup k bezplatné zkušební verzi[tady](https://releases.aspose.com/).
### Jak mohu získat podporu pro Aspose.Note?
 Navštivte[Fórum Aspose.Note](https://forum.aspose.com/c/note/28) za podporu komunity. Pro další pomoc zvažte nákup a[dočasná licence](https://purchase.aspose.com/temporary-license/).
### Jsou k dispozici nějaké vzorové dokumenty OneNotu k testování?
 Vzorové dokumenty naleznete v dokumentaci Aspose.Note[tady](https://reference.aspose.com/note/java/).