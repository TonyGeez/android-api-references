# BiFunction

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BiFunction

```
@FunctionalInterface interface BiFunction<T : Any!, U : Any!, R : Any!>
```

| [java.util.function.BiFunction](BiFunction.md) |

| Known Direct Subclasses [BinaryOperator](BinaryOperator.md) |----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------| | [BinaryOperator](BinaryOperator.md) | Represents an operation upon two operands of the same type, producing a result of the same type as the operands. | |
| --- | --- | --- | --- | --- | --- | --- |

Represents a function that accepts two arguments and produces a result. This is the two-arity specialization of [Function](Function.md).

This is a [functional interface](_package.md) whose functional method is [apply(java.lang.Object,java.lang.Object)](BiFunction.md)).

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [BiFunction](BiFunction.md)\<T,U,V\>! | [andThen](BiFunction.md))`(`after:` ` [Function](Function.md)<in` `R,` `out` `V>!`)` Returns a composed function that first applies this function to its input, and then applies the`after`function to the result. |
| abstractR | [apply](BiFunction.md))`(`t:` `T`, `u:` `U`)` Applies this function to the given arguments. |

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
| `after` | [Function](Function.md)\<inR,outV\>!:the function to apply after this function is applied |

| Return ||
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [BiFunction](BiFunction.md)<T,` `U,` `V>! | a composed function that first applies this function and then applies the`after`function |

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
