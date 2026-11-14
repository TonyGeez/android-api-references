# IntBinaryOperator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IntBinaryOperator

```
@FunctionalInterface interface IntBinaryOperator
```

| [java.util.function.IntBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntBinaryOperator#) |

Represents an operation upon two`int`-valued operands and producing an`int`-valued result. This is the primitive type specialization of [BinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator) for`int`.

This is a [functional interface](https://developer.android.com/reference/kotlin/java/util/function/package-summary) whose functional method is [applyAsInt(int,int)](https://developer.android.com/reference/kotlin/java/util/function/IntBinaryOperator#applyAsInt(kotlin.Int,%20kotlin.Int)).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [applyAsInt](https://developer.android.com/reference/kotlin/java/util/function/IntBinaryOperator#applyAsInt(kotlin.Int,%20kotlin.Int))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Applies this operator to the given operands. |

## Public methods

### applyAsInt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun applyAsInt(
    left: Int, 
    right: Int
): Int
```

Applies this operator to the given operands.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------|
| `left` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first operand |
| `right` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the second operand |

| Return ||
|----------------------------------------------------------------------------|---------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the operator result |
