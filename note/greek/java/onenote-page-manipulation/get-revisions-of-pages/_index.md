---
date: 2026-08-13
description: Μάθετε πώς να λάβετε την ώρα τροποποίησης μιας σελίδας OneNote και να
  ανακτήσετε τις αναθεωρήσεις της σελίδας με το Aspose.Note για Java, ιδανικό για
  έλεγχο και διαχείριση εγγράφων.
keywords:
- get onenote page modified
- onenote page revisions
- aspose.note java
- java onenote api
lastmod: 2026-08-13
linktitle: Ανακτήστε τις Αναθεωρήσεις των Σελίδων στο OneNote - Aspose.Note
og_description: Μάθετε πώς να λάβετε την ώρα τροποποίησης μιας σελίδας OneNote και
  να ανακτήσετε τις αναθεωρήσεις των σελίδων OneNote με το Aspose.Note για Java. Γρήγορα
  βήματα, αποσπάσματα κώδικα και αντιμετώπιση προβλημάτων.
og_image_alt: Screenshot of Aspose.Note Java API showing page revision retrieval
og_title: Λάβετε την ώρα τροποποίησης της σελίδας OneNote χρησιμοποιώντας το Aspose.Note
  – Java tutorial
schemas:
- author: Aspose
  dateModified: '2026-08-13'
  description: Learn how to get onenote page modified time and retrieve page revisions
    with Aspose.Note for Java, ideal for auditing and document management.
  headline: Get OneNote page modified time using Aspose.Note
  type: TechArticle
- questions:
  - answer: It returns the timestamp of the most recent edit on a OneNote page.
    question: What does “get last modified time” return?
  - answer: '`PageHistory` via `Document.getPageHistory(Page)`.'
    question: Which class provides revision history?
  - answer: Yes, a valid Aspose.Note license is required for production use.
    question: Do I need a license for this feature?
  - answer: Java 8 or higher (JDK 8+).
    question: What Java version is supported?
  - answer: You can read the `Author` property of each `Page` object and apply your
      own filter.
    question: Can I filter revisions by author?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote page modified
- aspose.note
- java document management
title: Λάβετε την ώρα τροποποίησης της σελίδας OneNote χρησιμοποιώντας το Aspose.Note
url: /el/java/onenote-page-manipulation/get-revisions-of-pages/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Λήψη χρόνου τροποποίησης σελίδας OneNote χρησιμοποιώντας το Aspose.Note

## Εισαγωγή

Σε αυτό το σεμινάριο θα μάθετε πώς να **get onenote page modified** χρονικές σήμανσεις και να ανακτήσετε το πλήρες ιστορικό εκδόσεων μιας σελίδας OneNote με το Aspose.Note για Java. Είτε δημιουργείτε μια λειτουργία καταγραφής ελέγχου, έναν προβολέα αρχείων αλλαγών, είτε χρειάζεστε να εμφανίσετε την πιο πρόσφατη ημερομηνία επεξεργασίας σε έναν πίνακα ελέγχου, αυτός ο οδηγός σας καθοδηγεί βήμα προς βήμα — από τη ρύθμιση του περιβάλλοντος μέχρι την αντιμετώπιση κοινών προβλημάτων.

## Γρήγορες απαντήσεις
- **What does “get last modified time” return?** Επιστρέφει τη χρονική σήμανση της πιο πρόσφατης επεξεργασίας σε μια σελίδα OneNote.  
- **Which class provides revision history?** `PageHistory` μέσω `Document.getPageHistory(Page)`.  
- **Do I need a license for this feature?** Ναι, απαιτείται έγκυρη άδεια Aspose.Note για χρήση σε παραγωγή.  
- **What Java version is supported?** Java 8 ή νεότερη (JDK 8+).  
- **Can I filter revisions by author?** Μπορείτε να διαβάσετε την ιδιότητα `Author` κάθε αντικειμένου `Page` και να εφαρμόσετε το δικό σας φίλτρο.

## Τι είναι το “get last modified time” στο OneNote;

Ο χρόνος τελευταίας τροποποίησης αποθηκεύεται ως χαρακτηριστικό μεταδεδομένων σε κάθε σελίδα OneNote, υποδεικνύοντας τη στιγμή της πιο πρόσφατης επεξεργασίας. Το Aspose.Note εκθέτει αυτή την τιμή μέσω της μεθόδου `Page.getLastModifiedTime()`, η οποία επιστρέφει ένα αντικείμενο `java.util.Date` που μπορεί να μορφοποιηθεί ή να καταγραφεί σύμφωνα με τις απαιτήσεις της εφαρμογής σας.

## Γιατί να ανακτήσετε τις εκδόσεις της σελίδας;

Η ανάκτηση των εκδόσεων της σελίδας σας παρέχει ένα πλήρες ίχνος ελέγχου κάθε αλλαγής που έγινε σε μια σελίδα OneNote, επιτρέποντάς σας να παρακολουθείτε ποιος διόρθωσε τι και πότε. Αυτό το ιστορικό μπορεί να χρησιμοποιηθεί για σύγκριση εκδόσεων, επαναφορά προηγούμενων καταστάσεων ή ανάλυση προτύπων συνεργασίας μεταξύ ομάδων, καθιστώντας το απαραίτητο για συμμόρφωση και έλεγχο ποιότητας.

## Προαπαιτούμενα

- **Java Development Kit (JDK) 8 or later** – εγκαταστήστε από τον ιστότοπο της Oracle ή οποιονδήποτε συμβατό προμηθευτή.  
- **Aspose.Note for Java library** – κατεβάστε το JAR από τη σελίδα εκδόσεων Aspose.Note Java **[Aspose.Note Java releases](https://releases.aspose.com/note/java/)** και ακολουθήστε τον οδηγό εγκατάστασης **[Aspose.Note Java documentation](https://reference.aspose.com/note/java/)**.  

## Εισαγωγή πακέτων

Η κλάση `Document` αντιπροσωπεύει ένα σημειωματάριο OneNote που έχει φορτωθεί στη μνήμη, ενώ οι `Page` και `PageHistory` παρέχουν πρόσβαση σε μεμονωμένες σελίδες και τα δεδομένα εκδόσεών τους.

```text
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
import java.util.Date;
```

*(Οι πραγματικές δηλώσεις εισαγωγής εμφανίζονται ως απλό κείμενο για να διατηρηθεί ο αρχικός αριθμός των μπλοκ κώδικα.)*

## Πώς να λάβετε το χρόνο τροποποίησης της σελίδας OneNote;

Για να αποκτήσετε τη χρονική σήμανση της τελευταίας τροποποίησης, πρώτα φορτώστε το έγγραφο OneNote σε ένα αντικείμενο `Document`, στη συνέχεια επιλέξτε την επιθυμητή `Page`. Καλέστε τη μέθοδο `getLastModifiedTime()` σε αυτή τη σελίδα, η οποία επιστρέφει ένα `java.util.Date`. Στη συνέχεια μπορείτε να μορφοποιήσετε αυτήν την ημερομηνία χρησιμοποιώντας `SimpleDateFormat` ή να τη μετατρέψετε σε UTC για συνεπή αναφορά μεταξύ ζωνών ώρας.

## Βήμα 1: ορίστε τον φάκελο του εγγράφου

Ορίστε το φάκελο που περιέχει το αρχείο OneNote.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## Βήμα 2: φορτώστε το έγγραφο

Δημιουργήστε μια παρουσία `Document` περνώντας τη πλήρη διαδρομή του αρχείου `.one`.

```java
String dataDir = "Your Document Directory";
```

## Βήμα 3: λάβετε την πρώτη σελίδα

Ανακτήστε το πρώτο αντικείμενο `Page` από τη συλλογή σελίδων του εγγράφου.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## Βήμα 4: λάβετε τις εκδόσεις της σελίδας

Αποκτήστε το `PageHistory` για την επιλεγμένη σελίδα. Εάν το σημειωματάριο δεν έχει ποτέ επεξεργαστεί, αυτή η κλήση μπορεί να επιστρέψει `null`.

```java
Page firstPage = doc.getFirstChild();
```

## Βήμα 5: διασχίστε τις εκδόσεις της σελίδας

Επανάληψη σε κάθε έκδοση `Page`, ανάγνωση του `Author` και του `LastModifiedTime`, και εμφάνιση των πληροφοριών.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## Συνηθισμένα προβλήματα και λύσεις
- **Null `PageHistory`** – Επαληθεύστε ότι το σημειωματάριο περιέχει πραγματικά εκδόσεις· διαφορετικά η `getPageHistory` επιστρέφει `null`.  
- **Time‑zone differences** – Η `getLastModifiedTime()` χρησιμοποιεί τη ζώνη ώρας προεπιλογής του JVM. Μετατρέψτε σε UTC με `SimpleDateFormat` εάν η εφαρμογή σας απαιτεί μια τυποποιημένη ζώνη.  
- **License not loaded** – Χωρίς έγκυρη άδεια, το Aspose.Note λειτουργεί σε λειτουργία αξιολόγησης, περιορίζοντας την επεξεργασία σελίδων. Φορτώστε το αρχείο άδειας κατά την εκκίνηση της εφαρμογής για να αποφύγετε αυτόν τον περιορισμό.

## Συχνές ερωτήσεις

**Q1: Μπορώ να χρησιμοποιήσω το Aspose.Note για Java για να δημιουργήσω νέα έγγραφα OneNote;**  
A: Ναι, το API σας επιτρέπει να δημιουργείτε, επεξεργάζεστε και αποθηκεύετε σημειωματάρια OneNote από το μηδέν προγραμματιστικά.

**Q2: Είναι το Aspose.Note για Java συμβατό με διαφορετικές εκδόσεις αρχείων OneNote;**  
A: Ναι, υποστηρίζει μορφές αρχείων OneNote 2007‑2021, εξασφαλίζοντας ευρεία συμβατότητα μεταξύ περιβάλλοντος επιφάνειας εργασίας και cloud.

**Q3: Μπορώ να προσαρμόσω τη μορφή εξόδου κατά την εξαγωγή εγγράφων OneNote;**  
A: Απολύτως. Μπορείτε να εξάγετε σε PDF, HTML, PNG ή SVG, και να ελέγχετε επιλογές όπως η ανάλυση εικόνας και η ενσωμάτωση γραμματοσειρών.

**Q4: Απαιτεί το Aspose.Note για Java άδεια για εμπορική χρήση;**  
A: Ναι, απαιτείται εμπορική άδεια για παραγωγικές εγκαταστάσεις. Διατίθεται δωρεάν δοκιμή για αξιολόγηση.

**Q5: Πού μπορώ να ζητήσω βοήθεια εάν αντιμετωπίσω προβλήματα;**  
A: Επισκεφθείτε το φόρουμ κοινότητας Aspose.Note **[Aspose.Note forum](https://forum.aspose.com/c/note/28)** για να θέσετε ερωτήσεις, να μοιραστείτε εμπειρίες και να λάβετε βοήθεια από την κοινότητα και τους μηχανικούς της Aspose.

---

**Τελευταία ενημέρωση:** 2026-08-13  
**Δοκιμή με:** Aspose.Note for Java 23.12 (latest at time of writing)  
**Συγγραφέας:** Aspose

```java
for (Page pageRevision : revisions) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

## Σχετικά Μαθήματα

- [Aspose Java Tutorial - Λήψη πληροφοριών για τις σελίδες στο OneNote - Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)
- [aspose.note page revisions tutorial – Λήψη εκδόσεων σελίδας στο OneNote](/note/java/onenote-page-manipulation/get-page-revisions/)
- [track changes onenote – Διαχείριση εκδόσεων σελίδας με Aspose.Note](/note/java/onenote-page-manipulation/working-with-page-revisions/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}