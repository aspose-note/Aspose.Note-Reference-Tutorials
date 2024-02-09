---
title: Ajouter des hyperliens dans les documents Aspose.Note
linktitle: Ajouter des hyperliens dans les documents Aspose.Note
second_title: API Aspose.Note .NET
description: Découvrez comment ajouter des hyperliens vers des documents Aspose.Note à l'aide d'Aspose.Note pour .NET. Améliorez l'interactivité des documents avec ce didacticiel étape par étape.
type: docs
weight: 10
url: /fr/net/hyperlinks/add-hyperlinks/
---
## Introduction

Dans ce didacticiel, vous apprendrez à ajouter des hyperliens au texte dans les documents Aspose.Note à l'aide du framework .NET. Aspose.Note fournit des fonctionnalités puissantes pour manipuler les documents OneNote par programme. L'ajout d'hyperliens peut améliorer l'interactivité et la convivialité de vos documents, les rendant plus attrayants pour les utilisateurs.

## Conditions préalables:

Avant de commencer, assurez-vous de disposer des prérequis suivants :

1. Compréhension de base du langage de programmation C#.
2. Visual Studio installé sur votre système.
3.  Aspose.Note pour la bibliothèque .NET installée. Vous pouvez le télécharger depuis[ici](https://releases.aspose.com/note/net/).
4. Familiarité avec la structure et les composants des documents Aspose.Note.

## Importer des espaces de noms :

Tout d’abord, vous devez importer les espaces de noms nécessaires dans votre projet C#. Ces espaces de noms donnent accès aux classes et méthodes requises pour travailler avec les documents Aspose.Note.

```csharp
using System;
using System.Drawing;
```

## Étape 1 : Créer un nouvel objet de document :

Commencez par créer une nouvelle instance de la classe Document. Cet objet représentera votre document Aspose.Note, auquel vous ajouterez le lien hypertexte.

```csharp
Document doc = new Document();
```

## Étape 2 : Définir les styles de texte :

Définissez les styles de texte pour le texte normal et le texte du lien hypertexte. Vous pouvez personnaliser divers attributs tels que la couleur de la police, le nom de la police et la taille de la police selon vos préférences.

```csharp
TextStyle textStyleRed = new TextStyle
{
    FontColor = Color.Red,
    FontName = "Arial",
    FontSize = 10,
};

TextStyle textStyleHyperlink = new TextStyle
{
    IsHyperlink = true,
    HyperlinkAddress = "www.google.com"
};
```

## Étape 3 : Créer des objets RichText :

Créez des objets RichText pour les segments de texte que vous souhaitez inclure dans votre document. Ajoutez le texte approprié et appliquez les styles de texte souhaités à chaque segment.

```csharp
RichText text = new RichText() { ParagraphStyle = ParagraphStyle.Default }
                    .Append("This is ", textStyleRed)
                    .Append("hyperlink", textStyleHyperlink)
                    .Append(". This text is not a hyperlink.", TextStyle.Default);
```

## Étape 4 : Créer un contour et un élément de contour :

Créez un objet Outline et un objet OutlineElement pour structurer le contenu de votre document. Ajoutez l'objet RichText contenant le lien hypertexte vers OutlineElement.

```csharp
Outline outline = new Outline()
{
    MaxWidth = 200,
    MaxHeight = 200,
    VerticalOffset = 100,
    HorizontalOffset = 100
};

OutlineElement outlineElem = new OutlineElement();
outlineElem.AppendChildLast(text);
```

## Étape 5 : ajouter des éléments à la page :

Créez un objet Titre et un objet Page. Ajoutez l’objet Outline à la page. Enfin, ajoutez la page au document.

```csharp
Title title = new Title() { TitleText = titleText };
Page page = new Note.Page() { Title = title };

page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## Étape 6 : Enregistrez le document :

Spécifiez le chemin du fichier dans lequel vous souhaitez enregistrer le document Aspose.Note et appelez la méthode Save pour l'enregistrer.

```csharp
string dataDir = "Your Document Directory";
string outputFilePath = Path.Combine(dataDir, "AddHyperlink_out.one");
doc.Save(outputFilePath);
```

## Conclusion:

Dans ce didacticiel, vous avez appris à ajouter des hyperliens vers des documents Aspose.Note à l'aide d'Aspose.Note pour .NET. En suivant ces étapes, vous pouvez améliorer l'interactivité de vos documents et offrir aux utilisateurs une expérience plus dynamique.

## FAQ

### Q1 : Puis-je ajouter plusieurs hyperliens dans le même document à l’aide d’Aspose.Note ?

A1 : Oui, vous pouvez ajouter plusieurs hyperliens vers différents segments de texte dans un seul document Aspose.Note.

### Q2 : Puis-je personnaliser l’apparence des hyperliens dans les documents Aspose.Note ?

A2 : Oui, vous pouvez personnaliser divers attributs tels que la couleur de la police, la taille de la police et le style de police pour les hyperliens dans les documents Aspose.Note.

### Q3 : Aspose.Note prend-il en charge les hyperliens vers des sites Web externes ?

A3 : Oui, Aspose.Note vous permet de créer des hyperliens qui dirigent les utilisateurs vers des sites Web ou des pages Web externes.

### Q4 : Aspose.Note est-il compatible avec toutes les versions de Microsoft OneNote ?

A4 : Aspose.Note est conçu pour fonctionner avec Microsoft OneNote 2010 et les versions ultérieures.

### Q5 : Puis-je ajouter des hyperliens par programme à l’aide des API Aspose.Note ?

A5 : Oui, Aspose.Note fournit des API qui vous permettent d'ajouter des hyperliens vers du texte par programmation dans vos applications .NET.