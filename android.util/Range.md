Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Range

Kotlin | [Java](https://developer.android.com/reference/android/util/Range "View this page in Java")
| --- | --- |

```
class Range<T : Comparable<T>!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.util.Range](https://developer.android.com/reference/kotlin/android/util/Range#) |

Immutable class for describing the range of two numeric values.

A range (or "interval") defines the inclusive boundaries around a contiguous span of values of some `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#` type; for example, "integers from 1 to 100 inclusive."

All ranges are bounded, and the left side of the range is always `<=` the right side of the range.

Although the implementation itself is immutable, there is no restriction that objects stored must also be immutable. If mutable objects are stored here, then the range effectively becomes mutable.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/util/Range#Range(android.util.Range.T,%20android.util.Range.T)(lower: T, upper: T)` Create a new immutable range. |

| Public methods ||
|---|---|
| T | `https://developer.android.com/reference/kotlin/android/util/Range#clamp(android.util.Range.T)(value: T)` Clamps `value` to this range. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/util/Range#contains(android.util.Range)(range: https://developer.android.com/reference/kotlin/android/util/Range#<T>!)` Checks if another `range` is within the bounds of this range. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/util/Range#contains(android.util.Range.T)(value: T)` Checks if the `value` is within the bounds of this range. |
| --- | --- |
| static [Range](https://developer.android.com/reference/kotlin/android/util/Range#)\<T\>! | `https://developer.android.com/reference/kotlin/android/util/Range#create(android.util.Range.create.T,%20android.util.Range.create.T)(lower: T, upper: T)` Create a new immutable range, with the argument types inferred. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/util/Range#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Compare two ranges for equality. |
| [Range](https://developer.android.com/reference/kotlin/android/util/Range#)\<T\>! | `https://developer.android.com/reference/kotlin/android/util/Range#extend(android.util.Range)(range: https://developer.android.com/reference/kotlin/android/util/Range#<T>!)` Returns the smallest range that includes this range and another `range`. |
| --- | --- |
| [Range](https://developer.android.com/reference/kotlin/android/util/Range#)\<T\>! | `https://developer.android.com/reference/kotlin/android/util/Range#extend(android.util.Range.T)(value: T)` Returns the smallest range that includes this range and the `value`. |
| [Range](https://developer.android.com/reference/kotlin/android/util/Range#)\<T\>! | `https://developer.android.com/reference/kotlin/android/util/Range#extend(android.util.Range.T,%20android.util.Range.T)(lower: T, upper: T)` Returns the smallest range that includes this range and the inclusive range specified by `[lower, upper]`. |
| T | `https://developer.android.com/reference/kotlin/android/util/Range#getLower()()` Get the lower endpoint. |
| --- | --- |
| T | `https://developer.android.com/reference/kotlin/android/util/Range#getUpper()()` Get the upper endpoint. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/Range#hashCode()()` Returns a hash code value for the object. |
| [Range](https://developer.android.com/reference/kotlin/android/util/Range#)\<T\>! | `https://developer.android.com/reference/kotlin/android/util/Range#intersect(android.util.Range)(range: https://developer.android.com/reference/kotlin/android/util/Range#<T>!)` Returns the intersection of this range and another `range`. |
| --- | --- |
| [Range](https://developer.android.com/reference/kotlin/android/util/Range#)\<T\>! | `https://developer.android.com/reference/kotlin/android/util/Range#intersect(android.util.Range.T,%20android.util.Range.T)(lower: T, upper: T)` Returns the intersection of this range and the inclusive range specified by `[lower, upper]`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/util/Range#toString()()` Return the range as a string representation `"[lower, upper]"`. |

## Public constructors

### Range

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Range(
    lower: T, 
    upper: T)
```

Create a new immutable range.

The endpoints are `[lower, upper]`; that is the range is bounded. `lower` must be `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#compareTo(java.lang.Comparable.T)` to `upper`.

| Parameters ||
|---|---|
| `lower` | T: The lower endpoint (inclusive) |
| `upper` | T: The upper endpoint (inclusive) |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `lower` or `upper` is `null` |

## Public methods

### clamp

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun clamp(value: T): T
```

Clamps `value` to this range.

If the value is within this range, it is returned. Otherwise, if it is `<` than the lower endpoint, the lower endpoint is returned, else the upper endpoint is returned. Comparisons are performed using the `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#` interface.

| Parameters ||
|---|---|
| `value` | T: a non-`null` `T` reference |

| Return ||
|---|---|
| `T` | `value` clamped to this range. |

### contains

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun contains(range: Range<T>!): Boolean
```

Checks if another `range` is within the bounds of this range.

A range is considered to be within this range if both of its endpoints are within this range.

| Parameters ||
|---|---|
| `range` | [Range](https://developer.android.com/reference/kotlin/android/util/Range#)\<T\>!: a non-`null` `T` reference |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the range is within this inclusive range, `false` otherwise |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `range` was `null` |

### contains

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun contains(value: T): Boolean
```

Checks if the `value` is within the bounds of this range.

A value is considered to be within this range if it's `>=` the lower endpoint *and* `<=` the upper endpoint (using the `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#` interface.)

| Parameters ||
|---|---|
| `value` | T: a non-`null` `T` reference |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the value is within this inclusive range, `false` otherwise |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `value` was `null` |

### create

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Comparable<T>!> create(
    lower: T, 
    upper: T
): Range<T>!
```

Create a new immutable range, with the argument types inferred.

The endpoints are `[lower, upper]`; that is the range is bounded. `lower` must be `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#compareTo(java.lang.Comparable.T)` to `upper`.

| Parameters ||
|---|---|
| `lower` | T: The lower endpoint (inclusive) |
| `upper` | T: The upper endpoint (inclusive) |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `lower` or `upper` is `null` |

### equals

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Compare two ranges for equality.

A range is considered equal if and only if both the lower and upper endpoints are also equal.

| Parameters ||
|---|---|
| `obj` | This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the ranges are equal, `false` otherwise |

### extend

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun extend(range: Range<T>!): Range<T>!
```

Returns the smallest range that includes this range and another `range`.

E.g. if a `<` b `<` c `<` d, the extension of \[a, c\] and \[b, d\] ranges is \[a, d\]. As the endpoints are object references, there is no guarantee which specific endpoint reference is used from the input ranges:

E.g. if a `==` a' `<` b `<` c, the extension of \[a, b\] and \[a', c\] ranges could be either \[a, c\] or \['a, c\], where \['a, c\] could be either the exact input range, or a newly created range with the same endpoints.

| Parameters ||
|---|---|
| `range` | [Range](https://developer.android.com/reference/kotlin/android/util/Range#)\<T\>!: a non-`null` `Range<T>` reference |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/util/Range#<T>!` | the extension of this range and the other range. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `range` was `null` |

### extend

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun extend(value: T): Range<T>!
```

Returns the smallest range that includes this range and the `value`.

See `https://developer.android.com/reference/kotlin/android/util/Range#extend(android.util.Range)` for more details, as this method is equivalent to `extend(Range.create(value, value))`.

| Parameters ||
|---|---|
| `value` | T: a non-`null` `T` reference |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/util/Range#<T>!` | the extension of this range and the value. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `value` was `null` |

### extend

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun extend(
    lower: T, 
    upper: T
): Range<T>!
```

Returns the smallest range that includes this range and the inclusive range specified by `[lower, upper]`.

See `https://developer.android.com/reference/kotlin/android/util/Range#extend(android.util.Range)` for more details.

| Parameters ||
|---|---|
| `lower` | T: a non-`null` `T` reference |
| `upper` | T: a non-`null` `T` reference |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/util/Range#<T>!` | the extension of this range and the other range. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `lower` or `upper` was `null` |

### getLower

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLower(): T
```

Get the lower endpoint.

| Return ||
|---|---|
| `T` | a non-`null` `T` reference |

### getUpper

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getUpper(): T
```

Get the upper endpoint.

| Return ||
|---|---|
| `T` | a non-`null` `T` reference |

### hashCode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### intersect

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun intersect(range: Range<T>!): Range<T>!
```

Returns the intersection of this range and another `range`.

E.g. if a `<` b `<` c `<` d, the intersection of \[a, c\] and \[b, d\] ranges is \[b, c\]. As the endpoints are object references, there is no guarantee which specific endpoint reference is used from the input ranges:

E.g. if a `==` a' `<` b `<` c, the intersection of \[a, b\] and \[a', c\] ranges could be either \[a, b\] or \['a, b\], where \[a, b\] could be either the exact input range, or a newly created range with the same endpoints.

| Parameters ||
|---|---|
| `range` | [Range](https://developer.android.com/reference/kotlin/android/util/Range#)\<T\>!: a non-`null` `Range<T>` reference |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/util/Range#<T>!` | the intersection of this range and the other range. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the ranges are disjoint. |
| `java.lang.NullPointerException` | if `range` was `null` |

### intersect

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun intersect(
    lower: T, 
    upper: T
): Range<T>!
```

Returns the intersection of this range and the inclusive range specified by `[lower, upper]`.

See `https://developer.android.com/reference/kotlin/android/util/Range#intersect(android.util.Range)` for more details.

| Parameters ||
|---|---|
| `lower` | T: a non-`null` `T` reference |
| `upper` | T: a non-`null` `T` reference |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/util/Range#<T>!` | the intersection of this range and the other range |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the ranges are disjoint. |
| `java.lang.NullPointerException` | if `lower` or `upper` was `null` |

### toString

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Return the range as a string representation `"[lower, upper]"`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | string representation of the range |
