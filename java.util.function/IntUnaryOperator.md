# IntUnaryOperator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IntUnaryOperator

```
@FunctionalInterface interface IntUnaryOperator
```

| [java.util.function.IntUnaryOperator](../java/util/function/IntUnaryOperator.md) |

Represents an operation on a single`int`-valued operand that produces an`int`-valued result. This is the primitive type specialization of [UnaryOperator](../java/util/function/UnaryOperator.md) for`int`.

This is a [functional interface](../java/util/function/_package.md) whose functional method is [applyAsInt(int)](../java/util/function/IntUnaryOperator.md)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [IntUnaryOperator](../java/util/function/IntUnaryOperator.md)! | [andThen](../java/util/function/IntUnaryOperator.md))`(`after:` ` [IntUnaryOperator](../java/util/function/IntUnaryOperator.md)!`)` Returns a composed operator that first applies this operator to its input, and then applies the`after`operator to the result. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [applyAsInt](../java/util/function/IntUnaryOperator.md))`(`operand:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Applies this operator to the given operand. |
| open [IntUnaryOperator](../java/util/function/IntUnaryOperator.md)! | [compose](../java/util/function/IntUnaryOperator.md))`(`before:` ` [IntUnaryOperator](../java/util/function/IntUnaryOperator.md)!`)` Returns a composed operator that first applies the`before`operator to its input, and then applies this operator to the result. |
| --- | --- |
| openstatic [IntUnaryOperator](../java/util/function/IntUnaryOperator.md)! | [identity](../java/util/function/IntUnaryOperator.md))`()` Returns a unary operator that always returns its input argument. |

## Public methods

### andThen

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun andThen(after: IntUnaryOperator!): IntUnaryOperator!
```

Returns a composed operator that first applies this operator to its input, and then applies the`after`operator to the result. If evaluation of either operator throws an exception, it is relayed to the caller of the composed operator.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `after` | [IntUnaryOperator](../java/util/function/IntUnaryOperator.md)!:the operator to apply after this operator is applied |

| Return ||
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [IntUnaryOperator](../java/util/function/IntUnaryOperator.md)! | a composed operator that first applies this operator and then applies the`after`operator |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | if after is null |

**See Also**

- [#compose(IntUnaryOperator)](../java/util/function/IntUnaryOperator.md)) 

### applyAsInt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun applyAsInt(operand: Int): Int
```

Applies this operator to the given operand.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------|
| `operand` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the operand |

| Return ||
|----------------------------------------------------------------------------|---------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the operator result |

### compose

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun compose(before: IntUnaryOperator!): IntUnaryOperator!
```

Returns a composed operator that first applies the`before`operator to its input, and then applies this operator to the result. If evaluation of either operator throws an exception, it is relayed to the caller of the composed operator.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `before` | [IntUnaryOperator](../java/util/function/IntUnaryOperator.md)!:the operator to apply before this operator is applied |

| Return ||
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [IntUnaryOperator](../java/util/function/IntUnaryOperator.md)! | a composed operator that first applies the`before`operator and then applies this operator |

| Exceptions ||
|----------------------------------|-------------------|
| `java.lang.NullPointerException` | if before is null |

**See Also**

- [#andThen(IntUnaryOperator)](../java/util/function/IntUnaryOperator.md)) 

### identity

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun identity(): IntUnaryOperator!
```

Returns a unary operator that always returns its input argument.

| Return ||
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [IntUnaryOperator](../java/util/function/IntUnaryOperator.md)! | a unary operator that always returns its input argument |
