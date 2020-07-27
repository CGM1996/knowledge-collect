### Redux

#### Store

#### State

#### Action

#### Action Creator

### HOOK

```js
 Hook 是一个特殊的函数，它可以让你“钩入” React 的特性
 什么时候我会用 Hook？ 如果你在编写函数组件并意识到需要向其添加一些 state，以前的做法是必须将其转化为 class。现在你可以在现有的函数组件中使用 Hook。
1. useState
2. useEffect
React 保证了每次运行 effect 的同时，DOM 都已经更新完毕。
Effect Hook  可以让你在函数组件中执行副作用操作
useEffect 做了什么？ 通过使用这个 Hook，你可以告诉 React 组件需要在渲染后执行某些操作。
与 componentDidMount 或 componentDidUpdate 不同，使用 useEffect 调度的 effect 不会阻塞浏览器更新屏幕，这让你的应用看起来响应更快。
```

### React.FC

```js
FC是FunctionComponent的简写, 这个类型定义了默认的 props(如 children)以及一些静态属性(如 defaultProps)
```



### 参考链接

[掘金](https://juejin.im/post/5cd7f2c4e51d453a7d63b715)

