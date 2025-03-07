---
title: Προσθήκη κόμβου πίνακα με ετικέτα στο Aspose.Note
linktitle: Προσθήκη κόμβου πίνακα με ετικέτα στο Aspose.Note
second_title: Aspose.Note .NET API
description: Μάθετε πώς να προσθέτετε πίνακες με ετικέτες στο Aspose.Note για .NET. Βελτιώστε τις δεξιότητες χειρισμού εγγράφων σας μέσω προγραμματισμού.
weight: 11
url: /el/net/tag-management/add-table-node-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Προσθήκη κόμβου πίνακα με ετικέτα στο Aspose.Note

## Εισαγωγή

Σε αυτό το σεμινάριο, θα σας καθοδηγήσουμε στη διαδικασία προσθήκης ενός κόμβου πίνακα με μια ετικέτα χρησιμοποιώντας το Aspose.Note για .NET. Ακολουθήστε τα παρακάτω βήματα για να το πετύχετε.

## Εισαγωγή χώρων ονομάτων

Πριν ξεκινήσετε, φροντίστε να εισαγάγετε τους απαραίτητους χώρους ονομάτων για να εργαστείτε με το Aspose.Σημείωση:

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using Aspose.Note.Examples.CSharp.Tables;
```

## Προαπαιτούμενα

Βεβαιωθείτε ότι έχετε ρυθμίσει τις ακόλουθες προϋποθέσεις πριν προχωρήσετε:

1.  Εγκατάσταση: Κατεβάστε και εγκαταστήστε τη βιβλιοθήκη Aspose.Note για .NET από[εδώ](https://releases.aspose.com/note/net/).
2.  Άδεια χρήσης: Αποκτήστε άδεια χρήσης ή χρησιμοποιήστε α[προσωρινή άδεια](https://purchase.aspose.com/temporary-license/) για χρήση της βιβλιοθήκης.
3. Περιβάλλον ανάπτυξης: Ρυθμίστε ένα συμβατό περιβάλλον ανάπτυξης, όπως το Visual Studio.

## Βήμα 1: Αρχικοποίηση αντικειμένων εγγράφου και σελίδας

 Ξεκινήστε δημιουργώντας μια παρουσία του`Document` κλάση και αρχικοποίηση α`Page` αντικείμενο:

```csharp
Document doc = new Document();
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## Βήμα 2: Δημιουργία αντικειμένων πίνακα, σειράς και κελιού

 Αρχικοποιήστε το`Table`, `TableRow` , και`TableCell` αντικείμενα:

```csharp
TableRow row = new TableRow(doc);
TableCell cell = new TableCell(doc);
```

## Βήμα 3: Εισαγάγετε περιεχόμενο στο κελί

 Προσθέστε περιεχόμενο στο κελί χρησιμοποιώντας το`AppendChildLast` μέθοδος:

```csharp
cell.AppendChildLast(InsertTable.GetOutlineElementWithText(doc, "Single cell."));
```

## Βήμα 4: Αρχικοποίηση κόμβου πίνακα

 Αρχικοποιήστε το`Table` αντικείμενο με καθορισμένες ιδιότητες:

```csharp
Table table = new Table(doc)
{
    IsBordersVisible = true,
    Columns = { new TableColumn { Width = 70 } }
};
```

## Βήμα 5: Προσθήκη σειράς στον πίνακα

Προσθέστε τον κόμβο γραμμής στον πίνακα:

```csharp
table.AppendChildLast(row);
```

## Βήμα 6: Προσθήκη ετικέτας στον κόμβο πίνακα

Συμπεριλάβετε μια ετικέτα για τον κόμβο πίνακα:

```csharp
table.Tags.Add(NoteTag.CreateQuestionMark());
```

## Βήμα 7: Προσθέστε τον κόμβο πίνακα στο στοιχείο περίγραμμα

 Δημιουργήστε ένα`Outline` και`OutlineElement` για να προσθέσετε τον κόμβο του πίνακα:

```csharp
Outline outline = new Outline(doc);
OutlineElement outlineElem = new OutlineElement(doc);
outlineElem.AppendChildLast(table);
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## Βήμα 8: Αποθήκευση εγγράφου

Αποθηκεύστε το έγγραφο του OneNote:

```csharp
string dataDir = "Your Document Directory";
dataDir = dataDir + "AddTableNodeWithTag_out.one";
doc.Save(dataDir);
Console.WriteLine("\nTable node with tag added successfully.\nFile saved at " + dataDir);
```

Αφού ακολουθήσετε αυτά τα βήματα, θα πρέπει να έχετε προσθέσει με επιτυχία έναν κόμβο πίνακα με μια ετικέτα χρησιμοποιώντας το Aspose.Note για .NET.

## συμπέρασμα

Σε αυτό το σεμινάριο, καλύψαμε τη διαδικασία προσθήκης ενός κόμβου πίνακα με μια ετικέτα στο Aspose.Note για .NET. Ακολουθώντας αυτά τα βήματα, μπορείτε να χειρίζεστε αποτελεσματικά τα έγγραφα του OneNote μέσω προγραμματισμού, βελτιώνοντας τις δυνατότητες διαχείρισης εγγράφων σας.

## Συχνές ερωτήσεις

### Ε1: Είναι το Aspose.Note συμβατό με όλες τις εκδόσεις του .NET;

A1: Το Aspose.Note για .NET υποστηρίζει εκδόσεις .NET Framework 2.0 και νεότερες, συμπεριλαμβανομένων των .NET Core και .NET Standard.

### Ε2: Μπορώ να δοκιμάσω το Aspose.Note πριν αγοράσω μια άδεια;

 A2: Ναι, μπορείτε να αποκτήσετε μια δωρεάν δοκιμή του Aspose.Note από[εδώ](https://releases.aspose.com/).

### Ε3: Πώς μπορώ να αποκτήσω μια προσωρινή άδεια για το Aspose.Note;

 A3: Μπορείτε να λάβετε μια προσωρινή άδεια από[αυτός ο σύνδεσμος](https://purchase.aspose.com/temporary-license/), η οποία ισχύει για 30 ημέρες.

### Ε4: Το Aspose.Note υποστηρίζει την κρυπτογράφηση εγγράφων;

A4: Ναι, το Aspose.Note παρέχει υποστήριξη για την κρυπτογράφηση εγγράφων OneNote για τη διασφάλιση της ασφάλειας των δεδομένων.

### Ε5: Είναι διαθέσιμη τεχνική υποστήριξη για τους χρήστες του Aspose.Note;

 A5: Ναι, παρέχεται τεχνική υποστήριξη μέσω των φόρουμ Aspose[εδώ](https://forum.aspose.com/c/note/28), όπου μπορείτε να ζητήσετε βοήθεια από ειδικούς.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
