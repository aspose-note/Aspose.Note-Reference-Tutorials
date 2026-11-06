---
date: 2026-11-05
description: Apprenez comment réduire la taille d'un fichier TIFF lors de la conversion
  de carnets OneNote en TIFF en Java avec Aspose.Note. Inclut les options JPEG, PackBits
  et TIFF noir‑et‑blanc.
keywords:
- reduce tiff file size
- black white tiff
- tiff jpeg compression
- aspose note java
lastmod: 2026-11-05
linktitle: Comment réduire la taille d'un fichier TIFF lors de la conversion de OneNote
  en Java
og_description: Apprenez comment réduire la taille d'un fichier TIFF lors de la conversion
  de carnets OneNote en TIFF en Java avec Aspose.Note. Inclut les options JPEG, PackBits
  et TIFF noir‑et‑blanc.
og_image_alt: Developer guide showing OneNote to TIFF conversion with compression
  options in Java
og_title: Comment réduire la taille d'un fichier TIFF lors de la conversion de OneNote
  en Java
schemas:
- author: Aspose
  dateModified: '2026-11-05'
  description: Learn how to reduce TIFF file size when converting OneNote notebooks
    to TIFF in Java using Aspose.Note. Includes JPEG, PackBits and black‑white TIFF
    options.
  headline: How to reduce TIFF file size when converting OneNote in Java
  type: TechArticle
- description: Learn how to reduce TIFF file size when converting OneNote notebooks
    to TIFF in Java using Aspose.Note. Includes JPEG, PackBits and black‑white TIFF
    options.
  name: How to reduce TIFF file size when converting OneNote in Java
  steps:
  - name: Point `dataDir` to the folder containing your `.one` file.
    text: Point `dataDir` to the folder containing your `.one` file.
  - name: Call `SaveToTiffUsingJpegCompression()` from your main method or service.
    text: Call `SaveToTiffUsingJpegCompression()` from your main method or service.
  - name: The resulting `.tiff` file will appear in the same directory.
    text: The resulting `.tiff` file will appear in the same directory.
  type: HowTo
- questions:
  - answer: Yes. While Aspose.Note focuses on OneNote files, Aspose.PDF, Aspose.Words,
      and other libraries provide similar `ImageSaveOptions` for their formats.
    question: Can I convert other document types (e.g., PDF, DOCX) to TIFF with these
      options?
  - answer: The JPEG algorithm is the same, but the image data lives inside a TIFF
      container, which can hold multiple pages and richer metadata.
    question: How does TIFF JPEG compression differ from a standard JPEG file?
  - answer: Absolutely. Iterate over a directory, call any of the three methods for
      each file, and collect the resulting TIFFs.
    question: Is it possible to batch‑process many `.one` files?
  - answer: Yes. Use `options.setResolution(int dpi)` before saving.
    question: Can I control the DPI/resolution of the output TIFF?
  - answer: The API itself is synchronous, but you can wrap calls in Java’s `CompletableFuture`
      or a thread pool for parallel execution.
    question: Does Aspose.Note support asynchronous processing?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- reduce tiff file size
- aspose.note
- java tiff conversion
- black white tiff
- image compression
title: Comment réduire la taille d'un fichier TIFF lors de la conversion de OneNote
  en Java
url: /fr/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment réduire la taille d'un fichier TIFF lors de la conversion de OneNote en Java

## Introduction

Dans ce tutoriel, vous découvrirez comment **réduire la taille d'un fichier TIFF** lors de la conversion de carnets OneNote en images TIFF à l'aide d'Aspose.Note pour Java. Nous passerons en revue trois méthodes de compression — TIFF JPEG, PackBits et CCITT Group 3 (TIFF noir et blanc) — et vous montrerons comment ajuster la qualité de l'image, contrôler le mode couleur et maintenir des tailles de fichier optimales pour le web, l'archivage ou les scénarios de type fax.

## Réponses rapides
- **Qu'est-ce que la compression TIFF JPEG ?** Une méthode de compression avec perte qui réduit la taille du fichier TIFF tout en préservant la qualité visuelle.  
- **Quelle bibliothèque gère la conversion ?** Aspose.Note pour Java.  
- **Ai-je besoin d'une licence ?** Un essai gratuit fonctionne pour les tests ; une licence est requise pour la production.  
- **Puis-je modifier la qualité de l'image ?** Oui, définissez la propriété `quality` sur `ImageSaveOptions`.  
- **La conversion par lots est‑elle possible ?** Absolument – parcourez les documents et appliquez les mêmes options.

## Vue d'ensemble de la compression TIFF JPEG

La compression TIFF JPEG stocke les données d'image dans un conteneur TIFF mais applique l'algorithme JPEG avec perte pour réduire le fichier. Elle est idéale lorsque vous avez besoin d'un équilibre entre **la qualité d'image TIFF** et une taille de fichier plus petite, notamment pour les scénarios web ou d'archivage.

## Pourquoi utiliser différents types de compression TIFF ?

Vous choisissez le type de compression en fonction du contenu et des besoins de stockage : JPEG convient le mieux aux photographies, PackBits offre une compression sans perte pour les graphiques avec de grandes zones uniformes, et CCITT Group 3 fournit une compression à haut ratio pour les documents monochromes de type fax. Sélectionner la bonne méthode vous permet de **réduire la taille d'un fichier TIFF** sans compromettre la fidélité visuelle requise par votre application.

## Choisir la bonne compression

- **JPEG** – Qualité réglable (0‑100) vous permet d'échanger taille contre détail, parfait pour les pages riches en couleur.  
- **PackBits** – Codage run‑length sans perte ; idéal lorsque vous devez conserver chaque pixel exactement.  
- **CCITT Group 3** – Monochrome uniquement ; maximise la compression pour les textes numérisés ou les documents fax.  

## Convertir OneNote en TIFF avec Aspose.Note

Si votre objectif est de **convertir OneNote en TIFF**, les trois méthodes ci‑dessus couvrent les scénarios les plus courants. Chaque méthode charge un fichier `.one`, configure `ImageSaveOptions` et enregistre le résultat sous forme de fichier `.tiff`.

## Prérequis

- Kit de développement Java (JDK) installé.  
- Bibliothèque Aspose.Note pour Java ajoutée à votre projet (Maven/Gradle ou JAR manuel).  
- Familiarité de base avec la syntaxe Java.

## Importer les packages

Les classes `ImageSaveOptions`, `TiffCompression` et `ColorMode` sont le cœur de l'API de conversion.  

`ImageSaveOptions` définit les options pour enregistrer les images, comme le format et la compression.  
`TiffCompression` énumère les algorithmes de compression TIFF pris en charge.  
`ColorMode` spécifie la profondeur de couleur, par ex. couleur ou noir et blanc.  

```java
// Placeholder for import statements – keep your imports here
```

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Étape 1 : enregistrer en TIFF avec compression TIFF JPEG

### Enregistrement d'un TIFF avec compression JPEG en Java

Chargez le fichier OneNote, configurez `ImageSaveOptions` avec la compression JPEG, définissez éventuellement la valeur `quality`, puis appelez la méthode d'enregistrement. Ce schéma en deux étapes vous donne un contrôle complet sur la taille de sortie et la fidélité visuelle.

1. Pointez `dataDir` vers le dossier contenant votre fichier `.one`.  
2. Appelez `SaveToTiffUsingJpegCompression()` depuis votre méthode principale ou service.  
3. Le fichier `.tiff` résultant apparaîtra dans le même répertoire.

```java
// Placeholder for the JPEG compression method implementation
```

```java
public static void SaveToTiffUsingJpegCompression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.Jpeg);
    options.setQuality(93);

    oneFile.save(Paths.get(dataDir,"SaveToTiffUsingJpegCompression.tiff").toString(), options);
}
```

**Explication**

- `ImageSaveOptions` indique à Aspose.Note de produire un fichier TIFF.  
- `setTiffCompression(TiffCompression.Jpeg)` sélectionne la compression JPEG.  
- `setQuality(93)` (optionnel) ajuste finement la qualité de l'image ; des valeurs plus faibles produisent des fichiers plus petits.

## Vue d'ensemble de la compression PackBits TIFF

PackBits est un algorithme de compression sans perte qui fonctionne le mieux pour les images avec de grandes zones de couleur unie. On l'appelle souvent **compression tiff packbits** dans la documentation.

## Enregistrement d'un TIFF avec compression PackBits en Java

Si vous avez besoin d'une option sans perte, PackBits est un algorithme simple de codage run‑length qui fonctionne bien pour les graphiques aux couleurs unies. Configurez `ImageSaveOptions` avec `TiffCompression.PackBits` et enregistrez le document.

```java
// Placeholder for the PackBits compression method implementation
```

```java
public static void SaveToTiffUsingPackBitsCompression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.PackBits);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingPackBitsCompression.tiff").toString(), options);
}
```

**Explication**

- `setTiffCompression(TiffCompression.PackBits)` change le mode de compression.  
- Aucun réglage de qualité n'est nécessaire car PackBits est sans perte.

## Enregistrement d'un TIFF avec compression CCITT Group 3 en Java

Pour les documents de type fax, vous souhaitez souvent un **TIFF noir et blanc**. CCITT Group 3 offre une compression élevée pour les images monochromes. Réglez le mode couleur sur noir et blanc et choisissez l'énumération de compression CCITT 3.

```java
// Placeholder for the CCITT Group 3 compression method implementation
```

```java
public static void SaveToTiffUsingCcitt3Compression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setColorMode(ColorMode.BlackAndWhite);
    options.setTiffCompression(TiffCompression.Ccitt3);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingCcitt3Compression.tiff").toString(), options);
}
```

**Explication**

- `setColorMode(ColorMode.BlackAndWhite)` force une sortie monochrome.  
- `setTiffCompression(TiffCompression.Ccitt3)` applique la compression orientée fax.

## Problèmes courants & astuces

| Problème | Solution |
|----------|----------|
| **Le fichier de sortie est plus grand que prévu** | Essayez de réduire la valeur `quality` du JPEG ou passez à PackBits si la compression sans perte est acceptable. |
| **Les couleurs semblent délavées** | Assurez‑vous de ne pas avoir défini accidentellement `ColorMode.BlackAndWhite` lorsque vous avez besoin de couleur complète. |
| **Erreur de format d'image non pris en charge** | Vérifiez que vous utilisez une version récente d'Aspose.Note ; les versions plus anciennes peuvent ne pas contenir certaines énumérations de compression. |
| **LicenseException à l'exécution** | Installez une licence Aspose.Note valide (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`). |

## Questions fréquemment posées

**Q : Puis‑je convertir d'autres types de documents (par ex., PDF, DOCX) en TIFF avec ces options ?**  
R : Oui. Bien qu'Aspose.Note se concentre sur les fichiers OneNote, Aspose.PDF, Aspose.Words et d'autres bibliothèques offrent des `ImageSaveOptions` similaires pour leurs formats.

**Q : En quoi la compression TIFF JPEG diffère‑t‑elle d'un fichier JPEG standard ?**  
R : L'algorithme JPEG est le même, mais les données d'image sont contenues dans un conteneur TIFF, qui peut contenir plusieurs pages et des métadonnées plus riches.

**Q : Est‑il possible de traiter par lots de nombreux fichiers `.one` ?**  
R : Absolument. Parcourez un répertoire, appelez l'une des trois méthodes pour chaque fichier et collectez les TIFF résultants.

**Q : Puis‑je contrôler le DPI/la résolution du TIFF de sortie ?**  
R : Oui. Utilisez `options.setResolution(int dpi)` avant d'enregistrer.

**Q : Aspose.Note prend‑il en charge le traitement asynchrone ?**  
R : L'API elle‑même est synchrone, mais vous pouvez encapsuler les appels dans un `CompletableFuture` Java ou un pool de threads pour une exécution parallèle.

## Conclusion

Vous disposez maintenant d'une boîte à outils complète de **conversion TIFF en Java** qui vous permet de **réduire la taille d'un fichier TIFF** lors de l'enregistrement de documents OneNote au format TIFF en utilisant la compression JPEG, PackBits ou CCITT Group 3 Fax. Ajustez la qualité, le mode couleur et la résolution pour répondre à vos exigences spécifiques, et intégrez ces méthodes dans des flux de travail par lots pour une productivité maximale.

---

**Dernière mise à jour :** 2026-11-05  
**Testé avec :** Aspose.Note for Java 26.4 (latest at time of writing)  
**Auteur :** Aspose

## Tutoriels associés

- [Comment rendre l'image d'une page OneNote (JPEG) en utilisant le format d'enregistrement avec Aspose.Note pour Java](/note/java/onenote-document-saving/save-to-jpeg-image-using-save-format/)
- [Utiliser Aspose.Note pour Java afin d'enregistrer OneNote en PNG avec options – Convertir le carnet en image](/note/java/onenote-notebook-operations/convert-notebook-to-image-with-options/)
- [Comment exporter OneNote en image en niveaux de gris – Aspose.Note](/note/java/onenote-document-saving/save-to-grayscale-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}