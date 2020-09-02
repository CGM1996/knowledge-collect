## mixin
混入。分发组件中的可复用功能。mixin 可包含
### 单个组件混入
```js
const mixin = {
  methods: {
    sayHello() {
      console.log('hello')
    }
  }
}

const vm = new Vue({
  mixins: [mixin],
  methods: {
    callHello() {
      this.sayHello() // hello
    }
  }
})
```

### 全局混入
```js
Vue.mixin({
  created: function () {
    console.log('created')
  }
})

```
!> 全局混入，因为它会影响每个单独创建的 Vue 实例 (包括第三方组件)。 慎用乃至不用！推荐使用插件完成全局功能。

## 插件
插件通常用来为vue添加全局功能。