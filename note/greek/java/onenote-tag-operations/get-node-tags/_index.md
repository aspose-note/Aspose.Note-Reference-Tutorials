---
date: 2026-02-28
description: Μάθετε πώς να εξάγετε ετικέτες από αρχεία OneNote χρησιμοποιώντας το
  Aspose.Note για Java. Αυτό το σεμινάριο δείχνει πώς να φορτώσετε ένα αρχείο OneNote,
  να λάβετε τις ετικέτες OneNote και να τροποποιήσετε τις ετικέτες OneNote αποδοτικά.
linktitle: How to Extract Tags from OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Πώς να εξάγετε ετικέτες από το OneNote με το Aspose.Note
url: /el/java/onenote-tag-operations/get-node-tags/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να εξάγετε ετικέτες από το OneNote με το Aspose.Note

## Εισαγωγή
Αν χρειάζεστε **πώς να εξάγετε ετικέτες** από ένα έγγραφο OneNote, βρίσκεστε στο σωστό μέρος. Σε αυτόν τον οδηγό θα περάσουμε από τη διαδικασία φόρτωσης ενός αρχείου OneNote, την ανάκτηση των ετικετών OneNote, και ακόμη την τροποποίηση αυτών των ετικετών χρησιμοποιώντας το Aspose.Note για Java. Στο τέλος του σεμιναρίου θα μπορείτε να ενσωματώσετε την εξαγωγή ετικετών σε οποιαδήποτε εφαρμογή Java με σιγουριά.

## Γρήγορες Απαντήσεις
- **Ποια είναι η κύρια κλάση για το άνοιγμα ενός αρχείου OneNote;** `Document`
- **Ποια μέθοδος επιστρέφει όλους τους κόμβους RichText;** `doc.getChildNodes(RichText.class)`
- **Μπορείτε να διαβάσετε την ώρα δημιουργίας ενός NoteTag;** Ναι, μέσω `noteTag.getCreationTime()`
- **Χρειάζομαι άδεια για παραγωγική χρήση;** Ναι, απαιτείται έγκυρη άδεια Aspose.Note
- **Είναι το API συμβατό με Java 8 και νεότερες εκδόσεις;** Απόλυτα, υποστηρίζει σύγχρονες εκδόσεις Java

## Τι σημαίνει “πώς να εξάγετε ετικέτες” στο OneNote;
Η εξαγωγή ετικετών σημαίνει ανάγνωση των μεταδεδομένων (όπως κατάσταση, ετικέτα, εικονίδιο και χρονικές σφραγίδες) που το OneNote προσθέτει σε παραγράφους, κουτιά ελέγχου ή άλλα στοιχεία περιεχομένου. Αυτές οι ετικέτες αποθηκεύονται ως αντικείμενα `NoteTag` μέσα σε κόμβους `RichText`.

## Γιατί να χρησιμοποιήσετε το Aspose.Note για εξαγωγή ετικετών;
- **Δεν απαιτείται εγκατάσταση του OneNote** – εργασία απευθείας με αρχεία .one.
- **Πλήρης έλεγχος** – ανάκτηση, ανάγνωση και τροποποίηση ιδιοτήτων ετικετών προγραμματιστικά.
- **Διαπλατφορμικό** – λειτουργεί σε οποιοδήποτε λειτουργικό σύστημα που υποστηρίζει Java.

## Προαπαιτούμενα
- Ένα περιβάλλον ανάπτυξης Java (JDK 8+).
- Η βιβλιοθήκη Aspose.Note που κατεβάστηκε από [εδώ](https://releases.aspose.com/note/java/).
- Ένα δείγμα εγγράφου OneNote (π.χ., `Sample1.one`) τοποθετημένο σε γνωστό φάκελο.

## Εισαγωγή Πακέτων
Ξεκινήστε εισάγοντας τις κλάσεις που θα χρειαστείτε. Αυτές οι εισαγωγές σας δίνουν πρόσβαση στη διαχείριση εγγράφων, στις διεπαφές ετικετών και στους κόμβους πλούσιου κειμένου.

```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.ITag;
import com.aspose.note.NoteTag;
import com.aspose.note.RichText;
```

## Πώς να φορτώσετε αρχείο OneNote
Το πρώτο βήμα είναι να φορτώσετε το αρχείο OneNote σε ένα αντικείμενο `Document`.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Load the document into Aspose.Note
Document doc = new Document(dataDir + "Sample1.one");
// Get all RichText nodes
List<RichText> nodes = doc.getChildNodes(RichText.class);
// Load the document into Aspose.Note
Document doc = new Document(dataDir + "Sample1.one");
```

> **Συμβουλή:** Κρατήστε το μονοπάτι `dataDir` απόλυτο ή χρησιμοποιήστε `Paths.get(...)` για να αποφύγετε σφάλματα σχετιζόμενα με τα μονοπάτια.

## Πώς να λάβετε ετικέτες OneNote
Μετά τη φόρτωση του εγγράφου, ανακτήστε όλους τους κόμβους `RichText`. Κάθε κόμβος μπορεί να περιέχει μία ή περισσότερες ετικέτες.

```java
// Get all RichText nodes
List<RichText> nodes = doc.getChildNodes(RichText.class);
```

## Επανάληψη σε κάθε κόμβο
Κάντε επανάληψη σε κάθε κόμβο `RichText` για να εξετάσετε τις ετικέτες του.

```java
// Iterate through each node
for (RichText richText : nodes) {
    // Process each node here
}
```

## Ανάκτηση Note Tags (Πώς να τροποποιήσετε ετικέτες OneNote)
Μέσα στον βρόχο, ελέγξτε αν μια ετικέτα είναι `NoteTag`. Αν είναι, μπορείτε να διαβάσετε τις ιδιότητές της — ή να τις τροποποιήσετε εάν χρειάζεται.

```java
for (ITag tag : richText.getTags()) {
    if (tag.getClass() == NoteTag.class) {
        NoteTag noteTag = (NoteTag) tag;
        // Retrieve properties
        System.out.println("Completed Time: " + noteTag.getCompletedTime());
        System.out.println("Create Time: " + noteTag.getCreationTime());
        System.out.println("Font Color: " + noteTag.getFontColor());
        System.out.println("Status: " + noteTag.getStatus());
        System.out.println("Label: " + noteTag.getLabel());
        System.out.println("Icon: " + noteTag.getIcon());
        System.out.println("High Light: " + noteTag.getHighlight());
        // Example of modifying a property
        // noteTag.setLabel("Updated Label");
    }
}
```

> **Προειδοποίηση:** Η τροποποίηση μιας ετικέτας αλλάζει το υποκείμενο έγγραφο. Θυμηθείτε να αποθηκεύσετε το έγγραφο μετά τις αλλαγές.

## Συμπέρασμα
Τώρα γνωρίζετε **πώς να εξάγετε ετικέτες**, πώς να **φορτώσετε αρχείο OneNote**, πώς να **λάβετε ετικέτες OneNote**, και ακόμη πώς να **τροποποιήσετε ετικέτες OneNote** χρησιμοποιώντας το Aspose.Note για Java. Ενσωματώστε αυτά τα αποσπάσματα κώδικα στα δικά σας έργα για να αυτοματοποιήσετε την ανάλυση σημειώσεων, την αναφορά ή τις εργασίες μετεγκατάστασης.

## Συχνές Ερωτήσεις
### Είναι το Aspose.Note συμβατό με όλες τις εκδόσεις του OneNote;
Το Aspose.Note υποστηρίζει διάφορες μορφές αρχείων OneNote, εξασφαλίζοντας συμβατότητα μεταξύ διαφορετικών εκδόσεων.

### Μπορώ να τροποποιήσω τις ανακτημένες ιδιότητες NoteTag;
Ναι, το Aspose.Note επιτρέπει την τροποποίηση και ενημέρωση των ιδιοτήτων NoteTag προγραμματιστικά.

### Υπάρχει διαθέσιμη δοκιμαστική έκδοση για το Aspose.Note;
Απολύτως! Μπορείτε να αποκτήσετε τη δωρεάν δοκιμαστική έκδοση [εδώ](https://releases.aspose.com/).

### Πού μπορώ να βρω ολοκληρωμένη τεκμηρίωση για το Aspose.Note για Java;
Εξερευνήστε την αναλυτική τεκμηρίωση [εδώ](https://reference.aspose.com/note/java/).

### Πώς μπορώ να λάβω υποστήριξη για τυχόν προβλήματα ή ερωτήσεις;
Μεταβείτε στο φόρουμ υποστήριξης [εδώ](https://forum.aspose.com/c/note/28) για βοήθεια από την κοινότητα του Aspose.

## Συχνές Ερωτήσεις
**Q:** *Μπορώ να εξάγω ετικέτες από αρχεία OneNote προστατευμένα με κωδικό;*  
**A:** Ναι, παρέχετε τον κωδικό όταν δημιουργείτε το αντικείμενο `Document`.

**Q:** *Πρέπει να καλέσω μέθοδο αποθήκευσης μετά την τροποποίηση των ετικετών;*  
**A:** Απόλυτα. Χρησιμοποιήστε `doc.save("UpdatedSample.one");` για να διατηρήσετε τις αλλαγές.

**Q:** *Είναι δυνατόν να φιλτράρετε τις ετικέτες κατά κατάσταση;*  
**A:** Μπορείτε να ελέγξετε `noteTag.getStatus()` μέσα στον βρόχο και να επεξεργαστείτε μόνο τις επιθυμητές καταστάσεις.

**Q:** *Τι συμβαίνει αν ένας κόμβος RichText δεν έχει ετικέτες;*  
**A:** `richText.getTags()` επιστρέφει μια κενή συλλογή· ο βρόχος απλώς το παραλείπει.

**Q:** *Μπορώ να επεξεργαστώ μαζικά πολλαπλά αρχεία OneNote;*  
**A:** Τυλίξτε τη λογική που παρουσιάστηκε σε μια ρουτίνα επανάληψης αρχείων και διαχειριστείτε κάθε έγγραφο διαδοχικά.

---

**Τελευταία Ενημέρωση:** 2026-02-28  
**Δοκιμάστηκε Με:** Aspose.Note for Java 24.12  
**Συγγραφέας:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}