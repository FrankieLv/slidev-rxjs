# try-catch-finally
"try-catch-finally" does not work anymore
```ts {}

try{
  ajax('https://api.github.com/users?per_page=5').subscribe(response => console.log(response));
}catch(error){
 console.log("error" + error);
}finally{
 ...
}
```

<!-- 
1. js, ts的异常处理都是使用try-catch finally 关键字来进行异常处理， 它们只能对同步代码进行处理，但是，rxjs的更多的是用于异步编程， try-catch机制，对异步异常处理是无效的，即使使用F12打开调试工具，也是无能为力。
2. 在我们课程开头提到的，异步发送请求和加载数据， 通过这中间发生错误，比如网络异常等等，如下同步代码中使用trycatch是无法捕获异常的。
3. 那回到我们开头说的，函数式编程，它是强调用函数来讲问题分解并解决。那在rxjs的世界中，异常也是数据，它们也应该在数据流中流动，所以，rxjs定义了专门用于处理异常的操作符。

-->