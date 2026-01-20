---
date: 2026-01-20
description: Μάθετε πώς να αλλάζετε το στυλ πίνακα στο OneNote χρησιμοποιώντας το
  Aspose.Note για Java και να ορίζετε τα χρώματα φόντου των γραμμών του πίνακα. Ακολουθήστε
  τον βήμα‑βήμα οδηγό για να εφαρμόσετε χρώμα φόντου, έντονο κείμενο και να αποθηκεύσετε
  το έγγραφο OneNote.
linktitle: Change Table Style in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Πώς να αλλάξετε το στυλ πίνακα στο OneNote με το Aspose.Note
url: /el/java/onenote-table-manipulation/change-table-style/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να Αλλάξετε το Στυλ Πίνακα στο OneNote με το Aspose.Note

## Εισαγωγή
Αν χρειάζεστε **πώς να αλλάξετε το στυλ πίνακα** σε ένα σημειωματάριο OneNote, το Aspose.Note for Java το κάνει παιχνιδάκι. Σε αυτό το tutorial θα περάσουμε από όλη τη διαδικασία — από τη φόρτωση ενός αρχείου OneNote, τον ορισμό χρωμάτων φόντου για τις γραμμές του πίνακα, την εφαρμογή έντονης και πλάγιας μορφοποίησης, μέχρι την τελική αποθήκευση του ενημερωμένου εγγράφου. Στο τέλος θα είστε άνετοι με τη μορφοποίηση πινάκων στο OneNote, θα ξέρετε πώς να εφαρμόζετε χρώμα φόντου στις γραμμές και θα κατανοείτε πώς να αποθηκεύετε το έγγραφο OneNote με τα νέα στυλ.

## Γρήγορες Απαντήσεις
- **Ποια βιβλιοθήκη είναι η καλύτερη για το στυλ πινάκων στο OneNote;** Aspose.Note for Java.  
- **Μπορώ να ορίσω χρώματα φόντου για τις γραμμές του πίνακα;** Ναι, χρησιμοποιώντας τη βοηθητική μέθοδο `setRowStyle`.  
- **Πώς κάνω έντονο κείμενο σε έναν πίνακα OneNote;** Ορίστε τη σημαία `bold` στη `setRowStyle`.  
- **Τι απαιτείται για να αποθηκεύσετε το τροποποιημένο αρχείο;** Καλέστε `document.save(...)` με έγκυρη διαδρομή.  
- **Χρειάζομαι άδεια για παραγωγική χρήση;** Ναι, απαιτείται εμπορική άδεια.

## Τι σημαίνει “πώς να αλλάξετε το στυλ πίνακα” στο OneNote;
Η αλλαγή του στυλ ενός πίνακα σημαίνει την τροποποίηση των χρωμάτων των γραμμών, της μορφοποίησης του κειμένου και της συνολικής εμφάνισης ώστε τα δεδομένα να είναι πιο ευανάγνωστα και οπτικά ελκυστικά. Το Aspose.Note παρέχει ένα ευέλικτο API για τον προγραμματιστικό χειρισμό αυτών των ιδιοτήτων.

## Γιατί να χρησιμοποιήσετε το Aspose.Note για Java;
- **Πλήρης έλεγχος** πάνω στις δομές του OneNote χωρίς χειροκίνητη εργασία UI.  
- **Διαπλατφορμική** υποστήριξη· λειτουργεί σε οποιοδήποτε OS που εκτελεί Java.  
- **Πλούσιες επιλογές μορφοποίησης** όπως χρώματα φόντου, έντονο και πλάγιο κείμενο.  

## Προαπαιτούμενα
- **Περιβάλλον Ανάπτυξης Java** – Εγκατεστημένο JDK 8 ή νεότερο.  
- **Βιβλιοθήκη Aspose.Note for Java** – Κατεβάστε από τη [σελίδα λήψης](https://releases.aspose.com/note/java/).  
- **Κατάλογος Εγγράφων** – Ένας φάκελος όπου θα αποθηκεύονται τα αρχεία `.one` σας.  

## Εισαγωγή Πακέτων
Στο έργο Java σας, εισάγετε τα απαραίτητα πακέτα για εργασία με το Aspose.Note:
```java
import com.aspose.note.*;
import java.awt.Color;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.List;
```

## Βήμα 1: Ρύθμιση του Εγγράφου
Φορτώστε το έγγραφο OneNote στο Aspose.Note και ανακτήστε τη λίστα των κόμβων πίνακα.
```java
// Set up the document and get the list of table nodes
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "ChangeTableStyleIn.one");
List<Table> nodes = document.getChildNodes(Table.class);
```

## Βήμα 2: Ορισμός Στυλ Γραμμών
Διατρέξτε κάθε πίνακα, ορίζοντας το στυλ για κάθε γραμμή, συμπεριλαμβανομένου του τονισμού της πρώτης γραμμής μετά την κεφαλίδα. Αυτό δείχνει **ορισμό φόντου γραμμής πίνακα** και **πώς να εφαρμόσετε χρώμα φόντου**.
```java
// Set row styles for each table in the document
for (Table table : nodes) {
    setRowStyle(table.getFirstChild(), Color.GRAY, true, true);
    // Highlight first row after the head.
    boolean flag = false;
    List<TableRow> rows = table.getChildren();
    for (int i = 1; i < rows.size(); ++i) {
        setRowStyle(rows.get(i), flag ? Color.lightGray : new java.awt.Color(-1, true), false, false);
        flag = !flag;
    }
}
```

## Μέθοδος setRowStyle
Η βοηθητική μέθοδος εφαρμόζει χρώμα φόντου, έντονη και πλάγια μορφοποίηση σε κάθε κελί μιας γραμμής. Εδώ υλοποιείται **πώς να κάνετε έντονο κείμενο στο onenote**.
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

## Βήμα 3: Αποθήκευση του Εγγράφου
Αφού μορφοποιήσετε τους πίνακες, αποθηκεύστε το τροποποιημένο έγγραφο. Αυτό δείχνει **πώς να αποθηκεύσετε έγγραφο onenote** με την νέα μορφοποίηση.
```java
// Save the modified document
document.save(Paths.get(dataDir, "ChangeTableStyleOut.one").toString());
```

## Συμπέρασμα
Το Aspose.Note for Java απλοποιεί τη διαδικασία χειρισμού αρχείων OneNote. Εκμεταλλευόμενοι τις δυνατότητες της βιβλιοθήκης, μπορείτε εύκολα να αλλάζετε τα στυλ πινάκων, να ορίζετε χρώματα φόντου για τις γραμμές, να κάνετε έντονο κείμενο και να αποθηκεύετε το έγγραφο OneNote — όλα με λίγες γραμμές κώδικα.

## Συχνές Ερωτήσεις
### Πού μπορώ να βρω την τεκμηρίωση για το Aspose.Note για Java;
Επισκεφθείτε την [τεκμηρίωση](https://reference.aspose.com/note/java/) για ολοκληρωμένη καθοδήγηση.

### Πώς μπορώ να αποκτήσω προσωρινή άδεια για το Aspose.Note για Java;
Ακολουθήστε αυτόν τον [σύνδεσμο](https://purchase.aspose.com/temporary-license/) για να αποκτήσετε προσωρινή άδεια.

### Υπάρχει δωρεάν δοκιμαστική έκδοση για το Aspose.Note για Java;
Ναι, μπορείτε να κατεβάσετε μια δωρεάν δοκιμαστική έκδοση από [εδώ](https://releases.aspose.com/).

### Πού μπορώ να λάβω υποστήριξη για το Aspose.Note για Java;
Συμμετέχετε στο [φόρουμ Aspose.Note](https://forum.aspose.com/c/note/28) για να ζητήσετε βοήθεια από την κοινότητα.

### Πώς μπορώ να αγοράσω το Aspose.Note για Java;
Μπορείτε να αγοράσετε τη βιβλιοθήκη [εδώ](https://purchase.aspose.com/buy).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Τελευταία Ενημέρωση:** 2026-01-20  
**Δοκιμάστηκε Με:** Aspose.Note for Java 24.11  
**Συγγραφέας:** Aspose  

---