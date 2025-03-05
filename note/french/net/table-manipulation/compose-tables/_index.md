---
title: Composer des tableaux avec Aspose.Note
linktitle: Composer des tableaux avec Aspose.Note
second_title: API Aspose.Note .NET
description: Apprenez à composer des tableaux structurés avec du contenu en texte enrichi à l'aide d'Aspose.Note pour .NET. Améliorez l’organisation et la lisibilité des documents sans effort.
type: docs
weight: 11
url: /fr/net/table-manipulation/compose-tables/
---
## Introduction

Les tableaux sont des éléments fondamentaux des documents, permettant une présentation structurée des informations. Aspose.Note pour .NET fournit des outils robustes pour composer des tableaux sans effort. Dans ce didacticiel, nous vous guiderons tout au long du processus de création de tableaux avec du contenu en texte enrichi à l'aide d'Aspose.Note.

## Conditions préalables

Avant de vous lancer dans la composition de tableaux avec Aspose.Note pour .NET, assurez-vous d'avoir les prérequis suivants :

1. Configuration de l'environnement : assurez-vous de disposer d'un environnement de développement approprié configuré avec .NET Framework ou .NET Core.
2.  Installation : Téléchargez et installez Aspose.Note pour .NET à partir du[site web](https://releases.aspose.com/note/net/).
3. Connaissances de base : Familiarisez-vous avec les concepts de base de la programmation C# et de la manipulation de documents.

## Importer des espaces de noms

Avant de commencer à composer des tables, assurez-vous d'importer les espaces de noms nécessaires :

```csharp
using System;
using System.Drawing;
using System.IO;
using System.Linq;
```

Décomposons l'exemple fourni en étapes gérables :

## Étape 1 : configurer le répertoire de documents

Avant de composer le tableau, définissez le répertoire dans lequel le document sera enregistré.

```csharp
string dataDir = "Your Document Directory";
```

## Étape 2 : Créer un texte d'en-tête

Définissez le texte d'en-tête avec des styles spécifiques tels que la taille de la police et le gras.

```csharp
var headerText = new RichText() { ParagraphStyle = new ParagraphStyle() { FontSize = 18, IsBold = true }, Alignment = HorizontalAlignment.Center }
					.Append("Super contest for suppliers.");
```

## Étape 3 : Créer une page et un plan

Initialisez une page et un plan pour structurer le contenu.

```csharp
var page = new Page();
var outline = page.AppendChildLast(new Outline() { HorizontalOffset = 50 });
outline.AppendChildLast(new OutlineElement()).AppendChildLast(headerText);
```

## Étape 4 : Ajouter un texte récapitulatif

Incluez un texte récapitulatif avant le tableau.

```csharp
var bodyTextHeader = outline.AppendChildLast(new OutlineElement()).AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default });
bodyTextHeader.Append("This is the final ranking of proposals got from our suppliers.");
```

## Étape 5 : Créer un tableau

Initialisez un tableau pour organiser les données en lignes et en colonnes.

```csharp
var ranking = outline.AppendChildLast(new OutlineElement()).AppendChildLast(new Table());
```

## Étape 6 : Ajouter une ligne d'en-tête

Remplissez le tableau avec une ligne d'en-tête contenant les titres des colonnes.

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

## Étape 7 : ajouter des lignes vides

Insérez des lignes vides pour préparer l'insertion des données.

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

## Étape 8 : ajouter des informations de contact

Remplissez la colonne « Contacts » avec le contenu du modèle.

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

## Étape 9 : Enregistrez le document

Enregistrez le document de table composé.

```csharp
var d = new Document();
d.AppendChildLast(page);
d.Save(Path.Combine(dataDir, "ComposeTable_out.one"));
```

## Étape 10 : Confirmation

Confirmez la composition réussie du document.

```csharp
Console.WriteLine("\nThe document is composed successfully.");
```

## Conclusion

Dans ce didacticiel, nous avons exploré comment composer des tableaux avec du contenu en texte enrichi à l'aide d'Aspose.Note pour .NET. En suivant ces instructions étape par étape, vous pouvez créer efficacement des tableaux structurés dans vos documents, améliorant ainsi la lisibilité et l'organisation.

## FAQ

### Q1 : Puis-je personnaliser le style des éléments du tableau ?
   
A1 : Oui, vous pouvez personnaliser divers aspects tels que la taille de la police, la couleur et l'alignement en fonction de vos besoins.

### Q2 : Aspose.Note est-il compatible avec d’autres bibliothèques .NET ?
   
A2 : Aspose.Note s'intègre de manière transparente à d'autres bibliothèques .NET, offrant une grande flexibilité dans la manipulation de documents.

### Q3 : Aspose.Note prend-il en charge l’exportation de tableaux vers différents formats ?
   
A3 : Absolument, Aspose.Note vous permet d'exporter des tableaux vers différents formats, notamment PDF, DOCX et HTML.

### Q4 : Puis-je remplir dynamiquement des tableaux avec des données provenant de sources externes ?
   
A4 : Oui, vous pouvez remplir dynamiquement des tables en récupérant des données à partir de bases de données, d'API ou d'entrées utilisateur.

### Q5 : Le support technique est-il disponible pour les utilisateurs d'Aspose.Note ?
   
A5 : Oui, Aspose fournit une assistance technique complète via ses forums et ses canaux d'assistance dédiés.