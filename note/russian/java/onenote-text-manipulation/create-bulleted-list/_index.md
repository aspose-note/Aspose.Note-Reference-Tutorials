---
title: Создать маркированный список в OneNote — Aspose.Note
linktitle: Создать маркированный список в OneNote — Aspose.Note
second_title: Aspose.Note Java API
description: Изучите пошаговое руководство по созданию маркированных списков в OneNote с помощью Aspose.Note для Java. Упростите создание документов.
type: docs
weight: 12
url: /ru/java/onenote-text-manipulation/create-bulleted-list/
---
## Введение
В динамичной среде разработки Java создание интересных и организованных документов имеет важное значение. Aspose.Note для Java предоставляет мощный набор инструментов для улучшения процесса создания документов. Это руководство проведет вас через процесс создания маркированных списков в OneNote с помощью Aspose.Note для Java. Давайте углубимся в детали.
## Предварительные условия
Прежде чем мы начнем, убедитесь, что у вас есть следующие предварительные условия:
- Базовые знания Java-программирования.
-  Установлена библиотека Aspose.Note для Java. Вы можете скачать его с сайта[Aspose.Note для документации Java](https://reference.aspose.com/note/java/).
- На вашем компьютере установлена интегрированная среда разработки Java (IDE).
## Импортировать пакеты
Начните с импорта необходимых пакетов в ваш Java-проект. Это гарантирует, что у вас будет доступ к функциям Aspose.Note для Java.
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NumberList;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.ParagraphStyle;
// Импорт пакетов Aspose.Note для Java
```
## Шаг 1. Инициализируйте документ и страницу
Создайте объект класса Document и инициализируйте объект класса Page.
```java
String dataDir = "Your Document Directory";
// создать объект класса Document
Document doc = new Document();
// инициализировать объект класса страницы
Page page = new Page();
```
## Шаг 2. Инициализируйте Outline и TextStyle
Теперь инициализируйте объект класса Outline и объект класса TextStyle со свойствами форматирования.
```java
// инициализировать объект класса Outline
Outline outline = new Outline();
// инициализировать объект класса TextStyle и установить свойства форматирования
ParagraphStyle defaultStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```
## Шаг 3. Создайте элементы маркированного списка
Создайте объекты класса OutlineElement и примените маркеры для создания маркированного списка.
```java
// инициализировать объекты класса OutlineElement и применять маркеры
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("*", "Arial", 10));
// инициализировать объект класса RichText и применить стиль текста
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
```
Повторите вышеуказанные шаги для каждого элемента маркированного списка.
## Шаг 4. Добавьте элементы структуры в структуру
Добавьте созданные объекты OutlineElement в Outline.
```java
// добавить элементы контура
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```
## Шаг 5. Добавьте схему на страницу и сохраните.
Добавьте узел «Структура» на страницу, а затем добавьте узел «Страница» в документ. Наконец, сохраните документ.
```java
// добавить узел структуры
page.appendChildLast(outline);
// добавить узел страницы
doc.appendChildLast(page);
// сохранить документ
doc.save(dataDir + "CreateBulletedList_out.pdf");
```
Поздравляем! Вы успешно создали маркированный список в OneNote с помощью Aspose.Note для Java.
## Заключение
Aspose.Note для Java упрощает процесс создания хорошо отформатированных документов. В этом руководстве вы узнаете, как создать маркированный список в OneNote. Откройте для себя больше возможностей с помощью Aspose.Note, чтобы улучшить процесс создания документов.
## Часто задаваемые вопросы
### Совместим ли Aspose.Note для Java со всеми Java IDE?
Да, Aspose.Note для Java совместим с популярными интегрированными средами разработки Java, такими как Eclipse и IntelliJ IDEA.
### Могу ли я настроить форматирование маркированного списка?
Абсолютно! Вы можете изменить шрифт, цвет и размер элементов маркированного списка в соответствии со своими предпочтениями.
### Где я могу найти дополнительную поддержку Aspose.Note для Java?
 Посетить[Форум поддержки Aspose.Note для Java](https://forum.aspose.com/c/note/28) за помощь сообщества.
### Доступна ли бесплатная пробная версия Aspose.Note для Java?
 Да, вы можете изучить бесплатную пробную версию[здесь](https://releases.aspose.com/).
### Как я могу получить временную лицензию на Aspose.Note для Java?
 Получить временную лицензию[здесь](https://purchase.aspose.com/temporary-license/).