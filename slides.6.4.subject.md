# Multi Operators - Others


- share() [Rxjs Guide](https://rxjs.dev/api/operators/share)]
- publishLast() [Rxjs Guide](https://rxjs.dev/api/operators/publishLast)
- publishReplay() [Rxjs Guide](https://rxjs.dev/api/operators/publishReplay)
<!--
1. multicast() 操作符 - 我们一般不会使用它去直接开发， 它更多的是用于创建其他的操作符，比如这些share()操作符等。
2. share() - 操作符返回一个普通的observerable对象可以直接被拿来被其他observer订阅实现广播， 它其实就是调用了multicast().refCount()返回的observable对象。
3. publishLast() - 操作符中使用了一个特殊的AysncSubject(Subject的子类),它会取到源头的最后一个数据，然后发送到下游。
4. publishReplay() - 操作符中使用了一个特殊的ReplaySubject（Subject的子类），它就是实现了录播的功能，可以直接一个size的参数，它会将上游的数据缓存起来，并且将这些数据发送给那些没有赶上直播的观众。
-->