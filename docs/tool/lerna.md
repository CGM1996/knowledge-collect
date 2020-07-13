### Monorepo vs Multirepo
Monorepo 的全称是 monolithic repository，即单体式仓库，与之对应的是 Multirepo(multiple repository)，这里的“单”和“多”是指每个仓库中所管理的模块数量。

Multirepo 是比较传统的做法，即每一个模块都单独用一个仓库来进行管理。典型案例[webpack](https://github.com/webpack/webpack)
Monorep 是把所有相关的 module 都放在一个仓库里进行管理，每个 module 独立发布，典型案例[babel](https://github.com/babel/babel/tree/master/packages)

### 参考链接
[参考](http://blog.runningcoder.me/2018/08/17/learning-lerna/)    
[掘金](https://juejin.im/post/5a989fb451882555731b88c2)