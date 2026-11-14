# BinaryOperator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BinaryOperator

```
@FunctionalInterface interface BinaryOperator<T : Any!> : BiFunction<T, T, T>
```

| [java.util.function.BinaryOperator](../java/util/function/BinaryOperator.md) |

Represents an operation upon two operands of the same type, producing a result of the same type as the operands. This is a specialization of [BiFunction](../java/util/function/BiFunction.md) for the case where the operands and the result are all of the same type.

This is a [functional interface](../java/util/function/_package.md) whose functional method is [apply(java.lang.Object,java.lang.Object)](../java/util/function/BiFunction.md)).

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [BinaryOperator](../java/util/function/BinaryOperator.md)\<T\>! | [maxBy](../java/util/function/BinaryOperator.md))`(`comparator:` ` [Comparator](../java/util/Comparator.md)<in` `T>!`)` Returns a [BinaryOperator](../java/util/function/BinaryOperator.md) which returns the greater of two elements according to the specified`Comparator`. |
| openstatic [BinaryOperator](../java/util/function/BinaryOperator.md)\<T\>! | [minBy](../java/util/function/BinaryOperator.md))`(`comparator:` ` [Comparator](../java/util/Comparator.md)<in` `T>!`)` Returns a [BinaryOperator](../java/util/function/BinaryOperator.md) which returns the lesser of two elements according to the specified`Comparator`. |

| Inherited functions ||
|---|---|
| From class [BiFunction](../java/util/function/BiFunction.md) |----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [BiFunction](../java/util/function/BiFunction.md)<T,` `U,` `V>! | [andThen](../java/util/function/BiFunction.md))`(`after:` ` [Function](../java/util/function/Function.md)<in` `R,` `out` `V>!`)` <br /> Returns a composed function that first applies this function to its input, and then applies the`after`function to the result. If evaluation of either function throws an exception, it is relayed to the caller of the composed function. <br /> | | R | [apply](../java/util/function/BiFunction.md))`(`t:` `T`, `u:` `U`)` <br /> Applies this function to the given arguments. <br /> | ||

## Public methods

### maxBy

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> maxBy(comparator: Comparator<in T>!): BinaryOperator<T>!
```

Returns a [BinaryOperator](../java/util/function/BinaryOperator.md) which returns the greater of two elements according to the specified`Comparator`.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the type of the input arguments of the comparator |
| `comparator` | [Comparator](../java/util/Comparator.md)\<inT\>!:a`Comparator`for comparing the two values |

| Return ||
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [BinaryOperator](../java/util/function/BinaryOperator.md)<T>! | a`BinaryOperator`which returns the greater of its operands, according to the supplied`Comparator` |

| Exceptions ||
|----------------------------------|-------------------------|
| `java.lang.NullPointerException` | if the argument is null |

### minBy

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> minBy(comparator: Comparator<in T>!): BinaryOperator<T>!
```

Returns a [BinaryOperator](../java/util/function/BinaryOperator.md) which returns the lesser of two elements according to the specified`Comparator`.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the type of the input arguments of the comparator |
| `comparator` | [Comparator](../java/util/Comparator.md)\<inT\>!:a`Comparator`for comparing the two values |

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [BinaryOperator](../java/util/function/BinaryOperator.md)<T>! | a`BinaryOperator`which returns the lesser of its operands, according to the supplied`Comparator` |

| Exceptions ||
|----------------------------------|-------------------------|
| `java.lang.NullPointerException` | if the argument is null |
