---
title: Σύνθεση πινάκων με Aspose.Σημείωση
linktitle: Σύνθεση πινάκων με Aspose.Σημείωση
second_title: Aspose.Note .NET API
description: Μάθετε πώς να συνθέτετε δομημένους πίνακες με περιεχόμενο πλούσιου κειμένου χρησιμοποιώντας το Aspose.Note για .NET. Βελτιώστε την οργάνωση και την αναγνωσιμότητα των εγγράφων χωρίς κόπο.
type: docs
weight: 11
url: /el/net/table-manipulation/compose-tables/
---
## Εισαγωγή

Οι πίνακες είναι θεμελιώδη στοιχεία των εγγράφων, που επιτρέπουν τη δομημένη παρουσίαση των πληροφοριών. Το Aspose.Note για .NET παρέχει ισχυρά εργαλεία για τη σύνταξη πινάκων χωρίς κόπο. Σε αυτό το σεμινάριο, θα σας καθοδηγήσουμε στη διαδικασία δημιουργίας πινάκων με περιεχόμενο εμπλουτισμένου κειμένου χρησιμοποιώντας το Aspose.Note.

## Προαπαιτούμενα

Πριν ξεκινήσετε τη σύνθεση του τραπεζιού με το Aspose.Note για .NET, βεβαιωθείτε ότι έχετε τις ακόλουθες προϋποθέσεις:

1. Ρύθμιση περιβάλλοντος: Βεβαιωθείτε ότι έχετε ρυθμίσει ένα κατάλληλο περιβάλλον ανάπτυξης με .NET Framework ή .NET Core.
2.  Εγκατάσταση: Κατεβάστε και εγκαταστήστε το Aspose.Note για .NET από το[δικτυακός τόπος](https://releases.aspose.com/note/net/).
3. Βασικές γνώσεις: Εξοικειωθείτε με τις βασικές έννοιες του προγραμματισμού C# και του χειρισμού εγγράφων.

## Εισαγωγή χώρων ονομάτων

Πριν ξεκινήσετε τη σύνθεση πινάκων, βεβαιωθείτε ότι έχετε εισαγάγει τους απαραίτητους χώρους ονομάτων:

```csharp
using System;
using System.Drawing;
using System.IO;
using System.Linq;
```

Ας αναλύσουμε το παράδειγμα που παρέχεται σε διαχειρίσιμα βήματα:

## Βήμα 1: Ρυθμίστε τον Κατάλογο Εγγράφων

Πριν συνθέσετε τον πίνακα, ορίστε τον κατάλογο όπου θα αποθηκευτεί το έγγραφο.

```csharp
string dataDir = "Your Document Directory";
```

## Βήμα 2: Δημιουργία κειμένου κεφαλίδας

Καθορίστε το κείμενο της κεφαλίδας με συγκεκριμένα στυλ, όπως μέγεθος γραμματοσειράς και έντονη γραφή.

```csharp
var headerText = new RichText() { ParagraphStyle = new ParagraphStyle() { FontSize = 18, IsBold = true }, Alignment = HorizontalAlignment.Center }
					.Append("Super contest for suppliers.");
```

## Βήμα 3: Δημιουργία σελίδας και περίγραμμα

Αρχικοποιήστε μια σελίδα και ένα περίγραμμα για τη δομή του περιεχομένου.

```csharp
var page = new Page();
var outline = page.AppendChildLast(new Outline() { HorizontalOffset = 50 });
outline.AppendChildLast(new OutlineElement()).AppendChildLast(headerText);
```

## Βήμα 4: Προσθήκη συνοπτικού κειμένου

Συμπεριλάβετε ένα συνοπτικό κείμενο πριν από τον πίνακα.

```csharp
var bodyTextHeader = outline.AppendChildLast(new OutlineElement()).AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default });
bodyTextHeader.Append("This is the final ranking of proposals got from our suppliers.");
```

## Βήμα 5: Δημιουργία πίνακα

Εκκινήστε έναν πίνακα για να οργανώσετε δεδομένα σε σειρές και στήλες.

```csharp
var ranking = outline.AppendChildLast(new OutlineElement()).AppendChildLast(new Table());
```

## Βήμα 6: Προσθήκη γραμμής κεφαλίδας

Συμπληρώστε τον πίνακα με μια σειρά κεφαλίδας που περιέχει τίτλους στηλών.

```csharp
var headerRow = ranking.AppendChildFirst(new TableRow());
foreach (var header in new[] { "Supplier", "Contacts", "Score A", "Score B", "Score C", "Final score", "Attached materials", "Comments" })
{
   ranking.Columns.Add(new TableColumn());
   headerRow.AppendChildLast(new TableCell() { BackgroundColor = backGroundColor })
			 .AppendChildLast(new OutlineElement())
			 .AppendChildLast(new RichText() { ParagraphStyle = headerStyle })
			 .Append(header);
}
```

## Βήμα 7: Προσθέστε κενές σειρές

Εισαγάγετε κενές σειρές για προετοιμασία για εισαγωγή δεδομένων.

```csharp
for (int i = 0; i < 5; i++)
{
   backGroundColor = backGroundColor.IsEmpty ? Color.LightGray : Color.Empty;
   var row = ranking.AppendChildLast(new TableRow());
   for (int j = 0; j < ranking.Columns.Count(); j++)
   {
	   row.AppendChildLast(new TableCell() { BackgroundColor = backGroundColor })
		  .AppendChildLast(new OutlineElement())
		  .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default });
   }
}
```

## Βήμα 8: Προσθήκη στοιχείων επικοινωνίας

Συμπληρώστε τη στήλη "Επαφές" με περιεχόμενο προτύπου.

```csharp
foreach (var row in ranking.Skip(1))
{
   var contactsCell = row.ElementAt(1);
   contactsCell.AppendChildLast(new OutlineElement())
			   .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default })
			   .Append("Web: ").Append("link", new TextStyle() { HyperlinkAddress = "www.link.com", IsHyperlink = true });
   contactsCell.AppendChildLast(new OutlineElement())
			   .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default })
			   .Append("E-mail: ").Append("mail", new TextStyle() { HyperlinkAddress = "mailto:hi@link.com", IsHyperlink = true });
}
```

## Βήμα 9: Αποθηκεύστε το έγγραφο

Αποθηκεύστε το έγγραφο του σύνθετου πίνακα.

```csharp
var d = new Document();
d.AppendChildLast(page);
d.Save(Path.Combine(dataDir, "ComposeTable_out.one"));
```

## Βήμα 10: Επιβεβαίωση

Επιβεβαιώστε την επιτυχημένη σύνθεση εγγράφου.

```csharp
Console.WriteLine("\nThe document is composed successfully.");
```

## συμπέρασμα

Σε αυτό το σεμινάριο, εξερευνήσαμε πώς να συνθέσουμε πίνακες με περιεχόμενο εμπλουτισμένου κειμένου χρησιμοποιώντας το Aspose.Note για .NET. Ακολουθώντας αυτές τις οδηγίες βήμα προς βήμα, μπορείτε να δημιουργήσετε αποτελεσματικά δομημένους πίνακες στα έγγραφά σας, βελτιώνοντας την αναγνωσιμότητα και την οργάνωση.

## Συχνές ερωτήσεις

### Ε1: Μπορώ να προσαρμόσω το στυλ των στοιχείων του τραπεζιού;
   
A1: Ναι, μπορείτε να προσαρμόσετε διάφορες πτυχές, όπως το μέγεθος γραμματοσειράς, το χρώμα και τη στοίχιση για να ταιριάζουν στις απαιτήσεις σας.

### Ε2: Είναι το Aspose.Note συμβατό με άλλες βιβλιοθήκες .NET;
   
A2: Το Aspose.Note ενσωματώνεται άψογα με άλλες βιβλιοθήκες .NET, προσφέροντας μεγάλη ευελιξία στη διαχείριση εγγράφων.

### Ε3: Υποστηρίζει το Aspose.Note την εξαγωγή πινάκων σε διαφορετικές μορφές;
   
A3: Απολύτως, το Aspose.Note σάς επιτρέπει να εξάγετε πίνακες σε διάφορες μορφές, όπως PDF, DOCX και HTML.

### Ε4: Μπορώ να συμπληρώσω δυναμικά πίνακες με δεδομένα από εξωτερικές πηγές;
   
A4: Ναι, μπορείτε να συμπληρώσετε δυναμικά πίνακες λαμβάνοντας δεδομένα από βάσεις δεδομένων, API ή εισόδους χρηστών.

### Ε5: Είναι διαθέσιμη τεχνική υποστήριξη για τους χρήστες του Aspose.Note;
   
A5: Ναι, η Aspose παρέχει ολοκληρωμένη τεχνική υποστήριξη μέσω των φόρουμ και των αποκλειστικών καναλιών υποστήριξης.