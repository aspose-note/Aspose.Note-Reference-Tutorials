---
title: Προσθήκη κόμβου εικόνας με ετικέτα στο Aspose.Note
linktitle: Προσθήκη κόμβου εικόνας με ετικέτα στο Aspose.Note
second_title: Aspose.Note .NET API
description: Μάθετε πώς να βελτιώσετε τα έγγραφά σας στο OneNote προσθέτοντας εικόνες με προσαρμοσμένες ετικέτες χρησιμοποιώντας το Aspose.Note για .NET.
weight: 10
url: /el/net/tag-management/add-image-node-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Προσθήκη κόμβου εικόνας με ετικέτα στο Aspose.Note

## Εισαγωγή

Σε αυτό το σεμινάριο, θα διερευνήσουμε πώς να προσθέσετε έναν κόμβο εικόνας με μια ετικέτα χρησιμοποιώντας το Aspose.Note για .NET. Αυτή η δυνατότητα σάς επιτρέπει να βελτιώσετε τα έγγραφά σας στο OneNote προσθέτοντας εικόνες με προσαρμοσμένες ετικέτες.

## Προαπαιτούμενα

Πριν ξεκινήσετε, βεβαιωθείτε ότι έχετε τα εξής:

1. Visual Studio: Εγκαταστήστε το Visual Studio IDE στο σύστημά σας.
2.  Aspose.Note για .NET: Κάντε λήψη και εγκαταστήστε τη βιβλιοθήκη Aspose.Note για .NET από τη[σύνδεσμος λήψης](https://releases.aspose.com/note/net/).
3. Βασικές γνώσεις: Εξοικειωθείτε με τη γλώσσα προγραμματισμού C# και το πλαίσιο .NET.

## Εισαγωγή χώρων ονομάτων

Πρώτα, φροντίστε να συμπεριλάβετε τους απαραίτητους χώρους ονομάτων στον κώδικα C#:

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

## Βήμα 1: Αρχικοποίηση αντικειμένων εγγράφου και σελίδας

 Ξεκινήστε δημιουργώντας ένα παράδειγμα του`Document` τάξη και α`Page` αντικείμενο:

```csharp
Document doc = new Document();
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## Βήμα 2: Αρχικοποίηση αντικειμένων Outline και OutlineElement

 Στη συνέχεια, αρχικοποίηση`Outline` και`OutlineElement` αντικείμενα:

```csharp
Outline outline = new Outline(doc);
OutlineElement outlineElem = new OutlineElement(doc);
```

## Βήμα 3: Φόρτωση και εισαγωγή εικόνας

Φορτώστε την επιθυμητή εικόνα και εισαγάγετε την στον κόμβο του εγγράφου:

```csharp
Aspose.Note.Image image = new Aspose.Note.Image(doc, "path_to_your_image.jpg");
outlineElem.AppendChildLast(image);
```

## Βήμα 4: Προσθήκη ετικέτας στην εικόνα

Προσθέστε μια προσαρμοσμένη ετικέτα στην εικόνα:

```csharp
image.Tags.Add(NoteTag.CreateYellowStar());
```

## Βήμα 5: Προσθήκη στοιχείου περιγράμματος και κόμβων σελίδας

Προσθέστε το στοιχείο περιγράμματος και τους κόμβους περιγράμματος στη σελίδα:

```csharp
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
```

## Βήμα 6: Αποθηκεύστε το έγγραφο

Αποθηκεύστε το τροποποιημένο έγγραφο του OneNote:

```csharp
doc.AppendChildLast(page);
string outputFilePath = "output_path/AddImageNodeWithTag_out.one";
doc.Save(outputFilePath);
```

## συμπέρασμα

Ακολουθώντας αυτά τα βήματα, μπορείτε να προσθέσετε απρόσκοπτα έναν κόμβο εικόνας με μια προσαρμοσμένη ετικέτα χρησιμοποιώντας το Aspose.Note για .NET, εμπλουτίζοντας τα έγγραφά σας στο OneNote με εξατομικευμένα γραφικά.

## Συχνές ερωτήσεις

### Ε1: Μπορώ να προσθέσω πολλές εικόνες με διαφορετικές ετικέτες σε ένα έγγραφο χρησιμοποιώντας το Aspose.Note;

A1: Ναι, μπορείτε να προσθέσετε πολλές εικόνες με διαφορετικές ετικέτες ακολουθώντας παρόμοια βήματα για κάθε εικόνα.

### Ε2: Είναι το Aspose.Note συμβατό με όλες τις εκδόσεις του OneNote;

A2: Το Aspose.Note υποστηρίζει διάφορες εκδόσεις του OneNote, διασφαλίζοντας τη συμβατότητα σε διαφορετικά περιβάλλοντα.

### Ε3: Μπορώ να προσαρμόσω την εμφάνιση της ετικέτας που προστέθηκε στην εικόνα;

A3: Ναι, το Aspose.Note παρέχει ευελιξία στην προσαρμογή της εμφάνισης της ετικέτας σύμφωνα με τις προτιμήσεις σας.

### Ε4: Το Aspose.Note προσφέρει υποστήριξη για την προσθήκη εικόνων από διευθύνσεις URL;

A4: Το Aspose.Note υποστηρίζει κυρίως την προσθήκη εικόνων από τοπικούς καταλόγους, αλλά μπορείτε να ενσωματώσετε εξωτερικές εικόνες κατεβάζοντάς τες πρώτα τοπικά.

### Ε5: Υπάρχουν περιορισμοί στο μέγεθος ή τη μορφή των εικόνων που μπορούν να προστεθούν;

A5: Το Aspose.Note υποστηρίζει ένα ευρύ φάσμα μορφών εικόνας και δεν επιβάλλει αυστηρούς περιορισμούς στο μέγεθος της εικόνας, επιτρέποντάς σας να ενσωματώνετε διάφορα οπτικά στοιχεία στα έγγραφά σας.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
