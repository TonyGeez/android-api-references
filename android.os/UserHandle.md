# UserHandle

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UserHandle

Kotlin| [Java](UserHandle.md) 
| --- | --- |

```
class UserHandle : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.UserHandle](UserHandle.md) |

Representation of a user on the device.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](Parcelable.md) |----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](Parcelable.md) <br /> Descriptor bit used with [describeContents()](Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](Parcelable.md) <br /> Flag for use with [writeToParcel](Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UserHandle](UserHandle.md))`(`in:` ` [Parcel](Parcel.md)!`)` Instantiate a new UserHandle from the data in a Parcel that was previously written with [writeToParcel(android.os.Parcel,int)](UserHandle.md)). |

| Public methods ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](UserHandle.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](UserHandle.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| static [UserHandle](UserHandle.md)! | [getUserHandleForUid](UserHandle.md))`(`uid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the user for a given uid. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](UserHandle.md))`()` <br /> |
| static [UserHandle](UserHandle.md)! | [readFromParcel](UserHandle.md))`(`in:` ` [Parcel](Parcel.md)!`)` Read a UserHandle from a Parcel that was previously written with [writeToParcel(android.os.UserHandle,android.os.Parcel)](UserHandle.md)), returning either a null or new object as appropriate. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](UserHandle.md))`()` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](UserHandle.md))`(`out:` ` [Parcel](Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](UserHandle.md))`(`h:` ` [UserHandle](UserHandle.md)!`, `out:` ` [Parcel](Parcel.md)!`)` Write a UserHandle to a Parcel, handling null pointers. |

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [UserHandle](UserHandle.md)!\> | [CREATOR](UserHandle.md) <br /> |

## Public constructors

### UserHandle

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UserHandle(in: Parcel!)
```

Instantiate a new UserHandle from the data in a Parcel that was previously written with [writeToParcel(android.os.Parcel,int)](UserHandle.md)). Note that you must not use this with data written by [writeToParcel(android.os.UserHandle,android.os.Parcel)](UserHandle.md))since it is not possible to handle a null UserHandle here.

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `in` | [Parcel](Parcel.md)!:The Parcel containing the previously written UserHandle, positioned at the location in the buffer where it was written. |

## Public methods

### describeContents

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](Parcelable.md) |

### equals

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|--------------------------|
| `obj` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getUserHandleForUid

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getUserHandleForUid(uid: Int): UserHandle!
```

Returns the user for a given uid.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------|
| `uid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A uid for an application running in a particular user. |

| Return ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [UserHandle](UserHandle.md)! | A [UserHandle](UserHandle.md) for that user. |

### hashCode

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### readFromParcel

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun readFromParcel(in: Parcel!): UserHandle!
```

Read a UserHandle from a Parcel that was previously written with [writeToParcel(android.os.UserHandle,android.os.Parcel)](UserHandle.md)), returning either a null or new object as appropriate.

| Parameters ||
|------|--------------------------------------------------------------------------------------------------------------------------|
| `in` | [Parcel](Parcel.md)!:The Parcel from which to read the UserHandle |

| Return ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [UserHandle](UserHandle.md)! | Returns a new UserHandle matching the previously written object, or null if a null had been written. |

**See Also**

- [#writeToParcel(UserHandle, Parcel)](UserHandle.md)) 

### toString

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    out: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

### writeToParcel

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun writeToParcel(
    h: UserHandle!, 
    out: Parcel!
): Unit
```

Write a UserHandle to a Parcel, handling null pointers. Must be read with [readFromParcel(android.os.Parcel)](UserHandle.md)).

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------|
| `h` | [UserHandle](UserHandle.md)!:The UserHandle to be written. |
| `out` | [Parcel](Parcel.md)!:The Parcel in which the UserHandle will be placed. |

**See Also**

- [#readFromParcel(Parcel)](UserHandle.md))

## Properties

### CREATOR

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<UserHandle!>
```
