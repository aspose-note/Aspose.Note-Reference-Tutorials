---
title: Εισαγάγετε τη λίστα κινεζικών αριθμών στο κείμενο Aspose.Note
linktitle: Εισαγάγετε τη λίστα κινεζικών αριθμών στο κείμενο Aspose.Note
second_title: Aspose.Note .NET API
description: Μάθετε πώς να εισάγετε λίστες κινεζικών αριθμών στο Aspose.Note για έγγραφα .NET χωρίς κόπο. Αναβαθμίστε τις δεξιότητές σας στη μορφοποίηση εγγράφων με αυτόν τον οδηγό βήμα προς βήμα.
weight: 20
url: /el/net/text-manipulation/insert-chinese-number-list/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Εισαγάγετε τη λίστα κινεζικών αριθμών στο κείμενο Aspose.Note

## Εισαγωγή
Θέλετε να βελτιώσετε τις δεξιότητές σας στο Aspose.Note για .NET ενσωματώνοντας λίστες κινεζικών αριθμών στα έγγραφά σας; Αν ναι, είστε στο σωστό μέρος! Σε αυτό το σεμινάριο, θα σας καθοδηγήσουμε στη διαδικασία εισαγωγής λιστών κινεζικών αριθμών χρησιμοποιώντας το Aspose.Note για .NET. Αυτή η ισχυρή βιβλιοθήκη σάς επιτρέπει να χειρίζεστε τα έγγραφα του OneNote απρόσκοπτα.
## Προαπαιτούμενα
Πριν ξεκινήσουμε το σεμινάριο, βεβαιωθείτε ότι έχετε τις ακόλουθες προϋποθέσεις:
- Βασικές γνώσεις προγραμματισμού C#.
-  Το Aspose.Note για .NET είναι εγκατεστημένο. Μπορείτε να το κατεβάσετε[εδώ](https://releases.aspose.com/note/net/).
## Εισαγωγή χώρων ονομάτων
Για να ξεκινήσετε, εισαγάγετε τους απαραίτητους χώρους ονομάτων στο έργο σας:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## Βήμα 1: Αρχικοποιήστε το έγγραφο OneNote
```csharp
string dataDir = "Your Document Directory";
Aspose.Note.Document doc = new Aspose.Note.Document();
```
## Βήμα 2: Αρχικοποιήστε τη σελίδα OneNote
```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
Outline outline = new Outline(doc);
```
## Βήμα 3: Εφαρμογή ρυθμίσεων στυλ κειμένου
```csharp
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## Βήμα 4: Δημιουργήστε στοιχεία περιγράμματος
Τώρα, ας δημιουργήσουμε τρία στοιχεία περιγράμματος με κινεζικές λίστες αριθμών:
### Βήμα 4.1: Πρώτο στοιχείο
```csharp
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
```
### Βήμα 4.2: Δεύτερο στοιχείο
```csharp
OutlineElement outlineElem2 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text2 = new RichText(doc) { Text = "Second", ParagraphStyle = defaultStyle };
outlineElem2.AppendChildLast(text2);
```
### Βήμα 4.3: Τρίτο στοιχείο
```csharp
OutlineElement outlineElem3 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text3 = new RichText(doc) { Text = "Third", ParagraphStyle = defaultStyle };
outlineElem3.AppendChildLast(text3);
```
## Βήμα 5: Προσθήκη στοιχείων στο περίγραμμα
```csharp
outline.AppendChildLast(outlineElem1);
outline.AppendChildLast(outlineElem2);
outline.AppendChildLast(outlineElem3);
```
## Βήμα 6: Προσθήκη Περίληψης στη Σελίδα
```csharp
page.AppendChildLast(outline);
```
## Βήμα 7: Προσθήκη σελίδας σε έγγραφο
```csharp
doc.AppendChildLast(page);
```
## Βήμα 8: Αποθήκευση εγγράφου OneNote
```csharp
dataDir = dataDir + "InsertChineseNumberList_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nChinese number list inserted successfully.\nFile saved at " + dataDir);
```
Συγχαρητήρια! Εισαγάγατε με επιτυχία λίστες κινεζικών αριθμών στο έγγραφο Aspose.Note χρησιμοποιώντας τη βιβλιοθήκη .NET.
## συμπέρασμα
Σε αυτό το σεμινάριο, καλύψαμε τη διαδικασία βήμα προς βήμα ενσωμάτωσης λιστών κινεζικών αριθμών στα έγγραφα Aspose.Note για έγγραφα .NET. Βελτιώστε τις δεξιότητές σας στη μορφοποίηση εγγράφων και κάντε το περιεχόμενό σας πιο ελκυστικό με αυτές τις τεχνικές.
## Συχνές ερωτήσεις
### Ε: Μπορώ να προσαρμόσω τη μορφοποίηση λιστών κινεζικών αριθμών;
 Α: Ναι, μπορείτε να προσαρμόσετε τη μορφοποίηση προσαρμόζοντας τις παραμέτρους στο`NumberList` κατασκευαστής.
### Ε: Είναι το Aspose.Note συμβατό με την πιο πρόσφατη έκδοση του .NET;
Α: Ναι, το Aspose.Note ενημερώνεται τακτικά για να υποστηρίζει τις πιο πρόσφατες εκδόσεις του .NET.
### Ε: Πού μπορώ να βρω επιπλέον παραδείγματα και τεκμηρίωση;
Α: Εξερευνήστε την περιεκτική[Aspose.Note τεκμηρίωση](https://reference.aspose.com/note/net/).
### Ε: Πώς μπορώ να πάρω μια προσωρινή άδεια για το Aspose.Note;
 Α: Λάβετε μια προσωρινή άδεια[εδώ](https://purchase.aspose.com/temporary-license/).
### Ε: Πού μπορώ να αναζητήσω βοήθεια ή να συζητήσω ερωτήματα σχετικά με το Aspose.Note;
 Α: Επισκεφθείτε το[Φόρουμ υποστήριξης Aspose.Note](https://forum.aspose.com/c/note/28) για κοινοτική υποστήριξη.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
