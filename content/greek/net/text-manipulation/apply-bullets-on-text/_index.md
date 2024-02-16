---
title: Εφαρμογή κουκκίδων σε κείμενο στο Aspose.Note
linktitle: Εφαρμογή κουκκίδων σε κείμενο στο Aspose.Note
second_title: Aspose.Note .NET API
description: Μάθετε πώς να εφαρμόζετε κουκκίδες σε κείμενο στο Aspose.Note για .NET για να βελτιώσετε τα έγγραφά σας στο OneNote. Ακολουθήστε αυτόν τον οδηγό βήμα προς βήμα για αποτελεσματική μορφοποίηση.
type: docs
weight: 10
url: /el/net/text-manipulation/apply-bullets-on-text/
---
## Εισαγωγή
Καλώς ήρθατε σε αυτόν τον αναλυτικό οδηγό για την εφαρμογή κουκκίδων σε κείμενο χρησιμοποιώντας το Aspose.Note για .NET. Το Aspose.Note είναι μια ισχυρή βιβλιοθήκη που επιτρέπει στους προγραμματιστές να εργάζονται απρόσκοπτα με τα αρχεία Microsoft OneNote στις εφαρμογές τους .NET. Σε αυτό το σεμινάριο, θα σας καθοδηγήσουμε στη διαδικασία εφαρμογής κουκκίδων στο κείμενο, βελτιώνοντας την οπτική ελκυστικότητα των εγγράφων σας στο OneNote.
## Προαπαιτούμενα
Πριν ξεκινήσουμε το σεμινάριο, βεβαιωθείτε ότι έχετε τις ακόλουθες προϋποθέσεις:
- Βασικές γνώσεις προγραμματισμού C# και .NET.
-  Εγκαταστάθηκε το Aspose.Note για τη βιβλιοθήκη .NET. Μπορείτε να το κατεβάσετε[εδώ](https://releases.aspose.com/note/net/).
## Εισαγωγή χώρων ονομάτων
Στον κώδικα C#, φροντίστε να συμπεριλάβετε τους απαραίτητους χώρους ονομάτων:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## Βήμα 1: Ρυθμίστε το έγγραφό σας
```csharp
// Η διαδρομή προς τον κατάλογο εγγράφων.
string dataDir = "Your Document Directory";
//Δημιουργήστε ένα αντικείμενο της κλάσης Document
Aspose.Note.Document doc = new Aspose.Note.Document();
```
## Βήμα 2: Αρχικοποίηση σελίδας και περίγραμμα
```csharp
// Αρχικοποίηση αντικειμένου κλάσης σελίδας
Aspose.Note.Page page = new Aspose.Note.Page(doc);
// Αρχικοποίηση αντικειμένου κλάσης Outline
Outline outline = new Outline(doc);
```
## Βήμα 3: Ορίστε το προεπιλεγμένο στυλ κειμένου
```csharp
// Εκκινήστε το αντικείμενο κλάσης TextStyle και ορίστε τις ιδιότητες μορφοποίησης
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## Βήμα 4: Δημιουργήστε στοιχεία περιγράμματος με κουκκίδες
```csharp
// Αρχικοποιήστε αντικείμενα κλάσης OutlineElement και εφαρμόστε κουκκίδες
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("*", "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
// Επαναλάβετε για άλλα στοιχεία περιγράμματος
```
## Βήμα 5: Προσθέστε στοιχεία περιγράμματος στο περίγραμμα
```csharp
// Προσθέστε στοιχεία περιγράμματος
outline.AppendChildLast(outlineElem1);
// Επαναλάβετε για άλλα στοιχεία περιγράμματος
```
## Βήμα 6: Προσθέστε περίγραμμα στη σελίδα
```csharp
// Προσθήκη κόμβου Outline
page.AppendChildLast(outline);
```
## Βήμα 7: Προσθήκη σελίδας στο Έγγραφο
```csharp
//Προσθήκη κόμβου σελίδας
doc.AppendChildLast(page);
```
## Βήμα 8: Αποθηκεύστε το έγγραφο OneNote
```csharp
// Αποθήκευση εγγράφου OneNote
dataDir = dataDir + "ApplyBulletsOnText_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nBullets applied successfully on a text.\nFile saved at " + dataDir); 
```
## συμπέρασμα
Συγχαρητήρια! Έχετε μάθει με επιτυχία πώς να εφαρμόζετε κουκκίδες σε κείμενο χρησιμοποιώντας το Aspose.Note για .NET. Αυτή η δυνατότητα μπορεί να βελτιώσει σημαντικά τη μορφοποίηση των εγγράφων σας στο OneNote, καθιστώντας τα πιο ελκυστικά οπτικά.
## Συχνές ερωτήσεις
### Μπορώ να εφαρμόσω διαφορετικά στυλ κουκκίδων σε κάθε στοιχείο της λίστας;
 Ναι, μπορείτε να προσαρμόσετε τα στυλ κουκκίδων τροποποιώντας το`NumberList` ιδιότητες για το καθένα`OutlineElement`.
### Είναι το Aspose.Note συμβατό με την πιο πρόσφατη έκδοση του Microsoft OneNote;
Το Aspose.Note υποστηρίζει διάφορες εκδόσεις του Microsoft OneNote, διασφαλίζοντας τη συμβατότητα τόσο με παλαιότερες όσο και με νεότερες εκδόσεις.
### Μπορώ να χρησιμοποιήσω το Aspose.Note για εμπορικούς σκοπούς;
 Ναι, μπορείτε να χρησιμοποιήσετε το Aspose.Note για .NET σε εμπορικά έργα. Για να λάβετε άδεια, επισκεφτείτε[εδώ](https://purchase.aspose.com/buy).
### Υπάρχει διαθέσιμη δοκιμαστική έκδοση για το Aspose.Note για .NET;
 Ναι, μπορείτε να κάνετε λήψη μιας δωρεάν δοκιμής[εδώ](https://releases.aspose.com/).
### Πού μπορώ να βρω πρόσθετη υποστήριξη και πόρους;
 Μπορείτε να επισκεφτείτε το φόρουμ κοινότητας Aspose.Note[εδώ](https://forum.aspose.com/c/note/28) για υποστήριξη και συζητήσεις.