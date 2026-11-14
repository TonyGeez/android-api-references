Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PersistableBundle

Kotlin | [Java](PersistableBundle.md)
| --- | --- |

```
class PersistableBundle : BaseBundle, Cloneable, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.os.BaseBundle](BaseBundle.md) ||
| | ↳ | [android.os.PersistableBundle](PersistableBundle.md) |

A mapping from String keys to values of various types. The set of types supported by this class is purposefully restricted to simple objects that can safely be persisted to and restored from disk.

**Warning:** Note that PersistableBundle is a lazy container and as such it does NOT implement equals or hashCode.

## Summary

| Inherited constants ||
|---|---|
| From class Parcelable |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| PersistableBundle Constructs a new, empty PersistableBundle. |
| PersistableBundle Constructs a PersistableBundle containing a copy of the mappings from the given PersistableBundle. |
| PersistableBundle Constructs a new, empty PersistableBundle sized to hold the given number of elements. |

| Public methods ||
|---|---|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | clone Clones the current PersistableBundle. |
| [PersistableBundle](PersistableBundle.md)! | deepCopy Make a deep copy of the given bundle. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Report the nature of this Parcelable's contents |
| --- | --- |
| [PersistableBundle](PersistableBundle.md)? | getPersistableBundle Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | putPersistableBundle Inserts a PersistableBundle value into the mapping of this Bundle, replacing any existing value for the given key. |
| static [PersistableBundle](PersistableBundle.md) | readFromStream Reads a PersistableBundle from an `https://developer.android.com/reference/kotlin/java/io/InputStream.html#`. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of the PersistableBundle that may be suitable for debugging. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Writes the PersistableBundle contents to a Parcel, typically in order for it to be passed through an IBinder connection. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToStream Writes the content of the PersistableBundle to a `https://developer.android.com/reference/kotlin/java/io/OutputStream.html#`. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class BaseBundle |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | clear Removes all elements from the mapping of this Bundle. Recycles the underlying parcel if it is still present. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | containsKey Returns true if the given key is contained in the mapping of this Bundle. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?` | get Returns the entry with the given key as an object. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | getBoolean Returns the value associated with the given key, or false if no mapping of the desired type exists for the given key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | getBoolean Returns the value associated with the given key, or defaultValue if no mapping of the desired type exists for the given key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html?` | getBooleanArray Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | getDouble Returns the value associated with the given key, or 0.0 if no mapping of the desired type exists for the given key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | getDouble Returns the value associated with the given key, or defaultValue if no mapping of the desired type exists for the given key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html?` | getDoubleArray Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getInt Returns the value associated with the given key, or 0 if no mapping of the desired type exists for the given key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getInt Returns the value associated with the given key, or defaultValue if no mapping of the desired type exists for the given key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html?` | getIntArray Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | getLong Returns the value associated with the given key, or 0L if no mapping of the desired type exists for the given key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | getLong Returns the value associated with the given key, or defaultValue if no mapping of the desired type exists for the given key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html?` | getLongArray Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | getString Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | getString Returns the value associated with the given key, or defaultValue if no mapping of the desired type exists for the given key or if a null value is explicitly associated with the given key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?` | getStringArray Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isEmpty Returns true if the mapping of this Bundle is empty, false otherwise. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | keySet Returns a Set containing the Strings used as keys in this Bundle. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | putAll Inserts all mappings from the given PersistableBundle into this BaseBundle. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | putBoolean Inserts a Boolean value into the mapping of this Bundle, replacing any existing value for the given key. Either key or value may be null. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | putBooleanArray Inserts a boolean array value into the mapping of this Bundle, replacing any existing value for the given key. Either key or value may be null. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | putDouble Inserts a double value into the mapping of this Bundle, replacing any existing value for the given key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | putDoubleArray Inserts a double array value into the mapping of this Bundle, replacing any existing value for the given key. Either key or value may be null. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | putInt Inserts an int value into the mapping of this Bundle, replacing any existing value for the given key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | putIntArray Inserts an int array value into the mapping of this Bundle, replacing any existing value for the given key. Either key or value may be null. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | putLong Inserts a long value into the mapping of this Bundle, replacing any existing value for the given key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | putLongArray Inserts a long array value into the mapping of this Bundle, replacing any existing value for the given key. Either key or value may be null. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | putString Inserts a String value into the mapping of this Bundle, replacing any existing value for the given key. Either key or value may be null. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | putStringArray Inserts a String array value into the mapping of this Bundle, replacing any existing value for the given key. Either key or value may be null. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | remove Removes any entry with the given key from the mapping of this Bundle. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | size Returns the number of mappings contained in this Bundle. <br /> | ||

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [PersistableBundle](PersistableBundle.md)!\> | `https://developer.android.com/reference/kotlin/android/os/PersistableBundle#CREATOR:android.os.Parcelable.Creator` <br /> |
| static [PersistableBundle](PersistableBundle.md)! | `https://developer.android.com/reference/kotlin/android/os/PersistableBundle#EMPTY:android.os.PersistableBundle` An unmodifiable `PersistableBundle` that is always isEmpty. |

## Public constructors

### PersistableBundle

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
PersistableBundle()
```

Constructs a new, empty PersistableBundle.

### PersistableBundle

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
PersistableBundle(b: PersistableBundle!)
```

Constructs a PersistableBundle containing a copy of the mappings from the given PersistableBundle. Does only a shallow copy of the original PersistableBundle -- see deepCopy if that is not what you want.

| Parameters ||
|---|---|
| `b` | [PersistableBundle](PersistableBundle.md)!: a PersistableBundle to be copied. |

**See Also**

- deepCopy

### PersistableBundle

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
PersistableBundle(capacity: Int)
```

Constructs a new, empty PersistableBundle sized to hold the given number of elements. The PersistableBundle will grow as needed.

| Parameters ||
|---|---|
| `capacity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the initial capacity of the PersistableBundle |

## Public methods

### clone

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun clone(): Any
```

Clones the current PersistableBundle. The internal map is cloned, but the keys and values to which it refers are copied by reference.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html` | a clone of this instance. |

| Exceptions ||
|---|---|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the `Cloneable` interface. Subclasses that override the `clone` method can also throw this exception to indicate that an instance cannot be cloned. |

### deepCopy

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun deepCopy(): PersistableBundle!
```

Make a deep copy of the given bundle. Traverses into inner containers and copies them as well, so they are not shared across bundles. Will traverse in to Bundle, PersistableBundle, `https://developer.android.com/reference/kotlin/java/util/ArrayList.html#`, and all types of primitive arrays. Other types of objects (such as Parcelable or Serializable) are referenced as-is and not copied in any way.

### describeContents

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Report the nature of this Parcelable's contents

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getPersistableBundle

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPersistableBundle(key: String?): PersistableBundle?
```

Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/PersistableBundle#?` | a Bundle value, or null |

### putPersistableBundle

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun putPersistableBundle(
    key: String?, 
    value: PersistableBundle?
): Unit
```

Inserts a PersistableBundle value into the mapping of this Bundle, replacing any existing value for the given key. Either key or value may be null.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or null |
| `value` | [PersistableBundle](PersistableBundle.md)?: a Bundle object, or null |

### readFromStream

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun readFromStream(inputStream: InputStream): PersistableBundle
```

Reads a PersistableBundle from an `https://developer.android.com/reference/kotlin/java/io/InputStream.html#`.

The stream must be generated by writeToStream.

| Parameters ||
|---|---|
| `inputStream` | [InputStream](../java.io/InputStream.md): This value cannot be `null`. |

| Return ||
|---|---|
| PersistableBundle | This value cannot be `null`. |

**See Also**

- writeToStream

### toString

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the PersistableBundle that may be suitable for debugging. It won't print the internal map if its content hasn't been unparcelled.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    parcel: Parcel, 
    flags: Int
): Unit
```

Writes the PersistableBundle contents to a Parcel, typically in order for it to be passed through an IBinder connection.

| Parameters ||
|---|---|
| `dest` | The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |
| `parcel` | [Parcel](Parcel.md): The parcel to copy this bundle to. |
| --- | --- |

### writeToStream

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToStream(outputStream: OutputStream): Unit
```

Writes the content of the PersistableBundle to a `https://developer.android.com/reference/kotlin/java/io/OutputStream.html#`.

The content can be read by a readFromStream.

| Parameters ||
|---|---|
| `outputStream` | [OutputStream](../java.io/OutputStream.md): This value cannot be `null`. |

**See Also**

- readFromStream

## Properties

### CREATOR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<PersistableBundle!>
```

### EMPTY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EMPTY: PersistableBundle!
```

An unmodifiable `PersistableBundle` that is always isEmpty.
