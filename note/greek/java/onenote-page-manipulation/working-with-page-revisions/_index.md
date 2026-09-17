---
date: 2026-01-15
description: Μάθετε πώς να παρακολουθείτε τις αλλαγές στο OneNote και να διαχειρίζεστε
  τις αναθεωρήσεις σελίδων σε έγγραφα OneNote χρησιμοποιώντας το Aspose.Note για Java.
  Περιλαμβάνει ένα παράδειγμα σύνοψης αναθεώρησης και πώς να τροποποιήσετε την ημερομηνία
  αναθεώρησης.
linktitle: Working with Page Revisions in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Παρακολούθηση αλλαγών στο OneNote – Διαχείριση εκδόσεων σελίδων με το Aspose.Note
url: /el/java/onenote-page-manipulation/working-with-page-revisions/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Δουλεύοντας με τις Αναθεωρήσεις Σελίδων στο OneNote - Aspose.Note

## Εισαγωγή

Το OneNote είναι ένα ισχυρό εργαλείο για την οργάνωση σημειώσεων και όταν χρειάζεται να **track changes onenote**, η διαχείριση των αναθεωρήσεων σελίδων γίνεται απαραίτητη για αποτελεσματική συνεργασία. Με το Aspose.Note for Java, μπορείτε προγραμματιστικά να χειριστείτε τις αναθεωρήσεις, να δείτε ποιος επεξεργάστηκε μια σελίδα και ακόμη να προσαρμόσετε τις χρονικές σήμανσεις. Αυτό το tutorial σας καθοδηγεί βήμα‑βήμα, από τη φόρτωση ενός εγγράφου μέχρι την ενημέρωση της σύνοψης αναθεώρησης.

## Γρήγορες Απαντήσεις
- **Τι σημαίνει “track changes onenote”;** Αναφέρεται στην παρακολούθηση του ποιος επεξεργάστηκε μια σελίδα OneNote και πότε.
- **Ποια βιβλιοθήκη απαιτείται;** Aspose.Note for Java.
- **Μπορώ να αλλάξω τον συγγραφέα ή την ημερομηνία μιας αναθεώρησης;** Ναι, χρησιμοποιώντας το RevisionSummary API (`modify revision date`).
- **Χρειάζεται αρχείο OneNote εκ των προτέρων;** Ναι, απαιτείται ένα δείγμα αρχείου `.one`.
- **Απαιτείται άδεια για παραγωγική χρήση;** Απαιτείται έγκυρη άδεια Aspose.Note για εμπορική χρήση.

## Τι είναι ένα παράδειγμα σύνοψης αναθεώρησης;
Μια *σύνοψη αναθεώρησης* παρέχει μεταδεδομένα σχετικά με τις πιο πρόσφατες αλλαγές σε μια σελίδα — όνομα συγγραφέα, ώρα τελευταίας τροποποίησης και άλλα στοιχεία. Σε αυτόν τον οδηγό θα ανακτήσουμε και θα εμφανίσουμε αυτές τις πληροφορίες, στη συνέχεια θα δείξουμε πώς να **modify revision date**.

## Γιατί να κάνετε track changes onenote με το Aspose.Note;
- **Συνεργασία:** Δείτε γρήγορα ποιος έκανε τις τελευταίες επεμβάσεις.
- **Έλεγχος:** Διατηρήστε αξιόπιστο ιστορικό αλλαγών για συμμόρφωση.
- **Αυτοματοποίηση:** Ενσωματώστε τη διαχείριση αναθεωρήσεων σε back‑end υπηρεσίες ή εργαλεία μετεγκατάστασης.

## Προαπαιτούμενα

### Περιβάλλον Ανάπτυξης Java
Βεβαιωθείτε ότι έχετε εγκατεστημένο το Java Development Kit (JDK) στο σύστημά σας.

### Βιβλιοθήκη Aspose.Note for Java
Κατεβάστε και εγκαταστήστε τη βιβλιοθήκη Aspose.Note for Java από [here](https://releases.aspose.com/note/java/).

### Έγγραφο OneNote
Διαθέστε ένα δείγμα εγγράφου OneNote για δοκιμές.

## Εισαγωγή Πακέτων

Στο έργο Java σας, εισάγετε τα απαραίτητα πακέτα για εργασία με το Aspose.Note for Java.

```java
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.RevisionSummary;
import java.io.IOException;
import java.util.Calendar;
```

Ας διασπάσουμε το παραδείγμα που δόθηκε σε πολλαπλά βήματα για καλύτερη κατανόηση.

## Βήμα 1: Φόρτωση Εγγράφου OneNote

Πρώτα, φορτώστε το έγγραφο OneNote και αποκτήστε την πρώτη παιδική σελίδα.

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
Page page = document.getFirstChild();
```

## Βήμα 2: Ανάγνωση Σύνοψης Αναθεώρησης Σελίδας

Αναγνώστε τη σύνοψη αναθεώρησης περιεχομένου για τη σελίδα. Αυτή είναι η **revision summary example** που δείχνει ποιος επεξεργάστηκε τελευταία τη σελίδα.

```java
RevisionSummary pageRevisionInfo = page.getPageContentRevisionSummary();
System.out.println(String.format("Author:\t%s\nModified:\t%s",
        pageRevisionInfo.getAuthorMostRecent(),
        pageRevisionInfo.getLastModifiedTime().toString()));
```

## Βήμα 3: Ενημέρωση Σύνοψης Αναθεώρησης Σελίδας

Ενημερώστε τη σύνοψη αναθεώρησης σελίδας με νέο συγγραφέα και νέα ημερομηνία τροποποίησης. Αυτό δείχνει πώς να **modify revision date** προγραμματιστικά.

```java
pageRevisionInfo.setAuthorMostRecent("New Author");
Calendar modifiedDate = Calendar.getInstance();
pageRevisionInfo.setLastModifiedTime(modifiedDate.getTime());
document.save(dataDir + "WorkingWithPageRevisions_out.one");
```

## Συμπέρασμα

Η προγραμματιστική διαχείριση των αναθεωρήσεων σελίδων σε έγγραφα OneNote μπορεί να απλοποιηθεί με το Aspose.Note for Java. Ακολουθώντας τα βήματα του tutorial, μπορείτε αποτελεσματικά να **track changes onenote**, να δείτε λεπτομέρειες αναθεώρησης και ακόμη να **modify revision date** ώστε να ταιριάζει στη ροή εργασίας σας.

## Συχνές Ερωτήσεις

### Ε1: Μπορώ να χρησιμοποιήσω το Aspose.Note for Java με άλλες βιβλιοθήκες Java;

Α: Ναι, το Aspose.Note for Java μπορεί να ενσωματωθεί με άλλες βιβλιοθήκες Java για ενίσχυση λειτουργικότητας.

### Ε2: Υποστηρίζει το Aspose.Note for Java όλες τις εκδόσεις εγγράφων OneNote;

Α: Το Aspose.Note for Java υποστηρίζει διάφορες εκδόσεις εγγράφων OneNote, συμπεριλαμβανομένων των παλαιότερων εκδόσεων.

### Ε3: Είναι το Aspose.Note for Java κατάλληλο για εφαρμογές επιχειρησιακού επιπέδου;

Α: Απόλυτα, το Aspose.Note for Java σχεδιάστηκε για να καλύψει τις ανάγκες εφαρμογών επιχειρησιακού επιπέδου με ισχυρά χαρακτηριστικά και κλιμακωσιμότητα.

### Ε4: Μπορώ να προσαρμόσω τις αναθεωρήσεις σελίδας με το Aspose.Note for Java;

Α: Ναι, μπορείτε να προσαρμόσετε τις αναθεωρήσεις σελίδας σύμφωνα με τις απαιτήσεις σας χρησιμοποιώντας το Aspose.Note for Java.

### Ε5: Πού μπορώ να λάβω υποστήριξη για το Aspose.Note for Java;

Α: Μπορείτε να λάβετε υποστήριξη για το Aspose.Note for Java από το [Aspose.Note forum](https://forum.aspose.com/c/note/28).

---

**Τελευταία Ενημέρωση:** 2026-01-15  
**Δοκιμασμένο Με:** Aspose.Note for Java 24.12  
**Συγγραφέας:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}