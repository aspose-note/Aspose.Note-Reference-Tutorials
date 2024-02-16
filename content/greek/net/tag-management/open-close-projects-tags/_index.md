---
title: Άνοιγμα και κλείσιμο έργων με ετικέτες στο Aspose.Note
linktitle: Άνοιγμα και κλείσιμο έργων με ετικέτες στο Aspose.Note
second_title: Aspose.Note .NET API
description: Μάθετε πώς να χειρίζεστε αρχεία Microsoft OneNote μέσω προγραμματισμού χρησιμοποιώντας το Aspose.Note για .NET. Ανοίξτε και κλείστε έργα με ετικέτες αποτελεσματικά.
type: docs
weight: 15
url: /el/net/tag-management/open-close-projects-tags/
---
## Εισαγωγή

Σε αυτό το σεμινάριο, θα μάθουμε πώς να χρησιμοποιούμε το Aspose.Note για .NET για να ανοίγουμε και να κλείνουμε έργα με ετικέτες. Το Aspose.Note είναι ένα ισχυρό API που επιτρέπει στους προγραμματιστές να εργάζονται με αρχεία Microsoft OneNote μέσω προγραμματισμού, επιτρέποντας εργασίες όπως ο χειρισμός κειμένου, εικόνων και ετικετών μέσα στα έγγραφα.

## Προαπαιτούμενα

Πριν ξεκινήσουμε, βεβαιωθείτε ότι έχετε ρυθμίσει τις ακόλουθες προϋποθέσεις:

## Εισαγωγή χώρων ονομάτων

```csharp
using System.IO;
using System.Linq;
```

Τώρα ας αναλύσουμε κάθε παράδειγμα σε πολλά βήματα:

## Βήμα 1: Φορτώστε το έγγραφο

Αρχικά, πρέπει να φορτώσουμε το έγγραφο στο Aspose.Note.

```csharp
string dataDir = "Your Document Directory";
var oneFile = new Document(Path.Combine(dataDir, "ProjectNotes.one"));
```

## Βήμα 2: Κλείστε τα στοιχεία του έργου C

Τώρα, ας κλείσουμε όλα τα στοιχεία του πλαισίου ελέγχου που σχετίζονται με το «Έργο Γ».

```csharp
foreach (var node in oneFile.GetChildNodes<ITaggable>())
{
    foreach (var checkBox in node.Tags.OfType<CheckBox>())
    {
        if (checkBox.Label.Contains("Project C") && !checkBox.Checked)
        {
            checkBox.SetCompleted();
        }
    }
}
```

## Βήμα 3: Αποθηκεύστε τις σημειώσεις C Closed Project C

Αποθηκεύστε το τροποποιημένο έγγραφο με κλειστά στοιχεία «Project C».

```csharp
oneFile.Save("Path to save the closed Project C notes");
```

## Βήμα 4: Ανοίξτε το Project C Items

Στη συνέχεια, ας ανοίξουμε όλα τα στοιχεία του πλαισίου ελέγχου που σχετίζονται με το «Έργο Γ».

```csharp
var oneFile = new Document("Path to the closed Project C notes");

foreach (var node in oneFile.GetChildNodes<ITaggable>())
{
    foreach (var checkBox in node.Tags.OfType<CheckBox>())
    {
        if (checkBox.Label.Contains("Project C") && checkBox.Checked)
        {
            checkBox.SetOpen();
        }
    }
}
```

## Βήμα 5: Αποθηκεύστε τις Σημειώσεις Open Project C

Αποθηκεύστε το τροποποιημένο έγγραφο με τα ανοιγμένα στοιχεία «Project C».

```csharp
oneFile.Save(Path.Combine(dataDir, "ProjectNoteWithOpenProjectC.one"));
```

Τώρα έχετε μάθει πώς να ανοίγετε και να κλείνετε έργα με ετικέτες στο Aspose.Note χρησιμοποιώντας .NET.

## συμπέρασμα

Το Aspose.Note για .NET παρέχει έναν βολικό τρόπο χειρισμού εγγράφων OneNote μέσω προγραμματισμού. Ακολουθώντας αυτό το σεμινάριο, μπορείτε να διαχειριστείτε αποτελεσματικά τα έργα σας ανοίγοντας και κλείνοντας στοιχεία χρησιμοποιώντας ετικέτες.

## Συχνές ερωτήσεις

### Ε1: Είναι το Aspose.Note συμβατό με όλες τις εκδόσεις του OneNote;

A1: Το Aspose.Note υποστηρίζει το Microsoft OneNote 2010 και νεότερες εκδόσεις.

### Ε2: Μπορώ να χρησιμοποιήσω το Aspose.Note για εμπορικά έργα;

 A2: Ναι, μπορείτε να χρησιμοποιήσετε το Aspose.Note τόσο για προσωπικά όσο και για εμπορικά έργα. Επίσκεψη[εδώ](https://purchase.aspose.com/buy) να αγοράσει άδεια.

### Ε3: Το Aspose.Note προσφέρει δωρεάν δοκιμή;

 A3: Ναι, μπορείτε να λάβετε μια δωρεάν δοκιμή[εδώ](https://releases.aspose.com/).

### Ε4: Πού μπορώ να βρω τεκμηρίωση για το Aspose.Note;

 A4: Μπορείτε να βρείτε την τεκμηρίωση[εδώ](https://reference.aspose.com/note/net/).

### Ε5: Πού μπορώ να λάβω υποστήριξη για το Aspose.Note;

 A5: Για υποστήριξη, μπορείτε να επισκεφτείτε το Aspose.Note[δικαστήριο](https://forum.aspose.com/c/note/28).