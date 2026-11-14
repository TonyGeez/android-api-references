# Messenger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Messenger

Kotlin| [Java](Messenger.md) 
| --- | --- |

```
class Messenger : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.Messenger](Messenger.md) |

Reference to a Handler, which others can use to send messages to it. This allows for the implementation of message-based communication across processes, by creating a Messenger pointing to a Handler in one process, and handing that Messenger to another process.

Note: the implementation underneath is just a simple wrapper around a [Binder](Binder.md) that is used to perform the communication. This means semantically you should treat it as such: this class does not impact process lifecycle management (you must be using some higher-level component to tell the system that your process needs to continue running), the connection will break if your process goes away for any reason, etc.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](Parcelable.md) |----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](Parcelable.md) <br /> Descriptor bit used with [describeContents()](Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](Parcelable.md) <br /> Flag for use with [writeToParcel](Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Messenger](Messenger.md))`(`target:` ` [Handler](Handler.md)!`)` Create a new Messenger pointing to the given Handler. |
| [Messenger](Messenger.md))`(`target:` ` [IBinder](IBinder.md)!`)` Create a Messenger from a raw IBinder, which had previously been retrieved with [getBinder](Messenger.md)). |

| Public methods ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](Messenger.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](Messenger.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Comparison operator on two Messenger objects, such that true is returned then they both point to the same Handler. |
| [IBinder](IBinder.md)! | [getBinder](Messenger.md))`()` Retrieve the IBinder that this Messenger is using to communicate with its associated Handler. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](Messenger.md))`()` <br /> |
| static [Messenger](Messenger.md)! | [readMessengerOrNullFromParcel](Messenger.md))`(`in:` ` [Parcel](Parcel.md)!`)` Convenience function for reading either a Messenger or null pointer from a Parcel. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [send](Messenger.md))`(`message:` ` [Message](Message.md)!`)` Send a Message to this Messenger's Handler. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeMessengerOrNullToParcel](Messenger.md))`(`messenger:` ` [Messenger](Messenger.md)!`, `out:` ` [Parcel](Parcel.md)!`)` Convenience function for writing either a Messenger or null pointer to a Parcel. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](Messenger.md))`(`out:` ` [Parcel](Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [Messenger](Messenger.md)!\> | [CREATOR](Messenger.md) <br /> |

## Public constructors

### Messenger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Messenger(target: Handler!)
```

Create a new Messenger pointing to the given Handler. Any Message objects sent through this Messenger will appear in the Handler as if [Handler.sendMessage(Message)](Handler.md))had been called directly.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------|
| `target` | [Handler](Handler.md)!:The Handler that will receive sent messages. |

### Messenger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Messenger(target: IBinder!)
```

Create a Messenger from a raw IBinder, which had previously been retrieved with [getBinder](Messenger.md)).

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------|
| `target` | [IBinder](IBinder.md)!:The IBinder this Messenger should communicate with. |

## Public methods

### describeContents

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](Parcelable.md) |

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
| [IBinder](IBinder.md)! | Returns the IBinder backing this Messenger. |

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

Convenience function for reading either a Messenger or null pointer from a Parcel. You must have previously written the Messenger with [writeMessengerOrNullToParcel](Messenger.md)).

| Parameters ||
|------|--------------------------------------------------------------------------------------------------------------------------|
| `in` | [Parcel](Parcel.md)!:The Parcel containing the written Messenger. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Messenger](Messenger.md)! | Returns the Messenger read from the Parcel, or null if null had been written. |

### send

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun send(message: Message!): Unit
```

Send a Message to this Messenger's Handler.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [Message](Message.md)!:The Message to send. Usually retrieved through [Message.obtain()](Message.md)). |

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

Convenience function for writing either a Messenger or null pointer to a Parcel. You must use this with [readMessengerOrNullFromParcel](Messenger.md))for later reading it.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------|
| `messenger` | [Messenger](Messenger.md)!:The Messenger to write, or null. |
| `out` | [Parcel](Parcel.md)!:Where to write the Messenger. |

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
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<Messenger!>
```
