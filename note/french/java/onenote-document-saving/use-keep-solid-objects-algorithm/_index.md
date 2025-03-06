---
title: Utiliser l'algorithme Conserver les objets solides dans OneNote - Aspose.Note
linktitle: Utiliser l'algorithme Conserver les objets solides dans OneNote - Aspose.Note
second_title: API Java Aspose.Note
description: Découvrez comment conserver les objets solides dans vos documents Aspose.Note lors de la conversion au format PDF à l'aide de l'algorithme Keep Solid Objects en Java.
weight: 25
url: /fr/java/onenote-document-saving/use-keep-solid-objects-algorithm/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Utiliser l'algorithme Conserver les objets solides dans OneNote - Aspose.Note

## Introduction

Dans ce didacticiel, nous explorerons comment utiliser l'algorithme Keep Solid Objects dans Aspose.Note pour Java. Cet algorithme est inestimable pour maintenir l'intégrité des objets solides dans vos documents lors de leur conversion au format PDF. Nous décomposerons le processus étape par étape, en garantissant la clarté et la compréhension à chaque étape.

## Conditions préalables

Avant de commencer, assurez-vous d'avoir les éléments suivants :

1. Kit de développement Java (JDK) installé sur votre système.
2.  Aspose.Note pour la bibliothèque Java. Vous pouvez le télécharger depuis[ici](https://releases.aspose.com/note/java/).

## Importer des packages

Commençons par importer les packages nécessaires :

```java
import java.io.IOException;
import com.aspose.note.AlwaysSplitObjectsAlgorithm;
import com.aspose.note.Document;
import com.aspose.note.KeepPartAndCloneSolidObjectToNextPageAlgorithm;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.PdfSaveOptions;
```

## Étape 1 : Charger le document

Chargez le document dans Aspose.Note à l'aide de l'extrait de code suivant :

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Aspose.one");
```

## Étape 2 : Configurer les options d'enregistrement PDF

Définissez PdfSaveOptions et définissez PageSplittingAlgorithm sur KeepSolidObjectsAlgorithm :

```java
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
pdfSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm());
```

## Étape 3 : Ajuster la limite de hauteur (facultatif)

Vous pouvez ajuster la limite de hauteur des pièces clonées si nécessaire :

```java
float heightLimitOfClonedPart = 500;
pdfSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm(heightLimitOfClonedPart));
```

## Étape 4 : Enregistrez le document

Enfin, enregistrez le document avec les options d'enregistrement PDF spécifiées :

```java
String outputDir = "Your Output Directory";
String outputFile = outputDir + "UsingKeepSolidObjectsAlgorithm_out.pdf";
doc.save(outputFile);
```

## Conclusion

Dans ce didacticiel, nous avons appris à utiliser l'algorithme Keep Solid Objects dans Aspose.Note pour Java. Cet algorithme garantit que les objets solides de vos documents sont préservés lors de leur conversion au format PDF, préservant ainsi l'intégrité du document.

## FAQ

### Q1 : Puis-je ajuster la limite de hauteur pour les pièces clonées ?

 A1 : Oui, vous pouvez ajuster la limite de hauteur des pièces clonées en fonction de vos besoins à l'aide du`heightLimitOfClonedPart` paramètre.

### Q2 : Où puis-je trouver plus de documentation ?

 A2 : Vous pouvez trouver une documentation détaillée sur Aspose.Note pour Java[ici](https://reference.aspose.com/note/java/).

### Q3 : Existe-t-il un essai gratuit disponible ?

 A3 : Oui, vous pouvez bénéficier d'un essai gratuit d'Aspose.Note pour Java[ici](https://releases.aspose.com/).

### Q4 : Comment puis-je obtenir de l'aide si je rencontre des problèmes ?

 A4 : Vous pouvez obtenir le soutien de la communauté Aspose[ici](https://forum.aspose.com/c/note/28).

### Q5 : Où puis-je acheter une licence ?

 A5 : Vous pouvez acheter une licence pour Aspose.Note pour Java[ici](https://purchase.aspose.com/buy).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
