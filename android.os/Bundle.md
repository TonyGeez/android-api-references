Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Bundle

```
class Bundle : BaseBundle, Cloneable, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.os.BaseBundle](https://developer.android.com/reference/kotlin/android/os/BaseBundle) ||
| | ↳ | [android.os.Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle#) |

A mapping from String keys to various `https://developer.android.com/reference/kotlin/android/os/Parcelable` values.

**Warning:** Note that `https://developer.android.com/reference/kotlin/android/os/Bundle#` is a lazy container and as such it does NOT implement `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` or `https://developer.android.com/reference/kotlin/java/lang/Object.html#hashCode()`.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle#Bundle()()` <br /> |
| `https://developer.android.com/reference/kotlin/android/os/Bundle#Bundle(android.os.Bundle)(b: https://developer.android.com/reference/kotlin/android/os/Bundle#!)` Constructs a Bundle containing a copy of the mappings from the given Bundle. |
| `https://developer.android.com/reference/kotlin/android/os/Bundle#Bundle(android.os.PersistableBundle)(b: https://developer.android.com/reference/kotlin/android/os/PersistableBundle!)` Constructs a Bundle containing a copy of the mappings from the given PersistableBundle. |
| `https://developer.android.com/reference/kotlin/android/os/Bundle#Bundle(kotlin.Int)(capacity: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Constructs a new, empty Bundle sized to hold the given number of elements. |
| `https://developer.android.com/reference/kotlin/android/os/Bundle#Bundle(java.lang.ClassLoader)(loader: https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#!)` Constructs a new, empty Bundle that uses a specific ClassLoader for instantiating Parcelable and Serializable objects. |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/Bundle#clear()()` Removes all elements from the mapping of this Bundle. |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | `https://developer.android.com/reference/kotlin/android/os/Bundle#clone()()` Clones the current Bundle. |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle#)! | `https://developer.android.com/reference/kotlin/android/os/Bundle#deepCopy()()` Make a deep copy of the given bundle. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Bundle#describeContents()()` Report the nature of this Parcelable's contents |
| [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder)? | `https://developer.android.com/reference/kotlin/android/os/Bundle#getBinder(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key. |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle#)? | `https://developer.android.com/reference/kotlin/android/os/Bundle#getBundle(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key. |
| --- | --- |
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/android/os/Bundle#getByte(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns the value associated with the given key, or (byte) 0 if no mapping of the desired type exists for the given key. |
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)! | `https://developer.android.com/reference/kotlin/android/os/Bundle#getByte(kotlin.String,%20kotlin.Byte)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, defaultValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)` Returns the value associated with the given key, or defaultValue if no mapping of the desired type exists for the given key. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | `https://developer.android.com/reference/kotlin/android/os/Bundle#getByteArray(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key. |
| --- | --- |
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | `https://developer.android.com/reference/kotlin/android/os/Bundle#getChar(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns the value associated with the given key, or (char) 0 if no mapping of the desired type exists for the given key. |
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | `https://developer.android.com/reference/kotlin/android/os/Bundle#getChar(kotlin.String,%20kotlin.Char)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, defaultValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Returns the value associated with the given key, or defaultValue if no mapping of the desired type exists for the given key. |
| [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)? | `https://developer.android.com/reference/kotlin/android/os/Bundle#getCharArray(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key. |
| --- | --- |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | `https://developer.android.com/reference/kotlin/android/os/Bundle#getCharSequence(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | `https://developer.android.com/reference/kotlin/android/os/Bundle#getCharSequence(kotlin.String,%20kotlin.CharSequence)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, defaultValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!)` Returns the value associated with the given key, or defaultValue if no mapping of the desired type exists for the given key or if a null value is explicitly associatd with the given key. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!\>? | `https://developer.android.com/reference/kotlin/android/os/Bundle#getCharSequenceArray(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key. |
| --- | --- |
| [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)\< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!\>? | `https://developer.android.com/reference/kotlin/android/os/Bundle#getCharSequenceArrayList(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key. |
| [ClassLoader](https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#)! | `https://developer.android.com/reference/kotlin/android/os/Bundle#getClassLoader()()` Return the ClassLoader currently associated with this Bundle. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/os/Bundle#getFloat(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns the value associated with the given key, or 0. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/os/Bundle#getFloat(kotlin.String,%20kotlin.Float)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, defaultValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Returns the value associated with the given key, or defaultValue if no mapping of the desired type exists for the given key. |
| [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)? | `https://developer.android.com/reference/kotlin/android/os/Bundle#getFloatArray(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key. |
| [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>? | `https://developer.android.com/reference/kotlin/android/os/Bundle#getIntegerArrayList(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key. |
| --- | --- |
| T? | `https://developer.android.com/reference/kotlin/android/os/Bundle#getParcelable(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Returns the value associated with the given key, or `null` if no mapping of the desired type exists for the given key or a `null` value is explicitly associated with the key. |
| T? | `https://developer.android.com/reference/kotlin/android/os/Bundle#getParcelable(kotlin.String,%20java.lang.Class)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, clazz: https://developer.android.com/reference/kotlin/java/lang/Class.html#<T>)` Returns the value associated with the given key or `null` if: - No mapping of the desired type exists for the given key. - A `null` value is explicitly associated with the key. - The object is not of type `clazz`. <br /> |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable)!\>? | `https://developer.android.com/reference/kotlin/android/os/Bundle#getParcelableArray(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Returns the value associated with the given key, or `null` if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key. |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>? | `https://developer.android.com/reference/kotlin/android/os/Bundle#getParcelableArray(kotlin.String,%20java.lang.Class)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, clazz: https://developer.android.com/reference/kotlin/java/lang/Class.html#<T>)` Returns the value associated with the given key, or `null` if: - No mapping of the desired type exists for the given key. - A `null` value is explicitly associated with the key. - The object is not of type `clazz`. <br /> |
| [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)\<T\>? | `https://developer.android.com/reference/kotlin/android/os/Bundle#getParcelableArrayList(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Returns the value associated with the given key, or `null` if no mapping of the desired type exists for the given key or a `null` value is explicitly associated with the key. |
| [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)\<T\>? | `https://developer.android.com/reference/kotlin/android/os/Bundle#getParcelableArrayList(kotlin.String,%20java.lang.Class)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, clazz: https://developer.android.com/reference/kotlin/java/lang/Class.html#<out T>)` Returns the value associated with the given key, or `null` if: - No mapping of the desired type exists for the given key. - A `null` value is explicitly associated with the key. - The object is not of type `clazz`. <br /> |
| --- | --- |
| [Serializable](https://developer.android.com/reference/kotlin/java/io/Serializable.html#)? | `https://developer.android.com/reference/kotlin/android/os/Bundle#getSerializable(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key. |
| T? | `https://developer.android.com/reference/kotlin/android/os/Bundle#getSerializable(kotlin.String,%20java.lang.Class)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, clazz: https://developer.android.com/reference/kotlin/java/lang/Class.html#<T>)` Returns the value associated with the given key, or `null` if: - No mapping of the desired type exists for the given key. - A `null` value is explicitly associated with the key. - The object is not of type `clazz`. <br /> |
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | `https://developer.android.com/reference/kotlin/android/os/Bundle#getShort(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns the value associated with the given key, or (short) 0 if no mapping of the desired type exists for the given key. |
| --- | --- |
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | `https://developer.android.com/reference/kotlin/android/os/Bundle#getShort(kotlin.String,%20kotlin.Short)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, defaultValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)` Returns the value associated with the given key, or defaultValue if no mapping of the desired type exists for the given key. |
| [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html)? | `https://developer.android.com/reference/kotlin/android/os/Bundle#getShortArray(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key. |
| [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#)? | `https://developer.android.com/reference/kotlin/android/os/Bundle#getSize(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key. |
| --- | --- |
| [SizeF](https://developer.android.com/reference/kotlin/android/util/SizeF.html#)? | `https://developer.android.com/reference/kotlin/android/os/Bundle#getSizeF(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key. |
| [SparseArray](https://developer.android.com/reference/kotlin/android/util/SparseArray.html#)\<T\>? | `https://developer.android.com/reference/kotlin/android/os/Bundle#getSparseParcelableArray(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key. |
| [SparseArray](https://developer.android.com/reference/kotlin/android/util/SparseArray.html#)\<T\>? | `https://developer.android.com/reference/kotlin/android/os/Bundle#getSparseParcelableArray(kotlin.String,%20java.lang.Class)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, clazz: https://developer.android.com/reference/kotlin/java/lang/Class.html#<out T>)` Returns the value associated with the given key, or `null` if: - No mapping of the desired type exists for the given key. - A `null` value is explicitly associated with the key. - The object is not of type `clazz`. <br /> |
| --- | --- |
| [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | `https://developer.android.com/reference/kotlin/android/os/Bundle#getStringArrayList(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/Bundle#hasFileDescriptors()()` Reports whether the bundle contains any parcelled file descriptors. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/Bundle#putAll(android.os.Bundle)(bundle: https://developer.android.com/reference/kotlin/android/os/Bundle#!)` Inserts all mappings from the given Bundle into this Bundle. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/Bundle#putBinder(kotlin.String,%20android.os.IBinder)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, value: https://developer.android.com/reference/kotlin/android/os/IBinder?)` Inserts an `https://developer.android.com/reference/kotlin/android/os/IBinder` value into the mapping of this Bundle, replacing any existing value for the given key. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/Bundle#putBundle(kotlin.String,%20android.os.Bundle)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, value: https://developer.android.com/reference/kotlin/android/os/Bundle#?)` Inserts a Bundle value into the mapping of this Bundle, replacing any existing value for the given key. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/Bundle#putByte(kotlin.String,%20kotlin.Byte)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)` Inserts a byte value into the mapping of this Bundle, replacing any existing value for the given key. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/Bundle#putByteArray(kotlin.String,%20kotlin.ByteArray)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html?)` Inserts a byte array value into the mapping of this Bundle, replacing any existing value for the given key. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/Bundle#putChar(kotlin.String,%20kotlin.Char)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Inserts a char value into the mapping of this Bundle, replacing any existing value for the given key. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/Bundle#putCharArray(kotlin.String,%20kotlin.CharArray)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html?)` Inserts a char array value into the mapping of this Bundle, replacing any existing value for the given key. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/Bundle#putCharSequence(kotlin.String,%20kotlin.CharSequence)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?)` Inserts a CharSequence value into the mapping of this Bundle, replacing any existing value for the given key. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/Bundle#putCharSequenceArray(kotlin.String,%20kotlin.Array)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!>?)` Inserts a CharSequence array value into the mapping of this Bundle, replacing any existing value for the given key. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/Bundle#putCharSequenceArrayList(kotlin.String,%20java.util.ArrayList)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, value: https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!>?)` Inserts an ArrayList value into the mapping of this Bundle, replacing any existing value for the given key. Either key or value may be null. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/Bundle#putFloat(kotlin.String,%20kotlin.Float)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Inserts a float value into the mapping of this Bundle, replacing any existing value for the given key. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/Bundle#putFloatArray(kotlin.String,%20kotlin.FloatArray)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html?)` Inserts a float array value into the mapping of this Bundle, replacing any existing value for the given key. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/Bundle#putIntegerArrayList(kotlin.String,%20java.util.ArrayList)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, value: https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>?)` Inserts an ArrayList value into the mapping of this Bundle, replacing any existing value for the given key. Either key or value may be null. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/Bundle#putParcelable(kotlin.String,%20android.os.Parcelable)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, value: https://developer.android.com/reference/kotlin/android/os/Parcelable?)` Inserts a Parcelable value into the mapping of this Bundle, replacing any existing value for the given key. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/Bundle#putParcelableArray(kotlin.String,%20kotlin.Array)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/os/Parcelable!>?)` Inserts an array of Parcelable values into the mapping of this Bundle, replacing any existing value for the given key. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/Bundle#putParcelableArrayList(kotlin.String,%20java.util.ArrayList)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, value: https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<out https://developer.android.com/reference/kotlin/android/os/Parcelable!>?)` Inserts a List of Parcelable values into the mapping of this Bundle, replacing any existing value for the given key. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/Bundle#putSerializable(kotlin.String,%20java.io.Serializable)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, value: https://developer.android.com/reference/kotlin/java/io/Serializable.html#?)` Inserts a Serializable value into the mapping of this Bundle, replacing any existing value for the given key. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/Bundle#putShort(kotlin.String,%20kotlin.Short)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)` Inserts a short value into the mapping of this Bundle, replacing any existing value for the given key. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/Bundle#putShortArray(kotlin.String,%20kotlin.ShortArray)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html?)` Inserts a short array value into the mapping of this Bundle, replacing any existing value for the given key. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/Bundle#putSize(kotlin.String,%20android.util.Size)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, value: https://developer.android.com/reference/kotlin/android/util/Size.html#?)` Inserts a Size value into the mapping of this Bundle, replacing any existing value for the given key. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/Bundle#putSizeF(kotlin.String,%20android.util.SizeF)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, value: https://developer.android.com/reference/kotlin/android/util/SizeF.html#?)` Inserts a SizeF value into the mapping of this Bundle, replacing any existing value for the given key. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/Bundle#putSparseParcelableArray(kotlin.String,%20android.util.SparseArray)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, value: https://developer.android.com/reference/kotlin/android/util/SparseArray.html#<out https://developer.android.com/reference/kotlin/android/os/Parcelable!>?)` Inserts a SparceArray of Parcelable values into the mapping of this Bundle, replacing any existing value for the given key. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/Bundle#putStringArrayList(kotlin.String,%20java.util.ArrayList)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, value: https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?)` Inserts an ArrayList value into the mapping of this Bundle, replacing any existing value for the given key. Either key or value may be null. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/Bundle#readFromParcel(android.os.Parcel)(parcel: https://developer.android.com/reference/kotlin/android/os/Parcel!)` Reads the Parcel contents into this Bundle, typically in order for it to be passed through an IBinder connection. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/Bundle#remove(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Removes any entry with the given key from the mapping of this Bundle. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/Bundle#setClassLoader(java.lang.ClassLoader)(loader: https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#!)` Changes the ClassLoader this Bundle uses when instantiating objects. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/Bundle#toString()()` Returns a string representation of the `https://developer.android.com/reference/kotlin/android/os/Bundle#` that may be suitable for debugging. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/Bundle#writeToParcel(android.os.Parcel,%20kotlin.Int)(parcel: https://developer.android.com/reference/kotlin/android/os/Parcel, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Writes the Bundle contents to a Parcel, typically in order for it to be passed through an IBinder connection. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/BaseBundle` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/os/BaseBundle#containsKey(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns true if the given key is contained in the mapping of this Bundle. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?` | `https://developer.android.com/reference/kotlin/android/os/BaseBundle#get(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns the entry with the given key as an object. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/os/BaseBundle#getBoolean(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns the value associated with the given key, or false if no mapping of the desired type exists for the given key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/os/BaseBundle#getBoolean(kotlin.String,%20kotlin.Boolean)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, defaultValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Returns the value associated with the given key, or defaultValue if no mapping of the desired type exists for the given key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html?` | `https://developer.android.com/reference/kotlin/android/os/BaseBundle#getBooleanArray(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | `https://developer.android.com/reference/kotlin/android/os/BaseBundle#getDouble(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns the value associated with the given key, or 0.0 if no mapping of the desired type exists for the given key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | `https://developer.android.com/reference/kotlin/android/os/BaseBundle#getDouble(kotlin.String,%20kotlin.Double)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, defaultValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns the value associated with the given key, or defaultValue if no mapping of the desired type exists for the given key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html?` | `https://developer.android.com/reference/kotlin/android/os/BaseBundle#getDoubleArray(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/BaseBundle#getInt(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns the value associated with the given key, or 0 if no mapping of the desired type exists for the given key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/BaseBundle#getInt(kotlin.String,%20kotlin.Int)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, defaultValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the value associated with the given key, or defaultValue if no mapping of the desired type exists for the given key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html?` | `https://developer.android.com/reference/kotlin/android/os/BaseBundle#getIntArray(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/android/os/BaseBundle#getLong(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns the value associated with the given key, or 0L if no mapping of the desired type exists for the given key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/android/os/BaseBundle#getLong(kotlin.String,%20kotlin.Long)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, defaultValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns the value associated with the given key, or defaultValue if no mapping of the desired type exists for the given key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html?` | `https://developer.android.com/reference/kotlin/android/os/BaseBundle#getLongArray(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | `https://developer.android.com/reference/kotlin/android/os/BaseBundle#getString(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | `https://developer.android.com/reference/kotlin/android/os/BaseBundle#getString(kotlin.String,%20kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, defaultValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns the value associated with the given key, or defaultValue if no mapping of the desired type exists for the given key or if a null value is explicitly associated with the given key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?` | `https://developer.android.com/reference/kotlin/android/os/BaseBundle#getStringArray(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/os/BaseBundle#isEmpty()()` Returns true if the mapping of this Bundle is empty, false otherwise. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | `https://developer.android.com/reference/kotlin/android/os/BaseBundle#keySet()()` Returns a Set containing the Strings used as keys in this Bundle. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/os/BaseBundle#putAll(android.os.PersistableBundle)(bundle: https://developer.android.com/reference/kotlin/android/os/PersistableBundle!)` Inserts all mappings from the given PersistableBundle into this BaseBundle. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/os/BaseBundle#putBoolean(kotlin.String,%20kotlin.Boolean)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Inserts a Boolean value into the mapping of this Bundle, replacing any existing value for the given key. Either key or value may be null. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/os/BaseBundle#putBooleanArray(kotlin.String,%20kotlin.BooleanArray)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html?)` Inserts a boolean array value into the mapping of this Bundle, replacing any existing value for the given key. Either key or value may be null. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/os/BaseBundle#putDouble(kotlin.String,%20kotlin.Double)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Inserts a double value into the mapping of this Bundle, replacing any existing value for the given key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/os/BaseBundle#putDoubleArray(kotlin.String,%20kotlin.DoubleArray)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html?)` Inserts a double array value into the mapping of this Bundle, replacing any existing value for the given key. Either key or value may be null. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/os/BaseBundle#putInt(kotlin.String,%20kotlin.Int)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Inserts an int value into the mapping of this Bundle, replacing any existing value for the given key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/os/BaseBundle#putIntArray(kotlin.String,%20kotlin.IntArray)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html?)` Inserts an int array value into the mapping of this Bundle, replacing any existing value for the given key. Either key or value may be null. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/os/BaseBundle#putLong(kotlin.String,%20kotlin.Long)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Inserts a long value into the mapping of this Bundle, replacing any existing value for the given key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/os/BaseBundle#putLongArray(kotlin.String,%20kotlin.LongArray)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html?)` Inserts a long array value into the mapping of this Bundle, replacing any existing value for the given key. Either key or value may be null. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/os/BaseBundle#putString(kotlin.String,%20kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Inserts a String value into the mapping of this Bundle, replacing any existing value for the given key. Either key or value may be null. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/os/BaseBundle#putStringArray(kotlin.String,%20kotlin.Array)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?)` Inserts a String array value into the mapping of this Bundle, replacing any existing value for the given key. Either key or value may be null. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/BaseBundle#size()()` Returns the number of mappings contained in this Bundle. <br /> | ||

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator)\< [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle#)!\> | `https://developer.android.com/reference/kotlin/android/os/Bundle#CREATOR:android.os.Parcelable.Creator` <br /> |
| static [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle#)! | `https://developer.android.com/reference/kotlin/android/os/Bundle#EMPTY:android.os.Bundle` An unmodifiable `Bundle` that is always `https://developer.android.com/reference/kotlin/android/os/BaseBundle#isEmpty()`. |

## Public constructors

### Bundle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Bundle()
```

### Bundle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Bundle(b: Bundle!)
```

Constructs a Bundle containing a copy of the mappings from the given Bundle. Does only a shallow copy of the original Bundle -- see `https://developer.android.com/reference/kotlin/android/os/Bundle#deepCopy()` if that is not what you want.

| Parameters ||
|---|---|
| `b` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle#)!: a Bundle to be copied. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/Bundle#deepCopy()`

### Bundle

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Bundle(b: PersistableBundle!)
```

Constructs a Bundle containing a copy of the mappings from the given PersistableBundle. Does only a shallow copy of the PersistableBundle -- see `https://developer.android.com/reference/kotlin/android/os/PersistableBundle#deepCopy()` if you don't want that.

| Parameters ||
|---|---|
| `b` | [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle)!: a PersistableBundle to be copied. |

### Bundle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Bundle(capacity: Int)
```

Constructs a new, empty Bundle sized to hold the given number of elements. The Bundle will grow as needed.

| Parameters ||
|---|---|
| `capacity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the initial capacity of the Bundle |

### Bundle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Bundle(loader: ClassLoader!)
```

Constructs a new, empty Bundle that uses a specific ClassLoader for instantiating Parcelable and Serializable objects.

| Parameters ||
|---|---|
| `loader` | [ClassLoader](https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#)!: An explicit ClassLoader to use when instantiating objects inside of the Bundle. |

## Public methods

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun clear(): Unit
```

Removes all elements from the mapping of this Bundle.

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun clone(): Any
```

Clones the current Bundle. The internal map is cloned, but the keys and values to which it refers are copied by reference.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html` | a clone of this instance. |

| Exceptions ||
|---|---|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the `Cloneable` interface. Subclasses that override the `clone` method can also throw this exception to indicate that an instance cannot be cloned. |

### deepCopy

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun deepCopy(): Bundle!
```

Make a deep copy of the given bundle. Traverses into inner containers and copies them as well, so they are not shared across bundles. Will traverse in to `https://developer.android.com/reference/kotlin/android/os/Bundle#`, `https://developer.android.com/reference/kotlin/android/os/PersistableBundle`, `https://developer.android.com/reference/kotlin/java/util/ArrayList.html#`, and all types of primitive arrays. Other types of objects (such as Parcelable or Serializable) are referenced as-is and not copied in any way.

### describeContents

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Report the nature of this Parcelable's contents

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getBinder

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getBinder(key: String?): IBinder?
```

Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/IBinder?` | an IBinder value, or null |

### getBundle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getBundle(key: String?): Bundle?
```

Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle#?` | a Bundle value, or null |

### getByte

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getByte(key: String!): Byte
```

Returns the value associated with the given key, or (byte) 0 if no mapping of the desired type exists for the given key.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a String |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html` | a byte value |

### getByte

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getByte(
    key: String!, 
    defaultValue: Byte
): Byte!
```

Returns the value associated with the given key, or defaultValue if no mapping of the desired type exists for the given key.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a String |
| `defaultValue` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html): Value to return if key does not exist |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html!` | a byte value |

### getByteArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getByteArray(key: String?): ByteArray?
```

Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html?` | a byte\[\] value, or null |

### getChar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getChar(key: String!): Char
```

Returns the value associated with the given key, or (char) 0 if no mapping of the desired type exists for the given key.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a String |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html` | a char value |

### getChar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getChar(
    key: String!, 
    defaultValue: Char
): Char
```

Returns the value associated with the given key, or defaultValue if no mapping of the desired type exists for the given key.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a String |
| `defaultValue` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): Value to return if key does not exist |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html` | a char value |

### getCharArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCharArray(key: String?): CharArray?
```

Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html?` | a char\[\] value, or null |

### getCharSequence

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCharSequence(key: String?): CharSequence?
```

Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | a CharSequence value, or null |

### getCharSequence

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCharSequence(
    key: String?, 
    defaultValue: CharSequence!
): CharSequence!
```

Returns the value associated with the given key, or defaultValue if no mapping of the desired type exists for the given key or if a null value is explicitly associatd with the given key.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or null |
| `defaultValue` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: Value to return if key does not exist or if a null value is associated with the given key. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!` | the CharSequence value associated with the given key, or defaultValue if no valid CharSequence object is currently mapped to that key. |

### getCharSequenceArray

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCharSequenceArray(key: String?): Array<CharSequence!>?
```

Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!>?` | a CharSequence\[\] value, or null |

### getCharSequenceArrayList

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCharSequenceArrayList(key: String?): ArrayList<CharSequence!>?
```

Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!>?` | an ArrayList value, or null |

### getClassLoader

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getClassLoader(): ClassLoader!
```

Return the ClassLoader currently associated with this Bundle.

### getFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getFloat(key: String!): Float
```

Returns the value associated with the given key, or 0.0f if no mapping of the desired type exists for the given key.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a String |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | a float value |

### getFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getFloat(
    key: String!, 
    defaultValue: Float
): Float
```

Returns the value associated with the given key, or defaultValue if no mapping of the desired type exists for the given key.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a String |
| `defaultValue` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Value to return if key does not exist |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | a float value |

### getFloatArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getFloatArray(key: String?): FloatArray?
```

Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html?` | a float\[\] value, or null |

### getIntegerArrayList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getIntegerArrayList(key: String?): ArrayList<Int!>?
```

Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>?` | an ArrayList value, or null |

### getParcelable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Parcelable!> getParcelable(key: String?): T?
```

**Deprecated:** *Use the type-safer `https://developer.android.com/reference/kotlin/android/os/Bundle#getParcelable(kotlin.String,%20java.lang.Class)` starting from Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES#TIRAMISU:kotlin.Int`.*

Returns the value associated with the given key, or `null` if no mapping of the desired type exists for the given key or a `null` value is explicitly associated with the key.

**Note:** if the expected value is not a class provided by the Android platform, you must call `https://developer.android.com/reference/kotlin/android/os/Bundle#setClassLoader(java.lang.ClassLoader)` with the proper `https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#` first. Otherwise, this method might throw an exception or return `null`.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or `null` |

| Return ||
|---|---|
| `T?` | a Parcelable value, or `null` |

### getParcelable

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Any!> getParcelable(
    key: String?, 
    clazz: Class<T>
): T?
```

Returns the value associated with the given key or `null` if:

- No mapping of the desired type exists for the given key.
- A `null` value is explicitly associated with the key.
- The object is not of type `clazz`.

<br />

**Note:** if the expected value is not a class provided by the Android platform, you must call `https://developer.android.com/reference/kotlin/android/os/Bundle#setClassLoader(java.lang.ClassLoader)` with the proper `https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#` first. Otherwise, this method might throw an exception or return `null`.

**Warning:** the class that implements `https://developer.android.com/reference/kotlin/android/os/Parcelable` has to be the immediately enclosing class of the runtime type of its CREATOR field (that is, `https://developer.android.com/reference/kotlin/java/lang/Class.html#getEnclosingClass()` has to return the parcelable implementing class), otherwise this method might throw an exception. If the Parcelable class does not enclose the CREATOR, use the deprecated `https://developer.android.com/reference/kotlin/android/os/Bundle#getParcelable(kotlin.String)` instead.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or `null` |
| `clazz` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<T\>: The type of the object expected. This value cannot be `null`. |

| Return ||
|---|---|
| `T?` | a Parcelable value, or `null` |

### getParcelableArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getParcelableArray(key: String?): Array<Parcelable!>?
```

**Deprecated:** *Use the type-safer `https://developer.android.com/reference/kotlin/android/os/Bundle#getParcelableArray(kotlin.String,%20java.lang.Class)` starting from Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES#TIRAMISU:kotlin.Int`.*

Returns the value associated with the given key, or `null` if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key.

**Note:** if the expected value is not a class provided by the Android platform, you must call `https://developer.android.com/reference/kotlin/android/os/Bundle#setClassLoader(java.lang.ClassLoader)` with the proper `https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#` first. Otherwise, this method might throw an exception or return `null`.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or `null` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/os/Parcelable!>?` | a Parcelable\[\] value, or `null` |

### getParcelableArray

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Any!> getParcelableArray(
    key: String?, 
    clazz: Class<T>
): Array<T>?
```

Returns the value associated with the given key, or `null` if:

- No mapping of the desired type exists for the given key.
- A `null` value is explicitly associated with the key.
- The object is not of type `clazz`.

<br />

**Note:** if the expected value is not a class provided by the Android platform, you must call `https://developer.android.com/reference/kotlin/android/os/Bundle#setClassLoader(java.lang.ClassLoader)` with the proper `https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#` first. Otherwise, this method might throw an exception or return `null`.

**Warning:** if the list contains items implementing the `https://developer.android.com/reference/kotlin/android/os/Parcelable` interface, the class that implements `https://developer.android.com/reference/kotlin/android/os/Parcelable` has to be the immediately enclosing class of the runtime type of its CREATOR field (that is, `https://developer.android.com/reference/kotlin/java/lang/Class.html#getEnclosingClass()` has to return the parcelable implementing class), otherwise this method might throw an exception. If the Parcelable class does not enclose the CREATOR, use the deprecated `https://developer.android.com/reference/kotlin/android/os/Bundle#getParcelableArray(kotlin.String)` instead.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or `null` |
| `clazz` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<T\>: The type of the items inside the array. This is only verified when unparceling. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<T>?` | a Parcelable\[\] value, or `null` |

### getParcelableArrayList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Parcelable!> getParcelableArrayList(key: String?): ArrayList<T>?
```

**Deprecated:** *Use the type-safer `https://developer.android.com/reference/kotlin/android/os/Bundle#getParcelable(kotlin.String,%20java.lang.Class)` starting from Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES#TIRAMISU:kotlin.Int`.*

Returns the value associated with the given key, or `null` if no mapping of the desired type exists for the given key or a `null` value is explicitly associated with the key.

**Note:** if the expected value is not a class provided by the Android platform, you must call `https://developer.android.com/reference/kotlin/android/os/Bundle#setClassLoader(java.lang.ClassLoader)` with the proper `https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#` first. Otherwise, this method might throw an exception or return `null`.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or `null` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<T>?` | an ArrayList value, or `null` |

### getParcelableArrayList

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Any!> getParcelableArrayList(
    key: String?, 
    clazz: Class<out T>
): ArrayList<T>?
```

Returns the value associated with the given key, or `null` if:

- No mapping of the desired type exists for the given key.
- A `null` value is explicitly associated with the key.
- The object is not of type `clazz`.

<br />

**Note:** if the expected value is not a class provided by the Android platform, you must call `https://developer.android.com/reference/kotlin/android/os/Bundle#setClassLoader(java.lang.ClassLoader)` with the proper `https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#` first. Otherwise, this method might throw an exception or return `null`.

**Warning:** if the list contains items implementing the `https://developer.android.com/reference/kotlin/android/os/Parcelable` interface, the class that implements `https://developer.android.com/reference/kotlin/android/os/Parcelable` has to be the immediately enclosing class of the runtime type of its CREATOR field (that is, `https://developer.android.com/reference/kotlin/java/lang/Class.html#getEnclosingClass()` has to return the parcelable implementing class), otherwise this method might throw an exception. If the Parcelable class does not enclose the CREATOR, use the deprecated `https://developer.android.com/reference/kotlin/android/os/Bundle#getParcelableArrayList(kotlin.String)` instead.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or `null` |
| `clazz` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<out T\>: The type of the items inside the array list. This is only verified when unparceling. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<T>?` | an ArrayList value, or `null` |

### getSerializable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSerializable(key: String?): Serializable?
```

**Deprecated:** *Use the type-safer `https://developer.android.com/reference/kotlin/android/os/Bundle#getSerializable(kotlin.String,%20java.lang.Class)` starting from Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES#TIRAMISU:kotlin.Int`.*

Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/Serializable.html#?` | a Serializable value, or null |

### getSerializable

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Serializable!> getSerializable(
    key: String?, 
    clazz: Class<T>
): T?
```

Returns the value associated with the given key, or `null` if:

- No mapping of the desired type exists for the given key.
- A `null` value is explicitly associated with the key.
- The object is not of type `clazz`.

<br />

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or null |
| `clazz` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<T\>: The expected class of the returned type. This value cannot be `null`. |

| Return ||
|---|---|
| `T?` | a Serializable value, or null |

### getShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getShort(key: String!): Short
```

Returns the value associated with the given key, or (short) 0 if no mapping of the desired type exists for the given key.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a String |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html` | a short value |

### getShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getShort(
    key: String!, 
    defaultValue: Short
): Short
```

Returns the value associated with the given key, or defaultValue if no mapping of the desired type exists for the given key.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a String |
| `defaultValue` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): Value to return if key does not exist |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html` | a short value |

### getShortArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getShortArray(key: String?): ShortArray?
```

Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html?` | a short\[\] value, or null |

### getSize

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSize(key: String?): Size?
```

Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/util/Size.html#?` | a Size value, or null |

### getSizeF

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSizeF(key: String?): SizeF?
```

Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/util/SizeF.html#?` | a Size value, or null |

### getSparseParcelableArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Parcelable!> getSparseParcelableArray(key: String?): SparseArray<T>?
```

**Deprecated:** *Use the type-safer `https://developer.android.com/reference/kotlin/android/os/Bundle#getSparseParcelableArray(kotlin.String,%20java.lang.Class)` starting from Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES#TIRAMISU:kotlin.Int`.*

Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/util/SparseArray.html#<T>?` | a SparseArray of T values, or null |

### getSparseParcelableArray

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Any!> getSparseParcelableArray(
    key: String?, 
    clazz: Class<out T>
): SparseArray<T>?
```

Returns the value associated with the given key, or `null` if:

- No mapping of the desired type exists for the given key.
- A `null` value is explicitly associated with the key.
- The object is not of type `clazz`.

<br />

**Warning:** if the list contains items implementing the `https://developer.android.com/reference/kotlin/android/os/Parcelable` interface, the class that implements `https://developer.android.com/reference/kotlin/android/os/Parcelable` has to be the immediately enclosing class of the runtime type of its CREATOR field (that is, `https://developer.android.com/reference/kotlin/java/lang/Class.html#getEnclosingClass()` has to return the parcelable implementing class), otherwise this method might throw an exception. If the Parcelable class does not enclose the CREATOR, use the deprecated `https://developer.android.com/reference/kotlin/android/os/Bundle#getSparseParcelableArray(kotlin.String)` instead.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or null |
| `clazz` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<out T\>: The type of the items inside the sparse array. This is only verified when unparceling. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/util/SparseArray.html#<T>?` | a SparseArray of T values, or null |

### getStringArrayList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getStringArrayList(key: String?): ArrayList<String!>?
```

Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?` | an ArrayList value, or null |

### hasFileDescriptors

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasFileDescriptors(): Boolean
```

Reports whether the bundle contains any parcelled file descriptors.

### putAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun putAll(bundle: Bundle!): Unit
```

Inserts all mappings from the given Bundle into this Bundle.

| Parameters ||
|---|---|
| `bundle` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle#)!: a Bundle |

### putBinder

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun putBinder(
    key: String?, 
    value: IBinder?
): Unit
```

Inserts an `https://developer.android.com/reference/kotlin/android/os/IBinder` value into the mapping of this Bundle, replacing any existing value for the given key. Either key or value may be null.

You should be very careful when using this function. In many places where Bundles are used (such as inside of Intent objects), the Bundle can live longer inside of another process than the process that had originally created it. In that case, the IBinder you supply here will become invalid when your process goes away, and no longer usable, even if a new process is created for you later on.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or null |
| `value` | [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder)?: an IBinder object, or null |

### putBundle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun putBundle(
    key: String?, 
    value: Bundle?
): Unit
```

Inserts a Bundle value into the mapping of this Bundle, replacing any existing value for the given key. Either key or value may be null.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or null |
| `value` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle#)?: a Bundle object, or null |

### putByte

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun putByte(
    key: String?, 
    value: Byte
): Unit
```

Inserts a byte value into the mapping of this Bundle, replacing any existing value for the given key.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or null |
| `value` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html): a byte |

### putByteArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun putByteArray(
    key: String?, 
    value: ByteArray?
): Unit
```

Inserts a byte array value into the mapping of this Bundle, replacing any existing value for the given key. Either key or value may be null.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or null |
| `value` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?: a byte array object, or null |

### putChar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun putChar(
    key: String?, 
    value: Char
): Unit
```

Inserts a char value into the mapping of this Bundle, replacing any existing value for the given key.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or null |
| `value` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): a char |

### putCharArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun putCharArray(
    key: String?, 
    value: CharArray?
): Unit
```

Inserts a char array value into the mapping of this Bundle, replacing any existing value for the given key. Either key or value may be null.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or null |
| `value` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)?: a char array object, or null |

### putCharSequence

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun putCharSequence(
    key: String?, 
    value: CharSequence?
): Unit
```

Inserts a CharSequence value into the mapping of this Bundle, replacing any existing value for the given key. Either key or value may be null.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or null |
| `value` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?: a CharSequence, or null |

### putCharSequenceArray

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun putCharSequenceArray(
    key: String?, 
    value: Array<CharSequence!>?
): Unit
```

Inserts a CharSequence array value into the mapping of this Bundle, replacing any existing value for the given key. Either key or value may be null.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or null |
| `value` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!\>?: a CharSequence array object, or null |

### putCharSequenceArrayList

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun putCharSequenceArrayList(
    key: String?, 
    value: ArrayList<CharSequence!>?
): Unit
```

Inserts an ArrayList value into the mapping of this Bundle, replacing any existing value for the given key. Either key or value may be null.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or null |
| `value` | [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)\< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!\>?: an ArrayList object, or null |

### putFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun putFloat(
    key: String?, 
    value: Float
): Unit
```

Inserts a float value into the mapping of this Bundle, replacing any existing value for the given key.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or null |
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): a float |

### putFloatArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun putFloatArray(
    key: String?, 
    value: FloatArray?
): Unit
```

Inserts a float array value into the mapping of this Bundle, replacing any existing value for the given key. Either key or value may be null.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or null |
| `value` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)?: a float array object, or null |

### putIntegerArrayList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun putIntegerArrayList(
    key: String?, 
    value: ArrayList<Int!>?
): Unit
```

Inserts an ArrayList value into the mapping of this Bundle, replacing any existing value for the given key. Either key or value may be null.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or null |
| `value` | [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>?: an ArrayList object, or null |

### putParcelable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun putParcelable(
    key: String?, 
    value: Parcelable?
): Unit
```

Inserts a Parcelable value into the mapping of this Bundle, replacing any existing value for the given key. Either key or value may be null.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or null |
| `value` | [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable)?: a Parcelable object, or null |

### putParcelableArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun putParcelableArray(
    key: String?, 
    value: Array<Parcelable!>?
): Unit
```

Inserts an array of Parcelable values into the mapping of this Bundle, replacing any existing value for the given key. Either key or value may be null.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or null |
| `value` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable)!\>?: an array of Parcelable objects, or null |

### putParcelableArrayList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun putParcelableArrayList(
    key: String?, 
    value: ArrayList<out Parcelable!>?
): Unit
```

Inserts a List of Parcelable values into the mapping of this Bundle, replacing any existing value for the given key. Either key or value may be null.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or null |
| `value` | [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)\<out [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable)!\>?: an ArrayList of Parcelable objects, or null |

### putSerializable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun putSerializable(
    key: String?, 
    value: Serializable?
): Unit
```

Inserts a Serializable value into the mapping of this Bundle, replacing any existing value for the given key. Either key or value may be null.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or null |
| `value` | [Serializable](https://developer.android.com/reference/kotlin/java/io/Serializable.html#)?: a Serializable object, or null |

### putShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun putShort(
    key: String?, 
    value: Short
): Unit
```

Inserts a short value into the mapping of this Bundle, replacing any existing value for the given key.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or null |
| `value` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): a short |

### putShortArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun putShortArray(
    key: String?, 
    value: ShortArray?
): Unit
```

Inserts a short array value into the mapping of this Bundle, replacing any existing value for the given key. Either key or value may be null.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or null |
| `value` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html)?: a short array object, or null |

### putSize

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun putSize(
    key: String?, 
    value: Size?
): Unit
```

Inserts a Size value into the mapping of this Bundle, replacing any existing value for the given key. Either key or value may be null.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or null |
| `value` | [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#)?: a Size object, or null |

### putSizeF

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun putSizeF(
    key: String?, 
    value: SizeF?
): Unit
```

Inserts a SizeF value into the mapping of this Bundle, replacing any existing value for the given key. Either key or value may be null.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or null |
| `value` | [SizeF](https://developer.android.com/reference/kotlin/android/util/SizeF.html#)?: a SizeF object, or null |

### putSparseParcelableArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun putSparseParcelableArray(
    key: String?, 
    value: SparseArray<out Parcelable!>?
): Unit
```

Inserts a SparceArray of Parcelable values into the mapping of this Bundle, replacing any existing value for the given key. Either key or value may be null.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or null |
| `value` | [SparseArray](https://developer.android.com/reference/kotlin/android/util/SparseArray.html#)\<out [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable)!\>?: a SparseArray of Parcelable objects, or null |

### putStringArrayList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun putStringArrayList(
    key: String?, 
    value: ArrayList<String!>?
): Unit
```

Inserts an ArrayList value into the mapping of this Bundle, replacing any existing value for the given key. Either key or value may be null.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a String, or null |
| `value` | [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: an ArrayList object, or null |

### readFromParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readFromParcel(parcel: Parcel!): Unit
```

Reads the Parcel contents into this Bundle, typically in order for it to be passed through an IBinder connection.

| Parameters ||
|---|---|
| `parcel` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel)!: The parcel to overwrite this bundle from. |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun remove(key: String!): Unit
```

Removes any entry with the given key from the mapping of this Bundle.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a String key |

### setClassLoader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setClassLoader(loader: ClassLoader!): Unit
```

Changes the ClassLoader this Bundle uses when instantiating objects.

| Parameters ||
|---|---|
| `loader` | [ClassLoader](https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#)!: An explicit ClassLoader to use when instantiating objects inside of the Bundle. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the `https://developer.android.com/reference/kotlin/android/os/Bundle#` that may be suitable for debugging. It won't print the internal map if its content hasn't been unparcelled.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    parcel: Parcel, 
    flags: Int
): Unit
```

Writes the Bundle contents to a Parcel, typically in order for it to be passed through an IBinder connection.

| Parameters ||
|---|---|
| `dest` | The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |
| `parcel` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel): The parcel to copy this bundle to. |
| --- | --- |

## Properties

### CREATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<Bundle!>
```

### EMPTY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EMPTY: Bundle!
```

An unmodifiable `Bundle` that is always `https://developer.android.com/reference/kotlin/android/os/BaseBundle#isEmpty()`.
