# IntUnaryOperator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IntUnaryOperator

```
@FunctionalInterface interface IntUnaryOperator
```

| [java.util.function.IntUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntUnaryOperator#) |

Represents an operation on a single`int`-valued operand that produces an`int`-valued result. This is the primitive type specialization of [UnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/UnaryOperator) for`int`.

This is a [functional interface](https://developer.android.com/reference/kotlin/java/util/function/package-summary) whose functional method is [applyAsInt(int)](https://developer.android.com/reference/kotlin/java/util/function/IntUnaryOperator#applyAsInt(kotlin.Int)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [IntUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntUnaryOperator#)! | [andThen](https://developer.android.com/reference/kotlin/java/util/function/IntUnaryOperator#andThen(java.util.function.IntUnaryOperator))`(`after:` ` [IntUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntUnaryOperator#)!`)` Returns a composed operator that first applies this operator to its input, and then applies the`after`operator to the result. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [applyAsInt](https://developer.android.com/reference/kotlin/java/util/function/IntUnaryOperator#applyAsInt(kotlin.Int))`(`operand:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Applies this operator to the given operand. |
| open [IntUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntUnaryOperator#)! | [compose](https://developer.android.com/reference/kotlin/java/util/function/IntUnaryOperator#compose(java.util.function.IntUnaryOperator))`(`before:` ` [IntUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntUnaryOperator#)!`)` Returns a composed operator that first applies the`before`operator to its input, and then applies this operator to the result. |
| openstatic [IntUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntUnaryOperator#)! | [identity](https://developer.android.com/reference/kotlin/java/util/function/IntUnaryOperator#identity())`()` Returns a unary operator that always returns its input argument. |

## Public methods

### andThen

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun andThen(after: IntUnaryOperator!): IntUnaryOperator!
```

Returns a composed operator that first applies this operator to its input, and then applies the`after`operator to the result. If evaluation of either operator throws an exception, it is relayed to the caller of the composed operator.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `after` | [IntUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntUnaryOperator#)!:the operator to apply after this operator is applied |

| Return ||
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [IntUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntUnaryOperator#)! | a composed operator that first applies this operator and then applies the`after`operator |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | if after is null |

**See Also**

- [#compose(IntUnaryOperator)](https://developer.android.com/reference/kotlin/java/util/function/IntUnaryOperator#compose(java.util.function.IntUnaryOperator)) 

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
| `before` | [IntUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntUnaryOperator#)!:the operator to apply before this operator is applied |

| Return ||
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [IntUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntUnaryOperator#)! | a composed operator that first applies the`before`operator and then applies this operator |

| Exceptions ||
|----------------------------------|-------------------|
| `java.lang.NullPointerException` | if before is null |

**See Also**

- [#andThen(IntUnaryOperator)](https://developer.android.com/reference/kotlin/java/util/function/IntUnaryOperator#andThen(java.util.function.IntUnaryOperator)) 

### identity

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun identity(): IntUnaryOperator!
```

Returns a unary operator that always returns its input argument.

| Return ||
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [IntUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntUnaryOperator#)! | a unary operator that always returns its input argument |
