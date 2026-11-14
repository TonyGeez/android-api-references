Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Predicate

```
@FunctionalInterface interface Predicate<T : Any!>
```

| [java.util.function.Predicate](Predicate.md) |

Represents a predicate (boolean-valued function) of one argument.

This is a [functional interface](_package.md) whose functional method is `https://developer.android.com/reference/kotlin/java/util/function/Predicate#test(java.util.function.Predicate.T)`.

## Summary

| Public methods ||
|---|---|
| open [Predicate](Predicate.md)\<T\>! | `https://developer.android.com/reference/kotlin/java/util/function/Predicate#and(java.util.function.Predicate)(other: https://developer.android.com/reference/kotlin/java/util/function/Predicate#<in T>!)` Returns a composed predicate that represents a short-circuiting logical AND of this predicate and another. |
| open static [Predicate](Predicate.md)\<T\>! | `https://developer.android.com/reference/kotlin/java/util/function/Predicate#isEqual(kotlin.Any)(targetRef: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` Returns a predicate that tests if two arguments are equal according to `https://developer.android.com/reference/kotlin/java/util/Objects.html#equals(kotlin.Any,%20kotlin.Any)`. |
| open [Predicate](Predicate.md)\<T\>! | `https://developer.android.com/reference/kotlin/java/util/function/Predicate#negate()()` Returns a predicate that represents the logical negation of this predicate. |
| --- | --- |
| open static [Predicate](Predicate.md)\<T\>! | `https://developer.android.com/reference/kotlin/java/util/function/Predicate#not(java.util.function.Predicate)(target: https://developer.android.com/reference/kotlin/java/util/function/Predicate#<in T>!)` Returns a predicate that is the negation of the supplied predicate. |
| open [Predicate](Predicate.md)\<T\>! | `https://developer.android.com/reference/kotlin/java/util/function/Predicate#or(java.util.function.Predicate)(other: https://developer.android.com/reference/kotlin/java/util/function/Predicate#<in T>!)` Returns a composed predicate that represents a short-circuiting logical OR of this predicate and another. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/function/Predicate#test(java.util.function.Predicate.T)(t: T)` Evaluates this predicate on the given argument. |
| --- | --- |

## Public methods

### and

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun and(other: Predicate<in T>!): Predicate<T>!
```

Returns a composed predicate that represents a short-circuiting logical AND of this predicate and another. When evaluating the composed predicate, if this predicate is `false`, then the `other` predicate is not evaluated.

Any exceptions thrown during evaluation of either predicate are relayed to the caller; if evaluation of this predicate throws an exception, the `other` predicate will not be evaluated.

| Parameters ||
|---|---|
| `other` | [Predicate](Predicate.md)\<in T\>!: a predicate that will be logically-ANDed with this predicate |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/function/Predicate#<T>!` | a composed predicate that represents the short-circuiting logical AND of this predicate and the `other` predicate |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if other is null |

### isEqual

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <T : Any!> isEqual(targetRef: Any!): Predicate<T>!
```

Returns a predicate that tests if two arguments are equal according to `https://developer.android.com/reference/kotlin/java/util/Objects.html#equals(kotlin.Any,%20kotlin.Any)`.

| Parameters ||
|---|---|
| `<T>` | the type of arguments to the predicate |
| `targetRef` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: the object reference with which to compare for equality, which may be `null` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/function/Predicate#<T>!` | a predicate that tests if two arguments are equal according to `https://developer.android.com/reference/kotlin/java/util/Objects.html#equals(kotlin.Any,%20kotlin.Any)` |

### negate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun negate(): Predicate<T>!
```

Returns a predicate that represents the logical negation of this predicate.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/function/Predicate#<T>!` | a predicate that represents the logical negation of this predicate |

### not

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <T : Any!> not(target: Predicate<in T>!): Predicate<T>!
```

Returns a predicate that is the negation of the supplied predicate. This is accomplished by returning result of the calling `target.negate()`.

| Parameters ||
|---|---|
| `<T>` | the type of arguments to the specified predicate |
| `target` | [Predicate](Predicate.md)\<in T\>!: predicate to negate |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/function/Predicate#<T>!` | a predicate that negates the results of the supplied predicate |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if target is null |

### or

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun or(other: Predicate<in T>!): Predicate<T>!
```

Returns a composed predicate that represents a short-circuiting logical OR of this predicate and another. When evaluating the composed predicate, if this predicate is `true`, then the `other` predicate is not evaluated.

Any exceptions thrown during evaluation of either predicate are relayed to the caller; if evaluation of this predicate throws an exception, the `other` predicate will not be evaluated.

| Parameters ||
|---|---|
| `other` | [Predicate](Predicate.md)\<in T\>!: a predicate that will be logically-ORed with this predicate |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/function/Predicate#<T>!` | a composed predicate that represents the short-circuiting logical OR of this predicate and the `other` predicate |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if other is null |

### test

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun test(t: T): Boolean
```

Evaluates this predicate on the given argument.

| Parameters ||
|---|---|
| `t` | T: the input argument |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the input argument matches the predicate, otherwise `false` |
