---
date: 2026-06-30
description: Aprenda como exportar o OneNote salvando um documento como imagem PNG
  em escala de cinza usando o Aspose.Note para Java. Inclui etapas para carregar o
  documento do OneNote e criar a imagem em escala de cinza.
keywords:
- how to export onenote
- adjust image resolution
- reduce onenote size
- create grayscale png
- grayscale conversion java
linktitle: Como Exportar OneNote como Imagem em Escala de Cinza – Aspose.Note
schemas:
- author: Aspose
  dateModified: '2026-06-30'
  description: Learn how to export onenote by saving a document as a grayscale PNG
    image using Aspose.Note for Java. Includes steps to load onenote document and
    create grayscale image.
  headline: How to Export OneNote as Grayscale Image – Aspose.Note
  type: TechArticle
- description: Learn how to export onenote by saving a document as a grayscale PNG
    image using Aspose.Note for Java. Includes steps to load onenote document and
    create grayscale image.
  name: How to Export OneNote as Grayscale Image – Aspose.Note
  steps:
  - name: Java Development Kit (JDK) 8 or newer installed.
    text: Java Development Kit (JDK) 8 or newer installed.
  - name: Aspose.Note for Java library – download the latest release from [here](https://releases.aspose.com/note/java/).
    text: Aspose.Note for Java library – download the latest release from [here](https://releases.aspose.com/note/java/).
  - name: A basic understanding of Java syntax and Maven/Gradle project setup.
    text: A basic understanding of Java syntax and Maven/Gradle project setup.
  type: HowTo
- questions:
  - answer: It refers to programmatically converting a OneNote file into another format,
      such as an image, using code.
    question: What does “how to export onenote” mean?
  - answer: PNG works well because it preserves loss‑less quality and supports a dedicated
      grayscale color mode.
    question: Which format is best for grayscale output?
  - answer: A valid Aspose.Note license is required for production use; a temporary
      trial license is available for testing.
    question: Do I need a license?
  - answer: Java 8 or higher is recommended.
    question: What Java version is required?
  - answer: Yes, you can adjust the `ImageSaveOptions` properties like `Resolution`
      or `PageSize` before saving.
    question: Can I change the image size?
  type: FAQPage
second_title: Aspose.Note Java API
title: Como Exportar OneNote como Imagem em Escala de Cinza – Aspose.Note
url: /pt/java/onenote-document-saving/save-to-grayscale-image/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salvar como Imagem em Tons de Cinza no OneNote - Aspose.Note

## Introdução

Neste tutorial você descobrirá **como exportar onenote** convertendo um arquivo OneNote `.one` em uma imagem PNG em tons de cinza de alta qualidade usando Aspose.Note para Java. A conversão para tons de cinza é frequentemente necessária para desenvolvedores Java para impressão, arquivamento ou para **reduzir o tamanho do OneNote** sem perder conteúdo essencial. Vamos percorrer o carregamento de um documento OneNote, a configuração das opções de salvamento — incluindo **ajustar a resolução da imagem** — e, finalmente, salvar o documento como PNG.

## Respostas Rápidas
- **O que significa “how to export onenote”?** Refere‑se a converter programaticamente um arquivo OneNote em outro formato, como uma imagem, usando código.  
- **Qual formato é melhor para saída em tons de cinza?** PNG funciona bem porque preserva qualidade sem perdas e suporta um modo de cor dedicado em tons de cinza.  
- **Preciso de uma licença?** Uma licença válida do Aspose.Note é necessária para uso em produção; uma licença de avaliação temporária está disponível para testes.  
- **Qual versão do Java é necessária?** Java 8 ou superior é recomendada.  
- **Posso alterar o tamanho da imagem?** Sim, você pode ajustar as propriedades do `ImageSaveOptions` como `Resolution` ou `PageSize` antes de salvar.

## O que é “how to export onenote”?

Exportar OneNote significa converter programaticamente um arquivo OneNote `.one` em outra representação — como PDF, HTML ou uma imagem. Neste guia, focamos em **criar imagens PNG em tons de cinza**, uma necessidade comum para documentação ou fluxos de trabalho prontos para impressão. Usando Aspose.Note, a conversão ocorre totalmente na memória, portanto você nunca precisa do Microsoft OneNote instalado no servidor.

## Por que exportar OneNote como uma imagem em tons de cinza?

Os PNGs em tons de cinza são tipicamente **30‑40 % menores** que suas versões em cores completas, o que acelera a entrega na web e reduz custos de armazenamento. Eles também fornecem **contraste mais nítido** em impressoras a laser, facilitando a leitura de relatórios. Como o PNG é universalmente suportado, os arquivos resultantes funcionam em navegadores, dispositivos móveis e editores de desktop sem codecs adicionais.

## Pré-requisitos

1. Java Development Kit (JDK) 8 ou mais recente instalado.  
2. Biblioteca Aspose.Note para Java – faça o download da versão mais recente a partir de [aqui](https://releases.aspose.com/note/java/).  
3. Um entendimento básico da sintaxe Java e da configuração de projetos Maven/Gradle.  

## Importar Pacotes

A classe `ImageSaveOptions` controla como o documento é renderizado para uma imagem.  
`ColorMode` é uma enumeração que permite alternar entre saída em cores completas e em tons de cinza.

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## Etapa 1: Carregar o Documento OneNote

`Document` representa um caderno OneNote e fornece métodos para carregar, editar e salvar seu conteúdo. Primeiro, **carregue o documento OneNote** no Aspose.Note. Substitua `"Your Document Directory"` pelo caminho da sua pasta local e `"Aspose.one"` pelo nome do seu arquivo OneNote.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Etapa 2: Definir o Caminho de Saída e as Opções

`ImageSaveOptions` configura como um documento OneNote é renderizado para um arquivo de imagem. A enumeração `ColorMode` seleciona o modo de renderização de cor, como tons de cinza ou cores completas. Defina o caminho de saída para a imagem em tons de cinza e especifique as opções de salvamento. Definiremos o `ColorMode` para `GrayScale` e usaremos o formato **salvar documento como PNG**. Você também pode **ajustar a resolução da imagem** para 300 DPI para impressões de alta qualidade.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## Etapa 3: Salvar o Documento

Finalmente, salve o documento como uma imagem PNG em tons de cinza usando as opções configuradas. O método `save` grava o arquivo no disco sem exigir arquivos temporários intermediários.

```java
oneFile.save(dataDir, options);
```

## Problemas Comuns e Soluções
- **FileNotFoundException** – Verifique se `dataDir` aponta para a pasta correta e se o arquivo `.one` existe.  
- **LicenseException** – Certifique‑se de que aplicou uma licença válida do Aspose.Note antes de chamar `save`.  
- **Saída de baixa resolução** – Ajuste `options.setResolution(300)` para aumentar o DPI; DPI mais alto produz impressões mais nítidas, porém arquivos maiores.  

## Perguntas Frequentes

**Q1: Posso salvar a imagem em tons de cinza em um formato diferente?**  
A1: Sim, basta alterar o parâmetro `SaveFormat` no construtor `ImageSaveOptions` para `Jpeg`, `Bmp` ou qualquer um dos mais de 20 formatos de imagem suportados.

**Q2: O Aspose.Note é compatível com todas as versões de documentos OneNote?**  
A2: O Aspose.Note suporta Microsoft OneNote 2010 e posteriores, cobrindo mais de 95 % dos cadernos em uso ativo hoje.

**Q3: O Aspose.Note requer uma licença para uso?**  
A3: Uma licença válida é necessária para uso em produção, mas uma licença de avaliação temporária pode ser obtida para avaliação sem custo.

**Q4: Posso manipular outros aspectos do documento antes de salvá‑lo como imagem?**  
A4: Absolutamente! O Aspose.Note fornece APIs para editar seções, páginas e elementos individuais como texto, tabelas e imagens antes da exportação.

**Q5: Onde posso encontrar suporte se encontrar problemas?**  
A5: Você pode encontrar suporte no fórum Aspose.Note [aqui](https://forum.aspose.com/c/note/28).

## Conclusão

Agora você aprendeu **como exportar onenote** carregando um arquivo OneNote, configurando as opções de salvamento para **criar uma imagem em tons de cinza** e **salvando o documento como PNG**. Essa abordagem é ideal para gerar visuais leves e prontos para impressão a partir de cadernos OneNote. Sinta‑se à vontade para experimentar outras configurações de `ColorMode`, valores de DPI mais altos ou formatos de imagem alternativos para atender aos requisitos do seu projeto.

---

**Last Updated:** 2026-06-30  
**Tested With:** Aspose.Note 27.0 for Java  
**Author:** Aspose  

---

{{< blocks/products/products-backtop-button >}}

## Tutoriais Relacionados

- [Exportar Página OneNote para Imagem PNG em Java usando Aspose.Note](/note/java/onenote-document-loading/convert-page-to-png-image/)
- [aspnote set jpeg resolution – Definir Resolução da Imagem de Saída no OneNote - Aspose.Note](/note/java/onenote-document-saving/set-output-image-resolution/)
- [Como Salvar OneNote como PDF com Aspose.Note para Java](/note/java/onenote-document-loading/load-save-format/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}