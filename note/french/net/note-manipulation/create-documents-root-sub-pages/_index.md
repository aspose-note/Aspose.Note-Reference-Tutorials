---
title: Créez des documents avec racine et sous-pages à l'aide d'Aspose.Note
linktitle: Créez des documents avec racine et sous-pages à l'aide d'Aspose.Note
second_title: API Aspose.Note .NET
description: Découvrez comment utiliser Aspose.Note pour .NET pour créer des documents OneNote dynamiques avec des structures hiérarchiques.
type: docs
weight: 11
url: /fr/net/note-manipulation/create-documents-root-sub-pages/
---
## Introduction

Bienvenue dans notre tutoriel sur la création de documents avec racine et sous-pages à l'aide d'Aspose.Note pour .NET ! Aspose.Note est une bibliothèque puissante qui permet aux développeurs de travailler avec des fichiers Microsoft OneNote par programme, permettant la création, la manipulation et la conversion de documents OneNote.

Dans ce didacticiel, nous vous guiderons étape par étape tout au long du processus de création d'un document OneNote avec racine et sous-pages. Nous fournirons des explications détaillées et des extraits de code en utilisant Aspose.Note pour .NET, ce qui vous permettra de suivre et de mettre en œuvre facilement vos propres projets.

## Conditions préalables

Avant de commencer, assurez-vous d'avoir les prérequis suivants :

1. Visual Studio : vous aurez besoin de Visual Studio installé sur votre système pour écrire et compiler du code .NET.
2.  Aspose.Note pour .NET : téléchargez et installez Aspose.Note pour .NET à partir du[page de téléchargement](https://releases.aspose.com/note/net/).
3. Connaissances de base en C# : Une connaissance du langage de programmation C# est requise pour comprendre et mettre en œuvre les exemples de code.

Maintenant que tout est configuré, passons au tutoriel !

## Importer des espaces de noms

Tout d'abord, importons les espaces de noms nécessaires dans notre projet :

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using System.Drawing;
```

## Étape 1 : initialiser l'objet de document

```csharp
//Créer un objet de la classe Document
Document doc = new Document();
```

## Étape 2 : Créer une page racine et des sous-pages

```csharp
// Initialiser les objets de classe Page et définir leurs niveaux
Page page1 = new Page(doc) { Level = 1 };
Page page2 = new Page(doc) { Level = 2 };
Page page3 = new Page(doc) { Level = 1 };
```

### Pour la page 1 :

```csharp
Outline outline1 = new Outline(doc);
OutlineElement outlineElem1 = new OutlineElement(doc);
ParagraphStyle textStyle1 = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text1 = new RichText(doc) { Text = "First page.", ParagraphStyle = textStyle1 };
outlineElem1.AppendChildLast(text1);
outline1.AppendChildLast(outlineElem1);
page1.AppendChildLast(outline1);
```

### Pour la page 2 :

```csharp
Outline outline2 = new Outline(doc);
OutlineElement outlineElem2 = new OutlineElement(doc);
ParagraphStyle textStyle2 = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text2 = new RichText(doc) { Text = "Second page.", ParagraphStyle = textStyle2 };
outlineElem2.AppendChildLast(text2);
outline2.AppendChildLast(outlineElem2);
page2.AppendChildLast(outline2);
```

### Pour la page 3 :

```csharp
Outline outline3 = new Outline(doc);
OutlineElement outlineElem3 = new OutlineElement(doc);
ParagraphStyle textStyle3 = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text3 = new RichText(doc) { Text = "Third page.", ParagraphStyle = textStyle3 };
outlineElem3.AppendChildLast(text3);
outline3.AppendChildLast(outlineElem3);
page3.AppendChildLast(outline3);
```

## Étape 4 : ajouter des pages au document

```csharp
// Ajouter des pages au document OneNote
doc.AppendChildLast(page1);
doc.AppendChildLast(page2);
doc.AppendChildLast(page3);
```

## Étape 5 : Enregistrer le document

```csharp
// Enregistrer le document OneNote
string dataDir = "Your Document Directory";
dataDir = dataDir + "CreateDocWithRootAndSubPages_out.one";
doc.Save(dataDir);
```

## Conclusion

Toutes nos félicitations! Vous avez appris avec succès comment créer des documents avec racine et sous-pages à l'aide d'Aspose.Note pour .NET. Vous pouvez désormais utiliser ces connaissances pour générer dynamiquement des documents OneNote complexes dans vos applications.

## FAQ

### Q1 : Aspose.Note peut-il gérer des documents OneNote volumineux ?

A1 : Oui, Aspose.Note est conçu pour gérer efficacement les documents OneNote volumineux sans compromettre les performances.

### Q2 : Aspose.Note est-il compatible avec .NET Core ?

A2 : Oui, Aspose.Note prend en charge .NET Core ainsi que le .NET Framework traditionnel.

### Q3 : Puis-je convertir des documents OneNote vers d’autres formats à l’aide d’Aspose.Note ?

A3 : Absolument, Aspose.Note offre des capacités de conversion vers divers formats, notamment PDF, DOCX, HTML, etc.

### Q4 : Aspose.Note propose-t-il une intégration cloud ?

A4 : Aspose.Note se concentre principalement sur le développement sur site, mais vous pouvez l'utiliser dans des environnements cloud avec une configuration appropriée.

### Q5 : Le support technique est-il disponible pour Aspose.Note ?

A5 : Oui, Aspose fournit une assistance technique dédiée via son forum où vous pouvez poser des questions et obtenir de l'aide.