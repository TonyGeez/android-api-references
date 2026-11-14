# BinaryOperator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BinaryOperator

```
@FunctionalInterface interface BinaryOperator<T : Any!> : BiFunction<T, T, T>
```

| [java.util.function.BinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator#) |

Represents an operation upon two operands of the same type, producing a result of the same type as the operands. This is a specialization of [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction) for the case where the operands and the result are all of the same type.

This is a [functional interface](https://developer.android.com/reference/kotlin/java/util/function/package-summary) whose functional method is [apply(java.lang.Object,java.lang.Object)](https://developer.android.com/reference/kotlin/java/util/function/BiFunction#apply(java.util.function.BiFunction.T,%20java.util.function.BiFunction.U)).

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [BinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator#)\<T\>! | [maxBy](https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator#maxBy(java.util.Comparator))`(`comparator:` ` [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator.html#)<in` `T>!`)` Returns a [BinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator#) which returns the greater of two elements according to the specified`Comparator`. |
| openstatic [BinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator#)\<T\>! | [minBy](https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator#minBy(java.util.Comparator))`(`comparator:` ` [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator.html#)<in` `T>!`)` Returns a [BinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator#) which returns the lesser of two elements according to the specified`Comparator`. |

| Inherited functions ||
|---|---|
| From class [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction) |----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction)<T,` `U,` `V>! | [andThen](https://developer.android.com/reference/kotlin/java/util/function/BiFunction#andThen(java.util.function.Function))`(`after:` ` [Function](https://developer.android.com/reference/kotlin/java/util/function/Function)<in` `R,` `out` `V>!`)` <br /> Returns a composed function that first applies this function to its input, and then applies the`after`function to the result. If evaluation of either function throws an exception, it is relayed to the caller of the composed function. <br /> | | R | [apply](https://developer.android.com/reference/kotlin/java/util/function/BiFunction#apply(java.util.function.BiFunction.T,%20java.util.function.BiFunction.U))`(`t:` `T`, `u:` `U`)` <br /> Applies this function to the given arguments. <br /> | ||

## Public methods

### maxBy

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> maxBy(comparator: Comparator<in T>!): BinaryOperator<T>!
```

Returns a [BinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator#) which returns the greater of two elements according to the specified`Comparator`.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the type of the input arguments of the comparator |
| `comparator` | [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator.html#)\<inT\>!:a`Comparator`for comparing the two values |

| Return ||
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [BinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator#)<T>! | a`BinaryOperator`which returns the greater of its operands, according to the supplied`Comparator` |

| Exceptions ||
|----------------------------------|-------------------------|
| `java.lang.NullPointerException` | if the argument is null |

### minBy

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> minBy(comparator: Comparator<in T>!): BinaryOperator<T>!
```

Returns a [BinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator#) which returns the lesser of two elements according to the specified`Comparator`.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the type of the input arguments of the comparator |
| `comparator` | [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator.html#)\<inT\>!:a`Comparator`for comparing the two values |

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [BinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator#)<T>! | a`BinaryOperator`which returns the lesser of its operands, according to the supplied`Comparator` |

| Exceptions ||
|----------------------------------|-------------------------|
| `java.lang.NullPointerException` | if the argument is null |
