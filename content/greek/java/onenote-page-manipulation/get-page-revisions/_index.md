---
title: Λάβετε αναθεωρήσεις σελίδας στο OneNote - Aspose.Note
linktitle: Λάβετε αναθεωρήσεις σελίδας στο OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Μάθετε πώς να ανακτάτε τις αναθεωρήσεις σελίδων στο OneNote χρησιμοποιώντας το Aspose.Note για Java. Ακολουθήστε τον βήμα προς βήμα οδηγό μας για αποτελεσματική παρακολούθηση των αλλαγών.
type: docs
weight: 14
url: /el/java/onenote-page-manipulation/get-page-revisions/
---
## Εισαγωγή

Το OneNote είναι ένα ισχυρό εργαλείο για την οργάνωση και τη διαχείριση των σημειώσεων σας, αλλά μερικές φορές χρειάζεται να παρακολουθείτε τις αλλαγές και τις αναθεωρήσεις που γίνονται στις σελίδες σας. Με το Aspose.Note για Java, μπορείτε εύκολα να ανακτήσετε τις αναθεωρήσεις σελίδων μέσω προγραμματισμού. Σε αυτό το σεμινάριο, θα σας καθοδηγήσουμε στη διαδικασία λήψης αναθεωρήσεων σελίδων στο OneNote χρησιμοποιώντας το Aspose.Note για Java.

## Προαπαιτούμενα

Πριν ξεκινήσουμε, βεβαιωθείτε ότι έχετε τις ακόλουθες προϋποθέσεις:

### 1. Java Development Kit (JDK)

Βεβαιωθείτε ότι έχετε εγκατεστημένο το Java Development Kit (JDK) στο σύστημά σας. Μπορείτε να κάνετε λήψη και εγκατάσταση του JDK από τον ιστότοπο της Oracle.

### 2. Aspose.Note για Java

Κατεβάστε και εγκαταστήστε το Aspose.Note για Java από το[σύνδεσμος λήψης](https://releases.aspose.com/note/java/).

### 3. Δείγμα εγγράφου OneNote

Προετοιμάστε ένα δείγμα εγγράφου OneNote (`Sample1.one`) που περιέχει τις σελίδες από τις οποίες θέλετε να ανακτήσετε τις αναθεωρήσεις.

## Εισαγωγή πακέτων

Αρχικά, πρέπει να εισαγάγετε τα απαραίτητα πακέτα από το Aspose.Note για Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

Τώρα, ας αναλύσουμε το παρεχόμενο παράδειγμα σε πολλά βήματα:

## Βήμα 1: Ρύθμιση καταλόγου εγγράφων

Καθορίστε τη διαδρομή καταλόγου όπου βρίσκεται το έγγραφό σας στο OneNote.

```java
String dataDir = "Your Document Directory";
```

## Βήμα 2: Φορτώστε το έγγραφο OneNote

 Φορτώστε το έγγραφο του OneNote χρησιμοποιώντας`LoadOptions` για να ενεργοποιήσετε το ιστορικό φόρτωσης.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

## Βήμα 3: Λήψη πρώτης σελίδας

Ανακτήστε την πρώτη σελίδα από το φορτωμένο έγγραφο.

```java
Page firstPage = document.getFirstChild();
```

## Βήμα 4: Επανάληψη μέσω αναθεωρήσεων σελίδας

Επαναλάβετε σε κάθε αναθεώρηση σελίδας και ανακτήστε σχετικές πληροφορίες όπως η τελευταία τροποποίηση του χρόνου, ο χρόνος δημιουργίας, ο τίτλος, το επίπεδο και ο συγγραφέας.

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

## συμπέρασμα

Σε αυτό το σεμινάριο, μάθαμε πώς να ανακτούμε τις αναθεωρήσεις σελίδων στο OneNote χρησιμοποιώντας το Aspose.Note για Java. Ακολουθώντας αυτά τα βήματα, μπορείτε να παρακολουθείτε αποτελεσματικά τις αλλαγές που έγιναν στις σελίδες σας στο OneNote μέσω προγραμματισμού.

## Συχνές ερωτήσεις

### Ε1: Μπορώ να χρησιμοποιήσω το Aspose.Note για Java για να τροποποιήσω τις αναθεωρήσεις σελίδων;

A1: Όχι, το Aspose.Note για Java υποστηρίζει αυτήν τη στιγμή την ανάκτηση αναθεωρήσεων σελίδων αλλά όχι την τροποποίησή τους.

### Ε2: Είναι το Aspose.Note για Java συμβατό με διαφορετικές εκδόσεις εγγράφων OneNote;

A2: Ναι, το Aspose.Note για Java υποστηρίζει διάφορες εκδόσεις των εγγράφων OneNote, επιτρέποντάς σας να εργάζεστε με διαφορετικές μορφές αρχείων απρόσκοπτα.

### Ε3: Το Aspose.Note για Java απαιτεί άδεια χρήσης;

A3: Ναι, πρέπει να αγοράσετε άδεια χρήσης για να χρησιμοποιήσετε το Aspose.Note για Java σε εμπορικά έργα. Ωστόσο, μπορείτε επίσης να αποκτήσετε μια προσωρινή άδεια για λόγους αξιολόγησης.

### Ε4: Μπορώ να αναζητήσω υποστήριξη εάν αντιμετωπίσω προβλήματα κατά τη χρήση του Aspose.Note για Java;

 A4: Ναι, μπορείτε να αναζητήσετε υποστήριξη από το φόρουμ Aspose.Note[εδώ](https://forum.aspose.com/c/note/28).

### Ε5: Υπάρχει διαθέσιμη δωρεάν δοκιμή για το Aspose.Note για Java;

 A5: Ναι, μπορείτε να έχετε πρόσβαση σε μια δωρεάν δοκιμή του Aspose.Note για Java από το[δικτυακός τόπος](https://releases.aspose.com/).