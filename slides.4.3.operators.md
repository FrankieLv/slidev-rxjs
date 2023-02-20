---
layout: two-cols
---

<template v-slot:default>

# Transformation
* map
* scan
* buffer

</template>
<template v-slot:right>

# Samples
- map
  - https://stackblitz.com/edit/jr7qda?devtoolsheight=50&file=index.ts
  - https://rxmarbles.com/#map
- scan
  - https://stackblitz.com/edit/ndvtik?devtoolsheight=50&file=index.ts
  - https://rxmarbles.com/#scan
- buffer
  - https://stackblitz.com/edit/v7eh6o?devtoolsheight=50&file=index.ts
  - https://rxmarbles.com/#buffer


</template>

<!-- 
1. map - 没点击鼠标一次，上游是中的数据是事件对象，但是map只从对象中读取鼠标位置，然后返回的新的observable对象会将鼠标位置发送出去
2. scan - 它会从上游数据中，拿出当前数据，并将缓存起来的上一次计算计算结果，一起再一次进行计算，然后返回的新的observable对象会发送这一次的计算结果数据。
3. buffer - 它会缓存上游数据中的每一个数据到一个数组中， 同时使用另一个observable对象发送数据的频率，来控制发送缓存数组中的数据，并且同时清空数组中缓存的数据。

-->