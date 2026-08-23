---
date: 2026-08-23
description: Μάθετε πώς να φορτώνετε αρχεία OneNote προστατευμένα με κωδικό χρησιμοποιώντας
  Aspose.Note για Java, να ανακτάτε το file format και να extract images από σημειωματάρια.
keywords:
- load password protected onenote
- extract images from onenote
- retrieve onenote file format
- get onenote file type
lastmod: 2026-08-23
linktitle: Φόρτωση Εγγράφου OneNote Προστατευμένου με Κωδικό – Java
og_description: Μάθετε πώς να φορτώνετε αρχεία OneNote προστατευμένα με κωδικό με
  Aspose.Note για Java, να ανακτάτε το file format και να extract images από σημειωματάρια
  σε secure workflow.
og_image_alt: Guide showing how to load a password‑protected OneNote file in Java
  with Aspose.Note
og_title: Φόρτωση προστατευμένου με κωδικό OneNote χρησιμοποιώντας Java – Οδηγός Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-08-23'
  description: Learn how to load password protected onenote files with Aspose.Note
    for Java, retrieve the file format and extract images from notebooks.
  headline: Load password protected onenote using Java
  type: TechArticle
- description: Learn how to load password protected onenote files with Aspose.Note
    for Java, retrieve the file format and extract images from notebooks.
  name: Load password protected onenote using Java
  steps:
  - name: Define the document directory
    text: Specify the folder path where the OneNote file is stored.
  - name: Create load options with the password
    text: Create a LoadOptions object and set the document password for decryption.
  - name: Load the password‑protected OneNote document
    text: Instantiate a Document with the file path and the configured LoadOptions
      to open the notebook.
  - name: Retrieve the OneNote file format (optional)
    text: Call getFileFormat() on the Document to obtain the OneNote version enum.
  type: HowTo
- questions:
  - answer: Yes. Simply repeat the loading steps for each file, supplying the appropriate
      password each time.
    question: Can I load multiple password‑protected OneNote documents simultaneously?
  - answer: The library supports a wide range of OneNote formats, including legacy
      files and the latest Office 365 notebooks.
    question: Is Aspose.Note for Java compatible with all OneNote versions?
  - answer: Catch `IOException` or `InvalidPasswordException`, log the incident, and
      optionally prompt the user for a new password.
    question: How should I handle decryption errors programmatically?
  - answer: Absolutely. You can download a fully functional 30‑day trial from the
      Aspose website.
    question: Is there a trial version of Aspose.Note for Java?
  - answer: Yes. The API is platform‑agnostic and works equally well in servlet containers,
      Spring Boot services, or standalone Java applications.
    question: Can I use this library in both desktop and web applications?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote loading
- Aspose.Note
- Java document processing
title: Φόρτωση προστατευμένου με κωδικό OneNote χρησιμοποιώντας Java
url: /el/java/onenote-document-loading/load-password-protected-onenote/
weight: 27
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Φόρτωση εγγράφου OneNote με προστασία κωδικού πρόσβασης χρησιμοποιώντας Java

Σε αυτό το μάθημα θα ανακαλύψετε **how to load password protected onenote** αρχεία με το Aspose.Note for Java. Είτε δημιουργείτε μια επιτραπέζια εφαρμογή, μια μικρο‑υπηρεσία, ή μια διαδικασία επεξεργασίας βασισμένη στο web, η δυνατότητα ανοίγματος κρυπτογραφημένων σημειωματάριων OneNote είναι ουσιώδης για ασφαλείς ροές εργασίας εγγράφων. Θα σας δείξουμε επίσης πώς να **retrieve onenote file format** πληροφορίες και πώς να **extract images from onenote** μετά το ξεκλείδωμα του εγγράφου.

## Γρήγορες απαντήσεις
- **Ποια βιβλιοθήκη διαχειρίζεται κρυπτογραφημένα αρχεία OneNote;** Aspose.Note for Java.  
- **Χρειάζομαι άδεια για τη φόρτωση σημειωματάριων με προστασία κωδικού;** Μια δωρεάν δοκιμή λειτουργεί για ανάπτυξη· απαιτείται εμπορική άδεια για παραγωγή.  
- **Ποια έκδοση Java απαιτείται;** Java 8 ή νεότερη.  
- **Μπορώ να ανακτήσω τη μορφή αρχείου μετά τη φόρτωση;** Ναι, χρησιμοποιήστε `doc.getFileFormat()`.  
- **Απαιτείται διαχείριση σφαλμάτων για λανθασμένους κωδικούς;** Απόλυτα – πιάστε `IOException` ή `InvalidPasswordException`.

## Τι είναι η φόρτωση κωδικού προστασίας onenote;
Η φόρτωση ενός σημειωματάριου OneNote με προστασία κωδικού σημαίνει την παροχή του σωστού κωδικού αποκρυπτογράφησης στο Aspose.Note API ώστε το αρχείο να ανοίξει στη μνήμη. Το Aspose.Note αποκρυπτογραφεί το αρχείο εν κινήσει, επιτρέποντάς σας να εργάζεστε με σελίδες, ενότητες και ενσωματωμένους πόρους χωρίς να αποθηκεύετε τον κωδικό.

## Γιατί να εξάγετε εικόνες από onenote;
Η εξαγωγή εικόνων σας επιτρέπει να επαναχρησιμοποιήσετε οπτικό περιεχόμενο εκτός του σημειωματάριου, να δημιουργήσετε μικρογραφίες για προεπισκόπηση ή να τροφοδοτήσετε τα γραφικά σε επόμενη επεξεργασία όπως OCR, μοντέλα μηχανικής μάθησης ή αγωγούς δημοσίευσης. Το Aspose.Note μπορεί να ανακτήσει κάθε ραστερ ή διανυσματική εικόνα ενσωματωμένη σε κάθε σελίδα διατηρώντας την αρχική ανάλυση, βάθος χρώματος και μεταδεδομένα, εξασφαλίζοντας πιστότητα για οποιαδήποτε μετέπειτα χρήση.

## Γιατί να ανακτήσετε τη μορφή αρχείου onenote;
Η γνώση της ακριβούς έκδοσης OneNote (π.χ., OneNote 2007, 2010, 2016 ή Office 365) σας επιτρέπει να εφαρμόσετε λογική εξαρτημένη από την έκδοση, όπως η διαχείριση παλαιού markup ή η αξιοποίηση νεότερων λειτουργιών όπως τα στίγματα μελάνης. Η κλήση `getFileFormat()` επιστρέφει ένα enum που μπορείτε να ελέγξετε για υπό όρους επεξεργασία.

## Προαπαιτούμενα

Πριν ξεκινήσουμε, βεβαιωθείτε ότι έχετε τα εξής:

### 1. Java Development Kit (JDK)
Ένα πρόσφατο JDK (8 ή νεότερο) εγκατεστημένο στο σύστημά σας. Μπορείτε να το κατεβάσετε από την ιστοσελίδα της Oracle ή να υιοθετήσετε μια διανομή OpenJDK.

### 2. Aspose.Note for Java
Προσθέστε τη βιβλιοθήκη Aspose.Note στο έργο σας μέσω Maven, Gradle ή κατεβάζοντας το JAR από την ιστοσελίδα της Aspose.

## Εισαγωγή πακέτων

Οι παρακάτω εισαγωγές φέρνουν τις απαραίτητες κλάσεις Aspose.Note για εργασία με αρχεία OneNote.
```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
```

## Πώς να φορτώσω ένα αρχείο OneNote με προστασία κωδικού πρόσβασης σε Java;

Φορτώστε το σημειωματάριο δημιουργώντας μια παρουσία `LoadOptions` που περιέχει τον κωδικό, στη συνέχεια περάστε αυτό το αντικείμενο επιλογών στον κατασκευαστή `Document`. Το Aspose.Note αποκρυπτογραφεί το αρχείο στη μνήμη, έτσι δεν γράφετε ποτέ τον κωδικό στο δίσκο. Μετά τη φόρτωση μπορείτε να καλέσετε `doc.getFileFormat()` ή να επαναλάβετε τις σελίδες για εξαγωγή εικόνων.

## Πώς να φορτώσετε προστατευμένο OneNote χρησιμοποιώντας Java

Για να φορτώσετε ένα αρχείο OneNote με προστασία κωδικού, πρώτα καθορίζετε το φάκελο που περιέχει το σημειωματάριο, στη συνέχεια δημιουργείτε ένα αντικείμενο LoadOptions με τον κωδικό αποκρυπτογράφησης. Περνάτε τόσο τη διαδρομή αρχείου όσο και το LoadOptions στον κατασκευαστή Document, ο οποίος ανοίγει το αρχείο στη μνήμη χωρίς να εκθέτει τον κωδικό στο δίσκο. Μόλις φορτωθεί, μπορείτε να ερωτήσετε τη μορφή του ή να εξάγετε τα περιεχόμενά του.

Παρακάτω είναι ο οδηγός βήμα‑βήμα που εκτελεί πραγματικά τη φόρτωση. Ακολουθήστε προσεκτικά κάθε βήμα και το σημειωματάριο θα είναι έτοιμο για περαιτέρω επεξεργασία.

### Βήμα 1: Ορισμός του καταλόγου εγγράφου
Καθορίστε τη διαδρομή φακέλου όπου αποθηκεύεται το αρχείο OneNote.
```java
String dataDir = "Your Document Directory";
```

### Βήμα 2: Δημιουργία επιλογών φόρτωσης με τον κωδικό πρόσβασης
Δημιουργήστε ένα αντικείμενο LoadOptions και ορίστε τον κωδικό του εγγράφου για αποκρυπτογράφηση.
```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setDocumentPassword("password");
```

### Βήμα 3: Φόρτωση του εγγράφου OneNote με προστασία κωδικού πρόσβασης
Δημιουργήστε ένα Document με τη διαδρομή αρχείου και τις ρυθμισμένες LoadOptions για άνοιγμα του σημειωματάριου.
```java
Document doc = new Document(dataDir + "Sample1.one", loadOptions);
```

### Βήμα 4: Ανάκτηση της μορφής αρχείου OneNote (προαιρετικό)
Καλέστε getFileFormat() στο Document για να λάβετε το enum έκδοσης OneNote.
```java
System.out.println(doc.getFileFormat());
```

## Γιατί μπορεί να χρειαστεί να ανακτήσετε τη μορφή αρχείου onenote
Το Aspose.Note υποστηρίζει **30+ OneNote file formats** και μπορεί να επεξεργαστεί σημειωματάρια έως **500 MB** χωρίς να φορτώνει ολόκληρο το αρχείο στη μνήμη. Η γνώση της ακριβούς μορφής (π.χ., OneNote 2007, OneNote 2010, OneNote 2016) σας βοηθά να αποφασίσετε αν θα εξάγετε σε PDF, θα μετατρέψετε σε HTML ή θα εφαρμόσετε χειρισμό εικόνων ειδικά για την έκδοση.

## Πώς να εξάγετε εικόνες από onenote μετά την αποκρυπτογράφηση
Αφού φορτωθεί επιτυχώς το σημειωματάριο, επαναλάβετε κάθε σελίδα χρησιμοποιώντας `doc.getPages()`. Για κάθε σελίδα καλέστε `page.getImages()` για να λάβετε μια συλλογή αντικειμένων Image. Κάθε Image μπορεί να αποθηκευτεί σε αρχείο ή ροή με `image.save(outputPath)`, επιτρέποντάς σας να εξάγετε όλα τα ενσωματωμένα γραφικά διατηρώντας την αρχική ποιότητα και τα μεταδεδομένα.

## Συνηθισμένα προβλήματα και λύσεις
| Πρόβλημα | Λύση |
|----------|------|
| **Λανθασμένος κωδικός πρόσβασης** | Τυλίξτε τον κώδικα φόρτωσης σε ένα μπλοκ try‑catch και εμφανίστε ένα φιλικό μήνυμα. |
| **Αρχείο δεν βρέθηκε** | Επαληθεύστε ότι το `dataDir` τελειώνει με διαχωριστικό διαδρομής και ότι το όνομα αρχείου είναι σωστό. |
| **Μη υποστηριζόμενη έκδοση OneNote** | Βεβαιωθείτε ότι χρησιμοποιείτε την πιο πρόσφατη έκδοση του Aspose.Note, η οποία προσθέτει υποστήριξη για νεότερες μορφές. |

## Συχνές ερωτήσεις

**Ε: Μπορώ να φορτώσω πολλαπλά έγγραφα OneNote με προστασία κωδικού ταυτόχρονα;**  
Α: Ναι. Απλώς επαναλάβετε τα βήματα φόρτωσης για κάθε αρχείο, παρέχοντας τον κατάλληλο κωδικό κάθε φορά.

**Ε: Είναι το Aspose.Note for Java συμβατό με όλες τις εκδόσεις OneNote;**  
Α: Η βιβλιοθήκη υποστηρίζει μια ευρεία γκάμα μορφών OneNote, συμπεριλαμβανομένων των παλαιών αρχείων και των πιο πρόσφατων σημειωματάριων Office 365.

**Ε: Πώς πρέπει να διαχειρίζομαι προγραμματιστικά τα σφάλματα αποκρυπτογράφησης;**  
Α: Πιάστε `IOException` ή `InvalidPasswordException`, καταγράψτε το περιστατικό και, προαιρετικά, ζητήστε από τον χρήστη νέο κωδικό.

**Ε: Υπάρχει δοκιμαστική έκδοση του Aspose.Note for Java;**  
Α: Απόλυτα. Μπορείτε να κατεβάσετε μια πλήρως λειτουργική δοκιμή 30‑ημέρας από την ιστοσελίδα της Aspose.

**Ε: Μπορώ να χρησιμοποιήσω αυτή τη βιβλιοθήκη τόσο σε επιτραπέζιες όσο και σε web εφαρμογές;**  
Α: Ναι. Το API είναι ανεξάρτητο από την πλατφόρμα και λειτουργεί εξίσου καλά σε servlet containers, υπηρεσίες Spring Boot ή αυτόνομες εφαρμογές Java.

**Ε: Υποστηρίζει η βιβλιοθήκη εξαγωγή εικόνων από σημειωματάριο με προστασία κωδικού;**  
Α: Μόλις το έγγραφο φορτωθεί επιτυχώς, μπορείτε να διασχίσετε τις σελίδες του και να εξάγετε εικόνες χρησιμοποιώντας το τυπικό API του Aspose.Note (δείτε το «Πώς να εξάγετε εικόνες από onenote μετά την αποκρυπτογράφηση» παραπάνω).

---

**Last Updated:** 2026-08-23  
**Tested With:** Aspose.Note for Java 26.4  
**Author:** Aspose

## Σχετικά Μαθήματα

- [Πώς να εντοπίσετε τη μορφή αρχείου OneNote με το Aspose.Note – Java](/note/java/onenote-document-loading/get-file-format-info/)
- [Πώς να εξάγετε εικόνες από έγγραφο OneNote χρησιμοποιώντας Java](/note/java/onenote-hyperlinks-images/extract-images/)
- [Προστασία κωδικού πρόσβασης onenote με Aspose.Note for Java](/note/java/onenote-notebook-operations/write-password-protected-document/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}