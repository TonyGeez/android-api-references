# IntPredicate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IntPredicate

```
@FunctionalInterface interface IntPredicate
```

| [java.util.function.IntPredicate](IntPredicate.md) |

Represents a predicate (boolean-valued function) of one`int`-valued argument. This is the`int`-consuming primitive type specialization of [Predicate](Predicate.md).

This is a [functional interface](_package.md) whose functional method is [test(int)](IntPredicate.md)).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [IntPredicate](IntPredicate.md)! | [and](IntPredicate.md))`(`other:` ` [IntPredicate](IntPredicate.md)!`)` Returns a composed predicate that represents a short-circuiting logical AND of this predicate and another. |
| open [IntPredicate](IntPredicate.md)! | [negate](IntPredicate.md))`()` Returns a predicate that represents the logical negation of this predicate. |
| open [IntPredicate](IntPredicate.md)! | [or](IntPredicate.md))`(`other:` ` [IntPredicate](IntPredicate.md)!`)` Returns a composed predicate that represents a short-circuiting logical OR of this predicate and another. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [test](IntPredicate.md))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Evaluates this predicate on the given argument. |

## Public methods

### and

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun and(other: IntPredicate!): IntPredicate!
```

Returns a composed predicate that represents a short-circuiting logical AND of this predicate and another. When evaluating the composed predicate, if this predicate is`false`, then the`other`predicate is not evaluated.

Any exceptions thrown during evaluation of either predicate are relayed to the caller; if evaluation of this predicate throws an exception, the`other`predicate will not be evaluated.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `other` | [IntPredicate](IntPredicate.md)!:a predicate that will be logically-ANDed with this predicate |

| Return ||
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [IntPredicate](IntPredicate.md)! | a composed predicate that represents the short-circuiting logical AND of this predicate and the`other`predicate |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | if other is null |

### negate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun negate(): IntPredicate!
```

Returns a predicate that represents the logical negation of this predicate.

| Return ||
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [IntPredicate](IntPredicate.md)! | a predicate that represents the logical negation of this predicate |

### or

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun or(other: IntPredicate!): IntPredicate!
```

Returns a composed predicate that represents a short-circuiting logical OR of this predicate and another. When evaluating the composed predicate, if this predicate is`true`, then the`other`predicate is not evaluated.

Any exceptions thrown during evaluation of either predicate are relayed to the caller; if evaluation of this predicate throws an exception, the`other`predicate will not be evaluated.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `other` | [IntPredicate](IntPredicate.md)!:a predicate that will be logically-ORed with this predicate |

| Return ||
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [IntPredicate](IntPredicate.md)! | a composed predicate that represents the short-circuiting logical OR of this predicate and the`other`predicate |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | if other is null |

### test

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun test(value: Int): Boolean
```

Evaluates this predicate on the given argument.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------|
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the input argument |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the input argument matches the predicate, otherwise`false` |
