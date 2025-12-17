---
date: 2025-12-17
description: Apprenez à enregistrer des documents OneNote au format TIFF en utilisant
  la compression TIFF JPEG, PackBits ou le fax CCITT Group 3 en Java. Contrôlez la
  qualité de l’image, la taille du fichier et le mode couleur avec Aspose.Note.
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

Dans ce tutoriel, vous découvrirez **comment enregistrer un document OneNote au format TIFF en utilisant la compression TIFF JPEG** ainsi que deux autres méthodes de compression populaires. Nous parcourrons la configuration requise, importerons les packages Java nécessaires, et fournirons du code clair étape par étape pour chaque option de compression. À la fin, vous pourrez contrôler **la qualité d'image TIFF**, réduire la taille du fichier, et même produire des TIFF noir et blanc pour une sortie de type fax.

## Quick Answers
- **Qu'est-ce que la compression TIFF JPEG ?** Une méthode de compression avec perte qui réduit la taille du fichier TIFF tout en préservant la qualité visuelle.  
- **Quelle bibliothèque gère la conversion ?** Aspose.Note for Java.  
- **Ai-je besoin d'une licence ?** Un essai gratuit suffit pour les tests ; une licence est requise pour la production.  
- **Puis-je modifier la qualité de l'image ?** Oui, définissez la propriété `quality` sur `ImageSaveOptions`.  
- **La conversion par lots est‑elle possible ?** Absolument – parcourez les documents et appliquez les mêmes options.

## Qu'est-ce que la compression TIFF JPEG ?
La compression TIFF JPEG stocke les données d'image dans le conteneur TIFF mais applique l'algorithme JPEG avec perte pour réduire le fichier. Elle est idéale lorsque vous avez besoin d'un équilibre entre **la qualité d'image TIFF** et une taille de fichier plus petite, notamment pour les scénarios web ou d'archivage.

## Pourquoi utiliser différents types de compression TIFF ?
- **JPEG** – Bon pour les photographies ; offre une qualité réglable.  
- **PackBits** – Encodage simple sans perte de type run‑length ; utile pour les graphiques avec de grandes zones uniformes.  
- **CCITT Group 3 Fax** – Noir et blanc uniquement ; parfait pour les documents numérisés et la transmission fax.  

Choisir la bonne compression vous permet de respecter les contraintes de stockage sans sacrifier la fidélité visuelle requise pour votre application.

## Prérequis

- Java Development Kit (JDK) installé.  
- Bibliothèque Aspose.Note for Java ajoutée à votre projet (Maven/Gradle ou JAR manuel).  
- Familiarité de base avec la syntaxe Java.

## Importer les packages

Tout d'abord, importez les classes Aspose.Note nécessaires dans votre fichier Java :

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Étape 1 : Enregistrer en TIFF en utilisant la compression TIFF JPEG

Voici la méthode complète qui charge un fichier OneNote et l'enregistre en TIFF avec compression JPEG. Ajustez la valeur `quality` (0‑100) pour contrôler **la qualité d'image TIFF**.

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

- `ImageSaveOptions` indique à Aspose.Note de générer un fichier TIFF.  
- `setTiffCompression(TiffCompression.Jpeg)` sélectionne la compression JPEG.  
- `setQuality(93)` (optionnel) ajuste finement la qualité de l'image ; des valeurs plus basses produisent des fichiers plus petits.

### Comment enregistrer un TIFF avec compression JPEG en Java
1. Pointez `dataDir` vers le dossier contenant votre fichier `.one`.  
2. Appelez `SaveToTiffUsingJpegCompression()` depuis votre méthode `main` ou service.  
3. Le fichier `.tiff` résultant apparaîtra dans le même répertoire.

## Étape 2 : Enregistrer en TIFF en utilisant la compression PackBits

Si vous avez besoin d'une option sans perte, PackBits est un algorithme simple de type run‑length qui fonctionne bien pour les graphiques aux couleurs unies.

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
- Aucun réglage de qualité n'est nécessaire car PackBits est sans perte.

## Étape 3 : Enregistrer en TIFF en utilisant la compression CCITT Group 3 Fax (TIFF noir et blanc)

Pour les documents de type fax, vous souhaitez souvent un **TIFF noir et blanc**. CCITT Group 3 offre une forte compression pour les images monochromes.

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

## Problèmes courants et astuces

| Problème | Solution |
|----------|----------|
| **Le fichier de sortie est plus grand que prévu** | Essayez de réduire la valeur `quality` du JPEG ou passez à PackBits si la compression sans perte est acceptable. |
| **Les couleurs semblent délavées** | Assurez‑vous de ne pas définir accidentellement `ColorMode.BlackAndWhite` lorsque vous avez besoin de couleur complète. |
| **Erreur de format d'image non pris en charge** | Vérifiez que vous utilisez une version récente d'Aspose.Note ; les anciennes versions peuvent ne pas contenir certains énumérateurs de compression. |
| **LicenseException à l'exécution** | Installez une licence Aspose.Note valide (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`). |

## Questions fréquentes

**Q : Puis‑je convertir d'autres types de documents (par ex., PDF, DOCX) en TIFF avec ces options ?**  
**R :** Oui. Aspose.Note se concentre sur les fichiers OneNote, mais les autres bibliothèques d'Aspose (PDF, Words) offrent des `ImageSaveOptions` similaires pour leurs formats respectifs.

**Q : En quoi la compression TIFF JPEG diffère‑t‑elle des fichiers JPEG standard ?**  
**R :** Les données d'image sont stockées à l'intérieur d'un conteneur TIFF, préservant les métadonnées et permettant plusieurs pages, tandis que l'algorithme de compression reste JPEG.

**Q : Est‑il possible de traiter en lot de nombreux fichiers `.one` ?**  
**R :** Absolument. Parcourez un dossier, appelez l'une des trois méthodes pour chaque fichier, et récupérez les TIFF résultants.

**Q : Puis‑je contrôler le DPI/la résolution du TIFF de sortie ?**  
**R :** Oui. Utilisez `options.setResolution(int dpi)` avant l'enregistrement.

**Q : Aspose.Note prend‑il en charge le traitement asynchrone ?**  
**R :** L'API elle‑même est synchrone, mais vous pouvez encapsuler les appels dans `CompletableFuture` de Java ou des pools de threads pour une exécution parallèle.

## Conclusion

Vous disposez maintenant d'une boîte à outils complète de **conversion TIFF Java** qui vous permet d'enregistrer des documents OneNote au format TIFF en utilisant la compression JPEG, PackBits ou CCITT Group 3 Fax. Ajustez la qualité, le mode couleur et la résolution pour répondre à vos exigences spécifiques en matière de **qualité d'image TIFF**, et intégrez ces méthodes dans des flux de travail par lots pour une productivité maximale.

---

**Dernière mise à jour :** 2025-12-17  
**Testé avec :** Aspose.Note for Java 23.12 (dernière version au moment de la rédaction)  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}