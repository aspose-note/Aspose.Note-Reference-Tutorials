---
date: 2026-03-29
description: Apprenez à définir la langue du texte dans OneNote à l'aide d'Aspose.Note
  pour Java. Ce guide étape par étape vous montre comment créer un document OneNote,
  modifier la langue du texte et enregistrer le fichier OneNote efficacement.
linktitle: Set Proofing Language for Text in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Comment définir la langue du texte dans OneNote – Aspose.Note
url: /fr/java/onenote-text-manipulation/set-proofing-language-for-text/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment définir la langue du texte dans OneNote – Aspose.Note

## Introduction
Si vous devez **comment définir la langue** pour des morceaux de texte spécifiques dans un carnet OneNote, Aspose.Note for Java rend cela simple. Dans ce tutoriel, vous apprendrez comment créer un document OneNote, modifier la langue du texte pour des mots ou des phrases individuels, puis enregistrer le fichier OneNote avec la langue de révision correcte appliquée. À la fin, vous comprendrez pourquoi la définition de la langue est importante pour la vérification orthographique et la localisation, et vous disposerez d’un exemple de code prêt à l’emploi.

## Réponses rapides
- **Qu’est‑ce que « set language » affecte ?** Cela indique à OneNote quel dictionnaire de révision utiliser pour la vérification orthographique et grammaticale.  
- **Puis‑je définir différentes langues dans la même note ?** Oui, vous pouvez attribuer une langue à chaque segment de texte.  
- **Ai‑je besoin d’une licence pour Aspose.Note ?** Un essai gratuit suffit pour les tests ; une licence commerciale est requise pour la production.  
- **Quelles versions de Java sont prises en charge ?** Aspose.Note for Java prend en charge Java 8 et les versions ultérieures.  
- **Le résultat est‑il un fichier .one ?** Oui, le document est enregistré au format OneNote *.one* file.

## Prérequis
Avant de plonger dans le code, assurez‑vous de disposer de ce qui suit :

1. **Environnement de développement Java** – JDK 8 ou supérieur installé et configuré.  
2. **Bibliothèque Aspose.Note for Java** – Téléchargez et installez la bibliothèque depuis le [download link](https://releases.aspose.com/note/java/).  
3. **Répertoire de documents** – Créez un dossier sur votre machine où le fichier OneNote généré sera enregistré.

## Pourquoi définir la langue du texte dans OneNote ?
Définir la langue de révision garantit que la vérification orthographique, les suggestions grammaticales et l’indexation de recherche fonctionnent correctement pour le contenu multilingue. Ceci est particulièrement utile pour :

- **Équipes mondiales** collaborant sur un même carnet.  
- **Documentation localisée** où chaque section peut être dans une langue différente.  
- **Applications basées sur les données** qui génèrent des notes de façon programmatique pour des utilisateurs du monde entier.

## Importer les packages
Commencez par importer les classes Aspose.Note nécessaires ainsi que les utilitaires Java.

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.Locale;
```

## Étape 1 : Configurer le document et la page
Créez un nouveau document OneNote et une page qui contiendra votre contenu. Cette étape montre également **create OneNote document**.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
```

## Étape 2 : Créer le contour et l’élément de contour
Un contour est le conteneur du contenu du carnet. Ici, nous construisons la structure qui contiendra plus tard le texte spécifique à une langue.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## Étape 3 : Ajouter du texte enrichi avec les paramètres de langue
Nous **modifier la langue du texte** maintenant en attachant un `TextStyle` avec un `Locale` spécifique à chaque segment de texte. Cela démontre **définir la langue du texte**.

```java
RichText text = new RichText()
                        .append("United States", new TextStyle().setLanguage(Locale.forLanguageTag("en-US")))
                        .append(" Germany", new TextStyle().setLanguage(Locale.forLanguageTag("de-DE")))
                        .append(" China", new TextStyle().setLanguage(Locale.forLanguageTag("zh-CN")));
text.setParagraphStyle(ParagraphStyle.getDefault());
```

## Étape 4 : Organiser les éléments et enregistrer
Assemblez la hiérarchie du contour, attachez‑la à la page, puis **enregistrer le fichier OneNote** avec les paramètres de langue appliqués.

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
document.appendChildLast(page);
document.save(Paths.get(dataDir, "SetProofingLanguageForText.one").toString()); 
```

## Écueils courants et conseils
- **Format du Locale** – Utilisez le tag IETF BCP‑47 (par ex., `en-US`, `de-DE`). Un tag incorrect reviendra à la langue du document.  
- **Chemin du fichier** – Assurez‑vous que `dataDir` pointe vers un dossier existant ; sinon `document.save` lèvera une `IOException`.  
- **Astuce :** Si vous devez définir la langue pour un paragraphe entier, appliquez le `TextStyle` au `ParagraphStyle` au lieu de chaque appel `append`.

## Conclusion
Vous venez d’apprendre **comment définir la langue** pour des fragments de texte individuels dans un carnet OneNote en utilisant Aspose.Note for Java. Cette fonctionnalité vous permet de **create OneNote document** programmatically, **modifier la langue du texte** à la volée, et **enregistrer le fichier OneNote** avec des métadonnées de révision précises.

## Questions fréquentes

**Q : Puis‑je définir la langue de révision pour d’autres langues non mentionnées dans l’exemple ?**  
R : Absolument ! Ajoutez des appels `append` supplémentaires avec le `Locale.forLanguageTag("xx-XX")` souhaité.

**Q : Aspose.Note for Java est‑il compatible avec les dernières versions de Java ?**  
R : Oui, la bibliothèque est régulièrement mise à jour pour prendre en charge les dernières versions de Java.

**Q : Comment gérer les erreurs lors du processus de définition de la langue ?**  
R : Enveloppez l’opération d’enregistrement dans un bloc `try‑catch` pour capturer `IOException` ou `AsposeException`.

**Q : Puis‑je intégrer ce code dans une application web ?**  
R : Bien sûr. Il suffit d’inclure le JAR Aspose.Note dans le classpath de votre projet web et de vous assurer que le serveur possède les droits d’écriture sur le répertoire cible.

**Q : Où puis‑je trouver des exemples supplémentaires et la documentation pour Aspose.Note for Java ?**  
R : Consultez la [documentation](https://reference.aspose.com/note/java/) pour une liste complète des API et des projets d’exemple.

**Dernière mise à jour :** 2026-03-29  
**Testé avec :** Aspose.Note for Java 24.12  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}