---
title: Crie uma lista com marcadores no OneNote - Aspose.Note
linktitle: Crie uma lista com marcadores no OneNote - Aspose.Note
second_title: API Java Aspose.Note
description: Explore o guia passo a passo sobre como criar listas com marcadores no OneNote usando Aspose.Note para Java. Eleve a criação de seus documentos com facilidade.
weight: 12
url: /pt/java/onenote-text-manipulation/create-bulleted-list/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Crie uma lista com marcadores no OneNote - Aspose.Note

## Introdução
No cenário dinâmico do desenvolvimento Java, a criação de documentos envolventes e organizados é essencial. Aspose.Note for Java fornece um conjunto de ferramentas poderoso para aprimorar seu processo de criação de documentos. Este tutorial irá guiá-lo através do processo de criação de listas com marcadores no OneNote usando Aspose.Note para Java. Vamos mergulhar nos detalhes.
## Pré-requisitos
Antes de começarmos, certifique-se de ter os seguintes pré-requisitos:
- Conhecimento básico de programação Java.
-  Biblioteca Aspose.Note para Java instalada. Você pode baixá-lo no[Aspose.Note para documentação Java](https://reference.aspose.com/note/java/).
- Um Java Integrated Development Environment (IDE) configurado em sua máquina.
## Importar pacotes
Comece importando os pacotes necessários para o seu projeto Java. Isso garante que você tenha acesso às funcionalidades do Aspose.Note for Java.
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NumberList;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.ParagraphStyle;
// Importar pacotes Aspose.Note para Java
```
## Etapa 1: inicializar documento e página
Crie um objeto da classe Document e inicialize um objeto da classe Page.
```java
String dataDir = "Your Document Directory";
// crie um objeto da classe Document
Document doc = new Document();
// inicializar objeto de classe Page
Page page = new Page();
```
## Etapa 2: inicializar Outline e TextStyle
Agora, inicialize um objeto da classe Outline e um objeto da classe TextStyle com propriedades de formatação.
```java
// inicializar o objeto da classe Outline
Outline outline = new Outline();
// inicialize o objeto da classe TextStyle e defina as propriedades de formatação
ParagraphStyle defaultStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```
## Etapa 3: criar elementos de lista com marcadores
Crie objetos da classe OutlineElement e aplique marcadores para criar uma lista com marcadores.
```java
// inicializar objetos da classe OutlineElement e aplicar marcadores
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("*", "Arial", 10));
// inicialize o objeto da classe RichText e aplique o estilo de texto
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
```
Repita as etapas acima para cada elemento da sua lista com marcadores.
## Etapa 4: adicionar elementos de contorno ao contorno
Adicione os objetos OutlineElement criados ao Outline.
```java
// adicionar elementos de contorno
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```
## Etapa 5: adicionar esboço à página e salvar
Adicione o nó Outline à Página e, em seguida, adicione o nó Página ao Documento. Por fim, salve o documento.
```java
// adicionar nó de contorno
page.appendChildLast(outline);
// adicionar nó de página
doc.appendChildLast(page);
// salve o documento
doc.save(dataDir + "CreateBulletedList_out.pdf");
```
Parabéns! Você criou com êxito uma lista com marcadores no OneNote usando Aspose.Note para Java.
## Conclusão
Aspose.Note for Java simplifica o processo de criação de documentos bem formatados. Este tutorial orientou você nas etapas para criar uma lista com marcadores no OneNote. Explore mais possibilidades com Aspose.Note para aprimorar sua experiência de criação de documentos.
## Perguntas frequentes
### O Aspose.Note for Java é compatível com todos os IDEs Java?
Sim, Aspose.Note for Java é compatível com ambientes de desenvolvimento integrados Java populares, como Eclipse e IntelliJ IDEA.
### Posso personalizar a formatação da lista com marcadores?
Absolutamente! Você pode modificar a fonte, a cor e o tamanho dos elementos da lista com marcadores de acordo com suas preferências.
### Onde posso encontrar suporte adicional para Aspose.Note for Java?
 Visite a[Fórum de suporte Aspose.Note para Java](https://forum.aspose.com/c/note/28) para obter ajuda da comunidade.
### Existe uma avaliação gratuita disponível para Aspose.Note para Java?
 Sim, você pode explorar uma versão de avaliação gratuita[aqui](https://releases.aspose.com/).
### Como posso obter uma licença temporária do Aspose.Note for Java?
 Obtenha uma licença temporária[aqui](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
