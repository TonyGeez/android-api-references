Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Objects

```
class Objects
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.util.Objects](https://developer.android.com/reference/kotlin/java/util/Objects#) |

This class consists of `static` utility methods for operating on objects, or checking certain conditions before operation. These utilities include `null`-safe or `null`-tolerant methods for computing the hash code of an object, returning a string for an object, comparing two objects, and checking if indexes or sub-range values are out of bounds.

## Summary

| Public methods ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Objects#checkFromIndexSize(kotlin.Int,%20kotlin.Int,%20kotlin.Int)(fromIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, size: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, length: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Checks if the sub-range from `fromIndex` (inclusive) to `fromIndex + size` (exclusive) is within the bounds of range from `0` (inclusive) to `length` (exclusive). |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/util/Objects#checkFromIndexSize(kotlin.Long,%20kotlin.Long,%20kotlin.Long)(fromIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, size: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, length: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Checks if the sub-range from `fromIndex` (inclusive) to `fromIndex + size` (exclusive) is within the bounds of range from `0` (inclusive) to `length` (exclusive). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Objects#checkFromToIndex(kotlin.Int,%20kotlin.Int,%20kotlin.Int)(fromIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, toIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, length: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Checks if the sub-range from `fromIndex` (inclusive) to `toIndex` (exclusive) is within the bounds of range from `0` (inclusive) to `length` (exclusive). |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/util/Objects#checkFromToIndex(kotlin.Long,%20kotlin.Long,%20kotlin.Long)(fromIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, toIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, length: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Checks if the sub-range from `fromIndex` (inclusive) to `toIndex` (exclusive) is within the bounds of range from `0` (inclusive) to `length` (exclusive). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Objects#checkIndex(kotlin.Int,%20kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, length: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Checks if the `index` is within the bounds of the range from `0` (inclusive) to `length` (exclusive). |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/util/Objects#checkIndex(kotlin.Long,%20kotlin.Long)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, length: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Checks if the `index` is within the bounds of the range from `0` (inclusive) to `length` (exclusive). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Objects#compare(java.util.Objects.compare.T,%20java.util.Objects.compare.T,%20java.util.Comparator)(a: T, b: T, c: https://developer.android.com/reference/kotlin/java/util/Comparator<in T>)` {@return 0 if the arguments are identical and {@code \* c. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/Objects#deepEquals(kotlin.Any,%20kotlin.Any)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?, b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` {@return {@code true} if the arguments are deeply equal to each other \* and {@code false} otherwise} Two `null` values are deeply equal. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/Objects#equals(kotlin.Any,%20kotlin.Any)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?, b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` {@return {@code true} if the arguments are equal to each other \* and {@code false} otherwise} Consequently, if both arguments are `null`, `true` is returned. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Objects#hash(kotlin.Any)(vararg values: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` {@return a hash code for a sequence of input values} The hash code is generated as if all the input values were placed into an array, and that array were hashed by calling `https://developer.android.com/reference/kotlin/java/util/Arrays#hashCode(kotlin.Array)`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Objects#hashCode(kotlin.Any)(o: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` {@return the hash code of a non-{@code null} argument and 0 for \* a {@code null} argument} |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/Objects#isNull(kotlin.Any)(obj: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` {@return {@code true} if the provided reference is {@code \* null}; {@code false} otherwise} |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/Objects#nonNull(kotlin.Any)(obj: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` {@return {@code true} if the provided reference is non-{@code null}; \* {@code false} otherwise} |
| static T | `https://developer.android.com/reference/kotlin/java/util/Objects#requireNonNull(java.util.Objects.requireNonNull.T)(obj: T?)` Checks that the specified object reference is not `null`. |
| static T | `https://developer.android.com/reference/kotlin/java/util/Objects#requireNonNull(java.util.Objects.requireNonNull.T,%20kotlin.String)(obj: T?, message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Checks that the specified object reference is not `null` and throws a customized `https://developer.android.com/reference/kotlin/java/lang/NullPointerException.html#` if it is. |
| static T | `https://developer.android.com/reference/kotlin/java/util/Objects#requireNonNull(java.util.Objects.requireNonNull.T,%20java.util.function.Supplier)(obj: T?, messageSupplier: https://developer.android.com/reference/kotlin/java/util/function/Supplier<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>)` Checks that the specified object reference is not `null` and throws a customized `https://developer.android.com/reference/kotlin/java/lang/NullPointerException.html#` if it is. |
| static T | `https://developer.android.com/reference/kotlin/java/util/Objects#requireNonNullElse(java.util.Objects.requireNonNullElse.T,%20java.util.Objects.requireNonNullElse.T)(obj: T?, defaultObj: T)` {@return the first argument if it is non-{@code null} and \* otherwise the second argument if it is non-{@code null}} |
| static T | `https://developer.android.com/reference/kotlin/java/util/Objects#requireNonNullElseGet(java.util.Objects.requireNonNullElseGet.T,%20java.util.function.Supplier)(obj: T?, supplier: https://developer.android.com/reference/kotlin/java/util/function/Supplier<out T>)` {@return the first argument if it is non-{@code null} and \* otherwise the value from {@code supplier. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/util/Objects#toIdentityString(kotlin.Any)(o: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)` {@return a string equivalent to the string returned by {@code \* Object. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/util/Objects#toString(kotlin.Any)(o: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` {@return the result of calling {@code toString} for a \* non-{@code null} argument and {@code "null"} for a \* {@code null} argument} |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/util/Objects#toString(kotlin.Any,%20kotlin.String)(o: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?, nullDefault: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` {@return the result of calling {@code toString} on the first \* argument if the first argument is not {@code null} and the \* second argument otherwise} |

## Public methods

### checkFromIndexSize

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun checkFromIndexSize(
    fromIndex: Int, 
    size: Int, 
    length: Int
): Int
```

Checks if the sub-range from `fromIndex` (inclusive) to `fromIndex + size` (exclusive) is within the bounds of range from `0` (inclusive) to `length` (exclusive).

The sub-range is defined to be out of bounds if any of the following inequalities is true:

- `fromIndex < 0`
- `size < 0`
- `fromIndex + size > length`, taking into account integer overflow
- `length < 0`, which is implied from the former inequalities

| Parameters ||
|---|---|
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the lower-bound (inclusive) of the sub-interval |
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the size of the sub-range |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the upper-bound (exclusive) of the range |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `fromIndex` if the sub-range within bounds of the range |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if the sub-range is out of bounds |

### checkFromIndexSize

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun checkFromIndexSize(
    fromIndex: Long, 
    size: Long, 
    length: Long
): Long
```

Checks if the sub-range from `fromIndex` (inclusive) to `fromIndex + size` (exclusive) is within the bounds of range from `0` (inclusive) to `length` (exclusive).

The sub-range is defined to be out of bounds if any of the following inequalities is true:

- `fromIndex < 0`
- `size < 0`
- `fromIndex + size > length`, taking into account integer overflow
- `length < 0`, which is implied from the former inequalities

| Parameters ||
|---|---|
| `fromIndex` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the lower-bound (inclusive) of the sub-interval |
| `size` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the size of the sub-range |
| `length` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the upper-bound (exclusive) of the range |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `fromIndex` if the sub-range within bounds of the range |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if the sub-range is out of bounds |

### checkFromToIndex

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun checkFromToIndex(
    fromIndex: Int, 
    toIndex: Int, 
    length: Int
): Int
```

Checks if the sub-range from `fromIndex` (inclusive) to `toIndex` (exclusive) is within the bounds of range from `0` (inclusive) to `length` (exclusive).

The sub-range is defined to be out of bounds if any of the following inequalities is true:

- `fromIndex < 0`
- `fromIndex > toIndex`
- `toIndex > length`
- `length < 0`, which is implied from the former inequalities

| Parameters ||
|---|---|
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the lower-bound (inclusive) of the sub-range |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the upper-bound (exclusive) of the sub-range |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the upper-bound (exclusive) the range |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `fromIndex` if the sub-range within bounds of the range |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if the sub-range is out of bounds |

### checkFromToIndex

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun checkFromToIndex(
    fromIndex: Long, 
    toIndex: Long, 
    length: Long
): Long
```

Checks if the sub-range from `fromIndex` (inclusive) to `toIndex` (exclusive) is within the bounds of range from `0` (inclusive) to `length` (exclusive).

The sub-range is defined to be out of bounds if any of the following inequalities is true:

- `fromIndex < 0`
- `fromIndex > toIndex`
- `toIndex > length`
- `length < 0`, which is implied from the former inequalities

| Parameters ||
|---|---|
| `fromIndex` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the lower-bound (inclusive) of the sub-range |
| `toIndex` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the upper-bound (exclusive) of the sub-range |
| `length` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the upper-bound (exclusive) the range |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `fromIndex` if the sub-range within bounds of the range |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if the sub-range is out of bounds |

### checkIndex

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun checkIndex(
    index: Int, 
    length: Int
): Int
```

Checks if the `index` is within the bounds of the range from `0` (inclusive) to `length` (exclusive).

The `index` is defined to be out of bounds if any of the following inequalities is true:

- `index < 0`
- `index >= length`
- `length < 0`, which is implied from the former inequalities

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the upper-bound (exclusive) of the range |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `index` if it is within bounds of the range |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if the `index` is out of bounds |

### checkIndex

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun checkIndex(
    index: Long, 
    length: Long
): Long
```

Checks if the `index` is within the bounds of the range from `0` (inclusive) to `length` (exclusive).

The `index` is defined to be out of bounds if any of the following inequalities is true:

- `index < 0`
- `index >= length`
- `length < 0`, which is implied from the former inequalities

| Parameters ||
|---|---|
| `index` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the index |
| `length` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the upper-bound (exclusive) of the range |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `index` if it is within bounds of the range |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if the `index` is out of bounds |

### compare

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> compare(
    a: T, 
    b: T, 
    c: Comparator<in T>
): Int
```

{@return 0 if the arguments are identical and {@code \* c.compare(a, b)} otherwise} Consequently, if both arguments are `null` 0 is returned.

Note that if one of the arguments is `null`, a `NullPointerException` may or may not be thrown depending on what ordering policy, if any, the `https://developer.android.com/reference/kotlin/java/util/Comparator` chooses to have for `null` values.

| Parameters ||
|---|---|
| `<T>` | the type of the objects being compared |
| `a` | T: an object |
| `b` | T: an object to be compared with `a` |
| `c` | [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator)\<in T\>: the `Comparator` to compare the first two arguments |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#`
- `https://developer.android.com/reference/kotlin/java/util/Comparator`

### deepEquals

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun deepEquals(
    a: Any?, 
    b: Any?
): Boolean
```

{@return {@code true} if the arguments are deeply equal to each other \* and {@code false} otherwise} Two `null` values are deeply equal. If both arguments are arrays, the algorithm in `https://developer.android.com/reference/kotlin/java/util/Arrays#deepEquals(kotlin.Array,%20kotlin.Array)` is used to determine equality. Otherwise, equality is determined by using the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method of the first argument.

| Parameters ||
|---|---|
| `a` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: an object |
| `b` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: an object to be compared with `a` for deep equality |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Arrays#deepEquals(kotlin.Array,%20kotlin.Array)`
- `https://developer.android.com/reference/kotlin/java/util/Objects#equals(kotlin.Any,%20kotlin.Any)`

### equals

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun equals(
    a: Any?, 
    b: Any?
): Boolean
```

{@return {@code true} if the arguments are equal to each other \* and {@code false} otherwise} Consequently, if both arguments are `null`, `true` is returned. Otherwise, if the first argument is not `null`, equality is determined by calling the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method of the first argument with the second argument of this method. Otherwise, `false` is returned.

| Parameters ||
|---|---|
| `a` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: an object |
| `b` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: an object to be compared with `a` for equality |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)`

### hash

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun hash(vararg values: Any!): Int
```

{@return a hash code for a sequence of input values} The hash code is generated as if all the input values were placed into an array, and that array were hashed by calling `https://developer.android.com/reference/kotlin/java/util/Arrays#hashCode(kotlin.Array)`.

This method is useful for implementing `https://developer.android.com/reference/kotlin/java/lang/Object.html#hashCode()` on objects containing multiple fields. For example, if an object that has three fields, `x`, `y`, and `z`, one could write:

```kotlin
@Override public int hashCode() {
      return Objects.hash(x, y, z);
  }
  
```
**Warning: When a single object reference is supplied, the returned value does not equal the hash code of that object reference.** This value can be computed by calling `https://developer.android.com/reference/kotlin/java/util/Objects#hashCode(kotlin.Any)`.

| Parameters ||
|---|---|
| `values` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: the values to be hashed |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Arrays#hashCode(kotlin.Array)`

### hashCode

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun hashCode(o: Any?): Int
```

{@return the hash code of a non-{@code null} argument and 0 for \* a {@code null} argument}

| Parameters ||
|---|---|
| `o` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: an object |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Object.html#hashCode()`

### isNull

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isNull(obj: Any?): Boolean
```

{@return {@code true} if the provided reference is {@code \* null}; {@code false} otherwise}

| Parameters ||
|---|---|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: a reference to be checked against `null` |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/function/Predicate`

### nonNull

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun nonNull(obj: Any?): Boolean
```

{@return {@code true} if the provided reference is non-{@code null}; \* {@code false} otherwise}

| Parameters ||
|---|---|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: a reference to be checked against `null` |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/function/Predicate`

### requireNonNull

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> requireNonNull(obj: T?): T
```

Checks that the specified object reference is not `null`. This method is designed primarily for doing parameter validation in methods and constructors, as demonstrated below:

```kotlin
public Foo(Bar bar) {
      this.bar = Objects.requireNonNull(bar);
  }
  
```

<br />

| Parameters ||
|---|---|
| `<T>` | the type of the reference |
| `obj` | T?: the object reference to check for nullity |

| Return ||
|---|---|
| `T` | `obj` if not `null` |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `obj` is `null` |

### requireNonNull

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> requireNonNull(
    obj: T?, 
    message: String
): T
```

Checks that the specified object reference is not `null` and throws a customized `https://developer.android.com/reference/kotlin/java/lang/NullPointerException.html#` if it is. This method is designed primarily for doing parameter validation in methods and constructors with multiple parameters, as demonstrated below:

```kotlin
public Foo(Bar bar, Baz baz) {
      this.bar = Objects.requireNonNull(bar, "bar must not be null");
      this.baz = Objects.requireNonNull(baz, "baz must not be null");
  }
  
```

<br />

| Parameters ||
|---|---|
| `<T>` | the type of the reference |
| `obj` | T?: the object reference to check for nullity |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): detail message to be used in the event that a `NullPointerException` is thrown |

| Return ||
|---|---|
| `T` | `obj` if not `null` |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `obj` is `null` |

### requireNonNull

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> requireNonNull(
    obj: T?, 
    messageSupplier: Supplier<String!>
): T
```

Checks that the specified object reference is not `null` and throws a customized `https://developer.android.com/reference/kotlin/java/lang/NullPointerException.html#` if it is.

Unlike the method `https://developer.android.com/reference/kotlin/java/util/Objects#requireNonNull(java.util.Objects.requireNonNull.T,%20kotlin.String)`, this method allows creation of the message to be deferred until after the null check is made. While this may confer a performance advantage in the non-null case, when deciding to call this method care should be taken that the costs of creating the message supplier are less than the cost of just creating the string message directly.

| Parameters ||
|---|---|
| `<T>` | the type of the reference |
| `obj` | T?: the object reference to check for nullity |
| `messageSupplier` | [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>: supplier of the detail message to be used in the event that a `NullPointerException` is thrown |

| Return ||
|---|---|
| `T` | `obj` if not `null` |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `obj` is `null` |

### requireNonNullElse

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> requireNonNullElse(
    obj: T?, 
    defaultObj: T
): T
```

{@return the first argument if it is non-{@code null} and \* otherwise the second argument if it is non-{@code null}}

| Parameters ||
|---|---|
| `<T>` | the type of the reference |
| `obj` | T?: an object |
| `defaultObj` | T: a non-`null` object to return if the first argument is `null` |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if both `obj` is null and `defaultObj` is `null` |

### requireNonNullElseGet

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> requireNonNullElseGet(
    obj: T?, 
    supplier: Supplier<out T>
): T
```

{@return the first argument if it is non-{@code null} and \* otherwise the value from {@code supplier.get()} if it is \* non-{@code null}}

| Parameters ||
|---|---|
| `<T>` | the type of the first argument and return type |
| `obj` | T?: an object |
| `supplier` | [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier)\<out T\>: of a non-`null` object to return if the first argument is `null` |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if both `obj` is null and either the `supplier` is `null` or the `supplier.get()` value is `null` |

### toIdentityString

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun toIdentityString(o: Any): String
```

{@return a string equivalent to the string returned by {@code \* Object.toString} if that method and {@code hashCode} are not \* overridden}

| Parameters ||
|---|---|
| `o` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html): an object |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the argument is null |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Object.html#toString()`
- `https://developer.android.com/reference/kotlin/java/lang/System.html#identityHashCode(kotlin.Any)`

### toString

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun toString(o: Any?): String
```

{@return the result of calling {@code toString} for a \* non-{@code null} argument and {@code "null"} for a \* {@code null} argument}

| Parameters ||
|---|---|
| `o` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: an object |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Object.html#toString()`
- `https://developer.android.com/reference/kotlin/java/lang/String.html#valueOf(kotlin.Any)`

### toString

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun toString(
    o: Any?, 
    nullDefault: String
): String
```

{@return the result of calling {@code toString} on the first \* argument if the first argument is not {@code null} and the \* second argument otherwise}

| Parameters ||
|---|---|
| `o` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: an object |
| `nullDefault` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): string to return if the first argument is `null` |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Objects#toString(kotlin.Any)`
