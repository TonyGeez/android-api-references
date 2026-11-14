# LongPredicate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LongPredicate

```
@FunctionalInterface interface LongPredicate
```

| [java.util.function.LongPredicate](LongPredicate.md) |

Represents a predicate (boolean-valued function) of one`long`-valued argument. This is the`long`-consuming primitive type specialization of [Predicate](Predicate.md).

This is a [functional interface](_package.md) whose functional method is [test(long)](LongPredicate.md)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [LongPredicate](LongPredicate.md)! | [and](LongPredicate.md))`(`other:` ` [LongPredicate](LongPredicate.md)!`)` Returns a composed predicate that represents a short-circuiting logical AND of this predicate and another. |
| open [LongPredicate](LongPredicate.md)! | [negate](LongPredicate.md))`()` Returns a predicate that represents the logical negation of this predicate. |
| open [LongPredicate](LongPredicate.md)! | [or](LongPredicate.md))`(`other:` ` [LongPredicate](LongPredicate.md)!`)` Returns a composed predicate that represents a short-circuiting logical OR of this predicate and another. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [test](LongPredicate.md))`(`value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Evaluates this predicate on the given argument. |

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
| `other` | [LongPredicate](LongPredicate.md)!:a predicate that will be logically-ANDed with this predicate |

| Return ||
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [LongPredicate](LongPredicate.md)! | a composed predicate that represents the short-circuiting logical AND of this predicate and the`other`predicate |

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
| [LongPredicate](LongPredicate.md)! | a predicate that represents the logical negation of this predicate |

### or

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun or(other: LongPredicate!): LongPredicate!
```

Returns a composed predicate that represents a short-circuiting logical OR of this predicate and another. When evaluating the composed predicate, if this predicate is`true`, then the`other`predicate is not evaluated.

Any exceptions thrown during evaluation of either predicate are relayed to the caller; if evaluation of this predicate throws an exception, the`other`predicate will not be evaluated.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `other` | [LongPredicate](LongPredicate.md)!:a predicate that will be logically-ORed with this predicate |

| Return ||
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [LongPredicate](LongPredicate.md)! | a composed predicate that represents the short-circuiting logical OR of this predicate and the`other`predicate |

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
