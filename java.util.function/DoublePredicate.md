# DoublePredicate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DoublePredicate

```
@FunctionalInterface interface DoublePredicate
```

| [java.util.function.DoublePredicate](../java/util/function/DoublePredicate.md) |

Represents a predicate (boolean-valued function) of one`double`-valued argument. This is the`double`-consuming primitive type specialization of [Predicate](../java/util/function/Predicate.md).

This is a [functional interface](../java/util/function/_package.md) whose functional method is [test(double)](../java/util/function/DoublePredicate.md)).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [DoublePredicate](../java/util/function/DoublePredicate.md)! | [and](../java/util/function/DoublePredicate.md))`(`other:` ` [DoublePredicate](../java/util/function/DoublePredicate.md)!`)` Returns a composed predicate that represents a short-circuiting logical AND of this predicate and another. |
| open [DoublePredicate](../java/util/function/DoublePredicate.md)! | [negate](../java/util/function/DoublePredicate.md))`()` Returns a predicate that represents the logical negation of this predicate. |
| open [DoublePredicate](../java/util/function/DoublePredicate.md)! | [or](../java/util/function/DoublePredicate.md))`(`other:` ` [DoublePredicate](../java/util/function/DoublePredicate.md)!`)` Returns a composed predicate that represents a short-circuiting logical OR of this predicate and another. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [test](../java/util/function/DoublePredicate.md))`(`value:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Evaluates this predicate on the given argument. |

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
| `other` | [DoublePredicate](../java/util/function/DoublePredicate.md)!:a predicate that will be logically-ANDed with this predicate |

| Return ||
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [DoublePredicate](../java/util/function/DoublePredicate.md)! | a composed predicate that represents the short-circuiting logical AND of this predicate and the`other`predicate |

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
| [DoublePredicate](../java/util/function/DoublePredicate.md)! | a predicate that represents the logical negation of this predicate |

### or

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun or(other: DoublePredicate!): DoublePredicate!
```

Returns a composed predicate that represents a short-circuiting logical OR of this predicate and another. When evaluating the composed predicate, if this predicate is`true`, then the`other`predicate is not evaluated.

Any exceptions thrown during evaluation of either predicate are relayed to the caller; if evaluation of this predicate throws an exception, the`other`predicate will not be evaluated.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `other` | [DoublePredicate](../java/util/function/DoublePredicate.md)!:a predicate that will be logically-ORed with this predicate |

| Return ||
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [DoublePredicate](../java/util/function/DoublePredicate.md)! | a composed predicate that represents the short-circuiting logical OR of this predicate and the`other`predicate |

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
