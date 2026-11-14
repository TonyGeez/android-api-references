# java.util.concurrent

# java.util.concurrent

## Interfaces

| [BlockingDeque](../java/util/concurrent/BlockingDeque.md) | A [Deque](../java/util/Deque.md) that additionally supports blocking operations that wait for the deque to become non-empty when retrieving an element, and wait for space to become available in the deque when storing an element. |
| --- | --- |
| [BlockingQueue](../java/util/concurrent/BlockingQueue.md) | A [Queue](../java/util/Queue.md) that additionally supports operations that wait for the queue to become non-empty when retrieving an element, and wait for space to become available in the queue when storing an element. |
| [Callable](../java/util/concurrent/Callable.md) | A task that returns a result and may throw an exception. |
| [AsynchronousCompletionTask](../java/util/concurrent/CompletableFuture.AsynchronousCompletionTask.md) | A marker interface identifying asynchronous tasks produced by`async`methods. |
| --- | --- |
| [CompletionService](../java/util/concurrent/CompletionService.md) | A service that decouples the production of new asynchronous tasks from the consumption of the results of completed tasks. |
| [CompletionStage](../java/util/concurrent/CompletionStage.md) | A stage of a possibly asynchronous computation, that performs an action or computes a value when another CompletionStage completes. |
| [ConcurrentMap](../java/util/concurrent/ConcurrentMap.md) | A [Map](../java/util/Map.md) providing thread safety and atomicity guarantees. |
| --- | --- |
| [ConcurrentNavigableMap](../java/util/concurrent/ConcurrentNavigableMap.md) | A [ConcurrentMap](../java/util/concurrent/ConcurrentMap.md) supporting [NavigableMap](../java/util/NavigableMap.md) operations, and recursively so for its navigable sub-maps. |
| [Delayed](../java/util/concurrent/Delayed.md) | A mix-in style interface for marking objects that should be acted upon after a given delay. |
| [Executor](../java/util/concurrent/Executor.md) | An object that executes submitted [Runnable](../java/lang/Runnable.md) tasks. |
| --- | --- |
| [ExecutorService](../java/util/concurrent/ExecutorService.md) | An [Executor](../java/util/concurrent/Executor.md) that provides methods to manage termination and methods that can produce a [Future](../java/util/concurrent/Future.md) for tracking progress of one or more asynchronous tasks. |
| [Processor](../java/util/concurrent/Flow.Processor.md) | A component that acts as both a Subscriber and Publisher. |
| [Publisher](../java/util/concurrent/Flow.Publisher.md) | A producer of items (and related control messages) received by Subscribers. |
| --- | --- |
| [Subscriber](../java/util/concurrent/Flow.Subscriber.md) | A receiver of messages. |
| [Subscription](../java/util/concurrent/Flow.Subscription.md) | Message control linking a [Publisher](../java/util/concurrent/Flow.Publisher.md) and [Subscriber](../java/util/concurrent/Flow.Subscriber.md). |
| [ForkJoinWorkerThreadFactory](../java/util/concurrent/ForkJoinPool.ForkJoinWorkerThreadFactory.md) | Factory for creating new [ForkJoinWorkerThread](../java/util/concurrent/ForkJoinWorkerThread.md) s. |
| --- | --- |
| [ManagedBlocker](../java/util/concurrent/ForkJoinPool.ManagedBlocker.md) | Interface for extending managed parallelism for tasks running in [ForkJoinPool](../java/util/concurrent/ForkJoinPool.md) s. |
| [Future](../java/util/concurrent/Future.md) | A represents the result of an asynchronous computation. |
| [RejectedExecutionHandler](../java/util/concurrent/RejectedExecutionHandler.md) | A handler for tasks that cannot be executed by a [ThreadPoolExecutor](../java/util/concurrent/ThreadPoolExecutor.md). |
| --- | --- |
| [RunnableFuture](../java/util/concurrent/RunnableFuture.md) | A [Future](../java/util/concurrent/Future.md) that is [Runnable](../java/lang/Runnable.md). |
| [RunnableScheduledFuture](../java/util/concurrent/RunnableScheduledFuture.md) | A [ScheduledFuture](../java/util/concurrent/ScheduledFuture.md) that is [Runnable](../java/lang/Runnable.md). |
| [ScheduledExecutorService](../java/util/concurrent/ScheduledExecutorService.md) | An [ExecutorService](../java/util/concurrent/ExecutorService.md) that can schedule commands to run after a given delay, or to execute periodically. |
| --- | --- |
| [ScheduledFuture](../java/util/concurrent/ScheduledFuture.md) | A delayed result-bearing action that can be cancelled. |
| [ThreadFactory](../java/util/concurrent/ThreadFactory.md) | An object that creates new threads on demand. |
| [TransferQueue](../java/util/concurrent/TransferQueue.md) | A [BlockingQueue](../java/util/concurrent/BlockingQueue.md) in which producers may wait for consumers to receive elements. |
| --- | --- |

## Classes

| [AbstractExecutorService](../java/util/concurrent/AbstractExecutorService.md) | Provides default implementations of [ExecutorService](../java/util/concurrent/ExecutorService.md) execution methods. |
| --- | --- |
| [ArrayBlockingQueue](../java/util/concurrent/ArrayBlockingQueue.md) | A bounded [blocking queue](../java/util/concurrent/BlockingQueue.md) backed by an array. |
| [CompletableFuture](../java/util/concurrent/CompletableFuture.md) | A [Future](../java/util/concurrent/Future.md) that may be explicitly completed (setting its value and status), and may be used as a [CompletionStage](../java/util/concurrent/CompletionStage.md), supporting dependent functions and actions that trigger upon its completion. |
| [ConcurrentHashMap](../java/util/concurrent/ConcurrentHashMap.md) | A hash table supporting full concurrency of retrievals and high expected concurrency for updates. |
| --- | --- |
| [ConcurrentLinkedDeque](../java/util/concurrent/ConcurrentLinkedDeque.md) | An unbounded concurrent [deque](../java/util/Deque.md) based on linked nodes. |
| [ConcurrentLinkedQueue](../java/util/concurrent/ConcurrentLinkedQueue.md) | An unbounded thread-safe [queue](../java/util/Queue.md) based on linked nodes. |
| [ConcurrentSkipListMap](../java/util/concurrent/ConcurrentSkipListMap.md) | A scalable concurrent [ConcurrentNavigableMap](../java/util/concurrent/ConcurrentNavigableMap.md) implementation. |
| --- | --- |
| [ConcurrentSkipListSet](../java/util/concurrent/ConcurrentSkipListSet.md) | A scalable concurrent [NavigableSet](../java/util/NavigableSet.md) implementation based on a [ConcurrentSkipListMap](../java/util/concurrent/ConcurrentSkipListMap.md). |
| [CopyOnWriteArrayList](../java/util/concurrent/CopyOnWriteArrayList.md) | A thread-safe variant of [java.util.ArrayList](../java/util/ArrayList.md) in which all mutative operations (`add`,`set`, and so on) are implemented by making a fresh copy of the underlying array. |
| [CopyOnWriteArraySet](../java/util/concurrent/CopyOnWriteArraySet.md) | A [Set](../java/util/Set.md) that uses an internal [CopyOnWriteArrayList](../java/util/concurrent/CopyOnWriteArrayList.md) for all of its operations. |
| --- | --- |
| [CountDownLatch](../java/util/concurrent/CountDownLatch.md) | A synchronization aid that allows one or more threads to wait until a set of operations being performed in other threads completes. |
| [CountedCompleter](../java/util/concurrent/CountedCompleter.md) | A [ForkJoinTask](../java/util/concurrent/ForkJoinTask.md) with a completion action performed when triggered and there are no remaining pending actions. |
| [CyclicBarrier](../java/util/concurrent/CyclicBarrier.md) | A synchronization aid that allows a set of threads to all wait for each other to reach a common barrier point. |
| --- | --- |
| [DelayQueue](../java/util/concurrent/DelayQueue.md) | An unbounded [blocking queue](../java/util/concurrent/BlockingQueue.md) of [Delayed](../java/util/concurrent/Delayed.md) elements, in which an element generally becomes eligible for removal when its delay has expired. |
| [Exchanger](../java/util/concurrent/Exchanger.md) | A synchronization point at which threads can pair and swap elements within pairs. |
| [ExecutorCompletionService](../java/util/concurrent/ExecutorCompletionService.md) | A [CompletionService](../java/util/concurrent/CompletionService.md) that uses a supplied [Executor](../java/util/concurrent/Executor.md) to execute tasks. |
| --- | --- |
| [Executors](../java/util/concurrent/Executors.md) | Factory and utility methods for [Executor](../java/util/concurrent/Executor.md), [ExecutorService](../java/util/concurrent/ExecutorService.md), [ScheduledExecutorService](../java/util/concurrent/ScheduledExecutorService.md), [ThreadFactory](../java/util/concurrent/ThreadFactory.md), and [Callable](../java/util/concurrent/Callable.md) classes defined in this package. |
| [Flow](../java/util/concurrent/Flow.md) | Interrelated interfaces and static methods for establishing flow-controlled components in which [Publishers](../java/util/concurrent/Flow.Publisher.md) produce items consumed by one or more [Subscribers](../java/util/concurrent/Flow.Subscriber.md), each managed by a [Subscription](../java/util/concurrent/Flow.Subscription.md). |
| [ForkJoinPool](../java/util/concurrent/ForkJoinPool.md) | An [ExecutorService](../java/util/concurrent/ExecutorService.md) for running [ForkJoinTask](../java/util/concurrent/ForkJoinTask.md) s. |
| --- | --- |
| [ForkJoinTask](../java/util/concurrent/ForkJoinTask.md) | Abstract base class for tasks that run within a [ForkJoinPool](../java/util/concurrent/ForkJoinPool.md). |
| [ForkJoinWorkerThread](../java/util/concurrent/ForkJoinWorkerThread.md) | A thread managed by a [ForkJoinPool](../java/util/concurrent/ForkJoinPool.md), which executes [ForkJoinTask](../java/util/concurrent/ForkJoinTask.md) s. |
| [FutureTask](../java/util/concurrent/FutureTask.md) | A cancellable asynchronous computation. |
| --- | --- |
| [LinkedBlockingDeque](../java/util/concurrent/LinkedBlockingDeque.md) | An optionally-bounded [blocking deque](../java/util/concurrent/BlockingDeque.md) based on linked nodes. |
| [LinkedBlockingQueue](../java/util/concurrent/LinkedBlockingQueue.md) | An optionally-bounded [blocking queue](../java/util/concurrent/BlockingQueue.md) based on linked nodes. |
| [LinkedTransferQueue](../java/util/concurrent/LinkedTransferQueue.md) | An unbounded [TransferQueue](../java/util/concurrent/TransferQueue.md) based on linked nodes. |
| --- | --- |
| [Phaser](../java/util/concurrent/Phaser.md) | A reusable synchronization barrier, similar in functionality to [CyclicBarrier](../java/util/concurrent/CyclicBarrier.md) and [CountDownLatch](../java/util/concurrent/CountDownLatch.md) but supporting more flexible usage. |
| [PriorityBlockingQueue](../java/util/concurrent/PriorityBlockingQueue.md) | An unbounded [blocking queue](../java/util/concurrent/BlockingQueue.md) that uses the same ordering rules as class [PriorityQueue](../java/util/PriorityQueue.md) and supplies blocking retrieval operations. |
| [RecursiveAction](../java/util/concurrent/RecursiveAction.md) | A recursive resultless [ForkJoinTask](../java/util/concurrent/ForkJoinTask.md). |
| --- | --- |
| [RecursiveTask](../java/util/concurrent/RecursiveTask.md) | A recursive result-bearing [ForkJoinTask](../java/util/concurrent/ForkJoinTask.md). |
| [ScheduledThreadPoolExecutor](../java/util/concurrent/ScheduledThreadPoolExecutor.md) | A [ThreadPoolExecutor](../java/util/concurrent/ThreadPoolExecutor.md) that can additionally schedule commands to run after a given delay, or to execute periodically. |
| [Semaphore](../java/util/concurrent/Semaphore.md) | A counting semaphore. |
| --- | --- |
| [SubmissionPublisher](../java/util/concurrent/SubmissionPublisher.md) | A [Flow.Publisher](../java/util/concurrent/Flow.Publisher.md) that asynchronously issues submitted (non-null) items to current subscribers until it is closed. |
| [SynchronousQueue](../java/util/concurrent/SynchronousQueue.md) | A [blocking queue](../java/util/concurrent/BlockingQueue.md) in which each insert operation must wait for a corresponding remove operation by another thread, and vice versa. |
| [ThreadLocalRandom](../java/util/concurrent/ThreadLocalRandom.md) | A random number generator (with period 264) isolated to the current thread. |
| --- | --- |
| [ThreadPoolExecutor](../java/util/concurrent/ThreadPoolExecutor.md) | An [ExecutorService](../java/util/concurrent/ExecutorService.md) that executes each submitted task using one of possibly several pooled threads, normally configured using [Executors](../java/util/concurrent/Executors.md) factory methods. |

## Exceptions

| [BrokenBarrierException](../java/util/concurrent/BrokenBarrierException.md) | Exception thrown when a thread tries to wait upon a barrier that is in a broken state, or which enters the broken state while the thread is waiting. |
| --- | --- |
| [CancellationException](../java/util/concurrent/CancellationException.md) | Exception indicating that the result of a value-producing task, such as a [FutureTask](../java/util/concurrent/FutureTask.md), cannot be retrieved because the task was cancelled. |
| [CompletionException](../java/util/concurrent/CompletionException.md) | Exception thrown when an error or other exception is encountered in the course of completing a result or task. |
| [ExecutionException](../java/util/concurrent/ExecutionException.md) | Exception thrown when attempting to retrieve the result of a task that aborted by throwing an exception. |
| --- | --- |
| [RejectedExecutionException](../java/util/concurrent/RejectedExecutionException.md) | Exception thrown by an [Executor](../java/util/concurrent/Executor.md) when a task cannot be accepted for execution. |
| [TimeoutException](../java/util/concurrent/TimeoutException.md) | Exception thrown when a blocking operation times out. |

## Enums

| [TimeUnit](../java/util/concurrent/TimeUnit.md) | A represents time durations at a given unit of granularity and provides utility methods to convert across units, and to perform timing and delay operations in these units. |
| --- | --- |
