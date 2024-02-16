---
title: 在 OneNote 中添加带有标签的新图像节点 - Aspose.Note
linktitle: 在 OneNote 中添加带有标签的新图像节点 - Aspose.Note
second_title: Aspose.Note Java API
description: 了解如何使用 Aspose.Note for Java 在 OneNote 中添加带有标签的新图像节点。轻松提升您的 Java 编程技能。
type: docs
weight: 10
url: /zh/java/onenote-tag-operations/add-new-image-node-with-tag/
---
## 介绍
在 Java 编程领域，Aspose.Note 作为轻松处理 OneNote 文档的强大工具而脱颖而出。如果您希望提高自己的技能并了解如何使用 Aspose.Note 在 OneNote 中添加带有标签的新图像节点，那么您来对地方了。本分步指南将引导您完成整个过程，确保您彻底掌握每个概念。
## 先决条件
在我们深入学习本教程之前，让我们确保您拥有所需的一切：
1.  Aspose.Note for Java：确保您已安装 Aspose.Note 库。如果没有的话可以下载[这里](https://releases.aspose.com/note/java/).
2. Java 开发环境：确保您的计算机上设置了有效的 Java 开发环境。
现在我们已经具备了先决条件，让我们继续下一步。
## 导入包
在您的 Java 项目中，首先导入必要的包：
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
## 第 1 步：创建文档对象
```java
//文档目录的路径。
String dataDir = "Your Document Directory";
//创建 Document 类的对象
Document doc = new Document();
```
## 第2步：初始化页面类对象
```java
//初始化Page类对象
Page page = new Page();
```
## 第3步：初始化Outline类对象
```java
//初始化 Outline 类对象
Outline outline = new Outline();
```
## 步骤 4：初始化 OutlineElement 类对象
```java
//初始化 OutlineElement 类对象
OutlineElement outlineElem = new OutlineElement();
```
## 第 5 步：加载并插入图像
```java
//加载图像
Image image = new Image(null, dataDir + "Input.jpg");
//在文档节点中插入图像
outlineElem.appendChildLast(image);
```
## 第 6 步：向图像添加注释标签
```java
//向图像添加黄色星形注释标签
NoteTag noteTag = NoteTag.createYellowStar();
image.getTags().add(noteTag);
```
## 第7步：添加轮廓元素节点
```java
//添加轮廓元素节点
outline.appendChildLast(outlineElem);
```
## 步骤8：添加轮廓节点
```java
//添加轮廓节点
page.appendChildLast(outline);
```
## 第9步：添加页面节点
```java
//添加页面节点
doc.appendChildLast(page);
```
## 第10步：保存OneNote文档
```java
//将 OneNote 文档另存为 PDF
doc.save(dataDir + "AddNewImageNodeWithTag_out.pdf", SaveFormat.Pdf);
```
恭喜！您已使用 Aspose.Note for Java 在 OneNote 中成功添加了带有标签的新图像节点。
## 结论
掌握 Aspose.Note for Java 为 OneNote 文档操作带来了令人兴奋的可能性。通过学习本教程，您将获得可应用于各种项目的实用技能。继续探索 Aspose.Note 文档[这里](https://reference.aspose.com/note/java/)以获得更高级的功能和可能性。
## 常见问题解答
### 在哪里可以找到 Aspose.Note 文档？
你可以找到文档[这里](https://reference.aspose.com/note/java/).
### 如何下载 Java 版 Aspose.Note？
您可以从发布页面下载它[这里](https://releases.aspose.com/note/java/).
### 有免费试用吗？
是的，您可以免费试用[这里](https://releases.aspose.com/).
### 在哪里可以获得 Aspose.Note 的支持？
访问社区论坛[这里](https://forum.aspose.com/c/note/28)为了支持。
### 我需要临时许可证吗？
如果需要，您可以获得临时许可证[这里](https://purchase.aspose.com/temporary-license/).