# LongBinaryOperator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LongBinaryOperator

```
@FunctionalInterface interface LongBinaryOperator
```

| [java.util.function.LongBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/LongBinaryOperator#) |

Represents an operation upon two`long`-valued operands and producing a`long`-valued result. This is the primitive type specialization of [BinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator) for`long`.

This is a [functional interface](https://developer.android.com/reference/kotlin/java/util/function/package-summary) whose functional method is [applyAsLong(long,long)](https://developer.android.com/reference/kotlin/java/util/function/LongBinaryOperator#applyAsLong(kotlin.Long,%20kotlin.Long)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [applyAsLong](https://developer.android.com/reference/kotlin/java/util/function/LongBinaryOperator#applyAsLong(kotlin.Long,%20kotlin.Long))`(`left:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `right:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Applies this operator to the given operands. |

## Public methods

### applyAsLong

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun applyAsLong(
    left: Long, 
    right: Long
): Long
```

Applies this operator to the given operands.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------|
| `left` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the first operand |
| `right` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the second operand |

| Return ||
|------------------------------------------------------------------------------|---------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the operator result |
