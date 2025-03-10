---
title: Получение редакций страниц в OneNote — Aspose.Note
linktitle: Получение редакций страниц в OneNote — Aspose.Note
second_title: Aspose.Note Java API
description: Узнайте, как получить версии страниц в документах OneNote с помощью Aspose.Note Java. Интегрируйте это в свои приложения Java для эффективного управления документами.
weight: 15
url: /ru/java/onenote-page-manipulation/get-revisions-of-pages/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Получение редакций страниц в OneNote — Aspose.Note

## Введение

В этом руководстве мы углубимся в возможности Aspose.Note для Java, мощной библиотеки, которая позволяет вам беспрепятственно работать с файлами Microsoft OneNote в ваших приложениях Java. В частности, мы сосредоточимся на том, как получить версии страниц в документе OneNote. К концу этого руководства вы будете обладать знаниями, позволяющими эффективно извлекать версии страниц, включая такие детали, как время последнего изменения, время создания, название, уровень и автор.

## Предварительные условия

Прежде чем приступить к изучению этого руководства, убедитесь, что у вас настроены следующие предварительные условия:

### Установлен пакет разработки Java (JDK)

Убедитесь, что в вашей системе установлен Java Development Kit. Вы можете загрузить и установить его с веб-сайта Oracle или использовать менеджер пакетов, если вы используете систему на базе Unix.

### Aspose.Note для библиотеки Java

 Загрузите и установите библиотеку Aspose.Note для Java с веб-сайта. Вы можете найти ссылку для скачивания[здесь](https://releases.aspose.com/note/java/) . Следуйте инструкциям по установке, приведенным в документации.[здесь](https://reference.aspose.com/note/java/).

## Импортировать пакеты

Для начала импортируйте необходимые пакеты в ваш Java-проект. Эти пакеты позволят вам использовать функциональность Aspose.Note для Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

Теперь давайте разобьем предоставленный пример кода на несколько шагов, чтобы понять каждый компонент и его функциональность.

## Шаг 1. Установите каталог документов

Определите каталог, в котором находится ваш документ OneNote.

```java
String dataDir = "Your Document Directory";
```

## Шаг 2. Загрузите документ

Загрузите документ OneNote в Aspose.Note.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## Шаг 3. Получите первую страницу

Получите первую страницу документа.

```java
Page firstPage = doc.getFirstChild();
```

## Шаг 4. Получите версии страницы

Получите историю изменений страницы.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## Шаг 5. Просмотрите изменения страницы.

Просмотрите список редакций страниц и получите соответствующую информацию.

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

## Заключение

В этом руководстве мы рассмотрели, как получить версии страниц в документе OneNote с помощью Aspose.Note для Java. Следуя пошаговому руководству и используя предоставленный пример кода, вы можете легко интегрировать эту функцию в свои приложения Java, обеспечивая эффективное управление файлами OneNote.

## Часто задаваемые вопросы

### Вопрос 1. Могу ли я использовать Aspose.Note для Java для создания новых документов OneNote?

О1: Да, Aspose.Note для Java обеспечивает комплексную поддержку для программного создания, чтения и управления документами OneNote.

### Вопрос 2. Совместим ли Aspose.Note для Java с различными версиями файлов OneNote?

О2: Да, Aspose.Note для Java поддерживает различные версии файлов Microsoft OneNote, обеспечивая совместимость в различных средах.

### Вопрос 3. Могу ли я настроить выходной формат при экспорте документов OneNote?

О3: Конечно, Aspose.Note для Java предлагает гибкость при экспорте документов OneNote в различные форматы, такие как PDF, HTML и изображения, с возможностью настройки.

### Вопрос 4: Требуется ли Aspose.Note for Java лицензия для коммерческого использования?

О4: Да, для коммерческого использования Aspose.Note для Java требуется действующая лицензия. Вы можете получить лицензию на веб-сайте Aspose.

### Вопрос 5. Куда я могу обратиться за помощью, если у меня возникнут проблемы или возникнут вопросы по Aspose.Note для Java?

 A5: Для поддержки и помощи вы можете посетить форум Aspose.Note.[здесь](https://forum.aspose.com/c/note/28)где вы можете задавать вопросы, делиться опытом и общаться с другими пользователями и экспертами.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
