# LongUnaryOperator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LongUnaryOperator

```
@FunctionalInterface interface LongUnaryOperator
```

| [java.util.function.LongUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/LongUnaryOperator#) |

Represents an operation on a single `long`-valued operand that produces a `long`-valued result. This is the primitive type specialization of [UnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/UnaryOperator) for `long`.

This is a [functional interface](https://developer.android.com/reference/kotlin/java/util/function/package-summary) whose functional method is [applyAsLong(long)](https://developer.android.com/reference/kotlin/java/util/function/LongUnaryOperator#applyAsLong(kotlin.Long)).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [LongUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/LongUnaryOperator#)! | [andThen](https://developer.android.com/reference/kotlin/java/util/function/LongUnaryOperator#andThen(java.util.function.LongUnaryOperator))`(`after:` ` [LongUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/LongUnaryOperator#)!`)` Returns a composed operator that first applies this operator to its input, and then applies the `after` operator to the result. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [applyAsLong](https://developer.android.com/reference/kotlin/java/util/function/LongUnaryOperator#applyAsLong(kotlin.Long))`(`operand:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Applies this operator to the given operand. |
| open [LongUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/LongUnaryOperator#)! | [compose](https://developer.android.com/reference/kotlin/java/util/function/LongUnaryOperator#compose(java.util.function.LongUnaryOperator))`(`before:` ` [LongUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/LongUnaryOperator#)!`)` Returns a composed operator that first applies the `before` operator to its input, and then applies this operator to the result. |
| --- | --- |
| open static [LongUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/LongUnaryOperator#)! | [identity](https://developer.android.com/reference/kotlin/java/util/function/LongUnaryOperator#identity())`()` Returns a unary operator that always returns its input argument. |

## Public methods

### andThen

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun andThen(after: LongUnaryOperator!): LongUnaryOperator!
```

Returns a composed operator that first applies this operator to its input, and then applies the `after` operator to the result. If evaluation of either operator throws an exception, it is relayed to the caller of the composed operator.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `after` | [LongUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/LongUnaryOperator#)!: the operator to apply after this operator is applied |

| Return ||
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [LongUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/LongUnaryOperator#)! | a composed operator that first applies this operator and then applies the `after` operator |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | if after is null |

**See Also**

- [#compose(LongUnaryOperator)](https://developer.android.com/reference/kotlin/java/util/function/LongUnaryOperator#compose(java.util.function.LongUnaryOperator)) 

### applyAsLong

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun applyAsLong(operand: Long): Long
```

Applies this operator to the given operand.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------|
| `operand` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the operand |

| Return ||
|------------------------------------------------------------------------------|---------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the operator result |

### compose

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun compose(before: LongUnaryOperator!): LongUnaryOperator!
```

Returns a composed operator that first applies the `before` operator to its input, and then applies this operator to the result. If evaluation of either operator throws an exception, it is relayed to the caller of the composed operator.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `before` | [LongUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/LongUnaryOperator#)!: the operator to apply before this operator is applied |

| Return ||
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [LongUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/LongUnaryOperator#)! | a composed operator that first applies the `before` operator and then applies this operator |

| Exceptions ||
|----------------------------------|-------------------|
| `java.lang.NullPointerException` | if before is null |

**See Also**

- [#andThen(LongUnaryOperator)](https://developer.android.com/reference/kotlin/java/util/function/LongUnaryOperator#andThen(java.util.function.LongUnaryOperator)) 

### identity

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun identity(): LongUnaryOperator!
```

Returns a unary operator that always returns its input argument.

| Return ||
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [LongUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/LongUnaryOperator#)! | a unary operator that always returns its input argument |
