# DoubleUnaryOperator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DoubleUnaryOperator

```
@FunctionalInterface interface DoubleUnaryOperator
```

| [java.util.function.DoubleUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/DoubleUnaryOperator#) |

Represents an operation on a single`double`-valued operand that produces a`double`-valued result. This is the primitive type specialization of [UnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/UnaryOperator) for`double`.

This is a [functional interface](https://developer.android.com/reference/kotlin/java/util/function/package-summary) whose functional method is [applyAsDouble(double)](https://developer.android.com/reference/kotlin/java/util/function/DoubleUnaryOperator#applyAsDouble(kotlin.Double)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [DoubleUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/DoubleUnaryOperator#)! | [andThen](https://developer.android.com/reference/kotlin/java/util/function/DoubleUnaryOperator#andThen(java.util.function.DoubleUnaryOperator))`(`after:` ` [DoubleUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/DoubleUnaryOperator#)!`)` Returns a composed operator that first applies this operator to its input, and then applies the`after`operator to the result. |
| abstract [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [applyAsDouble](https://developer.android.com/reference/kotlin/java/util/function/DoubleUnaryOperator#applyAsDouble(kotlin.Double))`(`operand:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Applies this operator to the given operand. |
| open [DoubleUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/DoubleUnaryOperator#)! | [compose](https://developer.android.com/reference/kotlin/java/util/function/DoubleUnaryOperator#compose(java.util.function.DoubleUnaryOperator))`(`before:` ` [DoubleUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/DoubleUnaryOperator#)!`)` Returns a composed operator that first applies the`before`operator to its input, and then applies this operator to the result. |
| openstatic [DoubleUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/DoubleUnaryOperator#)! | [identity](https://developer.android.com/reference/kotlin/java/util/function/DoubleUnaryOperator#identity())`()` Returns a unary operator that always returns its input argument. |

## Public methods

### andThen

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun andThen(after: DoubleUnaryOperator!): DoubleUnaryOperator!
```

Returns a composed operator that first applies this operator to its input, and then applies the`after`operator to the result. If evaluation of either operator throws an exception, it is relayed to the caller of the composed operator.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `after` | [DoubleUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/DoubleUnaryOperator#)!:the operator to apply after this operator is applied |

| Return ||
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [DoubleUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/DoubleUnaryOperator#)! | a composed operator that first applies this operator and then applies the`after`operator |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | if after is null |

**See Also**

- [#compose(DoubleUnaryOperator)](https://developer.android.com/reference/kotlin/java/util/function/DoubleUnaryOperator#compose(java.util.function.DoubleUnaryOperator)) 

### applyAsDouble

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun applyAsDouble(operand: Double): Double
```

Applies this operator to the given operand.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------|
| `operand` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the operand |

| Return ||
|----------------------------------------------------------------------------------|---------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the operator result |

### compose

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun compose(before: DoubleUnaryOperator!): DoubleUnaryOperator!
```

Returns a composed operator that first applies the`before`operator to its input, and then applies this operator to the result. If evaluation of either operator throws an exception, it is relayed to the caller of the composed operator.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `before` | [DoubleUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/DoubleUnaryOperator#)!:the operator to apply before this operator is applied |

| Return ||
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [DoubleUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/DoubleUnaryOperator#)! | a composed operator that first applies the`before`operator and then applies this operator |

| Exceptions ||
|----------------------------------|-------------------|
| `java.lang.NullPointerException` | if before is null |

**See Also**

- [#andThen(DoubleUnaryOperator)](https://developer.android.com/reference/kotlin/java/util/function/DoubleUnaryOperator#andThen(java.util.function.DoubleUnaryOperator)) 

### identity

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun identity(): DoubleUnaryOperator!
```

Returns a unary operator that always returns its input argument.

| Return ||
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [DoubleUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/DoubleUnaryOperator#)! | a unary operator that always returns its input argument |
