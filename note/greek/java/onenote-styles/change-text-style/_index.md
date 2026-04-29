---
date: 2026-01-18
description: Μάθετε πώς να ορίζετε το χρώμα γραμματοσειράς Java στο OneNote χρησιμοποιώντας
  το Aspose.Note, να επισημαίνετε κείμενο, να τροποποιείτε το μέγεθος γραμματοσειράς
  και να αποθηκεύετε το OneNote ως PDF. Οδηγός βήμα‑προς‑βήμα με κώδικα.
linktitle: Change Text Style in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Ορισμός χρώματος γραμματοσειράς Java στο OneNote – Aspose.Note
url: /el/java/onenote-styles/change-text-style/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ορισμός Χρώματος Γραμματοσειράς Java στο OneNote – Aspose.Note

## Εισαγωγή

Σε αυτό το tutorial θα ανακαλύψετε πώς να **set font color Java** για κείμενο μέσα σε ένα έγγραφο OneNote με το Aspose.Note for Java API. Θα περάσουμε από τη φόρτωση ενός αρχείου `.one`, την πρόσβαση στους κόμβους RichText, την εφαρμογή χρώματος, επισήμανσης και αλλαγών μεγέθους γραμματοσειράς, και τελικά **saving OneNote as PDF**. Είτε χρειάζεστε **highlight text onenote**, **modify font size onenote**, είτε απλώς να αλλάξετε το συνολικό στυλ κειμένου, τα παρακάτω βήματα σας παρέχουν μια πλήρη, έτοιμη για παραγωγή λύση.

## Γρήγορες Απαντήσεις
- **Can I change the font color of specific words?** Ναι – επαναλάβετε μέσω των αντικειμένων `TextRun` και ορίστε `setFontColor`.
- **Does Aspose.Note let me save OneNote as PDF?** Απολύτως· χρησιμοποιήστε `document.save("output.pdf")`.
- **What Java version is required?** Java 8 ή νεότερη.
- **Is highlighting supported?** Χρησιμοποιήστε `setHighlight(Color)` στο `TextStyle`.
- **Can I convert OneNote to PDF in one line?** Δεν είναι άμεσα, αλλά η μέθοδος `save` διαχειρίζεται τη μετατροπή.

## Τι είναι το “set font color java”; 

Η φράση αναφέρεται στην προγραμματιστική ανάθεση ενός νέου χρώματος γραμματοσειράς σε στοιχεία κειμένου σε ένα αρχείο OneNote χρησιμοποιώντας κώδικα Java. Με το Aspose.Note, αποκτάτε πλήρη έλεγχο πάνω σε χαρακτηριστικά στυλ όπως χρώμα γραμματοσειράς, επισήμανση και μέγεθος χωρίς να ανοίξετε το UI του OneNote.

## Γιατί να αλλάξετε το στυλ κειμένου στο OneNote; 

- **Βελτιωμένη αναγνωσιμότητα** – το χρωματιστό ή επισημασμένο κείμενο τραβά την προσοχή σε βασικά σημεία.  
- **Συνεπής εμπορική ταυτότητα** – επιβάλετε εταιρικά χρώματα σε σημειώσεις συναντήσεων.  
- **Ποιότητα εξαγωγής** – οι μορφοποιημένες σημειώσεις φαίνονται επαγγελματικές όταν **convert onenote to pdf** για κοινή χρήση.  

## Προαπαιτούμενα

1. Βασικές γνώσεις προγραμματισμού Java.  
2. Εγκατεστημένο JDK 8 ή νεότερο.  
3. Η βιβλιοθήκη Aspose.Note for Java προστέθηκε στο έργο σας (Maven/Gradle ή χειροκίνητο JAR).  
4. Ένα δείγμα αρχείου OneNote (`Sample1.one`) για πειραματισμό.  

## Εισαγωγή Πακέτων

Πρώτα, εισάγετε τις κλάσεις που θα χρειαστούμε:

```java
import java.awt.Color;
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.RichText;
import com.aspose.note.TextRun;
import com.aspose.note.TextStyle;
```

## Οδηγός Βήμα‑Βήμα

### Βήμα 1: Φόρτωση του Εγγράφου

```java
// Load the document into Aspose.Note
Document document = new Document("Your Document Directory/Sample1.one");
```

Φορτώνουμε το αρχείο OneNote (`Sample1.one`) ώστε το Aspose.Note να μπορεί να εργαστεί με την εσωτερική του δομή.

### Βήμα 2: Πρόσβαση στους Κόμβους RichText

```java
// Get a particular RichText node
List<RichText> richTextNodes = document.getChildNodes(RichText.class);
RichText richText = richTextNodes.get(0);
```

Τα αντικείμενα `RichText` περιέχουν τις πραγματικές παραγράφους. Ανακτώντας τον πρώτο κόμβο, λαμβάνουμε μια αναφορά στο κείμενο που θέλουμε να μορφοποιήσουμε.

### Βήμα 3: Αλλαγή Στυλ Κειμένου (set font color java)

```java
for (TextRun run : richText.getTextRuns()) {
    // Set font color
    run.getStyle().setFontColor(Color.yellow);
    // Set highlight color
    run.getStyle().setHighlight(Color.blue);
    // Set font size
    run.getStyle().setFontSize(20);
}
```

Μέσα στον βρόχο, **set font color Java** σε κίτρινο, εφαρμόζουμε μια μπλε επισήμανση (δείχνοντας **highlight text onenote**) και αυξάνουμε το μέγεθος στα 20 points, απεικονίζοντας **modify font size onenote**.

### Βήμα 4: Αποθήκευση του Εγγράφου (save onenote as pdf)

```java
document.save("Your Document Directory/ChangeTextStyle_out.pdf");
System.out.printf("File saved: %s\n", "Your Document Directory/ChangeTextStyle_out.pdf");
```

Καλώντας το `save` με επέκταση `.pdf`, γίνεται αυτόματα **convert onenote to pdf**, παρέχοντάς σας ένα έτοιμο προς κοινή χρήση αρχείο.

## Κοινά Προβλήματα & Λύσεις

| Πρόβλημα | Αιτία | Διόρθωση |
|----------|-------|----------|
| Δεν φαίνεται αλλαγή χρώματος | Το έγγραφο ήταν ανοιχτό στο OneNote πριν από την αποθήκευση | Κλείστε το OneNote ή επαναφορτώστε το αρχείο μετά το τέλος της διαδικασίας Java |
| Η επισήμανση δεν εφαρμόστηκε | Χρήση χρώματος που ταιριάζει με το φόντο | Επιλέξτε ένα αντιθετικό `Color` (π.χ., `Color.yellow`) |
| `document.save` ρίχνει `IOException` | Μη έγκυρη διαδρομή εξόδου | Βεβαιωθείτε ότι ο φάκελος υπάρχει και έχετε δικαιώματα εγγραφής |

## Συχνές Ερωτήσεις

**Q: Μπορώ να εφαρμόσω αυτές τις αλλαγές στυλ μόνο σε ορισμένα τμήματα του αρχείου OneNote μου;**  
A: Ναι – φιλτράρετε τους κόμβους `RichText` ανάλογα με τον γονέα τους `Section` ή `Page` πριν την επανάληψη στα `TextRun`s.

**Q: Εκτός από χρώμα, επισήμανση και μέγεθος, ποια άλλη μορφοποίηση μπορεί να διαχειριστεί το Aspose.Note;**  
A: Μπορείτε να αλλάξετε την οικογένεια γραμματοσειράς, έντονη/πλάγια/υπογράμμιση, στοίχιση και ακόμη και το διάστημα παραγράφων.

**Q: Είναι δυνατόν να επεξεργαστείτε πολλαπλά αρχεία OneNote σε παρτίδα;**  
A: Απόλυτα. Τυλίξτε τη λογική φόρτωσης και μορφοποίησης σε έναν βρόχο που επεξεργάζεται κάθε αρχείο `.one` σε έναν φάκελο.

**Q: Υποστηρίζει η βιβλιοθήκη την άμεση αποθήκευση σε άλλες μορφές όπως DOCX;**  
A: Ναι – το Aspose.Note μπορεί να εξάγει σε PDF, DOCX, HTML και σε διάφορες μορφές εικόνας.

**Q: Πού μπορώ να βρω περισσότερα παραδείγματα και αναφορά API;**  
A: Επισκεφθείτε τον επίσημο ιστότοπο τεκμηρίωσης του Aspose.Note, εξερευνήστε την αναφορά API και κατεβάστε τη δωρεάν δοκιμή για πρακτική δοκιμή.

## Συμπέρασμα

Τώρα έχετε ένα πλήρες, ολοκληρωμένο παράδειγμα για το πώς να **set font color Java**, να επισημαίνετε κείμενο, να ρυθμίζετε το μέγεθος γραμματοσειράς και να **save OneNote as PDF** χρησιμοποιώντας το Aspose.Note. Μη διστάσετε να προσαρμόσετε τον κώδικα για να στοχεύετε συγκεκριμένες σελίδες, να εφαρμόζετε υπό όρους μορφοποίηση ή να το ενσωματώσετε σε μεγαλύτερα pipelines επεξεργασίας εγγράφων.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-18  
**Tested With:** Aspose.Note 24.11 for Java  
**Author:** Aspose