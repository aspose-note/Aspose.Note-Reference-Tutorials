---
title: Convertir des blocs-notes en PDF (aplati) dans Aspose Note .NET
linktitle: Convertir des blocs-notes en PDF (aplati) dans Aspose Note .NET
second_title: API Aspose.Note .NET
description: Découvrez comment convertir facilement des blocs-notes OneNote en PDF aplatis à l’aide d’Aspose.Note pour .NET. Préservez votre contenu en toute transparence.
weight: 15
url: /fr/net/notebook-operations/convert-to-pdf-flattened/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir des blocs-notes en PDF (aplati) dans Aspose Note .NET

## Introduction

Cherchez-vous à convertir vos blocs-notes OneNote en PDF aplatis à l’aide d’Aspose Note .NET ? Vous êtes au bon endroit ! Dans ce didacticiel, nous suivrons le processus étape par étape.

## Conditions préalables

Avant de commencer, assurez-vous d'avoir les éléments suivants :

1.  Aspose.Note pour .NET : assurez-vous d'avoir téléchargé et installé Aspose.Note pour .NET. Sinon, vous pouvez l'obtenir auprès de[ici](https://releases.aspose.com/note/net/).
2. Visual Studio : vous aurez besoin de Visual Studio installé sur votre système pour le codage et la compilation.
3. Bloc-notes OneNote : préparez un bloc-notes OneNote que vous souhaitez convertir en PDF.

## Importer des espaces de noms

Commençons par importer les espaces de noms nécessaires dans votre code C# :

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Collections.Generic;
```

## Étape 1 : Chargez le bloc-notes OneNote

```csharp
// Le chemin d'accès au répertoire des documents.
string dataDir = "Your Document Directory";

// Charger un bloc-notes OneNote
var notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

 Dans cette étape, nous chargeons le bloc-notes OneNote à l'aide du`Notebook` classe fournie par Aspose.Note.

## Étape 2 : Convertir en PDF avec aplatissement

```csharp
// Enregistrez le bloc-notes au format PDF avec aplatissement
dataDir = dataDir + "ConvertToPDFAsFlattened_out.pdf";
notebook.Save(
    dataDir,
    new NotebookPdfSaveOptions
    {
        Flatten = true
    }); 
```

 Ici, nous enregistrons le cahier chargé au format PDF avec le`Flatten` propriété définie sur`true`. Cette propriété aplatit tout le contenu, y compris les annotations et les images, dans le PDF.

## Étape 3 : Imprimer le message de réussite

```csharp
Console.WriteLine("\nNoteBook document converted to PDF as flattened successfully.\nFile saved at " + dataDir);
```

Enfin, nous imprimons un message de réussite ainsi que le chemin où le PDF est enregistré.

## Conclusion

Toutes nos félicitations! Vous avez converti avec succès votre bloc-notes OneNote en PDF aplati à l'aide d'Aspose.Note pour .NET. Ce processus garantit que tout votre contenu est conservé avec précision au format PDF, ce qui facilite son partage et sa distribution.

## FAQ

### Q1 : Puis-je conserver des éléments interactifs dans le PDF ?

A1 : Aspose.Note aplatit le contenu, y compris les éléments interactifs tels que les cases à cocher ou les champs de formulaire, dans le PDF, les rendant ainsi statiques.

### Q2 : Aspose.Note prend-il en charge la conversion des blocs-notes vers d'autres formats ?

A2 : Oui, Aspose.Note prend en charge la conversion des blocs-notes vers divers formats tels que PDF, HTML, Image, etc.

### Q3 : Puis-je personnaliser les options de conversion ?

A3 : Absolument ! Aspose.Note fournit de nombreuses options de personnalisation pendant le processus de conversion, vous permettant d'adapter la sortie en fonction de vos besoins.

### Q4 : Existe-t-il une version d'essai disponible ?

 A4 : Oui, vous pouvez obtenir un essai gratuit d'Aspose.Note auprès de[ici](https://releases.aspose.com/).

### Q5 : Où puis-je obtenir de l'aide si je rencontre des problèmes ?

 A5 : Vous pouvez demander l’aide de la communauté Aspose à[Forums Aspose.Note](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
