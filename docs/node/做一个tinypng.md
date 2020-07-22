### chalk

chalk包的左右时修改控制台中字符串的样式,包括:
字体样式（加粗，隐藏等）、字体颜色、背景颜色

```
const chalk = require('chalk')
console.log(chalk.blue('Hello world!'))
console.log(chalk.bold.red('Hello world!'))
```

### 获取当前执行路径

```js
__dirname     获得当前执行文件所在目录的完整目录名
__filename    获得当前执行文件的带有完整绝对路径的文件名
process.cwd() 获得当前执行node命令时候的文件夹目录名 
./            文件所在目录
// process.cwd()是程序的执行路径，__filename和_dirname是js文件有的属性
// demo
console.log(process.execPath)
console.log(__dirname)
console.log(process.cwd())
```

### 命令行参数获取

```js
1. process.argv
node .\src\tiny.js -f hhh
console.log(process.argv)
[
  'C:\\Program Files\\nodejs\\node.exe',
  'D:\\code\\my\\anxin-tiny\\src\\tiny.js',
  '-f',
  'hhh'
] -f
```

```js
2. commander
npm i -S commander
// 使用
const { program } = require('commander')
program
  .version(tinyPackage.version, '-v, --version', '获取版本')
  .option('-f, --force', '是否覆盖')
  .option('-i, --imgs [imgs...]', '自定义想要压缩的图片img')
  // .requiredOption('-f, --force', 'force must have cheese')
  .parse(process.argv)、

console.log(program.opts())
// 执行 node .\src\tiny.js --imgs a b c
console.log(program.opts()) // { version: '1.0.0', force: undefined, imgs: [ 'a', 'b', 'c' ] }
```

### 用户交互 -inquirer

```js
// 交互式命令行工具
npm install inquirer

```



### 杂七杂八

```js
1. 获取文件大小
buffer.length
fs.statSync(filePath).size
2. 获取父级目录 path.resolve(process.execPath, '..')

// zl9LZpmhHsvYzTSTWBNFLrst9N4Lt0SZ
```



### 参考资料

> [手把手教你用node撸一个图片压缩工具](https://juejin.im/post/5bd350a76fb9a05d2d02697c)
> [require() 源码解读-阮一峰](http://www.ruanyifeng.com/blog/2015/05/require.html)
> [segmentfault-https请求tinypng](https://segmentfault.com/a/1190000015467084)
> [commanderjs-tj大神](https://github.com/tj/commander.js)





```js


```

