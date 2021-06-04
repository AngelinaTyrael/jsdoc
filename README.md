# jsdoc-js注释

注释用于解释 JavaScript 代码，增强其可读性。

## 基本使用

```js
/**
 * 
 * 
 */
```
- 每一行第一个*要对齐
- 内容行的*与内容要有一个空格

## 常用标签
### @alias 函数与变量别名

```js
(function () {
  /**
   * @alise test
   */ 
  window.test = test
})();
```
```js
function test () {

  a += 1;

  return function () {
    return a * a;
  }
}

/**
 * @alise test1 - test
 */ 
const test1 = test(5)
```
### @constructor 构造函数

```js
;(function () {

  /**
   * @constructor Test
   */ 
  var Test = function () {

  }

})();
```

```js
class Test {
  /**
   * @constructor Test
   */
  constructor() {

  }
}
```
### @description 描述

```js
/**
 * @description 这是一个HTML模板替换函数
 */ 
function telReplace (template, replaceObject) {
  /**
   * @description
   * 描述
   */
}
```

### @example 例子

```js
/**
 * @example
 * var t = new Test(1, 2)
 * t.plus() // 1 + 2的结果
 */ 
function Test (a, b) {
  this.a = a;
  this.b = b;
}

Test.prototype.plus = function () {
  return this.a + this.b
}
```
### @extends 继承关系

```js
import React, { Component } from 'react'

/**
 * @extends { React.Component }
 * @description 继承
 */  
class Test extends Component {

}

export default Test;
```
### @param 参数

```js
/**
 * @description 这是一个做加法运算的函数
 * @param {number} a - 是加法中的第一个数字
 * @param {number} b - 是加法中的第二字数字
 * @return
 */
function test (a, b) {
  return a + b;
}

// number
// string
// boolean
// function
// undefined

// object
// Array
// Object
// Null
```
### @property  属性

```js
/**
 * @property {string} type - 轮播图组件的类型
 * slide(default): 无缝轮播
 * fade: 淡入淡出
 * @property {number} duration - 轮播图轮播等待时间
 * @property {boolearn} autoplay - 轮播图是否自动轮播
 */ 
var obj = {
  type: 'slide',
  duration: 3000,
  autoplay: true
}
```
### @return 返回值 无返回值return void

```js
/**
 * @description 这是一个做加法运算的函数
 * @param {number} a - 是加法中的第一个数字
 * @param {number} b - 是加法中的第二字数字
 * @return a + b的结果
 */
function test (a, b) {
  return a + b;
}
```
### @type 变量类型

```js
var a = 1;
var b = 's';
var c = true
var d = function () {}
/**
 * @type {number} a - xxxx
 * @type {string} b - xxxx
 * @type {boolean} c - xxxx
 * @type {function} d - xxxx
 */
```
```js
/**
 * @type {Array.<number>} arr - xxxx
 * @type {number[]} arr - xxxx
 */
const arr = [1, 2, 3, 4]
```
### @access 访问等级
```js

class Test {
  /**
   * @access private a - 私有
   */
  #a = 0;

  constructor () {
    /**
     * @access private b - 私有
     * @access public c - 公共
     */
    this._b = 1;
    this.c = 2;
  }
}
```
### @author 作者
```js
/**
 * @author AngelinaTyrael <lucky18209714890@gmail.com>
 */ 
```
### @borrows 改变标识符
### @callback 回调函数
```js
function Test () {}

/**
 * @param {Test~testCallback} cb
 */
Test.prototype.a = function (cb) {
  cb();
}

/**
 * @callback Test~testCallback
 */
function b () {}
```
### @class
```js
/**
 * @class Test - xxxxx
 * @classdesc xxxxx
 */
class Test {

}
```
### @constant 常量
```js
/**
 * @constant {string}
 * @description xxx
 */
const TEST = 'test'       
```
### @file 文件描述 和 @copyright
```js
/**
 * @file xxx
 * @copyright xxx
 */ 
```
### @requires 模块依赖
```js
/**
 * @requires module:html-webpack-plugin
 * @description xxx
 */
const HtmlWebpackPlugin = require('html-webpack-plugin');
```