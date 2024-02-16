---
title: Создайте документ и вставьте изображение в OneNote с помощью Java
linktitle: Создайте документ и вставьте изображение в OneNote с помощью Java
second_title: Aspose.Note Java API
description: Узнайте, как создавать документы OneNote и вставлять изображения с помощью Aspose.Note для Java. Пошаговое руководство для бесшовной интеграции.
type: docs
weight: 12
url: /ru/java/onenote-hyperlinks-images/build-doc-insert-image/
---
## Введение

В этом уроке мы рассмотрим, как использовать Aspose.Note для Java для создания документов OneNote и вставки в них изображений. Aspose.Note — это мощный Java API, который позволяет разработчикам программно работать с файлами Microsoft OneNote. Мы подробно разберем каждый шаг, чтобы помочь вам в этом процессе.

## Предварительные условия

Прежде чем мы начнем, убедитесь, что у вас есть следующие предварительные условия:

1. Java Development Kit (JDK): убедитесь, что в вашей системе установлен JDK.
2.  Библиотека Aspose.Note для Java: Загрузите и установите библиотеку Aspose.Note для Java с сайта[Веб-сайт](https://releases.aspose.com/note/java/).
3. IDE (интегрированная среда разработки): для кодирования используйте любую IDE с поддержкой Java, например IntelliJ IDEA или Eclipse.

## Импортировать пакеты

Начните с импорта необходимых пакетов в ваш Java-код:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## Шаг 1. Настройте документ

Сначала создайте новый документ OneNote и инициализируйте необходимые объекты:

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

## Шаг 2: Инициализируйте структуру

Настройте контур документа и укажите свойства смещения:

```java
Outline outline = new Outline();
outline.setVerticalOffset(0);
outline.setHorizontalOffset(0);
```

## Шаг 3: Добавьте изображение

Загрузите изображение и укажите его выравнивание:

```java
Image image = new Image(null, dataDir + "Input.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## Шаг 4. Добавьте изображение к элементу структуры

Прикрепите изображение к элементу контура:

```java
OutlineElement outlineElem = new OutlineElement();
outlineElem.appendChildLast(image);
```

## Шаг 5. Добавьте узлы структуры и страницы

Добавьте в документ узлы структуры и страницы:

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## Шаг 6: Сохранить документ

Наконец, сохраните документ OneNote:

```java
try {
    doc.save(dataDir + "NewOneNotedocument_out", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Заключение

Поздравляем! Вы успешно научились создавать документы OneNote и вставлять в них изображения с помощью Aspose.Note для Java. Выполнив эти шаги, вы сможете эффективно управлять файлами OneNote и манипулировать ими в своих приложениях Java.

## Часто задаваемые вопросы

### Вопрос 1: Где я могу найти документацию по Aspose.Note для Java?

 A1: Вы можете получить доступ к документации[здесь](https://reference.aspose.com/note/java/).

### Вопрос 2: Как загрузить Aspose.Note для Java?

 О2: Вы можете скачать Aspose.Note для Java с сайта[страница загрузки](https://releases.aspose.com/note/java/).

### Вопрос 3. Существует ли бесплатная пробная версия Aspose.Note для Java?

 О3: Да, вы можете получить бесплатную пробную версию на сайте[Веб-сайт](https://releases.aspose.com/).

### Вопрос 4. Где я могу получить поддержку Aspose.Note для Java?

 A4: Для получения поддержки посетите[Форум Aspose.Note](https://forum.aspose.com/c/note/28).

### Вопрос 5: Могу ли я получить временную лицензию на Aspose.Note для Java?

 О5: Да, вы можете запросить временную лицензию.[здесь](https://purchase.aspose.com/temporary-license/).
