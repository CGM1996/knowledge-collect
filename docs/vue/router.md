### 迷惑的点
#### router 与 route
1. router为VueRouter实例，`只写对象`,想要导航到不同url,则使用router.push方法
```js
// router
// this.$router.push()
// this.$router.replace()
// this.$router.go()
```
2. route为当前router跳转对象,路由信息对象,`只读对象`,里面可以获取name、path、query、params等
```js
// route
// this.$route.query
// this.$route.params
```

#### params 与 query
1. params 
刷新页面params丢失
```js
// 传参: 
this.$router.push({ name: 'index' params:{ id }})
// 接收参数:
this.$route.params.id
// url的表现形式(url中没有参数) http://localhost:8080/#/index
```
2. query
刷新页面query不丢失
```js
// 传参
this.$router.push({ path: '/index' query:{ id }})
//接收参数
this.$route.query.id
// url的表现形式(url中带有参数) http://localhost:8080/#/index?id=1
```
!> params传参,push里面只能是 name:'xx',不能是path:'xx',因为params只能用name来引入路由,如果这里写成了path,接收参数页面会是undefined

### 编程式导航
#### router.push(location, onComplete?, onAbort?)
想要导航到不同的 URL，则使用 router.push 方法。这个方法会向 history 栈添加一个新的记录，所以，当用户点击浏览器后退按钮时，则回到之前的 URL。  
当你点击 <router-link> 时，router.push会在内部调用，所以说，点击 <router-link :to="..."> 等同于调用 router.push(...)。  
```js
// 字符串
router.push('home')
// 对象
router.push({ path: 'home' })
// 命名的路由
router.push({ name: 'user', params: { userId: '123' }})
// 带查询参数，变成 /register?plan=private
router.push({ path: 'register', query: { plan: 'private' }})
```

| 声明式                    | 编程式             |
| ------------------------- | ------------------ |
| `<router-link :to="...">` | `router.push(...)` |

#### router.replace(location, onComplete?, onAbort?)
跟 router.push 很像，唯一的不同就是，它不会向 history 添加新记录，replace会替换掉当前的 history 记录。

| 声明式                            | 编程式              |
| --------------------------------- | ------------------- |
| `<router-link :to="..." replace>` | `router.replace(..` |

#### router.go(n)
在 history 记录中向前或者后退多少步，类似 window.history.go(n)。
```js
// 在浏览器记录中前进一步，等同于 history.forward()
router.go(1)
// 后退一步记录，等同于 history.back()
router.go(-1)
```