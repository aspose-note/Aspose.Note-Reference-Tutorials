---
date: 2025-12-07
description: Μάθετε πώς να αποθηκεύετε το OneNote ως PDF και να μετατρέπετε αρχεία
  OneNote χρησιμοποιώντας το Aspose.Note για Java. Αυτός ο οδηγός σας δείχνει πώς
  να εξάγετε PDF από το OneNote, να εξάγετε κείμενο και πολλά άλλα.
language: el
linktitle: How to Save OneNote as PDF with Aspose.Note for Java
second_title: Aspose.Note Java API
title: Πώς να αποθηκεύσετε το OneNote ως PDF με το Aspose.Note για Java
url: /java/onenote-document-loading/load-save-format/
weight: 24
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Αποθήκευση OneNote ως PDF με Aspose.Note για Java

Στη σύγχρονη ανάπτυξη Java, η δυνατότητα **save OneNote as PDF** γρήγορα και αξιόπιστα αποτελεί κοινή απαίτηση — είτε χρειάζεται να αρχειοθετήσετε σημειώσεις συναντήσεων, να μοιραστείτε τεκμηρίωση με χρήστες που δεν χρησιμοποιούν OneNote, είτε να αυτοματοποιήσετε τη δημιουργία αναφορών. Αυτό το tutorial σας καθοδηγεί στη φόρτωση ενός εγγράφου OneNote και στην εξαγωγή του σε PDF χρησιμοποιώντας το Aspose.Note for Java, ώστε να μπορείτε να **convert OneNote files** με λίγες μόνο γραμμές κώδικα.

## Γρήγορες Απαντήσεις
- **Τι κάνει το Aspose.Note;** Παρέχει ένα καθαρό API Java για ανάγνωση, επεξεργασία και εξαγωγή αρχείων OneNote χωρίς να απαιτείται το Microsoft OneNote.  
- **Μπορώ να εξάγω απευθείας σε PDF;** Ναι — χρησιμοποιήστε το `SaveFormat.Pdf` για **save OneNote as PDF** σε ένα βήμα.  
- **Χρειάζομαι άδεια για παραγωγή;** Απαιτείται εμπορική άδεια για χρήση σε παραγωγή· διαθέσιμο είναι ένα δωρεάν trial για αξιολόγηση.  
- **Ποιες εκδόσεις της Java υποστηρίζονται;** Η Java 8 και νεότερες εκδόσεις υποστηρίζονται πλήρως.  
- **Είναι δυνατή η εξαγωγή κειμένου;** Απολύτως — μπορείτε επίσης να **extract text from OneNote** χρησιμοποιώντας το ίδιο API.

## Τι είναι το “save onenote as pdf”;
Η αποθήκευση OneNote ως PDF σημαίνει τη μετατροπή του ιδιόκτητου μορφότυπου αρχείου `.one` σε ένα ευρέως αποδεκτό, μόνο για ανάγνωση PDF έγγραφο. Αυτή η μετατροπή διατηρεί τη διάταξη, τις εικόνες και τη μορφοποίηση, ενώ καθιστά το περιεχόμενο προσβάσιμο σε οποιαδήποτε συσκευή.

## Γιατί να μετατρέψετε το OneNote σε PDF (ή να εξάγετε OneNote PDF);
- **Καθολική πρόσβαση:** Τα PDF μπορούν να ανοιχτούν σχεδόν σε οποιαδήποτε πλατφόρμα χωρίς να απαιτείται το OneNote.  
- **Αρχειοθετητική σταθερότητα:** Τα PDF είναι ιδανικά για μακροπρόθεσμη αποθήκευση και συμμόρφωση.  
- **Απλοποιημένη κοινή χρήση:** Τα ενδιαφερόμενα μέρη λαμβάνουν ένα ενιαίο, μη επεξεργάσιμο αρχείο.  
- **Αυτοματοποίηση:** Ενσωματώστε τη μετατροπή σε εργασίες batch ή web services.

## Προαπαιτούμενα
- **Java Development Kit (JDK)** – έκδοση 8 ή νεότερη.  
- **Aspose.Note for Java** library – κατεβάστε από την επίσημη [Aspose.Note download page](https://releases.aspose.com/note/java/).  
- Ένα υπάρχον αρχείο OneNote (`.one`) που θέλετε να μετατρέψετε.

## Εισαγωγή Πακέτων
Πρώτα, εισάγετε τις κλάσεις που απαιτούνται για τη φόρτωση και αποθήκευση εγγράφων OneNote.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.SaveFormat;
```

## Οδηγός Βήμα‑βήμα

### Βήμα 1: Φόρτωση του Εγγράφου OneNote
Φορτώστε το αρχείο `.one` σας σε ένα αντικείμενο `Aspose.Note` `Document`. Αντικαταστήστε το `Your Document Directory` με τη διαδρομή προς το αρχείο σας.

```java
// ExStart:SaveDocToOneNoteFormatUsingSaveFormat
// Load the document into Aspose.Note.
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one");
```

### Βήμα 2: Αποθήκευση του Εγγράφου στην Επιθυμητή Μορφή
Τώρα εξάγετε το φορτωμένο έγγραφο ως PDF. Αυτή η μοναδική γραμμή **saves OneNote as PDF** και δείχνει πώς να **export OneNote PDF**.

```java
// Save the document as PDF
oneFile.save(dataDir + "LoadDocIntoAsposeNoteUsingSaveformat_out.pdf", SaveFormat.Pdf);
// ExEnd:SaveDocToOneNoteFormatUsingSaveFormat
```

## Συχνά Προβλήματα και Λύσεις
| Πρόβλημα | Λύση |
|----------|------|
| **Αρχείο δεν βρέθηκε** | Επαληθεύστε ότι το `dataDir` δείχνει στο σωστό φάκελο και ότι το όνομα του αρχείου ταιριάζει ακριβώς, συμπεριλαμβανομένου του πεζού/κεφαλαίου. |
| **Το PDF εμφανίζεται κενό** | Βεβαιωθείτε ότι το αρχείο OneNote περιέχει ορατό περιεχόμενο· ορισμένες κρυφές σελίδες μπορεί να μην αποδοθούν. |
| **LicenseException** | Εφαρμόστε μια έγκυρη άδεια Aspose.Note πριν καλέσετε το `save()` για να αποφύγετε υδατογραφήματα αξιολόγησης. |
| **Μεγάλα αρχεία προκαλούν OutOfMemoryError** | Επεξεργαστείτε το έγγραφο σε ενότητες ή αυξήστε το μέγεθος της μνήμης heap της JVM (`-Xmx2g`). |

## Συχνές Ερωτήσεις

**Q: Μπορώ να μετατρέψω αρχεία OneNote σε άλλες μορφές εκτός από PDF;**  
A: Ναι, το Aspose.Note υποστηρίζει DOCX, XPS, HTML και άλλα μέσω της απαρίθμησης `SaveFormat`.

**Q: Πώς μπορώ να εξάγω κείμενο από ένα έγγραφο OneNote;**  
A: Χρησιμοποιήστε τη μέθοδο `Document.getText()` για να λάβετε απλό κείμενο, επιτρέποντας σας να **extract text onenote** για ευρετηρίαση αναζήτησης ή αναλύσεις.

**Q: Είναι δυνατόν να μετατρέψετε κρυπτογραφημένα αρχεία OneNote;**  
A: Απολύτως — παρέχετε τον κωδικό πρόσβασης κατά τη δημιουργία του αντικειμένου `Document` για την αποκρυπτογράφηση του αρχείου.

**Q: Λειτουργεί το Aspose.Note σε Linux/macOS;**  
A: Η βιβλιοθήκη είναι ανεξάρτητη από πλατφόρμα· λειτουργεί όπου υπάρχει συμβατή JVM.

**Q: Πού μπορώ να βρω υποστήριξη από την κοινότητα;**  
A: Συμμετέχετε στα φόρουμ της Aspose στη [Aspose.Note community page](https://forum.aspose.com/c/note/28) για συμβουλές και επίλυση προβλημάτων.

---

**Τελευταία Ενημέρωση:** 2025-12-07  
**Δοκιμάστηκε Με:** Aspose.Note for Java 24.11  
**Συγγραφέας:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}