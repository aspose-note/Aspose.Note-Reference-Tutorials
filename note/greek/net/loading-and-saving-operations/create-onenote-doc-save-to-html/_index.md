---
title: Δημιουργήστε ένα έγγραφο OneNote και αποθηκεύστε το σε HTML στο Aspose.Note
linktitle: Δημιουργήστε ένα έγγραφο OneNote και αποθηκεύστε το σε HTML στο Aspose.Note
second_title: Aspose.Note .NET API
description: Μάθετε πώς να δημιουργείτε και να αποθηκεύετε έγγραφα Microsoft OneNote σε μορφή HTML σε εφαρμογές .NET χρησιμοποιώντας το Aspose.Note API. Ακολουθήστε το περιεκτικό μας σεμινάριο με παραδείγματα βήμα προς βήμα.
type: docs
weight: 14
url: /el/net/loading-and-saving-operations/create-onenote-doc-save-to-html/
---
## Εισαγωγή

Το Aspose.Note για .NET είναι ένα ισχυρό API που επιτρέπει στους προγραμματιστές να εργάζονται με έγγραφα του Microsoft OneNote μέσω προγραμματισμού στις εφαρμογές τους .NET. Με το Aspose.Note, μπορείτε να δημιουργείτε, να χειρίζεστε και να μετατρέπετε αρχεία OneNote χωρίς κόπο. Σε αυτό το σεμινάριο, θα διερευνήσουμε πώς να δημιουργήσετε ένα έγγραφο OneNote και να το αποθηκεύσετε σε μορφή HTML χρησιμοποιώντας διάφορες επιλογές που παρέχονται από το Aspose.Note για .NET API.

## Προαπαιτούμενα

Πριν ξεκινήσουμε, βεβαιωθείτε ότι έχετε τις ακόλουθες προϋποθέσεις:

- Βασικές γνώσεις γλώσσας προγραμματισμού C#.
- Το Visual Studio είναι εγκατεστημένο στο σύστημά σας.
-  Aspose.Note για .NET API που είναι εγκατεστημένο στο έργο σας. Μπορείτε να το κατεβάσετε από[εδώ](https://releases.aspose.com/note/net/).
- Εξοικείωση με τη δομή των εγγράφων του Microsoft OneNote.

## Εισαγωγή χώρων ονομάτων

Πριν βουτήξουμε στο τμήμα κωδικοποίησης, ας εισαγάγουμε τους απαραίτητους χώρους ονομάτων:

```csharp
using System;
using System.Drawing;
using System.Globalization;
using System.IO;

using Aspose.Note.Saving;
using Aspose.Note.Saving.Html;

```

Τώρα, ας αναλύσουμε κάθε παράδειγμα σε πολλά βήματα και ας δούμε πώς να δημιουργήσετε ένα έγγραφο OneNote και να το αποθηκεύσετε σε μορφή HTML χρησιμοποιώντας το Aspose.Note για .NET.

## Βήμα 1: Δημιουργήστε ένα έγγραφο OneNote με προεπιλεγμένες επιλογές

```csharp
public static void CreateAndSaveToHTMLUsingDefaultOptions()
{
    // Αρχικοποιήστε το έγγραφο OneNote
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    // Προεπιλεγμένο στυλ για όλο το κείμενο στο έγγραφο.
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    // Αποθήκευση σε μορφή HTML
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateOneNoteDocAndSaveToHTML_out.html");
    doc.Save(outputPath);

    Console.WriteLine("\nOneNote document created successfully.\nFile saved at " + outputPath);
}
```

Σε αυτό το βήμα, αρχικοποιούμε ένα νέο έγγραφο του OneNote, προσθέτουμε μια σελίδα με τίτλο και το αποθηκεύουμε σε μορφή HTML χρησιμοποιώντας τις προεπιλεγμένες επιλογές.

## Βήμα 2: Δημιουργήστε και αποθηκεύστε ένα συγκεκριμένο εύρος σελίδων σε HTML

```csharp
public static void CreateAndSavePageRange()
{
    // Αρχικοποιήστε το έγγραφο OneNote
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    // Προεπιλεγμένο στυλ για όλο το κείμενο στο έγγραφο.
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    // Αποθήκευση σε μορφή HTML
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateAndSavePageRange_out.html");
    doc.Save(outputPath, new HtmlSaveOptions { PageCount = 1, PageIndex = 0 });

    Console.WriteLine("\nOneNote document created successfully and saved as page range.\nFile saved at " + outputPath);
}
```

Εδώ, δείχνουμε πώς να δημιουργήσετε ένα έγγραφο και να αποθηκεύσετε μια συγκεκριμένη περιοχή σελίδων σε μορφή HTML.

## Βήμα 3: Αποθήκευση ως HTML στη ροή μνήμης με ενσωματωμένους πόρους

```csharp
public static void SaveAsHTMLToMemoryStreamWithEmbeddedResources()
{
    // Φορτώστε το έγγραφο του OneNote
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Καθορίστε επιλογές αποθήκευσης HTML
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportEmbedded,
        ExportFonts = ResourceExportType.ExportEmbedded,
        ExportImages = ResourceExportType.ExportEmbedded,
        FontFaceTypes = FontFaceType.Ttf
    };

    // Αποθηκεύστε το έγγραφο σε ροή μνήμης
    var memoryStream = new MemoryStream();
    document.Save(memoryStream, options);
}
```

Αυτό το βήμα δείχνει πώς μπορείτε να αποθηκεύσετε ένα έγγραφο OneNote σε μορφή HTML με ενσωματωμένους πόρους (CSS, γραμματοσειρές και εικόνες) σε μια ροή μνήμης.

## Βήμα 4: Αποθήκευση ως HTML σε Αρχείο με πόρους σε ξεχωριστά αρχεία

```csharp
public static void SaveAsHTMLToFileWithResourcesInSeparateFiles()
{
    // Φορτώστε το έγγραφο του OneNote
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Καθορίστε επιλογές αποθήκευσης HTML
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportAsStream,
        ExportFonts = ResourceExportType.ExportAsStream,
        ExportImages = ResourceExportType.ExportAsStream,
        FontFaceTypes = FontFaceType.Ttf
    };

    // Αποθηκεύστε το έγγραφο σε αρχείο HTML με πόρους αποθηκευμένους σε ξεχωριστά αρχεία
    document.Save(Path.Combine(dataDir, "document_out.html"), options);
}
```

Σε αυτό το βήμα, αποθηκεύουμε ένα έγγραφο OneNote σε μορφή HTML με όλους τους πόρους (CSS, γραμματοσειρές και εικόνες) αποθηκευμένους σε ξεχωριστά αρχεία.

## Βήμα 5: Αποθήκευση ως HTML στη ροή μνήμης με επανακλήσεις για εξοικονόμηση πόρων

```csharp
public static void SaveAsHTMLToMemoryStreamWithCallBacksToSaveResources()
{
    // Καθορίστε τη διαμόρφωση αποθήκευσης επανάκλησης
    var savingCallbacks = new UserSavingCallbacks()
    {
        RootFolder = "documentFolder",
        CssFolder = "css",
        KeepCssStreamOpened = true,
        ImagesFolder = "images",
        FontsFolder = "fonts"
    };

    // Καθορίστε επιλογές αποθήκευσης HTML
    var options = new HtmlSaveOptions
    {
        FontFaceTypes = FontFaceType.Ttf,
        CssSavingCallback = savingCallbacks,
        FontSavingCallback = savingCallbacks,
        ImageSavingCallback = savingCallbacks
    };

    // Φορτώστε το έγγραφο του OneNote
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Αποθηκεύστε το έγγραφο σε μορφή HTML με πόρους που διαχειρίζονται από επανακλήσεις που ορίζονται από το χρήστη
    using (var stream = File.Create(Path.Combine(savingCallbacks.RootFolder, "document.html")))
    {
        document.Save(stream, options);
    }

    // Μη αυτόματη προσθήκη δεδομένων στη ροή CSS
    using (var writer = new StreamWriter(savingCallbacks.CssStream))
    {
        writer.WriteLine();
        writer.WriteLine("/* This line is appended to stream manually by user */");
    }
}
```

Εδώ, δείχνουμε πώς μπορείτε να αποθηκεύσετε ένα έγγραφο OneNote σε μορφή HTML με πόρους που διαχειρίζονται από επανακλήσεις που καθορίζονται από το χρήστη.

## συμπέρασμα

Σε αυτό το άρθρο, εξερευνήσαμε τον τρόπο εργασίας με έγγραφα του OneNote και την αποθήκευση τους σε μορφή HTML χρησιμοποιώντας το Aspose.Note για .NET. Ακολουθώντας τον οδηγό βήμα προς βήμα, μπορείτε εύκολα

 ενσωματώστε αυτή τη λειτουργία στις εφαρμογές σας .NET, επιτρέποντάς σας να χειρίζεστε αποτελεσματικά τα αρχεία του OneNote.

## Συχνές ερωτήσεις

### Ε1: Μπορώ να προσαρμόσω την εμφάνιση του αποθηκευμένου αρχείου HTML;

A1: Ναι, μπορείτε να προσαρμόσετε την εμφάνιση τροποποιώντας τα φύλλα στυλ CSS που δημιουργούνται κατά τη διαδικασία μετατροπής.

### Ε2: Το Aspose.Note υποστηρίζει τη μετατροπή σε άλλες μορφές εκτός από HTML;

A2: Ναι, το Aspose.Note υποστηρίζει τη μετατροπή σε διάφορες μορφές, όπως PDF, εικόνες και έγγραφα του Microsoft Word.

### Ε3: Είναι το Aspose.Note συμβατό με εφαρμογές .NET Core;

A3: Ναι, το Aspose.Note είναι συμβατό με εφαρμογές .NET Framework και .NET Core.

### Ε4: Μπορώ να εξαγάγω κείμενο και εικόνες από έγγραφα του OneNote χρησιμοποιώντας το Aspose.Note;

A4: Ναι, μπορείτε να εξαγάγετε κείμενο και εικόνες, καθώς και να εκτελέσετε διάφορους άλλους χειρισμούς χρησιμοποιώντας το Aspose.Note API.

### Ε5: Υπάρχει διαθέσιμη δοκιμαστική έκδοση για δοκιμή των χαρακτηριστικών Aspose.Note;

 A5: Ναι, μπορείτε να κάνετε λήψη μιας δωρεάν δοκιμαστικής έκδοσης από[εδώ](https://releases.aspose.com/).