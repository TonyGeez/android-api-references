# DoubleBinaryOperator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DoubleBinaryOperator

```
@FunctionalInterface interface DoubleBinaryOperator
```

| [java.util.function.DoubleBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/DoubleBinaryOperator#) |

Represents an operation upon two`double`-valued operands and producing a`double`-valued result. This is the primitive type specialization of [BinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator) for`double`.

This is a [functional interface](https://developer.android.com/reference/kotlin/java/util/function/package-summary) whose functional method is [applyAsDouble(double,double)](https://developer.android.com/reference/kotlin/java/util/function/DoubleBinaryOperator#applyAsDouble(kotlin.Double,%20kotlin.Double)).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [applyAsDouble](https://developer.android.com/reference/kotlin/java/util/function/DoubleBinaryOperator#applyAsDouble(kotlin.Double,%20kotlin.Double))`(`left:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `right:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Applies this operator to the given operands. |

## Public methods

### applyAsDouble

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun applyAsDouble(
    left: Double, 
    right: Double
): Double
```

Applies this operator to the given operands.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------|
| `left` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the first operand |
| `right` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the second operand |

| Return ||
|----------------------------------------------------------------------------------|---------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the operator result |
