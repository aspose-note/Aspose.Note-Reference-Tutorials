---
date: 2026-01-05
description: 学习如何设置默认语言区域、加载 OneNote 文档、设置 Aspose 许可证、将 OneNote 转换为 PNG，并使用 Aspose.Note
  for Java 将 OneNote 保存为图像。
linktitle: Working with Locales in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: 在 OneNote 中设置默认语言区域 – Aspose.Note Java
url: /zh/java/onenote-notebook-operations/working-with-locales/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 OneNote 中设置默认语言区域 – Aspose.Note Java

## 介绍

如果您在处理 OneNote 文件时需要 **设置默认语言区域**，Aspose.Note for Java 能让这件事轻而易举。在本教程中，我们将一步步演示从产品授权、加载 OneNote 文档、修改语言区域，到最终将文件转换为 PNG 图像的完整流程。完成后，您只需几行代码即可自定义语言设置并生成针对特定语言区域的输出。

## 快速答疑
- **“设置默认语言区域”有什么作用？** 它定义了 Aspose.Note 在读取或写入 OneNote 文件时使用的语言和地区格式。  
- **我需要许可证吗？** 是的——设置 Aspose 许可证后才能解锁全部功能。  
- **需要哪个 Java 版本？** 支持任何 JDK 8 及以上版本。  
- **可以将 OneNote 转换为 PNG 吗？** 当然可以；API 允许您将页面保存为图像。  
- **该过程是线程安全的吗？** 设置默认语言区域是全局的，请在应用启动时配置一次即可。

## Aspose.Note 中的“设置默认语言区域”是什么？
设置默认语言区域告诉 Aspose.Note 在解析日期、数字和文本时应使用哪种语言和文化约定。这对于需要在不同用户语言环境下保持一致格式的多地区应用至关重要。

## 为什么在使用 OneNote 时要设置默认语言区域？
- **准确的数据表示：** 日期和数字会根据目标受众正确显示。  
- **一致的 UI 文本：** 从 OneNote 提取的文本会遵循语言设置。  
- **简化的转换过程：** 当您随后将 OneNote 文件转换为 PNG 或其他格式时，视觉布局会匹配预期的语言区域。

## 前置条件

- **Java 开发环境：** 已安装 JDK 并配置 `JAVA_HOME`。  
- **Aspose.Note 库：** 从 [download link](https://releases.aspose.com/note/java/) 下载最新的 JAR 包。  
- **有效的 Aspose 许可证文件**（免费试用版可用于测试）。

## 导入包

在编写任何代码之前，先导入提供所需功能的类。

```java
import java.io.IOException;
import java.nio.file.Path;
import java.util.Locale;
import com.aspose.note.Document;
import com.aspose.note.License;
import com.aspose.note.LocaleOptions;
```

## 步骤 1：设置 Aspose 许可证

```java
License license = new License();
license.setLicense("licenseFile");
```

设置 Aspose 许可证后即可解锁所有功能，包括语言区域处理和图像转换。

## 步骤 2：设置默认语言区域

```java
java.util.Locale.setDefault(new java.util.Locale("en", "rs"));
```

此处我们将 **默认语言区域** 设置为英语 (`en`) 且国家代码为 `rs`。请根据目标地区调整语言和国家代码。

## 步骤 3：加载 OneNote 文档

```java
String inputFile = "Sample1.one";
Path inputPath = Paths.get(inputFile);

Document oneFile = new Document(inputPath.toString());
```

此步骤 **加载 OneNote 文档** 到 `Document` 对象，以便后续操作其内容。

## 步骤 4：将 OneNote 转换为 PNG（OneNote 文件转换）

```java
oneFile.save("sample.png");
```

`save` 方法执行 **OneNote 文件转换**，将笔记本（或特定页面）导出为 PNG 图像——相当于 **convert onenote to png** 并 **save onenote as image**。

## 常见问题与技巧

- **未找到许可证：** 确认 `licenseFile` 的路径正确且文件具有读取权限。  
- **语言区域未生效：** 在加载文档之前调用 `Locale.setDefault`。  
- **缺少图像输出：** 请确保 OneNote 文件实际包含可渲染的页面；空笔记本会生成空白 PNG。

## 常见问答

**Q: Aspose.Note 是否兼容不同版本的 Java？**  
A: 是的，Aspose.Note 支持 Java 8 及更高版本，确保在各种开发环境中都有广泛的兼容性。

**Q: 我可以将 Aspose.Note 与其他 Java 库集成吗？**  
A: 当然可以。该 API 可与 Apache POI、Jackson、Spring 等流行库无缝协作。

**Q: Aspose.Note 是否支持多种文件格式？**  
A: 虽然核心关注点是 OneNote 文件，但库也能导出为 PNG、JPEG、PDF 等图像格式。

**Q: 是否有 Aspose.Note 用户社区论坛可供求助和交流？**  
A: 有，Aspose 社区论坛为用户提供与专家交流、提问和协作的平台。访问 [support forum](https://forum.aspose.com/c/note/28) 获取帮助。

**Q: 我可以在购买前试用 Aspose.Note 吗？**  
A: 当然可以，您可以通过网站提供的免费试用版体验 Aspose.Note 的全部功能。

## 结论

通过本教程，您已经学会了如何 **设置默认语言区域**、**加载 OneNote 文档**、**设置 Aspose 许可证**，以及使用 Aspose.Note for Java **将 OneNote 转换为 PNG**。此工作流帮助您生成面向全球受众的语言区域感知报告和图像。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最后更新：** 2026-01-05  
**测试环境：** Aspose.Note 24.11 for Java  
**作者：** Aspose