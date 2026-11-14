# LongUnaryOperator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LongUnaryOperator

```
@FunctionalInterface interface LongUnaryOperator
```

| [java.util.function.LongUnaryOperator](LongUnaryOperator.md) |

Represents an operation on a single `long`-valued operand that produces a `long`-valued result. This is the primitive type specialization of [UnaryOperator](UnaryOperator.md) for `long`.

This is a [functional interface](_package.md) whose functional method is [applyAsLong(long)](LongUnaryOperator.md)).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [LongUnaryOperator](LongUnaryOperator.md)! | [andThen](LongUnaryOperator.md))`(`after:` ` [LongUnaryOperator](LongUnaryOperator.md)!`)` Returns a composed operator that first applies this operator to its input, and then applies the `after` operator to the result. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [applyAsLong](LongUnaryOperator.md))`(`operand:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Applies this operator to the given operand. |
| open [LongUnaryOperator](LongUnaryOperator.md)! | [compose](LongUnaryOperator.md))`(`before:` ` [LongUnaryOperator](LongUnaryOperator.md)!`)` Returns a composed operator that first applies the `before` operator to its input, and then applies this operator to the result. |
| --- | --- |
| open static [LongUnaryOperator](LongUnaryOperator.md)! | [identity](LongUnaryOperator.md))`()` Returns a unary operator that always returns its input argument. |

## Public methods

### andThen

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun andThen(after: LongUnaryOperator!): LongUnaryOperator!
```

Returns a composed operator that first applies this operator to its input, and then applies the `after` operator to the result. If evaluation of either operator throws an exception, it is relayed to the caller of the composed operator.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `after` | [LongUnaryOperator](LongUnaryOperator.md)!: the operator to apply after this operator is applied |

| Return ||
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [LongUnaryOperator](LongUnaryOperator.md)! | a composed operator that first applies this operator and then applies the `after` operator |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | if after is null |

**See Also**

- [#compose(LongUnaryOperator)](LongUnaryOperator.md)) 

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
| `before` | [LongUnaryOperator](LongUnaryOperator.md)!: the operator to apply before this operator is applied |

| Return ||
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [LongUnaryOperator](LongUnaryOperator.md)! | a composed operator that first applies the `before` operator and then applies this operator |

| Exceptions ||
|----------------------------------|-------------------|
| `java.lang.NullPointerException` | if before is null |

**See Also**

- [#andThen(LongUnaryOperator)](LongUnaryOperator.md)) 

### identity

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun identity(): LongUnaryOperator!
```

Returns a unary operator that always returns its input argument.

| Return ||
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [LongUnaryOperator](LongUnaryOperator.md)! | a unary operator that always returns its input argument |
