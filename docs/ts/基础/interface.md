## 官方解释
?>TypeScript的核心原则之一是对值所具有的结构进行类型检查。 它有时被称做“鸭式辨型法”或“结构性子类型化”。 在TypeScript里，接口的作用就是为这些类型命名和为你的代码或第三方代码定义契约。
接口是对 JavaScript 本身的随意性进行约束，通过定义一个接口，约定了变量、类、函数等应该按照什么样的格式进行声明，实现多人合作的一致性。TypeScript 编译器依赖接口用于类型检查，最终编译为 JavaScript 后，接口将会被移除。

## 语法
```js
// 语法格式
interface DemoInterface {
}
```

## 应用场景
在声明一个对象、函数或者类时，先定义接口，确保其数据结构的一致性。

## 接口的好处
在JS中：
```js
function getClothesInfo(clothes) {
  console.log(clothes.price)
}
let myClothes = {
  color: 'black', 
  size: 'XL', 
  price: 98 
}
getClothesInfo(myClothes)
```