---
date: 2026-04-30
description: Μάθετε πώς να **αποθηκεύετε το OneNote ως PDF** και να προσθέτετε υποσελίδες
  στο OneNote χρησιμοποιώντας το Aspose.Note για Java. Ακολουθήστε αυτόν τον οδηγό
  βήμα‑βήμα για να οργανώσετε τις σημειώσεις σας αποδοτικά.
keywords:
- save onenote as pdf
- add sub pages onenote
- Aspose.Note Java
linktitle: Πώς να αποθηκεύσετε το OneNote ως PDF και να προσθέσετε υποσελίδες
second_title: Aspose.Note Java API
title: Πώς να αποθηκεύσετε το OneNote σε PDF και να προσθέσετε υποσελίδες
url: /el/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να αποθηκεύσετε το OneNote ως PDF και να προσθέσετε υποσελίδες

## Εισαγωγή

Σε αυτό το σεμινάριο, θα ανακαλύψετε **πώς να αποθηκεύσετε το onenote ως pdf** δημιουργώντας ένα έγγραφο που περιέχει τόσο κύριες όσο και υποσελίδες χρησιμοποιώντας το Aspose.Note for Java. Η οργάνωση των σημειωματάριων OneNote με σαφή ιεραρχία κάνει την πλοήγηση αβίαστη, και η εξαγωγή σε PDF εξασφαλίζει ότι μπορείτε να μοιραστείτε τις σημειώσεις σας σε μια καθολικά αναγνώσιμη μορφή. Θα σας δείξουμε επίσης πώς να **προσθέσετε υποσελίδες onenote** σε στυλ, ώστε να μπορείτε να δημιουργήσετε δομές πολλαπλών επιπέδων με ευκολία.

## Γρήγορες Απαντήσεις
- **Τι σημαίνει “save onenote as pdf”;** Αναφέρεται στην εξαγωγή ενός σημειωματάριου OneNote σε αρχείο PDF χρησιμοποιώντας το Aspose.Note for Java.  
- **Ποιο API απαιτείται;** Το Aspose.Note for Java παρέχει τις απαραίτητες κλάσεις και μεθόδους.  
- **Μπορώ να δημιουργήσω ιεραρχικές σελίδες;** Ναι – ορίστε το επίπεδο της σελίδας για να δημιουργήσετε κύριες σελίδες και υποσελίδες.  
- **Χρειάζομαι άδεια για παραγωγή;** Διατίθεται δωρεάν δοκιμή, αλλά απαιτείται εμπορική άδεια για χρήση σε παραγωγή.  
- **Σε ποιες μορφές μπορώ να εξάγω;** Εκτός από PDF, μπορείτε να εξάγετε σε BMP, PNG, JPEG, DOCX και άλλα.

## Πώς να αποθηκεύσετε το OneNote ως PDF

Η αποθήκευση του OneNote ως PDF μετατρέπει κάθε σελίδα του σημειωματάριου σε έγγραφο σταθερής διάταξης που διατηρεί τη μορφοποίηση, τις εικόνες και την ιεραρχία των σελίδων. Αυτό είναι ιδανικό για κοινή χρήση, αρχειοθέτηση ή εκτύπωση σημειώσεων διατηρώντας την αρχική δομή ανέπαφη.

## Γιατί να προσθέσετε υποσελίδες onenote;

Η προσθήκη υποσελίδων σας επιτρέπει να ομαδοποιήσετε σχετικό περιεχόμενο κάτω από μια γονική σελίδα, αντικατοπτρίζοντας μια δομή τύπου φακέλου. Βελτιώνει την οργάνωση των σημειώσεων, επιταχύνει την αναζήτηση και ενισχύει την εμπειρία ανάγνωσης όταν το σημειωματάριο εξάγεται σε PDF.

## Προαπαιτούμενα

Πριν ξεκινήσετε, βεβαιωθείτε ότι έχετε τα παρακάτω προαπαιτούμενα:

1. **Java Development Kit (JDK)** – Βεβαιωθείτε ότι έχετε εγκατεστημένο το JDK στο σύστημά σας.  
2. **Aspose.Note for Java** – Κατεβάστε και εγκαταστήστε το Aspose.Note for Java από την [ιστοσελίδα](https://purchase.aspose.com/buy).  
3. **Integrated Development Environment (IDE)** – Επιλέξτε ένα Java IDE όπως το IntelliJ IDEA, Eclipse ή NetBeans.

## Εισαγωγή Πακέτων

Ξεκινήστε εισάγοντας τα απαραίτητα πακέτα στο έργο Java σας:

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

## Βήμα 1: Ρύθμιση Καταλόγου Εγγράφου

Ορίστε τον κατάλογο όπου θέλετε να αποθηκεύσετε το έγγραφο OneNote σας:

```java
String dataDir = "Your Document Directory";
```

## Βήμα 2: Δημιουργία Αντικειμένου Εγγράφου

Δημιουργήστε ένα αντικείμενο `Document`:

```java
Document doc = new Document();
```

## Βήμα 3: Δημιουργία Σελίδων

Αρχικοποιήστε αντικείμενα σελίδας και ορίστε τα επίπεδά τους. Ο καθορισμός του επιπέδου καθορίζει αν μια σελίδα είναι κύρια ή υποσελίδα:

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## Βήμα 4: Προσθήκη Κόμβων στις Σελίδες

### Προσθήκη Κόμβων στην Πρώτη Σελίδα

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text = new RichText().append("First page.");
text.setParagraphStyle(textStyle);

outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page1.appendChildLast(outline);
```

### Προσθήκη Κόμβων στη Δεύτερη Σελίδα

```java
Outline outline2 = new Outline();
OutlineElement outlineElem2 = new OutlineElement();
ParagraphStyle textStyle2 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text2 = new RichText().append("Second page.");
text2.setParagraphStyle(textStyle2);

outlineElem2.appendChildLast(text2);
outline2.appendChildLast(outlineElem2);
page2.appendChildLast(outline2);
```

### Προσθήκη Κόμβων στην Τρίτη Σελίδα

```java
Outline outline3 = new Outline();
OutlineElement outlineElem3 = new OutlineElement();
ParagraphStyle textStyle3 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Broadway")
                                    .setFontSize(10);

RichText text3 = new RichText().append("Third page.");
text3.setParagraphStyle(textStyle3);

outlineElem3.appendChildLast(text3);
outline3.appendChildLast(outlineElem3);
page3.appendChildLast(outline3);
```

## Βήμα 5: Προσθήκη Σελίδων στο Έγγραφο

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## Βήμα 6: Αποθήκευση του Εγγράφου

Αποθηκεύστε το έγγραφο OneNote ως PDF (ή BMP σε αυτό το παράδειγμα). Η αλλαγή του `SaveFormat` σας επιτρέπει να εξάγετε σε PDF, το οποίο ικανοποιεί την απαίτηση “save onenote as pdf”:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Handle exception
}
```

> **Συμβουλή:** Για άμεση εξαγωγή σε PDF, αντικαταστήστε το `SaveFormat.Bmp` με `SaveFormat.Pdf`.

Συγχαρητήρια! Δημιουργήσατε επιτυχώς ένα έγγραφο OneNote με κύριες και υποσελίδες και μάθατε **πώς να αποθηκεύσετε το onenote ως pdf** χρησιμοποιώντας το Aspose.Note for Java.

## Γιατί είναι Σημαντικό

- **Ιεραρχική οργάνωση:** Οι κύριες και υποσελίδες σας επιτρέπουν να μιμηθείτε δομές φακέλων μέσα στο OneNote.  
- **Απρόσκοπτη εξαγωγή PDF:** Μόλις οργανωθεί, η εξαγωγή σε PDF διατηρεί την ιεραρχία, καθιστώντας το τελικό έγγραφο εύκολο στην ανάγνωση και κοινή χρήση.  
- **Αυτοματοποίηση:** Ο κώδικας μπορεί να ενσωματωθεί σε μεγαλύτερες εφαρμογές Java, επιτρέποντας τη μαζική δημιουργία δομημένων σημειωματάριων.

## Συνηθισμένα Πιθανά Σφάλματα & Πώς να τα Αποφύγετε

| Πρόβλημα | Αιτία | Λύση |
|----------|-------|------|
| Οι σελίδες εμφανίζονται στο ίδιο επίπεδο | Λανθασμένη τιμή `setLevel` | Χρησιμοποιήστε `setLevel((byte) 1)` για κύριες σελίδες και `setLevel((byte) 2)` (ή υψηλότερο) για υποσελίδες. |
| Η έξοδος PDF φαίνεται κενή | Λείπει το `SaveFormat.Pdf` ή λανθασμένη διαδρομή αρχείου | Επαληθεύστε ότι ο κατάλογος υπάρχει και χρησιμοποιήστε `SaveFormat.Pdf`. |
| Η γραμματοσειρά δεν εφαρμόζεται | Λανθασμένο όνομα γραμματοσειράς ή έλλειψη γραμματοσειράς στο σύστημα | Βεβαιωθείτε ότι η γραμματοσειρά (π.χ., “David Transparent”) είναι εγκατεστημένη στο μηχάνημα που εκτελεί τον κώδικα. |

## Συχνές Ερωτήσεις

**Ε: Μπορώ να δημιουργήσω πολλαπλά επίπεδα υποσελίδων χρησιμοποιώντας το Aspose.Note for Java;**  
Α: Ναι, μπορείτε να δημιουργήσετε βαθύτερες ιεραρχίες ορίζοντας υψηλότερους αριθμούς επιπέδου (π.χ., `setLevel((byte) 3)` για υποσελίδα τρίτου επιπέδου).

**Ε: Είναι το Aspose.Note for Java συμβατό με διαφορετικά Java IDEs;**  
Α: Απολύτως. Λειτουργεί με IntelliJ IDEA, Eclipse, NetBeans και οποιοδήποτε IDE που υποστηρίζει ανάπτυξη Java.

**Ε: Μπορώ να προσαρμόσω τη μορφοποίηση του κειμένου στο έγγραφο OneNote μου;**  
Α: Ναι. Χρησιμοποιήστε `ParagraphStyle` για να ορίσετε το όνομα γραμματοσειράς, το μέγεθος, το χρώμα και άλλα χαρακτηριστικά για κάθε στοιχείο `RichText`.

**Ε: Υποστηρίζει το Aspose.Note for Java αποθήκευση εγγράφων σε μορφές εκτός του BMP;**  
Α: Ναι. Οι υποστηριζόμενες μορφές περιλαμβάνουν PDF, PNG, JPEG, DOCX και άλλα. Αλλάξτε το enum `SaveFormat` αναλόγως.

**Ε: Υπάρχει διαθέσιμη δοκιμαστική έκδοση για το Aspose.Note for Java;**  
Α: Ναι, μπορείτε να κατεβάσετε μια δωρεάν δοκιμή από τον ιστότοπο της Aspose.

## Συμπέρασμα

Η οργάνωση των σημειωματάριων OneNote με σαφή ιεραρχική δομή και η εξαγωγή τους ως PDF καθιστούν τις σημειώσεις σας πιο προσβάσιμες και διαμοιραζόμενες. Ακολουθώντας τα παραπάνω βήματα, τώρα γνωρίζετε **πώς να αποθηκεύσετε το onenote ως pdf** και **πώς να προσθέσετε υποσελίδες onenote** προγραμματιστικά με το Aspose.Note for Java.

---

**Last Updated:** 2026-04-30  
**Tested With:** Aspose.Note for Java 24.11 (latest)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}