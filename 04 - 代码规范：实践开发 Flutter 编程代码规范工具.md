# 04 | 代码规范：实践开发 Flutter 编程代码规范工具

## 命名规范

命名规范中包括了文件以及文件夹的命名规范，常量和变量的命名规范，类的命令规范。Dart 中只包含这三种命名标识。

- AaBb 类规范，首字母大写驼峰命名法，例如 IsClassName，常用于类的命名。

- aaBb 类规范，首字母小写驼峰命名法，例如 isParameterName，常用于常量以及变量命名。

- aa_bb 类规范，小写字母下划线连接法，例如 is_a_flutter_file_name，常用于文件及文件夹命名。

## 注释规范

### 单行注释
单行注释主要是“ // ”这类标示的注释方法

### 多行注释
在 Dart 中由于历史原因（前后对多行注释方式进行了修改）有两种注释方式，一种是 /// ，另外一种则是 ` / **......* / ` 或者 ` /*......*/ ` ，这两种都可以使用。` /**......*/ ` 和 ` /*......*/ ` 这种块级注释方式在其他语言（比如 JavaScript ）中是比较常用的，但是在 Dart 中更倾向于使用 `///`.

### 注释文档生成
点击界面上的 Terminal 打开命令行窗口,运行 

```
dartdoc
```

## 库引入规范
Dart 为了保持代码的整洁，规范了 import 库的顺序。将 import 库分为了几个部分，每个部分使用空行分割。分为 dart 库、package 库和其他的未带协议头（例如下面中的 util.dart ）的库。其次相同部分按照模块的首字母的顺序来排列

```
import 'dart:developer';
import 'package:flutter/material.dart';
import 'package:two_you_friend/pages/home_page.dart';
import 'util.dart';
```

## 代码美化
可以使用命令：

```
dartfmt -h
```

flutter 代码可以使用命令：

```
flutter dartfmt -h
```

### [dartfmt](https://github.com/dart-lang/dart_style)

[dartfmt](https://github.com/dart-lang/dart_style) 工具的规范包括了以下几点：

- 使用空格而不是 tab；

- 在一个完整的代码逻辑后面使用空行区分；

- 二元或者三元运算符之间使用空格；

- 在关键词 , 和 ; 之后使用空格；

- 一元运算符后请勿使用空格；

- 在流控制关键词，例如 for 和 while 后，使用空格区分；

- 在 ( [ { } ] ) 符号后请勿使用空格；

- 在 { 后前使用空格；

- 使用 . 操作符，从第二个 . 符号后每次都使用新的一行。

## 工具化

在 Dart 中可以使用 ` dartanalyzer ` 来保证代码质量。
该工具（ dartanalyzer ）已经集成在 Dart SDK ，你只需要在 Dart 项目根目录下新增analysis_options.yaml 文件，然后在文件中按照规范填写你需要执行的规则检查即可，目前现有的检查规则可以参考 [Dart linter rules](https://dart-lang.github.io/linter/lints/) 规范。