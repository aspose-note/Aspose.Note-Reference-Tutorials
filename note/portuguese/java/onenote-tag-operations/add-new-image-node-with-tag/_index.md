---
title: Adicionar novo nó de imagem com tag no OneNote - Aspose.Note
linktitle: Adicionar novo nó de imagem com tag no OneNote - Aspose.Note
second_title: API Java Aspose.Note
description: Aprenda como adicionar um novo nó de imagem com uma tag no OneNote usando Aspose.Note para Java. Eleve suas habilidades de programação Java sem esforço.
type: docs
weight: 10
url: /pt/java/onenote-tag-operations/add-new-image-node-with-tag/
---
## Introdução
No domínio da programação Java, Aspose.Note se destaca como uma ferramenta poderosa para lidar com documentos do OneNote com facilidade. Se você deseja aprimorar suas habilidades e aprender como adicionar um novo nó de imagem com uma tag no OneNote usando Aspose.Note, você veio ao lugar certo. Este guia passo a passo orientará você durante o processo, garantindo que você compreenda cada conceito completamente.
## Pré-requisitos
Antes de mergulharmos no tutorial, vamos ter certeza de que você tem tudo o que precisa:
1.  Aspose.Note para Java: certifique-se de ter a biblioteca Aspose.Note instalada. Se não, você pode baixá-lo[aqui](https://releases.aspose.com/note/java/).
2. Ambiente de desenvolvimento Java: certifique-se de ter um ambiente de desenvolvimento Java funcional configurado em sua máquina.
Agora que temos os pré-requisitos definidos, vamos passar para as próximas etapas.
## Importar pacotes
No seu projeto Java, comece importando os pacotes necessários:
```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Image;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
import com.aspose.note.TagIcon;
```
## Etapa 1: Criar objeto de documento
```java
// O caminho para o diretório de documentos.
String dataDir = "Your Document Directory";
// crie um objeto da classe Document
Document doc = new Document();
```
## Etapa 2: inicializar o objeto de classe de página
```java
// inicializar objeto de classe Page
Page page = new Page();
```
## Etapa 3: inicializar o objeto de classe Outline
```java
// inicializar o objeto da classe Outline
Outline outline = new Outline();
```
## Etapa 4: inicializar o objeto da classe OutlineElement
```java
// inicializar o objeto da classe OutlineElement
OutlineElement outlineElem = new OutlineElement();
```
## Etapa 5: carregar e inserir imagem
```java
// carregar uma imagem
Image image = new Image(null, dataDir + "Input.jpg");
// inserir imagem no nó do documento
outlineElem.appendChildLast(image);
```
## Etapa 6: adicionar etiqueta de nota à imagem
```java
// adicione uma etiqueta de nota com estrela amarela à imagem
NoteTag noteTag = NoteTag.createYellowStar();
image.getTags().add(noteTag);
```
## Etapa 7: Adicionar nó do elemento de contorno
```java
// adicionar nó de elemento de contorno
outline.appendChildLast(outlineElem);
```
## Etapa 8: adicionar nó de contorno
```java
// adicionar nó de contorno
page.appendChildLast(outline);
```
## Etapa 9: adicionar nó de página
```java
// adicionar nó de página
doc.appendChildLast(page);
```
## Etapa 10: Salvar documento do OneNote
```java
// salvar documento do OneNote como PDF
doc.save(dataDir + "AddNewImageNodeWithTag_out.pdf", SaveFormat.Pdf);
```
Parabéns! Você adicionou com êxito um novo nó de imagem com uma tag no OneNote usando Aspose.Note para Java.
## Conclusão
 Dominar o Aspose.Note para Java abre possibilidades interessantes na manipulação de documentos do OneNote. Seguindo este tutorial, você adquiriu uma habilidade prática que pode ser aplicada a vários projetos. Continue explorando a documentação do Aspose.Note[aqui](https://reference.aspose.com/note/java/)para recursos e possibilidades mais avançados.
## Perguntas frequentes
### Onde posso encontrar a documentação do Aspose.Note?
 Você pode encontrar a documentação[aqui](https://reference.aspose.com/note/java/).
### Como faço o download do Aspose.Note para Java?
 Você pode baixá-lo na página de lançamentos[aqui](https://releases.aspose.com/note/java/).
### Existe um teste gratuito disponível?
 Sim, você pode acessar o teste gratuito[aqui](https://releases.aspose.com/).
### Onde posso obter suporte para Aspose.Note?
 Visite o fórum da comunidade[aqui](https://forum.aspose.com/c/note/28) para suporte.
### Preciso de uma licença temporária?
 Se necessário, você pode obter uma licença temporária[aqui](https://purchase.aspose.com/temporary-license/).