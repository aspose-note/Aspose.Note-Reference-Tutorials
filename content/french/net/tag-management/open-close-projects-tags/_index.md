---
title: Ouvrir et fermer des projets avec des balises dans Aspose.Note
linktitle: Ouvrir et fermer des projets avec des balises dans Aspose.Note
second_title: API Aspose.Note .NET
description: Découvrez comment manipuler les fichiers Microsoft OneNote par programme à l'aide d'Aspose.Note pour .NET. Ouvrez et fermez efficacement des projets avec des balises.
type: docs
weight: 15
url: /fr/net/tag-management/open-close-projects-tags/
---
## Introduction

Dans ce didacticiel, nous apprendrons comment utiliser Aspose.Note pour .NET pour ouvrir et fermer des projets avec des balises. Aspose.Note est une API puissante qui permet aux développeurs de travailler avec des fichiers Microsoft OneNote par programme, permettant des tâches telles que la manipulation de texte, d'images et de balises dans les documents.

## Conditions préalables

Avant de commencer, assurez-vous d'avoir configuré les conditions préalables suivantes :

## Importer des espaces de noms

```csharp
using System.IO;
using System.Linq;
```

Décomposons maintenant chaque exemple en plusieurs étapes :

## Étape 1 : Charger le document

Tout d’abord, nous devons charger le document dans Aspose.Note.

```csharp
string dataDir = "Your Document Directory";
var oneFile = new Document(Path.Combine(dataDir, "ProjectNotes.one"));
```

## Étape 2 : Fermer les éléments du projet C

Maintenant, fermons toutes les cases à cocher liées au « Projet C ».

```csharp
foreach (var node in oneFile.GetChildNodes<ITaggable>())
{
    foreach (var checkBox in node.Tags.OfType<CheckBox>())
    {
        if (checkBox.Label.Contains("Project C") && !checkBox.Checked)
        {
            checkBox.SetCompleted();
        }
    }
}
```

## Étape 3 : Enregistrez les notes du projet C fermé

Enregistrez le document modifié avec les éléments fermés du « Projet C ».

```csharp
oneFile.Save("Path to save the closed Project C notes");
```

## Étape 4 : ouvrir les éléments du projet C

Ensuite, ouvrons toutes les cases à cocher liées au « Projet C ».

```csharp
var oneFile = new Document("Path to the closed Project C notes");

foreach (var node in oneFile.GetChildNodes<ITaggable>())
{
    foreach (var checkBox in node.Tags.OfType<CheckBox>())
    {
        if (checkBox.Label.Contains("Project C") && checkBox.Checked)
        {
            checkBox.SetOpen();
        }
    }
}
```

## Étape 5 : Enregistrez les notes ouvertes du projet C

Enregistrez le document modifié avec les éléments ouverts du « Projet C ».

```csharp
oneFile.Save(Path.Combine(dataDir, "ProjectNoteWithOpenProjectC.one"));
```

Vous avez maintenant appris à ouvrir et fermer des projets avec des balises dans Aspose.Note à l'aide de .NET.

## Conclusion

Aspose.Note pour .NET fournit un moyen pratique de manipuler des documents OneNote par programme. En suivant ce tutoriel, vous pourrez gérer efficacement vos projets en ouvrant et fermant des éléments à l'aide de balises.

## FAQ

### Q1 : Aspose.Note est-il compatible avec toutes les versions de OneNote ?

A1 : Aspose.Note prend en charge Microsoft OneNote 2010 et les versions plus récentes.

### Q2 : Puis-je utiliser Aspose.Note pour des projets commerciaux ?

 A2 : Oui, vous pouvez utiliser Aspose.Note pour des projets personnels et commerciaux. Visite[ici](https://purchase.aspose.com/buy) pour acheter une licence.

### Q3 : Aspose.Note propose-t-il un essai gratuit ?

A3 : Oui, vous pouvez bénéficier d'un essai gratuit[ici](https://releases.aspose.com/).

### Q4 : Où puis-je trouver de la documentation pour Aspose.Note ?

 A4 : Vous pouvez trouver la documentation[ici](https://reference.aspose.com/note/net/).

### Q5 : Où puis-je obtenir de l'aide pour Aspose.Note ?

A5 : Pour obtenir de l'aide, vous pouvez visiter Aspose.Note[forum](https://forum.aspose.com/c/note/28).