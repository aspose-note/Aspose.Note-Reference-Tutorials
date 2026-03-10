---
date: 2025-12-18
description: Apprenez comment **enregistrer OneNote au format PDF** en utilisant le
  sous‑système de polices spécifié en Java avec Aspose.Note. Ce guide montre également
  comment convertir OneNote en PDF, charger des fichiers de polices personnalisés
  et spécifier les polices par défaut.
linktitle: Save OneNote as PDF Using Specified Fonts Subsystem
second_title: Aspose.Note Java API
title: Enregistrer OneNote au format PDF à l'aide du sous‑système de polices spécifiées
url: /fr/java/onenote-document-saving/save-using-specified-fonts-subsystem/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Enregistrer OneNote en PDF en utilisant le sous‑système de polices spécifié

## Introduction

Dans de nombreux scénarios professionnels, vous devez **enregistrer OneNote en PDF** tout en conservant l’aspect exact des pages d’origine. Aspose.Note pour Java rend cela simple en vous permettant de contrôler le sous‑système de polices pendant la conversion. Dans ce tutoriel, nous passerons en revue trois méthodes pratiques pour **convertir OneNote en PDF**, en expliquant comment **charger des fichiers de polices personnalisées**, **spécifier une police par défaut**, et même **utiliser un flux de police** lorsque la police n’est pas disponible sur la machine cible.

## Réponses rapides
- **Que signifie « enregistrer OneNote en PDF » ?** Cela convertit un fichier .one en PDF tout en conservant la mise en page et le style intacts.  
- **Quelle API gère les polices ?** `DocumentFontsSubsystem` vous permet de définir une police par défaut ou de charger un fichier/flux de police personnalisé.  
- **Ai‑je besoin d’une licence pour la production ?** Oui, une licence commerciale Aspose.Note est requise pour une utilisation non‑d’évaluation.  
- **Puis‑je convertir plusieurs fichiers en lot ?** Absolument – il suffit de boucler sur la logique de chargement et d’enregistrement du `Document`.  
- **Quelle version de Java est requise ?** Java 15 ou supérieure (l’exemple utilise JDK 15).

## Qu’est‑ce que « enregistrer OneNote en PDF » avec un sous‑système de polices ?

Enregistrer OneNote en PDF avec un sous‑système de polices signifie que, pendant le processus de conversion, Aspose.Note remplace les glyphes manquants par la police que vous fournissez. Cela garantit que le PDF a exactement le même aspect sur n’importe quel appareil, même si la police d’origine n’est pas installée.

## Pourquoi contrôler le sous‑système de polices lors de la **conversion de OneNote en PDF** ?

- **Cohérence de la marque** – les documents d’entreprise conservent exactement la même typographie.  
- **Fiabilité multiplateforme** – les PDF s’affichent de la même façon sous Windows, macOS, Linux et sur mobile.  
- **Réduction des erreurs** – les avertissements de police manquante disparaissent, produisant une sortie propre.

## Prérequis

### 1. Kit de développement Java (JDK)

Assurez‑vous d’avoir le Kit de développement Java (JDK) installé sur votre système. Vous pouvez le télécharger [ici](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html) si ce n’est pas déjà fait.

### 2. Bibliothèque Aspose.Note pour Java

Téléchargez et configurez la bibliothèque Aspose.Note pour Java. Vous pouvez la télécharger depuis le [site web](https://releases.aspose.com/note/java/).

## Importer les packages

Assurez‑vous d’importer les packages nécessaires dans votre projet Java :

```java
import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
import com.aspose.note.fonts.DocumentFontsSubsystem;
import java.io.FileInputStream;
import java.io.IOException;
import java.io.InputStream;
import java.nio.file.Paths;
```

Décomposons maintenant chaque exemple en plusieurs étapes pour mieux comprendre le processus.

## Comment **enregistrer OneNote en PDF** en utilisant le sous‑système de polices du document avec une police par défaut

### Étape 1 : Enregistrer en utilisant le sous‑système de polices du document avec le nom de police par défaut

Cette étape montre comment **enregistrer OneNote en PDF** de manière simple en spécifiant un nom de police par défaut.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName() throws IOException
{
    // Load the document into Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Specify the default font.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFont("Times New Roman"));

    // Save the document as PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf", options);
}
```

Dans cette étape :
- Le document OneNote est chargé à l’aide d’Aspose.Note.  
- La **police par défaut** est définie sur **« Times New Roman »**.  
- Le document est enregistré au format PDF avec la police choisie.

### Étape 2 : Enregistrer en utilisant le sous‑système de polices du document avec une police par défaut depuis un fichier

Ici, nous **chargeons un fichier de police personnalisé** et l’utilisons comme police de secours lors de la conversion en PDF.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile() throws IOException
{
    // Load the document into Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Specify the path to the font file.
    String fontFile = "geo_1.ttf";

    // Specify the default font from the file.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromFile(fontFile));

    // Save the document as PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf", options);
}
```

Points clés :
- Le **fichier de police personnalisé** `geo_1.ttf` est **chargé depuis le disque**.  
- `usingDefaultFontFromFile` **spécifie la police par défaut depuis un fichier**, garantissant que le PDF utilise cette police lorsque l’originale est absente.  
- Le PDF résultant conserve l’aspect prévu.

### Étape 3 : Enregistrer en utilisant le sous‑système de polices du document avec une police par défaut depuis un flux

Parfois, la police peut être stockée dans une base de données ou reçue via le réseau. Cet exemple montre comment **utiliser un flux de police**.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream() throws IOException
{
    // Load the document into Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Specify the path to the font file.
    String fontFile = "geo_1.ttf";

    // Load the font file as a stream.
    InputStream stream = new FileInputStream(fontFile);

    try
    {
        // Specify the default font from the stream.
        PdfSaveOptions options = new PdfSaveOptions();
        options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromStream(stream));

        // Save the document as PDF.
        oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf", options);
    }
    catch (Exception e)
    {
        stream.close();
    }
}
```

Ce qui se passe ici :
- Le fichier de police est ouvert en tant qu’**InputStream**, ce qui est utile lorsque la police provient d’une source qui n’est pas un fichier.  
- `usingDefaultFontFromStream` **utilise un flux de police** pour définir la police de secours.  
- Le fichier OneNote est enregistré en PDF avec la police fournie via le flux.

## Problèmes courants et solutions

| Problème | Pourquoi cela se produit | Comment résoudre |
|----------|--------------------------|------------------|
| **Avertissements de police manquante** | Le fichier .one source fait référence à une police qui n’est pas présente sur la machine. | Fournir une police par défaut via `usingDefaultFont`, `usingDefaultFontFromFile` ou `usingDefaultFontFromStream`. |
| **Fichier de police personnalisé introuvable** | Chemin incorrect vers le fichier `.ttf`. | Utiliser des chemins absolus ou vérifier le chemin relatif par rapport au répertoire de travail. |
| **Flux non fermé** | Une exception se produit avant l’appel à `close()`. | Utiliser le try‑with‑resources (`try (InputStream stream = ...) { ... }`) pour une fermeture automatique. |

## Questions fréquemment posées

**Q : Puis‑je spécifier des polices différentes pour différentes parties du document ?**  
R : Oui, vous pouvez appliquer des paramètres de police personnalisés aux éléments de texte enrichi individuels en utilisant la classe `Font` d’Aspose.Note.

**Q : Aspose.Note est‑il compatible avec toutes les versions de OneNote ?**  
R : Aspose.Note prend en charge les fichiers OneNote des versions récentes de bureau et mobiles, assurant une large compatibilité.

**Q : Comment gérer les polices manquantes lors de l’enregistrement des documents ?**  
R : Utilisez les méthodes du sous‑système de polices présentées ci‑dessus (`usingDefaultFont`, `usingDefaultFontFromFile`, `usingDefaultFontFromStream`) pour fournir une police de secours.

**Q : Puis‑je personnaliser les propriétés de la police comme la taille et le style ?**  
R : Absolument – l’API permet de définir la taille, le style, la couleur et d’autres attributs au niveau de chaque run.

**Q : Existe‑t‑il une version d’essai disponible pour Aspose.Note pour Java ?**  
R : Oui, une version d’essai gratuite peut être téléchargée depuis le site web d’Aspose.

## Conclusion

Dans ce tutoriel, nous avons appris comment **enregistrer OneNote en PDF** tout en contrôlant le sous‑système de polices en Java avec Aspose.Note. En suivant les trois approches — spécifier un nom de police par défaut, charger un fichier de police personnalisé, ou utiliser un flux de police — vous pouvez garantir une représentation cohérente des polices sur toutes les plateformes lors de l’exportation ou de l’enregistrement de vos documents OneNote.

---

**Dernière mise à jour :** 2025-12-18  
**Testé avec :** Aspose.Note pour Java 24.11  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}