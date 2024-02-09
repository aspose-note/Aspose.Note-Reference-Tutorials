---
title: Gerar documento a partir de modelo em Aspose.Note
linktitle: Gerar documento a partir de modelo em Aspose.Note
second_title: API Aspose.Note .NET
description: Gere documentos dinâmicos sem esforço com Aspose.Note for .NET. Siga nosso guia passo a passo para criação de documentos personalizados e baseados em dados.
type: docs
weight: 18
url: /pt/net/text-manipulation/generate-document-from-template/
---
## Introdução
No cenário em constante evolução da criação de documentos, Aspose.Note for .NET se destaca como uma ferramenta poderosa para gerar documentos dinâmicos sem esforço. Esteja você lidando com relatórios, faturas ou documentos personalizados, este tutorial irá guiá-lo através do processo de geração de um documento a partir de um modelo usando Aspose.Note para .NET.
## Pré-requisitos
Antes de mergulhar no guia passo a passo, certifique-se de ter os seguintes pré-requisitos em vigor:
1.  Biblioteca Aspose.Note for .NET: Baixe e instale a biblioteca do[Documentação do Aspose.Note para .NET](https://reference.aspose.com/note/net/).
2. Modelo de documento: prepare um documento modelo no formato OneNote (com extensão .one). Isso servirá de base para seu documento gerado dinamicamente.
## Importar namespaces
Certifique-se de incluir os namespaces necessários em seu projeto:
```csharp
    using System;
    using System.Collections.Generic;
    using System.IO;
```
Agora, vamos detalhar cada etapa do guia.
## Etapa 1: Defina seu diretório de documentos
```csharp
string dataDir = "Your Document Directory";
```
Substitua “Seu diretório de documentos” pelo caminho onde você deseja salvar o documento gerado.
## Etapa 2: crie um dicionário com valores de substituição
```csharp
var templateData = new Dictionary<string, string>
{
    { "Company", "Atlas Shrugged Ltd" },
    { "CandidateName", "John Galt" },
    { "JobTitle", "Chief Entrepreneur Officer" },
    { "Department", "Sales" },
    { "Salary", "123456 USD" },
    { "Vacation", "30" },
    { "StartDate", "29 Feb 2024" },
    { "YourName", "Ayn Rand" }
};
```
Defina um dicionário onde as chaves sejam espaços reservados em seu modelo e os valores sejam os dados pelos quais você deseja substituí-los.

## Etapa 3: carregar o documento modelo
```csharp
var templateDocument = new Document(Path.Combine(dataDir, "JobOffer.one"));
```
Carregue seu documento modelo do OneNote no Aspose.Note.

## Etapa 4: substituir palavras de modelo por dados dinâmicos
```csharp
foreach (var paragraph in templateDocument.GetChildNodes<RichText>())
{
    foreach (var replacement in templateData)
    {
        paragraph.Replace($"${{{replacement.Key}}}", replacement.Value);
    }
}
```
Itere cada parágrafo do modelo, substituindo espaços reservados por dados dinâmicos.

## Etapa 5: salve o documento gerado
```csharp
templateDocument.Save(Path.Combine(dataDir, "JobOffer_out.one"));
```
Salve o documento gerado dinamicamente no diretório especificado.

## Conclusão
Parabéns! Você gerou com sucesso um documento dinâmico usando Aspose.Note for .NET. Este processo abre um mundo de possibilidades para a criação contínua de documentos personalizados e baseados em dados.

## perguntas frequentes
### Posso usar o Aspose.Note for .NET com outros formatos de documentos?
Sim, o Aspose.Note for .NET lida principalmente com documentos do OneNote, mas o Aspose fornece várias bibliotecas para diferentes formatos.
### Existe uma avaliação gratuita disponível para Aspose.Note for .NET?
 Sim, você pode explorar os recursos do Aspose.Note for .NET com uma avaliação gratuita. Visita[aqui](https://releases.aspose.com/) Para maiores informações.
### Como posso obter suporte para Aspose.Note para .NET?
 Visite a[Fórum Aspose.Note para .NET](https://forum.aspose.com/c/note/28) para obter assistência da comunidade e de especialistas.
### As licenças temporárias estão disponíveis para Aspose.Note for .NET?
 Sim, você pode obter uma licença temporária[aqui](https://purchase.aspose.com/temporary-license/) para fins de teste e avaliação.
### Onde posso encontrar documentação abrangente para Aspose.Note for .NET?
 Consulte o[documentação](https://reference.aspose.com/note/net/) para obter informações detalhadas sobre o uso do Aspose.Note for .NET.