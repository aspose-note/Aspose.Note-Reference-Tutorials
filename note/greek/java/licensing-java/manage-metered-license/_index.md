---
date: 2026-07-05
description: Μάθετε πώς να μετατρέψετε το OneNote σε PDF και να διαχειριστείτε μια
  μετρημένη άδεια σε Java χρησιμοποιώντας το Aspose.Note. Ελέγξτε τη χρήση, παρακολουθήστε
  τα credits και διατηρήστε το κόστος χαμηλό.
keywords:
- convert onenote to pdf
- how to convert onenote
- convert notebook to pdf
linktitle: Διαχείριση Μετρημένης Άδειας για το OneNote σε Java
schemas:
- author: Aspose
  dateModified: '2026-07-05'
  description: Learn how to convert OneNote to PDF and manage a metered license in
    Java using Aspose.Note. Control usage, monitor credits, and keep costs low.
  headline: Convert OneNote to PDF and Manage Metered License in Java
  type: TechArticle
- description: Learn how to convert OneNote to PDF and manage a metered license in
    Java using Aspose.Note. Control usage, monitor credits, and keep costs low.
  name: Convert OneNote to PDF and Manage Metered License in Java
  steps:
  - name: Set Up the Metered License
    text: The `Metered` class activates metered‑license mode for all subsequent Aspose.Note
      operations. You must provide the public and private keys you received from your
      Aspose account. Here we create a `Metered` object and inject the public/private
      keys you received from Aspose. This step activates the met
  - name: Load the OneNote Document and Convert to PDF
    text: 'The `Document` class represents a OneNote notebook in memory. After instantiation,
      you can call `save` with a `.pdf` extension to trigger the conversion. SaveFormat
      is an enumeration that specifies the output format for the document, such as
      PDF. - **Load**: `Document` reads the `.one` file located '
  - name: Check Credit Consumption Before and After Conversion
    text: The `Metered` class also provides methods to query credit usage. These two
      lines print the remaining credit balance and the amount of credit used by the
      conversion. Metered.getConsumptionCredit() returns the remaining credit balance,
      while Metered.getConsumptionQuantity() returns the credits used by
  type: HowTo
- questions:
  - answer: A metered license lets you pay for API usage based on credits, giving
      you fine‑grained cost control.
    question: What is a metered license?
  - answer: Purchase a license from the Aspose website or request a temporary evaluation
      key via your account dashboard.
    question: How do I obtain a metered key for Aspose products?
  - answer: Yes, but all consumption is aggregated under the same key, so monitor
      total usage carefully.
    question: Can I use a metered license across multiple applications?
  - answer: Yes, you can download a free trial from [here](https://releases.aspose.com/).
    question: Is there a free trial for Aspose.Note for Java?
  - answer: Ask questions on the Aspose community forums [here](https://forum.aspose.com/c/note/28).
    question: Where can I get support for Aspose.Note for Java?
  type: FAQPage
second_title: Aspose.Note Java API
title: Μετατροπή OneNote σε PDF και Διαχείριση Μετρημένης Άδειας σε Java
url: /el/java/licensing-java/manage-metered-license/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Μετατροπή OneNote σε PDF και Διαχείριση Μετρημένης Άδειας σε Java

## Εισαγωγή

Σε αυτό το tutorial θα ανακαλύψετε πώς να **μετατρέψετε το OneNote σε PDF** χρησιμοποιώντας μια μετρημένη άδεια με τη βιβλιοθήκη Aspose.Note for Java. Η μετρημένη άδεια σας επιτρέπει να παρακολουθείτε την κατανάλωση πίστωσης σε πραγματικό χρόνο, δίνοντάς σας την ευελιξία να πληρώνετε μόνο για ό,τι χρησιμοποιείτε. Θα περάσουμε από τη διαδικασία από την ρύθμιση των κλειδιών άδειας μέχρι τη φόρτωση ενός αρχείου OneNote, τη μετατροπή του σε PDF και τον έλεγχο της χρήσης των πιστώσεων.

## Γρήγορες Απαντήσεις
- **Τι σημαίνει “convert OneNote to PDF”;** Μετατρέπει ένα αρχείο σημειωματάριου `.one` σε ένα φορητό έγγραφο PDF που διατηρεί τη διάταξη, τις γραμματοσειρές και τις εικόνες.  
- **Ποια βιβλιοθήκη διαχειρίζεται τη μετατροπή;** Η Aspose.Note for Java παρέχει ένα απλό, υψηλής απόδοσης API για αυτήν την εργασία.  
- **Χρειάζομαι άδεια για τη μετατροπή;** Ναι, απαιτείται μια μετρημένη άδεια για χρήση σε παραγωγή και για ακριβή παρακολούθηση πίστωσης.  
- **Πώς μπορώ να παρακολουθήσω τη χρήση;** Καλέστε `Metered.getConsumptionCredit()` και `Metered.getConsumptionQuantity()` πριν και μετά τη μετατροπή.  
- **Απαιτείται κάποια πρόσθετη ρύθμιση;** Απλώς ένα Java JDK και το αρχείο Aspose.Note JAR· Maven ή Gradle μπορούν επίσης να διαχειριστούν την εξάρτηση.

## Τι είναι η “convert OneNote to PDF”; 

**Άμεση απάντηση:** Η μετατροπή OneNote σε PDF διαβάζει το σημειωματάριο `.one`, ισοπεδώνει κάθε σελίδα σε μια σελίδα PDF σταθερής διάταξης και γράφει το αποτέλεσμα σε ένα αρχείο `.pdf` που μπορεί να ανοιχθεί σε οποιαδήποτε συσκευή χωρίς την ανάγκη του OneNote. Αυτή η μετατροπή διατηρεί τη μορφοποίηση του κειμένου, τις ενσωματωμένες εικόνες, τους πίνακες και τα διανυσματικά γραφικά, καθιστώντας το PDF ιδανικό για κοινή χρήση, εκτύπωση ή αρχειοθέτηση.

Η διαδικασία μετατροπής διαχειρίζεται εξ ολοκλήρου από την πλευρά του διακομιστή, επομένως δεν απαιτείται απόδοση στην πλευρά του πελάτη ή λογισμικό τρίτου.

## Γιατί να χρησιμοποιήσετε μια μετρημένη άδεια για αυτήν τη μετατροπή; 

**Άμεση απάντηση:** Μια μετρημένη άδεια χρεώνει ανά πίστωσης που καταναλώνεται, επιτρέποντάς σας να κλιμακώνετε τη χρήση πάνω ή κάτω χωρίς σταθερό κόστος συνδρομής. Αναφέρει τη χρήση ανά δευτερόλεπτο, υποστηρίζει έως 10.000 πίστωσεις ανά μήνα ανά κλειδί και απενεργοποιεί αυτόματα το API όταν οι πίστωσεις εξαντληθούν, αποτρέποντας ανεπιθύμητες υπερπληρωμές. Αυτό το μοντέλο είναι ιδανικό για διαλείπουσες εργασίες ή έργα proof‑of‑concept όπου θέλετε αυστηρό έλεγχο κόστους.

## Προαπαιτούμενα

Πριν προχωρήσουμε, βεβαιωθείτε ότι έχετε:

1. **Java Development Kit (JDK)** – οποιαδήποτε πρόσφατη έκδοση (συνιστάται JDK 11+). Κατεβάστε το από [εδώ](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.Note for Java library** – αποκτήστε το τελευταίο JAR από την [επίσημη ιστοσελίδα](https://releases.aspose.com/note/java/).  

> **Συμβουλή:** Προσθέστε το Aspose.Note JAR στο classpath του έργου σας ή χρησιμοποιήστε ένα εργαλείο κατασκευής όπως Maven/Gradle για τη διαχείριση της εξάρτησης. Οι χρήστες Maven μπορούν να προσθέσουν την ακόλουθη εξάρτηση (αντικαταστήστε το `VERSION` με την πιο πρόσφατη):  

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-note</artifactId>
    <version>VERSION</version>
</dependency>
```

## Εισαγωγή Πακέτων

Οι δηλώσεις import φέρνουν τις κλάσεις Aspose.Note στο έργο Java σας, παρέχοντάς σας πρόσβαση σε άδειες, διαχείριση εγγράφων και API μετατροπής.

Πρώτα, εισάγετε τις κλάσεις που θα χρειαστείτε. Διατηρήστε αυτό το μπλοκ ακριβώς όπως φαίνεται — χωρίς αλλαγές στον κώδικα.

```java
import com.aspose.note.Document;
import com.aspose.note.Metered;



import java.nio.file.Paths;
```

## Πώς να Μετατρέψετε OneNote σε PDF σε Java; 

**Άμεση απάντηση:** Φορτώστε το αρχείο OneNote με `new Document("input.one")`, στη συνέχεια καλέστε `document.save("output.pdf", SaveFormat.Pdf)`. Αυτή η ακολουθία δύο γραμμών εκτελεί τη πλήρη μετατροπή, διατηρώντας αυτόματα τη διάταξη της σελίδας, τις γραμματοσειρές και τις εικόνες. Μετά την αποθήκευση, μπορείτε να ερωτήσετε τη μετρημένη άδεια για να δείτε πόσες πίστωσεις κατανάλωσε η λειτουργία.

### Βήμα 1: Ρύθμιση της Μετρημένης Άδειας

Η κλάση `Metered` ενεργοποιεί τη λειτουργία μετρημένης άδειας για όλες τις επόμενες λειτουργίες Aspose.Note. Πρέπει να παρέχετε τα δημόσια και ιδιωτικά κλειδιά που λάβατε από τον λογαριασμό σας στο Aspose.

```java
Metered metered = new Metered();
metered.setMeteredKey("MyPublicKey", "MyPrivateKey");
```

Εδώ δημιουργούμε ένα αντικείμενο `Metered` και ενσωματώνουμε τα δημόσια/ιδιωτικά κλειδιά που λάβατε από το Aspose. Αυτό το βήμα ενεργοποιεί τη λειτουργία μετρημένης άδειας για όλες τις επόμενες λειτουργίες, συμπεριλαμβανομένης της κλήσης **convert OneNote to PDF**.

### Βήμα 2: Φόρτωση του Εγγράφου OneNote και Μετατροπή σε PDF

Η κλάση `Document` αντιπροσωπεύει ένα σημειωματάριο OneNote στη μνήμη. Μετά τη δημιουργία, μπορείτε να καλέσετε `save` με επέκταση `.pdf` για να ενεργοποιήσετε τη μετατροπή.

Το SaveFormat είναι μια απαρίθμηση που καθορίζει τη μορφή εξόδου του εγγράφου, όπως PDF.

```java
String dataDir = "Your Document Directory";
Document doc = new Document(Paths.get(dataDir,"Sample1.one").toString());
doc.save(Paths.get(dataDir,"MeteredLicense.pdf").toString());
```

- **Φόρτωση**: Το `Document` διαβάζει το αρχείο `.one` που βρίσκεται στο `dataDir`. Αυτή είναι η κλασική μέθοδος για **φόρτωση εγγράφου OneNote** για επεξεργασία.  
- **Μετατροπή & Αποθήκευση**: Η κλήση `save` με επέκταση `.pdf` αυτόματα **μετατρέπει .one σε .pdf**. Η λειτουργία επίσης **αποθηκεύει PDF από OneNote** στον ίδιο φάκελο. Αντικαταστήστε το `"Your Document Directory"` με την πραγματική διαδρομή στο μηχάνημά σας.

### Βήμα 3: Έλεγχος Κατανάλωσης Πίστωσης Πριν και Μετά τη Μετατροπή

Η κλάση `Metered` παρέχει επίσης μεθόδους για ερώτηση της χρήσης πίστωσης. Αυτές οι δύο γραμμές εκτυπώνουν το υπόλοιπο πίστωσης και το ποσό πίστωσης που χρησιμοποιήθηκε από τη μετατροπή.

Το Metered.getConsumptionCredit() επιστρέφει το υπόλοιπο πίστωσης, ενώ το Metered.getConsumptionQuantity() επιστρέφει τις πίστωσεις που χρησιμοποιήθηκαν από την τελευταία λειτουργία.

```java
System.out.println(String.format("Credit before operation: %.02f", Metered.getConsumptionCredit()));
System.out.println(String.format("Consumption quantity before operation: %.02f", Metered.getConsumptionQuantity()));
```

Η εκτέλεση των ίδιων κλήσεων μετά τη λειτουργία `save` θα εμφανίσει τις ενημερωμένες τιμές, επιτρέποντάς σας να επαληθεύσετε ότι η μετρημένη άδεια παρακολουθεί σωστά τη χρήση.

{{< blocks/products/products-backtop-button >}}

## Συχνά Προβλήματα και Λύσεις

| Πρόβλημα | Γιατί συμβαίνει | Διόρθωση |
|----------|------------------|----------|
| **Μη έγκυρα κλειδιά μετρημένης άδειας** | Τα κλειδιά έχουν πληκτρολογηθεί λανθασμένα ή έχουν λήξει. | Ελέγξτε ξανά τα κλειδιά από τον λογαριασμό σας στο Aspose· δημιουργήστε νέα εάν χρειάζεται. |
| **Αρχείο δεν βρέθηκε** | Η διαδρομή `dataDir` είναι λανθασμένη. | Χρησιμοποιήστε απόλυτη διαδρομή ή επαληθεύστε τη σχετική διαδρομή από τη ρίζα του έργου σας. |
| **Ανεπαρκείς πίστωσεις** | Όλες οι πίστωσεις έχουν καταναλωθεί. | Αγοράστε επιπλέον πίστωσεις ή μεταβείτε σε μόνιμη άδεια για εργασίες υψηλού όγκου. |

## Συχνές Ερωτήσεις

**Ε: Τι είναι μια μετρημένη άδεια;**  
Α: Μια μετρημένη άδεια σας επιτρέπει να πληρώνετε για τη χρήση του API βάσει πίστωσης, παρέχοντας λεπτομερή έλεγχο κόστους.

**Ε: Πώς μπορώ να αποκτήσω κλειδί μετρημένης άδειας για προϊόντα Aspose;**  
Α: Αγοράστε μια άδεια από την ιστοσελίδα Aspose ή ζητήστε ένα προσωρινό κλειδί αξιολόγησης μέσω του πίνακα ελέγχου του λογαριασμού σας.

**Ε: Μπορώ να χρησιμοποιήσω μια μετρημένη άδεια σε πολλαπλές εφαρμογές;**  
Α: Ναι, αλλά όλη η κατανάλωση συγκεντρώνεται κάτω από το ίδιο κλειδί, επομένως παρακολουθείτε προσεκτικά τη συνολική χρήση.

**Ε: Υπάρχει δωρεάν δοκιμή για Aspose.Note for Java;**  
Α: Ναι, μπορείτε να κατεβάσετε μια δωρεάν δοκιμή από [εδώ](https://releases.aspose.com/).

**Ε: Πού μπορώ να λάβω υποστήριξη για Aspose.Note for Java;**  
Α: Κάντε ερωτήσεις στα φόρουμ της κοινότητας Aspose [εδώ](https://forum.aspose.com/c/note/28).

## Συμπέρασμα

Τώρα έχετε μια πλήρη, έτοιμη για παραγωγή ροή εργασίας για **μετατροπή OneNote σε PDF** ενώ διαχειρίζεστε μια μετρημένη άδεια σε Java. Ελέγχοντας την κατανάλωση πίστωσης πριν και μετά τη μετατροπή, μπορείτε να διασφαλίσετε ότι η εφαρμογή σας παραμένει εντός προϋπολογισμού και κλιμακώνεται αποδοτικά. Μη διστάσετε να εξερευνήσετε πρόσθετες δυνατότητες του Aspose.Note όπως προσαρμοσμένη απόδοση σελίδων, εξαγωγή εικόνων και επεξεργασία παρτίδας για να επεκτείνετε περαιτέρω αυτή τη λύση.

---

**Last Updated:** 2026-07-05  
**Tested With:** Aspose.Note for Java 24.12 (latest at time of writing)  
**Author:** Aspose

## Σχετικά Tutorials

- [Άδεια Aspose.Note με Java – Πώς να Παρακολουθείτε τις Πίστωση](/note/java/licensing-java/)
- [μετατροπή onenote σε pdf – Μετατροπή Σημειωματάριου σε PDF με Aspose.Note](/note/java/onenote-notebook-operations/convert-notebook-to-pdf/)
- [Μετατροπή Σημειωματάριου σε PDF με Επιλογές στο OneNote - Aspose.Note](/note/java/onenote-notebook-operations/convert-notebook-to-pdf-with-options/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}