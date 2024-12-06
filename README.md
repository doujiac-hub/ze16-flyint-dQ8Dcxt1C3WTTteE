
目录* [什么是 FastExcel](https://github.com)
* [主要特性](https://github.com)
* [适用场景](https://github.com)
* [结论](https://github.com)
* [导航](https://github.com)
* [快速开始](https://github.com)
* [EasyExcel 与 FastExcel 的区别](https://github.com)
* [EasyExcel 如何升级到 FastExcel](https://github.com)
	+ [1\. 修改依赖](https://github.com)
	+ [2\. 修改代码](https://github.com)
	+ [3\. 不修改代码直接依赖 FastExcel](https://github.com)
	+ [4\. 建议以后使用 FastExcel 类](https://github.com)
* [简单示例：读取 Excel 文件](https://github.com):[slower加速器](https://jisuanqi.org)
* [简单示例：创建 Excel 文件](https://github.com)

![image](https://img2024.cnblogs.com/blog/80824/202412/80824-20241205092158153-810920086.png)
[https://github.com/CodePhiliaX/fastexcel](https://github.com)
[https://github.com/CodePhiliaX/fastexcel\-doc](https://github.com)
[https://mvnrepository.com/artifact/cn.idev.excel/fastexcel](https://github.com)


[@psxjoy](https://github.com) ：还在为第一版的正式发布而努力。文档方面，我们已经完成了第一版的内容。会随着第一个正式版本同时发布。


## 什么是 FastExcel


FastExcel 是由原 EasyExcel 作者创建的最新作品。在 2023 年作者从阿里离职后，随着阿里宣布停止更新 EasyExcel，作者决定继续维护和升级这个项目。在重新开始时，作者选择为它起名为 FastExcel，以突出这个框架在处理 Excel 文件时的高性能表现，而不仅仅是简单易用。


FastExcel 将始终坚持免费开源，并采用最开放的 MIT 协议，使其适用于任何商业化场景。这为开发者和企业提供了极大的自由度和灵活性。FastExcel 的一些显著特点包括：


* 1、完全兼容原 EasyExcel 的所有功能和特性，这使得用户可以无缝过渡。
* 2、从 EasyExcel 迁移到 FastExcel 只需简单地更换包名和 Maven 依赖即可完成升级。
* 3、在功能上，比 EasyExcel 提供更多创新和改进。
* 4、FastExcel 1\.0\.0 版本新增了读取 Excel 指定行数和将 Excel 转换为 PDF 的功能。


我们计划在未来推出更多新特性，以不断提升用户体验和工具实用性。欢迎大家关注 程序员小懒的公众号 关注FastExcel的发展。FastExcel 致力于成为您处理 Excel 文件的最佳选择。


## 主要特性


* 1. 高性能读写：FastExcel 专注于性能优化，能够高效处理大规模的 Excel 数据。相比一些传统的 Excel 处理库，它能显著降低内存占用。
* 2. 简单易用：该库提供了简洁直观的 API，使得开发者可以轻松集成到项目中，无论是简单的 Excel 操作还是复杂的数据处理都能快速上手。
* 3. 流式操作：FastExcel 支持流式读取，将一次性加载大量数据的问题降到最低。这种设计方式在处理数十万甚至上百万行的数据时尤为重要。


## 适用场景


FastExcel 非常适用于需要进行大规模数据导入导出操作的企业级应用场景。典型的使用场景包括：


* 数据报表生成：快速生成复杂的业务报表，支持多表格和动态数据填充。
* 批量数据导入：有效地将 Excel 数据批量导入至数据库系统，适用于人事管理、销售数据统计等领域。
* ERP 系统集成：在 ERP 系统中实现自动化的 Excel 数据交换，以简化工作流程。
* 在线教育平台：用于导入学生成绩单、课程计划等大规模数据。
* 财务分析：处理财务报表和账单明细，以便进行细致的财务分析。
* 物联网数据处理：解析和处理 IoT 设备上传的批量数据文件，为后续数据分析和处理提供支持。
借助 FastExcel，开发者能够快速、高效地实现 Excel 数据的读写操作，极大地提升工作效率，减少开发成本。


## 结论


FastExcel 是一个轻量级但功能强大的 Java 库，专为需要高性能和低内存占用的 Excel 文件处理而设计。如果您的项目需要处理大规模的 Excel 数据，FastExcel 无疑是一个值得考虑的选择。其流式处理和灵活的 API 使其成为处理 Excel 文件的理想工具。无论是开发新应用还是优化现有系统，FastExcel 都能够帮助开发者更轻松地应对 Excel 数据处理的挑战。


## 导航


* [快速开始](https://github.com)
* [进阶主题](https://github.com)
* [最佳实践](https://github.com)
* [常见问题](https://github.com)
* [贡献指南](https://github.com)
* [反馈BUG](https://github.com)


## 快速开始


FastExcel 基础库对 Java 语言版本最低要求的情况：




| 版本 | jdk版本支持范围 | 备注 |
| --- | --- | --- |
| 1\.0\.0\+ | jdk8 \- jdk21 | 目前的master分支，完全兼容easyexcel |


强烈建议您使用最新版本的 FastExcel，因为最新版本中的性能优化、BUG修复和新功能都会让您的使用更加方便。



> 当前 FastExcel 底层使用 poi 作为基础包，如果您的项目中已经有 poi 相关组件，需要您手动排除 poi 的相关 jar 包。


请在 `pom.xml` 文件中引入以下配置：目前仓库中是0\.0\.1版本，近期会发布



```
<dependency>
    <groupId>cn.idev.excelgroupId>
    <artifactId>fastexcelartifactId>
    <version>1.0.0version>
dependency>

```

## EasyExcel 与 FastExcel 的区别


\_ 1\. FastExcel 支持所有 EasyExcel 的功能，但是 FastExcel 的性能更好，更稳定。
\_ 2\. FastExcel 与 EasyExcel 的 API 完全一致，可以无缝切换。
\_ 3\. FastExcel 会持续的更新，修复 bug，优化性能，增加新功能。


## EasyExcel 如何升级到 FastExcel


### 1\. 修改依赖


将 EasyExcel 的依赖替换为 FastExcel 的依赖，如下：



```

<dependency>
    <groupId>com.alibabagroupId>
    <artifactId>easyexcelartifactId>
    <version>xxxxversion>
dependency>

```

的依赖替换为



```
<dependency>
    <groupId>cn.idev.excelgroupId>
    <artifactId>fastexcelartifactId>
    <version>1.0.0version>
dependency>

```

### 2\. 修改代码


将 EasyExcel 的包名替换为 FastExcel 的包名，如下：



```
// 将 easyexcel 的包名替换为 FastExcel 的包名
import com.alibaba.excel.**;

```

替换为



```
import cn.idev.excel.**;

```

### 3\. 不修改代码直接依赖 FastExcel


如果由于种种原因您不想修改代码，可以直接依赖 FastExcel ，然后在 `pom.xml` 文件中直接依赖 FastExcel。
EasyExcel 与 FastExcel 可以共存，但是长期建议替换为 FastExcel。


### 4\. 建议以后使用 FastExcel 类


为了兼容性考虑保留了 EasyExcel 类，但是建议以后使用 FastExcel 类，FastExcel 类是 类，FastExcel 的入口类，功能包含了 EasyExcel 类的所有功能，以后新特性仅在 FastExcel 类中添加。


## 简单示例：读取 Excel 文件


下面是读取 Excel 文档的例子：



```
// 实现 ReadListener 接口，设置读取数据的操作
public class DemoDataListener implements ReadListener {
    @Override
    public void invoke(DemoData data, AnalysisContext context) {
        System.out.println("解析到一条数据" + JSON.toJSONString(data));
    }

    @Override
    public void doAfterAllAnalysed(AnalysisContext context) {
        System.out.println("所有数据解析完成！");
    }
}

public static void main(String[] args) {
    String fileName = "demo.xlsx";
    // 读取 Excel 文件
    FastExcel.read(fileName, DemoData.class, new DemoDataListener()).sheet().doRead();
}

```

## 简单示例：创建 Excel 文件


下面是一个创建 Excel 文档的简单例子：



```
// 示例数据类
public class DemoData {
    @ExcelProperty("字符串标题")
    private String string;
    @ExcelProperty("日期标题")
    private Date date;
    @ExcelProperty("数字标题")
    private Double doubleData;
    @ExcelIgnore
    private String ignore;
}

// 填充要写入的数据
private static List data() {
    List list = new ArrayList<>();
    for (int i = 0; i < 10; i++) {
        DemoData data = new DemoData();
        data.setString("字符串" + i);
        data.setDate(new Date());
        data.setDoubleData(0.56);
        list.add(data);
    }
    return list;
}

public static void main(String[] args) {
    String fileName = "demo.xlsx";
    // 创建一个名为“模板”的 sheet 页，并写入数据
    FastExcel.write(fileName, DemoData.class).sheet("模板").doWrite(data());
}

```

