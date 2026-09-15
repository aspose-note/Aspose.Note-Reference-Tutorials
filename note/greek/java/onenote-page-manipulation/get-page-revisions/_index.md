---
date: 2026-01-10
description: Μάθετε το σεμινάριο αναθεωρήσεων σελίδων Aspose.Note για Java – ανακτήστε
  προγραμματιστικά τις αναθεωρήσεις σελίδων του OneNote χρησιμοποιώντας το Aspose.Note.
  Ακολουθήστε τον βήμα‑βήμα οδηγό μας.
linktitle: Get Page Revisions in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Εκπαιδευτικό aspose.note για αναθεωρήσεις σελίδων – Λήψη αναθεωρήσεων σελίδας
  στο OneNote
url: /el/java/onenote-page-manipulation/get-page-revisions/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Λήψη Αναθεωρήσεων Σελίδας στο OneNote - Aspose.Note

Το OneNote είναι μια ισχυρή πλατφόρμα λήψης σημειώσεων, και όταν χρειάζεται να ελέγξετε τις αλλαγές, το **aspose.note page revisions tutorial** σας δείχνει ακριβώς πώς να ανακτήσετε το ιστορικό αναθεωρήσεων με μόνο μερικές γραμμές κώδικα Java. Σε αυτόν τον οδηγό θα περάσουμε από όλα όσα χρειάζεστε — από τη ρύθμιση του περιβάλλοντος μέχρι την εκτύπωση των λεπτομερειών κάθε αναθεώρησης — ώστε να μπορείτε να παρακολουθείτε τις επεξεργασίες, τις συνεισφορές των συγγραφέων και τις χρονικές σφραγίδες με ευκολία.

## Γρήγορες Απαντήσεις
- **Τι καλύπτει ο οδηγός;** Ανάκτηση του ιστορικού αναθεωρήσεων σελίδας από ένα αρχείο OneNote χρησιμοποιώντας το Aspose.Note for Java.  
- **Ποια έκδοση της βιβλιοθήκης απαιτείται;** Οποιαδήποτε πρόσφατη έκδοση του Aspose.Note for Java που υποστηρίζει το `LoadOptions.setLoadHistory`.  
- **Χρειάζομαι άδεια;** Μια προσωρινή άδεια αξιολόγησης λειτουργεί για δοκιμές· απαιτείται εμπορική άδεια για παραγωγή.  
- **Μπορώ να τροποποιήσω τις αναθεωρήσεις;** Το API είναι μόνο για ανάγνωση όσον αφορά τις αναθεωρήσεις· μπορείτε μόνο να τις ανακτήσετε.  
- **Ποιες είναι οι κύριες προαπαιτήσεις;** Java JDK, Aspose.Note for Java, και ένα έγγραφο OneNote με δεδομένα αναθεωρήσεων.

## Τι είναι το “aspose.note page revisions tutorial”;
Ο οδηγός δείχνει πώς να έχετε προγραμματιστική πρόσβαση στις ιστορικές εκδόσεις μιας σελίδας OneNote. Κάθε αναθεώρηση περιέχει μεταδεδομένα όπως ο συγγραφέας, η ώρα δημιουργίας και η ώρα τροποποίησης, επιτρέποντάς σας να δημιουργήσετε μητρώα ελέγχου ή λειτουργίες καταγραφής αλλαγών μέσα στις εφαρμογές σας.

## Γιατί να χρησιμοποιήσετε το Aspose.Note για παρακολούθηση αναθεωρήσεων σελίδας;
- **No UI dependency** – Χωρίς εξάρτηση από UI – λειτουργεί εξ ολοκλήρου σε κώδικα, ιδανικό για υπηρεσίες backend.  
- **Cross‑platform** – Δια‑πλατφόρμα – η Java τρέχει σε Windows, Linux και macOS.  
- **Full control** – Πλήρης έλεγχος – ανακτά κάθε ιδιότητα της αναθεώρησης χωρίς να ανοίγετε το OneNote χειροκίνητα.  
- **Performance** – Απόδοση – η φόρτωση του ιστορικού είναι βελτιστοποιημένη, έτσι ακόμη και μεγάλα σημειωματάρια επεξεργάζονται γρήγορα.

## Προαπαιτήσεις

### 1. Java Development Kit (JDK)
Βεβαιωθείτε ότι έχετε εγκατεστημένο ένα πρόσφατο JDK (8 ή νεότερο) και ότι το `JAVA_HOME` είναι ορισμένο.

### 2. Aspose.Note for Java
Κατεβάστε τη βιβλιοθήκη από το [download link](https://releases.aspose.com/note/java/).

### 3. Δείγμα Εγγράφου OneNote
Δημιουργήστε ή αποκτήστε ένα αρχείο OneNote (π.χ., `Sample1.one`) που περιέχει σελίδες με ιστορικό αναθεωρήσεων.

## Εισαγωγή Πακέτων
Πρώτα, εισάγετε τις απαιτούμενες κλάσεις του Aspose.Note.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## Υλοποίηση Βήμα‑Βήμα

### Βήμα 1: Ρύθμιση Καταλόγου Εγγράφου
Ορίστε το φάκελο όπου βρίσκεται το αρχείο OneNote.

```java
String dataDir = "Your Document Directory";
```

### Βήμα 2: Φόρτωση Εγγράφου OneNote με Ενεργοποιημένο Ιστορικό
Ενεργοποιήστε τη σημαία `LoadOptions` για να ανακτήσετε τα δεδομένα αναθεωρήσεων.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

### Βήμα 3: Λήψη Πρώτης Σελίδας
Πάρτε το αντικείμενο της πρώτης σελίδας· αυτό θα είναι το σημείο αναφοράς για την ανάκτηση του ιστορικού της.

```java
Page firstPage = document.getFirstChild();
```

### Βήμα 4: Επανάληψη Στις Αναθεωρήσεις Σελίδας
Κάντε επανάληψη σε κάθε αναθεώρηση και εκτυπώστε χρήσιμα μεταδεδομένα όπως χρονικές σφραγίδες, τίτλο, επίπεδο και συγγραφέα.

```java
for (Page pageRevision : document.getPageHistory(firstPage)) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

> **Συμβουλή:** Εάν χρειάζεται να φιλτράρετε τις αναθεωρήσεις κατά συγκεκριμένο συγγραφέα ή χρονικό εύρος, απλώς προσθέστε συνθήκες ελέγχου μέσα στον βρόχο `for`.

## Συχνά Προβλήματα & Λύσεις
- **Δεν επιστράφηκαν αναθεωρήσεις:** Βεβαιωθείτε ότι το `loadOptions.setLoadHistory(true)` καλείται πριν από τη φόρτωση του εγγράφου.  
- **Null συγγραφέας ή τίτλος:** Ορισμένες παλαιότερες εκδόσεις του OneNote μπορεί να μην αποθηκεύουν αυτά τα πεδία· διαχειριστείτε τις τιμές `null` με προσοχή.  
- **Καθυστέρηση απόδοσης σε μεγάλα σημειωματάρια:** Φορτώστε μόνο τις ενότητες που χρειάζεστε ή αυξήστε το μέγεθος της μνήμης heap του JVM.

## Συχνές Ερωτήσεις

**Q1: Μπορώ να χρησιμοποιήσω το Aspose.Note for Java για να τροποποιήσω τις αναθεωρήσεις σελίδας;**  
A1: Όχι, το API αυτή τη στιγμή υποστηρίζει μόνο πρόσβαση ανάγνωσης στις αναθεωρήσεις σελίδας.

**Q2: Είναι το Aspose.Note for Java συμβατό με διαφορετικές εκδόσεις εγγράφων OneNote;**  
A2: Ναι, λειτουργεί με διάφορες μορφές αρχείων OneNote, επιτρέποντας απρόσκοπτη επεξεργασία μεταξύ εκδόσεων.

**Q3: Απαιτεί το Aspose.Note for Java άδεια για χρήση;**  
A3: Απαιτείται εμπορική άδεια για παραγωγική χρήση, αλλά είναι διαθέσιμη προσωρινή άδεια αξιολόγησης για δοκιμές.

**Q4: Μπορώ να ζητήσω υποστήριξη εάν αντιμετωπίσω προβλήματα κατά τη χρήση του Aspose.Note for Java;**  
A4: Ναι, μπορείτε να θέσετε ερωτήσεις στο φόρουμ Aspose.Note [εδώ](https://forum.aspose.com/c/note/28).

**Q5: Υπάρχει δωρεάν δοκιμή διαθέσιμη για το Aspose.Note for Java;**  
A5: Ναι, μπορείτε να κατεβάσετε μια δωρεάν δοκιμή από την [ιστοσελίδα](https://releases.aspose.com/).

---

**Τελευταία Ενημέρωση:** 2026-01-10  
**Δοκιμάστηκε Με:** Aspose.Note for Java (latest release)  
**Συγγραφέας:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}