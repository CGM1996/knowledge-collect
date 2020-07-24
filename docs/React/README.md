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
## 参考链接
[Babel 入门教程 - 阮一峰](http://www.ruanyifeng.com/blog/2016/01/babel.html)  
