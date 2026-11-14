Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CompletableFuture

```
open class CompletableFuture<T : Any!> : CompletionStage<T>, Future<T>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.concurrent.CompletableFuture](CompletableFuture.md) |

A Future that may be explicitly completed (setting its value and status), and may be used as a CompletionStage, supporting dependent functions and actions that trigger upon its completion.

When two or more threads attempt to complete, completeExceptionally, or cancel a CompletableFuture, only one of them succeeds.

In addition to these and related methods for directly manipulating status and results, CompletableFuture implements interface CompletionStage with the following policies:

- Actions supplied for dependent completions of *non-async* methods may be performed by the thread that completes the current CompletableFuture, or by any other caller of a completion method.
- All *async* methods without an explicit Executor argument are performed using the commonPool (unless it does not support a parallelism level of at least two, in which case, a new Thread is created to run each task). To simplify monitoring, debugging, and tracking, all generated asynchronous tasks are instances of the marker interface `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture.AsynchronousCompletionTask`. Operations with time-delays can use adapter methods defined in this class, for example: `supplyAsync(supplier, delayedExecutor(timeout, timeUnit))`. To support methods with delays and timeouts, this class maintains at most one daemon thread for triggering and cancelling actions, not for running them.
- All CompletionStage methods are implemented independently of other public methods, so the behavior of one method is not impacted by overrides of others in subclasses.

CompletableFuture also implements Future with the following policies:

- Since (unlike FutureTask) this class has no direct control over the computation that causes it to be completed, cancellation is treated as just another form of exceptional completion. Method cancel has the same effect as `completeExceptionally(new CancellationException())`. Method isCompletedExceptionally can be used to determine if a CompletableFuture completed in any exceptional fashion.
- In case of exceptional completion with a CompletionException, methods get and get throw an ExecutionException with the same cause as held in the corresponding CompletionException. To simplify usage in most contexts, this class also defines methods join and getNow that instead throw the CompletionException directly in these cases.

Arguments used to pass a completion result (that is, for parameters of type `T`) for methods accepting them may be null, but passing a null value for any other parameter will result in a `https://developer.android.com/reference/kotlin/java/lang/NullPointerException.html#` being thrown.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture.AsynchronousCompletionTask` A marker interface identifying asynchronous tasks produced by `async` methods. |

| Public constructors ||
|---|---|
| CompletableFuture Creates a new incomplete CompletableFuture. |

| Public methods ||
|---|---|
| open [CompletableFuture](CompletableFuture.md)\< [Void](../java.lang/Void.md)!\>! | acceptEither Returns a new CompletionStage that, when either this or the other given stage complete normally, is executed with the corresponding result as argument to the supplied action. |
| open [CompletableFuture](CompletableFuture.md)\< [Void](../java.lang/Void.md)!\>! | acceptEitherAsync Returns a new CompletionStage that, when either this or the other given stage complete normally, is executed using this stage's default asynchronous execution facility, with the corresponding result as argument to the supplied action. |
| open [CompletableFuture](CompletableFuture.md)\< [Void](../java.lang/Void.md)!\>! | acceptEitherAsync Returns a new CompletionStage that, when either this or the other given stage complete normally, is executed using the supplied executor, with the corresponding result as argument to the supplied action. |
| --- | --- |
| open static [CompletableFuture](CompletableFuture.md)\< [Void](../java.lang/Void.md)!\>! | allOf Returns a new CompletableFuture that is completed when all of the given CompletableFutures complete. |
| open static [CompletableFuture](CompletableFuture.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | anyOf Returns a new CompletableFuture that is completed when any of the given CompletableFutures complete, with the same result. |
| open [CompletableFuture](CompletableFuture.md)\<U\>! | applyToEither Returns a new CompletionStage that, when either this or the other given stage complete normally, is executed with the corresponding result as argument to the supplied function. |
| --- | --- |
| open [CompletableFuture](CompletableFuture.md)\<U\>! | applyToEitherAsync Returns a new CompletionStage that, when either this or the other given stage complete normally, is executed using this stage's default asynchronous execution facility, with the corresponding result as argument to the supplied function. |
| open [CompletableFuture](CompletableFuture.md)\<U\>! | applyToEitherAsync Returns a new CompletionStage that, when either this or the other given stage complete normally, is executed using the supplied executor, with the corresponding result as argument to the supplied function. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | cancel If not already completed, completes this CompletableFuture with a CancellationException. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | complete If not already completed, sets the value returned by get and related methods to the given value. |
| open [CompletableFuture](CompletableFuture.md)\<T\>! | completeAsync Completes this CompletableFuture with the result of the given Supplier function invoked from an asynchronous task using the default executor. |
| open [CompletableFuture](CompletableFuture.md)\<T\>! | completeAsync Completes this CompletableFuture with the result of the given Supplier function invoked from an asynchronous task using the given executor. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | completeExceptionally If not already completed, causes invocations of get and related methods to throw the given exception. |
| open [CompletableFuture](CompletableFuture.md)\<T\>! | completeOnTimeout Completes this CompletableFuture with the given value if not otherwise completed before the given timeout. |
| open static [CompletableFuture](CompletableFuture.md)\<U\>! | completedFuture Returns a new CompletableFuture that is already completed with the given value. |
| --- | --- |
| open static [CompletionStage](CompletionStage.md)\<U\>! | completedStage Returns a new CompletionStage that is already completed with the given value and supports only those methods in interface CompletionStage. |
| open [CompletableFuture](CompletableFuture.md)\<T\>! | copy Returns a new CompletableFuture that is completed normally with the same value as this CompletableFuture when it completes normally. |
| open [Executor](Executor.md)! | defaultExecutor Returns the default Executor used for async methods that do not specify an Executor. |
| --- | --- |
| open static [Executor](Executor.md)! | delayedExecutor Returns a new Executor that submits a task to the default executor after the given delay (or no delay if non-positive). |
| open static [Executor](Executor.md)! | delayedExecutor Returns a new Executor that submits a task to the given base executor after the given delay (or no delay if non-positive). |
| open [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)! | exceptionNow Returns the exception thrown by the task, without waiting. |
| --- | --- |
| open [CompletableFuture](CompletableFuture.md)\<T\>! | exceptionally Returns a new CompletionStage that, when this stage completes exceptionally, is executed with this stage's exception as the argument to the supplied function. |
| open [CompletableFuture](CompletableFuture.md)\<T\>! | exceptionallyAsync Returns a new CompletionStage that, when this stage completes exceptionally, is executed with this stage's exception as the argument to the supplied function, using this stage's default asynchronous execution facility. |
| open [CompletableFuture](CompletableFuture.md)\<T\>! | exceptionallyAsync Returns a new CompletionStage that, when this stage completes exceptionally, is executed with this stage's exception as the argument to the supplied function, using the supplied Executor. |
| --- | --- |
| open [CompletableFuture](CompletableFuture.md)\<T\>! | exceptionallyCompose Returns a new CompletionStage that, when this stage completes exceptionally, is composed using the results of the supplied function applied to this stage's exception. |
| open [CompletableFuture](CompletableFuture.md)\<T\>! | exceptionallyComposeAsync Returns a new CompletionStage that, when this stage completes exceptionally, is composed using the results of the supplied function applied to this stage's exception, using this stage's default asynchronous execution facility. |
| open [CompletableFuture](CompletableFuture.md)\<T\>! | exceptionallyComposeAsync Returns a new CompletionStage that, when this stage completes exceptionally, is composed using the results of the supplied function applied to this stage's exception, using the supplied Executor. |
| --- | --- |
| open static [CompletableFuture](CompletableFuture.md)\<U\>! | failedFuture Returns a new CompletableFuture that is already completed exceptionally with the given exception. |
| open static [CompletionStage](CompletionStage.md)\<U\>! | failedStage Returns a new CompletionStage that is already completed exceptionally with the given exception and supports only those methods in interface CompletionStage. |
| open T | get Waits if necessary for this future to complete, and then returns its result. |
| --- | --- |
| open T | get Waits if necessary for at most the given time for this future to complete, and then returns its result, if available. |
| open T | getNow Returns the result value (or throws any encountered exception) if completed, else returns the given valueIfAbsent. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getNumberOfDependents Returns the estimated number of CompletableFutures whose completions are awaiting completion of this CompletableFuture. |
| --- | --- |
| open [CompletableFuture](CompletableFuture.md)\<U\>! | handle Returns a new CompletionStage that, when this stage completes either normally or exceptionally, is executed with this stage's result and exception as arguments to the supplied function. |
| open [CompletableFuture](CompletableFuture.md)\<U\>! | handleAsync Returns a new CompletionStage that, when this stage completes either normally or exceptionally, is executed using this stage's default asynchronous execution facility, with this stage's result and exception as arguments to the supplied function. |
| open [CompletableFuture](CompletableFuture.md)\<U\>! | handleAsync Returns a new CompletionStage that, when this stage completes either normally or exceptionally, is executed using the supplied executor, with this stage's result and exception as arguments to the supplied function. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isCancelled Returns `true` if this CompletableFuture was cancelled before it completed normally. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isCompletedExceptionally Returns `true` if this CompletableFuture completed exceptionally, in any way. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isDone Returns `true` if completed in any fashion: normally, exceptionally, or via cancellation. |
| --- | --- |
| open T | join Returns the result value when complete, or throws an (unchecked) exception if completed exceptionally. |
| open [CompletionStage](CompletionStage.md)\<T\>! | minimalCompletionStage Returns a new CompletionStage that is completed normally with the same value as this CompletableFuture when it completes normally, and cannot be independently completed or otherwise used in ways not defined by the methods of interface CompletionStage. |
| open [CompletableFuture](CompletableFuture.md)\<U\>! | newIncompleteFuture Returns a new incomplete CompletableFuture of the type to be returned by a CompletionStage method. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | obtrudeException Forcibly causes subsequent invocations of method get and related methods to throw the given exception, whether or not already completed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | obtrudeValue Forcibly sets or resets the value subsequently returned by method get and related methods, whether or not already completed. |
| open [CompletableFuture](CompletableFuture.md)\<T\>! | orTimeout Exceptionally completes this CompletableFuture with a TimeoutException if not otherwise completed before the given timeout. |
| --- | --- |
| open T | resultNow Returns the computed result, without waiting. |
| open [CompletableFuture](CompletableFuture.md)\< [Void](../java.lang/Void.md)!\>! | runAfterBoth Returns a new CompletionStage that, when this and the other given stage both complete normally, executes the given action. |
| open [CompletableFuture](CompletableFuture.md)\< [Void](../java.lang/Void.md)!\>! | runAfterBothAsync Returns a new CompletionStage that, when this and the other given stage both complete normally, executes the given action using this stage's default asynchronous execution facility. |
| --- | --- |
| open [CompletableFuture](CompletableFuture.md)\< [Void](../java.lang/Void.md)!\>! | runAfterBothAsync Returns a new CompletionStage that, when this and the other given stage both complete normally, executes the given action using the supplied executor. |
| open [CompletableFuture](CompletableFuture.md)\< [Void](../java.lang/Void.md)!\>! | runAfterEither Returns a new CompletionStage that, when either this or the other given stage complete normally, executes the given action. |
| open [CompletableFuture](CompletableFuture.md)\< [Void](../java.lang/Void.md)!\>! | runAfterEitherAsync Returns a new CompletionStage that, when either this or the other given stage complete normally, executes the given action using this stage's default asynchronous execution facility. |
| --- | --- |
| open [CompletableFuture](CompletableFuture.md)\< [Void](../java.lang/Void.md)!\>! | runAfterEitherAsync Returns a new CompletionStage that, when either this or the other given stage complete normally, executes the given action using the supplied executor. |
| open static [CompletableFuture](CompletableFuture.md)\< [Void](../java.lang/Void.md)!\>! | runAsync Returns a new CompletableFuture that is asynchronously completed by a task running in the commonPool after it runs the given action. |
| open static [CompletableFuture](CompletableFuture.md)\< [Void](../java.lang/Void.md)!\>! | runAsync Returns a new CompletableFuture that is asynchronously completed by a task running in the given executor after it runs the given action. |
| --- | --- |
| open [Future.State](../java/util/concurrent/Future.State.md)! | state {@return the computation state} |
| open static [CompletableFuture](CompletableFuture.md)\<U\>! | supplyAsync Returns a new CompletableFuture that is asynchronously completed by a task running in the commonPool with the value obtained by calling the given Supplier. |
| open static [CompletableFuture](CompletableFuture.md)\<U\>! | supplyAsync Returns a new CompletableFuture that is asynchronously completed by a task running in the given executor with the value obtained by calling the given Supplier. |
| --- | --- |
| open [CompletableFuture](CompletableFuture.md)\< [Void](../java.lang/Void.md)!\>! | thenAccept Returns a new CompletionStage that, when this stage completes normally, is executed with this stage's result as the argument to the supplied action. |
| open [CompletableFuture](CompletableFuture.md)\< [Void](../java.lang/Void.md)!\>! | thenAcceptAsync Returns a new CompletionStage that, when this stage completes normally, is executed using this stage's default asynchronous execution facility, with this stage's result as the argument to the supplied action. |
| open [CompletableFuture](CompletableFuture.md)\< [Void](../java.lang/Void.md)!\>! | thenAcceptAsync Returns a new CompletionStage that, when this stage completes normally, is executed using the supplied Executor, with this stage's result as the argument to the supplied action. |
| --- | --- |
| open [CompletableFuture](CompletableFuture.md)\< [Void](../java.lang/Void.md)!\>! | thenAcceptBoth Returns a new CompletionStage that, when this and the other given stage both complete normally, is executed with the two results as arguments to the supplied action. |
| open [CompletableFuture](CompletableFuture.md)\< [Void](../java.lang/Void.md)!\>! | thenAcceptBothAsync Returns a new CompletionStage that, when this and the other given stage both complete normally, is executed using this stage's default asynchronous execution facility, with the two results as arguments to the supplied action. |
| open [CompletableFuture](CompletableFuture.md)\< [Void](../java.lang/Void.md)!\>! | thenAcceptBothAsync Returns a new CompletionStage that, when this and the other given stage both complete normally, is executed using the supplied executor, with the two results as arguments to the supplied action. |
| --- | --- |
| open [CompletableFuture](CompletableFuture.md)\<U\>! | thenApply Returns a new CompletionStage that, when this stage completes normally, is executed with this stage's result as the argument to the supplied function. |
| open [CompletableFuture](CompletableFuture.md)\<U\>! | thenApplyAsync Returns a new CompletionStage that, when this stage completes normally, is executed using this stage's default asynchronous execution facility, with this stage's result as the argument to the supplied function. |
| open [CompletableFuture](CompletableFuture.md)\<U\>! | thenApplyAsync Returns a new CompletionStage that, when this stage completes normally, is executed using the supplied Executor, with this stage's result as the argument to the supplied function. |
| --- | --- |
| open [CompletableFuture](CompletableFuture.md)\<V\>! | thenCombine Returns a new CompletionStage that, when this and the other given stage both complete normally, is executed with the two results as arguments to the supplied function. |
| open [CompletableFuture](CompletableFuture.md)\<V\>! | thenCombineAsync Returns a new CompletionStage that, when this and the other given stage both complete normally, is executed using this stage's default asynchronous execution facility, with the two results as arguments to the supplied function. |
| open [CompletableFuture](CompletableFuture.md)\<V\>! | thenCombineAsync Returns a new CompletionStage that, when this and the other given stage both complete normally, is executed using the supplied executor, with the two results as arguments to the supplied function. |
| --- | --- |
| open [CompletableFuture](CompletableFuture.md)\<U\>! | thenCompose Returns a new CompletionStage that is completed with the same value as the CompletionStage returned by the given function. |
| open [CompletableFuture](CompletableFuture.md)\<U\>! | thenComposeAsync Returns a new CompletionStage that is completed with the same value as the CompletionStage returned by the given function, executed using this stage's default asynchronous execution facility. |
| open [CompletableFuture](CompletableFuture.md)\<U\>! | thenComposeAsync Returns a new CompletionStage that is completed with the same value as the CompletionStage returned by the given function, executed using the supplied Executor. |
| --- | --- |
| open [CompletableFuture](CompletableFuture.md)\< [Void](../java.lang/Void.md)!\>! | thenRun Returns a new CompletionStage that, when this stage completes normally, executes the given action. |
| open [CompletableFuture](CompletableFuture.md)\< [Void](../java.lang/Void.md)!\>! | thenRunAsync Returns a new CompletionStage that, when this stage completes normally, executes the given action using this stage's default asynchronous execution facility. |
| open [CompletableFuture](CompletableFuture.md)\< [Void](../java.lang/Void.md)!\>! | thenRunAsync Returns a new CompletionStage that, when this stage completes normally, executes the given action using the supplied Executor. |
| --- | --- |
| open [CompletableFuture](CompletableFuture.md)\<T\>! | toCompletableFuture Returns this CompletableFuture. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string identifying this CompletableFuture, as well as its completion state. |
| open [CompletableFuture](CompletableFuture.md)\<T\>! | whenComplete Returns a new CompletionStage with the same result or exception as this stage, that executes the given action when this stage completes. |
| --- | --- |
| open [CompletableFuture](CompletableFuture.md)\<T\>! | whenCompleteAsync Returns a new CompletionStage with the same result or exception as this stage, that executes the given action using this stage's default asynchronous execution facility when this stage completes. |
| open [CompletableFuture](CompletableFuture.md)\<T\>! | whenCompleteAsync Returns a new CompletionStage with the same result or exception as this stage, that executes the given action using the supplied Executor when this stage completes. |

## Public constructors

### CompletableFuture

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
CompletableFuture()
```

Creates a new incomplete CompletableFuture.

## Public methods

### acceptEither

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun acceptEither(
    other: CompletionStage<out T>!, 
    action: Consumer<in T>!
): CompletableFuture<Void!>!
```

Returns a new CompletionStage that, when either this or the other given stage complete normally, is executed with the corresponding result as argument to the supplied action. See the CompletionStage documentation for rules covering exceptional completion.

| Parameters ||
|---|---|
| `other` | [CompletionStage](CompletionStage.md)\<out T\>!: the other CompletionStage |
| `action` | [Consumer](../java.util.function/Consumer.md)\<in T\>!: the action to perform before completing the returned CompletionStage |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<https://developer.android.com/reference/kotlin/java/lang/Void.html#!>!` | the new CompletionStage |

### acceptEitherAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun acceptEitherAsync(
    other: CompletionStage<out T>!, 
    action: Consumer<in T>!
): CompletableFuture<Void!>!
```

Returns a new CompletionStage that, when either this or the other given stage complete normally, is executed using this stage's default asynchronous execution facility, with the corresponding result as argument to the supplied action. See the CompletionStage documentation for rules covering exceptional completion.

| Parameters ||
|---|---|
| `other` | [CompletionStage](CompletionStage.md)\<out T\>!: the other CompletionStage |
| `action` | [Consumer](../java.util.function/Consumer.md)\<in T\>!: the action to perform before completing the returned CompletionStage |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<https://developer.android.com/reference/kotlin/java/lang/Void.html#!>!` | the new CompletionStage |

### acceptEitherAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun acceptEitherAsync(
    other: CompletionStage<out T>!, 
    action: Consumer<in T>!, 
    executor: Executor!
): CompletableFuture<Void!>!
```

Returns a new CompletionStage that, when either this or the other given stage complete normally, is executed using the supplied executor, with the corresponding result as argument to the supplied action. See the CompletionStage documentation for rules covering exceptional completion.

| Parameters ||
|---|---|
| `other` | [CompletionStage](CompletionStage.md)\<out T\>!: the other CompletionStage |
| `action` | [Consumer](../java.util.function/Consumer.md)\<in T\>!: the action to perform before completing the returned CompletionStage |
| `executor` | [Executor](Executor.md)!: the executor to use for asynchronous execution |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<https://developer.android.com/reference/kotlin/java/lang/Void.html#!>!` | the new CompletionStage |

### allOf

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun allOf(vararg cfs: CompletableFuture<*>!): CompletableFuture<Void!>!
```

Returns a new CompletableFuture that is completed when all of the given CompletableFutures complete. If any of the given CompletableFutures complete exceptionally, then the returned CompletableFuture also does so, with a CompletionException holding this exception as its cause. Otherwise, the results, if any, of the given CompletableFutures are not reflected in the returned CompletableFuture, but may be obtained by inspecting them individually. If no CompletableFutures are provided, returns a CompletableFuture completed with the value `null`.

Among the applications of this method is to await completion of a set of independent CompletableFutures before continuing a program, as in: `CompletableFuture.allOf(c1, c2, c3).join();`.

| Parameters ||
|---|---|
| `cfs` | [CompletableFuture](CompletableFuture.md)\<\*\>!: the CompletableFutures |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<https://developer.android.com/reference/kotlin/java/lang/Void.html#!>!` | a new CompletableFuture that is completed when all of the given CompletableFutures complete |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the array or any of its elements are `null` |

### anyOf

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun anyOf(vararg cfs: CompletableFuture<*>!): CompletableFuture<Any!>!
```

Returns a new CompletableFuture that is completed when any of the given CompletableFutures complete, with the same result. Otherwise, if it completed exceptionally, the returned CompletableFuture also does so, with a CompletionException holding this exception as its cause. If no CompletableFutures are provided, returns an incomplete CompletableFuture.

| Parameters ||
|---|---|
| `cfs` | [CompletableFuture](CompletableFuture.md)\<\*\>!: the CompletableFutures |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!>!` | a new CompletableFuture that is completed with the result or exception of any of the given CompletableFutures when one completes |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the array or any of its elements are `null` |

### applyToEither

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <U : Any!> applyToEither(
    other: CompletionStage<out T>!, 
    fn: Function<in T, U>!
): CompletableFuture<U>!
```

Returns a new CompletionStage that, when either this or the other given stage complete normally, is executed with the corresponding result as argument to the supplied function. See the CompletionStage documentation for rules covering exceptional completion.

| Parameters ||
|---|---|
| `<U>` | the function's return type |
| `other` | [CompletionStage](CompletionStage.md)\<out T\>!: the other CompletionStage |
| `fn` | [Function](../java.util.function/Function.md)\<in T, U\>!: the function to use to compute the value of the returned CompletionStage |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<U>!` | the new CompletionStage |

### applyToEitherAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <U : Any!> applyToEitherAsync(
    other: CompletionStage<out T>!, 
    fn: Function<in T, U>!
): CompletableFuture<U>!
```

Returns a new CompletionStage that, when either this or the other given stage complete normally, is executed using this stage's default asynchronous execution facility, with the corresponding result as argument to the supplied function. See the CompletionStage documentation for rules covering exceptional completion.

| Parameters ||
|---|---|
| `<U>` | the function's return type |
| `other` | [CompletionStage](CompletionStage.md)\<out T\>!: the other CompletionStage |
| `fn` | [Function](../java.util.function/Function.md)\<in T, U\>!: the function to use to compute the value of the returned CompletionStage |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<U>!` | the new CompletionStage |

### applyToEitherAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <U : Any!> applyToEitherAsync(
    other: CompletionStage<out T>!, 
    fn: Function<in T, U>!, 
    executor: Executor!
): CompletableFuture<U>!
```

Returns a new CompletionStage that, when either this or the other given stage complete normally, is executed using the supplied executor, with the corresponding result as argument to the supplied function. See the CompletionStage documentation for rules covering exceptional completion.

| Parameters ||
|---|---|
| `<U>` | the function's return type |
| `other` | [CompletionStage](CompletionStage.md)\<out T\>!: the other CompletionStage |
| `fn` | [Function](../java.util.function/Function.md)\<in T, U\>!: the function to use to compute the value of the returned CompletionStage |
| --- | --- |
| `executor` | [Executor](Executor.md)!: the executor to use for asynchronous execution |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<U>!` | the new CompletionStage |

### cancel

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun cancel(mayInterruptIfRunning: Boolean): Boolean
```

If not already completed, completes this CompletableFuture with a CancellationException. Dependent CompletableFutures that have not already completed will also complete exceptionally, with a CompletionException caused by this `CancellationException`.

| Parameters ||
|---|---|
| `mayInterruptIfRunning` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): this value has no effect in this implementation because interrupts are not used to control processing. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this task is now cancelled |

### complete

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun complete(value: T): Boolean
```

If not already completed, sets the value returned by get and related methods to the given value.

| Parameters ||
|---|---|
| `value` | T: the result value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this invocation caused this CompletableFuture to transition to a completed state, else `false` |

### completeAsync

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun completeAsync(supplier: Supplier<out T>!): CompletableFuture<T>!
```

Completes this CompletableFuture with the result of the given Supplier function invoked from an asynchronous task using the default executor.

| Parameters ||
|---|---|
| `supplier` | [Supplier](../java.util.function/Supplier.md)\<out T\>!: a function returning the value to be used to complete this CompletableFuture |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<T>!` | this CompletableFuture |

### completeAsync

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun completeAsync(
    supplier: Supplier<out T>!, 
    executor: Executor!
): CompletableFuture<T>!
```

Completes this CompletableFuture with the result of the given Supplier function invoked from an asynchronous task using the given executor.

| Parameters ||
|---|---|
| `supplier` | [Supplier](../java.util.function/Supplier.md)\<out T\>!: a function returning the value to be used to complete this CompletableFuture |
| `executor` | [Executor](Executor.md)!: the executor to use for asynchronous execution |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<T>!` | this CompletableFuture |

### completeExceptionally

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun completeExceptionally(ex: Throwable!): Boolean
```

If not already completed, causes invocations of get and related methods to throw the given exception.

| Parameters ||
|---|---|
| `ex` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!: the exception |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this invocation caused this CompletableFuture to transition to a completed state, else `false` |

### completeOnTimeout

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun completeOnTimeout(
    value: T, 
    timeout: Long, 
    unit: TimeUnit!
): CompletableFuture<T>!
```

Completes this CompletableFuture with the given value if not otherwise completed before the given timeout.

| Parameters ||
|---|---|
| `value` | T: the value to use upon timeout |
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): how long to wait before completing normally with the given value, in units of `unit` |
| `unit` | [TimeUnit](TimeUnit.md)!: a `TimeUnit` determining how to interpret the `timeout` parameter |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<T>!` | this CompletableFuture |

### completedFuture

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <U : Any!> completedFuture(value: U): CompletableFuture<U>!
```

Returns a new CompletableFuture that is already completed with the given value.

| Parameters ||
|---|---|
| `<U>` | the type of the value |
| `value` | U: the value |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<U>!` | the completed CompletableFuture |

### completedStage

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <U : Any!> completedStage(value: U): CompletionStage<U>!
```

Returns a new CompletionStage that is already completed with the given value and supports only those methods in interface CompletionStage.

| Parameters ||
|---|---|
| `<U>` | the type of the value |
| `value` | U: the value |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletionStage<U>!` | the completed CompletionStage |

### copy

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copy(): CompletableFuture<T>!
```

Returns a new CompletableFuture that is completed normally with the same value as this CompletableFuture when it completes normally. If this CompletableFuture completes exceptionally, then the returned CompletableFuture completes exceptionally with a CompletionException with this exception as cause. The behavior is equivalent to `thenApply(x -> x)`. This method may be useful as a form of "defensive copying", to prevent clients from completing, while still being able to arrange dependent actions.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<T>!` | the new CompletableFuture |

### defaultExecutor

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun defaultExecutor(): Executor!
```

Returns the default Executor used for async methods that do not specify an Executor. This class uses the commonPool if it supports more than one parallel thread, or else an Executor using one thread per async task. This method may be overridden in subclasses to return an Executor that provides at least one independent thread.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor!` | the executor |

### delayedExecutor

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun delayedExecutor(
    delay: Long, 
    unit: TimeUnit!
): Executor!
```

Returns a new Executor that submits a task to the default executor after the given delay (or no delay if non-positive). Each delay commences upon invocation of the returned executor's `execute` method.

| Parameters ||
|---|---|
| `delay` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): how long to delay, in units of `unit` |
| `unit` | [TimeUnit](TimeUnit.md)!: a `TimeUnit` determining how to interpret the `delay` parameter |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor!` | the new delayed executor |

### delayedExecutor

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun delayedExecutor(
    delay: Long, 
    unit: TimeUnit!, 
    executor: Executor!
): Executor!
```

Returns a new Executor that submits a task to the given base executor after the given delay (or no delay if non-positive). Each delay commences upon invocation of the returned executor's `execute` method.

| Parameters ||
|---|---|
| `delay` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): how long to delay, in units of `unit` |
| `unit` | [TimeUnit](TimeUnit.md)!: a `TimeUnit` determining how to interpret the `delay` parameter |
| `executor` | [Executor](Executor.md)!: the base executor |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor!` | the new delayed executor |

### exceptionNow

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun exceptionNow(): Throwable!
```

Returns the exception thrown by the task, without waiting.

This method is for cases where the caller knows that the task has already completed with an exception.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html!` | the exception thrown by the task |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the task has not completed, the task completed normally, or the task was cancelled |

### exceptionally

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun exceptionally(fn: Function<Throwable!, out T>!): CompletableFuture<T>!
```

Returns a new CompletionStage that, when this stage completes exceptionally, is executed with this stage's exception as the argument to the supplied function. Otherwise, if this stage completes normally, then the returned stage also completes normally with the same value.

| Parameters ||
|---|---|
| `fn` | [Function](../java.util.function/Function.md)\< [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!, out T\>!: the function to use to compute the value of the returned CompletionStage if this CompletionStage completed exceptionally |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<T>!` | the new CompletionStage |

### exceptionallyAsync

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun exceptionallyAsync(fn: Function<Throwable!, out T>!): CompletableFuture<T>!
```

Returns a new CompletionStage that, when this stage completes exceptionally, is executed with this stage's exception as the argument to the supplied function, using this stage's default asynchronous execution facility. Otherwise, if this stage completes normally, then the returned stage also completes normally with the same value.

| Parameters ||
|---|---|
| `fn` | [Function](../java.util.function/Function.md)\< [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!, out T\>!: the function to use to compute the value of the returned CompletionStage if this CompletionStage completed exceptionally |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<T>!` | the new CompletionStage |

### exceptionallyAsync

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun exceptionallyAsync(
    fn: Function<Throwable!, out T>!, 
    executor: Executor!
): CompletableFuture<T>!
```

Returns a new CompletionStage that, when this stage completes exceptionally, is executed with this stage's exception as the argument to the supplied function, using the supplied Executor. Otherwise, if this stage completes normally, then the returned stage also completes normally with the same value.

| Parameters ||
|---|---|
| `fn` | [Function](../java.util.function/Function.md)\< [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!, out T\>!: the function to use to compute the value of the returned CompletionStage if this CompletionStage completed exceptionally |
| `executor` | [Executor](Executor.md)!: the executor to use for asynchronous execution |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<T>!` | the new CompletionStage |

### exceptionallyCompose

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun exceptionallyCompose(fn: Function<Throwable!, out CompletionStage<T>!>!): CompletableFuture<T>!
```

Returns a new CompletionStage that, when this stage completes exceptionally, is composed using the results of the supplied function applied to this stage's exception.

| Parameters ||
|---|---|
| `fn` | [Function](../java.util.function/Function.md)\< [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!, out [CompletionStage](CompletionStage.md)\<T\>!\>!: the function to use to compute the returned CompletionStage if this CompletionStage completed exceptionally |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<T>!` | the new CompletionStage |

### exceptionallyComposeAsync

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun exceptionallyComposeAsync(fn: Function<Throwable!, out CompletionStage<T>!>!): CompletableFuture<T>!
```

Returns a new CompletionStage that, when this stage completes exceptionally, is composed using the results of the supplied function applied to this stage's exception, using this stage's default asynchronous execution facility.

| Parameters ||
|---|---|
| `fn` | [Function](../java.util.function/Function.md)\< [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!, out [CompletionStage](CompletionStage.md)\<T\>!\>!: the function to use to compute the returned CompletionStage if this CompletionStage completed exceptionally |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<T>!` | the new CompletionStage |

### exceptionallyComposeAsync

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun exceptionallyComposeAsync(
    fn: Function<Throwable!, out CompletionStage<T>!>!, 
    executor: Executor!
): CompletableFuture<T>!
```

Returns a new CompletionStage that, when this stage completes exceptionally, is composed using the results of the supplied function applied to this stage's exception, using the supplied Executor.

| Parameters ||
|---|---|
| `fn` | [Function](../java.util.function/Function.md)\< [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!, out [CompletionStage](CompletionStage.md)\<T\>!\>!: the function to use to compute the returned CompletionStage if this CompletionStage completed exceptionally |
| `executor` | [Executor](Executor.md)!: the executor to use for asynchronous execution |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<T>!` | the new CompletionStage |

### failedFuture

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <U : Any!> failedFuture(ex: Throwable!): CompletableFuture<U>!
```

Returns a new CompletableFuture that is already completed exceptionally with the given exception.

| Parameters ||
|---|---|
| `<U>` | the type of the value |
| `ex` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!: the exception |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<U>!` | the exceptionally completed CompletableFuture |

### failedStage

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <U : Any!> failedStage(ex: Throwable!): CompletionStage<U>!
```

Returns a new CompletionStage that is already completed exceptionally with the given exception and supports only those methods in interface CompletionStage.

| Parameters ||
|---|---|
| `<U>` | the type of the value |
| `ex` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!: the exception |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletionStage<U>!` | the exceptionally completed CompletionStage |

### get

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun get(): T
```

Waits if necessary for this future to complete, and then returns its result.

| Return ||
|---|---|
| `T` | the result value |

| Exceptions ||
|---|---|
| `java.lang.InterruptedException` | if the current thread was interrupted while waiting |
| `java.util.concurrent.CancellationException` | if this future was cancelled |
| `java.util.concurrent.ExecutionException` | if this future completed exceptionally |
| --- | --- |

### get

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun get(
    timeout: Long, 
    unit: TimeUnit!
): T
```

Waits if necessary for at most the given time for this future to complete, and then returns its result, if available.

| Parameters ||
|---|---|
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the maximum time to wait |
| `unit` | [TimeUnit](TimeUnit.md)!: the time unit of the timeout argument |

| Return ||
|---|---|
| `T` | the result value |

| Exceptions ||
|---|---|
| `java.lang.InterruptedException` | if the current thread was interrupted while waiting |
| `java.util.concurrent.CancellationException` | if this future was cancelled |
| `java.util.concurrent.ExecutionException` | if this future completed exceptionally |
| --- | --- |
| `java.util.concurrent.TimeoutException` | if the wait timed out |

### getNow

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNow(valueIfAbsent: T): T
```

Returns the result value (or throws any encountered exception) if completed, else returns the given valueIfAbsent.

| Parameters ||
|---|---|
| `valueIfAbsent` | T: the value to return if not completed |

| Return ||
|---|---|
| `T` | the result value, if completed, else the given valueIfAbsent |

| Exceptions ||
|---|---|
| `java.util.concurrent.CancellationException` | if the computation was cancelled |
| `java.util.concurrent.CompletionException` | if this future completed exceptionally or a completion computation threw an exception |

### getNumberOfDependents

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNumberOfDependents(): Int
```

Returns the estimated number of CompletableFutures whose completions are awaiting completion of this CompletableFuture. This method is designed for use in monitoring system state, not for synchronization control.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of dependent CompletableFutures |

### handle

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <U : Any!> handle(fn: BiFunction<in T, Throwable!, out U>!): CompletableFuture<U>!
```

Returns a new CompletionStage that, when this stage completes either normally or exceptionally, is executed with this stage's result and exception as arguments to the supplied function.

When this stage is complete, the given function is invoked with the result (or `null` if none) and the exception (or `null` if none) of this stage as arguments, and the function's result is used to complete the returned stage.

| Parameters ||
|---|---|
| `<U>` | the function's return type |
| `fn` | [BiFunction](../java.util.function/BiFunction.md)\<in T, [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!, out U\>!: the function to use to compute the value of the returned CompletionStage |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<U>!` | the new CompletionStage |

### handleAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <U : Any!> handleAsync(fn: BiFunction<in T, Throwable!, out U>!): CompletableFuture<U>!
```

Returns a new CompletionStage that, when this stage completes either normally or exceptionally, is executed using this stage's default asynchronous execution facility, with this stage's result and exception as arguments to the supplied function.

When this stage is complete, the given function is invoked with the result (or `null` if none) and the exception (or `null` if none) of this stage as arguments, and the function's result is used to complete the returned stage.

| Parameters ||
|---|---|
| `<U>` | the function's return type |
| `fn` | [BiFunction](../java.util.function/BiFunction.md)\<in T, [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!, out U\>!: the function to use to compute the value of the returned CompletionStage |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<U>!` | the new CompletionStage |

### handleAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <U : Any!> handleAsync(
    fn: BiFunction<in T, Throwable!, out U>!, 
    executor: Executor!
): CompletableFuture<U>!
```

Returns a new CompletionStage that, when this stage completes either normally or exceptionally, is executed using the supplied executor, with this stage's result and exception as arguments to the supplied function.

When this stage is complete, the given function is invoked with the result (or `null` if none) and the exception (or `null` if none) of this stage as arguments, and the function's result is used to complete the returned stage.

| Parameters ||
|---|---|
| `<U>` | the function's return type |
| `fn` | [BiFunction](../java.util.function/BiFunction.md)\<in T, [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!, out U\>!: the function to use to compute the value of the returned CompletionStage |
| `executor` | [Executor](Executor.md)!: the executor to use for asynchronous execution |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<U>!` | the new CompletionStage |

### isCancelled

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isCancelled(): Boolean
```

Returns `true` if this CompletableFuture was cancelled before it completed normally.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this CompletableFuture was cancelled before it completed normally |

### isCompletedExceptionally

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isCompletedExceptionally(): Boolean
```

Returns `true` if this CompletableFuture completed exceptionally, in any way. Possible causes include cancellation, explicit invocation of `completeExceptionally`, and abrupt termination of a CompletionStage action.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this CompletableFuture completed exceptionally |

### isDone

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isDone(): Boolean
```

Returns `true` if completed in any fashion: normally, exceptionally, or via cancellation.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if completed |

### join

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun join(): T
```

Returns the result value when complete, or throws an (unchecked) exception if completed exceptionally. To better conform with the use of common functional forms, if a computation involved in the completion of this CompletableFuture threw an exception, this method throws an (unchecked) CompletionException with the underlying exception as its cause.

| Return ||
|---|---|
| `T` | the result value |

| Exceptions ||
|---|---|
| `java.util.concurrent.CancellationException` | if the computation was cancelled |
| `java.util.concurrent.CompletionException` | if this future completed exceptionally or a completion computation threw an exception |

### minimalCompletionStage

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun minimalCompletionStage(): CompletionStage<T>!
```

Returns a new CompletionStage that is completed normally with the same value as this CompletableFuture when it completes normally, and cannot be independently completed or otherwise used in ways not defined by the methods of interface CompletionStage. If this CompletableFuture completes exceptionally, then the returned CompletionStage completes exceptionally with a CompletionException with this exception as cause.

Unless overridden by a subclass, a new non-minimal CompletableFuture with all methods available can be obtained from a minimal CompletionStage via toCompletableFuture. For example, completion of a minimal stage can be awaited by

```kotlin
<code>minimalStage.toCompletableFuture().join(); </code>
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletionStage<T>!` | the new CompletionStage |

### newIncompleteFuture

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <U : Any!> newIncompleteFuture(): CompletableFuture<U>!
```

Returns a new incomplete CompletableFuture of the type to be returned by a CompletionStage method. Subclasses should normally override this method to return an instance of the same class as this CompletableFuture. The default implementation returns an instance of class CompletableFuture.

| Parameters ||
|---|---|
| `<U>` | the type of the value |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<U>!` | a new CompletableFuture |

### obtrudeException

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun obtrudeException(ex: Throwable!): Unit
```

Forcibly causes subsequent invocations of method get and related methods to throw the given exception, whether or not already completed. This method is designed for use only in error recovery actions, and even in such situations may result in ongoing dependent completions using established versus overwritten outcomes.

| Parameters ||
|---|---|
| `ex` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!: the exception |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the exception is null |

### obtrudeValue

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun obtrudeValue(value: T): Unit
```

Forcibly sets or resets the value subsequently returned by method get and related methods, whether or not already completed. This method is designed for use only in error recovery actions, and even in such situations may result in ongoing dependent completions using established versus overwritten outcomes.

| Parameters ||
|---|---|
| `value` | T: the completion value |

### orTimeout

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun orTimeout(
    timeout: Long, 
    unit: TimeUnit!
): CompletableFuture<T>!
```

Exceptionally completes this CompletableFuture with a TimeoutException if not otherwise completed before the given timeout.

| Parameters ||
|---|---|
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): how long to wait before completing exceptionally with a TimeoutException, in units of `unit` |
| `unit` | [TimeUnit](TimeUnit.md)!: a `TimeUnit` determining how to interpret the `timeout` parameter |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<T>!` | this CompletableFuture |

### resultNow

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun resultNow(): T
```

Returns the computed result, without waiting.

This method is for cases where the caller knows that the task has already completed successfully, for example when filtering a stream of Future objects for the successful tasks and using a mapping operation to obtain a stream of results. {@snippet lang=java : \* results = futures.stream() \* .filter(f -\> f.state() == Future.State.SUCCESS) \* .map(Future::resultNow) \* .toList(); \* }

| Return ||
|---|---|
| `T` | the computed result |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the task has not completed or the task did not complete with a result |

### runAfterBoth

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun runAfterBoth(
    other: CompletionStage<*>!, 
    action: Runnable!
): CompletableFuture<Void!>!
```

Returns a new CompletionStage that, when this and the other given stage both complete normally, executes the given action. See the CompletionStage documentation for rules covering exceptional completion.

| Parameters ||
|---|---|
| `other` | [CompletionStage](CompletionStage.md)\<\*\>!: the other CompletionStage |
| `action` | [Runnable](../java.lang/Runnable.md)!: the action to perform before completing the returned CompletionStage |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<https://developer.android.com/reference/kotlin/java/lang/Void.html#!>!` | the new CompletionStage |

### runAfterBothAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun runAfterBothAsync(
    other: CompletionStage<*>!, 
    action: Runnable!
): CompletableFuture<Void!>!
```

Returns a new CompletionStage that, when this and the other given stage both complete normally, executes the given action using this stage's default asynchronous execution facility. See the CompletionStage documentation for rules covering exceptional completion.

| Parameters ||
|---|---|
| `other` | [CompletionStage](CompletionStage.md)\<\*\>!: the other CompletionStage |
| `action` | [Runnable](../java.lang/Runnable.md)!: the action to perform before completing the returned CompletionStage |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<https://developer.android.com/reference/kotlin/java/lang/Void.html#!>!` | the new CompletionStage |

### runAfterBothAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun runAfterBothAsync(
    other: CompletionStage<*>!, 
    action: Runnable!, 
    executor: Executor!
): CompletableFuture<Void!>!
```

Returns a new CompletionStage that, when this and the other given stage both complete normally, executes the given action using the supplied executor. See the CompletionStage documentation for rules covering exceptional completion.

| Parameters ||
|---|---|
| `other` | [CompletionStage](CompletionStage.md)\<\*\>!: the other CompletionStage |
| `action` | [Runnable](../java.lang/Runnable.md)!: the action to perform before completing the returned CompletionStage |
| `executor` | [Executor](Executor.md)!: the executor to use for asynchronous execution |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<https://developer.android.com/reference/kotlin/java/lang/Void.html#!>!` | the new CompletionStage |

### runAfterEither

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun runAfterEither(
    other: CompletionStage<*>!, 
    action: Runnable!
): CompletableFuture<Void!>!
```

Returns a new CompletionStage that, when either this or the other given stage complete normally, executes the given action. See the CompletionStage documentation for rules covering exceptional completion.

| Parameters ||
|---|---|
| `other` | [CompletionStage](CompletionStage.md)\<\*\>!: the other CompletionStage |
| `action` | [Runnable](../java.lang/Runnable.md)!: the action to perform before completing the returned CompletionStage |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<https://developer.android.com/reference/kotlin/java/lang/Void.html#!>!` | the new CompletionStage |

### runAfterEitherAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun runAfterEitherAsync(
    other: CompletionStage<*>!, 
    action: Runnable!
): CompletableFuture<Void!>!
```

Returns a new CompletionStage that, when either this or the other given stage complete normally, executes the given action using this stage's default asynchronous execution facility. See the CompletionStage documentation for rules covering exceptional completion.

| Parameters ||
|---|---|
| `other` | [CompletionStage](CompletionStage.md)\<\*\>!: the other CompletionStage |
| `action` | [Runnable](../java.lang/Runnable.md)!: the action to perform before completing the returned CompletionStage |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<https://developer.android.com/reference/kotlin/java/lang/Void.html#!>!` | the new CompletionStage |

### runAfterEitherAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun runAfterEitherAsync(
    other: CompletionStage<*>!, 
    action: Runnable!, 
    executor: Executor!
): CompletableFuture<Void!>!
```

Returns a new CompletionStage that, when either this or the other given stage complete normally, executes the given action using the supplied executor. See the CompletionStage documentation for rules covering exceptional completion.

| Parameters ||
|---|---|
| `other` | [CompletionStage](CompletionStage.md)\<\*\>!: the other CompletionStage |
| `action` | [Runnable](../java.lang/Runnable.md)!: the action to perform before completing the returned CompletionStage |
| `executor` | [Executor](Executor.md)!: the executor to use for asynchronous execution |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<https://developer.android.com/reference/kotlin/java/lang/Void.html#!>!` | the new CompletionStage |

### runAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun runAsync(runnable: Runnable!): CompletableFuture<Void!>!
```

Returns a new CompletableFuture that is asynchronously completed by a task running in the commonPool after it runs the given action.

| Parameters ||
|---|---|
| `runnable` | [Runnable](../java.lang/Runnable.md)!: the action to run before completing the returned CompletableFuture |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<https://developer.android.com/reference/kotlin/java/lang/Void.html#!>!` | the new CompletableFuture |

### runAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun runAsync(
    runnable: Runnable!, 
    executor: Executor!
): CompletableFuture<Void!>!
```

Returns a new CompletableFuture that is asynchronously completed by a task running in the given executor after it runs the given action.

| Parameters ||
|---|---|
| `runnable` | [Runnable](../java.lang/Runnable.md)!: the action to run before completing the returned CompletableFuture |
| `executor` | [Executor](Executor.md)!: the executor to use for asynchronous execution |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<https://developer.android.com/reference/kotlin/java/lang/Void.html#!>!` | the new CompletableFuture |

### state

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun state(): Future.State!
```

{@return the computation state}

### supplyAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <U : Any!> supplyAsync(supplier: Supplier<U>!): CompletableFuture<U>!
```

Returns a new CompletableFuture that is asynchronously completed by a task running in the commonPool with the value obtained by calling the given Supplier.

| Parameters ||
|---|---|
| `<U>` | the function's return type |
| `supplier` | [Supplier](../java.util.function/Supplier.md)\<U\>!: a function returning the value to be used to complete the returned CompletableFuture |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<U>!` | the new CompletableFuture |

### supplyAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <U : Any!> supplyAsync(
    supplier: Supplier<U>!, 
    executor: Executor!
): CompletableFuture<U>!
```

Returns a new CompletableFuture that is asynchronously completed by a task running in the given executor with the value obtained by calling the given Supplier.

| Parameters ||
|---|---|
| `<U>` | the function's return type |
| `supplier` | [Supplier](../java.util.function/Supplier.md)\<U\>!: a function returning the value to be used to complete the returned CompletableFuture |
| `executor` | [Executor](Executor.md)!: the executor to use for asynchronous execution |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<U>!` | the new CompletableFuture |

### thenAccept

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun thenAccept(action: Consumer<in T>!): CompletableFuture<Void!>!
```

Returns a new CompletionStage that, when this stage completes normally, is executed with this stage's result as the argument to the supplied action. See the CompletionStage documentation for rules covering exceptional completion.

| Parameters ||
|---|---|
| `action` | [Consumer](../java.util.function/Consumer.md)\<in T\>!: the action to perform before completing the returned CompletionStage |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<https://developer.android.com/reference/kotlin/java/lang/Void.html#!>!` | the new CompletionStage |

### thenAcceptAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun thenAcceptAsync(action: Consumer<in T>!): CompletableFuture<Void!>!
```

Returns a new CompletionStage that, when this stage completes normally, is executed using this stage's default asynchronous execution facility, with this stage's result as the argument to the supplied action. See the CompletionStage documentation for rules covering exceptional completion.

| Parameters ||
|---|---|
| `action` | [Consumer](../java.util.function/Consumer.md)\<in T\>!: the action to perform before completing the returned CompletionStage |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<https://developer.android.com/reference/kotlin/java/lang/Void.html#!>!` | the new CompletionStage |

### thenAcceptAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun thenAcceptAsync(
    action: Consumer<in T>!, 
    executor: Executor!
): CompletableFuture<Void!>!
```

Returns a new CompletionStage that, when this stage completes normally, is executed using the supplied Executor, with this stage's result as the argument to the supplied action. See the CompletionStage documentation for rules covering exceptional completion.

| Parameters ||
|---|---|
| `action` | [Consumer](../java.util.function/Consumer.md)\<in T\>!: the action to perform before completing the returned CompletionStage |
| `executor` | [Executor](Executor.md)!: the executor to use for asynchronous execution |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<https://developer.android.com/reference/kotlin/java/lang/Void.html#!>!` | the new CompletionStage |

### thenAcceptBoth

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <U : Any!> thenAcceptBoth(
    other: CompletionStage<out U>!, 
    action: BiConsumer<in T, in U>!
): CompletableFuture<Void!>!
```

Returns a new CompletionStage that, when this and the other given stage both complete normally, is executed with the two results as arguments to the supplied action. See the CompletionStage documentation for rules covering exceptional completion.

| Parameters ||
|---|---|
| `<U>` | the type of the other CompletionStage's result |
| `other` | [CompletionStage](CompletionStage.md)\<out U\>!: the other CompletionStage |
| `action` | [BiConsumer](../java.util.function/BiConsumer.md)\<in T, in U\>!: the action to perform before completing the returned CompletionStage |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<https://developer.android.com/reference/kotlin/java/lang/Void.html#!>!` | the new CompletionStage |

### thenAcceptBothAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <U : Any!> thenAcceptBothAsync(
    other: CompletionStage<out U>!, 
    action: BiConsumer<in T, in U>!
): CompletableFuture<Void!>!
```

Returns a new CompletionStage that, when this and the other given stage both complete normally, is executed using this stage's default asynchronous execution facility, with the two results as arguments to the supplied action. See the CompletionStage documentation for rules covering exceptional completion.

| Parameters ||
|---|---|
| `<U>` | the type of the other CompletionStage's result |
| `other` | [CompletionStage](CompletionStage.md)\<out U\>!: the other CompletionStage |
| `action` | [BiConsumer](../java.util.function/BiConsumer.md)\<in T, in U\>!: the action to perform before completing the returned CompletionStage |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<https://developer.android.com/reference/kotlin/java/lang/Void.html#!>!` | the new CompletionStage |

### thenAcceptBothAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <U : Any!> thenAcceptBothAsync(
    other: CompletionStage<out U>!, 
    action: BiConsumer<in T, in U>!, 
    executor: Executor!
): CompletableFuture<Void!>!
```

Returns a new CompletionStage that, when this and the other given stage both complete normally, is executed using the supplied executor, with the two results as arguments to the supplied action. See the CompletionStage documentation for rules covering exceptional completion.

| Parameters ||
|---|---|
| `<U>` | the type of the other CompletionStage's result |
| `other` | [CompletionStage](CompletionStage.md)\<out U\>!: the other CompletionStage |
| `action` | [BiConsumer](../java.util.function/BiConsumer.md)\<in T, in U\>!: the action to perform before completing the returned CompletionStage |
| --- | --- |
| `executor` | [Executor](Executor.md)!: the executor to use for asynchronous execution |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<https://developer.android.com/reference/kotlin/java/lang/Void.html#!>!` | the new CompletionStage |

### thenApply

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <U : Any!> thenApply(fn: Function<in T, out U>!): CompletableFuture<U>!
```

Returns a new CompletionStage that, when this stage completes normally, is executed with this stage's result as the argument to the supplied function.

This method is analogous to map and map.

See the CompletionStage documentation for rules covering exceptional completion.

| Parameters ||
|---|---|
| `<U>` | the function's return type |
| `fn` | [Function](../java.util.function/Function.md)\<in T, out U\>!: the function to use to compute the value of the returned CompletionStage |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<U>!` | the new CompletionStage |

### thenApplyAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <U : Any!> thenApplyAsync(fn: Function<in T, out U>!): CompletableFuture<U>!
```

Returns a new CompletionStage that, when this stage completes normally, is executed using this stage's default asynchronous execution facility, with this stage's result as the argument to the supplied function. See the CompletionStage documentation for rules covering exceptional completion.

| Parameters ||
|---|---|
| `<U>` | the function's return type |
| `fn` | [Function](../java.util.function/Function.md)\<in T, out U\>!: the function to use to compute the value of the returned CompletionStage |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<U>!` | the new CompletionStage |

### thenApplyAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <U : Any!> thenApplyAsync(
    fn: Function<in T, out U>!, 
    executor: Executor!
): CompletableFuture<U>!
```

Returns a new CompletionStage that, when this stage completes normally, is executed using the supplied Executor, with this stage's result as the argument to the supplied function. See the CompletionStage documentation for rules covering exceptional completion.

| Parameters ||
|---|---|
| `<U>` | the function's return type |
| `fn` | [Function](../java.util.function/Function.md)\<in T, out U\>!: the function to use to compute the value of the returned CompletionStage |
| `executor` | [Executor](Executor.md)!: the executor to use for asynchronous execution |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<U>!` | the new CompletionStage |

### thenCombine

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <U : Any!, V : Any!> thenCombine(
    other: CompletionStage<out U>!, 
    fn: BiFunction<in T, in U, out V>!
): CompletableFuture<V>!
```

Returns a new CompletionStage that, when this and the other given stage both complete normally, is executed with the two results as arguments to the supplied function. See the CompletionStage documentation for rules covering exceptional completion.

| Parameters ||
|---|---|
| `<U>` | the type of the other CompletionStage's result |
| `<V>` | the function's return type |
| `other` | [CompletionStage](CompletionStage.md)\<out U\>!: the other CompletionStage |
| --- | --- |
| `fn` | [BiFunction](../java.util.function/BiFunction.md)\<in T, in U, out V\>!: the function to use to compute the value of the returned CompletionStage |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<V>!` | the new CompletionStage |

### thenCombineAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <U : Any!, V : Any!> thenCombineAsync(
    other: CompletionStage<out U>!, 
    fn: BiFunction<in T, in U, out V>!
): CompletableFuture<V>!
```

Returns a new CompletionStage that, when this and the other given stage both complete normally, is executed using this stage's default asynchronous execution facility, with the two results as arguments to the supplied function. See the CompletionStage documentation for rules covering exceptional completion.

| Parameters ||
|---|---|
| `<U>` | the type of the other CompletionStage's result |
| `<V>` | the function's return type |
| `other` | [CompletionStage](CompletionStage.md)\<out U\>!: the other CompletionStage |
| --- | --- |
| `fn` | [BiFunction](../java.util.function/BiFunction.md)\<in T, in U, out V\>!: the function to use to compute the value of the returned CompletionStage |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<V>!` | the new CompletionStage |

### thenCombineAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <U : Any!, V : Any!> thenCombineAsync(
    other: CompletionStage<out U>!, 
    fn: BiFunction<in T, in U, out V>!, 
    executor: Executor!
): CompletableFuture<V>!
```

Returns a new CompletionStage that, when this and the other given stage both complete normally, is executed using the supplied executor, with the two results as arguments to the supplied function. See the CompletionStage documentation for rules covering exceptional completion.

| Parameters ||
|---|---|
| `<U>` | the type of the other CompletionStage's result |
| `<V>` | the function's return type |
| `other` | [CompletionStage](CompletionStage.md)\<out U\>!: the other CompletionStage |
| --- | --- |
| `fn` | [BiFunction](../java.util.function/BiFunction.md)\<in T, in U, out V\>!: the function to use to compute the value of the returned CompletionStage |
| `executor` | [Executor](Executor.md)!: the executor to use for asynchronous execution |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<V>!` | the new CompletionStage |

### thenCompose

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <U : Any!> thenCompose(fn: Function<in T, out CompletionStage<U>!>!): CompletableFuture<U>!
```

Returns a new CompletionStage that is completed with the same value as the CompletionStage returned by the given function.

When this stage completes normally, the given function is invoked with this stage's result as the argument, returning another CompletionStage. When that stage completes normally, the CompletionStage returned by this method is completed with the same value.

To ensure progress, the supplied function must arrange eventual completion of its result.

This method is analogous to flatMap and flatMap.

See the CompletionStage documentation for rules covering exceptional completion.

| Parameters ||
|---|---|
| `<U>` | the type of the returned CompletionStage's result |
| `fn` | [Function](../java.util.function/Function.md)\<in T, out [CompletionStage](CompletionStage.md)\<U\>!\>!: the function to use to compute another CompletionStage |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<U>!` | the new CompletionStage |

### thenComposeAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <U : Any!> thenComposeAsync(fn: Function<in T, out CompletionStage<U>!>!): CompletableFuture<U>!
```

Returns a new CompletionStage that is completed with the same value as the CompletionStage returned by the given function, executed using this stage's default asynchronous execution facility.

When this stage completes normally, the given function is invoked with this stage's result as the argument, returning another CompletionStage. When that stage completes normally, the CompletionStage returned by this method is completed with the same value.

To ensure progress, the supplied function must arrange eventual completion of its result.

See the CompletionStage documentation for rules covering exceptional completion.

| Parameters ||
|---|---|
| `<U>` | the type of the returned CompletionStage's result |
| `fn` | [Function](../java.util.function/Function.md)\<in T, out [CompletionStage](CompletionStage.md)\<U\>!\>!: the function to use to compute another CompletionStage |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<U>!` | the new CompletionStage |

### thenComposeAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <U : Any!> thenComposeAsync(
    fn: Function<in T, out CompletionStage<U>!>!, 
    executor: Executor!
): CompletableFuture<U>!
```

Returns a new CompletionStage that is completed with the same value as the CompletionStage returned by the given function, executed using the supplied Executor.

When this stage completes normally, the given function is invoked with this stage's result as the argument, returning another CompletionStage. When that stage completes normally, the CompletionStage returned by this method is completed with the same value.

To ensure progress, the supplied function must arrange eventual completion of its result.

See the CompletionStage documentation for rules covering exceptional completion.

| Parameters ||
|---|---|
| `<U>` | the type of the returned CompletionStage's result |
| `fn` | [Function](../java.util.function/Function.md)\<in T, out [CompletionStage](CompletionStage.md)\<U\>!\>!: the function to use to compute another CompletionStage |
| `executor` | [Executor](Executor.md)!: the executor to use for asynchronous execution |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<U>!` | the new CompletionStage |

### thenRun

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun thenRun(action: Runnable!): CompletableFuture<Void!>!
```

Returns a new CompletionStage that, when this stage completes normally, executes the given action. See the CompletionStage documentation for rules covering exceptional completion.

| Parameters ||
|---|---|
| `action` | [Runnable](../java.lang/Runnable.md)!: the action to perform before completing the returned CompletionStage |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<https://developer.android.com/reference/kotlin/java/lang/Void.html#!>!` | the new CompletionStage |

### thenRunAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun thenRunAsync(action: Runnable!): CompletableFuture<Void!>!
```

Returns a new CompletionStage that, when this stage completes normally, executes the given action using this stage's default asynchronous execution facility. See the CompletionStage documentation for rules covering exceptional completion.

| Parameters ||
|---|---|
| `action` | [Runnable](../java.lang/Runnable.md)!: the action to perform before completing the returned CompletionStage |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<https://developer.android.com/reference/kotlin/java/lang/Void.html#!>!` | the new CompletionStage |

### thenRunAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun thenRunAsync(
    action: Runnable!, 
    executor: Executor!
): CompletableFuture<Void!>!
```

Returns a new CompletionStage that, when this stage completes normally, executes the given action using the supplied Executor. See the CompletionStage documentation for rules covering exceptional completion.

| Parameters ||
|---|---|
| `action` | [Runnable](../java.lang/Runnable.md)!: the action to perform before completing the returned CompletionStage |
| `executor` | [Executor](Executor.md)!: the executor to use for asynchronous execution |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<https://developer.android.com/reference/kotlin/java/lang/Void.html#!>!` | the new CompletionStage |

### toCompletableFuture

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toCompletableFuture(): CompletableFuture<T>!
```

Returns this CompletableFuture.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<T>!` | this CompletableFuture |

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string identifying this CompletableFuture, as well as its completion state. The state, in brackets, contains the String `"Completed Normally"` or the String `"Completed Exceptionally"`, or the String `"Not completed"` followed by the number of CompletableFutures dependent upon its completion, if any.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string identifying this CompletableFuture, as well as its state |

### whenComplete

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun whenComplete(action: BiConsumer<in T, in Throwable!>!): CompletableFuture<T>!
```

Returns a new CompletionStage with the same result or exception as this stage, that executes the given action when this stage completes.

When this stage is complete, the given action is invoked with the result (or `null` if none) and the exception (or `null` if none) of this stage as arguments. The returned stage is completed when the action returns.

Unlike method handle, this method is not designed to translate completion outcomes, so the supplied action should not throw an exception. However, if it does, the following rules apply: if this stage completed normally but the supplied action throws an exception, then the returned stage completes exceptionally with the supplied action's exception. Or, if this stage completed exceptionally and the supplied action throws an exception, then the returned stage completes exceptionally with this stage's exception.

| Parameters ||
|---|---|
| `action` | [BiConsumer](../java.util.function/BiConsumer.md)\<in T, in [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!\>!: the action to perform |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<T>!` | the new CompletionStage |

### whenCompleteAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun whenCompleteAsync(action: BiConsumer<in T, in Throwable!>!): CompletableFuture<T>!
```

Returns a new CompletionStage with the same result or exception as this stage, that executes the given action using this stage's default asynchronous execution facility when this stage completes.

When this stage is complete, the given action is invoked with the result (or `null` if none) and the exception (or `null` if none) of this stage as arguments. The returned stage is completed when the action returns.

Unlike method handleAsync, this method is not designed to translate completion outcomes, so the supplied action should not throw an exception. However, if it does, the following rules apply: If this stage completed normally but the supplied action throws an exception, then the returned stage completes exceptionally with the supplied action's exception. Or, if this stage completed exceptionally and the supplied action throws an exception, then the returned stage completes exceptionally with this stage's exception.

| Parameters ||
|---|---|
| `action` | [BiConsumer](../java.util.function/BiConsumer.md)\<in T, in [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!\>!: the action to perform |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<T>!` | the new CompletionStage |

### whenCompleteAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun whenCompleteAsync(
    action: BiConsumer<in T, in Throwable!>!, 
    executor: Executor!
): CompletableFuture<T>!
```

Returns a new CompletionStage with the same result or exception as this stage, that executes the given action using the supplied Executor when this stage completes.

When this stage is complete, the given action is invoked with the result (or `null` if none) and the exception (or `null` if none) of this stage as arguments. The returned stage is completed when the action returns.

Unlike method handleAsync, this method is not designed to translate completion outcomes, so the supplied action should not throw an exception. However, if it does, the following rules apply: If this stage completed normally but the supplied action throws an exception, then the returned stage completes exceptionally with the supplied action's exception. Or, if this stage completed exceptionally and the supplied action throws an exception, then the returned stage completes exceptionally with this stage's exception.

| Parameters ||
|---|---|
| `action` | [BiConsumer](../java.util.function/BiConsumer.md)\<in T, in [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!\>!: the action to perform |
| `executor` | [Executor](Executor.md)!: the executor to use for asynchronous execution |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CompletableFuture#<T>!` | the new CompletionStage |
