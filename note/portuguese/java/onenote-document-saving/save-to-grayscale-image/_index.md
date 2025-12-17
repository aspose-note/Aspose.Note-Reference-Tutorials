---
date: 2025-12-17
description: Aprenda como exportar o OneNote salvando um documento como imagem PNG
  em escala de cinza usando o Aspose.Note para Java. Inclui etapas para carregar o
  documento do OneNote e criar a imagem em escala de cinza.
linktitle: How to Export OneNote as Grayscale Image – Aspose.Note
second_title: Aspose.Note Java API
title: Como Exportar o OneNote como Imagem em Escala de Cinza – Aspose.Note
url: /pt/java/onenote-document-saving/save-to-grayscale-image/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salvar como Imagem em Tons de Cinza no OneNote - Aspose.Note

## Introdução

Neste tutorial, mostraremos **como exportar onenote** salvando um documento como uma imagem em tons de cinza usando o Aspose.Note para Java. Imagens em tons de cinza são fotos monocromáticas que contêm apenas sombras de cinza, o que pode ser útil para impressão, arquivamento ou redução do tamanho do arquivo. Percorreremos o carregamento de um documento OneNote, a configuração das opções de salvamento para **criar uma imagem em tons de cinza** e, finalmente, **salvar o documento como PNG**.

## Respostas Rápidas
- **O que significa “como exportar onenote”?** Refere‑se à conversão de um arquivo OneNote para outro formato, como uma imagem, de forma programática.  
- **Qual formato é o melhor para saída em tons de cinza?** PNG funciona bem porque preserva qualidade sem perdas e suporta o modo de cor em tons de cinza.  
- **Preciso de uma licença?** É necessária uma licença válida do Aspose.Note para uso em produção; uma licença de avaliação temporária está disponível para testes.  
- **Qual versão do Java é necessária?** Java 8 ou superior é recomendada.  
- **Posso alterar o tamanho da imagem?** Sim, você pode ajustar as propriedades do `ImageSaveOptions` como `Resolution` ou `PageSize` antes de salvar.

## O que é “como exportar onenote”?
Exportar OneNote significa converter programaticamente um arquivo OneNote `.one` para outra representação — como PDF, HTML ou uma imagem. Neste guia, focamos na exportação para uma **imagem PNG em tons de cinza**, que é uma necessidade comum em fluxos de documentação ou impressão.

## Por que exportar OneNote como imagem em tons de cinza?
- **Tamanho de arquivo reduzido** – PNGs em tons de cinza costumam ser menores que imagens em cores completas.  
- **Melhor legibilidade** – Em relatórios impressos, o cinza frequentemente oferece contraste mais claro.  
- **Compatibilidade** – PNG é amplamente suportado em navegadores, editores e dispositivos móveis.  

## Pré‑requisitos

Antes de começar, certifique‑se de que você tem o seguinte:

1. Java Development Kit (JDK) instalado no seu sistema.  
2. Biblioteca Aspose.Note para Java. Você pode baixá‑la [aqui](https://releases.aspose.com/note/java/).  
3. Noções básicas de programação em Java.  

## Importar Pacotes

Para iniciar, importe os pacotes necessários:

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## Etapa 1: Carregar o Documento OneNote

Primeiro, **carregue o documento onenote** no Aspose.Note. Substitua `"Your Document Directory"` pelo caminho da sua pasta local e `"Aspose.one"` pelo nome do seu arquivo OneNote.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Etapa 2: Definir Caminho de Saída e Opções

Defina o caminho de saída para a imagem em tons de cinza e especifique as opções de salvamento. Definiremos o `ColorMode` como `GrayScale` e usaremos o formato **save document as png**.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## Etapa 3: Salvar o Documento

Por fim, salve o documento como uma imagem PNG em tons de cinza usando as opções configuradas.

```java
oneFile.save(dataDir, options);
```

## Problemas Comuns e Soluções
- **FileNotFoundException** – Verifique se `dataDir` aponta para a pasta correta e se o arquivo `.one` existe.  
- **LicenseException** – Certifique‑se de que aplicou uma licença válida do Aspose.Note antes de chamar `save`.  
- **Saída de baixa resolução** – Ajuste `options.setResolution(300)` para aumentar o DPI, se necessário.

## Perguntas Frequentes

**Q1: Posso salvar a imagem em tons de cinza em outro formato?**  
A1: Sim, basta alterar o parâmetro `SaveFormat` no construtor `ImageSaveOptions` para `Jpeg`, `Bmp`, etc.

**Q2: O Aspose.Note é compatível com todas as versões de documentos OneNote?**  
A2: Aspose.Note suporta Microsoft OneNote 2010 e versões posteriores.

**Q3: O Aspose.Note requer licença para uso?**  
A3: Uma licença válida é necessária para uso em produção, mas uma licença de avaliação temporária pode ser obtida para avaliação.

**Q4: Posso manipular outros aspectos do documento antes de salvá‑lo como imagem?**  
A4: Absolutamente! Aspose.Note oferece uma API completa para editar seções, páginas e conteúdo antes da exportação.

**Q5: Onde posso encontrar suporte caso encontre problemas?**  
A5: Você pode encontrar suporte no fórum do Aspose.Note [aqui](https://forum.aspose.com/c/note/28).

## Conclusão

Agora você aprendeu **como exportar onenote** carregando um arquivo OneNote, configurando as opções de salvamento para **criar uma imagem em tons de cinza** e **salvando o documento como PNG**. Essa técnica é útil para gerar visuais leves e prontos para impressão a partir de cadernos OneNote. Sinta‑se à vontade para experimentar outras configurações de `ColorMode` ou formatos de imagem para atender às necessidades do seu projeto.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Última atualização:** 2025-12-17  
**Testado com:** Aspose.Note 24.12 para Java  
**Autor:** Aspose  

---