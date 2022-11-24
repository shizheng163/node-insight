- NodeJs的Event深入展开
- NodeJs的Stream深入展开

```js
const http = require('http');
http.createServer(function h1() {
  console.log('请求回调');
});
```

上述代码中，回调函数是怎么是如何触发的。
调用createServer返回了什么东西, 这是一个什么异步任务
我们知道SetTimeout，SetInterval生成的是一个计时器任务
CreateServer生成的是一个什么异步任务呢，他给内核注册了什么接口，使可以在有数据请求的时候调用回调
CreateServer后等待用户连接生成的是什么任务，他的底层是怎么实现的。