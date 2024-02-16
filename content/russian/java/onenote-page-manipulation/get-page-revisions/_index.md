---
title: Получить версии страницы в OneNote — Aspose.Note
linktitle: Получить версии страницы в OneNote — Aspose.Note
second_title: Aspose.Note Java API
description: Узнайте, как получить версии страницы в OneNote с помощью Aspose.Note для Java. Следуйте нашему пошаговому руководству для эффективного отслеживания изменений.
type: docs
weight: 14
url: /ru/java/onenote-page-manipulation/get-page-revisions/
---
## Введение

OneNote — мощный инструмент для организации заметок и управления ими, но иногда вам необходимо отслеживать изменения и исправления, внесенные на ваши страницы. С помощью Aspose.Note для Java вы можете легко получать версии страниц программным способом. В этом руководстве мы покажем вам процесс получения редакций страниц в OneNote с помощью Aspose.Note для Java.

## Предварительные условия

Прежде чем мы начнем, убедитесь, что у вас есть следующие предварительные условия:

### 1. Комплект разработки Java (JDK)

Убедитесь, что в вашей системе установлен Java Development Kit (JDK). Вы можете загрузить и установить JDK с веб-сайта Oracle.

### 2. Aspose.Note для Java

Загрузите и установите Aspose.Note для Java с сайта[ссылка для скачивания](https://releases.aspose.com/note/java/).

### 3. Образец документа OneNote

Подготовьте образец документа OneNote (`Sample1.one`), содержащий страницы, с которых вы хотите получить версии.

## Импортировать пакеты

Сначала вам необходимо импортировать необходимые пакеты из Aspose.Note для Java.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

Теперь давайте разобьем приведенный пример на несколько этапов:

## Шаг 1. Настройка каталога документов

Определите путь к каталогу, в котором находится ваш документ OneNote.

```java
String dataDir = "Your Document Directory";
```

## Шаг 2. Загрузите документ OneNote

 Загрузите документ OneNote, используя`LoadOptions` чтобы включить историю загрузки.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

## Шаг 3. Получите первую страницу

Получить первую страницу из загруженного документа.

```java
Page firstPage = document.getFirstChild();
```

## Шаг 4. Повторение изменений страницы

Перебирайте каждую редакцию страницы и получайте соответствующую информацию, такую как время последнего изменения, время создания, заголовок, уровень и автор.

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

## Заключение

В этом руководстве мы научились получать версии страниц в OneNote с помощью Aspose.Note для Java. Выполнив эти действия, вы сможете эффективно отслеживать изменения, внесенные на страницы OneNote программным способом.

## Часто задаваемые вопросы

### Вопрос 1: Могу ли я использовать Aspose.Note для Java для изменения версий страниц?

О1: Нет, Aspose.Note для Java в настоящее время поддерживает получение версий страниц, но не их изменение.

### Вопрос 2. Совместим ли Aspose.Note для Java с различными версиями документов OneNote?

О2: Да, Aspose.Note для Java поддерживает различные версии документов OneNote, что позволяет вам беспрепятственно работать с файлами разных форматов.

### Вопрос 3: Требуется ли лицензия для использования Aspose.Note for Java?

О3: Да, вам необходимо приобрести лицензию для использования Aspose.Note для Java в коммерческих проектах. Однако вы также можете получить временную лицензию для ознакомительных целей.

### Вопрос 4: Могу ли я обратиться за поддержкой, если у меня возникнут какие-либо проблемы при использовании Aspose.Note для Java?

 A4: Да, вы можете обратиться за поддержкой на форум Aspose.Note.[здесь](https://forum.aspose.com/c/note/28).

### Вопрос 5: Существует ли бесплатная пробная версия Aspose.Note для Java?

 О5: Да, вы можете получить доступ к бесплатной пробной версии Aspose.Note для Java на сайте[Веб-сайт](https://releases.aspose.com/).