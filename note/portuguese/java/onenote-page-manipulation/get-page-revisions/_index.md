---
date: 2026-01-10
description: Aprenda o tutorial de revisões de página do Aspose.Note para Java – recupere
  revisões de página do OneNote programaticamente usando Aspose.Note. Siga nosso guia
  passo a passo.
linktitle: Get Page Revisions in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Tutorial de revisões de página do aspose.note – Obtenha revisões de página
  no OneNote
url: /pt/java/onenote-page-manipulation/get-page-revisions/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Obter Revisões de Página no OneNote - Aspose.Note

OneNote é uma plataforma poderosa de tomada de notas, e quando você precisa auditar alterações, o **aspose.note page revisions tutorial** mostra exatamente como obter o histórico de revisões com apenas algumas linhas de código Java. Neste guia, percorreremos tudo o que você precisa — desde a configuração do ambiente até a impressão dos detalhes de cada revisão — para que você possa rastrear edições, contribuições de autores e carimbos de data/hora sem esforço.

## Respostas Rápidas
- **O que o tutorial cobre?** Recuperar o histórico de revisões de página de um arquivo OneNote usando Aspose.Note para Java.  
- **Qual versão da biblioteca é necessária?** Qualquer versão recente do Aspose.Note para Java que suporte `LoadOptions.setLoadHistory`.  
- **Preciso de uma licença?** Uma licença de avaliação temporária funciona para testes; uma licença comercial é necessária para produção.  
- **Posso modificar revisões?** A API é somente leitura para revisões; você pode apenas recuperá‑las.  
- **Quais são os pré-requisitos principais?** Java JDK, Aspose.Note para Java e um documento OneNote com dados de revisão.

## O é o “aspose.note page revisions tutorial”?
O tutorial demonstra como acessar programaticamente as versões históricas de uma página OneNote. Cada revisão contém metadados como autor, hora de criação e hora de modificação, permitindo que você crie trilhas de auditoria ou recursos de registro de alterações dentro de suas aplicações.

## Por que usar Aspose.Note para rastreamento de revisões de página?
- **No UI dependency** – Sem dependência de UI – funciona totalmente em código, perfeito para serviços de backend.  
- **Cross‑platform** – Multiplataforma – Java roda no Windows, Linux e macOS.  
- **Full control** – Controle total – recupere todas as propriedades de revisão sem abrir o OneNote manualmente.  
- **Performance** – Desempenho – o carregamento do histórico é otimizado, então até cadernos grandes são processados rapidamente.

## Pré-requisitos

### 1. Java Development Kit (JDK)
Certifique‑se de que um JDK (8 ou superior) esteja instalado e que `JAVA_HOME` esteja configurado.

### 2. Aspose.Note for Java
Baixe a biblioteca a partir do [download link](https://releases.aspose.com/note/java/).

### 3. Documento OneNote de Exemplo
Crie ou obtenha um arquivo OneNote (por exemplo, `Sample1.one`) que contenha páginas com histórico de revisões.

## Importar Pacotes
Primeiro, importe as classes necessárias do Aspose.Note.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## Implementação Passo a Passo

### Etapa 1: Configurar Diretório do Documento
Defina a pasta onde seu arquivo OneNote está localizado.

```java
String dataDir = "Your Document Directory";
```

### Etapa 2: Carregar Documento OneNote com Histórico Ativado
Habilite a flag `LoadOptions` para obter os dados de revisão.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

### Etapa 3: Obter a Primeira Página
Recupere o objeto da primeira página; este será o ponto de referência para obter seu histórico.

```java
Page firstPage = document.getFirstChild();
```

### Etapa 4: Iterar pelas Revisões da Página
Percorra cada revisão e imprima metadados úteis, como carimbos de data/hora, título, nível e autor.

```java
for (Page pageRevision : document.getPageHistory(firstPage)) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

> **Dica profissional:** Se precisar filtrar revisões por um autor específico ou intervalo de datas, basta adicionar verificações condicionais dentro do loop `for`.

## Problemas Comuns & Soluções
- **Nenhuma revisão retornada:** Verifique se `loadOptions.setLoadHistory(true)` é chamado antes de carregar o documento.  
- **Autor ou título nulo:** Algumas versões mais antigas do OneNote podem não armazenar esses campos; trate valores `null` de forma adequada.  
- **Atraso de desempenho em cadernos grandes:** Carregue apenas as seções necessárias ou aumente o tamanho do heap da JVM.

## Perguntas Frequentes

**Q1: Posso usar Aspose.Note para Java para modificar revisões de página?**  
A1: Não, a API atualmente suporta apenas acesso de leitura às revisões de página.

**Q2: O Aspose.Note para Java é compatível com diferentes versões de documentos OneNote?**  
A2: Sim, funciona com vários formatos de arquivos OneNote, permitindo processamento contínuo entre versões.

**Q3: O Aspose.Note para Java requer uma licença para uso?**  
A3: Uma licença comercial é necessária para uso em produção, mas uma licença de avaliação temporária está disponível para testes.

**Q4: Posso buscar suporte se encontrar algum problema ao usar Aspose.Note para Java?**  
A4: Sim, você pode fazer perguntas no fórum Aspose.Note [aqui](https://forum.aspose.com/c/note/28).

**Q5: Existe um teste gratuito disponível para Aspose.Note para Java?**  
A5: Sim, você pode baixar um teste gratuito no [site](https://releases.aspose.com/).

---

**Última atualização:** 2026-01-10  
**Testado com:** Aspose.Note para Java (última versão)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}