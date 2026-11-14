# BiFunction

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BiFunction

```
@FunctionalInterface interface BiFunction<T : Any!, U : Any!, R : Any!>
```

| [java.util.function.BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction#) |

| Known Direct Subclasses [BinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator) |----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------| | [BinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator) | Represents an operation upon two operands of the same type, producing a result of the same type as the operands. | |

Represents a function that accepts two arguments and produces a result. This is the two-arity specialization of [Function](https://developer.android.com/reference/kotlin/java/util/function/Function).

This is a [functional interface](https://developer.android.com/reference/kotlin/java/util/function/package-summary) whose functional method is [apply(java.lang.Object,java.lang.Object)](https://developer.android.com/reference/kotlin/java/util/function/BiFunction#apply(java.util.function.BiFunction.T,%20java.util.function.BiFunction.U)).

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction#)\<T,U,V\>! | [andThen](https://developer.android.com/reference/kotlin/java/util/function/BiFunction#andThen(java.util.function.Function))`(`after:` ` [Function](https://developer.android.com/reference/kotlin/java/util/function/Function)<in` `R,` `out` `V>!`)` Returns a composed function that first applies this function to its input, and then applies the`after`function to the result. |
| abstractR | [apply](https://developer.android.com/reference/kotlin/java/util/function/BiFunction#apply(java.util.function.BiFunction.T,%20java.util.function.BiFunction.U))`(`t:` `T`, `u:` `U`)` Applies this function to the given arguments. |

## Public methods

### andThen

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <V : Any!> andThen(after: Function<in R, out V>!): BiFunction<T, U, V>!
```

Returns a composed function that first applies this function to its input, and then applies the`after`function to the result. If evaluation of either function throws an exception, it is relayed to the caller of the composed function.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<V>` | the type of output of the`after`function, and of the composed function |
| `after` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function)\<inR,outV\>!:the function to apply after this function is applied |

| Return ||
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction#)<T,` `U,` `V>! | a composed function that first applies this function and then applies the`after`function |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | if after is null |

### apply

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun apply(
    t: T, 
    u: U
): R
```

Applies this function to the given arguments.

| Parameters ||
|-----|--------------------------------|
| `t` | T:the first function argument |
| `u` | U:the second function argument |

| Return ||
|---|---------------------|
| R | the function result |
