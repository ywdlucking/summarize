##同步 vs 异步
**同步I/O** 每个请求必须逐个地被处理，一个请求的处理会导致整个流程的暂时等待，这些事件无法并发地执行。用户线程发起I/O请求后需要等待或者轮询内核I/O操作完成后才能继续执行。

**异步I/O** 多个请求可以并发地执行，一个请求或者任务的执行不会导致整个流程的暂时等待，当内核I/O操作完成后会通知用户线程

##阻塞 vs.非阻塞
**阻塞** 某个请求发出后，由于该请求操作需要的条件不满足，请求操作一直阻塞，不会返回，直到条件满足。
**非阻塞** 请求发出后，若该请求需要的条件不满足，则立即返回一个标志信息告知条件不满足，而不会一直等待。


##差异性
同步和异步着重点在于多个任务执行过程中，后发起的任务是否必须等先发起的任务完成之后再进行。而不管先发起的任务请求是阻塞等待完成，还是立即返回通过循环等待请求成功，而阻塞和非阻塞重点在于请求的方法是否立即返回。