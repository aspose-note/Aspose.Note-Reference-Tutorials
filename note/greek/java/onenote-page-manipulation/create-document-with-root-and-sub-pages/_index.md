---
title: Δημιουργία εγγράφου με ρίζες και δευτερεύουσες σελίδες στο OneNote
linktitle: Δημιουργία εγγράφου με ρίζες και δευτερεύουσες σελίδες στο OneNote
second_title: Aspose.Note Java API
description: Δημιουργήστε ένα έγγραφο με ρίζες και δευτερεύουσες σελίδες στο OneNote χρησιμοποιώντας το Aspose.Note για Java. Ακολουθήστε τον οδηγό βήμα προς βήμα για να οργανώσετε αποτελεσματικά τις σημειώσεις σας.
weight: 11
url: /el/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Δημιουργία εγγράφου με ρίζες και δευτερεύουσες σελίδες στο OneNote

## Εισαγωγή

Σε αυτό το σεμινάριο, θα σας καθοδηγήσουμε στη διαδικασία δημιουργίας ενός εγγράφου με ρίζα και δευτερεύουσες σελίδες στο OneNote χρησιμοποιώντας το Aspose.Note για Java. Ακολουθώντας αυτά τα βήματα, θα μπορείτε να οργανώνετε αποτελεσματικά τα έγγραφά σας στο OneNote με ιεραρχική δομή.

## Προαπαιτούμενα

Πριν ξεκινήσετε, βεβαιωθείτε ότι έχετε τις ακόλουθες προϋποθέσεις:

1. Java Development Kit (JDK): Βεβαιωθείτε ότι έχετε εγκαταστήσει το JDK στο σύστημά σας.
2. Aspose.Note για Java: Κατεβάστε και εγκαταστήστε το Aspose.Note για Java από το[δικτυακός τόπος](https://purchase.aspose.com/buy).
3. Ενσωματωμένο περιβάλλον ανάπτυξης (IDE): Επιλέξτε ένα Java IDE όπως το IntelliJ IDEA, το Eclipse ή το NetBeans.

## Εισαγωγή πακέτων

Ξεκινήστε εισάγοντας τα απαραίτητα πακέτα στο έργο σας Java:

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

## Βήμα 1: Ρύθμιση καταλόγου εγγράφων

Καθορίστε τον κατάλογο στον οποίο θέλετε να αποθηκεύσετε το έγγραφό σας στο OneNote:

```java
String dataDir = "Your Document Directory";
```

## Βήμα 2: Δημιουργία αντικειμένου εγγράφου

 Στιγμιότυπο α`Document` αντικείμενο:

```java
Document doc = new Document();
```

## Βήμα 3: Δημιουργία Σελίδων

Αρχικοποιήστε τα αντικείμενα της σελίδας και ορίστε τα επίπεδά τους:

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## Βήμα 4: Προσθήκη κόμβων στις σελίδες

### Προσθήκη κόμβων στην πρώτη σελίδα

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

### Προσθήκη κόμβων στη δεύτερη σελίδα

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

### Προσθήκη κόμβων στην τρίτη σελίδα

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

## Βήμα 5: Προσθήκη σελίδων στο έγγραφο

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## Βήμα 6: Αποθηκεύστε το έγγραφο

Αποθηκεύστε το έγγραφο του OneNote:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Εξαίρεση λαβής
}
```

Συγχαρητήρια! Δημιουργήσατε επιτυχώς ένα έγγραφο με ρίζα και δευτερεύουσες σελίδες στο OneNote χρησιμοποιώντας το Aspose.Note για Java.

## συμπέρασμα

Η οργάνωση των εγγράφων του OneNote με ιεραρχική δομή είναι απαραίτητη για καλύτερη διαχείριση και πλοήγηση. Με το Aspose.Note για Java, μπορείτε να δημιουργήσετε αποτελεσματικά έγγραφα με ρίζες και δευτερεύουσες σελίδες, παρέχοντας μια σαφή και οργανωμένη διάταξη για τις σημειώσεις σας.

## Συχνές ερωτήσεις

### Ε1: Μπορώ να δημιουργήσω πολλαπλά επίπεδα υποσελίδων χρησιμοποιώντας το Aspose.Note για Java;

A1: Ναι, μπορείτε να δημιουργήσετε πολλαπλά επίπεδα υποσελίδων ορίζοντας το κατάλληλο επίπεδο για κάθε σελίδα.

### Ε2: Είναι το Aspose.Note για Java συμβατό με διαφορετικά Java IDE;

A2: Ναι, το Aspose.Note για Java είναι συμβατό με δημοφιλή Java IDE όπως τα IntelliJ IDEA, Eclipse και NetBeans.

### Ε3: Μπορώ να προσαρμόσω τη μορφοποίηση του κειμένου στο έγγραφό μου στο OneNote;

A3: Ναι, μπορείτε να προσαρμόσετε τη γραμματοσειρά, το χρώμα, το μέγεθος και άλλες επιλογές μορφοποίησης χρησιμοποιώντας το Aspose.Note για τις δυνατότητες εμπλουτισμένου κειμένου της Java.

### Ε4: Το Aspose.Note για Java υποστηρίζει την αποθήκευση εγγράφων σε διαφορετικές μορφές;

A4: Ναι, το Aspose.Note για Java υποστηρίζει την αποθήκευση εγγράφων σε διάφορες μορφές, όπως BMP, PDF, PNG και άλλα.

### Ε5: Υπάρχει διαθέσιμη δοκιμαστική έκδοση για το Aspose.Note για Java;

A5: Ναι, μπορείτε να κάνετε λήψη μιας δωρεάν δοκιμαστικής έκδοσης του Aspose.Note για Java από τον ιστότοπο.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
