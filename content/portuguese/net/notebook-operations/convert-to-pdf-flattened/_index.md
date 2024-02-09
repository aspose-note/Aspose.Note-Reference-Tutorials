---
title: Converter cadernos em PDF (achatado) no Aspose Note .NET
linktitle: Converter cadernos em PDF (achatado) no Aspose Note .NET
second_title: API Aspose.Note .NET
description: Aprenda como converter blocos de anotações do OneNote em PDFs nivelados sem esforço usando Aspose.Note para .NET. Preserve seu conteúdo perfeitamente.
type: docs
weight: 15
url: /pt/net/notebook-operations/convert-to-pdf-flattened/
---
## Introdução

Você deseja converter seus blocos de anotações do OneNote em PDFs nivelados usando o Aspose Note .NET? Você está no lugar certo! Neste tutorial, percorreremos o processo passo a passo.

## Pré-requisitos

Antes de começarmos, certifique-se de ter o seguinte:

1.  Aspose.Note for .NET: Certifique-se de ter baixado e instalado o Aspose.Note for .NET. Se não, você pode obtê-lo em[aqui](https://releases.aspose.com/note/net/).
2. Visual Studio: você precisará do Visual Studio instalado em seu sistema para codificação e compilação.
3. Bloco de anotações do OneNote: tenha um bloco de anotações do OneNote pronto que você deseja converter em PDF.

## Importar namespaces

Vamos começar importando os namespaces necessários em seu código C#:

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Collections.Generic;
```

## Etapa 1: carregar o bloco de anotações do OneNote

```csharp
// O caminho para o diretório de documentos.
string dataDir = "Your Document Directory";

// Carregar um bloco de anotações do OneNote
var notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

 Nesta etapa, carregamos o OneNote Notebook usando o`Notebook` classe fornecida por Aspose.Note.

## Passo 2: Converter para PDF com Achatamento

```csharp
// Salve o caderno como PDF com nivelamento
dataDir = dataDir + "ConvertToPDFAsFlattened_out.pdf";
notebook.Save(
    dataDir,
    new NotebookPdfSaveOptions
    {
        Flatten = true
    }); 
```

 Aqui, salvamos o caderno carregado como PDF com o`Flatten` propriedade definida como`true`. Esta propriedade nivela todo o conteúdo, incluindo anotações e imagens, no PDF.

## Etapa 3: Imprimir mensagem de sucesso

```csharp
Console.WriteLine("\nNoteBook document converted to PDF as flattened successfully.\nFile saved at " + dataDir);
```

Por fim, imprimimos uma mensagem de sucesso junto com o caminho onde o PDF foi salvo.

## Conclusão

Parabéns! Você converteu com sucesso seu OneNote Notebook em um PDF nivelado usando Aspose.Note para .NET. Este processo garante que todo o seu conteúdo seja preservado com precisão no formato PDF, facilitando o compartilhamento e a distribuição.

## Perguntas frequentes

### P1: Posso preservar elementos interativos no PDF?

A1: Aspose.Note nivela o conteúdo, incluindo elementos interativos como caixas de seleção ou campos de formulário, no PDF, tornando-os estáticos.

### Q2: O Aspose.Note oferece suporte à conversão de notebooks para outros formatos?

A2: Sim, Aspose.Note suporta a conversão de cadernos para vários formatos, como PDF, HTML, imagem e muito mais.

### P3: Posso personalizar as opções de conversão?

A3: Com certeza! Aspose.Note oferece amplas opções de personalização durante o processo de conversão, permitindo personalizar a saída de acordo com suas necessidades.

### Q4: Existe uma versão de teste disponível?

 A4: Sim, você pode obter uma avaliação gratuita do Aspose.Note em[aqui](https://releases.aspose.com/).

### P5: Onde posso obter suporte se encontrar algum problema?

 A5: Você pode buscar suporte na comunidade Aspose em[Fóruns Aspose.Note](https://forum.aspose.com/c/note/28).