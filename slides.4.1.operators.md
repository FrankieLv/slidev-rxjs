---
layout: two-cols
---

<template v-slot:default>

# Creation
* of
* interval
* fromEvent
* fromPromise

</template>
<template v-slot:right>

# Samples
- of
  - https://stackblitz.com/edit/sjgacb?devtoolsheight=50&file=index.ts
  - https://rxmarbles.com/#of
- interval
  - https://stackblitz.com/edit/nbwpfv?devtoolsheight=50&file=index.ts
  - https://rxmarbles.com/#interval
- fromEvent
  - https://stackblitz.com/edit/7puus8?devtoolsheight=50&file=index.ts
  - https://rxjs.dev/api/index/function/fromEvent#description


</template>

<!-- 
1. 我们先回想一下， 我们在上面有一个例子中是我们自己写new obervable的代码去创建一个observable对象的， 如果说真的需要开发人员频繁去写这样的代码去创建observable对象并且定义发送数据的行为，那Rxjs的存在就毫无意义了，我们可以自己实现这种模式，还需要它干什么呢。 但是，实际上Rxjs已经给我们封装好了很多很多的函数，这些函数会去创建observable对象并定义好发送数据的行为，这些函数几乎覆盖了我们项目所需的所有场景。我们只需要直接使用这些函数去获得observable对象，然后创建observer对象去接收并处理数据就好了。 这些内置的函数，就称之为操作符。真实项目开发中，这些操作符已经做够我们使用，不需要创建新的操作符。
2. 操作符有很多种类， 我们简单的介绍几种，并且看下样例。
- Creation： 就像我们刚才使用的of，interval之类的， 它是创建可以提供数据源的observerable。
- Filtering：剩下的这些操作符，都是对上游的observable对象中的数据进行再加工，并且返回一个新的observable对象。那filtering，就是对数据做过滤，将不符合条件的数据剔除掉，新生成的observable对象只会发送符合条件的数据。
- Transformation： 转换类，就是对数据进行加工，比如可以在接收到上游的数据1,2,3 后， 将它们都乘以2，在返回的新的observable对象中发送这些新的数据。
- Combination： 合并类，是对两个observable对象中的数据进行合并，返回的新的observable对象会发送合并后的数据。
3. 我们先来看一下创建类的操作符。

4. 对弹珠图解释一下， 为了更好的理解数据流中数据的状态， 我们通常会使用弹珠图去理解。 我们知道一个observable对象，有三种状态，处理状态，正常完结状态和异常完结状态， 在这个图中，一个个圆圈代表的数据处理的正常状态，如果遇到了竖线，代表是正常完结状态，遇到红叉，是异常完结状态。

5. 并不是所有的obsevable对象都有正常完结状态，比如上面的 fromEvent, 就是一个永不完结的observable， 因为只要程序运行期间，用户就有可能有点击操作，只要有点击操作，程序就需要处理产生的数据。所以是个永不完结的状态。

-->