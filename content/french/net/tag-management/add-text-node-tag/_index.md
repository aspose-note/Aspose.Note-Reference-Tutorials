---
title: Ajouter un nœud de texte avec une balise dans Aspose.Note
linktitle: Ajouter un nœud de texte avec une balise dans Aspose.Note
second_title: API Aspose.Note .NET
description: Découvrez comment ajouter des nœuds de texte avec des balises aux documents OneNote à l'aide d'Aspose.Note pour .NET.
type: docs
weight: 12
url: /fr/net/tag-management/add-text-node-tag/
---
## Introduction

Aspose.Note pour .NET est une bibliothèque puissante qui permet aux développeurs de créer, manipuler et convertir des fichiers Microsoft OneNote par programme à l'aide du framework .NET. Dans ce didacticiel, nous allons explorer comment ajouter un nœud de texte avec une balise à un document OneNote à l'aide d'Aspose.Note pour .NET.

## Conditions préalables

Avant de commencer, assurez-vous d'avoir les prérequis suivants :

1. Visual Studio : assurez-vous que Visual Studio est installé sur votre système.
2.  Aspose.Note pour .NET : téléchargez et installez Aspose.Note pour .NET à partir du[site web](https://releases.aspose.com/note/net/).
3. Connaissance de base de C# : Familiarisez-vous avec les principes fondamentaux du langage de programmation C#.

## Importer des espaces de noms

Tout d’abord, vous devez importer les espaces de noms nécessaires pour accéder aux classes et méthodes requises pour travailler avec Aspose.Note pour .NET.

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

## Étape 1 : Créer un objet de document

Initialisez un objet Document pour commencer à travailler avec un document OneNote.

```csharp
// Le chemin d'accès au répertoire des documents.
string dataDir = "Your Document Directory";
Document doc = new Document();
```

## Étape 2 : initialiser les objets de page et de plan

Créez des objets Page et Plan pour structurer le contenu du document OneNote.

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
Outline outline = new Outline(doc);
```

## Étape 3 : ajouter un nœud de texte avec une balise

Créez un objet RichText avec le texte et le style souhaités, puis ajoutez-le à OutlineElement.

```csharp
OutlineElement outlineElem = new OutlineElement(doc);
ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text = new RichText(doc) { Text = "OneNote text.", ParagraphStyle = textStyle };
text.Tags.Add(NoteTag.CreateYellowStar());
outlineElem.AppendChildLast(text);
```

## Étape 4 : Ajouter un élément de plan et des nœuds de page

Ajoutez le OutlineElement au Outline, puis ajoutez le Outline à la page. Enfin, ajoutez la page au document.

```csharp
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## Étape 5 : Enregistrez le document

Enregistrez le document OneNote modifié dans un emplacement spécifié.

```csharp
string dataDir = "Your Document Directory";
string outputPath = Path.Combine(dataDir, "AddTextNodeWithTag_out.one");
doc.Save(outputPath);
```

## Conclusion

Toutes nos félicitations! Vous avez appris avec succès comment ajouter un nœud de texte avec une balise à un document OneNote à l'aide d'Aspose.Note pour .NET. Grâce à ces connaissances, vous pouvez désormais personnaliser et améliorer vos fichiers OneNote par programme.

## FAQ

### Q1 : Puis-je ajouter plusieurs nœuds de texte avec des balises différentes dans le même document ?

A1 : Oui, vous pouvez ajouter plusieurs nœuds de texte avec des balises différentes en suivant le même processus pour chaque nœud.

### Q2 : Aspose.Note pour .NET est-il compatible avec toutes les versions de OneNote ?

A2 : Aspose.Note pour .NET prend en charge différentes versions de OneNote, notamment 2010, 2013, 2016 et supérieures.

### Q3 : Puis-je personnaliser les couleurs et les styles des balises ?

A3 : Oui, vous pouvez personnaliser les couleurs et les styles des étiquettes en fonction de vos besoins.

### Q4 : Aspose.Note pour .NET prend-il en charge le chiffrement des documents ?

A4 : Oui, Aspose.Note pour .NET prend en charge le cryptage des documents pour garantir la sécurité des données.

### Q5 : Où puis-je trouver plus de ressources et d’assistance pour Aspose.Note pour .NET ?

 A5 : Vous pouvez explorer le[Aspose.Note pour la documentation .NET](https://reference.aspose.com/note/net/) et solliciter l'aide du[Forum Aspose.Note](https://forum.aspose.com/c/note/28).