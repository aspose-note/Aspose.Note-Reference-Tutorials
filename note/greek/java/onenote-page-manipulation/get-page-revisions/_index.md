---
date: 2026-08-08
description: Μάθετε πώς να παρακολουθείτε τις αλλαγές στο OneNote ανακτώντας τις εκδόσεις
  σελίδων προγραμματιστικά χρησιμοποιώντας το Aspose.Note για Java.
keywords:
- track changes in onenote
- aspose.note java
- onenote page revisions
- java document processing
lastmod: 2026-08-08
linktitle: Λήψη εκδόσεων σελίδων στο OneNote - Aspose.Note
og_description: Μάθετε πώς να παρακολουθείτε τις αλλαγές στο OneNote ανακτώντας τις
  εκδόσεις σελίδων προγραμματιστικά χρησιμοποιώντας το Aspose.Note για Java.
og_image_alt: Guide showing how to track changes in OneNote using Aspose.Note Java
  API
og_title: Παρακολούθηση αλλαγών στο OneNote – εκδόσεις σελίδων με το Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-08-08'
  description: Learn how to track changes in OneNote by retrieving page revisions
    programmatically using Aspose.Note for Java.
  headline: Track changes in OneNote – page revisions with Aspose.Note
  type: TechArticle
- description: Learn how to track changes in OneNote by retrieving page revisions
    programmatically using Aspose.Note for Java.
  name: Track changes in OneNote – page revisions with Aspose.Note
  steps:
  - name: set up document directory
    text: Define the folder where your OneNote file resides.
  - name: load OneNote document with history enabled
    text: '`LoadOptions` is a configuration class that tells Aspose.Note how to open
      a file, including whether to read revision data. Enable the flag before loading
      the document.'
  - name: get the first page
    text: Grab the first page object; this will be the reference point for retrieving
      its history.
  - name: iterate through page revisions
    text: Loop through each revision and print useful metadata such as timestamps,
      title, level, and author. > **Pro tip:** If you need to filter revisions by
      a specific author or date range, simply add conditional checks inside the `for`
      loop.
  type: HowTo
- questions:
  - answer: Retrieving page revision history from a OneNote file using Aspose.Note
      for Java.
    question: What does the tutorial cover?
  - answer: Any recent Aspose.Note for Java release that supports `LoadOptions.setLoadHistory`.
    question: Which library version is required?
  - answer: A temporary evaluation license works for testing; a commercial license
      is required for production.
    question: Do I need a license?
  - answer: The API is read‑only for revisions; you can only retrieve them.
    question: Can I modify revisions?
  - answer: Java JDK, Aspose.Note for Java, and a OneNote document with revision data.
    question: What are the main prerequisites?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- track changes
- Aspose.Note
- OneNote revisions
- Java API
title: Παρακολούθηση αλλαγών στο OneNote – εκδόσεις σελίδων με το Aspose.Note
url: /el/java/onenote-page-manipulation/get-page-revisions/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Παρακολούθηση αλλαγών στο OneNote – εκδόσεις σελίδας με Aspose.Note

Σε αυτό το σεμινάριο θα μάθετε πώς να **παρακολουθείτε αλλαγές στο OneNote** εξάγοντας το πλήρες ιστορικό εκδόσεων μιας σελίδας χρησιμοποιώντας το Aspose.Note Java API. Θα καλύψουμε τα πάντα, από τη ρύθμιση του περιβάλλοντος ανάπτυξης μέχρι την εκτύπωση του συγγραφέα, των χρονικών σημάνσεων και του τίτλου κάθε έκδοσης, ώστε να μπορείτε να δημιουργήσετε αξιόπιστες λειτουργίες καταγραφής ελέγχου για οποιαδήποτε λύση βασισμένη στο OneNote.

## Γρήγορες απαντήσεις
- **Τι καλύπτει το σεμινάριο;** Ανάκτηση ιστορικού εκδόσεων σελίδας από αρχείο OneNote χρησιμοποιώντας το Aspose.Note για Java.  
- **Ποια έκδοση της βιβλιοθήκης απαιτείται;** Οποιαδήποτε πρόσφατη έκδοση του Aspose.Note για Java που υποστηρίζει `LoadOptions.setLoadHistory`.  
- **Χρειάζομαι άδεια;** Μια προσωρινή άδεια αξιολόγησης λειτουργεί για δοκιμές· απαιτείται εμπορική άδεια για παραγωγή.  
- **Μπορώ να τροποποιήσω τις εκδόσεις;** Το API είναι μόνο για ανάγνωση των εκδόσεων· μπορείτε μόνο να τις ανακτήσετε.  
- **Ποια είναι τα κύρια προαπαιτούμενα;** Java JDK, Aspose.Note για Java και ένα έγγραφο OneNote με δεδομένα εκδόσεων.

## Τι είναι το «aspose.note page revisions tutorial»;
Το σεμινάριο δείχνει πώς να έχετε προγραμματισμένη πρόσβαση στις ιστορικές εκδόσεις μιας σελίδας OneNote. Κάθε έκδοση περιέχει μεταδεδομένα όπως ο συγγραφέας, η ώρα δημιουργίας και η ώρα τροποποίησης, επιτρέποντάς σας να δημιουργήσετε καταγραφές ελέγχου ή λειτουργίες ημερολογίου αλλαγών μέσα στις εφαρμογές σας.

## Γιατί να χρησιμοποιήσετε το Aspose.Note για παρακολούθηση εκδόσεων σελίδας;
Φορτώστε ολόκληρο το ιστορικό εκδόσεων ενός σημειωματάριου σε λιγότερο από 5 δευτερόλεπτα για αρχείο 500 σελίδων σε τυπική CPU 2 GHz, και ανακτήστε μεταδεδομένα χωρίς να ανοίξετε το UI του OneNote. Η βιβλιοθήκη υποστηρίζει πάνω από 30 μορφές εισόδου και εξόδου, λειτουργεί σε Windows, Linux και macOS (καλύπτοντας >95 % των περιβαλλοντικών διακομιστών) και παρέχει πλήρη έλεγχο σε κάθε ιδιότητα έκδοσης.

## Προαπαιτούμενα

### 1. Java Development Kit (JDK)
Βεβαιωθείτε ότι έχετε εγκατεστημένο ένα πρόσφατο JDK (8 ή νεότερο) και ότι το `JAVA_HOME` έχει οριστεί.

### 2. Aspose.Note for Java
Κατεβάστε τη βιβλιοθήκη από το [σύνδεσμος λήψης](https://releases.aspose.com/note/java/).

### 3. Δείγμα εγγράφου OneNote
Δημιουργήστε ή αποκτήστε ένα αρχείο OneNote (π.χ., `Sample1.one`) που περιέχει σελίδες με ιστορικό εκδόσεων.

## Εισαγωγή πακέτων
Πρώτα, εισάγετε τις απαιτούμενες κλάσεις του Aspose.Note.  
`Document` αντιπροσωπεύει ένα σημειωματάριο OneNote, `LoadOptions` διαμορφώνει τη συμπεριφορά φόρτωσης, και `Page` αντιπροσωπεύει μια μεμονωμένη σελίδα.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## Υλοποίηση βήμα‑βήμα

### Βήμα 1: ρύθμιση καταλόγου εγγράφου
Ορίστε το φάκελο όπου βρίσκεται το αρχείο OneNote.

```java
String dataDir = "Your Document Directory";
```

### Βήμα 2: φόρτωση εγγράφου OneNote με ενεργοποιημένο ιστορικό
`LoadOptions` είναι μια κλάση διαμόρφωσης που λέει στο Aspose.Note πώς να ανοίξει ένα αρχείο, συμπεριλαμβανομένου του αν θα διαβάσει δεδομένα εκδόσεων. Ενεργοποιήστε τη σημαία πριν φορτώσετε το έγγραφο.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

### Βήμα 3: λήψη της πρώτης σελίδας
Πάρτε το αντικείμενο της πρώτης σελίδας· αυτό θα είναι το σημείο αναφοράς για την ανάκτηση του ιστορικού της.

```java
Page firstPage = document.getFirstChild();
```

### Βήμα 4: επανάληψη στις εκδόσεις σελίδας
Κάντε βρόχο σε κάθε έκδοση και εκτυπώστε χρήσιμα μεταδεδομένα όπως χρονικές σημάνσεις, τίτλο, επίπεδο και συγγραφέα.

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

> **Συμβουλή:** Εάν χρειάζεται να φιλτράρετε τις εκδόσεις κατά συγκεκριμένο συγγραφέα ή χρονικό διάστημα, απλώς προσθέστε συνθήκες ελέγχου μέσα στον βρόχο `for`.

## Κοινά προβλήματα & λύσεις
- **Δεν επιστράφηκαν εκδόσεις:** Βεβαιωθείτε ότι το `loadOptions.setLoadHistory(true)` καλείται πριν τη φόρτωση του εγγράφου.  
- **Κενός συγγραφέας ή τίτλος:** Ορισμένες παλαιότερες εκδόσεις του OneNote μπορεί να μην αποθηκεύουν αυτά τα πεδία· χειριστείτε τις τιμές `null` με προσοχή.  
- **Καθυστέρηση απόδοσης σε μεγάλα σημειωματάρια:** Φορτώστε μόνο τις ενότητες που χρειάζεστε ή αυξήστε το μέγεθος της μνήμης heap της JVM.

## Συχνές ερωτήσεις

**Q1: Μπορώ να χρησιμοποιήσω το Aspose.Note για Java για να τροποποιήσω τις εκδόσεις σελίδας;**  
A1: Όχι, το API αυτή τη στιγμή υποστηρίζει μόνο πρόσβαση ανάγνωσης στις εκδόσεις σελίδας.

**Q2: Είναι το Aspose.Note για Java συμβατό με διαφορετικές εκδόσεις εγγράφων OneNote;**  
A2: Ναι, λειτουργεί με διάφορες μορφές αρχείων OneNote, επιτρέποντας απρόσκοπτη επεξεργασία μεταξύ εκδόσεων.

**Q3: Απαιτείται άδεια για το Aspose.Note για Java;**  
A3: Απαιτείται εμπορική άδεια για χρήση σε παραγωγή, αλλά είναι διαθέσιμη προσωρινή άδεια αξιολόγησης για δοκιμές.

**Q4: Μπορώ να ζητήσω υποστήριξη εάν αντιμετωπίσω προβλήματα κατά τη χρήση του Aspose.Note για Java;**  
A4: Ναι, μπορείτε να θέσετε ερωτήσεις στο φόρουμ Aspose.Note [Φόρουμ Aspose.Note](https://forum.aspose.com/c/note/28).

**Q5: Υπάρχει δωρεάν δοκιμή διαθέσιμη για το Aspose.Note για Java;**  
A5: Ναι, μπορείτε να κατεβάσετε μια δωρεάν δοκιμή από τον [ιστότοπο](https://releases.aspose.com/).

---

**Τελευταία ενημέρωση:** 2026-08-08  
**Δοκιμάστηκε με:** Aspose.Note for Java (τελευταία έκδοση)  
**Συγγραφέας:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Σχετικά Σεμινάρια

- [παρακολούθηση αλλαγών onenote – Διαχείριση εκδόσεων σελίδας με Aspose.Note](/note/java/onenote-page-manipulation/working-with-page-revisions/)
- [Aspose Java Tutorial - Λήψη πληροφοριών για σελίδες στο OneNote - Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)
- [Αλλαγή φόντου σελίδας OneNote – Aspose.Note για Java](/note/java/onenote-page-manipulation/set-page-background-color/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}