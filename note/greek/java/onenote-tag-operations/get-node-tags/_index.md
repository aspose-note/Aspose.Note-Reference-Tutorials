---
date: 2026-10-26
description: Μάθετε πώς να εξάγετε ετικέτες από αρχεία OneNote χρησιμοποιώντας το
  Aspose.Note για Java. Αυτό το tutorial δείχνει πώς να load OneNote αρχείο, να get
  OneNote ετικέτες, και να modify τις OneNote ετικέτες αποδοτικά.
keywords:
- how to extract tags
- Aspose.Note Java
- OneNote tag extraction
- Java OneNote API
lastmod: 2026-10-26
linktitle: Πώς να εξάγετε ετικέτες από το OneNote - Aspose.Note
og_description: Μάθετε πώς να εξάγετε ετικέτες από αρχεία OneNote χρησιμοποιώντας
  το Aspose.Note για Java. Ακολουθήστε step‑by‑step code για να load, read, και modify
  ετικέτες αποδοτικά.
og_image_alt: Screenshot of Java code extracting OneNote tags with Aspose.Note
og_title: Πώς να εξάγετε ετικέτες από το OneNote με το Aspose.Note – οδηγός Java
schemas:
- author: Aspose
  dateModified: '2026-10-26'
  description: Learn how to extract tags from OneNote files using Aspose.Note for
    Java. This tutorial shows how to load OneNote file, get OneNote tags, and modify
    OneNote tags efficiently.
  headline: How to extract tags from OneNote with Aspose.Note
  type: TechArticle
- questions:
  - answer: '`Document`'
    question: What is the primary class for opening a OneNote file?
  - answer: '`doc.getChildNodes(RichText.class)`'
    question: Which method returns all RichText nodes?
  - answer: Yes, via `noteTag.getCreationTime()`
    question: Can you read a NoteTag’s creation time?
  - answer: Yes, a valid Aspose.Note license is required
    question: Do I need a license for production use?
  - answer: Absolutely, it supports modern Java versions
    question: Is the API compatible with Java 8 and later?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- OneNote
- Aspose.Note
- Java tag extraction
- document processing
- note tags
title: Πώς να εξάγετε ετικέτες από το OneNote με το Aspose.Note
url: /el/java/onenote-tag-operations/get-node-tags/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να εξάγετε ετικέτες από το OneNote με το Aspose.Note

## Εισαγωγή
Αν χρειάζεστε **πώς να εξάγετε ετικέτες** από ένα έγγραφο OneNote, βρίσκεστε στο σωστό μέρος. Σε αυτόν τον οδηγό θα περάσουμε από τη διαδικασία φόρτωσης ενός αρχείου OneNote, την απόκτηση ετικετών OneNote, και ακόμη την τροποποίηση αυτών των ετικετών χρησιμοποιώντας το Aspose.Note για Java. Στο τέλος του tutorial θα μπορείτε να ενσωματώσετε την εξαγωγή ετικετών σε οποιαδήποτε εφαρμογή Java με σιγουριά.

## Γρήγορες απαντήσεις
- **Ποια είναι η κύρια κλάση για το άνοιγμα ενός αρχείου OneNote;** `Document`
- **Ποια μέθοδος επιστρέφει όλους τους κόμβους RichText;** `doc.getChildNodes(RichText.class)`
- **Μπορείτε να διαβάσετε την ώρα δημιουργίας ενός NoteTag;** Ναι, μέσω `noteTag.getCreationTime()`
- **Χρειάζομαι άδεια για παραγωγική χρήση;** Ναι, απαιτείται έγκυρη άδεια Aspose.Note
- **Είναι το API συμβατό με Java 8 και νεότερες εκδόσεις;** Απόλυτα, υποστηρίζει σύγχρονες εκδόσεις Java

## Τι είναι η «εξαγωγή ετικετών» στο OneNote;
Η εξαγωγή ετικετών σημαίνει την ανάγνωση των μεταδεδομένων `NoteTag` που είναι συνδεδεμένα με στοιχεία περιεχομένου του OneNote όπως παράγραφοι, πλαίσια ελέγχου ή στοιχεία λίστας. Αυτές οι ετικέτες αποθηκεύουν κατάσταση, ετικέτα, εικονίδιο και χρονικές σφραγίδες, και αντιπροσωπεύονται ως αντικείμενα `NoteTag` μέσα σε κόμβους `RichText`, επιτρέποντάς σας να τις ελέγχετε ή να τις τροποποιείτε προγραμματιστικά.

## Γιατί να χρησιμοποιήσετε το Aspose.Note για εξαγωγή ετικετών;
Μπορείτε να επεξεργαστείτε αρχεία OneNote χωρίς να εγκαταστήσετε την εφαρμογή OneNote για υπολογιστές, μειώνοντας το μέγεθος της ανάπτυξης έως και 150 MB. Η βιβλιοθήκη λειτουργεί σε Windows, macOS και Linux, υποστηρίζοντας Java 8 μέχρι Java 17 LTS, προσφέροντάς σας πραγματική διαπλατφορμική δυνατότητα. Παρέχει επίσης πλήρη πρόσβαση ανάγνωσης/εγγραφής σε πάνω από 50 ιδιότητες σχετικές με ετικέτες, επιτρέποντας μαζική ανάλυση ή σενάρια μετεγκατάστασης.

## Προαπαιτούμενα
- Ένα περιβάλλον ανάπτυξης Java (JDK 8+).
- Βιβλιοθήκη Aspose.Note που έχει ληφθεί από τη [Aspose.Note for Java download page](https://releases.aspose.com/note/java/).
- Ένα δείγμα εγγράφου OneNote (π.χ., `Sample1.one`) τοποθετημένο σε γνωστό φάκελο.

## Εισαγωγή πακέτων
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
Φορτώστε το αρχείο `.one` δημιουργώντας ένα νέο αντικείμενο `Document` με τη διαδρομή του αρχείου, π.χ., `Document doc = new Document(dataDir + "Sample1.one");`. Αυτό διαβάζει το σημειωματάριο στη μνήμη και το προετοιμάζει για λειτουργίες ετικετών.

Η κλάση `Document` αντιπροσωπεύει ένα αρχείο OneNote στη μνήμη και παρέχει μεθόδους για ανάγνωση και τροποποίηση του περιεχομένου του.

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

> **Pro tip:** Κρατήστε τη διαδρομή `dataDir` απόλυτη ή χρησιμοποιήστε `Paths.get(...)` για να αποφύγετε σφάλματα σχετιζόμενα με διαδρομές.

## Πώς να λάβετε ετικέτες OneNote
Ανακτήστε όλους τους κόμβους `RichText` χρησιμοποιώντας `doc.getChildNodes(RichText.class)`, η οποία επιστρέφει μια συλλογή που μπορεί να περιέχει ένα ή περισσότερα αντικείμενα `NoteTag`. Στη συνέχεια μπορείτε να επαναλάβετε αυτή τη συλλογή για να εξετάσετε τις ετικέτες κάθε κόμβου.

Ένας κόμβος `RichText` αντιστοιχεί σε μια παράγραφο ή ένα μπλοκ κειμένου στο OneNote και μπορεί να περιέχει πολλαπλές ετικέτες.

```java
// Get all RichText nodes
List<RichText> nodes = doc.getChildNodes(RichText.class);
```

## Επανάληψη σε κάθε κόμβο
Κάντε βρόχο στη συλλογή `RichText` με ένα for‑each βρόχο, ελέγχοντας τη συλλογή ετικετών κάθε κόμβου για να επεξεργαστείτε τυχόν συνδεδεμένα αντικείμενα `NoteTag`. Μέσα στον βρόχο μπορείτε να διαβάσετε ιδιότητες όπως η κατάσταση ή η ώρα δημιουργίας, ή να αποφασίσετε να τις τροποποιήσετε όπως χρειάζεται.

```java
// Iterate through each node
for (RichText richText : nodes) {
    // Process each node here
}
```

## Ανάκτηση ετικετών σημειώσεων (πώς να τροποποιήσετε ετικέτες OneNote)
Μέσα στον βρόχο κόμβων, χρησιμοποιήστε `richText.getTags()` για να λάβετε τη λίστα ετικετών, φιλτράρετε για στιγμιότυπα `NoteTag`, και στη συνέχεια διαβάστε ή ορίστε ιδιότητες όπως `setStatus` ή `setLabel` πριν αποθηκεύσετε το έγγραφο.

Η κλάση `NoteTag` περιλαμβάνει μια ετικέτα OneNote, εκθέτοντας ιδιότητες όπως κατάσταση, ετικέτα, εικονίδιο, ώρα δημιουργίας και συγγραφέα.

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

> **Warning:** Η τροποποίηση μιας ετικέτας αλλάζει το υποκείμενο έγγραφο. Θυμηθείτε να αποθηκεύσετε το έγγραφο μετά τις αλλαγές.

## Συμπέρασμα
Τώρα γνωρίζετε **πώς να εξάγετε ετικέτες**, πώς να **φορτώσετε ένα αρχείο OneNote**, πώς να **λάβετε ετικέτες OneNote**, και ακόμη πώς να **τροποποιήσετε ετικέτες OneNote** χρησιμοποιώντας το Aspose.Note για Java. Ενσωματώστε αυτά τα αποσπάσματα κώδικα στα δικά σας έργα για αυτοματοποίηση ανάλυσης σημειώσεων, αναφορών ή εργασιών μετεγκατάστασης.

## Συχνές ερωτήσεις
### Είναι το Aspose.Note συμβατό με όλες τις εκδόσεις του OneNote;
Το Aspose.Note υποστηρίζει διάφορες μορφές αρχείων OneNote, εξασφαλίζοντας συμβατότητα με διαφορετικές εκδόσεις.

### Μπορώ να τροποποιήσω τις ανακτημένες ιδιότητες NoteTag;
Ναι, το Aspose.Note σας επιτρέπει να τροποποιήσετε και να ενημερώσετε τις ιδιότητες NoteTag προγραμματιστικά.

### Υπάρχει διαθέσιμη δοκιμαστική έκδοση για το Aspose.Note;
Απόλυτα! Μπορείτε να αποκτήσετε τη δωρεάν δοκιμαστική έκδοση από τη [Aspose free trial download page](https://releases.aspose.com/).

### Πού μπορώ να βρω ολοκληρωμένη τεκμηρίωση για το Aspose.Note για Java;
Εξερευνήστε την λεπτομερή τεκμηρίωση στο [Aspose.Note Java API documentation](https://reference.aspose.com/note/java/).

### Πώς μπορώ να λάβω υποστήριξη για τυχόν προβλήματα ή ερωτήσεις;
Μεταβείτε στο φόρουμ υποστήριξης [Aspose.Note support forum](https://forum.aspose.com/c/note/28) για βοήθεια από την κοινότητα του Aspose.

## Συχνές Ερωτήσεις
**Q:** *Μπορώ να εξάγω ετικέτες από αρχεία OneNote που είναι προστατευμένα με κωδικό πρόσβασης;*  
**A:** Ναι, παρέχετε τον κωδικό πρόσβασης κατά τη δημιουργία του αντικειμένου `Document`.

**Q:** *Πρέπει να καλέσω μια μέθοδο αποθήκευσης μετά την τροποποίηση των ετικετών;*  
**A:** Απόλυτα. Χρησιμοποιήστε `doc.save("UpdatedSample.one");` για να διατηρήσετε τις αλλαγές.

**Q:** *Είναι δυνατόν να φιλτράρετε τις ετικέτες κατά κατάσταση;*  
**A:** Μπορείτε να ελέγξετε `noteTag.getStatus()` μέσα στον βρόχο και να επεξεργαστείτε μόνο τις επιθυμητές καταστάσεις.

**Q:** *Τι συμβαίνει αν ένας κόμβος RichText δεν έχει ετικέτες;*  
**A:** `richText.getTags()` επιστρέφει μια κενή συλλογή· ο βρόχος απλώς το παραλείπει.

**Q:** *Μπορώ να επεξεργαστώ μαζικά πολλαπλά αρχεία OneNote;*  
**A:** Τυλίξτε τη λογική σε μια ρουτίνα επανάληψης αρχείων και χειριστείτε κάθε έγγραφο διαδοχικά.

**Τελευταία ενημέρωση:** 2026-10-26  
**Δοκιμάστηκε με:** Aspose.Note for Java 24.12  
**Συγγραφέας:** Aspose

## Σχετικά Μαθήματα

- [Δημιουργία αντικειμένου Notebook Java – Φόρτωση αρχείου OneNote με επιλογές - Aspose.Note](/note/java/onenote-notebook-operations/load-notebook-file-with-load-options/)
- [Μετατροπή OneNote σε απλό κείμενο – Εξαγωγή όλου του κειμένου με Aspose.Note για Java](/note/java/onenote-text-manipulation/extract-all-text/)
- [Ανάκτηση συνημμένων OneNote χρησιμοποιώντας Aspose.Note για Java](/note/java/onenote-java-integration/retrieve-attachment/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}