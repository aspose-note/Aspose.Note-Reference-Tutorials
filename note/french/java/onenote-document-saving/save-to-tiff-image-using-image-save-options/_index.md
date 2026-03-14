---
date: 2026-03-14
description: Apprenez à enregistrer des documents OneNote au format TIFF en utilisant
  la compression TIFF JPEG, la compression TIFF PackBits ou le fax CCITT Group 3 en
  Java. Contrôlez la qualité de l'image, la taille du fichier et le mode couleur avec
  Aspose.Note.
linktitle: Save to TIFF Image Using TIFF JPEG Compression in OneNote
second_title: Aspose.Note Java API
title: Enregistrer au format TIFF avec compression JPEG dans OneNote
url: /fr/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Enregistrer une image TIFF en utilisant la compression TIFF JPEG dans OneNote

## Introduction

Dans ce tutoriel, vous découvrirez **comment enregistrer un document OneNote au format TIFF en utilisant la compression TIFF JPEG** ainsi que deux autres méthodes de compression populaires. Nous parcourrons la configuration requise, importerons les packages Java nécessaires, et fournirons un code clair étape par étape pour chaque option de compression. À la fin, vous pourrez contrôler **la qualité d'image TIFF**, réduire la taille du fichier, et même produire des TIFF noir et blanc pour des sorties de type fax.

## Réponses rapides
- **Qu’est‑ce que la compression TIFF JPEG ?** Une méthode de compression avec perte qui réduit la taille du fichier TIFF tout en préservant la qualité visuelle.  
- **Quelle bibliothèque gère la conversion ?** Aspose.Note for Java.  
- **Ai‑je besoin d’une licence ?** Un essai gratuit suffit pour les tests ; une licence est requise en production.  
- **Puis‑je modifier la qualité de l’image ?** Oui, définissez la propriété `quality` sur `ImageSaveOptions`.  
- **La conversion par lots est‑elle possible ?** Absolument – parcourez les documents et appliquez les mêmes options.

## Qu’est‑ce que la compression TIFF JPEG ?
La compression TIFF JPEG stocke les données d’image dans un conteneur TIFF mais applique l’algorithme JPEG avec perte pour réduire le fichier. Elle est idéale lorsque vous avez besoin d’un compromis entre **la qualité d’image TIFF** et une taille de fichier plus petite, notamment pour le web ou l’archivage.

## Pourquoi utiliser différents types de compression TIFF ?
- **JPEG** – Idéal pour les photographies ; offre une qualité réglable.  
- **PackBits** – Encodage run‑length simple et sans perte ; utile pour les graphiques avec de grandes zones uniformes.  
- **CCITT Group 3 Fax** – Noir et blanc uniquement ; parfait pour les documents numérisés et la transmission fax.  

Choisir la bonne compression vous permet de respecter les contraintes de stockage sans sacrifier la fidélité visuelle requise pour votre application.

## Convertir OneNote en TIFF avec Aspose.Note
Si votre objectif est de **convertir OneNote en TIFF**, les trois méthodes ci‑dessous couvrent les scénarios les plus courants. Chaque méthode charge un fichier `.one`, configure `ImageSaveOptions`, et enregistre le résultat sous forme de fichier `.tiff`.

## Prérequis

- JDK (Java Development Kit) installé.  
- Bibliothèque Aspose.Note for Java ajoutée à votre projet (Maven/Gradle ou JAR manuel).  
- Familiarité de base avec la syntaxe Java.

## Importer les packages

Tout d’abord, importez les classes Aspose.Note nécessaires dans votre fichier Java :

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Étape 1 : Enregistrer en TIFF avec compression TIFF JPEG

Voici la méthode complète qui charge un fichier OneNote et l’enregistre en TIFF avec compression JPEG. Ajustez la valeur `quality` (0‑100) pour contrôler **la qualité d’image TIFF**.

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
- `setQuality(93)` (optionnel) ajuste la qualité de l’image ; des valeurs plus basses produisent des fichiers plus petits.

### Comment enregistrer un TIFF avec compression JPEG en Java
1. Pointez `dataDir` vers le dossier contenant votre fichier `.one`.  
2. Appelez `SaveToTiffUsingJpegCompression()` depuis votre méthode `main` ou votre service.  
3. Le fichier `.tiff` résultant apparaîtra dans le même répertoire.

## Vue d’ensemble de la compression TIFF PackBits

PackBits est un algorithme de compression sans perte qui fonctionne le mieux pour les images contenant de grandes zones de couleur unie. Il est souvent désigné comme **compression tiff packbits** dans la documentation.

## Étape 2 : Enregistrer en TIFF avec compression PackBits

Si vous avez besoin d’une option sans perte, PackBits est un algorithme simple de run‑length qui convient aux graphiques aux couleurs unies.

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

- `setTiffCompression(TiffCompression.PackBits)` change la méthode de compression.  
- Aucun réglage de qualité n’est nécessaire car PackBits est sans perte.

## Étape 3 : Enregistrer en TIFF avec compression CCITT Group 3 Fax (TIFF noir et blanc)

Pour les documents de type fax, vous souhaitez souvent un **TIFF noir et blanc**. CCITT Group 3 offre une compression élevée pour les images monochromes.

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

## Problèmes courants & Astuces

| Problème | Solution |
|----------|----------|
| **Le fichier de sortie est plus volumineux que prévu** | Essayez de réduire la valeur `quality` du JPEG ou passez à PackBits si la perte n’est pas un problème. |
| **Les couleurs semblent délavées** | Assurez‑vous de ne pas avoir défini accidentellement `ColorMode.BlackAndWhite` lorsque vous avez besoin de couleur complète. |
| **Erreur « format d’image non pris en charge »** | Vérifiez que vous utilisez une version récente d’Aspose.Note ; les anciennes versions peuvent ne pas contenir certains enums de compression. |
| **LicenseException à l’exécution** | Installez une licence Aspose.Note valide (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`). |

## Questions fréquentes

**Q : Puis‑je convertir d’autres types de documents (par ex. PDF, DOCX) en TIFF avec ces options ?**  
R : Oui. Bien qu’Aspose.Note se concentre sur les fichiers OneNote, Aspose.PDF, Aspose.Words et d’autres bibliothèques offrent des `ImageSaveOptions` similaires pour leurs formats.

**Q : En quoi la compression TIFF JPEG diffère‑t‑elle d’un fichier JPEG standard ?**  
R : L’algorithme JPEG est le même, mais les données d’image sont encapsulées dans un conteneur TIFF, qui peut contenir plusieurs pages et des métadonnées plus riches.

**Q : Est‑il possible de traiter en lot de nombreux fichiers `.one` ?**  
R : Absolument. Parcourez un répertoire, appelez l’une des trois méthodes pour chaque fichier, et récupérez les TIFF générés.

**Q : Puis‑je contrôler le DPI/la résolution du TIFF de sortie ?**  
R : Oui. Utilisez `options.setResolution(int dpi)` avant l’enregistrement.

**Q : Aspose.Note supporte‑t‑il le traitement asynchrone ?**  
R : L’API elle‑même est synchrone, mais vous pouvez encapsuler les appels dans un `CompletableFuture` ou un pool de threads Java pour une exécution parallèle.

## Conclusion

Vous disposez maintenant d’une boîte à outils complète **java tiff conversion** qui vous permet d’enregistrer des documents OneNote au format TIFF en utilisant la compression JPEG, PackBits ou CCITT Group 3 Fax. Ajustez la qualité, le mode couleur et la résolution pour répondre à vos exigences spécifiques de **qualité d’image TIFF**, et intégrez ces méthodes dans des flux de travail par lots pour une productivité maximale.

---

**Dernière mise à jour :** 2026-03-14  
**Testé avec :** Aspose.Note for Java 23.12 (dernière version au moment de la rédaction)  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}