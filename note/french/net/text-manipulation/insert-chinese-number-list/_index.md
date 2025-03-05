---
title: Insérer une liste de numéros chinois dans le texte Aspose.Note
linktitle: Insérer une liste de numéros chinois dans le texte Aspose.Note
second_title: API Aspose.Note .NET
description: Découvrez comment insérer sans effort des listes de numéros chinois dans Aspose.Note pour les documents .NET. Améliorez vos compétences en matière de formatage de documents avec ce guide étape par étape.
type: docs
weight: 20
url: /fr/net/text-manipulation/insert-chinese-number-list/
---
## Introduction
Cherchez-vous à améliorer vos compétences Aspose.Note pour .NET en incorporant des listes de chiffres chinois dans vos documents ? Si c'est le cas, vous êtes au bon endroit ! Dans ce didacticiel, nous vous guiderons tout au long du processus d'insertion de listes de numéros chinois à l'aide d'Aspose.Note pour .NET. Cette puissante bibliothèque vous permet de manipuler les documents OneNote de manière transparente.
## Conditions préalables
Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :
- Connaissance de base de la programmation C#.
-  Aspose.Note pour .NET installé. Vous pouvez le télécharger[ici](https://releases.aspose.com/note/net/).
## Importer des espaces de noms
Pour commencer, importez les espaces de noms nécessaires dans votre projet :
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## Étape 1 : initialiser le document OneNote
```csharp
string dataDir = "Your Document Directory";
Aspose.Note.Document doc = new Aspose.Note.Document();
```
## Étape 2 : initialiser la page OneNote
```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
Outline outline = new Outline(doc);
```
## Étape 3 : appliquer les paramètres de style de texte
```csharp
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## Étape 4 : Créer des éléments de plan
Créons maintenant trois éléments de plan avec des listes de nombres chinois :
### Étape 4.1 : Premier élément
```csharp
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
```
### Étape 4.2 : Deuxième élément
```csharp
OutlineElement outlineElem2 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text2 = new RichText(doc) { Text = "Second", ParagraphStyle = defaultStyle };
outlineElem2.AppendChildLast(text2);
```
### Étape 4.3 : Troisième élément
```csharp
OutlineElement outlineElem3 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text3 = new RichText(doc) { Text = "Third", ParagraphStyle = defaultStyle };
outlineElem3.AppendChildLast(text3);
```
## Étape 5 : Ajouter des éléments au plan
```csharp
outline.AppendChildLast(outlineElem1);
outline.AppendChildLast(outlineElem2);
outline.AppendChildLast(outlineElem3);
```
## Étape 6 : Ajouter le plan à la page
```csharp
page.AppendChildLast(outline);
```
## Étape 7 : Ajouter une page au document
```csharp
doc.AppendChildLast(page);
```
## Étape 8 : Enregistrer le document OneNote
```csharp
dataDir = dataDir + "InsertChineseNumberList_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nChinese number list inserted successfully.\nFile saved at " + dataDir);
```
Toutes nos félicitations! Vous avez inséré avec succès des listes de numéros chinois dans votre document Aspose.Note à l'aide de la bibliothèque .NET.
## Conclusion
Dans ce didacticiel, nous avons couvert le processus étape par étape d'intégration de listes de numéros chinois dans vos documents Aspose.Note pour .NET. Améliorez vos compétences en matière de formatage de documents et rendez votre contenu plus attrayant grâce à ces techniques.
## FAQ
### Q : Puis-je personnaliser le formatage des listes de numéros chinois ?
 R : Oui, vous pouvez personnaliser le formatage en ajustant les paramètres dans le`NumberList` constructeur.
### Q : Aspose.Note est-il compatible avec la dernière version de .NET ?
R : Oui, Aspose.Note est régulièrement mis à jour pour prendre en charge les dernières versions de .NET.
### Q : Où puis-je trouver des exemples et de la documentation supplémentaires ?
R : Explorez l'ensemble[Documentation Aspose.Note](https://reference.aspose.com/note/net/).
### Q : Comment puis-je obtenir une licence temporaire pour Aspose.Note ?
 R : Obtenez une licence temporaire[ici](https://purchase.aspose.com/temporary-license/).
### Q : Où puis-je demander de l'aide ou discuter des requêtes liées à Aspose.Note ?
 R : Visitez le[Forum d'assistance Aspose.Note](https://forum.aspose.com/c/note/28) pour le soutien de la communauté.