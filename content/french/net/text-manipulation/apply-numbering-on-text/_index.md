---
title: Appliquer la numérotation sur le texte dans Aspose.Note
linktitle: Appliquer la numérotation sur le texte dans Aspose.Note
second_title: API Aspose.Note .NET
description: Découvrez comment appliquer la numérotation de texte dans Aspose.Note pour .NET avec ce didacticiel complet. Améliorez le formatage de vos documents sans effort.
type: docs
weight: 12
url: /fr/net/text-manipulation/apply-numbering-on-text/
---
## Introduction
Aspose.Note pour .NET fournit des outils puissants pour la manipulation de documents dans les applications C#. Dans ce didacticiel, nous explorerons le processus d'application de la numérotation sur du texte à l'aide d'Aspose.Note. Suivez ces instructions étape par étape pour améliorer le formatage de votre document sans effort.
## Conditions préalables
Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :
- Compréhension de base du langage de programmation C#.
-  Aspose.Note pour .NET installé. Vous pouvez le télécharger[ici](https://releases.aspose.com/note/net/).
- Un environnement de développement intégré (IDE) tel que Visual Studio.
## Importer des espaces de noms
Pour commencer, assurez-vous d'importer les espaces de noms nécessaires dans votre projet C# :
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## Étape 1 : Configurez votre document
Commencez par créer un nouveau document et initialisez les objets requis :
```csharp
// Le chemin d'accès au répertoire des documents.
string dataDir = "Your Document Directory";
//Créer un objet de la classe Document
Document doc = new Document();
// Initialiser l'objet de classe Page
Aspose.Note.Page page = new Aspose.Note.Page(doc);
// Initialiser l'objet de classe Outline
Outline outline = new Outline(doc);
```
## Étape 2 : définir le style par défaut
Configurez le style par défaut de votre texte à l'aide de la classe ParagraphStyle :
```csharp
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## Étape 3 : Appliquer la numérotation
Initialisez les objets de la classe OutlineElement et appliquez une numérotation à chaque élément :
```csharp
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
OutlineElement outlineElem2 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text2 = new RichText(doc) { Text = "Second", ParagraphStyle = defaultStyle };
outlineElem2.AppendChildLast(text2);
OutlineElement outlineElem3 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text3 = new RichText(doc) { Text = "Third", ParagraphStyle = defaultStyle };
outlineElem3.AppendChildLast(text3);
```
## Étape 4 : Ajouter des éléments de plan
Ajoutez les éléments de plan au plan :
```csharp
outline.AppendChildLast(outlineElem1);
outline.AppendChildLast(outlineElem2);
outline.AppendChildLast(outlineElem3);
```
## Étape 5 : Enregistrez le document
Enregistrez le document OneNote avec la numérotation appliquée :
```csharp
dataDir = dataDir + "ApplyNumberingOnText_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nNumbering applied successfully on a text.\nFile saved at " + dataDir); 
```
## Conclusion
Toutes nos félicitations! Vous avez appris avec succès comment appliquer la numérotation sur du texte dans Aspose.Note pour .NET. Expérimentez avec différentes options de formatage pour créer sans effort des documents visuellement attrayants.
## FAQ
### 1. Puis-je personnaliser le format de numérotation ?
Oui, la classe NumberList vous permet de personnaliser le format de numérotation selon vos préférences.
### 2. Existe-t-il d'autres options de formatage disponibles ?
Aspose.Note propose une large gamme d'options de formatage, notamment le style de police, la couleur, etc.
### 3. Aspose.Note est-il compatible avec Visual Studio ?
Absolument! Aspose.Note s'intègre parfaitement à Visual Studio pour une expérience de développement fluide.
### 4. Puis-je essayer Aspose.Note avant d’acheter ?
 Certainement! Vous pouvez explorer un essai gratuit[ici](https://releases.aspose.com/).
### 5. Où puis-je obtenir de l'aide pour Aspose.Note ?
 Pour toute assistance ou question, visitez le[Forum Aspose.Note](https://forum.aspose.com/c/note/28).