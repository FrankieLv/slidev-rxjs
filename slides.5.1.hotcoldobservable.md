---
layout: two-cols
---

<template v-slot:default>

# Hot Observerable 

<img src="/images/TV.png" class="m-1 h-60 rounded shadow" />

</template>
<template v-slot:right>

# Cold Observerable 

<img src="/images/AiQiYi.png" class="m-1 h-60 rounded shadow" />

</template>

<!-- 
1. 还有两个概念，我们需要再进一步的讲解一下，hot observable和cold observable
2. 当我们收看电视的直播节目时候， 每家通过切换同一个节目的时间可能是不一样的， 有的早一些，有的晚一些， 因为是直播，所以晚一些的人是无法看到早一些直播的内容，他只能从当前时间点开始观看。那这个就是一个hot observable的概念，电视台的直播就可以类比成hot observable。
3. 当我们使用爱奇艺追剧的时候，即使每个人开始追剧的时间不一样，但是每个人都可以从第一集开始看。AiQiYi可以为每个人都从头开始播放剧集，那我们就可以把爱奇艺类比成一个cold observable。
4. 理解了这一点很重要，一会会讲到多播，和这两个概念息息相关。
-->

---

# Cold Observable
Example Link: https://stackblitz.com/edit/7znxxw?devtoolsheight=50&file=index.ts 
```ts {}
import { interval, take } from 'rxjs';

const numbers = interval(1000).pipe(take(4));

numbers.subscribe((x) => console.log('Observer1: ', x));

setTimeout(() => {
  numbers.subscribe((x) => console.log('Observer2: ', x));
}, 3000);
```

Output:
> Observer1: 0
> Observer1: 1
> Observer1: 2

> Observer2: 0
> Observer2: 1
> Observer2: 2

<!-- 
两个observer是在不同时间订阅observable的，但是每一个observer都可以接受到全部的信息。
-->
---

# HotObservable

- fromPromise
- fromEvent
- ...

<!-- 
一些操作符产生的observable对象是hot observable，什么是操作符，我们马上就会讲到。 刚才同样的代码用这个操作符产生的hotobservable去运行， 那第二个observer对象只能接收到2秒后发布出来的数据，而接收不到在两秒之前的数据。
-->