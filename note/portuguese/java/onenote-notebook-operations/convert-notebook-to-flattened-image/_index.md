---
date: 2025-12-25
description: Aprenda como converter OneNote para PNG usando Aspose.Note para Java.
  Este guia mostra como definir a resolução da imagem, achatar um caderno e salvar
  o OneNote como imagem de forma eficiente.
linktitle: How to Convert OneNote to PNG – Flatten Notebook to Image with Aspose.Note
second_title: Aspose.Note Java API
title: Como converter OneNote para PNG – Achatar caderno para imagem com Aspose.Note
url: /pt/java/onenote-notebook-operations/convert-notebook-to-flattened-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Converter Notebook para Imagem Achata em OneNote - Aspose.Note

## Introdução

Neste tutorial você descobrirá como **converter OneNote para PNG** transformando um notebook inteiro em uma única imagem achata usando Aspose.Note para Java. Essa abordagem é perfeita quando você precisa compartilhar um notebook como uma imagem estática, incorporá‑lo em relatórios ou arquivá‑lo sem perder detalhes visuais.

## Respostas Rápidas
- **O que significa “flatten notebook”?** Ele mescla todos os elementos da página em uma única imagem raster.  
- **Qual formato é usado?** PNG é o padrão, oferecendo qualidade sem perdas.  
- **Posso mudar o DPI?** Sim, use `setResolution` em `ImageSaveOptions`.  
- **Preciso de licença?** Uma avaliação gratuita funciona para testes; uma licença comercial é necessária para produção.  
- **Isso é suportado em todos os sistemas operacionais?** A API Java funciona onde quer que o Java rode.

## O que é converter OneNote para PNG?

Converter OneNote para PNG cria uma representação bitmap de cada página do notebook, preservando texto, desenhos e objetos incorporados em um único arquivo de imagem. Isso é especialmente útil para documentação, apresentações ou arquivos de conformidade.

## Por que converter OneNote para PNG com Aspose.Note?

- **Fidelidade total** – Todos os elementos visuais são mantidos.  
- **Saída em arquivo único** – Não é necessário gerenciar múltiplos arquivos de página.  
- **Resolução personalizável** – Ajuste o DPI para atender aos requisitos de qualidade.  
- **Sem necessidade de instalação do Office** – Funciona completamente independente do Microsoft OneNote.

## Pré‑requisitos

Antes de começar, certifique‑se de que você tem o seguinte:

1. Java Development Kit (JDK) instalado no seu sistema.  
2. Biblioteca Aspose.Note para Java baixada e configurada no seu projeto Java. Você pode baixar a biblioteca [aqui](https://releases.aspose.com/note/java/).  
3. Conhecimento básico de programação Java.

## Importar Pacotes

Para começar, você precisa importar os pacotes necessários do Aspose.Note para Java:

```java
import java.io.IOException;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Etapa 1: Configurar Diretório do Documento

Primeiro, defina o diretório onde seu arquivo de notebook está localizado:

```java
String dataDir = "Your Document Directory";
```

Substitua `"Your Document Directory"` pelo caminho do seu arquivo de notebook.

## Etapa 2: Carregar Notebook

Em seguida, carregue o arquivo de notebook usando a classe `Notebook`:

```java
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

Certifique‑se de substituir `"test.onetoc2"` pelo nome do seu arquivo de notebook.

## Etapa 3: Definir Opções de Salvamento de Imagem

Agora, configure as opções para salvar o notebook como uma imagem. Vamos especificar o formato de salvamento como PNG e definir a resolução para 400 DPI:

```java
NotebookImageSaveOptions saveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
ImageSaveOptions documentSaveOptions = saveOptions.getDocumentSaveOptions();
documentSaveOptions.setResolution(400);
```

Você pode ajustar a resolução conforme suas necessidades. É aqui que você **define a resolução da imagem** para controlar a qualidade da saída.

## Etapa 4: Achatar Notebook

Para garantir que todos os elementos sejam achatados em uma única imagem, defina a opção `flatten` como `true`:

```java
saveOptions.setFlatten(true);
```

Definir `flatten` como `true` garante que o PNG resultante mantenha o layout exato do seu notebook.

## Etapa 5: Salvar Imagem

Finalmente, salve o notebook como uma imagem achatada:

```java
notebook.save(dataDir + "ExportImageasFlattenedNotebook_out.png", saveOptions);
```

Substitua `"ExportImageasFlattenedNotebook_out.png"` pelo nome de arquivo de saída desejado. Esta etapa **salva o OneNote como uma imagem** que você pode compartilhar ou incorporar em qualquer lugar.

## Casos de Uso Comuns

- **Documentação:** Incorpore a imagem do notebook em manuais técnicos ou guias do usuário.  
- **Apresentações:** Use um slide PNG de alta resolução no PowerPoint sem se preocupar com compatibilidade de fontes ou objetos.  
- **Arquivamento:** Armazene um instantâneo somente‑leitura de um notebook para auditorias de conformidade.

## Dicas de Solução de Problemas

- **Arquivo não encontrado:** Verifique novamente o caminho `dataDir` e assegure‑se de que o arquivo `.onetoc2` exista.  
- **Imagem de baixa qualidade:** Aumente o DPI alterando `documentSaveOptions.setResolution(600);`.  
- **Elementos ausentes:** Verifique se `saveOptions.setFlatten(true);` está habilitado; caso contrário, algumas camadas podem permanecer separadas.

## Perguntas Frequentes

**Q1: Posso ajustar a resolução da imagem de saída?**  
A1: Sim, você pode ajustar a resolução de acordo com suas necessidades modificando o parâmetro do método `setResolution`.

**Q2: O Aspose.Note suporta outros formatos de imagem para exportação?**  
A2: Sim, o Aspose.Note suporta vários formatos de imagem como PNG, JPEG, BMP, etc., para exportar notebooks.

**Q3: Posso personalizar ainda mais a imagem de saída?**  
A3: Sim, o Aspose.Note oferece opções extensas para personalizar a imagem de saída, incluindo tamanho da página, orientação e configurações de qualidade.

**Q4: Existe uma versão de avaliação disponível para o Aspose.Note para Java?**  
A4: Sim, você pode obter uma versão de avaliação gratuita [aqui](https://releases.aspose.com/).

**Q5: Onde posso encontrar suporte para o Aspose.Note para Java?**  
A5: Você pode encontrar suporte e recursos no fórum Aspose.Note [aqui](https://forum.aspose.com/c/note/28).

---

**Última atualização:** 2025-12-25  
**Testado com:** Aspose.Note para Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}