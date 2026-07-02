---
date: 2026-01-10
description: Aprenda como obter a hora da última modificação e recuperar as revisões
  de páginas do OneNote usando Aspose.Note para Java. Integre isso em seus aplicativos
  Java para uma gestão de documentos eficiente.
linktitle: Get Revisions of Pages in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Como obter a hora da última modificação das páginas do OneNote – Aspose.Note
url: /pt/java/onenote-page-manipulation/get-revisions-of-pages/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Obter Revisões de Páginas no OneNote - Aspose.Note

## Introdução

Neste tutorial, você **obterá o horário da última modificação** das páginas dentro de um documento OneNote e explorará como recuperar o histórico completo de revisões usando Aspose.Note for Java. Seja construindo um sistema de gerenciamento de documentos, auditando alterações ou simplesmente precisando exibir quando uma página foi editada pela última vez, este guia mostra exatamente como extrair essas informações programaticamente.

## Respostas Rápidas
- **O que `get last modified time` retorna?** O carimbo de data/hora da edição mais recente em uma página do OneNote.  
- **Qual classe fornece o histórico de revisões?** `PageHistory` via `Document.getPageHistory(Page)`.  
- **Preciso de licença para este recurso?** Sim, uma licença válida do Aspose.Note é necessária para uso em produção.  
- **Qual versão do Java é suportada?** Java 8 ou superior (JDK 8+).  
- **Posso filtrar revisões por autor?** Você pode ler a propriedade `Author` de cada objeto `Page` e aplicar seu próprio filtro.

## O que é “get last modified time” no OneNote?

O **horário da última modificação** é um campo de metadados armazenado em cada página que registra quando a página foi alterada pela última vez. Aspose.Note expõe esse valor através do método `Page.getLastModifiedTime()`, facilitando a exibição ou registro das datas de alteração.

## Por que recuperar revisões de página?

- **Rastreios de auditoria:** Mantenha um registro de quem alterou o quê e quando.  
- **Comparação de versões:** Crie recursos que comparem duas revisões lado a lado.  
- **Insights de colaboração de usuários:** Entenda os padrões de edição em blocos de notas compartilhados.  

## Pré-requisitos

Antes de começar, certifique-se de que você tem o seguinte:

### Java Development Kit (JDK) Instalado
Instale o JDK 8 ou posterior a partir do site da Oracle ou do seu gerenciador de pacotes preferido.

### Biblioteca Aspose.Note for Java
Baixe a biblioteca do site oficial. Você pode encontrar o link de download **[aqui](https://releases.aspose.com/note/java/)**. Siga as instruções de instalação na documentação **[aqui](https://reference.aspose.com/note/java/)**.

## Importar Pacotes

Para começar, importe os pacotes necessários ao seu projeto Java. Esses pacotes permitirão que você aproveite a funcionalidade fornecida pelo Aspose.Note for Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

Agora, vamos dividir o código de exemplo fornecido em várias etapas para entender cada componente e sua funcionalidade.

## Como Obter o Horário da Última Modificação de uma Página OneNote

### Etapa 1: Definir o Diretório do Documento
Defina o diretório onde seu documento OneNote está localizado.

```java
String dataDir = "Your Document Directory";
```

### Etapa 2: Carregar o Documento
Carregue o documento OneNote no Aspose.Note.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

### Etapa 3: Obter a Primeira Página
Recupere a primeira página do documento.

```java
Page firstPage = doc.getFirstChild();
```

### Etapa 4: Obter Revisões da Página
Obtenha o histórico de revisões da página.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

### Etapa 5: Percorrer as Revisões da Página
Itere pela lista de revisões da página e recupere informações relevantes, incluindo o **horário da última modificação**.

```java
for (Page pageRevision : revisions) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

## Problemas Comuns e Soluções
- **`PageHistory` nulo:** Certifique-se de que o documento realmente contém revisões; caso contrário, `getPageHistory` pode retornar `null`.  
- **Diferenças de fuso horário:** `getLastModifiedTime()` retorna um `java.util.Date` no fuso horário padrão do sistema. Converta para UTC se necessário.  
- **Licença não carregada:** Sem uma licença válida, o Aspose.Note pode operar em modo de avaliação, limitando o número de páginas processadas.

## Perguntas Frequentes

### Q1: Posso usar Aspose.Note for Java para criar novos documentos OneNote?
R1: Sim, o Aspose.Note for Java oferece suporte abrangente para criar, ler e manipular documentos OneNote programaticamente.

### Q2: O Aspose.Note for Java é compatível com diferentes versões de arquivos OneNote?
R2: Sim, o Aspose.Note for Java suporta várias versões de arquivos Microsoft OneNote, garantindo compatibilidade em diferentes ambientes.

### Q3: Posso personalizar o formato de saída ao exportar documentos OneNote?
R3: Absolutamente, o Aspose.Note for Java oferece flexibilidade ao exportar documentos OneNote para diferentes formatos, como PDF, HTML e imagens, com opções de personalização.

### Q4: O Aspose.Note for Java requer licença para uso comercial?
R4: Sim, uma licença válida é necessária para uso comercial do Aspose.Note for Java. Você pode obter uma licença no site da Aspose.

### Q5: Onde posso buscar assistência se encontrar problemas ou tiver dúvidas sobre o Aspose.Note for Java?
R5: Para suporte e assistência, você pode visitar o fórum Aspose.Note **[aqui](https://forum.aspose.com/c/note/28)**, onde pode fazer perguntas, compartilhar experiências e interagir com outros usuários e especialistas.

---

**Última atualização:** 2026-01-10  
**Testado com:** Aspose.Note for Java 23.12 (latest at time of writing)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}