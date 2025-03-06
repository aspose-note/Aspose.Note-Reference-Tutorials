---
title: Ajouter un nœud de table avec une balise dans Aspose.Note
linktitle: Ajouter un nœud de table avec une balise dans Aspose.Note
second_title: API Aspose.Note .NET
description: Découvrez comment ajouter des tables avec des balises dans Aspose.Note pour .NET. Améliorez vos compétences en manipulation de documents par programmation.
weight: 11
url: /fr/net/tag-management/add-table-node-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ajouter un nœud de table avec une balise dans Aspose.Note

## Introduction

Dans ce didacticiel, nous vous guiderons tout au long du processus d'ajout d'un nœud de table avec une balise à l'aide d'Aspose.Note pour .NET. Suivez les étapes ci-dessous pour y parvenir.

## Importer des espaces de noms

Avant de commencer, assurez-vous d'importer les espaces de noms nécessaires pour travailler avec Aspose. Remarque :

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using Aspose.Note.Examples.CSharp.Tables;
```

## Conditions préalables

Assurez-vous d'avoir configuré les conditions préalables suivantes avant de continuer :

1.  Installation : Téléchargez et installez la bibliothèque Aspose.Note pour .NET à partir de[ici](https://releases.aspose.com/note/net/).
2.  Licence : acquérir une licence ou utiliser un[permis temporaire](https://purchase.aspose.com/temporary-license/) pour utiliser la bibliothèque.
3. Environnement de développement : disposez d'un environnement de développement compatible, tel que Visual Studio.

## Étape 1 : initialiser les objets de document et de page

 Commencez par créer une instance du`Document` classe et initialiser un`Page` objet:

```csharp
Document doc = new Document();
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## Étape 2 : Créer des objets de table, de ligne et de cellule

 Initialisez le`Table`, `TableRow` , et`TableCell` objets:

```csharp
TableRow row = new TableRow(doc);
TableCell cell = new TableCell(doc);
```

## Étape 3 : Insérer du contenu dans la cellule

 Ajoutez du contenu à la cellule en utilisant le`AppendChildLast` méthode:

```csharp
cell.AppendChildLast(InsertTable.GetOutlineElementWithText(doc, "Single cell."));
```

## Étape 4 : initialiser le nœud de table

 Initialisez le`Table` objet avec les propriétés spécifiées :

```csharp
Table table = new Table(doc)
{
    IsBordersVisible = true,
    Columns = { new TableColumn { Width = 70 } }
};
```

## Étape 5 : ajouter une ligne au tableau

Ajoutez le nœud de ligne au tableau :

```csharp
table.AppendChildLast(row);
```

## Étape 6 : ajouter une balise au nœud de table

Incluez une balise pour le nœud de table :

```csharp
table.Tags.Add(NoteTag.CreateQuestionMark());
```

## Étape 7 : ajouter un nœud de table à l'élément de plan

 Créé un`Outline` et`OutlineElement` pour ajouter le nœud de table :

```csharp
Outline outline = new Outline(doc);
OutlineElement outlineElem = new OutlineElement(doc);
outlineElem.AppendChildLast(table);
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## Étape 8 : Enregistrer le document

Enregistrez le document OneNote :

```csharp
string dataDir = "Your Document Directory";
dataDir = dataDir + "AddTableNodeWithTag_out.one";
doc.Save(dataDir);
Console.WriteLine("\nTable node with tag added successfully.\nFile saved at " + dataDir);
```

Après avoir suivi ces étapes, vous devriez avoir ajouté avec succès un nœud de table avec une balise à l'aide d'Aspose.Note pour .NET.

## Conclusion

Dans ce didacticiel, nous avons couvert le processus d'ajout d'un nœud de table avec une balise dans Aspose.Note pour .NET. En suivant ces étapes, vous pouvez manipuler efficacement les documents OneNote par programmation, améliorant ainsi vos capacités de gestion de documents.

## FAQ

### Q1 : Aspose.Note est-il compatible avec toutes les versions de .NET ?

A1 : Aspose.Note pour .NET prend en charge les versions .NET Framework 2.0 et supérieures, y compris .NET Core et .NET Standard.

### Q2 : Puis-je essayer Aspose.Note avant d’acheter une licence ?

 A2 : Oui, vous pouvez obtenir un essai gratuit d'Aspose.Note auprès de[ici](https://releases.aspose.com/).

### Q3 : Comment puis-je acquérir une licence temporaire pour Aspose.Note ?

 A3 : Vous pouvez obtenir une licence temporaire auprès de[ce lien](https://purchase.aspose.com/temporary-license/), valable 30 jours.

### Q4 : Aspose.Note prend-il en charge le cryptage des documents ?

A4 : Oui, Aspose.Note prend en charge le cryptage des documents OneNote pour garantir la sécurité des données.

### Q5 : Le support technique est-il disponible pour les utilisateurs d'Aspose.Note ?

 A5 : Oui, le support technique est fourni via les forums Aspose[ici](https://forum.aspose.com/c/note/28), où vous pouvez demander l’aide d’experts.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
