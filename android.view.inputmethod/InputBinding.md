# InputBinding

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InputBinding

Kotlin| [Java](InputBinding.md) 
| --- | --- |

```
class InputBinding : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.inputmethod.InputBinding](InputBinding.md) |

Information given to an [InputMethod](InputMethod.md) about a client connecting to it.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [InputBinding](InputBinding.md))`(`conn:` ` [InputConnection](InputConnection.md)!`, `connToken:` ` [IBinder](../android.os/IBinder.md)!`, `uid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructor. |
| [InputBinding](InputBinding.md))`(`conn:` ` [InputConnection](InputConnection.md)!`, `binding:` ` [InputBinding](InputBinding.md)!`)` Constructor from an existing InputBinding taking a new local input connection interface. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](InputBinding.md))`()` <br /> |
| [InputConnection](InputConnection.md)! | [getConnection](InputBinding.md))`()` Return the connection for interacting back with the application. |
| [IBinder](../android.os/IBinder.md)! | [getConnectionToken](InputBinding.md))`()` Return the token for the connection back to the application. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPid](InputBinding.md))`()` Return the process id where this binding came from. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getUid](InputBinding.md))`()` Return the user id of the client associated with this binding. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](InputBinding.md))`()` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](InputBinding.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Used to package this object into a [Parcel](../android.os/Parcel.md). |

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [InputBinding](InputBinding.md)!\> | [CREATOR](InputBinding.md) Used to make this class parcelable. |

## Public constructors

### InputBinding

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InputBinding(
    conn: InputConnection!, 
    connToken: IBinder!, 
    uid: Int, 
    pid: Int)
```

Constructor.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `conn` | [InputConnection](InputConnection.md)!:The interface for communicating back with the application. |
| `connToken` | [IBinder](../android.os/IBinder.md)!:A remoteable token for communicating across processes. |
| `uid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The user id of the client of this binding. |
| --- | --- |
| `pid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The process id of where the binding came from. |

### InputBinding

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InputBinding(
    conn: InputConnection!, 
    binding: InputBinding!)
```

Constructor from an existing InputBinding taking a new local input connection interface.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `conn` | [InputConnection](InputConnection.md)!:The new connection interface. |
| `binding` | [InputBinding](InputBinding.md)!:Existing binding to copy. |

## Public methods

### describeContents

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### getConnection

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConnection(): InputConnection!
```

Return the connection for interacting back with the application. 

### getConnectionToken

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConnectionToken(): IBinder!
```

Return the token for the connection back to the application. You can not use this directly, it must be converted to a [InputConnection](InputConnection.md) for you. 

### getPid

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPid(): Int
```

Return the process id where this binding came from. 

### getUid

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUid(): Int
```

Return the user id of the client associated with this binding. 

### toString

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Used to package this object into a [Parcel](../android.os/Parcel.md).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android.os/Parcel.md):The [Parcel](../android.os/Parcel.md) to be written. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The flags used for parceling. |

## Properties

### CREATOR

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<InputBinding!>
```

Used to make this class parcelable.
