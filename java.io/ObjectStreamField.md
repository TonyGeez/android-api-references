Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ObjectStreamField

```
open class ObjectStreamField : Comparable<Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.io.ObjectStreamField](ObjectStreamField.md) |

A description of a Serializable field from a Serializable class. An array of ObjectStreamFields is used to declare the Serializable fields of a class.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/ObjectStreamField#ObjectStreamField(kotlin.String,%20java.lang.Class)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, type: https://developer.android.com/reference/kotlin/java/lang/Class.html#<*>!)` Create a Serializable field with the specified type. |
| `https://developer.android.com/reference/kotlin/java/io/ObjectStreamField#ObjectStreamField(kotlin.String,%20java.lang.Class,%20kotlin.Boolean)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, type: https://developer.android.com/reference/kotlin/java/lang/Class.html#<*>!, unshared: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Creates an ObjectStreamField representing a serializable field with the given name and type. |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/io/ObjectStreamField#compareTo(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` Compare this field with another `ObjectStreamField`. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/io/ObjectStreamField#getName()()` Get the name of this field. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/io/ObjectStreamField#getOffset()()` Offset of field within instance data. |
| --- | --- |
| open [Class](../java.lang/Class.md)\<\*\>! | `https://developer.android.com/reference/kotlin/java/io/ObjectStreamField#getType()()` Get the type of the field. |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | `https://developer.android.com/reference/kotlin/java/io/ObjectStreamField#getTypeCode()()` Returns character encoding of field type. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/io/ObjectStreamField#getTypeString()()` Return the JVM type signature. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/io/ObjectStreamField#isPrimitive()()` Return true if this field has a primitive type. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/io/ObjectStreamField#isUnshared()()` Returns boolean value indicating whether or not the serializable field represented by this ObjectStreamField instance is unshared. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/io/ObjectStreamField#toString()()` Return a string that describes this field. |
| --- | --- |

| Protected methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/ObjectStreamField#setOffset(kotlin.Int)(offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Offset within instance data. |

## Public constructors

### ObjectStreamField

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ObjectStreamField(
    name: String!, 
    type: Class<*>!)
```

Create a Serializable field with the specified type. This field should be documented with a `serialField` tag.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the name of the serializable field |
| `type` | [Class](../java.lang/Class.md)\<\*\>!: the `Class` object of the serializable field |

### ObjectStreamField

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ObjectStreamField(
    name: String!, 
    type: Class<*>!, 
    unshared: Boolean)
```

Creates an ObjectStreamField representing a serializable field with the given name and type. If unshared is false, values of the represented field are serialized and deserialized in the default manner--if the field is non-primitive, object values are serialized and deserialized as if they had been written and read by calls to writeObject and readObject. If unshared is true, values of the represented field are serialized and deserialized as if they had been written and read by calls to writeUnshared and readUnshared.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: field name |
| `type` | [Class](../java.lang/Class.md)\<\*\>!: field type |
| `unshared` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): if false, write/read field values in the same manner as writeObject/readObject; if true, write/read in the same manner as writeUnshared/readUnshared |
| --- | --- |

## Public methods

### compareTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun compareTo(other: Any!): Int
```

Compare this field with another `ObjectStreamField`. Return -1 if this is smaller, 0 if equal, 1 if greater. Types that are primitives are "smaller" than object types. If equal, the field names are compared.

| Parameters ||
|---|---|
| `o` | the object to be compared. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a negative integer, zero, or a positive integer as this object is less than, equal to, or greater than the specified object. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |
| `java.lang.NullPointerException` | if the specified object is null |

### getName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getName(): String!
```

Get the name of this field.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | a `String` representing the name of the serializable field |

### getOffset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOffset(): Int
```

Offset of field within instance data.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the offset of this field |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/ObjectStreamField#setOffset(kotlin.Int)`

### getType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getType(): Class<*>!
```

Get the type of the field. If the type is non-primitive and this `ObjectStreamField` was obtained from a deserialized `https://developer.android.com/reference/kotlin/java/io/ObjectStreamClass` instance, then `Object.class` is returned. Otherwise, the `Class` object for the type of the field is returned.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/Class.html#<*>!` | a `Class` object representing the type of the serializable field |

### getTypeCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTypeCode(): Char
```

Returns character encoding of field type. The encoding is as follows:

```kotlin
B            byte
  C            char
  D            double
  F            float
  I            int
  J            long
  L            class or interface
  S            short
  Z            boolean
  [            array
  
```

<br />

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html` | the typecode of the serializable field |

### getTypeString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTypeString(): String!
```

Return the JVM type signature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | null if this field has a primitive type. |

### isPrimitive

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isPrimitive(): Boolean
```

Return true if this field has a primitive type.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if and only if this field corresponds to a primitive type |

### isUnshared

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isUnshared(): Boolean
```

Returns boolean value indicating whether or not the serializable field represented by this ObjectStreamField instance is unshared.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this field is unshared |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Return a string that describes this field.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

## Protected methods

### setOffset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun setOffset(offset: Int): Unit
```

Offset within instance data.

| Parameters ||
|---|---|
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the offset of the field |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/ObjectStreamField#getOffset()`
