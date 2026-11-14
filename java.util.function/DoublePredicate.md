# DoublePredicate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DoublePredicate

```
@FunctionalInterface interface DoublePredicate
```

| [java.util.function.DoublePredicate](https://developer.android.com/reference/kotlin/java/util/function/DoublePredicate#) |

Represents a predicate (boolean-valued function) of one`double`-valued argument. This is the`double`-consuming primitive type specialization of [Predicate](https://developer.android.com/reference/kotlin/java/util/function/Predicate).

This is a [functional interface](https://developer.android.com/reference/kotlin/java/util/function/package-summary) whose functional method is [test(double)](https://developer.android.com/reference/kotlin/java/util/function/DoublePredicate#test(kotlin.Double)).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [DoublePredicate](https://developer.android.com/reference/kotlin/java/util/function/DoublePredicate#)! | [and](https://developer.android.com/reference/kotlin/java/util/function/DoublePredicate#and(java.util.function.DoublePredicate))`(`other:` ` [DoublePredicate](https://developer.android.com/reference/kotlin/java/util/function/DoublePredicate#)!`)` Returns a composed predicate that represents a short-circuiting logical AND of this predicate and another. |
| open [DoublePredicate](https://developer.android.com/reference/kotlin/java/util/function/DoublePredicate#)! | [negate](https://developer.android.com/reference/kotlin/java/util/function/DoublePredicate#negate())`()` Returns a predicate that represents the logical negation of this predicate. |
| open [DoublePredicate](https://developer.android.com/reference/kotlin/java/util/function/DoublePredicate#)! | [or](https://developer.android.com/reference/kotlin/java/util/function/DoublePredicate#or(java.util.function.DoublePredicate))`(`other:` ` [DoublePredicate](https://developer.android.com/reference/kotlin/java/util/function/DoublePredicate#)!`)` Returns a composed predicate that represents a short-circuiting logical OR of this predicate and another. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [test](https://developer.android.com/reference/kotlin/java/util/function/DoublePredicate#test(kotlin.Double))`(`value:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Evaluates this predicate on the given argument. |

## Public methods

### and

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun and(other: DoublePredicate!): DoublePredicate!
```

Returns a composed predicate that represents a short-circuiting logical AND of this predicate and another. When evaluating the composed predicate, if this predicate is`false`, then the`other`predicate is not evaluated.

Any exceptions thrown during evaluation of either predicate are relayed to the caller; if evaluation of this predicate throws an exception, the`other`predicate will not be evaluated.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `other` | [DoublePredicate](https://developer.android.com/reference/kotlin/java/util/function/DoublePredicate#)!:a predicate that will be logically-ANDed with this predicate |

| Return ||
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [DoublePredicate](https://developer.android.com/reference/kotlin/java/util/function/DoublePredicate#)! | a composed predicate that represents the short-circuiting logical AND of this predicate and the`other`predicate |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | if other is null |

### negate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun negate(): DoublePredicate!
```

Returns a predicate that represents the logical negation of this predicate.

| Return ||
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [DoublePredicate](https://developer.android.com/reference/kotlin/java/util/function/DoublePredicate#)! | a predicate that represents the logical negation of this predicate |

### or

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun or(other: DoublePredicate!): DoublePredicate!
```

Returns a composed predicate that represents a short-circuiting logical OR of this predicate and another. When evaluating the composed predicate, if this predicate is`true`, then the`other`predicate is not evaluated.

Any exceptions thrown during evaluation of either predicate are relayed to the caller; if evaluation of this predicate throws an exception, the`other`predicate will not be evaluated.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `other` | [DoublePredicate](https://developer.android.com/reference/kotlin/java/util/function/DoublePredicate#)!:a predicate that will be logically-ORed with this predicate |

| Return ||
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [DoublePredicate](https://developer.android.com/reference/kotlin/java/util/function/DoublePredicate#)! | a composed predicate that represents the short-circuiting logical OR of this predicate and the`other`predicate |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | if other is null |

### test

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun test(value: Double): Boolean
```

Evaluates this predicate on the given argument.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------|
| `value` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the input argument |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the input argument matches the predicate, otherwise`false` |
