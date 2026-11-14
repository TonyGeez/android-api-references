Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Record

```
abstract class Record
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.lang.Record](Record.md) |

This is the common base class of all Java language record classes.

More information about records, including descriptions of the implicitly declared methods synthesized by the compiler, can be found in section 8.10 of The Java Language Specification.

A *record class* is a shallowly immutable, transparent carrier for a fixed set of values, called the *record components* . The Java language provides concise syntax for declaring record classes, whereby the record components are declared in the record header. The list of record components declared in the record header form the *record descriptor*.

A record class has the following mandated members: a *canonical constructor*, which must provide at least as much access as the record class and whose descriptor is the same as the record descriptor; a private final field corresponding to each component, whose name and type are the same as that of the component; a public accessor method corresponding to each component, whose name and return type are the same as that of the component. If not explicitly declared in the body of the record, implicit implementations for these members are provided.

The implicit declaration of the canonical constructor has the same accessibility as the record class and initializes the component fields from the corresponding constructor arguments. The implicit declaration of the accessor methods returns the value of the corresponding component field. The implicit declaration of the `https://developer.android.com/reference/kotlin/java/lang/Object#equals(kotlin.Any)`, `https://developer.android.com/reference/kotlin/java/lang/Object#hashCode()`, and `https://developer.android.com/reference/kotlin/java/lang/Object#toString()` methods are derived from all of the component fields.

The primary reasons to provide an explicit declaration for the canonical constructor or accessor methods are to validate constructor arguments, perform defensive copies on mutable components, or normalize groups of components (such as reducing a rational number to lowest terms.)

For all record classes, the following invariant must hold: if a record R's components are `c1, c2, ... cn`, then if a record instance is copied as follows:

```kotlin
R copy = new R(r.c1(), r.c2(), ..., r.cn());
  
```
then it must be the case that `r.equals(copy)`.

## Summary

| Protected constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/Record#Record()()` Constructor for record classes to call. |

| Public methods ||
|---|---|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Record#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Record#hashCode()()` Returns a hash code value for the record. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Record#toString()()` Returns a string representation of the record. |
| --- | --- |

## Protected constructors

### Record

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected Record()
```

Constructor for record classes to call.

## Public methods

### equals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one. In addition to the general contract of `https://developer.android.com/reference/kotlin/java/lang/Object#equals(kotlin.Any)`, record classes must further obey the invariant that when a record instance is "copied" by passing the result of the record component accessor methods to the canonical constructor, as follows:

```kotlin
R copy = new R(r.c1(), r.c2(), ..., r.cn());
  
```
then it must be the case that `r.equals(copy)`.

<br />

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this record is equal to the argument; `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Objects.html#equals(kotlin.Any,%20kotlin.Any)`

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun hashCode(): Int
```

Returns a hash code value for the record. Obeys the general contract of `https://developer.android.com/reference/kotlin/java/lang/Object#hashCode()`. For records, hashing behavior is constrained by the refined contract of `https://developer.android.com/reference/kotlin/java/lang/Record#equals(kotlin.Any)`, so that any two records created from the same components must have the same hash code.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this record. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Object#hashCode()`

### toString

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun toString(): String
```

Returns a string representation of the record. In accordance with the general contract of `https://developer.android.com/reference/kotlin/java/lang/Object#toString()`, the `toString` method returns a string that "textually represents" this record. The result should be a concise but informative representation that is easy for a person to read.

In addition to this general contract, record classes must further participate in the invariant that any two records which are [equal](Record.md)) must produce equal strings. This invariant is necessarily relaxed in the rare case where corresponding equal component values might fail to produce equal strings for themselves.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Object#toString()`
