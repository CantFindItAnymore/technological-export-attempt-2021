[仓库地址](https://github.com/CantFindItAnymore/koa2-test)

### 一. 初始化 

```js
const Koa = require('koa')

const app = new Koa()

app.listen(3000)
```



### 二. 中间件

```js
const Koa = require('koa')

const app = new Koa()

////////////////////////////////////// 方式一
// 中间件
const hello = () => {
  console.log('hello I\'m koa')
}

// 注册
app.use(hello)

////////////////////////////////////// 方式二
// ctx 上下文
// next 下一个中间件函数
// 打印顺序：1 3 4 2
app.use((ctx, next) => {
  console.log(1)
  next()
  console.log(2)
})

app.use((ctx, next) => {
  console.log(3)
  next()
  console.log(4)
})
/////////////////////////////////////////////

app.listen(3000)
```



### 三. 洋葱模型

### 四. 强制promise

### 五. 

