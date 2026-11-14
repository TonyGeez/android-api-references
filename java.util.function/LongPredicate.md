# LongPredicate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LongPredicate

```
@FunctionalInterface interface LongPredicate
```

| [java.util.function.LongPredicate](https://developer.android.com/reference/kotlin/java/util/function/LongPredicate#) |

Represents a predicate (boolean-valued function) of one`long`-valued argument. This is the`long`-consuming primitive type specialization of [Predicate](https://developer.android.com/reference/kotlin/java/util/function/Predicate).

This is a [functional interface](https://developer.android.com/reference/kotlin/java/util/function/package-summary) whose functional method is [test(long)](https://developer.android.com/reference/kotlin/java/util/function/LongPredicate#test(kotlin.Long)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [LongPredicate](https://developer.android.com/reference/kotlin/java/util/function/LongPredicate#)! | [and](https://developer.android.com/reference/kotlin/java/util/function/LongPredicate#and(java.util.function.LongPredicate))`(`other:` ` [LongPredicate](https://developer.android.com/reference/kotlin/java/util/function/LongPredicate#)!`)` Returns a composed predicate that represents a short-circuiting logical AND of this predicate and another. |
| open [LongPredicate](https://developer.android.com/reference/kotlin/java/util/function/LongPredicate#)! | [negate](https://developer.android.com/reference/kotlin/java/util/function/LongPredicate#negate())`()` Returns a predicate that represents the logical negation of this predicate. |
| open [LongPredicate](https://developer.android.com/reference/kotlin/java/util/function/LongPredicate#)! | [or](https://developer.android.com/reference/kotlin/java/util/function/LongPredicate#or(java.util.function.LongPredicate))`(`other:` ` [LongPredicate](https://developer.android.com/reference/kotlin/java/util/function/LongPredicate#)!`)` Returns a composed predicate that represents a short-circuiting logical OR of this predicate and another. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [test](https://developer.android.com/reference/kotlin/java/util/function/LongPredicate#test(kotlin.Long))`(`value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Evaluates this predicate on the given argument. |

## Public methods

### and

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun and(other: LongPredicate!): LongPredicate!
```

Returns a composed predicate that represents a short-circuiting logical AND of this predicate and another. When evaluating the composed predicate, if this predicate is`false`, then the`other`predicate is not evaluated.

Any exceptions thrown during evaluation of either predicate are relayed to the caller; if evaluation of this predicate throws an exception, the`other`predicate will not be evaluated.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `other` | [LongPredicate](https://developer.android.com/reference/kotlin/java/util/function/LongPredicate#)!:a predicate that will be logically-ANDed with this predicate |

| Return ||
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [LongPredicate](https://developer.android.com/reference/kotlin/java/util/function/LongPredicate#)! | a composed predicate that represents the short-circuiting logical AND of this predicate and the`other`predicate |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | if other is null |

### negate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun negate(): LongPredicate!
```

Returns a predicate that represents the logical negation of this predicate.

| Return ||
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [LongPredicate](https://developer.android.com/reference/kotlin/java/util/function/LongPredicate#)! | a predicate that represents the logical negation of this predicate |

### or

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun or(other: LongPredicate!): LongPredicate!
```

Returns a composed predicate that represents a short-circuiting logical OR of this predicate and another. When evaluating the composed predicate, if this predicate is`true`, then the`other`predicate is not evaluated.

Any exceptions thrown during evaluation of either predicate are relayed to the caller; if evaluation of this predicate throws an exception, the`other`predicate will not be evaluated.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `other` | [LongPredicate](https://developer.android.com/reference/kotlin/java/util/function/LongPredicate#)!:a predicate that will be logically-ORed with this predicate |

| Return ||
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [LongPredicate](https://developer.android.com/reference/kotlin/java/util/function/LongPredicate#)! | a composed predicate that represents the short-circuiting logical OR of this predicate and the`other`predicate |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | if other is null |

### test

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun test(value: Long): Boolean
```

Evaluates this predicate on the given argument.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------|
| `value` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the input argument |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the input argument matches the predicate, otherwise`false` |
