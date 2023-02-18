# 2.1 Rxjs

# https://rxjs.dev

<img src="/images/Rx_Logo.png" class="m-1 h-60 rounded shadow" />

<!-- 
1. Rxjs是实现响应式编程的一个工具。
2. Rx的概念最初是由微软公司实现并开源，也就是Rx.NET. 因为Rx带来的编程方式大大改进了异步编程模型，后续C++的RxCpp还有Ruby的Rx.rb, Python的RxPy，还有Java的RxJava。
3. 很多东西都是触类旁通的，将一门精通之后，再学习其他的会轻松自在很多。
4. 这是Rxjs的官方网站，目前最新的版本是v7.8. 因为从v5版本，它做了很大的改动，所以网上很多的blog，教程等给出的代码是旧版本的代码，已经是过时的东西，大家在后续自学的时候，需要结合官方文档，有辨别性的学习。
-->
---

# 2.2 A Simple Running Example

Example Link: 
https://stackblitz.com/edit/rxjs-ddvox5?file=README.md

```ts {}
import { of, map, Observable } from 'rxjs';

of('Hello World')
  .pipe(map((name) => `Hello, ${name}!`))
  .subscribe(console.log);
```


Output:
```ts {}
Hello, Hello World!
```


<!-- 
1. 可以使用画笔，讲述一下， of源头， 中间在管道中使用map()函数处理数据，最终，通过将数据输出到控制台作为响应。
2. 在之前上一届的培训中，发现指导每一个人去在本地搭建开发环境是非常浪费时间的， 所以，我们会使用这个cloudIDE提供好的开发环境，这样同学可以更加的关注于rxjs本身的内容上，而不用浪费时间在环境搭建与调试上。
3. 每个人可以，打开“https://stackblitz.com” 新建一个rxjs的项目， 可以用于练习课上的实例代码。
-->