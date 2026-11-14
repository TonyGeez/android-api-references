Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Boolean

```
class Boolean : Comparable<Boolean!>, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.lang.Boolean](Boolean.md) |

The Boolean class wraps a value of the primitive type `boolean` in an object. An object of type `Boolean` contains a single field whose type is `boolean`.

In addition, this class provides many methods for converting a `boolean` to a `String` and a `String` to a `boolean`, as well as other constants and methods useful when dealing with a `boolean`.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/Boolean#Boolean(kotlin.Boolean)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Allocates a `Boolean` object representing the `value` argument. |
| `https://developer.android.com/reference/kotlin/java/lang/Boolean#Boolean(kotlin.String)(s: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Allocates a `Boolean` object representing the value `true` if the string argument is not `null` and is equal, ignoring case, to the string `"true"`. |

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Boolean#booleanValue()()` Returns the value of this `Boolean` object as a boolean primitive. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Boolean#compare(kotlin.Boolean,%20kotlin.Boolean)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Compares two `boolean` values. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Boolean#compareTo(kotlin.Boolean)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Compares this `Boolean` instance with another. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Boolean#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Returns `true` if and only if the argument is not `null` and is a `Boolean` object that represents the same `boolean` value as this object. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Boolean#getBoolean(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns `true` if and only if the system property named by the argument exists and is equal to, ignoring case, the string `"true"`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Boolean#hashCode()()` Returns a hash code for this `Boolean` object. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Boolean#hashCode(kotlin.Boolean)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Returns a hash code for a `boolean` value; compatible with `Boolean.hashCode()`. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Boolean#logicalAnd(kotlin.Boolean,%20kotlin.Boolean)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Returns the result of applying the logical AND operator to the specified `boolean` operands. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Boolean#logicalOr(kotlin.Boolean,%20kotlin.Boolean)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Returns the result of applying the logical OR operator to the specified `boolean` operands. |
| --- | --- |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Boolean#logicalXor(kotlin.Boolean,%20kotlin.Boolean)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Returns the result of applying the logical XOR operator to the specified `boolean` operands. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Boolean#parseBoolean(kotlin.String)(s: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Parses the string argument as a boolean. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Boolean#toString()()` Returns a `String` object representing this Boolean's value. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Boolean#toString(kotlin.Boolean)(b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Returns a `String` object representing the specified boolean. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Boolean#valueOf(kotlin.Boolean)(b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Returns a `Boolean` instance representing the specified `boolean` value. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Boolean#valueOf(kotlin.String)(s: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Returns a `Boolean` with a value represented by the specified string. |
| --- | --- |

| Properties ||
|---|---|
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)! | `https://developer.android.com/reference/kotlin/java/lang/Boolean#FALSE:kotlin.Boolean` The `Boolean` object corresponding to the primitive value `false`. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)! | `https://developer.android.com/reference/kotlin/java/lang/Boolean#TRUE:kotlin.Boolean` The `Boolean` object corresponding to the primitive value `true`. |
| static [Class](Class.md)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\>! | `https://developer.android.com/reference/kotlin/java/lang/Boolean#TYPE:java.lang.Class` The Class object representing the primitive type boolean. |
| --- | --- |

## Public constructors

### Boolean

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Boolean(value: Boolean)
```

**Deprecated:** *It is rarely appropriate to use this constructor. The static factory `https://developer.android.com/reference/kotlin/java/lang/Boolean#valueOf(kotlin.Boolean)` is generally a better choice, as it is likely to yield significantly better space and time performance. Also consider using the final fields `https://developer.android.com/reference/kotlin/java/lang/Boolean#TRUE:kotlin.Boolean` and `https://developer.android.com/reference/kotlin/java/lang/Boolean#FALSE:kotlin.Boolean` if possible.*

Allocates a `Boolean` object representing the `value` argument.

| Parameters ||
|---|---|
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): the value of the `Boolean`. |

### Boolean

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Boolean(s: String?)
```

**Deprecated:** *It is rarely appropriate to use this constructor. Use `https://developer.android.com/reference/kotlin/java/lang/Boolean#parseBoolean(kotlin.String)` to convert a string to a `boolean` primitive, or use `https://developer.android.com/reference/kotlin/java/lang/Boolean#valueOf(kotlin.String)` to convert a string to a `Boolean` object.*

Allocates a `Boolean` object representing the value `true` if the string argument is not `null` and is equal, ignoring case, to the string `"true"`. Otherwise, allocates a `Boolean` object representing the value `false`.

| Parameters ||
|---|---|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: the string to be converted to a `Boolean`. |

## Public methods

### booleanValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun booleanValue(): Boolean
```

Returns the value of this `Boolean` object as a boolean primitive.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | the primitive `boolean` value of this object. |

### compare

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun compare(
    x: Boolean, 
    y: Boolean
): Int
```

Compares two `boolean` values. The value returned is identical to what would be returned by:

```kotlin
Boolean.valueOf(x).compareTo(Boolean.valueOf(y))
  
```

<br />

| Parameters ||
|---|---|
| `x` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): the first `boolean` to compare |
| `y` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): the second `boolean` to compare |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value `0` if `x == y`; a value less than `0` if `!x && y`; and a value greater than `0` if `x && !y` |

### compareTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun compareTo(other: Boolean): Int
```

Compares this `Boolean` instance with another.

| Parameters ||
|---|---|
| `o` | the object to be compared. |
| `b` | the `Boolean` instance to be compared |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | zero if this object represents the same boolean value as the argument; a positive value if this object represents true and the argument represents false; and a negative value if this object represents false and the argument represents true |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |
| `java.lang.NullPointerException` | if the argument is `null` |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Comparable`

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Returns `true` if and only if the argument is not `null` and is a `Boolean` object that represents the same `boolean` value as this object.

| Parameters ||
|---|---|
| `obj` | the object to compare with. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the Boolean objects represent the same value; `false` otherwise. |

### getBoolean

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getBoolean(name: String): Boolean
```

Returns `true` if and only if the system property named by the argument exists and is equal to, ignoring case, the string `"true"`. A system property is accessible through `getProperty`, a method defined by the `System` class.

If there is no property with the specified name, or if the specified name is empty or null, then `false` is returned.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the system property name. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | the `boolean` value of the system property. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | for the same reasons as `https://developer.android.com/reference/kotlin/java/lang/System#getProperty(kotlin.String)` |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/System#getProperty(kotlin.String)`
- `https://developer.android.com/reference/kotlin/java/lang/System#getProperty(kotlin.String,%20kotlin.String)`

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code for this `Boolean` object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the integer `1231` if this object represents `true`; returns the integer `1237` if this object represents `false`. |

### hashCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun hashCode(value: Boolean): Int
```

Returns a hash code for a `boolean` value; compatible with `Boolean.hashCode()`.

| Parameters ||
|---|---|
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): the value to hash |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for a `boolean` value. |

### logicalAnd

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun logicalAnd(
    a: Boolean, 
    b: Boolean
): Boolean
```

Returns the result of applying the logical AND operator to the specified `boolean` operands.

| Parameters ||
|---|---|
| `a` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): the first operand |
| `b` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): the second operand |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | the logical AND of `a` and `b` |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator.html#`

### logicalOr

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun logicalOr(
    a: Boolean, 
    b: Boolean
): Boolean
```

Returns the result of applying the logical OR operator to the specified `boolean` operands.

| Parameters ||
|---|---|
| `a` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): the first operand |
| `b` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): the second operand |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | the logical OR of `a` and `b` |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator.html#`

### logicalXor

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun logicalXor(
    a: Boolean, 
    b: Boolean
): Boolean
```

Returns the result of applying the logical XOR operator to the specified `boolean` operands.

| Parameters ||
|---|---|
| `a` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): the first operand |
| `b` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): the second operand |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | the logical XOR of `a` and `b` |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator.html#`

### parseBoolean

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun parseBoolean(s: String?): Boolean
```

Parses the string argument as a boolean. The `boolean` returned represents the value `true` if the string argument is not `null` and is equal, ignoring case, to the string `"true"`. Otherwise, a false value is returned, including for a null argument.

Example: `Boolean.parseBoolean("True")` returns `true`. 
Example: `Boolean.parseBoolean("yes")` returns `false`.

| Parameters ||
|---|---|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: the `String` containing the boolean representation to be parsed |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | the boolean represented by the string argument |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a `String` object representing this Boolean's value. If this object represents the value `true`, a string equal to `"true"` is returned. Otherwise, a string equal to `"false"` is returned.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of this object. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun toString(b: Boolean): String
```

Returns a `String` object representing the specified boolean. If the specified boolean is `true`, then the string `"true"` will be returned, otherwise the string `"false"` will be returned.

| Parameters ||
|---|---|
| `b` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): the boolean to be converted |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | the string representation of the specified `boolean` |

### valueOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun valueOf(b: Boolean): Boolean
```

Returns a `Boolean` instance representing the specified `boolean` value. If the specified `boolean` value is `true`, this method returns `Boolean.TRUE`; if it is `false`, this method returns `Boolean.FALSE`. If a new `Boolean` instance is not required, this method should generally be used in preference to the constructor `https://developer.android.com/reference/kotlin/java/lang/Boolean#Boolean(kotlin.Boolean)`, as this method is likely to yield significantly better space and time performance.

| Parameters ||
|---|---|
| `b` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): a boolean value. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | a `Boolean` instance representing `b`. |

### valueOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun valueOf(s: String?): Boolean
```

Returns a `Boolean` with a value represented by the specified string. The `Boolean` returned represents a true value if the string argument is not `null` and is equal, ignoring case, to the string `"true"`. Otherwise, a false value is returned, including for a null argument.

| Parameters ||
|---|---|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a string. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | the `Boolean` value represented by the string. |

## Properties

### FALSE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FALSE: Boolean!
```

The `Boolean` object corresponding to the primitive value `false`.

### TRUE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRUE: Boolean!
```

The `Boolean` object corresponding to the primitive value `true`.

### TYPE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE: Class<Boolean!>!
```

The Class object representing the primitive type boolean.
