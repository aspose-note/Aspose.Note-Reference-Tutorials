---
title: Αποθήκευση με χρήση καθορισμένων γραμματοσειρών στο Aspose.Note
linktitle: Αποθήκευση με χρήση καθορισμένων γραμματοσειρών στο Aspose.Note
second_title: Aspose.Note .NET API
description: Μάθετε πώς να αποθηκεύετε έγγραφα με καθορισμένες γραμματοσειρές στο Aspose.Note για .NET. Προσαρμόστε εύκολα τις ρυθμίσεις γραμματοσειράς για συνεπή μορφοποίηση εγγράφων.
type: docs
weight: 28
url: /el/net/loading-and-saving-operations/save-using-specified-fonts/
---
## Εισαγωγή

Σε αυτό το σεμινάριο, θα μάθουμε πώς να αποθηκεύουμε έγγραφα χρησιμοποιώντας καθορισμένες γραμματοσειρές στο Aspose.Note για .NET. Θα εξερευνήσουμε διάφορες μεθόδους για να το πετύχουμε αυτό, βήμα προς βήμα.

## Προαπαιτούμενα

Πριν ξεκινήσουμε, βεβαιωθείτε ότι έχετε τα εξής:

1.  Aspose.Note για .NET: Βεβαιωθείτε ότι έχετε εγκαταστήσει το Aspose.Note για .NET. Μπορείτε να το κατεβάσετε από[εδώ](https://releases.aspose.com/note/net/).

2. Περιβάλλον ανάπτυξης: Χρειάζεστε ένα περιβάλλον ανάπτυξης που έχει ρυθμιστεί για την ανάπτυξη .NET.

## Εισαγωγή χώρων ονομάτων

Αρχικά, ας εισάγουμε τους απαραίτητους χώρους ονομάτων:

```csharp
using System;
using System.IO;

using Aspose.Note.Fonts;
using Aspose.Note.Saving;

```

## Βήμα 1: Αποθήκευση με το προεπιλεγμένο όνομα γραμματοσειράς

Σε αυτό το βήμα, θα αποθηκεύσουμε ένα έγγραφο χρησιμοποιώντας ένα καθορισμένο προεπιλεγμένο όνομα γραμματοσειράς.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName()
{
    // Η διαδρομή προς τον κατάλογο εγγράφων.
    string dataDir = "Your Document Directory";

    // Φορτώστε το έγγραφο στο Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Αποθηκεύστε το έγγραφο ως PDF με καθορισμένη προεπιλεγμένη γραμματοσειρά.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFont("Times New Roman")
                          });
}
```

## Βήμα 2: Αποθήκευση με προεπιλεγμένη γραμματοσειρά από το Αρχείο

Στη συνέχεια, ας αποθηκεύσουμε ένα έγγραφο χρησιμοποιώντας μια προεπιλεγμένη γραμματοσειρά που έχει φορτωθεί από ένα αρχείο.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile()
{
    // Η διαδρομή προς τον κατάλογο εγγράφων.
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    // Φορτώστε το έγγραφο στο Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Αποθηκεύστε το έγγραφο ως PDF με προεπιλεγμένη γραμματοσειρά φορτωμένη από το αρχείο.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromFile(fontFile)
                          });
}
```

## Βήμα 3: Αποθήκευση με προεπιλεγμένη γραμματοσειρά από τη ροή

Τέλος, ας αποθηκεύσουμε ένα έγγραφο χρησιμοποιώντας μια προεπιλεγμένη γραμματοσειρά που έχει φορτωθεί από μια ροή.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream()
{
    // Η διαδρομή προς τον κατάλογο εγγράφων.
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    // Φορτώστε το έγγραφο στο Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Αποθηκεύστε το έγγραφο ως PDF με προεπιλεγμένη γραμματοσειρά φορτωμένη από τη ροή.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf";

    using (var stream = File.Open(fontFile, FileMode.Open, FileAccess.Read, FileShare.Read))
    {
        oneFile.Save(dataDir, new PdfSaveOptions()
                              {
                                  FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromStream(stream)
                              });
    }
}
```

## συμπέρασμα

Σε αυτό το σεμινάριο, εξερευνήσαμε τον τρόπο αποθήκευσης εγγράφων χρησιμοποιώντας καθορισμένες γραμματοσειρές στο Aspose.Note για .NET. Ακολουθώντας αυτά τα βήματα, μπορείτε να προσαρμόσετε τις ρυθμίσεις γραμματοσειράς σύμφωνα με τις απαιτήσεις σας, διασφαλίζοντας ότι τα έγγραφά σας έχουν μορφοποιηθεί όπως επιθυμείτε.

## Συχνές ερωτήσεις

### Ε1: Μπορώ να χρησιμοποιήσω οποιαδήποτε γραμματοσειρά για την αποθήκευση εγγράφων στο Aspose.Note;

A1: Ναι, μπορείτε να καθορίσετε οποιαδήποτε γραμματοσειρά για την αποθήκευση εγγράφων. Απλώς βεβαιωθείτε ότι το αρχείο γραμματοσειράς είναι προσβάσιμο και φορτωμένο σωστά.

### Ε2: Είναι το Aspose.Note συμβατό με διαφορετικές μορφές εγγράφων;

A2: Το Aspose.Note λειτουργεί κυρίως με έγγραφα OneNote, αλλά παρέχει επιλογές αποθήκευσης σε διάφορες μορφές, συμπεριλαμβανομένου του PDF.

### Ε3: Πώς μπορώ να χειριστώ τις γραμματοσειρές που λείπουν κατά την αποθήκευση εγγράφων;

A3: Το Aspose.Note προσφέρει επιλογές για χρήση προεπιλεγμένων γραμματοσειρών σε περίπτωση που λείπει η καθορισμένη γραμματοσειρά, διασφαλίζοντας συνεπή μορφοποίηση εγγράφων.

### Ε4: Το Aspose.Note υποστηρίζει την ενσωμάτωση γραμματοσειράς σε έγγραφα εξόδου;

A4: Ναι, το Aspose.Note επιτρέπει την ενσωμάτωση γραμματοσειρών για τη διασφάλιση της φορητότητας των εγγράφων και τη συνεπή απόδοση σε διαφορετικές πλατφόρμες.

### Ε5: Πού μπορώ να λάβω περαιτέρω βοήθεια με το Aspose.Note;

 A5: Για περαιτέρω βοήθεια ή τεχνική υποστήριξη, μπορείτε να επισκεφτείτε το[Aspose.Note φόρουμ](https://forum.aspose.com/c/note/28).