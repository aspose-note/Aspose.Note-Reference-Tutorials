---
title: Abra e feche projetos com tags em Aspose.Note
linktitle: Abra e feche projetos com tags em Aspose.Note
second_title: API Aspose.Note .NET
description: Aprenda como manipular arquivos do Microsoft OneNote programaticamente usando Aspose.Note for .NET. Abra e feche projetos com tags de forma eficiente.
weight: 15
url: /pt/net/tag-management/open-close-projects-tags/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Abra e feche projetos com tags em Aspose.Note

## Introdução

Neste tutorial, aprenderemos como usar Aspose.Note for .NET para abrir e fechar projetos com tags. Aspose.Note é uma API poderosa que permite aos desenvolvedores trabalhar com arquivos do Microsoft OneNote de forma programática, permitindo tarefas como manipulação de texto, imagens e tags nos documentos.

## Pré-requisitos

Antes de começarmos, certifique-se de ter os seguintes pré-requisitos configurados:

## Importar namespaces

```csharp
using System.IO;
using System.Linq;
```

Agora vamos dividir cada exemplo em várias etapas:

## Etapa 1: carregue o documento

Primeiro, precisamos carregar o documento no Aspose.Note.

```csharp
string dataDir = "Your Document Directory";
var oneFile = new Document(Path.Combine(dataDir, "ProjectNotes.one"));
```

## Etapa 2: fechar os itens do projeto C

Agora, vamos fechar todos os itens da caixa de seleção relacionados ao ‘Projeto C’.

```csharp
foreach (var node in oneFile.GetChildNodes<ITaggable>())
{
    foreach (var checkBox in node.Tags.OfType<CheckBox>())
    {
        if (checkBox.Label.Contains("Project C") && !checkBox.Checked)
        {
            checkBox.SetCompleted();
        }
    }
}
```

## Etapa 3: Salvar as notas do projeto C fechado

Salve o documento modificado com os itens fechados do 'Projeto C'.

```csharp
oneFile.Save("Path to save the closed Project C notes");
```

## Etapa 4: abra os itens do projeto C

A seguir, vamos abrir todos os itens da caixa de seleção relacionados ao ‘Projeto C’.

```csharp
var oneFile = new Document("Path to the closed Project C notes");

foreach (var node in oneFile.GetChildNodes<ITaggable>())
{
    foreach (var checkBox in node.Tags.OfType<CheckBox>())
    {
        if (checkBox.Label.Contains("Project C") && checkBox.Checked)
        {
            checkBox.SetOpen();
        }
    }
}
```

## Etapa 5: salve as notas do projeto C aberto

Salve o documento modificado com os itens do 'Projeto C' abertos.

```csharp
oneFile.Save(Path.Combine(dataDir, "ProjectNoteWithOpenProjectC.one"));
```

Agora você aprendeu como abrir e fechar projetos com tags no Aspose.Note usando .NET.

## Conclusão

Aspose.Note for .NET fornece uma maneira conveniente de manipular documentos do OneNote programaticamente. Seguindo este tutorial, você pode gerenciar seus projetos com eficiência abrindo e fechando itens usando tags.

## Perguntas frequentes

### Q1: O Aspose.Note é compatível com todas as versões do OneNote?

A1: Aspose.Note oferece suporte ao Microsoft OneNote 2010 e versões mais recentes.

### Q2: Posso usar Aspose.Note para projetos comerciais?

 A2: Sim, você pode usar Aspose.Note para projetos pessoais e comerciais. Visita[aqui](https://purchase.aspose.com/buy) para comprar uma licença.

### Q3: O Aspose.Note oferece uma avaliação gratuita?

 A3: Sim, você pode obter uma avaliação gratuita[aqui](https://releases.aspose.com/).

### Q4: Onde posso encontrar documentação para Aspose.Note?

 A4: Você pode encontrar a documentação[aqui](https://reference.aspose.com/note/net/).

### Q5: Onde posso obter suporte para Aspose.Note?

 A5: Para suporte, você pode visitar o Aspose.Note[fórum](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
