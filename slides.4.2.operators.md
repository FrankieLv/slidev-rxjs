---
layout: two-cols
---

<template v-slot:default>

# Filtering
* skip
* distinct
* take

</template>
<template v-slot:right>

# Samples
- skip
  - https://stackblitz.com/edit/f8u2ms?devtoolsheight=50&file=index.ts
  - https://rxmarbles.com/#skip
- distinct
  - https://stackblitz.com/edit/ftikcs?devtoolsheight=50&file=index.ts
  - https://rxmarbles.com/#distinct
- take
  - https://stackblitz.com/edit/ydakos?devtoolsheight=50&file=index.ts
  - https://rxmarbles.com/#take


</template>

<!-- 
前面提到了，除了创建类的操作符是源头操作符， 其他类型的操作符都是要依赖一个上游的observerable对象，它们会对上游数据进行处理并且在新返回的observable对象中发送这些数据。

-->