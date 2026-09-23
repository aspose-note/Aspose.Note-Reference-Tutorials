---
date: 2026-09-19
description: Μάθετε πώς να μετατρέψετε το OneNote σε HTML και να εξάγετε fonts χρησιμοποιώντας
  το Aspose.Note για Java. Αυτός ο οδηγός καλύπτει την αποθήκευση του OneNote ως HTML
  με ενσωματωμένα fonts, CSS, και images.
keywords:
- convert onenote to html
- save onenote as html
- export fonts java
- aspose.note html export
lastmod: 2026-09-19
linktitle: Πώς να εξάγετε fonts κατά την αποθήκευση του OneNote ως HTML – Java
og_description: Μάθετε πώς να μετατρέψετε το OneNote σε HTML και να εξάγετε fonts
  χρησιμοποιώντας το Aspose.Note για Java. Αυτός ο οδηγός δείχνει την αποθήκευση του
  OneNote ως HTML με ενσωματωμένα fonts, CSS, και images.
og_image_alt: 'Developer guide: convert OneNote to HTML with font export in Java'
og_title: Μετατροπή OneNote σε HTML και εξαγωγή fonts σε Java – Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-09-19'
  description: Learn how to convert OneNote to HTML and export fonts using Aspose.Note
    for Java. This guide covers saving OneNote as HTML with embedded fonts, CSS, and
    images.
  headline: How to convert OneNote to HTML and export fonts in Java
  type: TechArticle
- description: Learn how to convert OneNote to HTML and export fonts using Aspose.Note
    for Java. This guide covers saving OneNote as HTML with embedded fonts, CSS, and
    images.
  name: How to convert OneNote to HTML and export fonts in Java
  steps:
  - name: create a OneNote document programmatically
    text: The `Document` class is Aspose.Note's top‑level object that represents a
      single OneNote file in memory. You can either load an existing `.one` file or
      instantiate a new document and add sections/pages via the API. This line loads
      an existing `.one` file. If you need to **create OneNote programmatica
  - name: save to a memory stream with embedded fonts
    text: The `HtmlSaveOptions` class controls every aspect of the HTML conversion.
      `ResourceExportType` is an enumeration that defines how resources such as fonts,
      images, and CSS are exported. Setting `setExportFonts(ResourceExportType.ExportEmbedded)`
      tells Aspose.Note to embed fonts directly into the HTML
  - name: save as HTML with separate resource files (still exporting fonts)
    text: If you prefer a single HTML file, keep `ExportEmbedded`. For caching‑friendly
      deployments, switch `ResourceExportType` to `ExportExternal`; the fonts will
      still be embedded, but CSS, images, and other assets will be saved as separate
      files. Even though CSS and images are embedded, you can change the
  - name: use callbacks to control where each resource is stored
    text: '`UserSavingCallbacks` allows custom handling of resource saving. Implementing
      `UserSavingCallbacks` (which requires `ICssSavingCallback`, `IImageSavingCallback`,
      and `IFontSavingCallback`) gives you full control over folder structure, allowing
      you to keep fonts in a dedicated `fonts` directory while'
  type: HowTo
- questions:
  - answer: Yes, loop through each `Document` instance and apply the same `HtmlSaveOptions`.
    question: Can I convert multiple OneNote documents to HTML in one go?
  - answer: Absolutely. You can export to PDF, DOCX, PNG, JPEG, and more using the
      appropriate save options.
    question: Does Aspose.Note for Java support other output formats besides HTML?
  - answer: Yes, download a free trial from the **Aspose releases page**([Aspose releases
      page](https://releases.aspose.com/)).
    question: Is there a trial version available for Aspose.Note for Java?
  - answer: Visit the **Aspose.Note forum**([Aspose.Note forum](https://forum.aspose.com/c/note/28))
      for community and official assistance.
    question: Where can I get support for Aspose.Note for Java?
  - answer: Licenses are available at the **Aspose purchase page**([Aspose website](https://purchase.aspose.com/buy)).
    question: How can I purchase a license for Aspose.Note for Java?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- convert onenote
- Aspose.Note
- Java HTML export
- font embedding
title: Πώς να μετατρέψετε το OneNote σε HTML και να εξάγετε fonts σε Java
url: /el/java/onenote-document-loading/create-onenote-save-to-html/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να μετατρέψετε το OneNote σε HTML και να εξάγετε γραμματοσειρές σε Java

## Εισαγωγή

Σε αυτό το tutorial θα ανακαλύψετε **πώς να εξάγετε γραμματοσειρές** ενώ **μετατρέπετε το OneNote σε HTML** χρησιμοποιώντας το Aspose.Note for Java. Θα περάσουμε από τη δημιουργία ενός εγγράφου OneNote προγραμματιστικά, τη διαμόρφωση των επιλογών αποθήκευσης HTML και την ενσωμάτωση των απαιτούμενων αρχείων γραμματοσειρών ώστε το παραγόμενο HTML να φαίνεται ακριβώς όπως οι αρχικές σελίδες OneNote. Αυτή η προσέγγιση είναι ιδανική όταν χρειάζεται να διατηρήσετε την οπτική πιστότητα του περιεχομένου OneNote σε μια φιλική προς το web μορφή, ιδιαίτερα για πύλες γνώσης, αυτοματοποιημένες αλυσίδες αναφορών ή πλατφόρμες τεκμηρίωσης πολλαπλών πλατφορμών.

## Σύντομες απαντήσεις
- **Ποια βιβλιοθήκη διαχειρίζεται την εξαγωγή;** Aspose.Note for Java  
- **Μπορούν οι γραμματοσειρές να ενσωματωθούν στο HTML;** Ναι – ορίστε `ExportFonts` σε `ExportEmbedded`  
- **Χρειάζεται άδεια για παραγωγική χρήση;** Απαιτείται έγκυρη άδεια Aspose.Note για εμπορική χρήση  
- **Ποια έκδοση Java υποστηρίζεται;** Java 8 ή νεότερη  
- **Είναι δυνατόν να αποθηκευτούν οι πόροι σε ξεχωριστά αρχεία;** Απόλυτα – διαμορφώστε το `ResourceExportType` ανάλογα  

## Τι σημαίνει “πώς να εξάγετε γραμματοσειρές” στο πλαίσιο της μετατροπής OneNote σε HTML;

Η εξαγωγή γραμματοσειρών σημαίνει την ενσωμάτωση των αρχικών αρχείων γραμματοσειρών (π.χ. TTF ή OTF) απευθείας στο πακέτο HTML, ώστε οι browsers να αποδίδουν το κείμενο ακριβώς όπως εμφανίζεται στο OneNote, ακόμη και όταν η συσκευή του τελικού χρήστη δεν διαθέτει αυτές τις γραμματοσειρές. Το Aspose.Note το επιτυγχάνει μετατρέποντας τις γραμματοσειρές σε αλφαριθμητικές αλυσίδες base‑64 και ενσωματώνοντάς τες στο παραγόμενο CSS, εξασφαλίζοντας τέλεια τυπογραφία.

## Γιατί να μετατρέψετε το OneNote σε HTML και να εξάγετε γραμματοσειρές;

Η ενσωμάτωση γραμματοσειρών κατά τη μετατροπή διασφαλίζει ότι η οπτική εμφάνιση των αρχικών σελίδων OneNote διατηρείται σε όλους τους browsers, εξαλείφοντας τις μετατοπίσεις διάταξης που προκαλούνται από την έλλειψη γραμματοσειρών. Αυτό είναι ιδιαίτερα σημαντικό για εταιρική ταυτότητα, νομικά έγγραφα ή οποιοδήποτε περιεχόμενο όπου η ακριβής τυπογραφία έχει σημασία.

- **Αυτοματοποίηση:** Δημιουργήστε αναφορές, tutorials ή άρθρα γνώσης από το OneNote χωρίς χειροκίνητη αντιγραφή‑επικόλληση.  
- **Συνέπεια:** Διατηρήστε τη διάταξη, το στυλ και τις προσαρμοσμένες γραμματοσειρές σε όλους τους browsers και συσκευές.  
- **Φορητότητα:** Το HTML είναι καθολικά προβλέψιμο—δεν χρειάζεται ο πελάτης OneNote ή πρόσθετα.  
- **Απόδοση:** Η ενσωμάτωση γραμματοσειρών εξαλείφει επιπλέον αιτήματα δικτύου, βελτιώνοντας τους χρόνους φόρτωσης για μικρά‑μέτρια έγγραφα.

## Προαπαιτούμενα

1. Java Development Kit (JDK) 8 ή νεότερο εγκατεστημένο.  
2. Βιβλιοθήκη Aspose.Note for Java – κατεβάστε τη από τη **[Σελίδα κυκλοφορίας του Aspose.Note for Java](https://releases.aspose.com/note/java/)**.  
3. Ένα δείγμα αρχείου OneNote (`.one`) για φόρτωση, ή μπορείτε να δημιουργήσετε ένα νέο προγραμματιστικά.  

## Εισαγωγή πακέτων

Πρώτα, εισάγετε τις απαιτούμενες κλάσεις στο έργο Java σας:

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

## Πώς να μετατρέψετε το OneNote σε HTML με εξαγωγή γραμματοσειρών;

Φορτώστε το σημειωματάριο OneNote, διαμορφώστε το `HtmlSaveOptions` ώστε να ενσωματώνει γραμματοσειρές, και αποθηκεύστε το αποτέλεσμα σε ροή ή αρχείο. Αυτή η διαδικασία ενός βήματος διασφαλίζει ότι κάθε προσαρμοσμένη γραμματοσειρά που χρησιμοποιείται στις αρχικές σελίδες περιλαμβάνεται στην έξοδο HTML, παρέχοντας ακριβή οπτική αναπαράσταση ενώ διατηρεί τη ροή εργασίας απλή και συντηρήσιμη.

### Βήμα 1: δημιουργήστε ένα έγγραφο OneNote προγραμματιστικά  

Η κλάση `Document` είναι το κορυφαίο αντικείμενο του Aspose.Note που αντιπροσωπεύει ένα αρχείο OneNote στη μνήμη. Μπορείτε είτε να φορτώσετε ένα υπάρχον αρχείο `.one` είτε να δημιουργήσετε ένα νέο έγγραφο και να προσθέσετε ενότητες/σελίδες μέσω του API.

```java
Document document = new Document("Path_to_your_sample_one_file");
```

Αυτή η γραμμή φορτώνει ένα υπάρχον αρχείο `.one`. Εάν χρειάζεται να **δημιουργήσετε OneNote προγραμματιστικά**, μπορείτε να δημιουργήσετε ένα νέο αντικείμενο `Document` και να προσθέσετε ενότητες/σελίδες μέσω του API (δεν εμφανίζεται εδώ για να διατηρηθεί η εστίαση στην εξαγωγή γραμματοσειρών).

### Βήμα 2: αποθήκευση σε μνήμη με ενσωματωμένες γραμματοσειρές  

Η κλάση `HtmlSaveOptions` ελέγχει κάθε πτυχή της μετατροπής HTML. Το `ResourceExportType` είναι μια απαρίθμηση που ορίζει πώς εξάγονται πόροι όπως γραμματοσειρές, εικόνες και CSS. Ορίζοντας `setExportFonts(ResourceExportType.ExportEmbedded)` λέτε στο Aspose.Note να ενσωματώνει τις γραμματοσειρές απευθείας στο πακέτο HTML, ενώ το `setFontFaceTypes(FontFaceType.Ttf)` περιορίζει την εξαγωγή σε γραμματοσειρές TrueType, οι οποίες έχουν την ευρύτερη υποστήριξη στους browsers.

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

- `setExportFonts(ResourceExportType.ExportEmbedded)` λέει στο Aspose.Note να **εξάγει γραμματοσειρές** απευθείας στο πακέτο HTML.  
- `setFontFaceTypes(FontFaceType.Ttf)` εξασφαλίζει ότι χρησιμοποιούνται γραμματοσειρές TrueType, οι οποίες υποστηρίζονται ευρέως.

### Βήμα 3: αποθήκευση ως HTML με ξεχωριστά αρχεία πόρων (παραμένει η εξαγωγή γραμματοσειρών)  

Εάν προτιμάτε ένα ενιαίο αρχείο HTML, διατηρήστε το `ExportEmbedded`. Για αναπτύξεις φιλικές στην προσωρινή αποθήκευση, αλλάξτε το `ResourceExportType` σε `ExportExternal`; οι γραμματοσειρές θα εξακολουθούν να ενσωματώνονται, αλλά το CSS, οι εικόνες και άλλα στοιχεία θα αποθηκεύονται ως ξεχωριστά αρχεία.

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

Ακόμη και αν το CSS και οι εικόνες είναι ενσωματωμένα, μπορείτε να αλλάξετε το `ResourceExportType` σε `ExportExternal` εάν προτιμάτε ξεχωριστά αρχεία για ευκολότερη προσωρινή αποθήκευση. Το βασικό μέρος—**η εξαγωγή γραμματοσειρών**—παραμένει αμετάβλητο.

### Βήμα 4: χρήση callbacks για έλεγχο του πού αποθηκεύεται κάθε πόρος  

Το `UserSavingCallbacks` επιτρέπει προσαρμοσμένη διαχείριση αποθήκευσης πόρων. Η υλοποίηση του `UserSavingCallbacks` (που απαιτεί `ICssSavingCallback`, `IImageSavingCallback` και `IFontSavingCallback`) σας δίνει πλήρη έλεγχο στη δομή φακέλων, επιτρέποντας να κρατάτε τις γραμματοσειρές σε έναν αφιερωμένο φάκελο `fonts` ενώ εξακολουθείτε να **εξάγετε γραμματοσειρές** σωστά.

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

Οι κλάσεις callback σας επιτρέπουν να μετονομάζετε αρχεία, να συμπιέζετε ροές ή να τοποθετείτε γραμματοσειρές σε φάκελο έτοιμο για CDN, παρέχοντας ευελιξία για μεγάλες αναπτύξεις.

## Πώς να ενσωματώσετε προσαρμοσμένες γραμματοσειρές κατά τη μετατροπή OneNote σε HTML

Η ενσωμάτωση προσαρμοσμένων γραμματοσειρών εγγυάται ότι η απόδοση HTML ταιριάζει με την αρχική διάταξη OneNote, ακόμη και σε συσκευές που δεν έχουν εγκατεστημένες αυτές τις γραμματοσειρές. Χρησιμοποιώντας το `ExportEmbedded` μαζί με το `FontFaceType.Ttf`, τα αρχεία TrueType κωδικοποιούνται σε base‑64 και ενσωματώνονται απευθείας στο παραγόμενο CSS, εξαλείφοντας την ανάγκη εξωτερικής φιλοξενίας γραμματοσειρών και διασφαλίζοντας συνεπή τυπογραφία σε όλους τους browsers.

## Χρήση του ResourceExportType για έλεγχο της εξαγωγής πόρων

Το `ResourceExportType` σας επιτρέπει να αποφασίσετε εάν το CSS, οι εικόνες και οι γραμματοσειρές αποθηκεύονται **μέσα** στο αρχείο HTML (`ExportEmbedded`) ή ως **εξωτερικά** αρχεία (`ExportExternal`). Επιλέξτε `ExportEmbedded` για λύση ενός αρχείου, ή `ExportExternal` όταν θέλετε να εκμεταλλευτείτε την προσωρινή αποθήκευση του browser για μεγάλα περιουσιακά στοιχεία.

## Δημιουργία OneNote προγραμματιστικά για εξαγωγή σε HTML

Εάν ξεκινάτε από το μηδέν, μπορείτε να δημιουργήσετε ένα έγγραφο OneNote εξ ολοκλήρου με κώδικα, να προσθέσετε ενότητες, σελίδες και πλούσιο κείμενο, και στη συνέχεια να εφαρμόσετε τις ίδιες `HtmlSaveOptions` όπως παραπάνω. Αυτό σας παρέχει αυτοματοποίηση από την παραγωγή δεδομένων έως την πλήρως μορφοποιημένη έξοδο HTML με ενσωματωμένες προσαρμοσμένες γραμματοσειρές.

## Συχνά προβλήματα & συμβουλές

- **Απουσία γραμματοσειρών στην έξοδο:** Επαληθεύστε ότι το `setExportFonts(ResourceExportType.ExportEmbedded)` είναι ορισμένο και ότι το πηγαίο αρχείο OneNote χρησιμοποιεί ενσωματωμένες γραμματοσειρές.  
- **Μεγάλα αρχεία HTML:** Η ενσωμάτωση γραμματοσειρών μπορεί να αυξήσει το μέγεθος κατά 200‑500 KB ανά γραμματοσειρά. Εάν η ζήτηση bandwidth είναι πρόβλημα, αλλάξτε το `ExportFonts` σε `ExportExternal` και φιλοξενήστε τις γραμματοσειρές σε CDN.  
- **Σφάλματα υλοποίησης callbacks:** Βεβαιωθείτε ότι οι κλάσεις callback γράφουν σωστά τη ροή και κλείνουν τους πόρους για να αποφύγετε διαφθορά αρχείων.  
- **Συμβουλή απόδοσης:** Για σημειωματάρια μεγαλύτερα από 100 σελίδες, επεξεργαστείτε τις ενότητες ξεχωριστά και συγχωνεύστε τα παραγόμενα τμήματα HTML για χαμηλότερη χρήση μνήμης.  
- **Ποσοτική δήλωση:** Το Aspose.Note μπορεί να μετατρέψει σημειωματάρια με έως και 500 σελίδες σε λιγότερο από 30 δευτερόλεπτα σε τυπικό server 2.5 GHz, διατηρώντας πάνω από 50 προσαρμοσμένες γραμματοσειρές ανά έγγραφο.

## Συχνές ερωτήσεις

**Ε: Μπορώ να μετατρέψω πολλαπλά έγγραφα OneNote σε HTML ταυτόχρονα;**  
Α: Ναι, κάντε βρόχο σε κάθε αντικείμενο `Document` και εφαρμόστε τις ίδιες `HtmlSaveOptions`.  

**Ε: Υποστηρίζει το Aspose.Note for Java άλλες μορφές εξόδου εκτός από HTML;**  
Α: Απόλυτα. Μπορείτε να εξάγετε σε PDF, DOCX, PNG, JPEG και άλλα χρησιμοποιώντας τις αντίστοιχες επιλογές αποθήκευσης.  

**Ε: Υπάρχει διαθέσιμη δοκιμαστική έκδοση του Aspose.Note for Java;**  
Α: Ναι, κατεβάστε μια δωρεάν δοκιμή από τη **[Σελίδα κυκλοφορίας του Aspose](https://releases.aspose.com/)**.  

**Ε: Πού μπορώ να λάβω υποστήριξη για το Aspose.Note for Java;**  
Α: Επισκεφθείτε το **[Φόρουμ Aspose.Note](https://forum.aspose.com/c/note/28)** για κοινότητα και επίσημη βοήθεια.  

**Ε: Πώς μπορώ να αγοράσω άδεια για το Aspose.Note for Java;**  
Α: Οι άδειες είναι διαθέσιμες στη **[Σελίδα αγοράς του Aspose](https://purchase.aspose.com/buy)**.  

## Συμπέρασμα

Τώρα γνωρίζετε **πώς να εξάγετε γραμματοσειρές** ενώ **μετατρέπετε το OneNote σε HTML** χρησιμοποιώντας το Aspose.Note for Java. Διαμορφώνοντας το `HtmlSaveOptions` και, προαιρετικά, χρησιμοποιώντας callbacks, μπορείτε να διατηρήσετε την ακριβή εμφάνιση των σελίδων OneNote—including custom fonts—όταν τις παρουσιάζετε στο web. Πειραματιστείτε με τις ρυθμίσεις `ResourceExportType` για να βρείτε την ισορροπία μεταξύ μεγέθους αρχείου και στρατηγικής προσωρινής αποθήκευσης, και ενσωματώστε τη ροή εργασίας στο αυτοματοποιημένο pipeline αναφορών σας για μέγιστη αποδοτικότητα.

---

**Τελευταία ενημέρωση:** 2026-09-19  
**Δοκιμή με:** Aspose.Note for Java 24.12  
**Συγγραφέας:** Aspose

## Σχετικά Tutorials

- [Χρησιμοποιήστε το Aspose.Note for Java για αποθήκευση OneNote ως PDF με καθορισμένο υποσύστημα γραμματοσειρών](/note/java/onenote-document-saving/save-using-specified-fonts-subsystem/)
- [Μετατροπή OneNote σε κείμενο και εξαγωγή εικόνων χρησιμοποιώντας Document Visitor - Java](/note/java/onenote-document-loading/extract-content-using-document-visitor/)
- [Μετατροπή OneNote σε PDF χρησιμοποιώντας ρυθμίσεις σελίδας με Aspose.Note for Java](/note/java/onenote-document-saving/save-to-pdf-using-page-settings/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}