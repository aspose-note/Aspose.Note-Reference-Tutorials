---
title: Получить информацию об изображении из OneNote с помощью Java
linktitle: Получить информацию об изображении из OneNote с помощью Java
second_title: Aspose.Note Java API
description: Извлекайте информацию об изображении из документов OneNote на Java! Получите размеры изображения, имена файлов и многое другое. Включены простые шаги и примеры кода. #OneNote #Java #Aspose
type: docs
weight: 15
url: /ru/java/onenote-hyperlinks-images/get-image-info/
---
## Введение

В сфере разработки Java извлечение информации из документов различных форматов является обычной задачей. OneNote, популярная платформа для создания заметок, часто содержит изображения рядом с текстом. Программное получение информации об изображении из файлов OneNote с использованием Java может упростить рабочие процессы обработки документов. В этом уроке мы углубимся в то, как извлечь детали изображения из документов OneNote с помощью Aspose.Note для Java.

## Предварительные условия

Прежде чем мы углубимся в реализацию, убедитесь, что у вас есть следующие предварительные условия:

### 1. Комплект разработки Java (JDK)

Убедитесь, что в вашей системе установлен Java Development Kit (JDK). Вы можете загрузить и установить последнюю версию JDK с сайта[веб-сайт Oracle](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).

### 2. Aspose.Note для библиотеки Java

 Загрузите и включите библиотеку Aspose.Note for Java в свой проект. Вы можете получить библиотеку по адресу[страница загрузки](https://releases.aspose.com/note/java/).

### 3. Документ OneNote

Подготовьте образец документа OneNote, содержащего изображения. Этот документ будет использоваться для программного извлечения информации об изображении.

## Импортировать пакеты

Для начала импортируйте необходимые пакеты из Aspose.Note for Java:

```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.Image;
```

Давайте разобьем приведенный выше код на пошаговые инструкции:

## Шаг 1. Установите каталог документов

```java
String dataDir = "Your Document Directory";
```

 Заменять`"Your Document Directory"` с путем к вашему документу OneNote.

## Шаг 2. Загрузите документ

```java
Document doc = new Document(dataDir + "Sample1.one");
```

Загрузите документ OneNote с помощью библиотеки Aspose.Note для Java. Убедитесь, что вы указали правильный путь к документу.

## Шаг 3: Получите все изображения

```java
List<Image> list = doc.getChildNodes(Image.class);
```

Получите все изображения из загруженного документа OneNote.

## Шаг 4. Распечатайте общее количество изображений

```java
System.out.printf("Total Images: %s\n\n", list.size());
```

Выведите общее количество изображений, найденных в документе.

## Шаг 5. Просмотр и печать информации об изображении

```java
for (Image image : list) {
    System.out.println("Width: " + image.getWidth());
    System.out.println("Height: " + image.getHeight());
    System.out.println("OriginalWidth: " + image.getOriginalWidth());
    System.out.println("OriginalHeight: " + image.getOriginalHeight());
    System.out.println("FileName: " + image.getFileName());
    System.out.println("LastModifiedTime: " + image.getLastModifiedTime());
    System.out.println();
}
```

Перебирайте список изображений и печатайте такие детали, как ширина, высота, исходные размеры, имя файла и время последнего изменения для каждого изображения.

## Заключение

Следуя шагам, описанным в этом руководстве, вы сможете эффективно получать информацию об изображениях из документов OneNote с помощью Java с помощью библиотеки Aspose.Note для Java. Интеграция этой функции в ваши приложения может автоматизировать задачи, связанные с обработкой документов, повышая эффективность и производительность.

## Часто задаваемые вопросы

### Вопрос 1. Может ли Aspose.Note для Java обрабатывать документы других форматов, кроме OneNote?

О1: Да, Aspose.Note для Java поддерживает различные форматы документов, включая OneNote, PDF и Microsoft Word.

### Вопрос 2. Подходит ли Aspose.Note для Java как для личного, так и для коммерческого использования?

О2: Да, вы можете использовать Aspose.Note для Java как в личных, так и в коммерческих целях.

### В3: Предлагает ли Aspose.Note для Java техническую поддержку?

 О3: Да, техническая поддержка доступна на форумах Aspose по адресу[здесь](https://forum.aspose.com/c/note/28).

### Вопрос 4: Могу ли я попробовать Aspose.Note для Java перед покупкой?

 О4: Да, вы можете ознакомиться с бесплатной пробной версией Aspose.Note для Java на сайте[Aspose.Note для Java](https://releases.aspose.com/note/java/).

### Вопрос 5: Как я могу получить временную лицензию на Aspose.Note для Java?
 
 О5: Вы можете приобрести временную лицензию на[Временная лицензия/](https://purchase.aspose.com/temporary-license/).