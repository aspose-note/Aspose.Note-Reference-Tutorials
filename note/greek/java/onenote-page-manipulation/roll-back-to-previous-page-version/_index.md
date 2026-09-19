---
date: 2026-05-25
description: Μάθετε πώς να επαναφέρετε την προηγούμενη έκδοση του OneNote και να επαναφέρετε
  τις σελίδες OneNote χρησιμοποιώντας το Aspose.Note για Java. Ακολουθήστε αυτόν τον
  οδηγό βήμα‑βήμα για αποτελεσματική διαχείριση εγγράφων.
keywords:
- restore previous onenote version
- how to roll back onenote
- read .one file java
- recover previous onenote page
linktitle: Πώς να Επαναφέρετε Προηγούμενη Έκδοση OneNote – Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-05-25'
  description: Learn how to restore previous OneNote version and roll back OneNote
    pages using Aspose.Note for Java. Follow this step‑by‑step guide for efficient
    document management.
  headline: How to Restore Previous OneNote Version – Aspose.Note
  type: TechArticle
- description: Learn how to restore previous OneNote version and roll back OneNote
    pages using Aspose.Note for Java. Follow this step‑by‑step guide for efficient
    document management.
  name: How to Restore Previous OneNote Version – Aspose.Note
  steps:
  - name: '**Install Java Development Kit (JDK):** Grab the latest JDK from the Oracle
      website or your preferred package manager.'
    text: '**Install Java Development Kit (JDK):** Grab the latest JDK from the Oracle
      website or your preferred package manager.'
  - name: '**Configure Environment Variables:** Set `JAVA_HOME` and update `PATH`
      so the `java` and `javac` commands are reachable from the command line.'
    text: '**Configure Environment Variables:** Set `JAVA_HOME` and update `PATH`
      so the `java` and `javac` commands are reachable from the command line.'
  - name: '**Add Aspose.Note for Java:** Download the library from the [website](https://purchase.aspose.com/buy)
      and add the JAR to your project''s classpath.'
    text: '**Add Aspose.Note for Java:** Download the library from the [website](https://purchase.aspose.com/buy)
      and add the JAR to your project''s classpath.'
  type: HowTo
- questions:
  - answer: Restoring a page to a prior version saved in its history.
    question: What does “roll back” mean for OneNote?
  - answer: '`PageHistory` class in Aspose.Note for Java.'
    question: Which API handles the rollback?
  - answer: A valid Aspose.Note license is required for production use.
    question: Do I need a license?
  - answer: Yes – you can pick any entry from the page’s history list.
    question: Can I choose any previous version?
  - answer: Absolutely; the operation works on individual pages without loading the
      entire notebook into memory.
    question: Is this approach safe for large notebooks?
  type: FAQPage
second_title: Aspose.Note Java API
title: Πώς να Επαναφέρετε Προηγούμενη Έκδοση OneNote – Aspose.Note
url: /el/java/onenote-page-manipulation/roll-back-to-previous-page-version/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να Επαναφέρετε Προηγούμενη Έκδοση OneNote – Aspose.Note

## Εισαγωγή

Αν χρειάζεστε έναν αξιόπιστο, προγραμματιστικό τρόπο για **restore previous OneNote version** όταν διαπράξει τυχαία επεξεργασία, βρίσκεστε στο σωστό μέρος. Σε αυτό το tutorial θα περάσουμε από το Aspose.Note for Java, δείχνοντάς σας ακριβώς πώς να επαναφέρετε μια σελίδα OneNote σε προηγούμενη κατάσταση. Είτε δημιουργείτε μια αυτοματοποιημένη υπηρεσία διαχείρισης σημειώσεων είτε προσθέτετε ένα δίχτυ ασφαλείας για συνεργατικά σημειωματάρια, η δυνατότητα επαναφοράς μιας σελίδας διατηρεί το περιεχόμενό σας ακριβές, αξιόπιστο και έτοιμο για έλεγχο.

## Γρήγορες Απαντήσεις
- **Τι σημαίνει “roll back” για το OneNote;** Επαναφορά μιας σελίδας σε προηγούμενη έκδοση που αποθηκεύτηκε στο ιστορικό της.  
- **Ποιο API διαχειρίζεται το rollback;** Κλάση `PageHistory` στο Aspose.Note for Java.  
- **Χρειάζομαι άδεια;** Απαιτείται έγκυρη άδεια Aspose.Note για χρήση σε παραγωγή.  
- **Μπορώ να επιλέξω οποιαδήποτε προηγούμενη έκδοση;** Ναι – μπορείτε να επιλέξετε οποιαδήποτε καταχώρηση από τη λίστα ιστορικού της σελίδας.  
- **Είναι αυτή η προσέγγιση ασφαλής για μεγάλα σημειωματάρια;** Απολύτως· η λειτουργία εργάζεται σε μεμονωμένες σελίδες χωρίς να φορτώνει ολόκληρο το σημειωματάριο στη μνήμη.

## Τι είναι το “restore previous onenote version”;
**`restore previous onenote version`** αναφέρεται στη διαδικασία ανάκτησης ενός προηγούμενου στιγμιότυπου μιας σελίδας OneNote από το εσωτερικό ιστορικό εκδόσεων και αντικατάστασης του τρέχοντος περιεχομένου της σελίδας με αυτό το στιγμιότυπο. Αυτή η λειτουργία υποστηρίζεται πλήρως από το API `PageHistory` του Aspose.Note και δεν απαιτεί χειροκίνητες ενέργειες undo.

## Γιατί να χρησιμοποιήσετε το Aspose.Note για την επαναφορά σελίδων OneNote;
Το Aspose.Note μπορεί να επεξεργαστεί σημειωματάρια με **χίλιες σελίδες** διατηρώντας τη χρήση μνήμης κάτω από **50 MB** επειδή λειτουργεί σε επίπεδο σελίδας. Υποστηρίζει **30+ OneNote‑συγκεκριμένα χαρακτηριστικά**, συμπεριλαμβανομένης της ανάγνωσης αρχείων `.one`, εξαγωγής μεταδεδομένων και επαναφοράς οποιασδήποτε ιστορικής καταχώρησης. Αυτό το καθιστά ιδανικό για αυτοματοποίηση σε επιχειρησιακό επίπεδο όπου η αξιοπιστία και η απόδοση είναι κρίσιμες.

## Προαπαιτούμενα

Πριν βουτήξουμε στον κώδικα, βεβαιωθείτε ότι έχετε τα παρακάτω έτοιμα:

### Ρύθμιση Περιβάλλοντος Ανάπτυξης Java
1. **Εγκατάσταση Java Development Kit (JDK):** Κατεβάστε το πιο πρόσφατο JDK από την ιστοσελίδα της Oracle ή από τον προτιμώμενο διαχειριστή πακέτων σας.  
2. **Διαμόρφωση Μεταβλητών Περιβάλλοντος:** Ορίστε το `JAVA_HOME` και ενημερώστε το `PATH` ώστε οι εντολές `java` και `javac` να είναι προσβάσιμες από τη γραμμή εντολών.  
3. **Προσθήκη Aspose.Note for Java:** Κατεβάστε τη βιβλιοθήκη από το [website](https://purchase.aspose.com/buy) και προσθέστε το JAR στο classpath του έργου σας.

## Εισαγωγή Πακέτων

Για να αλληλεπιδράσετε με αρχεία OneNote, εισάγετε τις απαραίτητες κλάσεις του Aspose.Note:

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## Πώς να επαναφέρω μια προηγούμενη έκδοση σελίδας OneNote;

Φορτώστε το στοχευόμενο σημειωματάριο, ανακτήστε την επιθυμητή ιστορική καταχώρηση με το `PageHistory`, αφαιρέστε την τρέχουσα σελίδα και προσθέστε ξανά την επιλεγμένη έκδοση στο έγγραφο – όλα σε λιγότερο από δέκα γραμμές κώδικα Java. Αυτή η προσέγγιση εγγυάται ότι μόνο η συγκεκριμένη σελίδα επηρεάζεται, διατηρώντας το υπόλοιπο του σημειωματάριου αμετάβλητο και ελαχιστοποιώντας τη χρήση μνήμης.

## Βήμα 1: Φόρτωση Εγγράφου OneNote

`Document` είναι το αντικείμενο υψηλότερου επιπέδου του Aspose.Note που αντιπροσωπεύει ένα μοναδικό αρχείο OneNote στη μνήμη. Πρώτα δείχνουμε στο φάκελο που περιέχει το αρχείο `.one` και το φορτώνουμε σε μια παρουσία `Document`.

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
```
Πρώτα δείχνουμε στο φάκελο που περιέχει το αρχείο `.one` και το φορτώνουμε σε ένα αντικείμενο `Document`.

## Βήμα 2: Λήψη Ιστορικού Σελίδας

`PageHistory` παρέχει πρόσβαση σε κάθε αποθηκευμένη έκδοση μιας επιλεγμένης σελίδας, ενεργοποιώντας τη δυνατότητα **restore previous onenote version**. Καλώντας το `getHistory()` λαμβάνετε μια λίστα που μπορείτε να διατρέξετε ή να προσπελάσετε άμεσα με δείκτη.

```java
Page page = document.getFirstChild();
PageHistory pageHistory = document.getPageHistory(page);
```
`PageHistory` σας δίνει πρόσβαση σε κάθε αποθηκευμένη έκδοση της επιλεγμένης σελίδας, ενεργοποιώντας τη δυνατότητα **restore previous onenote version**.

## Βήμα 3: Αφαίρεση Τρέχουσας Σελίδας

`Page` αντιπροσωπεύει μια μεμονωμένη σελίδα μέσα σε ένα σημειωματάριο OneNote. Η αφαίρεση της τρέχουσας σελίδας δημιουργεί χώρο για την ιστορική έκδοση που θέλετε να επαναφέρετε.

```java
document.removeChild(page);
```
Αφαιρώντας την τρέχουσα σελίδα δημιουργούμε χώρο για την έκδοση που θέλουμε να επαναφέρουμε.

## Βήμα 4: Προσθήκη Προηγούμενης Έκδοσης Σελίδας

`appendChildLast` προσθέτει έναν κόμβο στο τέλος της συλλογής παιδιών ενός εγγράφου. Εδώ επιλέγουμε την πιο πρόσφατη ιστορική καταχώρηση (μπορείτε να αλλάξετε το δείκτη για να στοχεύσετε οποιαδήποτε παλαιότερη έκδοση) και την προσθέτουμε ξανά στο έγγραφο.

```java
document.appendChildLast(pageHistory.get_Item(pageHistory.size() - 1));
```
Εδώ επιλέγουμε την πιο πρόσφατη ιστορική καταχώρηση (μπορείτε να αλλάξετε το δείκτη για να στοχεύσετε οποιαδήποτε παλαιότερη έκδοση) και την προσθέτουμε ξανά στο έγγραφο.

## Βήμα 5: Αποθήκευση Εγγράφου

Η αποθήκευση γράφει το τροποποιημένο σημειωματάριο πίσω στο δίσκο, δημιουργώντας ένα αρχείο που τώρα περιέχει τη σελίδα που επαναφέρθηκε. Η λειτουργία γράφει μόνο τη σελίδα που άλλαξε, έτσι τα μεγάλα σημειωματάρια παραμένουν γρήγορα στην επεξεργασία.

```java
document.save(dataDir + "RollBackToPreviousPageVersion_out.one");
```
Τέλος, αποθηκεύστε το τροποποιημένο σημειωματάριο. Το αρχείο εξόδου τώρα περιέχει τη σελίδα που επαναφέρθηκε.

## Κοινά Προβλήματα & Συμβουλές
- **Κενό Ιστορικό:** Αν το `pageHistory.size()` επιστρέψει 0, η σελίδα δεν έχει αποθηκευμένες εκδόσεις—βεβαιωθείτε ότι η καταγραφή εκδόσεων είναι ενεργοποιημένη στο OneNote.  
- **Δείκτης Εκτός Ορίων:** Θυμηθείτε ότι η λίστα ιστορικού είναι μηδενική (zero‑based). Προσαρμόστε το δείκτη (`size() - 1`) για να στοχεύσετε την ακριβή έκδοση που χρειάζεστε.  
- **Απόδοση:** Η εργασία με μία μόνο σελίδα αποφεύγει τη φόρτωση ολόκληρου του σημειωματάριου στη μνήμη, διατηρώντας τη λειτουργία γρήγορη ακόμη και για σημειωματάρια με **10.000+ σελίδες**.  
- **Ανάγνωση αρχείων .one σε Java:** Χρησιμοποιήστε `Document.load("path/to/file.one")` για να διαβάσετε ένα αρχείο OneNote· το Aspose.Note υποστηρίζει πλήρως τη μορφή `.one` χωρίς να απαιτείται εγκατάσταση του Microsoft Office.  
- **Ασφαλής Ανάκτηση Προηγούμενης Σελίδας OneNote:** Πάντα δημιουργείτε αντίγραφο ασφαλείας του αρχικού αρχείου `.one` πριν εκτελέσετε μαζικές επαναφορές, ειδικά όταν αυτοματοποιείτε σε πολλά σημειωματάρια.

## Συχνές Ερωτήσεις

**Q1: Μπορώ να επαναφέρω πολλαπλές εκδόσεις μιας σελίδας;**  
A: Ναι, μπορείτε να έχετε πρόσβαση σε όλο το ιστορικό της σελίδας και να επαναφέρετε οποιαδήποτε προηγούμενη έκδοση επιλέγοντας τον κατάλληλο δείκτη από τη λίστα `PageHistory`.

**Q2: Υποστηρίζει το Aspose.Note άλλες γλώσσες προγραμματισμού εκτός της Java;**  
A: Ναι, το Aspose.Note παρέχει βιβλιοθήκες για .NET, C++ και Python, επιτρέποντάς σας να εκτελείτε τις ίδιες λειτουργίες επαναφοράς σε διαφορετικές πλατφόρμες.

**Q3: Είναι το Aspose.Note συμβατό με όλες τις εκδόσεις του OneNote;**  
A: Το Aspose.Note υποστηρίζει όλες τις κύριες μορφές αρχείων OneNote, συμπεριλαμβανομένων των παλαιών αρχείων `.one` και των νεότερων δομών OneNote 2016/365, εξασφαλίζοντας ευρεία συμβατότητα.

**Q4: Μπορώ να αυτοματοποιήσω άλλες εργασίες στο OneNote χρησιμοποιώντας το Aspose.Note;**  
A: Απόλυτα. Το API σας επιτρέπει να προσθέτετε, διαγράφετε και τροποποιείτε προγραμματιστικά ενότητες, σελίδες και ενσωματωμένους πόρους, καθιστώντας το ιδανικό για μαζικές μετα迁ές και προσαρμοσμένες αναφορές.

**Q5: Υπάρχει κοινότητα ή υποστήριξη διαθέσιμη για το Aspose.Note;**  
A: Ναι, μπορείτε να επισκεφθείτε το [Aspose.Note forum](https://forum.aspose.com/c/note/28) για βοήθεια από την κοινότητα ή να επικοινωνήσετε με την αφοσιωμένη ομάδα υποστήριξης του Aspose για εμπορική βοήθεια.

---

**Τελευταία Ενημέρωση:** 2026-05-25  
**Δοκιμή Με:** Aspose.Note for Java (latest release)  
**Συγγραφέας:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Σχετικά Μαθήματα

- [Πώς να Αποθηκεύσετε Έκδοση Σελίδας OneNote – Προώθηση Τρέχουσας Έκδοσης Σελίδας στο OneNote - Aspose.Note](/note/java/onenote-page-manipulation/push-current-page-version/)
- [Aspose Java Tutorial - Λήψη Πληροφοριών για Σελίδες στο OneNote - Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)
- [Λήψη Αριθμού Σελίδων OneNote με Aspose.Note for Java](/note/java/onenote-page-manipulation/get-page-count/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}