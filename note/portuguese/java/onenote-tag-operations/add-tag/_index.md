---
date: 2026-01-28
description: Aprenda a criar esboço no OneNote, adicionar tags ao OneNote e gerar
  PDF a partir do OneNote usando Aspose.Note para Java.
linktitle: Create Outline in OneNote and Add Tag – Aspose.Note
second_title: Aspose.Note Java API
title: Criar contorno no OneNote e adicionar etiqueta – Aspose.Note
url: /pt/java/onenote-tag-operations/add-tag/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Criar Estrutura no OneNote e Adicionar Tag – Aspose.Note

## Introdução
Você está procurando **criar estrutura no OneNote** e melhorar a colaboração com tags usando Java? Aspose.Note for Java torna simples adicionar tags, estruturar suas notas e até **gerar PDF a partir de arquivos OneNote**. Neste tutorial percorreremos cada passo, explicaremos *por que* cada parte é importante e mostraremos como produzir um PDF polido ao final.

## Respostas Rápidas
- **O que significa “criar estrutura no OneNote”?** Ele cria uma estrutura hierárquica (esboços) que organiza o conteúdo como títulos e subseções.  
- **Qual biblioteca adiciona tags ao OneNote?** Aspose.Note for Java fornece a classe `NoteTag` para marcadores visuais.  
- **Posso exportar o resultado para PDF?** Sim – use `SaveFormat.Pdf` para **gerar PDF a partir de OneNote**.  
- **Preciso de licença para produção?** Uma licença temporária está disponível para testes; uma licença completa é necessária para uso comercial.  
- **Quais são os principais pré‑requisitos?** JDK instalado, biblioteca Aspose.Note for Java e conhecimento básico de Java.

## O que é “criar estrutura no OneNote”?
Criar uma estrutura no OneNote significa adicionar objetos `Outline` e `OutlineElement` que definem uma estrutura em árvore para suas notas. Essa hierarquia permite recolher, expandir e organizar informações assim como títulos em um documento.

## Por que adicionar tag ao OneNote?
Tags como estrelas, marcas de verificação ou ícones personalizados dão ao leitor pistas visuais, melhoram a capacidade de busca e ajudam as equipes a priorizar itens. Com Aspose.Note você pode anexar programaticamente um `NoteTag` a qualquer trecho de texto.

## Pré‑requisitos
Antes de começar, confirme que você tem:
- Java Development Kit (JDK) instalado.
- Biblioteca Aspose.Note for Java baixada. Você pode obtê‑la [aqui](https://releases.aspose.com/note/java/).
- Um entendimento básico de programação Java.

## Importar Pacotes
Certifique‑se de importar os pacotes necessários para iniciar seu projeto:
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.TagIcon;
import com.aspose.note.ParagraphStyle;
```
Vamos dividir o código acima em um guia passo a passo.

## Etapa 1: Configurar Documento e Página
Comece criando um novo objeto `Document` e inicializando um objeto `Page`:
```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```
Aqui, definimos o caminho para o diretório de documentos, criamos um novo `Document` e inicializamos uma `Page`.

## Etapa 2: Criar uma Estrutura
Em seguida, crie um objeto `Outline` para estruturar seu conteúdo:
```java
Outline outline = new Outline();
```
Estruturas fornecem uma hierarquia ao seu documento, facilitando **criar estrutura no OneNote** e manter as informações organizadas.

## Etapa 3: Inicializar OutlineElement e ParagraphStyle
Agora, inicialize um `OutlineElement` e defina `ParagraphStyle` para formatação de texto:
```java
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                .setFontColor(Color.black)
                                .setFontName("Arial")
                                .setFontSize(10);
```
`OutlineElement` representa um elemento dentro da estrutura, e `ParagraphStyle` define as propriedades de formatação do texto.

## Etapa 4: Adicionar RichText com NoteTag
Crie um objeto `RichText`, anexe seu texto do OneNote e adicione um `NoteTag`:
```java
RichText text = new RichText().append("OneNote text.");
text.setParagraphStyle(textStyle);
NoteTag noteTag = NoteTag.createYellowStar();
text.getTags().add(noteTag);
```
`RichText` permite incorporar texto formatado, e o `NoteTag` **adiciona tag ao OneNote** como um indicativo visual.

## Etapa 5: Construir Estrutura da Estrutura
Adicione o nó de texto, o nó de elemento da estrutura e o nó da estrutura para montar a hierarquia do documento:
```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```
Esta etapa garante que seu conteúdo esteja organizado dentro do documento, concluindo o processo de **criar estrutura no OneNote**.

## Etapa 6: Salvar o Documento
Salve o documento no formato PDF, que **gera PDF a partir de OneNote**:
```java
doc.save(dataDir + "AddTag_out.pdf", SaveFormat.Pdf);
System.out.printf("File Saved: %s\n", dataDir + "AddTag_out.pdf");
```
Agora, seu documento OneNote com tags adicionadas está salvo como PDF.

Seguindo estas etapas, você pode aprimorar facilmente seus documentos OneNote usando Aspose.Note for Java.

## Conclusão
Neste tutorial exploramos como **criar estrutura no OneNote**, adicionar uma tag ao OneNote e então **gerar PDF a partir de OneNote** usando Aspose.Note for Java. Utilizar Java lhe dá controle total sobre a estrutura da nota, a marcação visual e as opções de exportação, tornando suas notas mais organizadas e compartilháveis.

## Perguntas Frequentes
### 1. Posso usar Aspose.Note for Java com outras linguagens de programação?
Aspose.Note suporta principalmente Java, mas também há versões disponíveis para .NET.

### 2. Aspose.Note for Java é adequado para iniciantes?
Sim, Aspose.Note for Java oferece documentação abrangente e suporte, tornando‑a acessível tanto para iniciantes quanto para desenvolvedores experientes.

### 3. Como posso obter uma licença temporária para Aspose.Note for Java?
Você pode obter uma licença temporária [aqui](https://purchase.aspose.com/temporary-license/).

### 4. Onde posso encontrar suporte adicional?
Para dúvidas ou assistência, visite o [fórum Aspose.Note](https://forum.aspose.com/c/note/28).

### 5. Existe uma versão de teste gratuita?
Sim, você pode explorar uma avaliação gratuita [aqui](https://releases.aspose.com/).

**Perguntas e Respostas Adicionais**

**P: Posso personalizar o ícone da tag?**  
R: Sim – Aspose.Note fornece vários ícones predefinidos via `TagIcon` e também permite imagens personalizadas.

**P: Como altero as configurações de saída do PDF?**  
R: Use `PdfSaveOptions` para controlar qualidade de imagem, compressão e segurança antes de chamar `doc.save`.

**P: É possível adicionar múltiplas tags ao mesmo texto?**  
R: Absolutamente. Chame `text.getTags().add()` várias vezes com diferentes instâncias de `NoteTag`.

---

**Última atualização:** 2026-01-28  
**Testado com:** Aspose.Note for Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}