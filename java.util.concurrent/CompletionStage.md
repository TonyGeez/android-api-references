# CompletionStage

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CompletionStage

```
interface CompletionStage<T : Any!>
```

| [java.util.concurrent.CompletionStage](CompletionStage.md) |

| Known Direct Subclasses [CompletableFuture](CompletableFuture.md) |------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [CompletableFuture](CompletableFuture.md) | A [Future](Future.md) that may be explicitly completed (setting its value and status), and may be used as a [CompletionStage](CompletionStage.md), supporting dependent functions and actions that trigger upon its completion. | |
| --- | --- | --- | --- | --- | --- | --- |

A stage of a possibly asynchronous computation, that performs an action or computes a value when another CompletionStage completes. A stage completes upon termination of its computation, but this may in turn trigger other dependent stages. The functionality defined in this interface takes only a few basic forms, which expand out to a larger set of methods to capture a range of usage styles:

- The computation performed by a stage may be expressed as a Function, Consumer, or Runnable (using methods with names including*apply* ,*accept* , or*run* , respectively) depending on whether it requires arguments and/or produces results. For example: 

  ```kotlin
  <code>stage.thenApply(x -&gt; square(x))
         .thenAccept(x -&gt; System.out.print(x))
         .thenRun(() -&gt; System.out.println());</code>
  ```
 An additional form (*compose* ) allows the construction of computation pipelines from functions returning completion stages.

 Any argument to a stage's computation is the outcome of a triggering stage's computation.
- One stage's execution may be triggered by completion of a single stage, or both of two stages, or either of two stages. Dependencies on a single stage are arranged using methods with prefix*then* . Those triggered by completion of*both* of two stages may*combine* their results or effects, using correspondingly named methods. Those triggered by*either*of two stages make no guarantees about which of the results or effects are used for the dependent stage's computation.
- Dependencies among stages control the triggering of computations, but do not otherwise guarantee any particular ordering. Additionally, execution of a new stage's computations may be arranged in any of three ways: default execution, default asynchronous execution (using methods with suffix*async* that employ the stage's default asynchronous execution facility), or custom (via a supplied [Executor](Executor.md)). The execution properties of default and async modes are specified by CompletionStage implementations, not this interface. Methods with explicit Executor arguments may have arbitrary execution properties, and might not even support concurrent execution, but are arranged for processing in a way that accommodates asynchrony.
- Two method forms ([handle](CompletionStage.md))and [whenComplete](CompletionStage.md))) support unconditional computation whether the triggering stage completed normally or exceptionally. Method [exceptionally](CompletionStage.md))supports computation only when the triggering stage completes exceptionally, computing a replacement result, similarly to the java`catch`keyword. In all other cases, if a stage's computation terminates abruptly with an (unchecked) exception or error, then all dependent stages requiring its completion complete exceptionally as well, with a [CompletionException](CompletionException.md) holding the exception as its cause. If a stage is dependent on*both* of two stages, and both complete exceptionally, then the CompletionException may correspond to either one of these exceptions. If a stage is dependent on*either* of two others, and only one of them completes exceptionally, no guarantees are made about whether the dependent stage completes normally or exceptionally. In the case of method`whenComplete`, when the supplied action itself encounters an exception, then the stage completes exceptionally with this exception unless the source stage also completed exceptionally, in which case the exceptional completion from the source stage is given preference and propagated to the dependent stage.

<br />

All methods adhere to the above triggering, execution, and exceptional completion specifications (which are not repeated in individual method specifications). Additionally, while arguments used to pass a completion result (that is, for parameters of type`T`) for methods accepting them may be null, passing a null value for any other parameter will result in a [NullPointerException](../java.lang/NullPointerException.md) being thrown.

Method form [handle](CompletionStage.md))is the most general way of creating a continuation stage, unconditionally performing a computation that is given both the result and exception (if any) of the triggering CompletionStage, and computing an arbitrary result. Method [whenComplete](CompletionStage.md))is similar, but preserves the result of the triggering stage instead of computing a new one. Because a stage's normal result may be`null`, both methods should have a computation structured thus: 

```kotlin
<code>(result, exception) -&gt; {
    if (exception == null) {
      // triggering stage completed normally
    } else {
      // triggering stage completed exceptionally
    }
  }</code>
```

This interface does not define methods for initially creating, forcibly completing normally or exceptionally, probing completion status or results, or awaiting completion of a stage. Implementations of CompletionStage may provide means of achieving such effects, as appropriate. Method [toCompletableFuture](CompletionStage.md))enables interoperability among different implementations of this interface by providing a common conversion type.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [CompletionStage](CompletionStage.md)\< [Void](../java.lang/Void.md)!\>! | [acceptEither](CompletionStage.md))`(`other:` ` [CompletionStage](CompletionStage.md)<out` `T>!`, `action:` ` [Consumer](../java.util.function/Consumer.md)<in` `T>!`)` Returns a new CompletionStage that, when either this or the other given stage complete normally, is executed with the corresponding result as argument to the supplied action. |
| abstract [CompletionStage](CompletionStage.md)\< [Void](../java.lang/Void.md)!\>! | [acceptEitherAsync](CompletionStage.md))`(`other:` ` [CompletionStage](CompletionStage.md)<out` `T>!`, `action:` ` [Consumer](../java.util.function/Consumer.md)<in` `T>!`)` Returns a new CompletionStage that, when either this or the other given stage complete normally, is executed using this stage's default asynchronous execution facility, with the corresponding result as argument to the supplied action. |
| abstract [CompletionStage](CompletionStage.md)\< [Void](../java.lang/Void.md)!\>! | [acceptEitherAsync](CompletionStage.md))`(`other:` ` [CompletionStage](CompletionStage.md)<out` `T>!`, `action:` ` [Consumer](../java.util.function/Consumer.md)<in` `T>!`, `executor:` ` [Executor](Executor.md)!`)` Returns a new CompletionStage that, when either this or the other given stage complete normally, is executed using the supplied executor, with the corresponding result as argument to the supplied action. |
| --- | --- |
| abstract [CompletionStage](CompletionStage.md)\<U\>! | [applyToEither](CompletionStage.md))`(`other:` ` [CompletionStage](CompletionStage.md)<out` `T>!`, `fn:` ` [Function](../java.util.function/Function.md)<in` `T,` `U>!`)` Returns a new CompletionStage that, when either this or the other given stage complete normally, is executed with the corresponding result as argument to the supplied function. |
| abstract [CompletionStage](CompletionStage.md)\<U\>! | [applyToEitherAsync](CompletionStage.md))`(`other:` ` [CompletionStage](CompletionStage.md)<out` `T>!`, `fn:` ` [Function](../java.util.function/Function.md)<in` `T,` `U>!`)` Returns a new CompletionStage that, when either this or the other given stage complete normally, is executed using this stage's default asynchronous execution facility, with the corresponding result as argument to the supplied function. |
| abstract [CompletionStage](CompletionStage.md)\<U\>! | [applyToEitherAsync](CompletionStage.md))`(`other:` ` [CompletionStage](CompletionStage.md)<out` `T>!`, `fn:` ` [Function](../java.util.function/Function.md)<in` `T,` `U>!`, `executor:` ` [Executor](Executor.md)!`)` Returns a new CompletionStage that, when either this or the other given stage complete normally, is executed using the supplied executor, with the corresponding result as argument to the supplied function. |
| --- | --- |
| abstract [CompletionStage](CompletionStage.md)\<T\>! | [exceptionally](CompletionStage.md))`(`fn:` ` [Function](../java.util.function/Function.md)< [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!,` `out` `T>!`)` Returns a new CompletionStage that, when this stage completes exceptionally, is executed with this stage's exception as the argument to the supplied function. |
| open [CompletionStage](CompletionStage.md)\<T\>! | [exceptionallyAsync](CompletionStage.md))`(`fn:` ` [Function](../java.util.function/Function.md)< [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!,` `out` `T>!`)` Returns a new CompletionStage that, when this stage completes exceptionally, is executed with this stage's exception as the argument to the supplied function, using this stage's default asynchronous execution facility. |
| open [CompletionStage](CompletionStage.md)\<T\>! | [exceptionallyAsync](CompletionStage.md))`(`fn:` ` [Function](../java.util.function/Function.md)< [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!,` `out` `T>!`, `executor:` ` [Executor](Executor.md)!`)` Returns a new CompletionStage that, when this stage completes exceptionally, is executed with this stage's exception as the argument to the supplied function, using the supplied Executor. |
| --- | --- |
| open [CompletionStage](CompletionStage.md)\<T\>! | [exceptionallyCompose](CompletionStage.md))`(`fn:` ` [Function](../java.util.function/Function.md)< [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!,` `out` ` [CompletionStage](CompletionStage.md)<T>!>!`)` Returns a new CompletionStage that, when this stage completes exceptionally, is composed using the results of the supplied function applied to this stage's exception. |
| open [CompletionStage](CompletionStage.md)\<T\>! | [exceptionallyComposeAsync](CompletionStage.md))`(`fn:` ` [Function](../java.util.function/Function.md)< [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!,` `out` ` [CompletionStage](CompletionStage.md)<T>!>!`)` Returns a new CompletionStage that, when this stage completes exceptionally, is composed using the results of the supplied function applied to this stage's exception, using this stage's default asynchronous execution facility. |
| open [CompletionStage](CompletionStage.md)\<T\>! | [exceptionallyComposeAsync](CompletionStage.md))`(`fn:` ` [Function](../java.util.function/Function.md)< [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!,` `out` ` [CompletionStage](CompletionStage.md)<T>!>!`, `executor:` ` [Executor](Executor.md)!`)` Returns a new CompletionStage that, when this stage completes exceptionally, is composed using the results of the supplied function applied to this stage's exception, using the supplied Executor. |
| --- | --- |
| abstract [CompletionStage](CompletionStage.md)\<U\>! | [handle](CompletionStage.md))`(`fn:` ` [BiFunction](../java.util.function/BiFunction.md)<in` `T,` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!,` `out` `U>!`)` Returns a new CompletionStage that, when this stage completes either normally or exceptionally, is executed with this stage's result and exception as arguments to the supplied function. |
| abstract [CompletionStage](CompletionStage.md)\<U\>! | [handleAsync](CompletionStage.md))`(`fn:` ` [BiFunction](../java.util.function/BiFunction.md)<in` `T,` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!,` `out` `U>!`)` Returns a new CompletionStage that, when this stage completes either normally or exceptionally, is executed using this stage's default asynchronous execution facility, with this stage's result and exception as arguments to the supplied function. |
| abstract [CompletionStage](CompletionStage.md)\<U\>! | [handleAsync](CompletionStage.md))`(`fn:` ` [BiFunction](../java.util.function/BiFunction.md)<in` `T,` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!,` `out` `U>!`, `executor:` ` [Executor](Executor.md)!`)` Returns a new CompletionStage that, when this stage completes either normally or exceptionally, is executed using the supplied executor, with this stage's result and exception as arguments to the supplied function. |
| --- | --- |
| abstract [CompletionStage](CompletionStage.md)\< [Void](../java.lang/Void.md)!\>! | [runAfterBoth](CompletionStage.md))`(`other:` ` [CompletionStage](CompletionStage.md)<*>!`, `action:` ` [Runnable](../java.lang/Runnable.md)!`)` Returns a new CompletionStage that, when this and the other given stage both complete normally, executes the given action. |
| abstract [CompletionStage](CompletionStage.md)\< [Void](../java.lang/Void.md)!\>! | [runAfterBothAsync](CompletionStage.md))`(`other:` ` [CompletionStage](CompletionStage.md)<*>!`, `action:` ` [Runnable](../java.lang/Runnable.md)!`)` Returns a new CompletionStage that, when this and the other given stage both complete normally, executes the given action using this stage's default asynchronous execution facility. |
| abstract [CompletionStage](CompletionStage.md)\< [Void](../java.lang/Void.md)!\>! | [runAfterBothAsync](CompletionStage.md))`(`other:` ` [CompletionStage](CompletionStage.md)<*>!`, `action:` ` [Runnable](../java.lang/Runnable.md)!`, `executor:` ` [Executor](Executor.md)!`)` Returns a new CompletionStage that, when this and the other given stage both complete normally, executes the given action using the supplied executor. |
| --- | --- |
| abstract [CompletionStage](CompletionStage.md)\< [Void](../java.lang/Void.md)!\>! | [runAfterEither](CompletionStage.md))`(`other:` ` [CompletionStage](CompletionStage.md)<*>!`, `action:` ` [Runnable](../java.lang/Runnable.md)!`)` Returns a new CompletionStage that, when either this or the other given stage complete normally, executes the given action. |
| abstract [CompletionStage](CompletionStage.md)\< [Void](../java.lang/Void.md)!\>! | [runAfterEitherAsync](CompletionStage.md))`(`other:` ` [CompletionStage](CompletionStage.md)<*>!`, `action:` ` [Runnable](../java.lang/Runnable.md)!`)` Returns a new CompletionStage that, when either this or the other given stage complete normally, executes the given action using this stage's default asynchronous execution facility. |
| abstract [CompletionStage](CompletionStage.md)\< [Void](../java.lang/Void.md)!\>! | [runAfterEitherAsync](CompletionStage.md))`(`other:` ` [CompletionStage](CompletionStage.md)<*>!`, `action:` ` [Runnable](../java.lang/Runnable.md)!`, `executor:` ` [Executor](Executor.md)!`)` Returns a new CompletionStage that, when either this or the other given stage complete normally, executes the given action using the supplied executor. |
| --- | --- |
| abstract [CompletionStage](CompletionStage.md)\< [Void](../java.lang/Void.md)!\>! | [thenAccept](CompletionStage.md))`(`action:` ` [Consumer](../java.util.function/Consumer.md)<in` `T>!`)` Returns a new CompletionStage that, when this stage completes normally, is executed with this stage's result as the argument to the supplied action. |
| abstract [CompletionStage](CompletionStage.md)\< [Void](../java.lang/Void.md)!\>! | [thenAcceptAsync](CompletionStage.md))`(`action:` ` [Consumer](../java.util.function/Consumer.md)<in` `T>!`)` Returns a new CompletionStage that, when this stage completes normally, is executed using this stage's default asynchronous execution facility, with this stage's result as the argument to the supplied action. |
| abstract [CompletionStage](CompletionStage.md)\< [Void](../java.lang/Void.md)!\>! | [thenAcceptAsync](CompletionStage.md))`(`action:` ` [Consumer](../java.util.function/Consumer.md)<in` `T>!`, `executor:` ` [Executor](Executor.md)!`)` Returns a new CompletionStage that, when this stage completes normally, is executed using the supplied Executor, with this stage's result as the argument to the supplied action. |
| --- | --- |
| abstract [CompletionStage](CompletionStage.md)\< [Void](../java.lang/Void.md)!\>! | [thenAcceptBoth](CompletionStage.md))`(`other:` ` [CompletionStage](CompletionStage.md)<out` `U>!`, `action:` ` [BiConsumer](../java.util.function/BiConsumer.md)<in` `T,` `in` `U>!`)` Returns a new CompletionStage that, when this and the other given stage both complete normally, is executed with the two results as arguments to the supplied action. |
| abstract [CompletionStage](CompletionStage.md)\< [Void](../java.lang/Void.md)!\>! | [thenAcceptBothAsync](CompletionStage.md))`(`other:` ` [CompletionStage](CompletionStage.md)<out` `U>!`, `action:` ` [BiConsumer](../java.util.function/BiConsumer.md)<in` `T,` `in` `U>!`)` Returns a new CompletionStage that, when this and the other given stage both complete normally, is executed using this stage's default asynchronous execution facility, with the two results as arguments to the supplied action. |
| abstract [CompletionStage](CompletionStage.md)\< [Void](../java.lang/Void.md)!\>! | [thenAcceptBothAsync](CompletionStage.md))`(`other:` ` [CompletionStage](CompletionStage.md)<out` `U>!`, `action:` ` [BiConsumer](../java.util.function/BiConsumer.md)<in` `T,` `in` `U>!`, `executor:` ` [Executor](Executor.md)!`)` Returns a new CompletionStage that, when this and the other given stage both complete normally, is executed using the supplied executor, with the two results as arguments to the supplied action. |
| --- | --- |
| abstract [CompletionStage](CompletionStage.md)\<U\>! | [thenApply](CompletionStage.md))`(`fn:` ` [Function](../java.util.function/Function.md)<in` `T,` `out` `U>!`)` Returns a new CompletionStage that, when this stage completes normally, is executed with this stage's result as the argument to the supplied function. |
| abstract [CompletionStage](CompletionStage.md)\<U\>! | [thenApplyAsync](CompletionStage.md))`(`fn:` ` [Function](../java.util.function/Function.md)<in` `T,` `out` `U>!`)` Returns a new CompletionStage that, when this stage completes normally, is executed using this stage's default asynchronous execution facility, with this stage's result as the argument to the supplied function. |
| abstract [CompletionStage](CompletionStage.md)\<U\>! | [thenApplyAsync](CompletionStage.md))`(`fn:` ` [Function](../java.util.function/Function.md)<in` `T,` `out` `U>!`, `executor:` ` [Executor](Executor.md)!`)` Returns a new CompletionStage that, when this stage completes normally, is executed using the supplied Executor, with this stage's result as the argument to the supplied function. |
| --- | --- |
| abstract [CompletionStage](CompletionStage.md)\<V\>! | [thenCombine](CompletionStage.md))`(`other:` ` [CompletionStage](CompletionStage.md)<out` `U>!`, `fn:` ` [BiFunction](../java.util.function/BiFunction.md)<in` `T,` `in` `U,` `out` `V>!`)` Returns a new CompletionStage that, when this and the other given stage both complete normally, is executed with the two results as arguments to the supplied function. |
| abstract [CompletionStage](CompletionStage.md)\<V\>! | [thenCombineAsync](CompletionStage.md))`(`other:` ` [CompletionStage](CompletionStage.md)<out` `U>!`, `fn:` ` [BiFunction](../java.util.function/BiFunction.md)<in` `T,` `in` `U,` `out` `V>!`)` Returns a new CompletionStage that, when this and the other given stage both complete normally, is executed using this stage's default asynchronous execution facility, with the two results as arguments to the supplied function. |
| abstract [CompletionStage](CompletionStage.md)\<V\>! | [thenCombineAsync](CompletionStage.md))`(`other:` ` [CompletionStage](CompletionStage.md)<out` `U>!`, `fn:` ` [BiFunction](../java.util.function/BiFunction.md)<in` `T,` `in` `U,` `out` `V>!`, `executor:` ` [Executor](Executor.md)!`)` Returns a new CompletionStage that, when this and the other given stage both complete normally, is executed using the supplied executor, with the two results as arguments to the supplied function. |
| --- | --- |
| abstract [CompletionStage](CompletionStage.md)\<U\>! | [thenCompose](CompletionStage.md))`(`fn:` ` [Function](../java.util.function/Function.md)<in` `T,` `out` ` [CompletionStage](CompletionStage.md)<U>!>!`)` Returns a new CompletionStage that is completed with the same value as the CompletionStage returned by the given function. |
| abstract [CompletionStage](CompletionStage.md)\<U\>! | [thenComposeAsync](CompletionStage.md))`(`fn:` ` [Function](../java.util.function/Function.md)<in` `T,` `out` ` [CompletionStage](CompletionStage.md)<U>!>!`)` Returns a new CompletionStage that is completed with the same value as the CompletionStage returned by the given function, executed using this stage's default asynchronous execution facility. |
| abstract [CompletionStage](CompletionStage.md)\<U\>! | [thenComposeAsync](CompletionStage.md))`(`fn:` ` [Function](../java.util.function/Function.md)<in` `T,` `out` ` [CompletionStage](CompletionStage.md)<U>!>!`, `executor:` ` [Executor](Executor.md)!`)` Returns a new CompletionStage that is completed with the same value as the CompletionStage returned by the given function, executed using the supplied Executor. |
| --- | --- |
| abstract [CompletionStage](CompletionStage.md)\< [Void](../java.lang/Void.md)!\>! | [thenRun](CompletionStage.md))`(`action:` ` [Runnable](../java.lang/Runnable.md)!`)` Returns a new CompletionStage that, when this stage completes normally, executes the given action. |
| abstract [CompletionStage](CompletionStage.md)\< [Void](../java.lang/Void.md)!\>! | [thenRunAsync](CompletionStage.md))`(`action:` ` [Runnable](../java.lang/Runnable.md)!`)` Returns a new CompletionStage that, when this stage completes normally, executes the given action using this stage's default asynchronous execution facility. |
| abstract [CompletionStage](CompletionStage.md)\< [Void](../java.lang/Void.md)!\>! | [thenRunAsync](CompletionStage.md))`(`action:` ` [Runnable](../java.lang/Runnable.md)!`, `executor:` ` [Executor](Executor.md)!`)` Returns a new CompletionStage that, when this stage completes normally, executes the given action using the supplied Executor. |
| --- | --- |
| abstract [CompletableFuture](CompletableFuture.md)\<T\>! | [toCompletableFuture](CompletionStage.md))`()` Returns a [CompletableFuture](CompletableFuture.md) maintaining the same completion properties as this stage. |
| abstract [CompletionStage](CompletionStage.md)\<T\>! | [whenComplete](CompletionStage.md))`(`action:` ` [BiConsumer](../java.util.function/BiConsumer.md)<in` `T,` `in` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!>!`)` Returns a new CompletionStage with the same result or exception as this stage, that executes the given action when this stage completes. |
| abstract [CompletionStage](CompletionStage.md)\<T\>! | [whenCompleteAsync](CompletionStage.md))`(`action:` ` [BiConsumer](../java.util.function/BiConsumer.md)<in` `T,` `in` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!>!`)` Returns a new CompletionStage with the same result or exception as this stage, that executes the given action using this stage's default asynchronous execution facility when this stage completes. |
| --- | --- |
| abstract [CompletionStage](CompletionStage.md)\<T\>! | [whenCompleteAsync](CompletionStage.md))`(`action:` ` [BiConsumer](../java.util.function/BiConsumer.md)<in` `T,` `in` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!>!`, `executor:` ` [Executor](Executor.md)!`)` Returns a new CompletionStage with the same result or exception as this stage, that executes the given action using the supplied Executor when this stage completes. |

## Public methods

### acceptEither

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun acceptEither(
    other: CompletionStage<out T>!, 
    action: Consumer<in T>!
): CompletionStage<Void!>!
```

Returns a new CompletionStage that, when either this or the other given stage complete normally, is executed with the corresponding result as argument to the supplied action. See the [CompletionStage](CompletionStage.md) documentation for rules covering exceptional completion.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `other` | [CompletionStage](CompletionStage.md)\<outT\>!:the other CompletionStage |
| `action` | [Consumer](../java.util.function/Consumer.md)\<inT\>!:the action to perform before completing the returned CompletionStage |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| [CompletionStage](CompletionStage.md)< [Void](../java.lang/Void.md)!>! | the new CompletionStage |

### acceptEitherAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun acceptEitherAsync(
    other: CompletionStage<out T>!, 
    action: Consumer<in T>!
): CompletionStage<Void!>!
```

Returns a new CompletionStage that, when either this or the other given stage complete normally, is executed using this stage's default asynchronous execution facility, with the corresponding result as argument to the supplied action. See the [CompletionStage](CompletionStage.md) documentation for rules covering exceptional completion.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `other` | [CompletionStage](CompletionStage.md)\<outT\>!:the other CompletionStage |
| `action` | [Consumer](../java.util.function/Consumer.md)\<inT\>!:the action to perform before completing the returned CompletionStage |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| [CompletionStage](CompletionStage.md)< [Void](../java.lang/Void.md)!>! | the new CompletionStage |

### acceptEitherAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun acceptEitherAsync(
    other: CompletionStage<out T>!, 
    action: Consumer<in T>!, 
    executor: Executor!
): CompletionStage<Void!>!
```

Returns a new CompletionStage that, when either this or the other given stage complete normally, is executed using the supplied executor, with the corresponding result as argument to the supplied action. See the [CompletionStage](CompletionStage.md) documentation for rules covering exceptional completion.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `other` | [CompletionStage](CompletionStage.md)\<outT\>!:the other CompletionStage |
| `action` | [Consumer](../java.util.function/Consumer.md)\<inT\>!:the action to perform before completing the returned CompletionStage |
| `executor` | [Executor](Executor.md)!:the executor to use for asynchronous execution |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| [CompletionStage](CompletionStage.md)< [Void](../java.lang/Void.md)!>! | the new CompletionStage |

### applyToEither

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <U : Any!> applyToEither(
    other: CompletionStage<out T>!, 
    fn: Function<in T, U>!
): CompletionStage<U>!
```

Returns a new CompletionStage that, when either this or the other given stage complete normally, is executed with the corresponding result as argument to the supplied function. See the [CompletionStage](CompletionStage.md) documentation for rules covering exceptional completion.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `other` | [CompletionStage](CompletionStage.md)\<outT\>!:the other CompletionStage |
| `fn` | [Function](../java.util.function/Function.md)\<inT,U\>!:the function to use to compute the value of the returned CompletionStage |
| `<U>` | the function's return type |
| --- | --- |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-------------------------|
| [CompletionStage](CompletionStage.md)<U>! | the new CompletionStage |

### applyToEitherAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <U : Any!> applyToEitherAsync(
    other: CompletionStage<out T>!, 
    fn: Function<in T, U>!
): CompletionStage<U>!
```

Returns a new CompletionStage that, when either this or the other given stage complete normally, is executed using this stage's default asynchronous execution facility, with the corresponding result as argument to the supplied function. See the [CompletionStage](CompletionStage.md) documentation for rules covering exceptional completion.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `other` | [CompletionStage](CompletionStage.md)\<outT\>!:the other CompletionStage |
| `fn` | [Function](../java.util.function/Function.md)\<inT,U\>!:the function to use to compute the value of the returned CompletionStage |
| `<U>` | the function's return type |
| --- | --- |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-------------------------|
| [CompletionStage](CompletionStage.md)<U>! | the new CompletionStage |

### applyToEitherAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <U : Any!> applyToEitherAsync(
    other: CompletionStage<out T>!, 
    fn: Function<in T, U>!, 
    executor: Executor!
): CompletionStage<U>!
```

Returns a new CompletionStage that, when either this or the other given stage complete normally, is executed using the supplied executor, with the corresponding result as argument to the supplied function. See the [CompletionStage](CompletionStage.md) documentation for rules covering exceptional completion.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `other` | [CompletionStage](CompletionStage.md)\<outT\>!:the other CompletionStage |
| `fn` | [Function](../java.util.function/Function.md)\<inT,U\>!:the function to use to compute the value of the returned CompletionStage |
| `executor` | [Executor](Executor.md)!:the executor to use for asynchronous execution |
| --- | --- |
| `<U>` | the function's return type |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-------------------------|
| [CompletionStage](CompletionStage.md)<U>! | the new CompletionStage |

### exceptionally

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun exceptionally(fn: Function<Throwable!, out T>!): CompletionStage<T>!
```

Returns a new CompletionStage that, when this stage completes exceptionally, is executed with this stage's exception as the argument to the supplied function. Otherwise, if this stage completes normally, then the returned stage also completes normally with the same value.

| Parameters ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fn` | [Function](../java.util.function/Function.md)\< [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!,outT\>!:the function to use to compute the value of the returned CompletionStage if this CompletionStage completed exceptionally |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-------------------------|
| [CompletionStage](CompletionStage.md)<T>! | the new CompletionStage |

### exceptionallyAsync

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun exceptionallyAsync(fn: Function<Throwable!, out T>!): CompletionStage<T>!
```

Returns a new CompletionStage that, when this stage completes exceptionally, is executed with this stage's exception as the argument to the supplied function, using this stage's default asynchronous execution facility. Otherwise, if this stage completes normally, then the returned stage also completes normally with the same value.

| Parameters ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fn` | [Function](../java.util.function/Function.md)\< [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!,outT\>!:the function to use to compute the value of the returned CompletionStage if this CompletionStage completed exceptionally |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-------------------------|
| [CompletionStage](CompletionStage.md)<T>! | the new CompletionStage |

### exceptionallyAsync

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun exceptionallyAsync(
    fn: Function<Throwable!, out T>!, 
    executor: Executor!
): CompletionStage<T>!
```

Returns a new CompletionStage that, when this stage completes exceptionally, is executed with this stage's exception as the argument to the supplied function, using the supplied Executor. Otherwise, if this stage completes normally, then the returned stage also completes normally with the same value.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fn` | [Function](../java.util.function/Function.md)\< [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!,outT\>!:the function to use to compute the value of the returned CompletionStage if this CompletionStage completed exceptionally |
| `executor` | [Executor](Executor.md)!:the executor to use for asynchronous execution |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-------------------------|
| [CompletionStage](CompletionStage.md)<T>! | the new CompletionStage |

### exceptionallyCompose

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun exceptionallyCompose(fn: Function<Throwable!, out CompletionStage<T>!>!): CompletionStage<T>!
```

Returns a new CompletionStage that, when this stage completes exceptionally, is composed using the results of the supplied function applied to this stage's exception.

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fn` | [Function](../java.util.function/Function.md)\< [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!,out [CompletionStage](CompletionStage.md)\<T\>!\>!:the function to use to compute the returned CompletionStage if this CompletionStage completed exceptionally |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-------------------------|
| [CompletionStage](CompletionStage.md)<T>! | the new CompletionStage |

### exceptionallyComposeAsync

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun exceptionallyComposeAsync(fn: Function<Throwable!, out CompletionStage<T>!>!): CompletionStage<T>!
```

Returns a new CompletionStage that, when this stage completes exceptionally, is composed using the results of the supplied function applied to this stage's exception, using this stage's default asynchronous execution facility.

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fn` | [Function](../java.util.function/Function.md)\< [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!,out [CompletionStage](CompletionStage.md)\<T\>!\>!:the function to use to compute the returned CompletionStage if this CompletionStage completed exceptionally |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-------------------------|
| [CompletionStage](CompletionStage.md)<T>! | the new CompletionStage |

### exceptionallyComposeAsync

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun exceptionallyComposeAsync(
    fn: Function<Throwable!, out CompletionStage<T>!>!, 
    executor: Executor!
): CompletionStage<T>!
```

Returns a new CompletionStage that, when this stage completes exceptionally, is composed using the results of the supplied function applied to this stage's exception, using the supplied Executor.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fn` | [Function](../java.util.function/Function.md)\< [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!,out [CompletionStage](CompletionStage.md)\<T\>!\>!:the function to use to compute the returned CompletionStage if this CompletionStage completed exceptionally |
| `executor` | [Executor](Executor.md)!:the executor to use for asynchronous execution |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-------------------------|
| [CompletionStage](CompletionStage.md)<T>! | the new CompletionStage |

### handle

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <U : Any!> handle(fn: BiFunction<in T, Throwable!, out U>!): CompletionStage<U>!
```

Returns a new CompletionStage that, when this stage completes either normally or exceptionally, is executed with this stage's result and exception as arguments to the supplied function.

When this stage is complete, the given function is invoked with the result (or`null`if none) and the exception (or`null`if none) of this stage as arguments, and the function's result is used to complete the returned stage.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fn` | [BiFunction](../java.util.function/BiFunction.md)\<inT, [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!,outU\>!:the function to use to compute the value of the returned CompletionStage |
| `<U>` | the function's return type |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-------------------------|
| [CompletionStage](CompletionStage.md)<U>! | the new CompletionStage |

### handleAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <U : Any!> handleAsync(fn: BiFunction<in T, Throwable!, out U>!): CompletionStage<U>!
```

Returns a new CompletionStage that, when this stage completes either normally or exceptionally, is executed using this stage's default asynchronous execution facility, with this stage's result and exception as arguments to the supplied function.

When this stage is complete, the given function is invoked with the result (or`null`if none) and the exception (or`null`if none) of this stage as arguments, and the function's result is used to complete the returned stage.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fn` | [BiFunction](../java.util.function/BiFunction.md)\<inT, [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!,outU\>!:the function to use to compute the value of the returned CompletionStage |
| `<U>` | the function's return type |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-------------------------|
| [CompletionStage](CompletionStage.md)<U>! | the new CompletionStage |

### handleAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <U : Any!> handleAsync(
    fn: BiFunction<in T, Throwable!, out U>!, 
    executor: Executor!
): CompletionStage<U>!
```

Returns a new CompletionStage that, when this stage completes either normally or exceptionally, is executed using the supplied executor, with this stage's result and exception as arguments to the supplied function.

When this stage is complete, the given function is invoked with the result (or`null`if none) and the exception (or`null`if none) of this stage as arguments, and the function's result is used to complete the returned stage.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fn` | [BiFunction](../java.util.function/BiFunction.md)\<inT, [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!,outU\>!:the function to use to compute the value of the returned CompletionStage |
| `executor` | [Executor](Executor.md)!:the executor to use for asynchronous execution |
| `<U>` | the function's return type |
| --- | --- |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-------------------------|
| [CompletionStage](CompletionStage.md)<U>! | the new CompletionStage |

### runAfterBoth

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun runAfterBoth(
    other: CompletionStage<*>!, 
    action: Runnable!
): CompletionStage<Void!>!
```

Returns a new CompletionStage that, when this and the other given stage both complete normally, executes the given action. See the [CompletionStage](CompletionStage.md) documentation for rules covering exceptional completion.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `other` | [CompletionStage](CompletionStage.md)\<\*\>!:the other CompletionStage |
| `action` | [Runnable](../java.lang/Runnable.md)!:the action to perform before completing the returned CompletionStage |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| [CompletionStage](CompletionStage.md)< [Void](../java.lang/Void.md)!>! | the new CompletionStage |

### runAfterBothAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun runAfterBothAsync(
    other: CompletionStage<*>!, 
    action: Runnable!
): CompletionStage<Void!>!
```

Returns a new CompletionStage that, when this and the other given stage both complete normally, executes the given action using this stage's default asynchronous execution facility. See the [CompletionStage](CompletionStage.md) documentation for rules covering exceptional completion.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `other` | [CompletionStage](CompletionStage.md)\<\*\>!:the other CompletionStage |
| `action` | [Runnable](../java.lang/Runnable.md)!:the action to perform before completing the returned CompletionStage |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| [CompletionStage](CompletionStage.md)< [Void](../java.lang/Void.md)!>! | the new CompletionStage |

### runAfterBothAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun runAfterBothAsync(
    other: CompletionStage<*>!, 
    action: Runnable!, 
    executor: Executor!
): CompletionStage<Void!>!
```

Returns a new CompletionStage that, when this and the other given stage both complete normally, executes the given action using the supplied executor. See the [CompletionStage](CompletionStage.md) documentation for rules covering exceptional completion.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `other` | [CompletionStage](CompletionStage.md)\<\*\>!:the other CompletionStage |
| `action` | [Runnable](../java.lang/Runnable.md)!:the action to perform before completing the returned CompletionStage |
| `executor` | [Executor](Executor.md)!:the executor to use for asynchronous execution |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| [CompletionStage](CompletionStage.md)< [Void](../java.lang/Void.md)!>! | the new CompletionStage |

### runAfterEither

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun runAfterEither(
    other: CompletionStage<*>!, 
    action: Runnable!
): CompletionStage<Void!>!
```

Returns a new CompletionStage that, when either this or the other given stage complete normally, executes the given action. See the [CompletionStage](CompletionStage.md) documentation for rules covering exceptional completion.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `other` | [CompletionStage](CompletionStage.md)\<\*\>!:the other CompletionStage |
| `action` | [Runnable](../java.lang/Runnable.md)!:the action to perform before completing the returned CompletionStage |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| [CompletionStage](CompletionStage.md)< [Void](../java.lang/Void.md)!>! | the new CompletionStage |

### runAfterEitherAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun runAfterEitherAsync(
    other: CompletionStage<*>!, 
    action: Runnable!
): CompletionStage<Void!>!
```

Returns a new CompletionStage that, when either this or the other given stage complete normally, executes the given action using this stage's default asynchronous execution facility. See the [CompletionStage](CompletionStage.md) documentation for rules covering exceptional completion.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `other` | [CompletionStage](CompletionStage.md)\<\*\>!:the other CompletionStage |
| `action` | [Runnable](../java.lang/Runnable.md)!:the action to perform before completing the returned CompletionStage |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| [CompletionStage](CompletionStage.md)< [Void](../java.lang/Void.md)!>! | the new CompletionStage |

### runAfterEitherAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun runAfterEitherAsync(
    other: CompletionStage<*>!, 
    action: Runnable!, 
    executor: Executor!
): CompletionStage<Void!>!
```

Returns a new CompletionStage that, when either this or the other given stage complete normally, executes the given action using the supplied executor. See the [CompletionStage](CompletionStage.md) documentation for rules covering exceptional completion.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `other` | [CompletionStage](CompletionStage.md)\<\*\>!:the other CompletionStage |
| `action` | [Runnable](../java.lang/Runnable.md)!:the action to perform before completing the returned CompletionStage |
| `executor` | [Executor](Executor.md)!:the executor to use for asynchronous execution |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| [CompletionStage](CompletionStage.md)< [Void](../java.lang/Void.md)!>! | the new CompletionStage |

### thenAccept

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun thenAccept(action: Consumer<in T>!): CompletionStage<Void!>!
```

Returns a new CompletionStage that, when this stage completes normally, is executed with this stage's result as the argument to the supplied action. See the [CompletionStage](CompletionStage.md) documentation for rules covering exceptional completion.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [Consumer](../java.util.function/Consumer.md)\<inT\>!:the action to perform before completing the returned CompletionStage |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| [CompletionStage](CompletionStage.md)< [Void](../java.lang/Void.md)!>! | the new CompletionStage |

### thenAcceptAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun thenAcceptAsync(action: Consumer<in T>!): CompletionStage<Void!>!
```

Returns a new CompletionStage that, when this stage completes normally, is executed using this stage's default asynchronous execution facility, with this stage's result as the argument to the supplied action. See the [CompletionStage](CompletionStage.md) documentation for rules covering exceptional completion.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [Consumer](../java.util.function/Consumer.md)\<inT\>!:the action to perform before completing the returned CompletionStage |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| [CompletionStage](CompletionStage.md)< [Void](../java.lang/Void.md)!>! | the new CompletionStage |

### thenAcceptAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun thenAcceptAsync(
    action: Consumer<in T>!, 
    executor: Executor!
): CompletionStage<Void!>!
```

Returns a new CompletionStage that, when this stage completes normally, is executed using the supplied Executor, with this stage's result as the argument to the supplied action. See the [CompletionStage](CompletionStage.md) documentation for rules covering exceptional completion.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [Consumer](../java.util.function/Consumer.md)\<inT\>!:the action to perform before completing the returned CompletionStage |
| `executor` | [Executor](Executor.md)!:the executor to use for asynchronous execution |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| [CompletionStage](CompletionStage.md)< [Void](../java.lang/Void.md)!>! | the new CompletionStage |

### thenAcceptBoth

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <U : Any!> thenAcceptBoth(
    other: CompletionStage<out U>!, 
    action: BiConsumer<in T, in U>!
): CompletionStage<Void!>!
```

Returns a new CompletionStage that, when this and the other given stage both complete normally, is executed with the two results as arguments to the supplied action. See the [CompletionStage](CompletionStage.md) documentation for rules covering exceptional completion.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `other` | [CompletionStage](CompletionStage.md)\<outU\>!:the other CompletionStage |
| `action` | [BiConsumer](../java.util.function/BiConsumer.md)\<inT,inU\>!:the action to perform before completing the returned CompletionStage |
| `<U>` | the type of the other CompletionStage's result |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| [CompletionStage](CompletionStage.md)< [Void](../java.lang/Void.md)!>! | the new CompletionStage |

### thenAcceptBothAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <U : Any!> thenAcceptBothAsync(
    other: CompletionStage<out U>!, 
    action: BiConsumer<in T, in U>!
): CompletionStage<Void!>!
```

Returns a new CompletionStage that, when this and the other given stage both complete normally, is executed using this stage's default asynchronous execution facility, with the two results as arguments to the supplied action. See the [CompletionStage](CompletionStage.md) documentation for rules covering exceptional completion.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `other` | [CompletionStage](CompletionStage.md)\<outU\>!:the other CompletionStage |
| `action` | [BiConsumer](../java.util.function/BiConsumer.md)\<inT,inU\>!:the action to perform before completing the returned CompletionStage |
| `<U>` | the type of the other CompletionStage's result |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| [CompletionStage](CompletionStage.md)< [Void](../java.lang/Void.md)!>! | the new CompletionStage |

### thenAcceptBothAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <U : Any!> thenAcceptBothAsync(
    other: CompletionStage<out U>!, 
    action: BiConsumer<in T, in U>!, 
    executor: Executor!
): CompletionStage<Void!>!
```

Returns a new CompletionStage that, when this and the other given stage both complete normally, is executed using the supplied executor, with the two results as arguments to the supplied action. See the [CompletionStage](CompletionStage.md) documentation for rules covering exceptional completion.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `other` | [CompletionStage](CompletionStage.md)\<outU\>!:the other CompletionStage |
| `action` | [BiConsumer](../java.util.function/BiConsumer.md)\<inT,inU\>!:the action to perform before completing the returned CompletionStage |
| `executor` | [Executor](Executor.md)!:the executor to use for asynchronous execution |
| --- | --- |
| `<U>` | the type of the other CompletionStage's result |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| [CompletionStage](CompletionStage.md)< [Void](../java.lang/Void.md)!>! | the new CompletionStage |

### thenApply

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <U : Any!> thenApply(fn: Function<in T, out U>!): CompletionStage<U>!
```

Returns a new CompletionStage that, when this stage completes normally, is executed with this stage's result as the argument to the supplied function.

This method is analogous to [Optional.map](../java.util/Optional.md))and [Stream.map](../java.util.stream/Stream.md)).

See the [CompletionStage](CompletionStage.md) documentation for rules covering exceptional completion.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fn` | [Function](../java.util.function/Function.md)\<inT,outU\>!:the function to use to compute the value of the returned CompletionStage |
| `<U>` | the function's return type |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-------------------------|
| [CompletionStage](CompletionStage.md)<U>! | the new CompletionStage |

### thenApplyAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <U : Any!> thenApplyAsync(fn: Function<in T, out U>!): CompletionStage<U>!
```

Returns a new CompletionStage that, when this stage completes normally, is executed using this stage's default asynchronous execution facility, with this stage's result as the argument to the supplied function. See the [CompletionStage](CompletionStage.md) documentation for rules covering exceptional completion.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fn` | [Function](../java.util.function/Function.md)\<inT,outU\>!:the function to use to compute the value of the returned CompletionStage |
| `<U>` | the function's return type |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-------------------------|
| [CompletionStage](CompletionStage.md)<U>! | the new CompletionStage |

### thenApplyAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <U : Any!> thenApplyAsync(
    fn: Function<in T, out U>!, 
    executor: Executor!
): CompletionStage<U>!
```

Returns a new CompletionStage that, when this stage completes normally, is executed using the supplied Executor, with this stage's result as the argument to the supplied function. See the [CompletionStage](CompletionStage.md) documentation for rules covering exceptional completion.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fn` | [Function](../java.util.function/Function.md)\<inT,outU\>!:the function to use to compute the value of the returned CompletionStage |
| `executor` | [Executor](Executor.md)!:the executor to use for asynchronous execution |
| `<U>` | the function's return type |
| --- | --- |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-------------------------|
| [CompletionStage](CompletionStage.md)<U>! | the new CompletionStage |

### thenCombine

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <U : Any!, V : Any!> thenCombine(
    other: CompletionStage<out U>!, 
    fn: BiFunction<in T, in U, out V>!
): CompletionStage<V>!
```

Returns a new CompletionStage that, when this and the other given stage both complete normally, is executed with the two results as arguments to the supplied function. See the [CompletionStage](CompletionStage.md) documentation for rules covering exceptional completion.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `other` | [CompletionStage](CompletionStage.md)\<outU\>!:the other CompletionStage |
| `fn` | [BiFunction](../java.util.function/BiFunction.md)\<inT,inU,outV\>!:the function to use to compute the value of the returned CompletionStage |
| `<U>` | the type of the other CompletionStage's result |
| --- | --- |
| `<V>` | the function's return type |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-------------------------|
| [CompletionStage](CompletionStage.md)<V>! | the new CompletionStage |

### thenCombineAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <U : Any!, V : Any!> thenCombineAsync(
    other: CompletionStage<out U>!, 
    fn: BiFunction<in T, in U, out V>!
): CompletionStage<V>!
```

Returns a new CompletionStage that, when this and the other given stage both complete normally, is executed using this stage's default asynchronous execution facility, with the two results as arguments to the supplied function. See the [CompletionStage](CompletionStage.md) documentation for rules covering exceptional completion.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `other` | [CompletionStage](CompletionStage.md)\<outU\>!:the other CompletionStage |
| `fn` | [BiFunction](../java.util.function/BiFunction.md)\<inT,inU,outV\>!:the function to use to compute the value of the returned CompletionStage |
| `<U>` | the type of the other CompletionStage's result |
| --- | --- |
| `<V>` | the function's return type |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-------------------------|
| [CompletionStage](CompletionStage.md)<V>! | the new CompletionStage |

### thenCombineAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <U : Any!, V : Any!> thenCombineAsync(
    other: CompletionStage<out U>!, 
    fn: BiFunction<in T, in U, out V>!, 
    executor: Executor!
): CompletionStage<V>!
```

Returns a new CompletionStage that, when this and the other given stage both complete normally, is executed using the supplied executor, with the two results as arguments to the supplied function. See the [CompletionStage](CompletionStage.md) documentation for rules covering exceptional completion.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `other` | [CompletionStage](CompletionStage.md)\<outU\>!:the other CompletionStage |
| `fn` | [BiFunction](../java.util.function/BiFunction.md)\<inT,inU,outV\>!:the function to use to compute the value of the returned CompletionStage |
| `executor` | [Executor](Executor.md)!:the executor to use for asynchronous execution |
| --- | --- |
| `<U>` | the type of the other CompletionStage's result |
| `<V>` | the function's return type |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-------------------------|
| [CompletionStage](CompletionStage.md)<V>! | the new CompletionStage |

### thenCompose

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <U : Any!> thenCompose(fn: Function<in T, out CompletionStage<U>!>!): CompletionStage<U>!
```

Returns a new CompletionStage that is completed with the same value as the CompletionStage returned by the given function.

When this stage completes normally, the given function is invoked with this stage's result as the argument, returning another CompletionStage. When that stage completes normally, the CompletionStage returned by this method is completed with the same value.

To ensure progress, the supplied function must arrange eventual completion of its result.

This method is analogous to [Optional.flatMap](../java.util/Optional.md))and [Stream.flatMap](../java.util.stream/Stream.md)).

See the [CompletionStage](CompletionStage.md) documentation for rules covering exceptional completion.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fn` | [Function](../java.util.function/Function.md)\<inT,out [CompletionStage](CompletionStage.md)\<U\>!\>!:the function to use to compute another CompletionStage |
| `<U>` | the type of the returned CompletionStage's result |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-------------------------|
| [CompletionStage](CompletionStage.md)<U>! | the new CompletionStage |

### thenComposeAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <U : Any!> thenComposeAsync(fn: Function<in T, out CompletionStage<U>!>!): CompletionStage<U>!
```

Returns a new CompletionStage that is completed with the same value as the CompletionStage returned by the given function, executed using this stage's default asynchronous execution facility.

When this stage completes normally, the given function is invoked with this stage's result as the argument, returning another CompletionStage. When that stage completes normally, the CompletionStage returned by this method is completed with the same value.

To ensure progress, the supplied function must arrange eventual completion of its result.

See the [CompletionStage](CompletionStage.md) documentation for rules covering exceptional completion.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fn` | [Function](../java.util.function/Function.md)\<inT,out [CompletionStage](CompletionStage.md)\<U\>!\>!:the function to use to compute another CompletionStage |
| `<U>` | the type of the returned CompletionStage's result |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-------------------------|
| [CompletionStage](CompletionStage.md)<U>! | the new CompletionStage |

### thenComposeAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <U : Any!> thenComposeAsync(
    fn: Function<in T, out CompletionStage<U>!>!, 
    executor: Executor!
): CompletionStage<U>!
```

Returns a new CompletionStage that is completed with the same value as the CompletionStage returned by the given function, executed using the supplied Executor.

When this stage completes normally, the given function is invoked with this stage's result as the argument, returning another CompletionStage. When that stage completes normally, the CompletionStage returned by this method is completed with the same value.

To ensure progress, the supplied function must arrange eventual completion of its result.

See the [CompletionStage](CompletionStage.md) documentation for rules covering exceptional completion.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fn` | [Function](../java.util.function/Function.md)\<inT,out [CompletionStage](CompletionStage.md)\<U\>!\>!:the function to use to compute another CompletionStage |
| `executor` | [Executor](Executor.md)!:the executor to use for asynchronous execution |
| `<U>` | the type of the returned CompletionStage's result |
| --- | --- |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-------------------------|
| [CompletionStage](CompletionStage.md)<U>! | the new CompletionStage |

### thenRun

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun thenRun(action: Runnable!): CompletionStage<Void!>!
```

Returns a new CompletionStage that, when this stage completes normally, executes the given action. See the [CompletionStage](CompletionStage.md) documentation for rules covering exceptional completion.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [Runnable](../java.lang/Runnable.md)!:the action to perform before completing the returned CompletionStage |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| [CompletionStage](CompletionStage.md)< [Void](../java.lang/Void.md)!>! | the new CompletionStage |

### thenRunAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun thenRunAsync(action: Runnable!): CompletionStage<Void!>!
```

Returns a new CompletionStage that, when this stage completes normally, executes the given action using this stage's default asynchronous execution facility. See the [CompletionStage](CompletionStage.md) documentation for rules covering exceptional completion.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [Runnable](../java.lang/Runnable.md)!:the action to perform before completing the returned CompletionStage |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| [CompletionStage](CompletionStage.md)< [Void](../java.lang/Void.md)!>! | the new CompletionStage |

### thenRunAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun thenRunAsync(
    action: Runnable!, 
    executor: Executor!
): CompletionStage<Void!>!
```

Returns a new CompletionStage that, when this stage completes normally, executes the given action using the supplied Executor. See the [CompletionStage](CompletionStage.md) documentation for rules covering exceptional completion.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [Runnable](../java.lang/Runnable.md)!:the action to perform before completing the returned CompletionStage |
| `executor` | [Executor](Executor.md)!:the executor to use for asynchronous execution |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| [CompletionStage](CompletionStage.md)< [Void](../java.lang/Void.md)!>! | the new CompletionStage |

### toCompletableFuture

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun toCompletableFuture(): CompletableFuture<T>!
```

Returns a [CompletableFuture](CompletableFuture.md) maintaining the same completion properties as this stage. If this stage is already a CompletableFuture, this method may return this stage itself. Otherwise, invocation of this method may be equivalent in effect to`thenApply(x -> x)`, but returning an instance of type`CompletableFuture`.

| Return ||
|----------------------------------------------------------------------------------------------------------------|-----------------------|
| [CompletableFuture](CompletableFuture.md)<T>! | the CompletableFuture |

### whenComplete

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun whenComplete(action: BiConsumer<in T, in Throwable!>!): CompletionStage<T>!
```

Returns a new CompletionStage with the same result or exception as this stage, that executes the given action when this stage completes.

When this stage is complete, the given action is invoked with the result (or`null`if none) and the exception (or`null`if none) of this stage as arguments. The returned stage is completed when the action returns.

Unlike method [handle](CompletionStage.md)), this method is not designed to translate completion outcomes, so the supplied action should not throw an exception. However, if it does, the following rules apply: if this stage completed normally but the supplied action throws an exception, then the returned stage completes exceptionally with the supplied action's exception. Or, if this stage completed exceptionally and the supplied action throws an exception, then the returned stage completes exceptionally with this stage's exception.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [BiConsumer](../java.util.function/BiConsumer.md)\<inT,in [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!\>!:the action to perform |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-------------------------|
| [CompletionStage](CompletionStage.md)<T>! | the new CompletionStage |

### whenCompleteAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun whenCompleteAsync(action: BiConsumer<in T, in Throwable!>!): CompletionStage<T>!
```

Returns a new CompletionStage with the same result or exception as this stage, that executes the given action using this stage's default asynchronous execution facility when this stage completes.

When this stage is complete, the given action is invoked with the result (or`null`if none) and the exception (or`null`if none) of this stage as arguments. The returned stage is completed when the action returns.

Unlike method [handleAsync](CompletionStage.md)), this method is not designed to translate completion outcomes, so the supplied action should not throw an exception. However, if it does, the following rules apply: If this stage completed normally but the supplied action throws an exception, then the returned stage completes exceptionally with the supplied action's exception. Or, if this stage completed exceptionally and the supplied action throws an exception, then the returned stage completes exceptionally with this stage's exception.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [BiConsumer](../java.util.function/BiConsumer.md)\<inT,in [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!\>!:the action to perform |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-------------------------|
| [CompletionStage](CompletionStage.md)<T>! | the new CompletionStage |

### whenCompleteAsync

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun whenCompleteAsync(
    action: BiConsumer<in T, in Throwable!>!, 
    executor: Executor!
): CompletionStage<T>!
```

Returns a new CompletionStage with the same result or exception as this stage, that executes the given action using the supplied Executor when this stage completes.

When this stage is complete, the given action is invoked with the result (or`null`if none) and the exception (or`null`if none) of this stage as arguments. The returned stage is completed when the action returns.

Unlike method [handleAsync](CompletionStage.md)), this method is not designed to translate completion outcomes, so the supplied action should not throw an exception. However, if it does, the following rules apply: If this stage completed normally but the supplied action throws an exception, then the returned stage completes exceptionally with the supplied action's exception. Or, if this stage completed exceptionally and the supplied action throws an exception, then the returned stage completes exceptionally with this stage's exception.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [BiConsumer](../java.util.function/BiConsumer.md)\<inT,in [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!\>!:the action to perform |
| `executor` | [Executor](Executor.md)!:the executor to use for asynchronous execution |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-------------------------|
| [CompletionStage](CompletionStage.md)<T>! | the new CompletionStage |
