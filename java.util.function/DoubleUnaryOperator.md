# DoubleUnaryOperator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DoubleUnaryOperator

```
@FunctionalInterface interface DoubleUnaryOperator
```

| [java.util.function.DoubleUnaryOperator](../java/util/function/DoubleUnaryOperator.md) |

Represents an operation on a single`double`-valued operand that produces a`double`-valued result. This is the primitive type specialization of [UnaryOperator](../java/util/function/UnaryOperator.md) for`double`.

This is a [functional interface](../java/util/function/_package.md) whose functional method is [applyAsDouble(double)](../java/util/function/DoubleUnaryOperator.md)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [DoubleUnaryOperator](../java/util/function/DoubleUnaryOperator.md)! | [andThen](../java/util/function/DoubleUnaryOperator.md))`(`after:` ` [DoubleUnaryOperator](../java/util/function/DoubleUnaryOperator.md)!`)` Returns a composed operator that first applies this operator to its input, and then applies the`after`operator to the result. |
| abstract [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [applyAsDouble](../java/util/function/DoubleUnaryOperator.md))`(`operand:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Applies this operator to the given operand. |
| open [DoubleUnaryOperator](../java/util/function/DoubleUnaryOperator.md)! | [compose](../java/util/function/DoubleUnaryOperator.md))`(`before:` ` [DoubleUnaryOperator](../java/util/function/DoubleUnaryOperator.md)!`)` Returns a composed operator that first applies the`before`operator to its input, and then applies this operator to the result. |
| --- | --- |
| openstatic [DoubleUnaryOperator](../java/util/function/DoubleUnaryOperator.md)! | [identity](../java/util/function/DoubleUnaryOperator.md))`()` Returns a unary operator that always returns its input argument. |

## Public methods

### andThen

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun andThen(after: DoubleUnaryOperator!): DoubleUnaryOperator!
```

Returns a composed operator that first applies this operator to its input, and then applies the`after`operator to the result. If evaluation of either operator throws an exception, it is relayed to the caller of the composed operator.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `after` | [DoubleUnaryOperator](../java/util/function/DoubleUnaryOperator.md)!:the operator to apply after this operator is applied |

| Return ||
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [DoubleUnaryOperator](../java/util/function/DoubleUnaryOperator.md)! | a composed operator that first applies this operator and then applies the`after`operator |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | if after is null |

**See Also**

- [#compose(DoubleUnaryOperator)](../java/util/function/DoubleUnaryOperator.md)) 

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
| `before` | [DoubleUnaryOperator](../java/util/function/DoubleUnaryOperator.md)!:the operator to apply before this operator is applied |

| Return ||
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [DoubleUnaryOperator](../java/util/function/DoubleUnaryOperator.md)! | a composed operator that first applies the`before`operator and then applies this operator |

| Exceptions ||
|----------------------------------|-------------------|
| `java.lang.NullPointerException` | if before is null |

**See Also**

- [#andThen(DoubleUnaryOperator)](../java/util/function/DoubleUnaryOperator.md)) 

### identity

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun identity(): DoubleUnaryOperator!
```

Returns a unary operator that always returns its input argument.

| Return ||
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [DoubleUnaryOperator](../java/util/function/DoubleUnaryOperator.md)! | a unary operator that always returns its input argument |
