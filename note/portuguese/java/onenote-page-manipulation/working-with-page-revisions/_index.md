---
date: 2026-01-15
description: Aprenda como rastrear alterações no OneNote e gerenciar revisões de páginas
  em documentos do OneNote usando Aspose.Note para Java. Inclui um exemplo de resumo
  de revisões e como modificar a data da revisão.
linktitle: Working with Page Revisions in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Rastrear alterações no OneNote – Gerenciar revisões de página com Aspose.Note
url: /pt/java/onenote-page-manipulation/working-with-page-revisions/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Trabalhando com Revisões de Página no OneNote - Aspose.Note

## Introdução

OneNote é uma ferramenta poderosa para organizar notas, e quando você precisa **track changes onenote**, gerenciar revisões de página se torna essencial para uma colaboração eficaz. Com Aspose.Note for Java, você pode manipular revisões programaticamente, visualizar quem editou uma página e até ajustar timestamps. Este tutorial orienta você passo a passo, desde o carregamento de um documento até a atualização do resumo de revisão.

## Respostas Rápidas
- **What does “track changes onenote” mean?** Refere‑se ao monitoramento de quem editou uma página do OneNote e quando.
- **Which library is required?** Aspose.Note for Java.
- **Can I change the author or date of a revision?** Sim, usando a API RevisionSummary (`modify revision date`).
- **Do I need a OneNote file beforehand?** Sim, é necessário um arquivo `.one` de exemplo.
- **Is a license needed for production?** Uma licença válida do Aspose.Note é necessária para uso comercial.

## O que é um exemplo de resumo de revisão?
Um *revision summary* fornece metadados sobre as alterações mais recentes em uma página — nome do autor, hora da última modificação e outros detalhes. Neste guia, recuperaremos e exibiremos essas informações e, em seguida, mostraremos como **modify revision date**.

## Por que rastrear alterações onenote com Aspose.Note?
- **Collaboration:** Veja rapidamente quem fez as últimas edições.
- **Auditing:** Mantenha um histórico confiável de alterações para conformidade.
- **Automation:** Integre o gerenciamento de revisões em serviços de back‑end ou ferramentas de migração.

## Pré‑requisitos

### Ambiente de Desenvolvimento Java
Certifique‑se de que o Java Development Kit (JDK) esteja instalado em seu sistema.

### Biblioteca Aspose.Note for Java
Faça o download e instale a biblioteca Aspose.Note for Java a partir de [here](https://releases.aspose.com/note/java/).

### Documento OneNote
Tenha um documento OneNote de exemplo pronto para fins de teste.

## Importar Pacotes

No seu projeto Java, importe os pacotes necessários para trabalhar com Aspose.Note for Java.

```java
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.RevisionSummary;
import java.io.IOException;
import java.util.Calendar;
```

Vamos dividir o exemplo fornecido em várias etapas para uma compreensão clara.

## Etapa 1: Carregar Documento OneNote

Primeiro, carregue o documento OneNote e obtenha a primeira página filha.

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
Page page = document.getFirstChild();
```

## Etapa 2: Ler Resumo de Revisão da Página

Leia o resumo de revisão de conteúdo da página. Este é o **revision summary example** que mostra quem editou a página por último.

```java
RevisionSummary pageRevisionInfo = page.getPageContentRevisionSummary();
System.out.println(String.format("Author:\t%s\nModified:\t%s",
        pageRevisionInfo.getAuthorMostRecent(),
        pageRevisionInfo.getLastModifiedTime().toString()));
```

## Etapa 3: Atualizar Resumo de Revisão da Página

Atualize o resumo de revisão da página com um novo autor e uma nova data de modificação. Isso demonstra como **modify revision date** programaticamente.

```java
pageRevisionInfo.setAuthorMostRecent("New Author");
Calendar modifiedDate = Calendar.getInstance();
pageRevisionInfo.setLastModifiedTime(modifiedDate.getTime());
document.save(dataDir + "WorkingWithPageRevisions_out.one");
```

## Conclusão

Gerenciar revisões de página em documentos OneNote programaticamente pode ser simplificado com Aspose.Note for Java. Seguindo as etapas descritas neste tutorial, você pode efetivamente **track changes onenote**, visualizar detalhes da revisão e até **modify revision date** para adequar ao seu fluxo de trabalho.

## Perguntas Frequentes

### Q1: Posso usar Aspose.Note for Java com outras bibliotecas Java?
A: Sim, Aspose.Note for Java pode ser integrado com outras bibliotecas Java para melhorar a funcionalidade.

### Q2: O Aspose.Note for Java suporta todas as versões de documentos OneNote?
A: Aspose.Note for Java suporta várias versões de documentos OneNote, incluindo versões mais antigas.

### Q3: O Aspose.Note for Java é adequado para aplicações de nível empresarial?
A: Absolutamente, Aspose.Note for Java foi projetado para atender às necessidades de aplicações de nível empresarial com recursos robustos e escalabilidade.

### Q4: Posso personalizar revisões de página com Aspose.Note for Java?
A: Sim, você pode personalizar revisões de página de acordo com seus requisitos usando Aspose.Note for Java.

### Q5: Onde posso obter suporte para Aspose.Note for Java?
A: Você pode obter suporte para Aspose.Note for Java no [Aspose.Note forum](https://forum.aspose.com/c/note/28).

---

**Última atualização:** 2026-01-15  
**Testado com:** Aspose.Note for Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}