---
title: Recuperar lista de marcadores ou números no texto Aspose.Note
linktitle: Recuperar lista de marcadores ou números no texto Aspose.Note
second_title: API Aspose.Note .NET
description: Desbloqueie o potencial do Aspose.Note para .NET com nosso guia passo a passo sobre como recuperar listas de marcadores ou números. Eleve suas habilidades de manipulação de documentos do OneNote!
type: docs
weight: 23
url: /pt/net/text-manipulation/retrieve-bullet-number-list/
---
## Introdução
Bem-vindo ao mundo do Aspose.Note for .NET, uma biblioteca robusta e versátil que permite aos desenvolvedores lidar com a manipulação de documentos do OneNote sem esforço. Neste tutorial, nos aprofundaremos no processo de recuperação de listas de marcadores ou números usando Aspose.Note para .NET. Quer você seja um desenvolvedor experiente ou um entusiasta de codificação, este guia irá equipá-lo com o conhecimento para navegar pelas complexidades de trabalhar com listas no Aspose.Note.
## Pré-requisitos
Antes de embarcarmos nesta jornada de codificação, certifique-se de ter os seguintes pré-requisitos em vigor:
-  Aspose.Note para .NET: Certifique-se de ter a biblioteca Aspose.Note instalada. Caso contrário, você pode baixá-lo no[Documentação do Aspose.Note para .NET](https://reference.aspose.com/note/net/).
- Ambiente de Desenvolvimento: Tenha um ambiente de desenvolvimento funcional, de preferência Microsoft Visual Studio, configurado em sua máquina.
- Conhecimento básico de C#: Familiarize-se com C#, pois este tutorial foi escrito nesta linguagem.
## Importar namespaces
Para interagir com o Aspose.Note for .NET, você precisa importar os namespaces necessários para o seu projeto. Inclua os seguintes namespaces no início do seu código:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
```
Agora, vamos detalhar o processo de recuperação de listas de marcadores ou números passo a passo:
## Etapa 1: defina seu diretório de documentos
```csharp
// O caminho para o diretório de documentos.
string dataDir = "Your Document Directory";
```
 Substituir`"Your Document Directory"` com o caminho real onde seu documento Aspose.Note está localizado.
## Etapa 2: carregue o documento
```csharp
// Carregue o documento no Aspose.Note.
Document oneFile = new Document(dataDir + "ApplyNumberingOnText.one");
```
 Certifique-se de substituir`"ApplyNumberingOnText.one"` com o nome do seu documento específico do OneNote.
## Etapa 3: recuperar a coleção de nós
```csharp
// Recuperar uma coleção de nós do elemento de contorno.
IList<OutlineElement> nodes = oneFile.GetChildNodes<OutlineElement>();
```
Esta etapa recupera uma coleção de nós de estrutura de tópicos do documento carregado.
## Etapa 4: iterar em cada nó
```csharp
// Itere em cada nó.
foreach (OutlineElement node in nodes)
{
    if (node.NumberList != null)
    {
        NumberList list = node.NumberList;
        // Continue para as próximas etapas...
    }
}
```
Este loop garante que estamos lidando apenas com nós que contêm uma lista numérica.
## Etapa 5: recuperar informações da fonte
```csharp
// Recuperar nome da fonte
Console.WriteLine("Font Name: " + list.Font);
// Recuperar comprimento da fonte
Console.WriteLine("Font Length: " + list.Font.Length);
// Recuperar tamanho da fonte
Console.WriteLine("Font Size: " + list.FontSize);
// Recuperar cor da fonte
Console.WriteLine("Font Color: " + list.FontColor);
// Recuperar formato
Console.WriteLine("Font format: " + list.Format);
// Marque negrito
Console.WriteLine("Is bold: " + list.IsBold);
// Verifique itálico
Console.WriteLine("Is italic: " + list.IsItalic);
Console.WriteLine();
```
Essas linhas de código extraem várias informações relacionadas às fontes da lista de números.
## Conclusão
 Parabéns! Você aprendeu com sucesso como recuperar listas de marcadores ou números usando Aspose.Note para .NET. À medida que você continua sua exploração, consulte o[documentação](https://reference.aspose.com/note/net/) para obter insights e funcionalidades mais aprofundados.
## Perguntas frequentes
### Posso usar o Aspose.Note for .NET com outras linguagens de programação?
Aspose.Note oferece suporte principalmente a .NET, mas existem outras versões da biblioteca adaptadas para diferentes plataformas e idiomas.
### O Aspose.Note é compatível com os formatos mais recentes do OneNote?
Sim, o Aspose.Note oferece suporte a uma ampla variedade de formatos do OneNote, garantindo compatibilidade com as versões mais recentes.
### Como posso obter uma licença temporária para Aspose.Note?
 Visita[esse link](https://purchase.aspose.com/temporary-license/) para obter uma licença temporária para fins de avaliação.
### Quais opções de suporte estão disponíveis para usuários do Aspose.Note?
Você pode explorar e procurar ajuda no[Fórum Aspose.Note](https://forum.aspose.com/c/note/28) para quaisquer dúvidas ou problemas que você possa encontrar.
### Existe uma versão de teste gratuita do Aspose.Note para .NET?
 Sim, você pode acessar a versão de avaliação gratuita do Aspose.Note for .NET[aqui](https://releases.aspose.com/).