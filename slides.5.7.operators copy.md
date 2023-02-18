---
layout: two-cols
---

<template v-slot:default>

# 5.1 Utitlity
* defer

</template>
<template v-slot:right>

# Samples
- defer
  - https://stackblitz.com/edit/eqcsys?devtoolsheight=50&file=index.ts
  - https://rxjs.dev/api/index/function/defer#description

</template>

<!-- 
1. 我们之前提到，我们先创建了observable对象，但是，在没有observer对象订阅它时，它不会发送出去数据。但是这个时候，observerable对象已经创建好了，相当于提前预定了行为，只是没有发送数据而已。
2. defer - 但是defer创建的observable对象，实际上还没有真正的创建出来，它只有在有observer对象定义它时候，才会真的创建这个对象，再发送数据。
3. 大家可能会有个疑问，这么做的意义在哪？
4. 回到我们之前说的那个异步发送请求的例子中，在用ajax操作符创建observerable对象时，http请求就已经被发送出去了，只是从后端获取到的数据没有向下游发送而已，在有observer订阅后，再将后端返回的数据发送出去。这样，产生的一个问题就是应用程序根据业务流程的变化，有可能不需要查询后端数据了，但是这个时候，后端已经发送请求去获取数据了，这就造成了资源浪费。
5. 所以在这种情况下，是应该使用defer操作符来创建一个observable对象的代理对象，只有在真正订阅时候，在创建真实的observable对象，去请求数据。
-->