---
date: 2025-12-18
description: Aprenda a **salvar OneNote como PDF** usando o subsistema de fontes especificado
  em Java com Aspose.Note. Este guia também mostra como converter OneNote para PDF,
  carregar arquivos de fontes personalizados e especificar fontes padrão.
linktitle: Save OneNote as PDF Using Specified Fonts Subsystem
second_title: Aspose.Note Java API
title: Salvar OneNote como PDF usando o subsistema de fontes especificadas
url: /pt/java/onenote-document-saving/save-using-specified-fonts-subsystem/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salvar OneNote como PDF usando o Subsistema de Fontes Especificado

## Introdução

Em muitos cenários de negócios, você precisa **salvar OneNote como PDF** preservando a aparência exata das páginas originais. Aspose.Note for Java torna isso simples ao permitir que você controle o subsistema de fontes durante a conversão. Neste tutorial, percorreremos três maneiras práticas de **converter OneNote para PDF**, abordando como **carregar arquivos de fontes personalizados**, **especificar uma fonte padrão** e até **usar um fluxo de fonte** quando a fonte não está disponível na máquina de destino.

## Respostas Rápidas
- **O que significa “salvar OneNote como PDF”?** Converte um arquivo .one em PDF mantendo o layout e o estilo intactos.  
- **Qual API lida com fontes?** `DocumentFontsSubsystem` permite definir uma fonte padrão ou carregar um arquivo/fluxo de fonte personalizado.  
- **Preciso de uma licença para produção?** Sim, uma licença comercial do Aspose.Note é necessária para uso que não seja de avaliação.  
- **Posso converter vários arquivos em lote?** Absolutamente – basta percorrer a lógica de carregamento e salvamento do `Document`.  
- **Qual versão do Java é necessária?** Java 15 ou posterior (o exemplo usa JDK 15).

## O que é “salvar OneNote como PDF” com um subsistema de fontes?

Salvar OneNote como PDF com um subsistema de fontes significa que, durante o processo de conversão, o Aspose.Note substitui quaisquer glifos ausentes pela fonte que você fornece. Isso garante que o PDF tenha a mesma aparência em qualquer dispositivo, mesmo quando a fonte original não está instalada.

## Por que controlar o subsistema de fontes ao **converter OneNote para PDF**?

- **Marca consistente** – documentos corporativos mantêm a tipografia exata.  
- **Confiabilidade multiplataforma** – PDFs são renderizados da mesma forma no Windows, macOS, Linux e dispositivos móveis.  
- **Redução de erros** – avisos de fonte ausente desaparecem, produzindo saída limpa.

## Pré-requisitos

### 1. Java Development Kit (JDK)

Certifique-se de que o Java Development Kit (JDK) esteja instalado em seu sistema. Você pode baixá-lo [aqui](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html) se ainda não o fez.

### 2. Biblioteca Aspose.Note para Java

Faça o download e configure a biblioteca Aspose.Note para Java. Você pode baixá-la do [site](https://releases.aspose.com/note/java/).

## Importar Pacotes

Certifique-se de importar os pacotes necessários em seu projeto Java:

```java
import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
import com.aspose.note.fonts.DocumentFontsSubsystem;
import java.io.FileInputStream;
import java.io.IOException;
import java.io.InputStream;
import java.nio.file.Paths;
```

Agora vamos dividir cada exemplo em várias etapas para entender melhor o processo.

## Como **salvar OneNote como PDF** usando o Subsistema de Fontes de Documento com uma fonte padrão

### Etapa 1: Salvar usando o Subsistema de Fontes de Documento com Nome de Fonte Padrão

Esta etapa demonstra como **salvar OneNote como PDF** de maneira simples, especificando um nome de fonte padrão.

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

Nesta etapa:
- O documento OneNote é carregado usando Aspose.Note.
- A **fonte padrão** é especificada como **"Times New Roman"**.
- O documento é salvo em formato PDF com a fonte escolhida.

### Etapa 2: Salvar usando o Subsistema de Fontes de Documento com Fonte Padrão a partir de Arquivo

Aqui nós **carregamos um arquivo de fonte personalizado** e o usamos como fallback ao converter para PDF.

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

Pontos principais:
- O **arquivo de fonte personalizado** `geo_1.ttf` é **carregado do disco**.
- `usingDefaultFontFromFile` **especifica a fonte padrão a partir de um arquivo**, garantindo que o PDF use essa fonte quando a original estiver ausente.
- O PDF resultante preserva a aparência pretendida.

### Etapa 3: Salvar usando o Subsistema de Fontes de Documento com Fonte Padrão a partir de Fluxo

Às vezes a fonte pode estar armazenada em um banco de dados ou recebida pela rede. Este exemplo mostra como **usar um fluxo de fonte**.

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

O que acontece aqui:
- O arquivo de fonte é aberto como um **InputStream**, o que é útil quando a fonte reside em uma fonte que não é um arquivo.
- `usingDefaultFontFromStream` **usa um fluxo de fonte** para definir a fonte de fallback.
- O arquivo OneNote é salvo como PDF com a fonte baseada em fluxo.

## Problemas Comuns e Soluções

| Problema | Por que acontece | Como corrigir |
|----------|------------------|---------------|
| **Avisos de fonte ausente** | O arquivo .one de origem referencia uma fonte que não está presente na máquina. | Forneça uma fonte padrão via `usingDefaultFont`, `usingDefaultFontFromFile` ou `usingDefaultFontFromStream`. |
| **Arquivo de fonte personalizada não encontrado** | Caminho incorreto para o arquivo `.ttf`. | Use caminhos absolutos ou verifique o caminho relativo a partir do diretório de trabalho. |
| **Fluxo não fechado** | Exceção ocorre antes de `close()` ser chamado. | Use try‑with‑resources (`try (InputStream stream = ...) { ... }`) para fechamento automático. |

## Perguntas Frequentes

**Q: Posso especificar fontes diferentes para diferentes partes do documento?**  
A: Sim, você pode aplicar configurações de fonte personalizadas a elementos de texto rico individuais usando a classe `Font` no Aspose.Note.

**Q: O Aspose.Note é compatível com todas as versões do OneNote?**  
A: O Aspose.Note suporta arquivos OneNote das versões recentes de desktop e mobile, garantindo ampla compatibilidade.

**Q: Como posso lidar com fontes ausentes ao salvar documentos?**  
A: Use os métodos do subsistema de fontes mostrados acima (`usingDefaultFont`, `usingDefaultFontFromFile`, `usingDefaultFontFromStream`) para fornecer um fallback.

**Q: Posso personalizar propriedades da fonte, como tamanho e estilo?**  
A: Absolutamente – a API permite definir tamanho, estilo, cor e outros atributos por execução (per‑run).

**Q: Existe uma versão de avaliação disponível para o Aspose.Note para Java?**  
A: Sim, uma avaliação gratuita pode ser baixada do site da Aspose.

## Conclusão

Neste tutorial aprendemos como **salvar OneNote como PDF** enquanto controlamos o subsistema de fontes em Java com Aspose.Note. Seguindo as três abordagens — especificar um nome de fonte padrão, carregar um arquivo de fonte personalizado ou usar um fluxo de fonte — você pode garantir uma representação consistente das fontes em todas as plataformas ao exportar ou salvar seus documentos OneNote.

---

**Última atualização:** 2025-12-18  
**Testado com:** Aspose.Note for Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}