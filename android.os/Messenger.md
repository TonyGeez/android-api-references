# Messenger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Messenger

Kotlin| [Java](../android/os/Messenger.md) 
| --- | --- |

```
class Messenger : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.Messenger](../android/os/Messenger.md) |

Reference to a Handler, which others can use to send messages to it. This allows for the implementation of message-based communication across processes, by creating a Messenger pointing to a Handler in one process, and handing that Messenger to another process.

Note: the implementation underneath is just a simple wrapper around a [Binder](../android/os/Binder.md) that is used to perform the communication. This means semantically you should treat it as such: this class does not impact process lifecycle management (you must be using some higher-level component to tell the system that your process needs to continue running), the connection will break if your process goes away for any reason, etc.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Messenger](../android/os/Messenger.md))`(`target:` ` [Handler](../android/os/Handler.md)!`)` Create a new Messenger pointing to the given Handler. |
| [Messenger](../android/os/Messenger.md))`(`target:` ` [IBinder](../android/os/IBinder.md)!`)` Create a Messenger from a raw IBinder, which had previously been retrieved with [getBinder](../android/os/Messenger.md)). |

| Public methods ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/os/Messenger.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/os/Messenger.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Comparison operator on two Messenger objects, such that true is returned then they both point to the same Handler. |
| [IBinder](../android/os/IBinder.md)! | [getBinder](../android/os/Messenger.md))`()` Retrieve the IBinder that this Messenger is using to communicate with its associated Handler. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/os/Messenger.md))`()` <br /> |
| static [Messenger](../android/os/Messenger.md)! | [readMessengerOrNullFromParcel](../android/os/Messenger.md))`(`in:` ` [Parcel](../android/os/Parcel.md)!`)` Convenience function for reading either a Messenger or null pointer from a Parcel. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [send](../android/os/Messenger.md))`(`message:` ` [Message](../android/os/Message.md)!`)` Send a Message to this Messenger's Handler. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeMessengerOrNullToParcel](../android/os/Messenger.md))`(`messenger:` ` [Messenger](../android/os/Messenger.md)!`, `out:` ` [Parcel](../android/os/Parcel.md)!`)` Convenience function for writing either a Messenger or null pointer to a Parcel. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/os/Messenger.md))`(`out:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [Messenger](../android/os/Messenger.md)!\> | [CREATOR](../android/os/Messenger.md) <br /> |

## Public constructors

### Messenger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Messenger(target: Handler!)
```

Create a new Messenger pointing to the given Handler. Any Message objects sent through this Messenger will appear in the Handler as if [Handler.sendMessage(Message)](../android/os/Handler.md))had been called directly.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------|
| `target` | [Handler](../android/os/Handler.md)!:The Handler that will receive sent messages. |

### Messenger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Messenger(target: IBinder!)
```

Create a Messenger from a raw IBinder, which had previously been retrieved with [getBinder](../android/os/Messenger.md)).

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------|
| `target` | [IBinder](../android/os/IBinder.md)!:The IBinder this Messenger should communicate with. |

## Public methods

### describeContents

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

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
| [IBinder](../android/os/IBinder.md)! | Returns the IBinder backing this Messenger. |

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

Convenience function for reading either a Messenger or null pointer from a Parcel. You must have previously written the Messenger with [writeMessengerOrNullToParcel](../android/os/Messenger.md)).

| Parameters ||
|------|--------------------------------------------------------------------------------------------------------------------------|
| `in` | [Parcel](../android/os/Parcel.md)!:The Parcel containing the written Messenger. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Messenger](../android/os/Messenger.md)! | Returns the Messenger read from the Parcel, or null if null had been written. |

### send

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun send(message: Message!): Unit
```

Send a Message to this Messenger's Handler.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [Message](../android/os/Message.md)!:The Message to send. Usually retrieved through [Message.obtain()](../android/os/Message.md)). |

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

Convenience function for writing either a Messenger or null pointer to a Parcel. You must use this with [readMessengerOrNullFromParcel](../android/os/Messenger.md))for later reading it.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------|
| `messenger` | [Messenger](../android/os/Messenger.md)!:The Messenger to write, or null. |
| `out` | [Parcel](../android/os/Parcel.md)!:Where to write the Messenger. |

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
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<Messenger!>
```
