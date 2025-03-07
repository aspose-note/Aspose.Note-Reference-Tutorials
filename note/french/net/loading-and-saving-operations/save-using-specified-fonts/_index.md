---
title: Enregistrer en utilisant les polices spécifiées dans Aspose.Note
linktitle: Enregistrer en utilisant les polices spécifiées dans Aspose.Note
second_title: API Aspose.Note .NET
description: Découvrez comment enregistrer des documents avec les polices spécifiées dans Aspose.Note pour .NET. Personnalisez facilement les paramètres de police pour un formatage cohérent des documents.
weight: 28
url: /fr/net/loading-and-saving-operations/save-using-specified-fonts/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Enregistrer en utilisant les polices spécifiées dans Aspose.Note

## Introduction

Dans ce didacticiel, nous apprendrons comment enregistrer des documents en utilisant les polices spécifiées dans Aspose.Note pour .NET. Nous explorerons différentes méthodes pour y parvenir, étape par étape.

## Conditions préalables

Avant de commencer, assurez-vous d'avoir les éléments suivants :

1.  Aspose.Note pour .NET : assurez-vous d'avoir installé Aspose.Note pour .NET. Vous pouvez le télécharger depuis[ici](https://releases.aspose.com/note/net/).

2. Environnement de développement : vous avez besoin d'un environnement de développement configuré pour le développement .NET.

## Importer des espaces de noms

Commençons par importer les espaces de noms nécessaires :

```csharp
using System;
using System.IO;

using Aspose.Note.Fonts;
using Aspose.Note.Saving;

```

## Étape 1 : enregistrement avec le nom de police par défaut

Dans cette étape, nous enregistrerons un document en utilisant un nom de police par défaut spécifié.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName()
{
    // Le chemin d'accès au répertoire des documents.
    string dataDir = "Your Document Directory";

    // Chargez le document dans Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Enregistrez le document au format PDF avec la police par défaut spécifiée.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFont("Times New Roman")
                          });
}
```

## Étape 2 : enregistrement avec la police par défaut du fichier

Ensuite, enregistrons un document en utilisant une police par défaut chargée à partir d'un fichier.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile()
{
    // Le chemin d'accès au répertoire des documents.
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    // Chargez le document dans Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Enregistrez le document au format PDF avec la police par défaut chargée à partir du fichier.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromFile(fontFile)
                          });
}
```

## Étape 3 : enregistrement avec la police par défaut de Stream

Enfin, enregistrons un document en utilisant une police par défaut chargée à partir d'un flux.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream()
{
    // Le chemin d'accès au répertoire des documents.
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    // Chargez le document dans Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Enregistrez le document au format PDF avec la police par défaut chargée à partir du flux.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf";

    using (var stream = File.Open(fontFile, FileMode.Open, FileAccess.Read, FileShare.Read))
    {
        oneFile.Save(dataDir, new PdfSaveOptions()
                              {
                                  FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromStream(stream)
                              });
    }
}
```

## Conclusion

Dans ce didacticiel, nous avons expliqué comment enregistrer des documents à l'aide des polices spécifiées dans Aspose.Note pour .NET. En suivant ces étapes, vous pouvez personnaliser les paramètres de police en fonction de vos besoins, garantissant ainsi que vos documents sont formatés comme vous le souhaitez.

## FAQ

### Q1 : Puis-je utiliser n’importe quelle police pour enregistrer des documents dans Aspose.Note ?

A1 : Oui, vous pouvez spécifier n'importe quelle police pour enregistrer les documents. Assurez-vous simplement que le fichier de police est accessible et chargé correctement.

### Q2 : Aspose.Note est-il compatible avec différents formats de documents ?

A2 : Aspose.Note fonctionne principalement avec les documents OneNote mais offre des options pour enregistrer dans divers formats, y compris PDF.

### Q3 : Comment puis-je gérer les polices manquantes lors de l'enregistrement de documents ?

A3 : Aspose.Note propose des options pour utiliser les polices par défaut au cas où la police spécifiée serait manquante, garantissant ainsi un formatage cohérent du document.

### Q4 : Aspose.Note prend-il en charge l'intégration de polices dans les documents de sortie ?

A4 : Oui, Aspose.Note permet d'intégrer des polices pour garantir la portabilité des documents et un rendu cohérent sur différentes plates-formes.

### Q5 : Où puis-je obtenir de l'aide supplémentaire concernant Aspose.Note ?

 A5 : Pour une assistance supplémentaire ou un support technique, vous pouvez visiter le[Forum Aspose.Note](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
