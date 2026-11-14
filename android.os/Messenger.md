# Messenger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Messenger

Kotlin| [Java](https://developer.android.com/reference/android/os/Messenger "View this page in Java") 
| --- | --- |

```
class Messenger : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.Messenger](https://developer.android.com/reference/kotlin/android/os/Messenger#) |

Reference to a Handler, which others can use to send messages to it. This allows for the implementation of message-based communication across processes, by creating a Messenger pointing to a Handler in one process, and handing that Messenger to another process.

Note: the implementation underneath is just a simple wrapper around a [Binder](https://developer.android.com/reference/kotlin/android/os/Binder) that is used to perform the communication. This means semantically you should treat it as such: this class does not impact process lifecycle management (you must be using some higher-level component to tell the system that your process needs to continue running), the connection will break if your process goes away for any reason, etc.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable) |----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Messenger](https://developer.android.com/reference/kotlin/android/os/Messenger#Messenger(android.os.Handler))`(`target:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler)!`)` Create a new Messenger pointing to the given Handler. |
| [Messenger](https://developer.android.com/reference/kotlin/android/os/Messenger#Messenger(android.os.IBinder))`(`target:` ` [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder)!`)` Create a Messenger from a raw IBinder, which had previously been retrieved with [getBinder](https://developer.android.com/reference/kotlin/android/os/Messenger#getBinder()). |

| Public methods ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/os/Messenger#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/os/Messenger#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Comparison operator on two Messenger objects, such that true is returned then they both point to the same Handler. |
| [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder)! | [getBinder](https://developer.android.com/reference/kotlin/android/os/Messenger#getBinder())`()` Retrieve the IBinder that this Messenger is using to communicate with its associated Handler. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/os/Messenger#hashCode())`()` <br /> |
| static [Messenger](https://developer.android.com/reference/kotlin/android/os/Messenger#)! | [readMessengerOrNullFromParcel](https://developer.android.com/reference/kotlin/android/os/Messenger#readMessengerOrNullFromParcel(android.os.Parcel))`(`in:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel)!`)` Convenience function for reading either a Messenger or null pointer from a Parcel. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [send](https://developer.android.com/reference/kotlin/android/os/Messenger#send(android.os.Message))`(`message:` ` [Message](https://developer.android.com/reference/kotlin/android/os/Message)!`)` Send a Message to this Messenger's Handler. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeMessengerOrNullToParcel](https://developer.android.com/reference/kotlin/android/os/Messenger#writeMessengerOrNullToParcel(android.os.Messenger,%20android.os.Parcel))`(`messenger:` ` [Messenger](https://developer.android.com/reference/kotlin/android/os/Messenger#)!`, `out:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel)!`)` Convenience function for writing either a Messenger or null pointer to a Parcel. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Messenger#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`out:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator)\< [Messenger](https://developer.android.com/reference/kotlin/android/os/Messenger#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/os/Messenger#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public constructors

### Messenger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Messenger(target: Handler!)
```

Create a new Messenger pointing to the given Handler. Any Message objects sent through this Messenger will appear in the Handler as if [Handler.sendMessage(Message)](https://developer.android.com/reference/kotlin/android/os/Handler#sendMessage(android.os.Message))had been called directly.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------|
| `target` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler)!:The Handler that will receive sent messages. |

### Messenger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Messenger(target: IBinder!)
```

Create a Messenger from a raw IBinder, which had previously been retrieved with [getBinder](https://developer.android.com/reference/kotlin/android/os/Messenger#getBinder()).

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------|
| `target` | [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder)!:The IBinder this Messenger should communicate with. |

## Public methods

### describeContents

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Comparison operator on two Messenger objects, such that true is returned then they both point to the same Handler.

| Parameters ||
|------------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `otherObj` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getBinder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBinder(): IBinder!
```

Retrieve the IBinder that this Messenger is using to communicate with its associated Handler.

| Return ||
|-------------------------------------------------------------------------------|---------------------------------------------|
| [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder)! | Returns the IBinder backing this Messenger. |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### readMessengerOrNullFromParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun readMessengerOrNullFromParcel(in: Parcel!): Messenger!
```

Convenience function for reading either a Messenger or null pointer from a Parcel. You must have previously written the Messenger with [writeMessengerOrNullToParcel](https://developer.android.com/reference/kotlin/android/os/Messenger#writeMessengerOrNullToParcel(android.os.Messenger,%20android.os.Parcel)).

| Parameters ||
|------|--------------------------------------------------------------------------------------------------------------------------|
| `in` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel)!:The Parcel containing the written Messenger. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Messenger](https://developer.android.com/reference/kotlin/android/os/Messenger#)! | Returns the Messenger read from the Parcel, or null if null had been written. |

### send

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun send(message: Message!): Unit
```

Send a Message to this Messenger's Handler.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [Message](https://developer.android.com/reference/kotlin/android/os/Message)!:The Message to send. Usually retrieved through [Message.obtain()](https://developer.android.com/reference/kotlin/android/os/Message#obtain()). |

| Exceptions ||
|------------------------------|--------------------------------------------------------------------|
| `android.os.RemoteException` | Throws DeadObjectException if the target Handler no longer exists. |

### writeMessengerOrNullToParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun writeMessengerOrNullToParcel(
    messenger: Messenger!, 
    out: Parcel!
): Unit
```

Convenience function for writing either a Messenger or null pointer to a Parcel. You must use this with [readMessengerOrNullFromParcel](https://developer.android.com/reference/kotlin/android/os/Messenger#readMessengerOrNullFromParcel(android.os.Parcel))for later reading it.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------|
| `messenger` | [Messenger](https://developer.android.com/reference/kotlin/android/os/Messenger#)!:The Messenger to write, or null. |
| `out` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel)!:Where to write the Messenger. |

### writeToParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    out: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<Messenger!>
```
