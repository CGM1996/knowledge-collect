## JSX
JS + XML 语法糖 需要Babel编译。Babel 会把 JSX 转译成一个名为 React.createElement() 函数调用。
注意，网页中实时将ES6代码转为ES5，对性能会有影响。生产环境需要加载已经转码完成的脚本。

## 插值表达式
* 表达式： 运行之后会返回一个值   
* 输出类型
    字符串 数字=》原样输出  
    布尔值 空 未定义 =》 忽略
## 条件输出
三元表达式、短路运输符&&
## 列表渲染
* jsx不能写循环语句for while
* 可以接受数组 arr.map(item => XXXxXX) 数组只能使用有返回值的api
* 对象 Object.keys(obj).map(item => XXX)

## 基于自动化的集成环境模式 create-react-app 脚手架

## 编辑器高亮

## JSX语法

```js
// jsx不是html,写法与html有区别
0. 只有一个顶层元素
1. 类名
className="div"
动态类名
3. 行内样式style接受一个对象
style={{color: 'red'}}
4. 列表渲染必须加key
5. 标签一定要闭合
6. 事件处理 onClick必须使用preventDefault 阻止默认行为
7. 谨慎对待JSX中的this.在JS中class的方法默认不会绑定this
破解方法：箭头函数、 class fields 语法
1). <div onClick={ () => this.handleClick }> </div>
2) handleClick = () => {
    console.log('this is:', this);
  }
8. 向事件处理程序传递参数
<button onClick={(e) => this.deleteRow(id, e)}>Delete Row</button>
<button onClick={this.deleteRow.bind(this, id)}>Delete Row</button>
```

## 组件

```js
0. 类式组件
必须要继承自React.component
必须要有render方法
1. 函数式组件 
props 从参数传入
在16.7之前，函数组件没有状态，只能用于纯渲染
16.7 Hooks
2. 组件的首字母大写，属性小写
3. setState修改组件数据， 不要直接通过this.state.XXX 修改数据
```

## 组件通信

```js
1. 父-》子 ： props
2. 子 -》 父 【单向数据流】： 调用方法
3. 同级
4. 跨组件通信 context 【面试考点】
import { createContext } from 'react'
createContext(defaultValue)
Context.provider 在父组件调用Provider传递数据
接受数据：
class.contextType = Context
static contextType = Context
Context.Consumer
```

## 生命周期

```js

```



## 添加事件

```js
1. 驼峰命名
2. 事件处理函数中的this,默认是undefined  =》 用箭头函数
```




## 需要看的
```js
1. createElement
React.js提供React.js的核心功能代码，如虚拟dom，组件
React.createElement(type, props, children)
ReactDOM 提供了与浏览器交互的DOM功能，如DOM渲染
ReactDOM.render(element, container, [, callback])
2. setState 每次在组件中调用 setState 时，React 都会自动更新其子组件。
```

## 杂七杂八学到的
```js
1. del * 删除文件夹下所有文件
2. vscode setting.json配置jsx自动闭合 "emmet.includeLanguages": {"javascript":"javascriptreact" }
3. import React { Component } from 'react'
```

## 参考链接
[Babel 入门教程 - 阮一峰](http://www.ruanyifeng.com/blog/2016/01/babel.html)  