---
title: Λάβετε αναθεωρήσεις σελίδων στο OneNote - Aspose.Note
linktitle: Λάβετε αναθεωρήσεις σελίδων στο OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Μάθετε πώς να ανακτάτε αναθεωρήσεις σελίδων στα έγγραφα του OneNote χρησιμοποιώντας το Aspose.Note Java. Ενσωματώστε το στις εφαρμογές σας Java για αποτελεσματική διαχείριση εγγράφων.
weight: 15
url: /el/java/onenote-page-manipulation/get-revisions-of-pages/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Λάβετε αναθεωρήσεις σελίδων στο OneNote - Aspose.Note

## Εισαγωγή

Σε αυτό το σεμινάριο, θα εμβαθύνουμε στις δυνατότητες του Aspose.Note για Java, μιας ισχυρής βιβλιοθήκης που σας δίνει τη δυνατότητα να εργάζεστε με αρχεία Microsoft OneNote απρόσκοπτα στις εφαρμογές σας Java. Συγκεκριμένα, θα εστιάσουμε στον τρόπο ανάκτησης αναθεωρήσεων σελίδων σε ένα έγγραφο του OneNote. Μέχρι το τέλος αυτού του οδηγού, θα έχετε τη γνώση για την αποτελεσματική εξαγωγή αναθεωρήσεων σελίδων, συμπεριλαμβανομένων λεπτομερειών όπως ο χρόνος τελευταίας τροποποίησης, ο χρόνος δημιουργίας, ο τίτλος, το επίπεδο και ο συγγραφέας.

## Προαπαιτούμενα

Πριν προχωρήσετε σε αυτό το σεμινάριο, βεβαιωθείτε ότι έχετε ρυθμίσει τις ακόλουθες προϋποθέσεις:

### Εγκατεστημένο Java Development Kit (JDK).

Βεβαιωθείτε ότι έχετε εγκατεστημένο το Java Development Kit στο σύστημά σας. Μπορείτε να το κατεβάσετε και να το εγκαταστήσετε από τον ιστότοπο της Oracle ή να χρησιμοποιήσετε έναν διαχειριστή πακέτων εάν χρησιμοποιείτε σύστημα που βασίζεται σε Unix.

### Aspose.Note for Java Library

 Κατεβάστε και εγκαταστήστε το Aspose.Note για τη βιβλιοθήκη Java από τον ιστότοπο. Μπορείτε να βρείτε τον σύνδεσμο λήψης[εδώ](https://releases.aspose.com/note/java/) . Ακολουθήστε τις οδηγίες εγκατάστασης που παρέχονται στην τεκμηρίωση[εδώ](https://reference.aspose.com/note/java/).

## Εισαγωγή πακέτων

Για να ξεκινήσετε, εισαγάγετε τα απαραίτητα πακέτα στο έργο σας Java. Αυτά τα πακέτα θα σας επιτρέψουν να αξιοποιήσετε τη λειτουργικότητα που παρέχεται από το Aspose.Note για Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

Τώρα, ας αναλύσουμε το παράδειγμα κώδικα που παρέχεται σε πολλά βήματα για να κατανοήσουμε κάθε στοιχείο και τη λειτουργικότητά του.

## Βήμα 1: Ορισμός καταλόγου εγγράφων

Καθορίστε τον κατάλογο στον οποίο βρίσκεται το έγγραφό σας στο OneNote.

```java
String dataDir = "Your Document Directory";
```

## Βήμα 2: Φορτώστε το έγγραφο

Φορτώστε το έγγραφο του OneNote στο Aspose.Note.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## Βήμα 3: Λήψη πρώτης σελίδας

Ανακτήστε την πρώτη σελίδα από το έγγραφο.

```java
Page firstPage = doc.getFirstChild();
```

## Βήμα 4: Λήψη αναθεωρήσεων σελίδας

Λάβετε το ιστορικό αναθεωρήσεων της σελίδας.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## Βήμα 5: Διασχίζοντας αναθεωρήσεις σελίδας

Επαναλάβετε τη λίστα με τις αναθεωρήσεις της σελίδας και ανακτήστε σχετικές πληροφορίες.

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

## συμπέρασμα

Σε αυτό το σεμινάριο, εξερευνήσαμε τον τρόπο ανάκτησης αναθεωρήσεων σελίδων σε ένα έγγραφο του OneNote χρησιμοποιώντας το Aspose.Note για Java. Ακολουθώντας τον οδηγό βήμα προς βήμα και αξιοποιώντας τον παρεχόμενο παράδειγμα κώδικα, μπορείτε εύκολα να ενσωματώσετε αυτήν τη λειτουργία στις εφαρμογές σας Java, επιτρέποντας την αποτελεσματική διαχείριση των αρχείων OneNote.

## Συχνές ερωτήσεις

### Ε1: Μπορώ να χρησιμοποιήσω το Aspose.Note για Java για τη δημιουργία νέων εγγράφων OneNote;

A1: Ναι, το Aspose.Note για Java παρέχει ολοκληρωμένη υποστήριξη για τη δημιουργία, την ανάγνωση και τον χειρισμό εγγράφων OneNote μέσω προγραμματισμού.

### Ε2: Είναι το Aspose.Note για Java συμβατό με διαφορετικές εκδόσεις αρχείων OneNote;

A2: Ναι, το Aspose.Note για Java υποστηρίζει διάφορες εκδόσεις αρχείων Microsoft OneNote, διασφαλίζοντας τη συμβατότητα σε διαφορετικά περιβάλλοντα.

### Ε3: Μπορώ να προσαρμόσω τη μορφή εξόδου κατά την εξαγωγή εγγράφων OneNote;

A3: Απολύτως, το Aspose.Note για Java προσφέρει ευελιξία στην εξαγωγή εγγράφων OneNote σε διαφορετικές μορφές όπως PDF, HTML και εικόνες, με επιλογές για προσαρμογή.

### Ε4: Το Aspose.Note για Java απαιτεί άδεια για εμπορική χρήση;

A4: Ναι, απαιτείται έγκυρη άδεια χρήσης για εμπορική χρήση του Aspose.Note για Java. Μπορείτε να αποκτήσετε άδεια από τον ιστότοπο Aspose.

### Ε5: Πού μπορώ να αναζητήσω βοήθεια εάν αντιμετωπίζω προβλήματα ή έχω ερωτήσεις σχετικά με το Aspose.Note για Java;

 A5: Για υποστήριξη και βοήθεια, μπορείτε να επισκεφτείτε το φόρουμ Aspose.Note[εδώ](https://forum.aspose.com/c/note/28)όπου μπορείτε να κάνετε ερωτήσεις, να μοιραστείτε εμπειρίες και να αλληλεπιδράσετε με άλλους χρήστες και ειδικούς.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
