# java.util.concurrent

# java.util.concurrent

## Interfaces

| [BlockingDeque](BlockingDeque.md) | A [Deque](../java.util/Deque.md) that additionally supports blocking operations that wait for the deque to become non-empty when retrieving an element, and wait for space to become available in the deque when storing an element. |
| --- | --- |
| [BlockingQueue](BlockingQueue.md) | A [Queue](../java.util/Queue.md) that additionally supports operations that wait for the queue to become non-empty when retrieving an element, and wait for space to become available in the queue when storing an element. |
| [Callable](Callable.md) | A task that returns a result and may throw an exception. |
| [AsynchronousCompletionTask](../java/util/concurrent/CompletableFuture.AsynchronousCompletionTask.md) | A marker interface identifying asynchronous tasks produced by`async`methods. |
| --- | --- |
| [CompletionService](CompletionService.md) | A service that decouples the production of new asynchronous tasks from the consumption of the results of completed tasks. |
| [CompletionStage](CompletionStage.md) | A stage of a possibly asynchronous computation, that performs an action or computes a value when another CompletionStage completes. |
| [ConcurrentMap](ConcurrentMap.md) | A [Map](../java.util/Map.md) providing thread safety and atomicity guarantees. |
| --- | --- |
| [ConcurrentNavigableMap](ConcurrentNavigableMap.md) | A [ConcurrentMap](ConcurrentMap.md) supporting [NavigableMap](../java.util/NavigableMap.md) operations, and recursively so for its navigable sub-maps. |
| [Delayed](Delayed.md) | A mix-in style interface for marking objects that should be acted upon after a given delay. |
| [Executor](Executor.md) | An object that executes submitted [Runnable](../java.lang/Runnable.md) tasks. |
| --- | --- |
| [ExecutorService](ExecutorService.md) | An [Executor](Executor.md) that provides methods to manage termination and methods that can produce a [Future](Future.md) for tracking progress of one or more asynchronous tasks. |
| [Processor](../java/util/concurrent/Flow.Processor.md) | A component that acts as both a Subscriber and Publisher. |
| [Publisher](../java/util/concurrent/Flow.Publisher.md) | A producer of items (and related control messages) received by Subscribers. |
| --- | --- |
| [Subscriber](../java/util/concurrent/Flow.Subscriber.md) | A receiver of messages. |
| [Subscription](../java/util/concurrent/Flow.Subscription.md) | Message control linking a [Publisher](../java/util/concurrent/Flow.Publisher.md) and [Subscriber](../java/util/concurrent/Flow.Subscriber.md). |
| [ForkJoinWorkerThreadFactory](../java/util/concurrent/ForkJoinPool.ForkJoinWorkerThreadFactory.md) | Factory for creating new [ForkJoinWorkerThread](ForkJoinWorkerThread.md) s. |
| --- | --- |
| [ManagedBlocker](../java/util/concurrent/ForkJoinPool.ManagedBlocker.md) | Interface for extending managed parallelism for tasks running in [ForkJoinPool](ForkJoinPool.md) s. |
| [Future](Future.md) | A represents the result of an asynchronous computation. |
| [RejectedExecutionHandler](RejectedExecutionHandler.md) | A handler for tasks that cannot be executed by a [ThreadPoolExecutor](ThreadPoolExecutor.md). |
| --- | --- |
| [RunnableFuture](RunnableFuture.md) | A [Future](Future.md) that is [Runnable](../java.lang/Runnable.md). |
| [RunnableScheduledFuture](RunnableScheduledFuture.md) | A [ScheduledFuture](ScheduledFuture.md) that is [Runnable](../java.lang/Runnable.md). |
| [ScheduledExecutorService](ScheduledExecutorService.md) | An [ExecutorService](ExecutorService.md) that can schedule commands to run after a given delay, or to execute periodically. |
| --- | --- |
| [ScheduledFuture](ScheduledFuture.md) | A delayed result-bearing action that can be cancelled. |
| [ThreadFactory](ThreadFactory.md) | An object that creates new threads on demand. |
| [TransferQueue](TransferQueue.md) | A [BlockingQueue](BlockingQueue.md) in which producers may wait for consumers to receive elements. |
| --- | --- |

## Classes

| [AbstractExecutorService](AbstractExecutorService.md) | Provides default implementations of [ExecutorService](ExecutorService.md) execution methods. |
| --- | --- |
| [ArrayBlockingQueue](ArrayBlockingQueue.md) | A bounded [blocking queue](BlockingQueue.md) backed by an array. |
| [CompletableFuture](CompletableFuture.md) | A [Future](Future.md) that may be explicitly completed (setting its value and status), and may be used as a [CompletionStage](CompletionStage.md), supporting dependent functions and actions that trigger upon its completion. |
| [ConcurrentHashMap](ConcurrentHashMap.md) | A hash table supporting full concurrency of retrievals and high expected concurrency for updates. |
| --- | --- |
| [ConcurrentLinkedDeque](ConcurrentLinkedDeque.md) | An unbounded concurrent [deque](../java.util/Deque.md) based on linked nodes. |
| [ConcurrentLinkedQueue](ConcurrentLinkedQueue.md) | An unbounded thread-safe [queue](../java.util/Queue.md) based on linked nodes. |
| [ConcurrentSkipListMap](ConcurrentSkipListMap.md) | A scalable concurrent [ConcurrentNavigableMap](ConcurrentNavigableMap.md) implementation. |
| --- | --- |
| [ConcurrentSkipListSet](ConcurrentSkipListSet.md) | A scalable concurrent [NavigableSet](../java.util/NavigableSet.md) implementation based on a [ConcurrentSkipListMap](ConcurrentSkipListMap.md). |
| [CopyOnWriteArrayList](CopyOnWriteArrayList.md) | A thread-safe variant of [java.util.ArrayList](../java.util/ArrayList.md) in which all mutative operations (`add`,`set`, and so on) are implemented by making a fresh copy of the underlying array. |
| [CopyOnWriteArraySet](CopyOnWriteArraySet.md) | A [Set](../java.util/Set.md) that uses an internal [CopyOnWriteArrayList](CopyOnWriteArrayList.md) for all of its operations. |
| --- | --- |
| [CountDownLatch](CountDownLatch.md) | A synchronization aid that allows one or more threads to wait until a set of operations being performed in other threads completes. |
| [CountedCompleter](CountedCompleter.md) | A [ForkJoinTask](ForkJoinTask.md) with a completion action performed when triggered and there are no remaining pending actions. |
| [CyclicBarrier](CyclicBarrier.md) | A synchronization aid that allows a set of threads to all wait for each other to reach a common barrier point. |
| --- | --- |
| [DelayQueue](DelayQueue.md) | An unbounded [blocking queue](BlockingQueue.md) of [Delayed](Delayed.md) elements, in which an element generally becomes eligible for removal when its delay has expired. |
| [Exchanger](Exchanger.md) | A synchronization point at which threads can pair and swap elements within pairs. |
| [ExecutorCompletionService](ExecutorCompletionService.md) | A [CompletionService](CompletionService.md) that uses a supplied [Executor](Executor.md) to execute tasks. |
| --- | --- |
| [Executors](Executors.md) | Factory and utility methods for [Executor](Executor.md), [ExecutorService](ExecutorService.md), [ScheduledExecutorService](ScheduledExecutorService.md), [ThreadFactory](ThreadFactory.md), and [Callable](Callable.md) classes defined in this package. |
| [Flow](Flow.md) | Interrelated interfaces and static methods for establishing flow-controlled components in which [Publishers](../java/util/concurrent/Flow.Publisher.md) produce items consumed by one or more [Subscribers](../java/util/concurrent/Flow.Subscriber.md), each managed by a [Subscription](../java/util/concurrent/Flow.Subscription.md). |
| [ForkJoinPool](ForkJoinPool.md) | An [ExecutorService](ExecutorService.md) for running [ForkJoinTask](ForkJoinTask.md) s. |
| --- | --- |
| [ForkJoinTask](ForkJoinTask.md) | Abstract base class for tasks that run within a [ForkJoinPool](ForkJoinPool.md). |
| [ForkJoinWorkerThread](ForkJoinWorkerThread.md) | A thread managed by a [ForkJoinPool](ForkJoinPool.md), which executes [ForkJoinTask](ForkJoinTask.md) s. |
| [FutureTask](FutureTask.md) | A cancellable asynchronous computation. |
| --- | --- |
| [LinkedBlockingDeque](LinkedBlockingDeque.md) | An optionally-bounded [blocking deque](BlockingDeque.md) based on linked nodes. |
| [LinkedBlockingQueue](LinkedBlockingQueue.md) | An optionally-bounded [blocking queue](BlockingQueue.md) based on linked nodes. |
| [LinkedTransferQueue](LinkedTransferQueue.md) | An unbounded [TransferQueue](TransferQueue.md) based on linked nodes. |
| --- | --- |
| [Phaser](Phaser.md) | A reusable synchronization barrier, similar in functionality to [CyclicBarrier](CyclicBarrier.md) and [CountDownLatch](CountDownLatch.md) but supporting more flexible usage. |
| [PriorityBlockingQueue](PriorityBlockingQueue.md) | An unbounded [blocking queue](BlockingQueue.md) that uses the same ordering rules as class [PriorityQueue](../java.util/PriorityQueue.md) and supplies blocking retrieval operations. |
| [RecursiveAction](RecursiveAction.md) | A recursive resultless [ForkJoinTask](ForkJoinTask.md). |
| --- | --- |
| [RecursiveTask](RecursiveTask.md) | A recursive result-bearing [ForkJoinTask](ForkJoinTask.md). |
| [ScheduledThreadPoolExecutor](ScheduledThreadPoolExecutor.md) | A [ThreadPoolExecutor](ThreadPoolExecutor.md) that can additionally schedule commands to run after a given delay, or to execute periodically. |
| [Semaphore](Semaphore.md) | A counting semaphore. |
| --- | --- |
| [SubmissionPublisher](SubmissionPublisher.md) | A [Flow.Publisher](../java/util/concurrent/Flow.Publisher.md) that asynchronously issues submitted (non-null) items to current subscribers until it is closed. |
| [SynchronousQueue](SynchronousQueue.md) | A [blocking queue](BlockingQueue.md) in which each insert operation must wait for a corresponding remove operation by another thread, and vice versa. |
| [ThreadLocalRandom](ThreadLocalRandom.md) | A random number generator (with period 264) isolated to the current thread. |
| --- | --- |
| [ThreadPoolExecutor](ThreadPoolExecutor.md) | An [ExecutorService](ExecutorService.md) that executes each submitted task using one of possibly several pooled threads, normally configured using [Executors](Executors.md) factory methods. |

## Exceptions

| [BrokenBarrierException](BrokenBarrierException.md) | Exception thrown when a thread tries to wait upon a barrier that is in a broken state, or which enters the broken state while the thread is waiting. |
| --- | --- |
| [CancellationException](CancellationException.md) | Exception indicating that the result of a value-producing task, such as a [FutureTask](FutureTask.md), cannot be retrieved because the task was cancelled. |
| [CompletionException](CompletionException.md) | Exception thrown when an error or other exception is encountered in the course of completing a result or task. |
| [ExecutionException](ExecutionException.md) | Exception thrown when attempting to retrieve the result of a task that aborted by throwing an exception. |
| --- | --- |
| [RejectedExecutionException](RejectedExecutionException.md) | Exception thrown by an [Executor](Executor.md) when a task cannot be accepted for execution. |
| [TimeoutException](TimeoutException.md) | Exception thrown when a blocking operation times out. |

## Enums

| [TimeUnit](TimeUnit.md) | A represents time durations at a given unit of granularity and provides utility methods to convert across units, and to perform timing and delay operations in these units. |
| --- | --- |
