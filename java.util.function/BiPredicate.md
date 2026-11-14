# BiPredicate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BiPredicate

```
@FunctionalInterface interface BiPredicate<T : Any!, U : Any!>
```

| [java.util.function.BiPredicate](https://developer.android.com/reference/kotlin/java/util/function/BiPredicate#) |

Represents a predicate (boolean-valued function) of two arguments. This is the two-arity specialization of [Predicate](https://developer.android.com/reference/kotlin/java/util/function/Predicate).

This is a [functional interface](https://developer.android.com/reference/kotlin/java/util/function/package-summary) whose functional method is [test(java.lang.Object,java.lang.Object)](https://developer.android.com/reference/kotlin/java/util/function/BiPredicate#test(java.util.function.BiPredicate.T,%20java.util.function.BiPredicate.U)).

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [BiPredicate](https://developer.android.com/reference/kotlin/java/util/function/BiPredicate#)\<T,U\>! | [and](https://developer.android.com/reference/kotlin/java/util/function/BiPredicate#and(java.util.function.BiPredicate))`(`other:` ` [BiPredicate](https://developer.android.com/reference/kotlin/java/util/function/BiPredicate#)<in` `T,` `in` `U>!`)` Returns a composed predicate that represents a short-circuiting logical AND of this predicate and another. |
| open [BiPredicate](https://developer.android.com/reference/kotlin/java/util/function/BiPredicate#)\<T,U\>! | [negate](https://developer.android.com/reference/kotlin/java/util/function/BiPredicate#negate())`()` Returns a predicate that represents the logical negation of this predicate. |
| open [BiPredicate](https://developer.android.com/reference/kotlin/java/util/function/BiPredicate#)\<T,U\>! | [or](https://developer.android.com/reference/kotlin/java/util/function/BiPredicate#or(java.util.function.BiPredicate))`(`other:` ` [BiPredicate](https://developer.android.com/reference/kotlin/java/util/function/BiPredicate#)<in` `T,` `in` `U>!`)` Returns a composed predicate that represents a short-circuiting logical OR of this predicate and another. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [test](https://developer.android.com/reference/kotlin/java/util/function/BiPredicate#test(java.util.function.BiPredicate.T,%20java.util.function.BiPredicate.U))`(`t:` `T`, `u:` `U`)` Evaluates this predicate on the given arguments. |

## Public methods

### and

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun and(other: BiPredicate<in T, in U>!): BiPredicate<T, U>!
```

Returns a composed predicate that represents a short-circuiting logical AND of this predicate and another. When evaluating the composed predicate, if this predicate is`false`, then the`other`predicate is not evaluated.

Any exceptions thrown during evaluation of either predicate are relayed to the caller; if evaluation of this predicate throws an exception, the`other`predicate will not be evaluated.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `other` | [BiPredicate](https://developer.android.com/reference/kotlin/java/util/function/BiPredicate#)\<inT,inU\>!:a predicate that will be logically-ANDed with this predicate |

| Return ||
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [BiPredicate](https://developer.android.com/reference/kotlin/java/util/function/BiPredicate#)<T,` `U>! | a composed predicate that represents the short-circuiting logical AND of this predicate and the`other`predicate |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | if other is null |

### negate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun negate(): BiPredicate<T, U>!
```

Returns a predicate that represents the logical negation of this predicate.

| Return ||
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [BiPredicate](https://developer.android.com/reference/kotlin/java/util/function/BiPredicate#)<T,` `U>! | a predicate that represents the logical negation of this predicate |

### or

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun or(other: BiPredicate<in T, in U>!): BiPredicate<T, U>!
```

Returns a composed predicate that represents a short-circuiting logical OR of this predicate and another. When evaluating the composed predicate, if this predicate is`true`, then the`other`predicate is not evaluated.

Any exceptions thrown during evaluation of either predicate are relayed to the caller; if evaluation of this predicate throws an exception, the`other`predicate will not be evaluated.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `other` | [BiPredicate](https://developer.android.com/reference/kotlin/java/util/function/BiPredicate#)\<inT,inU\>!:a predicate that will be logically-ORed with this predicate |

| Return ||
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [BiPredicate](https://developer.android.com/reference/kotlin/java/util/function/BiPredicate#)<T,` `U>! | a composed predicate that represents the short-circuiting logical OR of this predicate and the`other`predicate |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | if other is null |

### test

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun test(
    t: T, 
    u: U
): Boolean
```

Evaluates this predicate on the given arguments.

| Parameters ||
|-----|-----------------------------|
| `t` | T:the first input argument |
| `u` | U:the second input argument |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the input arguments match the predicate, otherwise`false` |
