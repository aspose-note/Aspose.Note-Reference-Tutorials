---
date: 2026-05-25
description: Μάθετε πώς να παρακολουθείτε τις αλλαγές στο OneNote και να διαχειρίζεστε
  τις αναθεωρήσεις σελίδων σε έγγραφα OneNote χρησιμοποιώντας το Aspose.Note για Java.
  Περιλαμβάνει ένα παράδειγμα σύνοψης αναθεώρησης και πώς να τροποποιήσετε την ημερομηνία
  αναθεώρησης.
keywords:
- track changes onenote
- OneNote page revisions
- Aspose.Note Java
- revision summary example
- modify revision date
linktitle: Εργασία με Αναθεωρήσεις Σελίδας στο OneNote - Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-05-25'
  description: Learn how to track changes onenote and manage page revisions in OneNote
    documents using Aspose.Note for Java. Includes a revision summary example and
    how to modify revision date.
  headline: track changes onenote – Manage Page Revisions with Aspose.Note
  type: TechArticle
- questions:
  - answer: It means detecting who edited a OneNote page and when the edit occurred.
    question: What does “track changes onenote” mean?
  - answer: Aspose.Note for Java supplies a full‑featured API for page‑revision handling.
    question: Which library provides this capability?
  - answer: Yes—use the `RevisionSummary` object to set a new author name and modified
      date.
    question: Can I change the author or date of a revision?
  - answer: A sample `.one` file is required; the API works with any OneNote 2010‑2021
      format.
    question: Do I need a OneNote file beforehand?
  - answer: A valid Aspose.Note license must be applied for commercial deployments.
    question: Is a license required for production use?
  type: FAQPage
second_title: Aspose.Note Java API
title: Παρακολούθηση αλλαγών OneNote – Διαχείριση Αναθεωρήσεων Σελίδας με Aspose.Note
url: /el/java/onenote-page-manipulation/working-with-page-revisions/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Εργασία με Αναθεωρήσεις Σελίδων στο OneNote - Aspose.Note

## Εισαγωγή

Το OneNote είναι μια ισχυρή πλατφόρμα λήψης σημειώσεων, και όταν χρειάζεται να **track changes onenote**, η διαχείριση των αναθεωρήσεων σελίδων γίνεται απαραίτητη για αποτελεσματική συνεργασία. Με το Aspose.Note for Java μπορείτε προγραμματιστικά να διαβάζετε ποιος επεξεργάστηκε μια σελίδα, να ανακτάτε χρονικές σφραγίδες και ακόμη να τροποποιείτε αυτές τις χρονικές σφραγίδες. Αυτό το σεμινάριο σας καθοδηγεί στη φόρτωση ενός εγγράφου, την εξαγωγή της σύνοψης αναθεώρησης και την ενημέρωση των πληροφοριών συγγραφέα ή ημερομηνίας — όλα χωρίς να ανοίξετε το OneNote χειροκίνητα.

## Γρήγορες Απαντήσεις
- **Τι σημαίνει “track changes onenote”;** Σημαίνει την ανίχνευση του ποιος επεξεργάστηκε μια σελίδα OneNote και πότε έγινε η επεξεργασία.  
- **Ποια βιβλιοθήκη παρέχει αυτή τη δυνατότητα;** Το Aspose.Note for Java παρέχει ένα πλήρες API για τη διαχείριση αναθεωρήσεων σελίδων.  
- **Μπορώ να αλλάξω τον συγγραφέα ή την ημερομηνία μιας αναθεώρησης;** Ναι—χρησιμοποιήστε το αντικείμενο `RevisionSummary` για να ορίσετε νέο όνομα συγγραφέα και τροποποιημένη ημερομηνία.  
- **Χρειάζομαι αρχείο OneNote εκ των προτέρων;** Απαιτείται ένα δείγμα αρχείου `.one`; το API λειτουργεί με οποιαδήποτε μορφή OneNote 2010‑2021.  
- **Απαιτείται άδεια για χρήση σε παραγωγή;** Πρέπει να εφαρμοστεί μια έγκυρη άδεια Aspose.Note για εμπορικές εκδόσεις.

## Ποιο είναι ένα παράδειγμα σύνοψης αναθεώρησης;

Μια *revision summary* είναι ένα ελαφρύ μπλοκ μεταδεδομένων που αποθηκεύει το όνομα του πιο πρόσφατου επεξεργαστή, την ακριβή ώρα τροποποίησης και μερικές επιπλέον σημαίες. Σας επιτρέπει να εμφανίσετε “last edited by John Doe on 2026‑04‑30 10:15 AM” χωρίς να αναλύσετε ολόκληρο το περιεχόμενο της σελίδας. Συνήθως περιλαμβάνει το εμφανιζόμενο όνομα του επεξεργαστή, την ακριβή ώρα UTC της αλλαγής και ένα μοναδικό αναγνωριστικό αναθεώρησης που μπορεί να χρησιμοποιηθεί για συγχρονισμό.

## Γιατί να παρακολουθείτε τις αλλαγές onenote με το Aspose.Note;

Η χρήση του Aspose.Note για την παρακολούθηση αλλαγών παρέχει έναν προγραμματιστικό τρόπο εξαγωγής δεδομένων αναθεώρησης χωρίς χειροκίνητη επιθεώρηση, επιτρέποντας αυτοματοποιημένες αναφορές, ελέγχους συμμόρφωσης και ενσωμάτωση σε CI pipelines. Το API παρέχει γρήγορη, αποδοτική σε μνήμη πρόσβαση στα μεταδεδομένα αναθεώρησης σε μεγάλα σημειωματάρια και υποστηρίζει επεξεργασία παρτίδων για χιλιάδες σελίδες.

## Προαπαιτούμενα

### Περιβάλλον Ανάπτυξης Java
Εγκαταστήστε το JDK 17 ή νεότερο και ρυθμίστε το IDE σας (IntelliJ IDEA, Eclipse ή VS Code) για ανάπτυξη Java.

### Βιβλιοθήκη Aspose.Note for Java
Κατεβάστε το πιο πρόσφατο πακέτο Aspose.Note for Java από [here](https://releases.aspose.com/note/java/). Προσθέστε το JAR στην classpath του έργου σας.

### Έγγραφο OneNote
Προετοιμάστε ένα αρχείο `.one` που περιέχει τουλάχιστον μία σελίδα που θέλετε να ελέγξετε ή να τροποποιήσετε.

## Εισαγωγή Πακέτων

Η κλάση `Document` αντιπροσωπεύει ένα αρχείο OneNote, το `Page` αντιπροσωπεύει μια μεμονωμένη σελίδα, και το `RevisionSummary` παρέχει μεταδεδομένα για τις πιο πρόσφατες αλλαγές.

```java
import com.aspose.note.*;
import java.util.Date;
```

## Πώς φορτώνω ένα έγγραφο OneNote και αποκτώ πρόσβαση στην πρώτη του σελίδα;

Για να φορτώσετε ένα αρχείο OneNote, δημιουργήστε ένα αντικείμενο `Document` με τη διαδρομή προς το αρχείο .one. Το αντικείμενο `Document` αναλύει τη δομή του αρχείου χωρίς να αποδίδει το UI. Στη συνέχεια, ανακτήστε την πρώτη σελίδα καλώντας `getPages().get_Item(0)`, η οποία επιστρέφει ένα αντικείμενο `Page` που αντιπροσωπεύει το περιεχόμενο και τα μεταδεδομένα της σελίδας. Αυτή η προσέγγιση διατηρεί τη χρήση μνήμης χαμηλή.

```java
Document oneNoteDoc = new Document("sample.one");
Page firstPage = oneNoteDoc.getPages().get_Item(0);
```

## Πώς διαβάζω τη σύνοψη αναθεώρησης της σελίδας;

Προσπελάστε τα μεταδεδομένα αναθεώρησης καλώντας `getRevisionSummary()` στην παρουσία `Page`. Το επιστρεφόμενο αντικείμενο `RevisionSummary` περιέχει πεδία όπως το όνομα του συγγραφέα, η τελευταία χρονική σφραγίδα τροποποίησης και το αναγνωριστικό αναθεώρησης. Μπορείτε να διαβάσετε αυτές τις τιμές με `getAuthor()`, `getLastModifiedTime()` και `getRevisionId()` για να εμφανίσετε ή να καταγράψετε τις πληροφορίες της τελευταίας επεξεργασίας.

```java
RevisionSummary revSummary = firstPage.getRevisionSummary();
System.out.println("Author: " + revSummary.getAuthor());
System.out.println("Last Modified: " + revSummary.getLastModifiedTime());
```

## Πώς μπορώ να ενημερώσω τη σύνοψη αναθεώρησης με νέο συγγραφέα και ημερομηνία;

Δημιουργήστε ή αποκτήστε το υπάρχον `RevisionSummary` από τη σελίδα και τροποποιήστε τις ιδιότητές του. Χρησιμοποιήστε `setAuthor(String)` για να ορίσετε νέο όνομα συγγραφέα και `setLastModifiedTime(Date)` για να θέσετε την επιθυμητή χρονική σφραγίδα (σε UTC). Μετά τις αλλαγές, καλέστε `document.save()` για να γράψετε τα ενημερωμένα δεδομένα αναθεώρησης πίσω στο αρχείο .one.

```java
revSummary.setAuthor("Jane Smith");
revSummary.setLastModifiedTime(new Date()); // sets to current time
oneNoteDoc.save("updated.one");
```

## Συνηθισμένα Παράπλευρα Ζητήματα και Συμβουλές

- **Μην ξεχάσετε να καλέσετε `save()`** μετά την τροποποίηση του `RevisionSummary`; διαφορετικά οι αλλαγές παραμένουν μόνο στη μνήμη.  
- **Οι ζώνες ώρας έχουν σημασία:** Τα αντικείμενα `Date` αποθηκεύονται σε UTC. Μετατρέψτε τις τοπικές ώρες σε UTC εάν χρειάζεστε συνεπή αναφορά μεταξύ περιοχών.  
- **Μεγάλα σημειωματάρια:** Όταν επεξεργάζεστε σημειωματάρια μεγαλύτερα από 200 σελίδες, επαναλάβετε τις σελίδες σε παρτίδες για να διατηρήσετε τη χρήση μνήμης κάτω από 100 MB.

## Συχνές Ερωτήσεις

**Q:** *Μπορώ να χρησιμοποιήσω το Aspose.Note for Java μαζί με άλλες βιβλιοθήκες Java;*  
**A:** Ναι. Το API είναι καθαρά Java και λειτουργεί αβίαστα με βιβλιοθήκες όπως Apache POI, Jackson ή Spring Boot.

**Q:** *Το Aspose.Note υποστηρίζει παλαιότερες μορφές αρχείων OneNote;*  
**A:** Υποστηρίζει όλες τις μορφές OneNote από το 2007 και μετά, καλύπτοντας περισσότερα από 30 έτη ιστορίας εκδόσεων.

**Q:** *Το Aspose.Note είναι κατάλληλο για εφαρμογές επιχειρησιακού μεγέθους;*  
**A:** Απόλυτα. Διαχειρίζεται σημειωματάρια πολλαπλών γιγαμπάιτ, προσφέρει λειτουργίες ασφαλείς για νήματα και έχει άδεια για απεριόριστη παραγωγική χρήση.

**Q:** *Μπορώ να προσαρμόσω τα μεταδεδομένα αναθεώρησης πέρα από τον συγγραφέα και την ημερομηνία;*  
**A:** Το `RevisionSummary` εκθέτει επιπλέον πεδία όπως `RevisionId` και `IsDeleted`; μπορείτε να τα διαβάσετε ή να τα ορίσετε όπως χρειάζεται.

**Q:** *Πού μπορώ να λάβω βοήθεια αν αντιμετωπίσω προβλήματα;*  
**A:** Δημοσιεύστε ερωτήσεις στο επίσημο [Aspose.Note forum](https://forum.aspose.com/c/note/28) όπου τόσο οι μηχανικοί της Aspose όσο και τα μέλη της κοινότητας παρέχουν βοήθεια.

## Συμπέρασμα

Με τη χρήση του Aspose.Note for Java μπορείτε πλήρως να **track changes onenote**, να εξάγετε λεπτομέρειες αναθεώρησης και προγραμματιστικά να τροποποιήσετε ονόματα συγγραφέων ή χρονικές σφραγίδες. Αυτή η δυνατότητα βελτιστοποιεί τη συνεργασία, ικανοποιεί τις απαιτήσεις ελέγχου και ενδυναμώνει αυτοματοποιημένα σενάρια μετανάστευσης ή καθαρισμού για μεγάλα αποθετήρια OneNote.

---

**Τελευταία Ενημέρωση:** 2026-05-25  
**Δοκιμή Με:** Aspose.Note for Java 24.12  
**Συγγραφέας:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
pageRevisionInfo.setAuthorMostRecent("New Author");
Calendar modifiedDate = Calendar.getInstance();
pageRevisionInfo.setLastModifiedTime(modifiedDate.getTime());
document.save(dataDir + "WorkingWithPageRevisions_out.one");
```

## Σχετικά Σεμινάρια

- [aspose.note σεμινάριο αναθεωρήσεων σελίδας – Λήψη Αναθεωρήσεων Σελίδας στο OneNote](/note/java/onenote-page-manipulation/get-page-revisions/)
- [Πώς να τροποποιήσετε το ιστορικό σελίδας onenote με το Aspose.Note](/note/java/onenote-page-manipulation/modify-page-history/)
- [Λήψη Αριθμού Σελίδων OneNote με Aspose.Note for Java](/note/java/onenote-page-manipulation/get-page-count/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

```java
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.RevisionSummary;
import java.io.IOException;
import java.util.Calendar;
```

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
Page page = document.getFirstChild();
```

```java
RevisionSummary pageRevisionInfo = page.getPageContentRevisionSummary();
System.out.println(String.format("Author:\t%s\nModified:\t%s",
        pageRevisionInfo.getAuthorMostRecent(),
        pageRevisionInfo.getLastModifiedTime().toString()));
```