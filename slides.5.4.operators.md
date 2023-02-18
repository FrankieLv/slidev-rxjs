---
layout: two-cols
---

<template v-slot:default>

# 5.1 Combination
* concat
* merge
* zip

</template>
<template v-slot:right>

# Samples
- concat
  - https://stackblitz.com/edit/yri4uj?devtoolsheight=50&file=index.ts
  - https://rxmarbles.com/#concat
- merge
  - https://stackblitz.com/edit/zqm447?devtoolsheight=50&file=index.ts
  - https://rxmarbles.com/#merge
- zip
  - https://stackblitz.com/edit/ngr4nu?devtoolsheight=50&file=index.ts
  - https://rxmarbles.com/#zip


</template>

<!-- 
1. concat - 它是将多个上游数据流进行收尾相连，新返回的observerable对象会依次发送相连后所有的数据。
2. merge - 它是将多个上游数据流中的每个数据，进行交叉组合，新返回的observable对象会依次发送交叉后的所有数据。
3. zip - 它是将多个上游数据流中的每个相同位置的数据，组合为一个数组，新返回的observable对象会依次发送所有的数组数据

-->