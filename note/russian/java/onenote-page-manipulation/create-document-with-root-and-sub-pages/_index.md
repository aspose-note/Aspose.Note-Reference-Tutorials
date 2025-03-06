---
title: Создать документ с корневыми и подстраницами в OneNote
linktitle: Создать документ с корневыми и подстраницами в OneNote
second_title: Aspose.Note Java API
description: Создайте документ с корневыми и подстраницами в OneNote, используя Aspose.Note для Java. Следуйте пошаговому руководству, чтобы эффективно организовать свои заметки.
weight: 11
url: /ru/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Создать документ с корневыми и подстраницами в OneNote

## Введение

В этом руководстве мы покажем вам процесс создания документа с корневыми и подстраницами в OneNote с использованием Aspose.Note для Java. Выполнив эти шаги, вы сможете эффективно организовать свои документы OneNote с помощью иерархической структуры.

## Предварительные условия

Прежде чем начать, убедитесь, что у вас есть следующие предварительные условия:

1. Java Development Kit (JDK): убедитесь, что в вашей системе установлен JDK.
2. Aspose.Note для Java: Загрузите и установите Aspose.Note для Java с сайта[Веб-сайт](https://purchase.aspose.com/buy).
3. Интегрированная среда разработки (IDE): выберите Java IDE, например IntelliJ IDEA, Eclipse или NetBeans.

## Импортировать пакеты

Начните с импорта необходимых пакетов в ваш Java-проект:

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

## Шаг 1. Настройка каталога документов

Определите каталог, в котором вы хотите сохранить документ OneNote:

```java
String dataDir = "Your Document Directory";
```

## Шаг 2. Создайте объект документа

 Создать экземпляр`Document` объект:

```java
Document doc = new Document();
```

## Шаг 3: Создайте страницы

Инициализируйте объекты страницы и установите их уровни:

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## Шаг 4. Добавьте узлы на страницы

### Добавление узлов на первую страницу

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text = new RichText().append("First page.");
text.setParagraphStyle(textStyle);

outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page1.appendChildLast(outline);
```

### Добавление узлов на вторую страницу

```java
Outline outline2 = new Outline();
OutlineElement outlineElem2 = new OutlineElement();
ParagraphStyle textStyle2 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text2 = new RichText().append("Second page.");
text2.setParagraphStyle(textStyle2);

outlineElem2.appendChildLast(text2);
outline2.appendChildLast(outlineElem2);
page2.appendChildLast(outline2);
```

### Добавление узлов на третью страницу

```java
Outline outline3 = new Outline();
OutlineElement outlineElem3 = new OutlineElement();
ParagraphStyle textStyle3 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Broadway")
                                    .setFontSize(10);

RichText text3 = new RichText().append("Third page.");
text3.setParagraphStyle(textStyle3);

outlineElem3.appendChildLast(text3);
outline3.appendChildLast(outlineElem3);
page3.appendChildLast(outline3);
```

## Шаг 5. Добавьте страницы в документ

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## Шаг 6: Сохраните документ

Сохраните документ OneNote:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Обработка исключения
}
```

Поздравляем! Вы успешно создали документ с корневой и подстраницами в OneNote с помощью Aspose.Note для Java.

## Заключение

Организация документов OneNote с помощью иерархической структуры необходима для лучшего управления и навигации. С помощью Aspose.Note для Java вы можете эффективно создавать документы с корневыми и подстраницами, обеспечивая четкий и организованный макет для ваших заметок.

## Часто задаваемые вопросы

### Вопрос 1: Могу ли я создать несколько уровней подстраниц с помощью Aspose.Note для Java?

О1: Да, вы можете создать несколько уровней подстраниц, установив соответствующий уровень для каждой страницы.

### Вопрос 2. Совместим ли Aspose.Note для Java с различными IDE Java?

О2: Да, Aspose.Note для Java совместим с популярными Java IDE, такими как IntelliJ IDEA, Eclipse и NetBeans.

### Вопрос 3. Могу ли я настроить форматирование текста в документе OneNote?

О3: Да, вы можете настроить шрифт, цвет, размер и другие параметры форматирования с помощью функций форматированного текста Aspose.Note для Java.

### Вопрос 4: Поддерживает ли Aspose.Note для Java сохранение документов в разных форматах?

О4: Да, Aspose.Note для Java поддерживает сохранение документов в различных форматах, включая BMP, PDF, PNG и другие.

### Вопрос 5: Доступна ли пробная версия Aspose.Note для Java?

О5: Да, вы можете загрузить бесплатную пробную версию Aspose.Note для Java с веб-сайта.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
