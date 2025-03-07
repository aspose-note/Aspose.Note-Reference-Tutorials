---
title: Προσθήκη κόμβου κειμένου με ετικέτα στο OneNote - Aspose.Note
linktitle: Προσθήκη κόμβου κειμένου με ετικέτα στο OneNote - Aspose.Note
second_title: Aspose.Note Java API
description: Εξερευνήστε πώς μπορείτε να προσθέσετε κόμβους κειμένου με ετικέτες στο OneNote χρησιμοποιώντας το Aspose.Note για Java. Εύκολο, αποτελεσματικό και φιλικό προς τους προγραμματιστές. Κατεβάστε τη βιβλιοθήκη τώρα!
weight: 13
url: /el/java/onenote-tag-operations/add-text-node-with-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Προσθήκη κόμβου κειμένου με ετικέτα στο OneNote - Aspose.Note

## Εισαγωγή
Σε αυτό το σεμινάριο, θα διερευνήσουμε πώς να προσθέσετε έναν κόμβο κειμένου με μια ετικέτα στο OneNote χρησιμοποιώντας το Aspose.Note για Java. Το Aspose.Note είναι μια ισχυρή βιβλιοθήκη Java που επιτρέπει στους προγραμματιστές να εργάζονται με αρχεία Microsoft OneNote μέσω προγραμματισμού. Η προσθήκη κόμβων κειμένου με ετικέτες είναι μια κοινή απαίτηση στην επεξεργασία εγγράφων και το Aspose.Note απλοποιεί αυτήν την εργασία.
## Προαπαιτούμενα
Πριν ξεκινήσουμε το σεμινάριο, βεβαιωθείτε ότι έχετε τις ακόλουθες προϋποθέσεις:
- Βασικές γνώσεις προγραμματισμού Java.
-  Εγκαταστάθηκε το Aspose.Note για τη βιβλιοθήκη Java. Μπορείτε να το κατεβάσετε[εδώ](https://releases.aspose.com/note/java/).
- Ένα ολοκληρωμένο περιβάλλον ανάπτυξης (IDE) που έχει δημιουργηθεί για ανάπτυξη Java.
## Εισαγωγή πακέτων
Ξεκινήστε εισάγοντας τα απαραίτητα πακέτα για το έργο σας Java. Στον κώδικά σας, συμπεριλάβετε τις ακόλουθες εισαγωγές:
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.TagIcon;
import com.aspose.note.ParagraphStyle;
```
## Βήμα 1: Δημιουργία αντικειμένου εγγράφου
Αρχικοποιήστε ένα αντικείμενο κλάσης Document για να αντιπροσωπεύσει το έγγραφο του OneNote:
```java
// Η διαδρομή προς τον κατάλογο εγγράφων.
String dataDir = "Your Document Directory";
//Δημιουργήστε ένα αντικείμενο της κλάσης Document
Document doc = new Document();
```
## Βήμα 2: Αρχικοποίηση αντικειμένου κλάσης σελίδας
Αρχικοποιήστε ένα αντικείμενο κλάσης σελίδας για να αναπαραστήσετε τη σελίδα μέσα στο έγγραφο:
```java
// Αρχικοποίηση αντικειμένου κλάσης σελίδας
Page page = new Page();
```
## Βήμα 3: Αρχικοποίηση αντικειμένου κλάσης Outline
Αρχικοποιήστε ένα αντικείμενο κλάσης Outline για τη δομή του περιεχομένου μέσα στη σελίδα:
```java
// Αρχικοποίηση αντικειμένου κλάσης Outline
Outline outline = new Outline();
```
## Βήμα 4: Αρχικοποίηση αντικειμένου κλάσης OutlineElement
Αρχικοποιήστε ένα αντικείμενο κλάσης OutlineElement για να αναπαραστήσετε ένα στοιχείο μέσα στο περίγραμμα:
```java
// Αρχικοποίηση αντικειμένου κλάσης OutlineElement
OutlineElement outlineElem = new OutlineElement();
```
## Βήμα 5: Προσαρμογή στυλ κειμένου
Ρυθμίστε το στυλ για τον κόμβο κειμένου, όπως χρώμα γραμματοσειράς, όνομα και μέγεθος:
```java
// Προσαρμόστε το στυλ κειμένου
ParagraphStyle textStyle = new ParagraphStyle()
                                .setFontColor(Color.BLACK)
                                .setFontName("Arial")
                                .setFontSize(10);
```
## Βήμα 6: Δημιουργία αντικειμένου εμπλουτισμένου κειμένου
Δημιουργήστε ένα αντικείμενο RichText και προσθέστε το επιθυμητό κείμενο σε αυτό:
```java
// Δημιουργία αντικειμένου εμπλουτισμένου κειμένου
RichText text = new RichText().append("OneNote text.");
text.setParagraphStyle(textStyle);
```
## Βήμα 7: Προσθήκη ετικέτας σημείωσης
Προσθέστε μια ετικέτα σημείωσης, όπως ένα κίτρινο αστέρι, στο κείμενο:
```java
// Προσθήκη ετικέτας σημείωσης
NoteTag noteTag = NoteTag.createYellowStar();
text.getTags().add(noteTag);
```
## Βήμα 8: Προσθήκη κόμβου κειμένου
Προσθέστε τον κόμβο κειμένου στο στοιχείο περίγραμμα:
```java
// Προσθήκη κόμβου κειμένου
outlineElem.appendChildLast(text);
```
## Βήμα 9: Προσθήκη στοιχείου περιγράμματος στο περίγραμμα
Προσθέστε το στοιχείο περίγραμμα στο περίγραμμα:
```java
// Προσθήκη κόμβου στοιχείου περιγράμματος
outline.appendChildLast(outlineElem);
```
## Βήμα 10: Προσθέστε περίγραμμα στη σελίδα
Προσθέστε το περίγραμμα στη σελίδα:
```java
// Προσθήκη κόμβου περιγράμματος
page.appendChildLast(outline);
```
## Βήμα 11: Προσθήκη σελίδας στο έγγραφο
Προσθέστε τη σελίδα στο έγγραφο:
```java
// Προσθήκη κόμβου σελίδας
doc.appendChildLast(page);
```
## Βήμα 12: Αποθήκευση εγγράφου OneNote
Αποθηκεύστε το έγγραφο του OneNote στον καθορισμένο κατάλογο:
```java
// Αποθήκευση εγγράφου OneNote
doc.save(dataDir + "AddTextNodeWithTag_out.one");
```
Συγχαρητήρια! Προσθέσατε με επιτυχία έναν κόμβο κειμένου με ετικέτα στο OneNote χρησιμοποιώντας το Aspose.Note για Java.
## συμπέρασμα
Σε αυτό το σεμινάριο, καλύψαμε τη διαδικασία βήμα προς βήμα της προσθήκης ενός κόμβου κειμένου με μια ετικέτα στο OneNote χρησιμοποιώντας τη βιβλιοθήκη Aspose.Note για Java. Αυτή η ισχυρή βιβλιοθήκη απλοποιεί τις εργασίες επεξεργασίας εγγράφων, διευκολύνοντας τους προγραμματιστές να χειρίζονται αρχεία OneNote μέσω προγραμματισμού.
## Συχνές Ερωτήσεις
### Ε: Μπορώ να χρησιμοποιήσω το Aspose.Note για Java με άλλες βιβλιοθήκες Java;
Α: Ναι, το Aspose.Note για Java μπορεί να ενσωματωθεί απρόσκοπτα με άλλες βιβλιοθήκες Java για τη βελτίωση των δυνατοτήτων επεξεργασίας εγγράφων.
### Ε: Υπάρχει διαθέσιμη δωρεάν δοκιμή για το Aspose.Note για Java;
 Α: Ναι, μπορείτε να έχετε πρόσβαση στη δωρεάν δοκιμή[εδώ](https://releases.aspose.com/).
### Ε: Πώς μπορώ να λάβω υποστήριξη για το Aspose.Note για Java;
Α: Μπορείτε να αναζητήσετε υποστήριξη από την κοινότητα Aspose.Note[δικαστήριο](https://forum.aspose.com/c/note/28).
### Ε: Είναι διαθέσιμες προσωρινές άδειες χρήσης για το Aspose.Note για Java;
 Α: Ναι, μπορείτε να αποκτήσετε προσωρινές άδειες[εδώ](https://purchase.aspose.com/temporary-license/).
### Ε: Πού μπορώ να βρω την τεκμηρίωση για το Aspose.Note για Java;
 Α: Η τεκμηρίωση είναι διαθέσιμη[εδώ](https://reference.aspose.com/note/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
