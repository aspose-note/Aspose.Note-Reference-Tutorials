---
title: Salvar usando fontes especificadas em Aspose.Note
linktitle: Salvar usando fontes especificadas em Aspose.Note
second_title: API Aspose.Note .NET
description: Aprenda como salvar documentos com fontes especificadas no Aspose.Note for .NET. Personalize facilmente as configurações de fonte para uma formatação consistente de documentos.
weight: 28
url: /pt/net/loading-and-saving-operations/save-using-specified-fonts/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salvar usando fontes especificadas em Aspose.Note

## Introdução

Neste tutorial, aprenderemos como salvar documentos usando fontes especificadas no Aspose.Note for .NET. Exploraremos diferentes métodos para conseguir isso, passo a passo.

## Pré-requisitos

Antes de começarmos, certifique-se de ter o seguinte:

1.  Aspose.Note para .NET: Certifique-se de ter instalado o Aspose.Note para .NET. Você pode baixá-lo em[aqui](https://releases.aspose.com/note/net/).

2. Ambiente de desenvolvimento: você precisa de um ambiente de desenvolvimento configurado para desenvolvimento .NET.

## Importar namespaces

Primeiro, vamos importar os namespaces necessários:

```csharp
using System;
using System.IO;

using Aspose.Note.Fonts;
using Aspose.Note.Saving;

```

## Etapa 1: Salvar com nome de fonte padrão

Nesta etapa, salvaremos um documento usando um nome de fonte padrão especificado.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName()
{
    // O caminho para o diretório de documentos.
    string dataDir = "Your Document Directory";

    // Carregue o documento no Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Salve o documento como PDF com a fonte padrão especificada.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFont("Times New Roman")
                          });
}
```

## Etapa 2: Salvar com fonte padrão do arquivo

A seguir, vamos salvar um documento usando uma fonte padrão carregada de um arquivo.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile()
{
    // O caminho para o diretório de documentos.
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    // Carregue o documento no Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Salve o documento como PDF com a fonte padrão carregada do arquivo.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromFile(fontFile)
                          });
}
```

## Etapa 3: Salvar com fonte padrão do stream

Por último, vamos salvar um documento usando uma fonte padrão carregada de um stream.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream()
{
    // O caminho para o diretório de documentos.
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    // Carregue o documento no Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Salve o documento como PDF com a fonte padrão carregada do stream.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf";

    using (var stream = File.Open(fontFile, FileMode.Open, FileAccess.Read, FileShare.Read))
    {
        oneFile.Save(dataDir, new PdfSaveOptions()
                              {
                                  FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromStream(stream)
                              });
    }
}
```

## Conclusão

Neste tutorial, exploramos como salvar documentos usando fontes especificadas no Aspose.Note for .NET. Seguindo essas etapas, você pode personalizar as configurações de fonte de acordo com suas necessidades, garantindo que seus documentos sejam formatados conforme desejado.

## Perguntas frequentes

### Q1: Posso usar qualquer fonte para salvar documentos no Aspose.Note?

A1: Sim, você pode especificar qualquer fonte para salvar documentos. Apenas certifique-se de que o arquivo da fonte esteja acessível e carregado corretamente.

### Q2: O Aspose.Note é compatível com diferentes formatos de documento?

A2: Aspose.Note funciona principalmente com documentos do OneNote, mas oferece opções para salvar em vários formatos, incluindo PDF.

### P3: Como posso lidar com fontes ausentes ao salvar documentos?

A3: Aspose.Note oferece opções para usar fontes padrão caso a fonte especificada esteja faltando, garantindo uma formatação consistente do documento.

### Q4: O Aspose.Note oferece suporte à incorporação de fontes em documentos de saída?

A4: Sim, Aspose.Note permite incorporar fontes para garantir a portabilidade do documento e renderização consistente em diferentes plataformas.

### Q5: Onde posso obter mais assistência com Aspose.Note?

 A5: Para obter mais assistência ou suporte técnico, você pode visitar o[Fórum Aspose.Note](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
