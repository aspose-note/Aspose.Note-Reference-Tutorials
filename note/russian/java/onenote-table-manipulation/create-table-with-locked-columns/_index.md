---
title: Создать таблицу с заблокированными столбцами в OneNote — Aspose.Note
linktitle: Создать таблицу с заблокированными столбцами в OneNote — Aspose.Note
second_title: Aspose.Note Java API
description: Расширьте возможности OneNote с помощью Aspose.Note для Java. Узнайте, как создавать таблицы с заблокированными столбцами, используя пошаговое руководство. Загрузите бесплатную пробную версию прямо сейчас!
weight: 12
url: /ru/java/onenote-table-manipulation/create-table-with-locked-columns/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Создать таблицу с заблокированными столбцами в OneNote — Aspose.Note

## Введение
OneNote — мощный инструмент для организации информации, а Aspose.Note для Java расширяет его возможности, предоставляя простой способ создания таблиц с заблокированными столбцами. В этом руководстве мы покажем вам процесс использования Aspose.Note для Java для создания таблицы с заблокированными столбцами в OneNote.
## Предварительные условия
Прежде чем начать, убедитесь, что у вас есть следующие предварительные условия:
- [Комплект разработки Java (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html)установлен на вашей машине.
- [Aspose.Note для Java](https://downloads.aspose.com/note/java) библиотека загружена и добавлена в ваш проект.
## Импортировать пакеты
В свой Java-проект импортируйте необходимые пакеты для работы с Aspose.Note:
```java
import com.aspose.note.*;
import java.io.IOException;
```
## Шаг 1. Настройте свой проект
Начните с создания нового проекта Java и добавления библиотеки Aspose.Note в ваш путь к классам. Убедитесь, что ваш проект настроен для использования JDK.
## Шаг 2. Инициализация объектов документа и страницы
```java
// Путь к каталогу документов.
String dataDir = "Your Document Directory";
//Создайте объект класса Document
Document doc = new Document();
// Инициализировать объект класса страницы
Page page = new Page();
```
## Шаг 3. Создайте строки и ячейки таблицы
```java
// Инициализировать объект класса TableRow
TableRow row1 = new TableRow();
// Инициализируйте объект класса TableCell и установите текстовое содержимое.
TableCell cell11 = new TableCell();
cell11.appendChildLast(InsertTable.GetOutlineElementWithText("Small text"));
row1.appendChildLast(cell11);
// Инициализировать объект класса TableRow
TableRow row2 = new TableRow();
// Инициализируйте объект класса TableCell и установите текстовое содержимое.
TableCell cell21 = new TableCell();
cell21.appendChildLast(InsertTable.GetOutlineElementWithText("Long   text    with    several   words and    spaces."));
row2.appendChildLast(cell21);
```
## Шаг 4. Создайте и настройте таблицу
```java
// Инициализировать объект класса таблицы
Table table = new Table();
table.setBordersVisible(true);
TableColumn col = new TableColumn();
col.setWidth(200);
col.setLockedWidth(true);
table.getColumns().addItem(col);
// Добавить строки
table.appendChildLast(row1);
table.appendChildLast(row2);
```
## Шаг 5. Добавьте таблицу в структуру и на страницу
```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
// Добавить узел таблицы
outlineElem.appendChildLast(table);
// Добавить узел элемента контура
outline.appendChildLast(outlineElem);
// Добавить узел контура
page.appendChildLast(outline);
// Добавить узел страницы
doc.appendChildLast(page);
```
## Шаг 6: Сохраните документ
```java
dataDir = dataDir + "CreateTableWithLockedColumns_out.one";
doc.save(dataDir);
```
Поздравляем! Вы успешно создали таблицу с заблокированными столбцами в OneNote с помощью Aspose.Note для Java.
## Заключение
В этом руководстве мы рассмотрели процесс использования Aspose.Note для Java для улучшения работы с OneNote путем создания таблиц с заблокированными столбцами. Эта функция добавляет новый уровень организации и структуры в ваши заметки.
## Часто задаваемые вопросы
### Совместим ли Aspose.Note для Java со всеми версиями Java?
Да, Aspose.Note для Java совместим с Java 6 и более поздними версиями.
### Могу ли я дополнительно настроить внешний вид таблицы?
Абсолютно! Aspose.Note для Java предоставляет широкие возможности настройки таблиц, такие как настройка границ, интервалов между ячейками и многое другое.
### Доступна ли пробная версия перед покупкой?
 Да, ты можешь[скачать бесплатную пробную версию](https://releases.aspose.com/) изучить возможности Aspose.Note для Java.
### Где я могу найти дополнительную поддержку или обсуждения в сообществе?
 Посетить[Форум Aspose.Note](https://forum.aspose.com/c/note/28) за поддержку и обсуждения в сообществе.
### Как я могу получить временную лицензию на Aspose.Note для Java?
 Посещать[эта ссылка](https://purchase.aspose.com/temporary-license/) получить временную лицензию для целей тестирования.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
