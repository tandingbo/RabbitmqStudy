# 注意：这里的rpc 跟官方的rpc不是一样的
# 官方是使用 reply这种内置实现的  参考helloword-spring项目
# 这里直接采用  
 ## 1.主动方调用被动方，使用A队列，被动方消费A队列消息。同时主动方消费B队列，用来接受被动方远程调用的反馈。
 ## 2.被动方调用远程方法，并把结果通知到B队列。
 ## 3.A消费B队列消息
  
 ## 类似远程，其实原理一样。这样A和B队列可以分开管理，减少使用一个队列造成性能瓶颈。        

