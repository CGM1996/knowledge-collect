# 类型

## 基本类型 & 对象类型
ts中的原始类型：boolean, string, number, void, null, undefined, symbol, bigint

ts中的对象类型：元组tuple, 枚举enum, 任意 any, unknown,never, 数组Array,对象 object
### 变量声明
> 变量声明语法：冒号 : 前面是变量名称，后面是变量类型。
### demo 原始类型
```js
// boolean
const flag: boolean = true
// number
const num: numebr = 3,
    notNum: number = NaN
// string
const str: string = 'i am a string'
const modelStr: string = `hhh${str}`
// void: 当一个函数没有返回值时，可以将其返回值类型定义为 void
function doNothing(): void {
  let a  = 10
}
// 声明一个 void 类型的变量没有什么用，因为你只能将它赋值为 undefined 和 null：
let nothing: void = undefined
// null & undefined

```
### demo 对象类型
```js
// 数组类型 2种表示方法 =》推荐使用第一种，比较简洁
let list: number[] = [1, 2, 3] 
let namrArr: string[] = ['llhe', 'cgm']
let list1: Array<number> = [1, 2, 3]
// 混合各种元素类型
let list3: any[] = ['llhe', 2020]

// any
//有时候接收来自用户的输入，我们是不能确定其变量类型的。这种情况下，我们不希望类型检查器对这些值进行检查，而是直接让它们通过编译阶段的检查，此时可以使用 any
let input: any = 'nothing'
// 如果一个数据是 any 类型，那么可以访问它的任意属性，即使这个属性不存在
input.onfocus() // 不会报错
```

## 注意
* TypeScript 中描述类型要用 小写。
* 不要滥用 any !