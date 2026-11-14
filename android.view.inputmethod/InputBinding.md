# InputBinding

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InputBinding

Kotlin| [Java](https://developer.android.com/reference/android/view/inputmethod/InputBinding "View this page in Java") 
| --- | --- |

```
class InputBinding : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.inputmethod.InputBinding](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputBinding#) |

Information given to an [InputMethod](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethod) about a client connecting to it.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [InputBinding](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputBinding#InputBinding(android.view.inputmethod.InputConnection,%20android.os.IBinder,%20kotlin.Int,%20kotlin.Int))`(`conn:` ` [InputConnection](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection)!`, `connToken:` ` [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder.html#)!`, `uid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructor. |
| [InputBinding](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputBinding#InputBinding(android.view.inputmethod.InputConnection,%20android.view.inputmethod.InputBinding))`(`conn:` ` [InputConnection](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection)!`, `binding:` ` [InputBinding](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputBinding#)!`)` Constructor from an existing InputBinding taking a new local input connection interface. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputBinding#describeContents())`()` <br /> |
| [InputConnection](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection)! | [getConnection](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputBinding#getConnection())`()` Return the connection for interacting back with the application. |
| [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder.html#)! | [getConnectionToken](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputBinding#getConnectionToken())`()` Return the token for the connection back to the application. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPid](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputBinding#getPid())`()` Return the process id where this binding came from. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getUid](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputBinding#getUid())`()` Return the user id of the client associated with this binding. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputBinding#toString())`()` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputBinding#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Used to package this object into a [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#). |

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [InputBinding](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputBinding#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputBinding#CREATOR:android.os.Parcelable.Creator) Used to make this class parcelable. |

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
| `conn` | [InputConnection](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection)!:The interface for communicating back with the application. |
| `connToken` | [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder.html#)!:A remoteable token for communicating across processes. |
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
| `conn` | [InputConnection](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection)!:The new connection interface. |
| `binding` | [InputBinding](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputBinding#)!:Existing binding to copy. |

## Public methods

### describeContents

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

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

Return the token for the connection back to the application. You can not use this directly, it must be converted to a [InputConnection](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection) for you. 

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

Used to package this object into a [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#) to be written. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The flags used for parceling. |

## Properties

### CREATOR

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<InputBinding!>
```

Used to make this class parcelable.
