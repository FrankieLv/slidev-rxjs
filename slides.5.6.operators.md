---
layout: two-cols
---

<template v-slot:default>

# 5.6 Error Handling
* catchError
* retry
* retryWhen
* tap

</template>
<template v-slot:right>

# Samples
- catchError
  - https://stackblitz.com/edit/mb4gky?devtoolsheight=50&file=index.ts
  - https://rxjs.dev/api/operators/catchError#description
- retry
  - https://stackblitz.com/edit/lxbvv1?devtoolsheight=50&file=index.ts
  - https://rxjs.dev/api/operators/retry#description
- retryWhen
  - https://stackblitz.com/edit/zytdcx?devtoolsheight=50&file=index.ts
  - https://rxjs.dev/api/operators/retryWhen#description
- tap
  - https://stackblitz.com/edit/vfn3pq?devtoolsheight=50&file=index.ts
  - https://rxjs.dev/api/operators/tap#description

</template>

<!-- 
1. catchError - 它返回的新的observable对象，只会把上游的正常数据原封不动的发送出去，但是会拦截处理上游的异常数据,并且不会再把异常数据发送到下游。
2. retry - 它是在拦截到上游的异常数据后，让上游的数据再重新走一遍，尝试是否可以恢复错误。 这种情况只适用于网络异常情况，但是对于代码错误是无能为力的。
3. retryWhen - retry是捕获异常后，立马进行重试，retryWhen提供了一种机制可以，控制重试的节奏，可以是在捕获异常数据后，延迟几秒在进行重试。 但是，这个操作符，会在v9，v10版本里合并到retry操作符中，retry会添加一个新参数实现相同功能。
4. tap - 它是用于调试用的，当有错误数据产生后，我们希望打印一些log信息进行分析，这个时候就需要tap了。 它返回的新的observable只是单纯的看一眼每个流经它的数据，不会做任何修改。
-->