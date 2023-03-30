# promise
1. 同步 会发生阻塞,异步 不会发生阻塞
2. js实现异步的两种形式，js单线程语言
   1. 回调函数，如setTimeout,容易产生回调地狱
   2. Promise,如fetch，AJAX,链式调用可以将多个异步操作串联起来，catch捕获错误，同步编程try/catch，链式调用中可以使用then,finally,all等
3. async/await async标记异步函数 await替代then,await只能使用在异步函数中