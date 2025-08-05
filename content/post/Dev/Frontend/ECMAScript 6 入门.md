---
title: ECMAScript 6 入门
description: Notes for ECMAScript 6
slug: ecmascript
date: 2018-05-01
categories:
  - Development
tags:
  - Development
  - Frontend
  - JavaScript
---

# 1. ECMAScript 6 简介

ECMAScript 是标准

JavaScript 是实现

Babel 是转码器，a toolchain that is mainly used to convert ECMAScript 2015+ code into a backwards compatible version of JavaScript in current and older browsers or environments.

- 默认只转句法（syntax）
- 不转 API
- 转 API 需要用 core-js 和 regenrator-runtime

# 2. let 和 const 命令

var 全局声明

let 块级作用于声明

es6 有 6 种声明变量方法：var，function，let，const，import 和 class

顶层对象

- 浏览器里面，顶层对象是`window`，但 Node 和 Web Worker 没有`window`。
- 浏览器和 Web Worker 里面，`self`也指向顶层对象，但是 Node 没有`self`。
- Node 里面，顶层对象是`global`，但其他环境都不支持。

this

- 全局环境中，`this`会返回顶层对象。但是，Node.js 模块中`this`返回的是当前模块，ES6 模块中`this`返回的是`undefined`。
- 函数里面的`this`，如果函数不是作为对象的方法运行，而是单纯作为函数运行，`this`会指向顶层对象。但是，严格模式下，这时`this`会返回`undefined`。
- 不管是严格模式，还是普通模式，`new Function('return this')()`，总是会返回全局对象。但是，如果浏览器用了 CSP（Content Security Policy，内容安全策略），那么`eval`、`new Function`这些方法都可能无法使用。

ES2020 引入 globalThis 解决以上问题

# 3. 变量的解构赋值

解构可以定义默认值

解构数组、对象、字符串、数值和布尔值

解构函数参数

用途

- 交换变量的值
- 从函数返回多个值
- 函数参数的定义
- 提取 JSON 数据
- 函数参数的默认值
- 遍历 Map 结构
- 输入模块的指定方法

# 4. 字符串的扩展

# 5. 字符串的新增方法

- String.fromCodePoint() 不懂
- String.raw() 不懂
- codePointAt() 不懂
- normalize() 不懂
- includes(), startsWith(), endsWith()
- repeat()
- padStart(), padEnd()
- trimStart(), trimEnd()
- matchAll()
- replaceAll()

# 6. 正则的扩展

构造函数，第二个参数为修饰符（flag），会替换原有的修饰符

字符串的正则方法

- match()
- replace()
- search()
- split()

u 修饰符 不懂

y 修饰符类似 g 修饰符但是不同

flags 属性返回正则表达式的修饰符

...

需要继续研读此章节

# 7. 数值的扩展

二进制和八进制的表示方法 0b, 0o

Number.isFinite(), Number.isNaN() 只对数值有效，与全局 isFinite(), isNan()不同，全局会先调用 Number 把非数值转换为数值

Number.parseInt(), Number.parseFloat()移植到 Number 对象

Number.isInteger()，JavaScript 采用 64 位双精度格式存储数值，数值超过 53 个二进制位可能会误判

Number.EPSILON 极小常量

Number.isSafeInteger()

Math 方法

...

需要继续研读此章节
