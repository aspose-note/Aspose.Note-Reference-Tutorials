---
title: Εφαρμογή αρίθμησης σε κείμενο στο Aspose.Σημείωση
linktitle: Εφαρμογή αρίθμησης σε κείμενο στο Aspose.Σημείωση
second_title: Aspose.Note .NET API
description: Μάθετε πώς να εφαρμόζετε την αρίθμηση κειμένου στο Aspose.Note για .NET με αυτό το ολοκληρωμένο σεμινάριο. Βελτιώστε τη μορφοποίηση του εγγράφου σας χωρίς κόπο.
type: docs
weight: 12
url: /el/net/text-manipulation/apply-numbering-on-text/
---
## Εισαγωγή
Το Aspose.Note για .NET παρέχει ισχυρά εργαλεία για χειρισμό εγγράφων σε εφαρμογές C#. Σε αυτό το σεμινάριο, θα διερευνήσουμε τη διαδικασία εφαρμογής αρίθμησης σε κείμενο χρησιμοποιώντας το Aspose.Note. Ακολουθήστε αυτές τις οδηγίες βήμα προς βήμα για να βελτιώσετε τη μορφοποίηση του εγγράφου σας χωρίς κόπο.
## Προαπαιτούμενα
Πριν βουτήξετε στο σεμινάριο, βεβαιωθείτε ότι έχετε τις ακόλουθες προϋποθέσεις:
- Βασική κατανόηση της γλώσσας προγραμματισμού C#.
-  Το Aspose.Note για .NET είναι εγκατεστημένο. Μπορείτε να το κατεβάσετε[εδώ](https://releases.aspose.com/note/net/).
- Ένα ολοκληρωμένο περιβάλλον ανάπτυξης (IDE) όπως το Visual Studio.
## Εισαγωγή χώρων ονομάτων
Για να ξεκινήσετε, φροντίστε να εισαγάγετε τους απαραίτητους χώρους ονομάτων στο έργο C#:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## Βήμα 1: Ρυθμίστε το έγγραφό σας
Ξεκινήστε δημιουργώντας ένα νέο έγγραφο και αρχικοποιώντας τα απαιτούμενα αντικείμενα:
```csharp
// Η διαδρομή προς τον κατάλογο εγγράφων.
string dataDir = "Your Document Directory";
// Δημιουργήστε ένα αντικείμενο της κλάσης Document
Document doc = new Document();
// Αρχικοποίηση αντικειμένου κλάσης σελίδας
Aspose.Note.Page page = new Aspose.Note.Page(doc);
// Αρχικοποίηση αντικειμένου κλάσης Outline
Outline outline = new Outline(doc);
```
## Βήμα 2: Ορίστε το προεπιλεγμένο στυλ
Ρυθμίστε το προεπιλεγμένο στυλ για το κείμενό σας χρησιμοποιώντας την κλάση ParagraphStyle:
```csharp
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## Βήμα 3: Εφαρμογή αρίθμησης
Αρχικοποιήστε αντικείμενα κλάσης OutlineElement και εφαρμόστε αρίθμηση σε κάθε στοιχείο:
```csharp
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
OutlineElement outlineElem2 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text2 = new RichText(doc) { Text = "Second", ParagraphStyle = defaultStyle };
outlineElem2.AppendChildLast(text2);
OutlineElement outlineElem3 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text3 = new RichText(doc) { Text = "Third", ParagraphStyle = defaultStyle };
outlineElem3.AppendChildLast(text3);
```
## Βήμα 4: Προσθέστε στοιχεία περίγραμμα
Προσθέστε τα στοιχεία του περιγράμματος στο περίγραμμα:
```csharp
outline.AppendChildLast(outlineElem1);
outline.AppendChildLast(outlineElem2);
outline.AppendChildLast(outlineElem3);
```
## Βήμα 5: Αποθηκεύστε το έγγραφο
Αποθηκεύστε το έγγραφο OneNote με την εφαρμοσμένη αρίθμηση:
```csharp
dataDir = dataDir + "ApplyNumberingOnText_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nNumbering applied successfully on a text.\nFile saved at " + dataDir); 
```
## συμπέρασμα
Συγχαρητήρια! Μάθατε με επιτυχία πώς να εφαρμόζετε αρίθμηση σε κείμενο στο Aspose.Note για .NET. Πειραματιστείτε με διαφορετικές επιλογές μορφοποίησης για να δημιουργήσετε οπτικά ελκυστικά έγγραφα χωρίς κόπο.
## Συχνές ερωτήσεις
### 1. Μπορώ να προσαρμόσω τη μορφή αρίθμησης;
Ναι, η κλάση NumberList σάς επιτρέπει να προσαρμόσετε τη μορφή αρίθμησης σύμφωνα με τις προτιμήσεις σας.
### 2. Υπάρχουν άλλες διαθέσιμες επιλογές μορφοποίησης;
Το Aspose.Note παρέχει ένα ευρύ φάσμα επιλογών μορφοποίησης, συμπεριλαμβανομένου του στυλ γραμματοσειράς, του χρώματος και άλλων.
### 3. Είναι το Aspose.Note συμβατό με το Visual Studio;
Απολύτως! Το Aspose.Note ενσωματώνεται άψογα με το Visual Studio για μια ομαλή εμπειρία ανάπτυξης.
### 4. Μπορώ να δοκιμάσω το Aspose.Note πριν από την αγορά;
 Σίγουρα! Μπορείτε να εξερευνήσετε μια δωρεάν δοκιμή[εδώ](https://releases.aspose.com/).
### 5. Πού μπορώ να λάβω υποστήριξη για το Aspose.Note;
 Για οποιαδήποτε βοήθεια ή απορία, επισκεφθείτε το[Aspose.Note φόρουμ](https://forum.aspose.com/c/note/28).