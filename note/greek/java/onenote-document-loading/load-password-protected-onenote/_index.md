---
date: 2026-08-29
description: Μάθετε πώς να ανοίξετε αρχεία OneNote προστατευμένα με κωδικό πρόσβασης
  σε Java με το Aspose.Note, να ανακτήσετε τη μορφή αρχείου OneNote και να εξάγετε
  εικόνες από τα σημειωματάρια.
keywords:
- open password protected onenote
- extract images from onenote
- retrieve onenote file format
lastmod: 2026-08-29
linktitle: Φόρτωση εγγράφου OneNote προστατευμένου με κωδικό – Java
og_description: Μάθετε πώς να ανοίξετε αρχεία OneNote προστατευμένα με κωδικό σε Java
  χρησιμοποιώντας το Aspose.Note, να ανακτήσετε τη μορφή αρχείου και να εξάγετε εικόνες
  από τα σημειωματάρια.
og_image_alt: Developer guide showing Java code that opens a password‑protected OneNote
  notebook with Aspose.Note
og_title: Άνοιγμα OneNote προστατευμένου με κωδικό σε Java – Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-08-29'
  description: Learn how to open password protected OneNote files in Java with Aspose.Note,
    retrieve the OneNote file format, and extract images from notebooks.
  headline: How to open password protected OneNote documents using Java – Aspose.Note
    Java
  type: TechArticle
- description: Learn how to open password protected OneNote files in Java with Aspose.Note,
    retrieve the OneNote file format, and extract images from notebooks.
  name: How to open password protected OneNote documents using Java – Aspose.Note
    Java
  steps:
  - name: define the document directory
    text: Tell the application where the OneNote file lives.
  - name: create load options with the password
    text: '`LoadOptions` is a class that lets you specify loading parameters such
      as the document password.'
  - name: load the password‑protected OneNote document
    text: '`Document` represents a OneNote notebook loaded into memory, providing
      access to its pages, sections, and resources.'
  - name: retrieve the OneNote file format (optional)
    text: '`doc.getFileFormat()` returns an enum indicating the exact OneNote version
      the file conforms to.'
  type: HowTo
- questions:
  - answer: Yes. Simply repeat the loading steps for each file, supplying the appropriate
      password each time.
    question: Can I load multiple password‑protected OneNote documents simultaneously?
  - answer: The library supports a wide range of OneNote formats, including legacy
      and the latest Office 365 notebooks.
    question: Is Aspose.Note for Java compatible with all OneNote versions?
  - answer: Catch `IOException` or a specific `InvalidPasswordException`, log the
      incident, and optionally prompt the user for a new password.
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
- onenote
- aspose.note
- java document processing
title: Πώς να ανοίξετε έγγραφα OneNote προστατευμένα με κωδικό πρόσβασης χρησιμοποιώντας
  Java – Aspose.Note
url: /el/java/onenote-document-loading/load-password-protected-onenote/
weight: 27
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Άνοιγμα εγγράφων OneNote με προστασία κωδικού πρόσβασης χρησιμοποιώντας Java

Σε αυτό το σεμινάριο θα μάθετε **πώς να ανοίγετε αρχεία OneNote με προστασία κωδικού πρόσβασης** με το Aspose.Note for Java. Είτε δημιουργείτε μια επιτραπέζια εφαρμογή, μια μικρο‑υπηρεσία ή μια διαδικτυακή αλυσίδα επεξεργασίας, η δυνατότητα ξεκλειδώματος κρυπτογραφημένων σημειωματάριων OneNote είναι ουσιώδης για ασφαλείς ροές εργασίας εγγράφων. Θα καλύψουμε επίσης πώς να **ανακτήσετε τη μορφή αρχείου OneNote** και πώς να **εξάγετε εικόνες από το OneNote** μετά το ξεκλείδωμα του σημειωματάριου.

## Σύντομες απαντήσεις
- **Ποια βιβλιοθήκη διαχειρίζεται κρυπτογραφημένα αρχεία OneNote;** Aspose.Note for Java.  
- **Χρειάζομαι άδεια για το άνοιγμα σημειωματάριων με προστασία κωδικού;** Μια δωρεάν δοκιμή λειτουργεί για ανάπτυξη· απαιτείται εμπορική άδεια για παραγωγή.  
- **Ποια έκδοση της Java απαιτείται;** Java 8 ή νεότερη.  
- **Μπορώ να ανακτήσω τη μορφή αρχείου μετά τη φόρτωση;** Ναι, καλέστε `doc.getFileFormat()`.  
- **Απαιτείται διαχείριση σφαλμάτων για λανθασμένους κωδικούς;** Απόλυτα – πιάστε `IOException` ή `InvalidPasswordException`.

## Τι είναι το άνοιγμα OneNote με προστασία κωδικού;
Το άνοιγμα ενός σημειωματάριου OneNote με προστασία κωδικού σημαίνει την παροχή του σωστού κωδικού αποκρυπτογράφησης στο Aspose.Note ώστε το API να μπορεί να διαβάσει την εσωτερική δομή του αρχείου. Η βιβλιοθήκη στη συνέχεια εκθέτει τις σελίδες, τις ενότητες και τους πόρους ως κανονικά αντικείμενα, επιτρέποντάς σας να περιηγηθείτε, να επεξεργαστείτε ή να εξάγετε περιεχόμενο προγραμματιστικά. Χωρίς τον κωδικό, το αρχείο παραμένει κρυπτογραφημένο και μη προσβάσιμο.

## Γιατί να χρησιμοποιήσετε το Aspose.Note για αυτήν την εργασία;
Το Aspose.Note υποστηρίζει **πάνω από 30 εκδόσεις OneNote** (συμπεριλαμβανομένων των παλαιών 2007, 2010, 2016 και των μορφών Office 365) και μπορεί να επεξεργαστεί σημειωματάρια έως **500 MB** χωρίς να φορτώνει ολόκληρο το αρχείο στη μνήμη, παρέχοντάς σας προβλέψιμη απόδοση σε μέτριους διακομιστές. Παρέχει επίσης APIs υψηλού επιπέδου για εξαγωγή κειμένου, εικόνων και μεταδεδομένων, απλοποιώντας την ανάπτυξη και μειώνοντας την ανάγκη για προσαρμοσμένους αναλυτές.

## Προαπαιτούμενα

Πριν ξεκινήσουμε, βεβαιωθείτε ότι έχετε τα εξής:

### 1. Java Development Kit (JDK)
Ένα πρόσφατο JDK (8 ή νεότερο) εγκατεστημένο στον υπολογιστή σας. Μπορείτε να το κατεβάσετε από την ιστοσελίδα της Oracle ή να υιοθετήσετε μια διανομή OpenJDK.

### 2. Aspose.Note for Java
Προσθέστε τη βιβλιοθήκη Aspose.Note στο έργο σας μέσω Maven, Gradle ή κατεβάζοντας το JAR από την ιστοσελίδα της Aspose.

## Εισαγωγή πακέτων

Πρώτα, εισάγετε τις κλάσεις που θα χρειαστούμε. Αυτό το τμήμα πρέπει να παραμείνει ακριβώς όπως φαίνεται.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
```

## Πώς να φορτώσετε προστατευμένο έγγραφο OneNote σε Java

Φορτώστε το σημειωματάριο σε δύο απλά βήματα: παρέχετε τον κωδικό μέσω του `LoadOptions`, στη συνέχεια δημιουργήστε μια παρουσία της κλάσης `Document` με αυτές τις επιλογές. Το API θα αποκρυπτογραφήσει το αρχείο αυτόματα αν ο κωδικός είναι σωστός· διαφορετικά θα ρίξει μια εξαίρεση που μπορείτε να πιάσετε.

### Βήμα 1: ορίστε τον κατάλογο του εγγράφου
Ενημερώστε την εφαρμογή πού βρίσκεται το αρχείο OneNote.

```java
String dataDir = "Your Document Directory";
```

### Βήμα 2: δημιουργήστε επιλογές φόρτωσης με τον κωδικό
`LoadOptions` είναι μια κλάση που σας επιτρέπει να καθορίσετε παραμέτρους φόρτωσης όπως ο κωδικός του εγγράφου.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setDocumentPassword("password");
```

### Βήμα 3: φορτώστε το προστατευμένο κωδικό OneNote έγγραφο
`Document` αντιπροσωπεύει ένα σημειωματάριο OneNote που έχει φορτωθεί στη μνήμη, παρέχοντας πρόσβαση στις σελίδες, τις ενότητες και τους πόρους του.

```java
Document doc = new Document(dataDir + "Sample1.one", loadOptions);
```

### Βήμα 4: ανακτήστε τη μορφή αρχείου OneNote (προαιρετικό)
`doc.getFileFormat()` επιστρέφει ένα enum που υποδεικνύει την ακριβή έκδοση OneNote στην οποία συμμορφώνεται το αρχείο.

```java
System.out.println(doc.getFileFormat());
```

## Γιατί μπορεί να χρειαστείτε την ανάκτηση της μορφής αρχείου OneNote
Μπορείτε αμέσως να καθορίσετε αν το σημειωματάριο ακολουθεί το σχήμα OneNote 2007, 2010, 2016 ή Office 365. Η γνώση της ακριβούς μορφής σας επιτρέπει να εφαρμόσετε κανόνες μετατροπής ειδικούς για την έκδοση, να παραλείψετε μη υποστηριζόμενα χαρακτηριστικά ή να επιλέξετε τη σωστή μηχανή απόδοσης πριν ξεκινήσετε την επεξεργασία. Αυτός ο προ‑έλεγχος βοηθά στην αποφυγή σφαλμάτων χρόνου εκτέλεσης και εξασφαλίζει συνεπή έξοδο μεταξύ διαφορετικών εκδόσεων OneNote.

## Πώς να εξάγετε εικόνες από το OneNote μετά την αποκρυπτογράφηση
`Image` είναι μια κλάση που αντιπροσωπεύει έναν πόρο εικόνας που μπορεί να αποθηκευτεί σε αρχείο ή ροή.  
`doc.getPages()` επιστρέφει μια συλλογή αντικειμένων σελίδας στο σημειωματάριο.

Αφού το σημειωματάριο ανοίξει επιτυχώς, μπορείτε να περιηγηθείτε στις σελίδες του και να εξάγετε τυχόν ενσωματωμένες εικόνες. Επανάλαβε το `doc.getPages()`, καλέστε `page.getImages()` για κάθε σελίδα και χρησιμοποιήστε `Image.save(outputPath)` για να γράψετε την εικόνα στο δίσκο ή σε ροή. Αυτή η προσέγγιση λειτουργεί για όλες τις υποστηριζόμενες μορφές εικόνας και διατηρεί την αρχική ανάλυση.

> **Συμβουλή:** Συνδυάστε τη λογική εξαγωγής εικόνων με τον έλεγχο μορφής αρχείου για να διαχειρίζεστε αυτόματα εικόνες ειδικές για την έκδοση.

## Συνηθισμένα προβλήματα και λύσεις
| Πρόβλημα | Λύση |
|-------|----------|
| **Λάθος κωδικός** | Τυλίξτε τον κώδικα φόρτωσης σε μπλοκ try‑catch και εμφανίστε ένα φιλικό μήνυμα. |
| **Αρχείο δεν βρέθηκε** | Επαληθεύστε ότι το `dataDir` τελειώνει με διαχωριστικό διαδρομής και ότι το όνομα αρχείου είναι σωστό. |
| **Μη υποστηριζόμενη έκδοση OneNote** | Βεβαιωθείτε ότι χρησιμοποιείτε την πιο πρόσφατη έκδοση του Aspose.Note, η οποία προσθέτει υποστήριξη για νεότερες μορφές. |

## Συχνές ερωτήσεις

**Q: Μπορώ να φορτώσω πολλαπλά έγγραφα OneNote με προστασία κωδικού ταυτόχρονα;**  
A: Ναι. Απλώς επαναλάβετε τα βήματα φόρτωσης για κάθε αρχείο, παρέχοντας τον κατάλληλο κωδικό κάθε φορά.

**Q: Είναι το Aspose.Note for Java συμβατό με όλες τις εκδόσεις OneNote;**  
A: Η βιβλιοθήκη υποστηρίζει μια ευρεία γκάμα μορφών OneNote, συμπεριλαμβανομένων των παλαιών και των πιο πρόσφατων σημειωματάριων Office 365.

**Q: Πώς πρέπει να διαχειρίζομαι τα σφάλματα αποκρυπτογράφησης προγραμματιστικά;**  
A: Πιάστε `IOException` ή ένα συγκεκριμένο `InvalidPasswordException`, καταγράψτε το περιστατικό και προαιρετικά ζητήστε από τον χρήστη νέο κωδικό.

**Q: Υπάρχει δοκιμαστική έκδοση του Aspose.Note for Java;**  
A: Απόλυτα. Μπορείτε να κατεβάσετε μια πλήρως λειτουργική δοκιμή 30 ημερών από την ιστοσελίδα της Aspose.

**Q: Μπορώ να χρησιμοποιήσω αυτή τη βιβλιοθήκη τόσο σε επιτραπέζιες όσο και σε διαδικτυακές εφαρμογές;**  
A: Ναι. Το API είναι ανεξάρτητο από την πλατφόρμα και λειτουργεί εξίσου καλά σε servlet containers, υπηρεσίες Spring Boot ή αυτόνομες εφαρμογές Java.

**Q: Η βιβλιοθήκη υποστηρίζει την εξαγωγή εικόνων από ένα σημειωματάριο με προστασία κωδικού;**  
A: Μόλις το έγγραφο φορτωθεί επιτυχώς, μπορείτε να διασχίσετε τις σελίδες του και να εξάγετε εικόνες χρησιμοποιώντας το τυπικό API του Aspose.Note (δείτε την ενότητα “Πώς να εξάγετε εικόνες από το OneNote” παραπάνω).

**Τελευταία ενημέρωση:** 2026-08-29  
**Δοκιμάστηκε με:** Aspose.Note for Java 26.4  
**Συγγραφέας:** Aspose

## Σχετικά Σεμινάρια

- [Προστασία κωδικού OneNote με Aspose.Note for Java](/note/java/onenote-notebook-operations/write-password-protected-document/)
- [Πώς να εντοπίσετε τη μορφή αρχείου OneNote με Aspose.Note – Java](/note/java/onenote-document-loading/get-file-format-info/)
- [Μετατροπή OneNote σε κείμενο και εξαγωγή εικόνων χρησιμοποιώντας Document Visitor - Java](/note/java/onenote-document-loading/extract-content-using-document-visitor/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}