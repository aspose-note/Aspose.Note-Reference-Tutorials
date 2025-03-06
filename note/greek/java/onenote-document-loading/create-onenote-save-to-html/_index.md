---
title: Δημιουργήστε ένα έγγραφο OneNote και αποθηκεύστε το σε HTML - Java
linktitle: Δημιουργήστε ένα έγγραφο OneNote και αποθηκεύστε το σε HTML - Java
second_title: Aspose.Note Java API
description: Μάθετε να δημιουργείτε και να αποθηκεύετε έγγραφα OneNote ως HTML χρησιμοποιώντας το Aspose.Note για Java. Ενσωματωθείτε σε εφαρμογές Java για προγραμματικό χειρισμό αρχείων OneNote.

weight: 18
url: /el/java/onenote-document-loading/create-onenote-save-to-html/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Δημιουργήστε ένα έγγραφο OneNote και αποθηκεύστε το σε HTML - Java

## Εισαγωγή

Το Aspose.Note για Java είναι μια ισχυρή βιβλιοθήκη που επιτρέπει στους προγραμματιστές να εργάζονται με αρχεία Microsoft OneNote μέσω προγραμματισμού. Σε αυτό το σεμινάριο, θα διερευνήσουμε πώς να δημιουργήσετε ένα έγγραφο OneNote και να το αποθηκεύσετε σε μορφή HTML χρησιμοποιώντας το Aspose.Note για Java.

## Προαπαιτούμενα

Πριν ξεκινήσουμε, βεβαιωθείτε ότι έχετε τα εξής:

1. Το Java Development Kit (JDK) είναι εγκατεστημένο στο σύστημά σας.
2.  Aspose.Note για τη βιβλιοθήκη Java. Μπορείτε να το κατεβάσετε από[εδώ](https://releases.aspose.com/note/java/).
3. Βασικές γνώσεις προγραμματισμού Java.

## Εισαγωγή πακέτων

Πρώτα, εισαγάγετε τα απαραίτητα πακέτα στο έργο σας Java:

```java
import java.io.ByteArrayOutputStream;
import java.io.File;
import java.io.FileOutputStream;
import java.io.IOException;
import java.io.OutputStream;
import java.io.OutputStreamWriter;
import java.nio.file.Paths;
import com.aspose.note.CssSavingArgs;
import com.aspose.note.Document;
import com.aspose.note.FontFaceType;
import com.aspose.note.FontSavingArgs;
import com.aspose.note.HtmlSaveOptions;
import com.aspose.note.ICssSavingCallback;
import com.aspose.note.IFontSavingCallback;
import com.aspose.note.IImageSavingCallback;
import com.aspose.note.ImageSavingArgs;
import com.aspose.note.ResourceExportType;
```

## Βήμα 1: Δημιουργήστε ένα αντικείμενο εγγράφου OneNote

```java
Document document = new Document("Path_to_your_sample_one_file");
```

 Αυτός ο κώδικας αρχικοποιεί α`Document` αντικείμενο φορτώνοντας ένα δείγμα αρχείου OneNote.

## Βήμα 2: Αποθήκευση ως HTML στη ροή μνήμης

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

Εδώ, ρυθμίζουμε τις επιλογές αποθήκευσης HTML και αποθηκεύουμε το έγγραφο σε μια ροή μνήμης.

## Βήμα 3: Αποθήκευση ως HTML με πόρους σε ξεχωριστά αρχεία

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

Αυτό το βήμα αποθηκεύει το έγγραφο ως HTML με πόρους όπως CSS, γραμματοσειρές και εικόνες σε ξεχωριστά αρχεία.

## Βήμα 4: Αποθήκευση ως HTML στη ροή μνήμης με επανακλήσεις για εξοικονόμηση πόρων

```java
Document document = new Document("Path_to_your_sample_one_file");

UserSavingCallbacks savingCallbacks = new UserSavingCallbacks();
savingCallbacks.setRootFolder("documentFolder");
savingCallbacks.setCssFolder("css");
savingCallbacks.setKeepCssStreamOpened(true);
savingCallbacks.setImagesFolder("images");
savingCallbacks.setFontsFolder("fonts");

HtmlSaveOptions options = new HtmlSaveOptions();
options.setFontFaceTypes(FontFaceType.Ttf);
options.setCssSavingCallback(savingCallbacks);
options.setImageSavingCallback(savingCallbacks);
options.setFontSavingCallback(savingCallbacks);
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);

File dir = new File(savingCallbacks.getRootFolder());
if (!dir.exists()) {
    dir.mkdir();
}

document.save(Paths.get(savingCallbacks.getRootFolder(), "document.html").toString(), options);
```

Εδώ, αποθηκεύουμε το έγγραφο ως HTML σε μια ροή μνήμης χρησιμοποιώντας επανακλήσεις για να χειριστούμε την εξοικονόμηση πόρων.

## συμπέρασμα

Συγχαρητήρια! Έχετε μάθει πώς να δημιουργείτε ένα έγγραφο OneNote και να το αποθηκεύετε σε μορφή HTML χρησιμοποιώντας το Aspose.Note για Java. Τώρα μπορείτε να ενσωματώσετε αυτήν τη λειτουργία στις εφαρμογές σας Java για να εργαστείτε με αρχεία OneNote μέσω προγραμματισμού.

## Συχνές ερωτήσεις

### Ε1: Μπορώ να μετατρέψω πολλαπλά έγγραφα OneNote σε HTML με μία κίνηση;

A1: Ναι, μπορείτε να κάνετε επαναληπτικό κύκλο σε πολλά έγγραφα και να εφαρμόσετε τη διαδικασία αποθήκευσης επαναληπτικά.

### Ε2: Το Aspose.Note για Java υποστηρίζει άλλες μορφές εξόδου εκτός από το HTML;

A2: Ναι, το Aspose.Note για Java υποστηρίζει διάφορες μορφές εξόδου, συμπεριλαμβανομένων των μορφών PDF, DOCX και εικόνας.

### Ε3: Υπάρχει διαθέσιμη δοκιμαστική έκδοση για το Aspose.Note για Java;

A3: Ναι, μπορείτε να κάνετε λήψη μιας δωρεάν δοκιμαστικής έκδοσης από[εδώ](https://releases.aspose.com/).

### Ε4: Πού μπορώ να λάβω υποστήριξη για το Aspose.Note για Java;

 A4: Μπορείτε να λάβετε υποστήριξη από το[Aspose.Note φόρουμ](https://forum.aspose.com/c/note/28).

### Ε5: Πώς μπορώ να αγοράσω άδεια χρήσης για το Aspose.Note για Java;

 A5: Μπορείτε να αγοράσετε μια άδεια από το[Aspose website](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
