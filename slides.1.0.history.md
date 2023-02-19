---
layout: center
---

# 1 - Reactive Programming & Function Programming

---

# Reactive Programming

<img src="/images/huanghe.png" class="m-1 h-60 rounded shadow" />
<!-- 
1. 响应式编程是基于数据流和对数据流中数据发生的变化(变化传递)做出响应的编程范式。
2. 简单说，可以把这个过程想象为，一条河流，河流总有一个源头，河水在河床中流淌，下游的人们对河水有不同的用途。
3. 诞生之初主要用于解决异步问题.
2. 什么是异步，可以简单举个例子给大家理解下：
我们访问一个web页面， 最终页面上会将数据以一种优美的格式显示出来。
a. 如果程序是同步的处理这个过程，会是什么样子，它会先发请求到服务器后端，拿到数据后，在将数据以一种优雅的排版渲染在页面上。 如果这个数据量是巨大的，需要耗时很久才能返回，那我们能看见的就是一个空白页面，这是一种非常不好的用户体验。
b. 那异步的过程，就是程序发送请求到后端后，它会直接进行页面渲染的代码而不等待后端数据返回后在渲染页面，只不过因为此时还没有真正的数据，所以会显示一些友好的提示信息，诸如：小主耐心等待，我骑着我心爱的小摩托，奋力加载. 在数据放回后，程序会再将数据渲染到页面上，我们把这个发送请求和随后的数据渲染过程，称之为异步。
3. 那响应式编程，就是一种异步编程模型，用来解决异步处理数据和响应的问题。
4. Rxjs是实现响应式编程的一个工具。
5. Rx的概念最初是由微软公司实现并开源，也就是Rx.NET. 因为Rx带来的编程方式大大改进了异步编程模型，后续C++的RxCpp还有Ruby的Rx.rb, Python的RxPy，还有Java的RxJava。
-->
---

# Function Programming
Functional programming is a way of programming that places great importance on using functions to solve problems

Object oriented programming: command
```ts {}
function addone(arr){
    const = results = [];
    for(let i = 0; i < arr.length; i++>){
        result.push(arr[i] + 1);
    }
    return results;
}
```

Functional programming: declarative
```ts {}
function addone(arr){
    return arr.map( arr => arr.map(item => item + 1) )
}
```

<!--
1. 函数式编程就是非常强调使用函数来解决问题的一种编程方式。与之对应的就是面向对象编程。可以通过一个小例子来理解，什么是函数式编程：
2. 因为函数式编程天然契合响应式，所以我们今天的主角Rxjs同时具有了响应式和函数式的特性。
-->

---
layout: center
---
# Is functional programming a new concept?
<!-- 
说来话长， 想当年，阿兰*图灵和冯*诺依曼祖师爷创立计算机这么学科，因为前无古人，所以最早一批学者都有其他专业的背景。

数学家提出的编程语言模型自然具有存数学的气质，阿隆佐*邱奇，在计算机诞生之初就提出了lambda演算的概念，也就是用纯函数的组合来描述计算过程。

当时的硬件技术很不发达，电子原件没有当今这样的水平，而函数式编程想要实现，只能通过一层软件模拟来复现数学家设想，这多出来的一层无疑要耗费性能，所以光是性能一个因素，就让函数式编程难以实践推广。

但是，现如今硬件早已今非昔比，芯片发展转为多喝，软件架构也想分布式方向发展。函数式编程比命令式更加适合于分布式计算场景。随着CPU性能和存储设备性能的提高，当初导致函数式编程性能问题，现在都不是问题了，这也是给函数式编程崛起增加了助推力。
-->
