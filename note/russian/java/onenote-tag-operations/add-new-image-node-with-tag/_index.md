---
title: Добавить новый узел изображения с тегом в OneNote — Aspose.Note
linktitle: Добавить новый узел изображения с тегом в OneNote — Aspose.Note
second_title: Aspose.Note Java API
description: Узнайте, как добавить новый узел изображения с тегом в OneNote с помощью Aspose.Note для Java. Совершенствуйте свои навыки программирования на Java без особых усилий.
weight: 10
url: /ru/java/onenote-tag-operations/add-new-image-node-with-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Добавить новый узел изображения с тегом в OneNote — Aspose.Note

## Введение
В области программирования на Java Aspose.Note выделяется как мощный инструмент для простой обработки документов OneNote. Если вы хотите улучшить свои навыки и научиться добавлять новый узел изображения с тегом в OneNote с помощью Aspose.Note, вы попали по адресу. Это пошаговое руководство проведет вас через весь процесс, гарантируя, что вы полностью поймете каждую концепцию.
## Предварительные условия
Прежде чем мы углубимся в руководство, давайте убедимся, что у вас есть все необходимое:
1.  Aspose.Note для Java: убедитесь, что у вас установлена библиотека Aspose.Note. Если нет, то вы можете скачать его[здесь](https://releases.aspose.com/note/java/).
2. Среда разработки Java. Убедитесь, что на вашем компьютере установлена работающая среда разработки Java.
Теперь, когда у нас есть все необходимые условия, давайте перейдем к следующим шагам.
## Импортировать пакеты
В вашем проекте Java начните с импорта необходимых пакетов:
```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Image;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
import com.aspose.note.TagIcon;
```
## Шаг 1. Создайте объект документа
```java
// Путь к каталогу документов.
String dataDir = "Your Document Directory";
// создать объект класса Document
Document doc = new Document();
```
## Шаг 2. Инициализация объекта класса страницы
```java
// инициализировать объект класса страницы
Page page = new Page();
```
## Шаг 3. Инициализация объекта класса Outline
```java
// инициализировать объект класса Outline
Outline outline = new Outline();
```
## Шаг 4. Инициализация объекта класса OutlineElement
```java
// инициализировать объект класса OutlineElement
OutlineElement outlineElem = new OutlineElement();
```
## Шаг 5: Загрузите и вставьте изображение
```java
// загрузить изображение
Image image = new Image(null, dataDir + "Input.jpg");
// вставить изображение в узел документа
outlineElem.appendChildLast(image);
```
## Шаг 6. Добавьте тег заметки к изображению
```java
// добавить к изображению желтую звездочку
NoteTag noteTag = NoteTag.createYellowStar();
image.getTags().add(noteTag);
```
## Шаг 7. Добавьте узел элемента контура
```java
// добавить узел элемента контура
outline.appendChildLast(outlineElem);
```
## Шаг 8: Добавьте узел структуры
```java
// добавить узел контура
page.appendChildLast(outline);
```
## Шаг 9: Добавьте узел страницы
```java
// добавить узел страницы
doc.appendChildLast(page);
```
## Шаг 10. Сохраните документ OneNote
```java
// сохранить документ OneNote в формате PDF
doc.save(dataDir + "AddNewImageNodeWithTag_out.pdf", SaveFormat.Pdf);
```
Поздравляем! Вы успешно добавили новый узел изображения с тегом в OneNote с помощью Aspose.Note для Java.
## Заключение
 Освоение Aspose.Note для Java открывает захватывающие возможности манипулирования документами OneNote. Следуя этому руководству, вы приобрели практические навыки, которые можно применять в различных проектах. Продолжайте изучать документацию Aspose.Note.[здесь](https://reference.aspose.com/note/java/)для более продвинутых функций и возможностей.
## Часто задаваемые вопросы
### Где я могу найти документацию Aspose.Note?
 Вы можете найти документацию[здесь](https://reference.aspose.com/note/java/).
### Как загрузить Aspose.Note для Java?
 Вы можете скачать его со страницы релизов.[здесь](https://releases.aspose.com/note/java/).
### Доступна ли бесплатная пробная версия?
 Да, вы можете получить доступ к бесплатной пробной версии[здесь](https://releases.aspose.com/).
### Где я могу получить поддержку для Aspose.Note?
 Посетите форум сообщества[здесь](https://forum.aspose.com/c/note/28) для поддержки.
### Нужна ли мне временная лицензия?
 При необходимости вы можете получить временную лицензию.[здесь](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
