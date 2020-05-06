# 总结
宿主发起的任务称为宏任务，把JavaScript引擎发起的任务称为微任务。许多的微任务的队列组成了宏任务。循环执行宏任务，就是事件循环。
## 宏任务
+ script
+ mousemove等UI事件
+ setTimeout/setInterval
当JS引擎忙于执行宏任务时，宏任务就会形成一个队列，直到上一个宏任务执行完成，才会继续执行宏任务队列中的任务。
比如，当JS引擎忙于执行外部script脚本时，此时界面触发了鼠标移动事件，然后又触发了计时器，这时候，鼠标移动事件和计时器会形成宏任务队列，等待执行。

## 微任务
+ then
+ catch
+ finally

## 事件循环
事件循环不属于JavaScript引擎实现的东西，而是由浏览器或nodejs宿主环境实现的。事件循环是说，js引擎等待宏任务并执行，然后继续等待宏任务并执行的循环过程。
```js
function sleep(duration) {
  return new Promise(function(resolve, reject) {
    console.log("b");
    setTimeout(resolve,duration);
  })
}
console.log("a");
sleep(5000).then(()=>console.log("c")); // 先后输出a, b, c
````
