---
title: Ajouter un nœud d'image avec une balise dans Aspose.Note
linktitle: Ajouter un nœud d'image avec une balise dans Aspose.Note
second_title: API Aspose.Note .NET
description: Découvrez comment améliorer vos documents OneNote en ajoutant des images avec des balises personnalisées à l'aide d'Aspose.Note pour .NET.
weight: 10
url: /fr/net/tag-management/add-image-node-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ajouter un nœud d'image avec une balise dans Aspose.Note

## Introduction

Dans ce didacticiel, nous allons explorer comment ajouter un nœud d'image avec une balise à l'aide d'Aspose.Note pour .NET. Cette fonctionnalité vous permet d'améliorer vos documents OneNote en ajoutant des images avec des balises personnalisées.

## Conditions préalables

Avant de commencer, assurez-vous d'avoir les éléments suivants :

1. Visual Studio : installez Visual Studio IDE sur votre système.
2.  Aspose.Note pour .NET : téléchargez et installez la bibliothèque Aspose.Note pour .NET à partir du[lien de téléchargement](https://releases.aspose.com/note/net/).
3. Connaissances de base : Familiarisez-vous avec le langage de programmation C# et le framework .NET.

## Importer des espaces de noms

Tout d’abord, assurez-vous d’inclure les espaces de noms nécessaires dans votre code C# :

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

## Étape 1 : initialiser les objets de document et de page

 Commencez par créer une instance de`Document` classe et un`Page` objet:

```csharp
Document doc = new Document();
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## Étape 2 : initialiser les objets Outline et OutlineElement

 Ensuite, initialisez`Outline` et`OutlineElement` objets:

```csharp
Outline outline = new Outline(doc);
OutlineElement outlineElem = new OutlineElement(doc);
```

## Étape 3 : Charger et insérer une image

Chargez l'image souhaitée et insérez-la dans le nœud du document :

```csharp
Aspose.Note.Image image = new Aspose.Note.Image(doc, "path_to_your_image.jpg");
outlineElem.AppendChildLast(image);
```

## Étape 4 : ajouter une balise à l'image

Ajoutez une balise personnalisée à l'image :

```csharp
image.Tags.Add(NoteTag.CreateYellowStar());
```

## Étape 5 : Ajouter un élément de plan et des nœuds de page

Ajoutez l'élément de plan et les nœuds de plan à la page :

```csharp
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
```

## Étape 6 : Enregistrez le document

Enregistrez le document OneNote modifié :

```csharp
doc.AppendChildLast(page);
string outputFilePath = "output_path/AddImageNodeWithTag_out.one";
doc.Save(outputFilePath);
```

## Conclusion

En suivant ces étapes, vous pouvez ajouter en toute transparence un nœud d'image avec une balise personnalisée à l'aide d'Aspose.Note pour .NET, enrichissant ainsi vos documents OneNote avec des visuels personnalisés.

## FAQ

### Q1 : Puis-je ajouter plusieurs images avec des balises différentes dans un seul document à l’aide d’Aspose.Note ?

A1 : Oui, vous pouvez ajouter plusieurs images avec des balises différentes en suivant des étapes similaires pour chaque image.

### Q2 : Aspose.Note est-il compatible avec toutes les versions de OneNote ?

A2 : Aspose.Note prend en charge différentes versions de OneNote, garantissant la compatibilité entre différents environnements.

### Q3 : Puis-je personnaliser l’apparence de la balise ajoutée à l’image ?

A3 : Oui, Aspose.Note offre une flexibilité dans la personnalisation de l’apparence des balises en fonction de vos préférences.

### Q4 : Aspose.Note offre-t-il la prise en charge de l'ajout d'images à partir d'URL ?

A4 : Aspose.Note prend principalement en charge l'ajout d'images à partir de répertoires locaux, mais vous pouvez incorporer des images externes en les téléchargeant d'abord localement.

### Q5 : Existe-t-il des limites quant à la taille ou au format des images pouvant être ajoutées ?

A5 : Aspose.Note prend en charge un large éventail de formats d'image et n'impose aucune limitation stricte sur la taille de l'image, vous permettant d'incorporer divers visuels dans vos documents.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
