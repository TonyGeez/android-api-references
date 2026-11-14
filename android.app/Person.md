Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Person

Kotlin | [Java](Person.md)
| --- | --- |

```
class Person : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.Person](Person.md) |

Provides an immutable reference to an entity that appears repeatedly on different surfaces of the platform. For example, this could represent the sender of a message.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/app/Person.Builder` Builder for the immutable `https://developer.android.com/reference/kotlin/android/app/Person#` class. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Person#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/Person#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [Icon](../android.graphics.drawable/Icon.md)? | `https://developer.android.com/reference/kotlin/android/app/Person#getIcon()()` <br /> |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/app/Person#getKey()()` <br /> |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | `https://developer.android.com/reference/kotlin/android/app/Person#getName()()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/app/Person#getUri()()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Person#hashCode()()` Returns a hash code value for the object. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/Person#isBot()()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/Person#isImportant()()` <br /> |
| --- | --- |
| [Person.Builder](../android/app/Person.Builder.md)! | `https://developer.android.com/reference/kotlin/android/app/Person#toBuilder()()` Creates and returns a new `https://developer.android.com/reference/kotlin/android/app/Person.Builder` initialized with this Person's data. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/Person#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [Person](Person.md)!\> | `https://developer.android.com/reference/kotlin/android/app/Person#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public methods

### describeContents

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|---|---|
| `obj` | This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getIcon

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getIcon(): Icon?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#?` | the icon provided for this person or `null` if no icon was provided. |

### getKey

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getKey(): String?
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | the key provided for this person or `null` if no key was provided. |

### getName

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getName(): CharSequence?
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | the name provided for this person or `null` if no name was provided. |

### getUri

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getUri(): String?
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | the uri provided for this person or `null` if no Uri was provided. |

### hashCode

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

### isBot

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isBot(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether this Person is a machine. |

### isImportant

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isImportant(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether this Person is important. |

### toBuilder

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toBuilder(): Person.Builder!
```

Creates and returns a new `https://developer.android.com/reference/kotlin/android/app/Person.Builder` initialized with this Person's data.

### writeToParcel

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android.os/Parcel.md): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<Person!>
```
