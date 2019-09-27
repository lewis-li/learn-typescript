# TypeScript

TypeScript 是 JavaScript 的超集.

它扩展了:
* 静态类型系统:严格的类型检查,以及为构建更良好的项目而增加的特性
* 将代码划分为设计时,运行时,最终转译为标准的 JavaScript

[toc]


## 项目:

### 类型声明空间

### 模块: 

使用文件模块,禁止全局模块
使用ES 模块语法

```
// export_file.ts

export { vars }

// import_file.ts

import { varName1, varName2, ...} from "./export_file"

```

确保导入
```
import foo = require('./foo');
import bar = require('./bar');
import bas = require('./bas');

const ensureImport: any = foo || bar || bas;
```

### 迁移

第三方代码: 在 [DefinitelyTyped](https://github.com/borisyankov/DefinitelyTyped) 找对应的声明文件或自己写一个.

第三方 NPM 模块

使用 @types

环境声明: 声明文件 d.ts

```
declare <name>: <type>
```

---


## 静态类型系统:

类型注解: 使用 ``` :TypeAnnotation ``` 语法

### 类型分类:
* JavaScript 提供的类型 (略)
* TypeScript 扩展的类型
  * interface
  * 特殊类型
    * any
    * null
    * undefined
    * void
  * 范型
  * 联合类型 ``` : type1 | type2 ```
  * 交叉类型 
  * 元组类型 ``` : [type1, type2] ```
  * 类型别名

### 接口,内联注解

### 枚举

```
// 值都是数字类型
enum <name> {
    <nam1>,
    <name2>,
    <name3>
}

// 或
enum <name> {
    <name1>,
    <name2> = <value> :int | string
}
```

### 函数

* 参数
    * 注解
    * 可选参数
    * 函数重载
* 返回值
    * 注解

### 可调用的

可实例化: 可调用的一种情况

```
interface <name> {
    new (): <type>
}
```

### 类型断言

```
    <name> = <value> as <type>
```

类型断言被认为是有害的

### Freshness 字面量检查

### 类型保护

* typeof
* instanceof
* in
* 字面量
* 自定义: 自定义函数实现自定义类型保护

### 字面量类型

### readonly

### 范型

为成员提供约束,成员可以是:
* 类的实例成员
* 类的方法
* 函数参数
* 函数返回值

### 类型推断

使用场景:
* 变量定义,函数返回值,赋值,结构化
* 解构
* 类型保护

### Never

### ThisType

---



## 编译: 转译为阅读友好的 JavaScript

todo

---