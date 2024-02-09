---
title: Enregistrer au format PDF dans Aspose.Note
linktitle: Enregistrer au format PDF dans Aspose.Note
second_title: API Aspose.Note .NET
description: Découvrez comment enregistrer des documents Microsoft OneNote au format PDF à l'aide d'Aspose.Note pour .NET. Tutoriel étape par étape avec des exemples de code pour les mises en page Lettre et A4.
type: docs
weight: 26
url: /fr/net/loading-and-saving-operations/save-to-pdf/
---
## Introduction

Dans ce didacticiel, nous verrons comment enregistrer des documents au format PDF à l'aide d'Aspose.Note pour .NET. Aspose.Note est une bibliothèque puissante qui permet aux développeurs de travailler avec des fichiers Microsoft OneNote par programme. Nous couvrirons les conditions préalables, importerons des espaces de noms et fournirons des guides étape par étape pour enregistrer des documents au format PDF dans différentes mises en page.

## Conditions préalables

Avant de commencer, assurez-vous d'avoir les éléments suivants :

- Visual Studio installé sur votre système.
-  Aspose.Note pour la bibliothèque .NET téléchargée et installée. Vous pouvez le télécharger depuis[ici](https://releases.aspose.com/note/net/).
- Connaissance de base du langage de programmation C#.

## Importer des espaces de noms

Tout d’abord, importons les espaces de noms nécessaires dans notre code C# :

```csharp
using System;
using System.IO;

using Aspose.Note.Saving;
```

Maintenant que nous avons couvert les conditions préalables et importé les espaces de noms, procédons à l'enregistrement des documents au format PDF dans différentes mises en page.

## Étape 1 : Enregistrer au format PDF à l'aide des paramètres de page de lettre


```csharp
public static void SaveToPdfUsingLetterPageSettings()
{
    // Le chemin d'accès au répertoire des documents.
    string dataDir = "Your Document Directory";

    // Chargez le document dans Aspose.Note.
    Document oneFile = new Document(dataDir + "OneNote.one");

    var dst = Path.Combine(dataDir, "SaveToPdfUsingLetterPageSettings.pdf");

    //Enregistrez le document.
    oneFile.Save(dst, new PdfSaveOptions() { PageSettings = PageSettings.Letter });

    Console.WriteLine("\nOneNote document saved successfully.\nFile saved at " + dst);
}
```

### Explication:

- Nous chargeons le document OneNote dans Aspose.Note.
- Définissez le chemin de destination du fichier PDF enregistré.
-  Enregistrez le document au format PDF en utilisant`PdfSaveOptions` avec`PageSettings` mis à`Letter`.

## Étape 2 : Enregistrer au format PDF en utilisant les paramètres de page A4 sans limite de hauteur

```csharp
public static void SaveToPdfUsingA4PageSettingsWithoutHeightLimit()
{
    // Le chemin d'accès au répertoire des documents.
    string dataDir = "Your Document Directory";

    // Chargez le document dans Aspose.Note.
    Document oneFile = new Document(dataDir + "OneNote.one");

    var dst = Path.Combine(dataDir, "SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf");

    //Enregistrez le document.
    oneFile.Save(dst, new PdfSaveOptions() { PageSettings = PageSettings.A4NoHeightLimit });

    Console.WriteLine("\nOneNote document saved successfully.\nFile saved at " + dst);
}
```

### Explication:

- Semblable à l’étape précédente, nous chargeons le document OneNote dans Aspose.Note.
- Définissez le chemin de destination du fichier PDF enregistré.
-  Enregistrez le document au format PDF en utilisant`PdfSaveOptions` avec`PageSettings` mis à`A4NoHeightLimit`.

## Conclusion

Dans ce didacticiel, nous avons appris à enregistrer des documents au format PDF à l'aide d'Aspose.Note pour .NET. Nous avons couvert deux mises en page différentes : Lettre et A4 sans limite de hauteur. Avec Aspose.Note, les développeurs peuvent facilement manipuler les fichiers OneNote par programmation, offrant ainsi flexibilité et efficacité dans les tâches de gestion de documents.

## FAQ

### Q1 : Aspose.Note peut-il gérer des fichiers OneNote complexes ?

A1 : Oui, Aspose.Note prend en charge diverses fonctionnalités pour gérer efficacement les fichiers OneNote complexes.

### Q2 : Aspose.Note est-il adapté aux projets commerciaux ?

 A2 : Absolument, Aspose.Note peut être utilisé facilement dans des projets commerciaux. Vous pouvez acheter une licence[ici](https://purchase.aspose.com/buy).

### Q3 : Aspose.Note propose-t-il un essai gratuit ?

 A3 : Oui, vous pouvez explorer Aspose.Note avec un essai gratuit disponible[ici](https://releases.aspose.com/).

### Q4 : Où puis-je trouver de la documentation pour Aspose.Note ?

 A4 : Vous pouvez trouver une documentation détaillée[ici](https://reference.aspose.com/note/net/).

### Q5 : Besoin d’une aide supplémentaire ?

 A5 : N'hésitez pas à poser des questions ou à demander de l'aide sur le forum Aspose.Note[ici](https://forum.aspose.com/c/note/28).