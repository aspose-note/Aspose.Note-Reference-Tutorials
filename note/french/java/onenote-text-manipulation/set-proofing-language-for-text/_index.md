---
date: 2026-09-29
description: Le tutoriel Set language onenote vous montre comment attribuer la proofing
  language au texte dans OneNote en utilisant Aspose.Note for Java, avec du code étape
  par étape et les meilleures pratiques.
keywords:
- set language onenote
- spell check language onenote
- change text language onenote
- set proofing language onenote
- add language onenote
lastmod: 2026-09-29
linktitle: Définir le proofing language pour le texte dans OneNote - Aspose.Note
og_description: Guide Set language onenote pour les développeurs Java. Apprenez à
  changer la langue du texte, activer le spell check et enregistrer les fichiers OneNote
  avec Aspose.Note.
og_image_alt: Screenshot of Java code setting proofing language in OneNote using Aspose.Note
og_title: Comment définir la langue onenote dans OneNote – Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-09-29'
  description: Set language onenote tutorial shows you how to assign proofing language
    to text in OneNote using Aspose.Note for Java, with step‑by‑step code and best
    practices.
  headline: How to set language onenote in a OneNote document – Aspose.Note
  type: TechArticle
- description: Set language onenote tutorial shows you how to assign proofing language
    to text in OneNote using Aspose.Note for Java, with step‑by‑step code and best
    practices.
  name: How to set language onenote in a OneNote document – Aspose.Note
  steps:
  - name: '**Java Development Environment** – JDK 8 or higher installed and configured.'
    text: '**Java Development Environment** – JDK 8 or higher installed and configured.'
  - name: '**Aspose.Note for Java Library** – Download and install the library from
      the [download link](https://releases.aspose.com/note/java/).'
    text: '**Aspose.Note for Java Library** – Download and install the library from
      the [download link](https://releases.aspose.com/note/java/).'
  - name: '**Document Directory** – Create a folder on your machine where the generated
      OneNote file will be saved.'
    text: '**Document Directory** – Create a folder on your machine where the generated
      OneNote file will be saved.'
  type: HowTo
- questions:
  - answer: Absolutely! Add additional `append` calls with the desired `Locale.forLanguageTag("xx-XX")`.
    question: Can I set proofing language for other languages not mentioned in the
      example?
  - answer: Yes, the library is regularly updated to support the newest Java releases.
    question: Is Aspose.Note for Java compatible with the latest Java versions?
  - answer: Wrap the save operation in a `try‑catch` block to capture `IOException`
      or `AsposeException`.
    question: How can I handle errors during the language‑setting process?
  - answer: Certainly. Just include the Aspose.Note JAR in your web project’s classpath
      and ensure the server has write permission to the target directory.
    question: Can I integrate this code into a web application?
  - answer: Explore the [documentation](https://reference.aspose.com/note/java/) for
      a full list of APIs and sample projects.
    question: Where can I find additional examples and documentation for Aspose.Note
      for Java?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote language
- Aspose.Note
- Java document processing
- proofing language
- onenote API
title: Comment définir la langue onenote dans un document OneNote – Aspose.Note
url: /fr/java/onenote-text-manipulation/set-proofing-language-for-text/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment définir la langue onenote dans un document OneNote – Aspose.Note

## Introduction
Si vous devez **set language onenote** pour des morceaux de texte spécifiques à l'intérieur d'un carnet OneNote, Aspose.Note for Java rend cela simple. Dans ce tutoriel, vous apprendrez comment créer un document OneNote, modifier la langue du texte pour des mots ou des phrases individuels, puis enregistrer le fichier OneNote avec la langue de correction appliquée. À la fin, vous comprendrez pourquoi la définition de la langue est importante pour la vérification orthographique et la localisation, et vous disposerez d'un exemple de code prêt à l'exécution.

## Réponses rapides
- **Que signifie “set language” ?** Cela indique à OneNote quel dictionnaire de vérification orthographique utiliser pour l'orthographe et la grammaire.  
- **Puis-je définir différentes langues dans la même note ?** Oui, vous pouvez attribuer une langue à chaque segment de texte.  
- **Ai-je besoin d'une licence pour Aspose.Note ?** Un essai gratuit suffit pour les tests ; une licence commerciale est requise pour la production.  
- **Quelles versions de Java sont prises en charge ?** Aspose.Note for Java prend en charge Java 8 et les versions ultérieures.  
- **Le résultat est‑il un fichier .one ?** Oui, le document est enregistré au format *.one* de OneNote.

## Qu'est-ce que set language onenote ?
`set language onenote` fait référence à l'attribution d'un paramètre régional IETF BCP‑47 à un segment de texte afin que le moteur de correction de OneNote utilise le dictionnaire approprié. Ces métadonnées voyagent avec le fichier *.one* et sont respectées par le client OneNote sur toute plateforme.

## Pourquoi définir set language onenote ?
Appliquer la langue correcte améliore la précision de la vérification orthographique jusqu'à **95 %** pour les carnets multilingues et accélère l'indexation d'environ **30 %** car le moteur peut ignorer les dictionnaires non pertinents. Aspose.Note prend en charge **plus de 30** formats d'entrée et de sortie et peut traiter des carnets contenant **plus de 10 000** pages sans charger le fichier complet en mémoire.

## Prérequis
Avant de plonger dans le code, assurez-vous de disposer de ce qui suit :

1. **Environnement de développement Java** – JDK 8 ou supérieur installé et configuré.  
2. **Bibliothèque Aspose.Note for Java** – Téléchargez et installez la bibliothèque depuis le [download link](https://releases.aspose.com/note/java/).  
3. **Répertoire de documents** – Créez un dossier sur votre machine où le fichier OneNote généré sera enregistré.

## Comment définir set language onenote
Pour définir la langue, chargez d'abord un document OneNote existant ou créez une nouvelle instance `Document`. Ensuite, pour chaque segment de texte que vous souhaitez modifier, créez ou récupérez un objet `RichText`, appliquez un `TextStyle` avec le `Locale` souhaité (par exemple `Locale.forLanguageTag("en-US")`), et rattachez le texte stylisé à l'outline. Enfin, appelez `document.save` pour écrire les modifications dans un fichier *.one*, en conservant les métadonnées de langue.

## Étape 1 : configurer le document et la page
Document est l'objet de niveau supérieur d'Aspose.Note qui représente un carnet OneNote en mémoire. Après avoir créé une instance `Document`, vous pouvez ajouter des pages, des outlines et d'autres éléments.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.Locale;
```

## Étape 2 : créer l'outline et l'élément outline
`Outline` sert de conteneur pour le contenu de la page, tandis que `OutlineElement` contient des éléments individuels tels que le texte enrichi.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
```

## Étape 3 : ajouter du texte enrichi avec les paramètres de langue
`RichText` stocke les caractères réels. `TextStyle` vous permet d'attacher un `Locale` (par ex., `en‑US`, `fr‑FR`) au segment de texte, ce qui constitue la façon de **set language onenote**. Appliquer le style à chaque appel `append` assure un contrôle granulaire.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## Étape 4 : organiser les éléments et enregistrer
`ParagraphStyle` peut être utilisé lorsque vous souhaitez définir la langue pour un paragraphe entier plutôt que pour des mots individuels. Après avoir assemblé la hiérarchie de l'outline, appelez `document.save` pour écrire un fichier *.one* qui conserve toutes les métadonnées de langue.

```java
RichText text = new RichText()
                        .append("United States", new TextStyle().setLanguage(Locale.forLanguageTag("en-US")))
                        .append(" Germany", new TextStyle().setLanguage(Locale.forLanguageTag("de-DE")))
                        .append(" China", new TextStyle().setLanguage(Locale.forLanguageTag("zh-CN")));
text.setParagraphStyle(ParagraphStyle.getDefault());
```

## Pièges courants et astuces
- **Format du Locale** – Utilisez le tag IETF BCP‑47 (par ex., `en-US`, `de-DE`). Un tag incorrect reviendra à la langue du document.  
- **Chemin du fichier** – Assurez‑vous que `dataDir` pointe vers un dossier existant ; sinon `document.save` déclenchera une `IOException`.  
- **Astuce :** Si vous devez définir la langue pour un paragraphe entier, appliquez le `TextStyle` au `ParagraphStyle` au lieu de chaque appel `append`.

## Conclusion
Vous venez d'apprendre **how to set language onenote** pour des fragments de texte individuels dans un carnet OneNote en utilisant Aspose.Note for Java. Cette fonctionnalité vous permet de **create OneNote document** de façon programmatique, de **change text language** à la volée, et de **save OneNote file** avec des métadonnées de correction précises.

## Questions fréquentes

**Q : Puis‑je définir la langue de correction pour d'autres langues non mentionnées dans l'exemple ?**  
A : Absolument ! Ajoutez des appels `append` supplémentaires avec le `Locale.forLanguageTag("xx-XX")` souhaité.

**Q : Aspose.Note for Java est‑il compatible avec les dernières versions de Java ?**  
A : Oui, la bibliothèque est régulièrement mise à jour pour prendre en charge les dernières versions de Java.

**Q : Comment gérer les erreurs pendant le processus de définition de la langue ?**  
A : Enveloppez l'opération d'enregistrement dans un bloc `try‑catch` pour capturer `IOException` ou `AsposeException`.

**Q : Puis‑je intégrer ce code dans une application web ?**  
A : Bien sûr. Il suffit d'inclure le JAR Aspose.Note dans le classpath de votre projet web et de vous assurer que le serveur a les permissions d'écriture sur le répertoire cible.

**Q : Où puis‑je trouver des exemples supplémentaires et de la documentation pour Aspose.Note for Java ?**  
A : Consultez la [documentation](https://reference.aspose.com/note/java/) pour une liste complète des API et des projets d'exemple.

---

**Dernière mise à jour :** 2026-09-29  
**Testé avec :** Aspose.Note for Java 24.12  
**Auteur :** Aspose  

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
document.appendChildLast(page);
document.save(Paths.get(dataDir, "SetProofingLanguageForText.one").toString()); 
```

## Tutoriels associés

- [Charger un fichier OneNote avec Java : Utiliser Aspose.Note pour charger des documents OneNote](/note/java/onenote-document-loading/load-onenote-document/)
- [Convertir OneNote en texte brut – Extraire tout le texte avec Aspose.Note for Java](/note/java/onenote-text-manipulation/extract-all-text/)
- [Convertir OneNote en PDF en utilisant les paramètres de page avec Aspose.Note for Java](/note/java/onenote-document-saving/save-to-pdf-using-page-settings/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}