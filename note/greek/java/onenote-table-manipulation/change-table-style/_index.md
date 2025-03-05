---
title: Αλλαγή στυλ πίνακα στο OneNote - Aspose.Note
linktitle: Αλλαγή στυλ πίνακα στο OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Βελτιώστε τους πίνακες OneNote χωρίς κόπο με το Aspose.Note για Java. Ακολουθήστε τον βήμα προς βήμα οδηγό μας για να αλλάξετε στυλ πίνακα. Κατεβάστε τη βιβλιοθήκη τώρα!
type: docs
weight: 10
url: /el/java/onenote-table-manipulation/change-table-style/
---
## Εισαγωγή
Το Aspose.Note για Java είναι μια ισχυρή βιβλιοθήκη που επιτρέπει στους προγραμματιστές να χειρίζονται τα αρχεία του OneNote χωρίς κόπο. Σε αυτό το σεμινάριο, θα επικεντρωθούμε στην αλλαγή του στυλ πίνακα σε ένα έγγραφο του OneNote χρησιμοποιώντας το Aspose.Note για Java. Ακολουθήστε τον οδηγό βήμα προς βήμα για να βελτιώσετε την οπτική γοητεία των τραπεζιών σας.
## Προαπαιτούμενα
Πριν ξεκινήσετε, βεβαιωθείτε ότι έχετε τα εξής:
- Περιβάλλον ανάπτυξης Java: Βεβαιωθείτε ότι έχετε ρυθμίσει ένα περιβάλλον ανάπτυξης Java στον υπολογιστή σας.
-  Aspose.Note for Java Library: Κατεβάστε και εγκαταστήστε τη βιβλιοθήκη Aspose.Note για Java από το[σελίδα λήψης](https://releases.aspose.com/note/java/).
- Κατάλογος εγγράφων: Προετοιμάστε έναν κατάλογο για να αποθηκεύσετε τα έγγραφά σας στο OneNote.
## Εισαγωγή πακέτων
Στο έργο σας Java, εισαγάγετε τα απαραίτητα πακέτα για να εργαστείτε με το Aspose.Σημείωση:
```java
import com.aspose.note.*;
import java.awt.Color;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.List;
```
## Βήμα 1: Ρύθμιση του εγγράφου
Φορτώστε το έγγραφο του OneNote στο Aspose.Note και ανακτήστε τη λίστα των κόμβων πίνακα
```java
// Ρυθμίστε το έγγραφο και λάβετε τη λίστα με τους κόμβους του πίνακα
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "ChangeTableStyleIn.one");
List<Table> nodes = document.getChildNodes(Table.class);
```
## Βήμα 2: Ορισμός στυλ γραμμής
Επαναλάβετε σε κάθε πίνακα, ορίζοντας το στυλ για κάθε σειρά, συμπεριλαμβανομένης της επισήμανσης της πρώτης σειράς μετά την κεφαλίδα.

```java
// Ορίστε στυλ σειρών για κάθε πίνακα στο έγγραφο
for (Table table : nodes) {
    setRowStyle(table.getFirstChild(), Color.GRAY, true, true);
    // Επισημάνετε την πρώτη σειρά μετά το κεφάλι.
    boolean flag = false;
    List<TableRow> rows = table.getChildren();
    for (int i = 1; i < rows.size(); ++i) {
        setRowStyle(rows.get(i), flag ? Color.lightGray : new java.awt.Color(-1, true), false, false);
        flag = !flag;
    }
}
```
## Μέθοδος setRowStyle
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
## Βήμα 3: Αποθηκεύστε το έγγραφο
Αποθηκεύστε το τροποποιημένο έγγραφο με τα νέα στυλ πίνακα.
Ακολουθώντας αυτά τα βήματα, μπορείτε εύκολα να αλλάξετε το στυλ πίνακα σε ένα έγγραφο OneNote χρησιμοποιώντας το Aspose.Note για Java.

```java
// Αποθηκεύστε το τροποποιημένο έγγραφο
document.save(Paths.get(dataDir, "ChangeTableStyleOut.one").toString());
```
## συμπέρασμα
Το Aspose.Note για Java απλοποιεί τη διαδικασία χειρισμού αρχείων OneNote. Αξιοποιώντας τις δυνατότητες της βιβλιοθήκης, μπορείτε να βελτιώσετε την οπτική παρουσίαση των τραπεζιών σας χωρίς κόπο.

## Συχνές ερωτήσεις
### Πού μπορώ να βρω την τεκμηρίωση για το Aspose.Note για Java;
 Επισκέψου το[τεκμηρίωση](https://reference.aspose.com/note/java/) για ολοκληρωμένη καθοδήγηση.
### Πώς μπορώ να αποκτήσω μια προσωρινή άδεια χρήσης για το Aspose.Note για Java;
 Ακολουθήστε αυτό[Σύνδεσμος](https://purchase.aspose.com/temporary-license/) για την απόκτηση προσωρινής άδειας.
### Υπάρχει διαθέσιμη δωρεάν δοκιμή για το Aspose.Note για Java;
 Ναι, μπορείτε να κάνετε λήψη μιας δωρεάν δοκιμαστικής έκδοσης από[εδώ](https://releases.aspose.com/).
### Πού μπορώ να λάβω υποστήριξη για το Aspose.Note για Java;
 Γίνε μελος[Aspose.Note φόρουμ](https://forum.aspose.com/c/note/28) να ζητήσει βοήθεια από την κοινότητα.
### Πώς μπορώ να αγοράσω το Aspose.Note για Java;
 Μπορείτε να αγοράσετε τη βιβλιοθήκη[εδώ](https://purchase.aspose.com/buy).