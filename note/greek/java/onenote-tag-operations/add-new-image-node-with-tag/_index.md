---
title: Προσθήκη νέου κόμβου εικόνας με ετικέτα στο OneNote - Aspose.Note
linktitle: Προσθήκη νέου κόμβου εικόνας με ετικέτα στο OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Μάθετε πώς μπορείτε να προσθέσετε έναν νέο κόμβο εικόνας με μια ετικέτα στο OneNote χρησιμοποιώντας το Aspose.Note για Java. Αναβαθμίστε τις δεξιότητές σας στον προγραμματισμό Java χωρίς κόπο.
type: docs
weight: 10
url: /el/java/onenote-tag-operations/add-new-image-node-with-tag/
---
## Εισαγωγή
Στον τομέα του προγραμματισμού Java, το Aspose.Note ξεχωρίζει ως ένα ισχυρό εργαλείο για τον εύκολο χειρισμό εγγράφων του OneNote. Αν θέλετε να βελτιώσετε τις δεξιότητές σας και να μάθετε πώς να προσθέτετε έναν νέο κόμβο εικόνας με μια ετικέτα στο OneNote χρησιμοποιώντας το Aspose.Note, έχετε έρθει στο σωστό μέρος. Αυτός ο οδηγός βήμα προς βήμα θα σας καθοδηγήσει στη διαδικασία, διασφαλίζοντας ότι κατανοείτε κάθε έννοια πλήρως.
## Προαπαιτούμενα
Πριν ξεκινήσουμε το σεμινάριο, ας βεβαιωθούμε ότι έχετε όλα όσα χρειάζεστε:
1.  Aspose.Note για Java: Βεβαιωθείτε ότι έχετε εγκαταστήσει τη βιβλιοθήκη Aspose.Note. Εάν όχι, μπορείτε να το κατεβάσετε[εδώ](https://releases.aspose.com/note/java/).
2. Περιβάλλον ανάπτυξης Java: Βεβαιωθείτε ότι έχετε ρυθμίσει ένα λειτουργικό περιβάλλον ανάπτυξης Java στον υπολογιστή σας.
Τώρα που έχουμε τα προαπαιτούμενα, ας προχωρήσουμε στα επόμενα βήματα.
## Εισαγωγή πακέτων
Στο έργο σας Java, ξεκινήστε εισάγοντας τα απαραίτητα πακέτα:
```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Image;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
import com.aspose.note.TagIcon;
```
## Βήμα 1: Δημιουργία αντικειμένου εγγράφου
```java
// Η διαδρομή προς τον κατάλογο εγγράφων.
String dataDir = "Your Document Directory";
// δημιουργήστε ένα αντικείμενο της κλάσης Document
Document doc = new Document();
```
## Βήμα 2: Αρχικοποίηση αντικειμένου κλάσης σελίδας
```java
// αρχικοποίηση αντικειμένου κλάσης σελίδας
Page page = new Page();
```
## Βήμα 3: Αρχικοποίηση αντικειμένου κλάσης Outline
```java
// αρχικοποίηση αντικειμένου κλάσης Outline
Outline outline = new Outline();
```
## Βήμα 4: Αρχικοποίηση αντικειμένου κλάσης OutlineElement
```java
// αρχικοποίηση αντικειμένου κλάσης OutlineElement
OutlineElement outlineElem = new OutlineElement();
```
## Βήμα 5: Φόρτωση και εισαγωγή εικόνας
```java
// φορτώστε μια εικόνα
Image image = new Image(null, dataDir + "Input.jpg");
// εισαγάγετε εικόνα στον κόμβο του εγγράφου
outlineElem.appendChildLast(image);
```
## Βήμα 6: Προσθήκη ετικέτας σημείωσης στην εικόνα
```java
// προσθέστε μια κίτρινη ετικέτα νότας αστεριού στην εικόνα
NoteTag noteTag = NoteTag.createYellowStar();
image.getTags().add(noteTag);
```
## Βήμα 7: Προσθήκη κόμβου στοιχείου περιγράμματος
```java
// προσθήκη κόμβου στοιχείου περιγράμματος
outline.appendChildLast(outlineElem);
```
## Βήμα 8: Προσθήκη κόμβου περιγράμματος
```java
// προσθήκη κόμβου περιγράμματος
page.appendChildLast(outline);
```
## Βήμα 9: Προσθήκη Κόμβου σελίδας
```java
// προσθήκη κόμβου σελίδας
doc.appendChildLast(page);
```
## Βήμα 10: Αποθήκευση εγγράφου OneNote
```java
// αποθηκεύστε το έγγραφο του OneNote ως PDF
doc.save(dataDir + "AddNewImageNodeWithTag_out.pdf", SaveFormat.Pdf);
```
Συγχαρητήρια! Προσθέσατε με επιτυχία έναν νέο κόμβο εικόνας με ετικέτα στο OneNote χρησιμοποιώντας το Aspose.Note για Java.
## συμπέρασμα
 Το Mastering Aspose.Note για Java ανοίγει συναρπαστικές δυνατότητες στη διαχείριση εγγράφων του OneNote. Ακολουθώντας αυτό το σεμινάριο, έχετε αποκτήσει μια πρακτική δεξιότητα που μπορεί να εφαρμοστεί σε διάφορα έργα. Συνεχίστε να εξερευνάτε την τεκμηρίωση Aspose.Note[εδώ](https://reference.aspose.com/note/java/)για πιο προηγμένες λειτουργίες και δυνατότητες.
## Συχνές ερωτήσεις
### Πού μπορώ να βρω την τεκμηρίωση του Aspose.Note;
 Μπορείτε να βρείτε την τεκμηρίωση[εδώ](https://reference.aspose.com/note/java/).
### Πώς μπορώ να κατεβάσω το Aspose.Note για Java;
 Μπορείτε να το κατεβάσετε από τη σελίδα εκδόσεων[εδώ](https://releases.aspose.com/note/java/).
### Υπάρχει δωρεάν δοκιμή διαθέσιμη;
 Ναι, μπορείτε να έχετε πρόσβαση στη δωρεάν δοκιμή[εδώ](https://releases.aspose.com/).
### Πού μπορώ να λάβω υποστήριξη για το Aspose.Note;
 Επισκεφθείτε το φόρουμ της κοινότητας[εδώ](https://forum.aspose.com/c/note/28) για υποστήριξη.
### Χρειάζομαι προσωρινή άδεια;
 Εάν απαιτείται, μπορείτε να αποκτήσετε προσωρινή άδεια[εδώ](https://purchase.aspose.com/temporary-license/).