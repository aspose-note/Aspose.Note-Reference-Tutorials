---
date: 2025-12-09
description: Aprenda como salvar o OneNote como PDF com texto rico formatado em Java
  usando o Aspose.Note para Java. Siga nosso guia passo a passo para automação de
  documentos sem complicações.
linktitle: Save OneNote as PDF with Formatted Rich Text in Java
second_title: Aspose.Note Java API
title: Salvar OneNote como PDF com Texto Rico Formatado em Java
url: /pt/java/onenote-document-manipulation/create-onenote-document-formatted-rich-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salvar OneNote como PDF com Texto Rico Formatado em Java

## Introdução

Se você precisa **salvar OneNote como PDF** preservando a formatação de texto rico, está no lugar certo. Neste tutorial vamos percorrer a criação de um documento OneNote, a aplicação de estilos personalizados e a exportação direta para PDF usando Aspose.Note for Java. Ao final, você terá um trecho de código reutilizável que pode ser inserido em qualquer projeto Java para automatizar conversões elegantes de OneNote para PDF.

## Respostas Rápidas
- **O que este tutorial ensina?** Como criar um documento OneNote com texto estilizado e salvá‑lo como PDF.  
- **Qual biblioteca é necessária?** Aspose.Note for Java (disponível para download no site oficial).  
- **Preciso de licença?** Uma licença temporária funciona para testes; uma licença completa é necessária para produção.  
 **Qual IDE posso usar?** Qualquer IDE Java — IntelliJ IDEA, Eclipse ou Net.  
- **Posso mudar o formato de saída?** Sim, o Aspose.Note suporta PDF, HTML, PNG e muito mais.

## O que significa “salvar onenote como pdf”?
Salvar OneNote como PDF significa converter a estrutura da página OneNote — incluindo texto, imagens e formatação — em um arquivo PDF estático que pode ser visualizado em qualquer plataforma sem a necessidade do OneNote.

## Por que formatar texto rico em java?
Aplicar formatação de texto rico (fontes, cores, estilos) diretamente em Java permite gerar documentos que parecem profissionais e que seguem as diretrizes da sua marca sem edição manual.

## Pré‑requisitos

1. **Java Development Kit (JDK)** – qualquer versão recente (8 ou superior).  
2. **Aspose.Note for Java JAR** – faça o download pelo [link de download](https://releases.aspose.com/note/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse ou qualquer editor de sua preferência.  

## Importar Pacotes

Primeiro, você precisa importar os pacotes necessários ao seu projeto Java. Adicione as seguintes instruções de importação ao início do seu arquivo Java:

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

## Etapa 1: Configurar Documento e Página

Vamos começar inicializando os objetos `Document` e `Page`:

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

## Etapa 2: Criar Título com Formatação

Agora, vamos criar um título com texto formatado:

```java
Title title = new Title();
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);

RichText titleText = new RichText().append("Title!");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
```

## Etapa 3: Criar Texto Rico com Formatação

Em seguida, vamos criar texto rico com vários estilos de formatação:

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();

TextStyle textStyleForHelloWord = new TextStyle()
                                        .setFontColor(Color.red)
                                        .setFontName("Arial")
                                        .setFontSize(10);

TextStyle textStyleForOneNoteWord = new TextStyle()
                                        .setFontColor(Color.green)
                                        .setFontName("Calibri")
                                        .setFontSize(10)
                                        .setItalic(true);

TextStyle textStyleForTextWord = new TextStyle()
                                        .setFontColor(Color.blue)
                                        .setFontName("Arial")
                                        .setFontSize(15)
                                        .setBold(true)
                                        .setItalic(true);

RichText text = new RichText()
        .append("Hello", textStyleForHelloWord)
        .append(" OneNote", textStyleForOneNoteWord)
        .append(" text", textStyleForTextWord)
        .append("!", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
```

## Etapa 4: Adicionar Elementos à Página e ao Documento

Agora, vamos adicionar o título e o texto rico à página e aos elementos de contorno:

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.setTitle(title);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## Etapa 5: Salvar Documento

Por fim, salve o documento OneNote criado como PDF:

```java
doc.save(dataDir + "CreateOneNoteDocument_out.pdf", SaveFormat.Pdf);
```

## Problemas Comuns e Soluções

| Problema | Solução |
|----------|----------|
| **Arquivo não encontrado** | Verifique se `dataDir` aponta para uma pasta existente e se você tem permissões de gravação. |
| **Fontes ausentes** | Certifique‑se de que fontes referenciadas (por exemplo, *Calibri*) estejam instaladas na máquina host. |
| **Licença não aplicada** | Carregue sua licença Aspose antes de criar o `Document` para evitar marcas d'água de avaliação. |

## Perguntas Frequentes

**P: Posso personalizar ainda mais os estilos de fonte?**  
R: Sim, você pode ajustar propriedades adicionais como sublinhado, tachado e alinhamento de texto via as classes `TextStyle` e `ParagraphStyle`.

**P: O Aspose.Note for Java é compatível com todas as IDEs Java?**  
R: Absolutamente. Desde que a IDE suporte desenvolvimento Java padrão, você pode adicionar o JAR do Aspose.Note ao classpath do projeto.

**P: Posso integrar essa funcionalidade em aplicações web?**  
R: Sim, o mesmo código funciona em aplicações baseadas em servlet ou Spring Boot, permitindo a geração dinâmica de OneNote‑para‑PDF no lado do servidor.

**P: Existem requisitos de licenciamento para usar o Aspose.Note for Java?**  
R: Uma licença comercial é necessária para uso em produção. Uma licença temporária está disponível para avaliação e testes.

**P: O Aspose.Note for Java suporta outros formatos de documento além do OneNote?**  
R: Ele suporta PDF, HTML, PNG, JPEG e vários outros formatos de exportação, oferecendo flexibilidade para converter páginas OneNote no formato que você precisar.

## Conclusão

Neste guia demonstramos como **salvar OneNote como PDF** aplicando formatação de texto rico usando Aspose.Note for Java. Seguindo as instruções passo a passo, você pode automatizar a criação de documentos OneNote bem elaborados e convertê‑los para PDF em qualquer solução baseada em Java.

---

**Última atualização:** 2025-12-09  
**Testado com:** Aspose.Note for Java 24.11 (mais recente na data de escrita)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-wrap-class >}}
{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}