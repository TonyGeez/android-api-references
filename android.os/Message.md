# Message

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Message

Kotlin| [Java](Message.md) 
| --- | --- |

```
class Message : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.Message](Message.md) |

Defines a message containing a description and arbitrary data object that can be sent to a [Handler](Handler.md). This object contains two extra int fields and an extra object field that allow you to not do allocations in many cases.

While the constructor of Message is public, the best way to get one of these is to call #obtain or one of the android.os.Handler#obtainMessage methods, which will pull them from a pool of recycled objects.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](Parcelable.md) |----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](Parcelable.md) <br /> Descriptor bit used with [describeContents()](Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](Parcelable.md) <br /> Flag for use with [writeToParcel](Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Message](Message.md))`()` Constructor (but the preferred way to get a Message is to call [Message.obtain()](Message.md))). |

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [copyFrom](Message.md))`(`o:` ` [Message](Message.md)!`)` Make this message like o. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](Message.md))`()` <br /> |
| [Runnable](../java.lang/Runnable.md)! | [getCallback](Message.md))`()` Retrieve callback object that will execute when this message is handled. |
| --- | --- |
| [Bundle](Bundle.md)! | [getData](Message.md))`()` Obtains a Bundle of arbitrary data associated with this event, lazily creating it if necessary. |
| [Handler](Handler.md)! | [getTarget](Message.md))`()` Retrieve the [Handler](Handler.md) implementation that will receive this message. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getWhen](Message.md))`()` Return the targeted delivery time of this message, in milliseconds. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAsynchronous](Message.md))`()` Returns true if the message is asynchronous, meaning that it is not subject to [Looper](Looper.md) synchronization barriers. |
| static [Message](Message.md)! | [obtain](Message.md))`()` Return a new Message instance from the global pool. |
| static [Message](Message.md)! | [obtain](Message.md))`(`h:` ` [Handler](Handler.md)!`)` Same as [obtain()](Message.md)), but sets the value for the*target*member on the Message returned. |
| --- | --- |
| static [Message](Message.md)! | [obtain](Message.md))`(`h:` ` [Handler](Handler.md)!`, `what:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Same as [obtain()](Message.md)), but sets the values for both*target* and*what*members on the Message. |
| static [Message](Message.md)! | [obtain](Message.md))`(`h:` ` [Handler](Handler.md)!`, `what:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `arg1:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `arg2:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Same as [obtain()](Message.md)), but sets the values of the*target* ,*what* ,*arg1* , and*arg2*members. |
| static [Message](Message.md)! | [obtain](Message.md))`(`h:` ` [Handler](Handler.md)!`, `what:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `arg1:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `arg2:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Same as [obtain()](Message.md)), but sets the values of the*target* ,*what* ,*arg1* ,*arg2* , and*obj*members. |
| --- | --- |
| static [Message](Message.md)! | [obtain](Message.md))`(`h:` ` [Handler](Handler.md)!`, `what:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Same as [obtain()](Message.md)), but sets the values of the*target* ,*what* , and*obj*members. |
| static [Message](Message.md)! | [obtain](Message.md))`(`h:` ` [Handler](Handler.md)!`, `callback:` ` [Runnable](../java.lang/Runnable.md)!`)` Same as [obtain(android.os.Handler)](Message.md)), but assigns a callback Runnable on the Message that is returned. |
| static [Message](Message.md)! | [obtain](Message.md))`(`orig:` ` [Message](Message.md)!`)` Same as [obtain()](Message.md)), but copies the values of an existing message (including its target) into the new one. |
| --- | --- |
| [Bundle](Bundle.md)? | [peekData](Message.md))`()` Like getData(), but does not lazily create the Bundle. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [recycle](Message.md))`()` Return a Message instance to the global pool. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendToTarget](Message.md))`()` Sends this Message to the Handler specified by [getTarget](Message.md)). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAsynchronous](Message.md))`(`async:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether the message is asynchronous, meaning that it is not subject to [Looper](Looper.md) synchronization barriers. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setData](Message.md))`(`data:` ` [Bundle](Bundle.md)!`)` Sets a Bundle of arbitrary data values. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTarget](Message.md))`(`target:` ` [Handler](Handler.md)!`)` <br /> |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](Message.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](Message.md))`(`dest:` ` [Parcel](Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [Message](Message.md)!\> | [CREATOR](Message.md) <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [arg1](Message.md) arg1 and arg2 are lower-cost alternatives to using [setData()](Message.md))if you only need to store a few integer values. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [arg2](Message.md) arg1 and arg2 are lower-cost alternatives to using [setData()](Message.md))if you only need to store a few integer values. |
| --- | --- |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [obj](Message.md) An arbitrary object to send to the recipient. |
| [Messenger](Messenger.md)! | [replyTo](Message.md) Optional Messenger where replies to this message can be sent. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [sendingUid](Message.md) Optional field indicating the uid that sent the message. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [what](Message.md) User-defined message code so that the recipient can identify what this message is about. |

## Public constructors

### Message

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Message()
```

Constructor (but the preferred way to get a Message is to call [Message.obtain()](Message.md))).

## Public methods

### copyFrom

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun copyFrom(o: Message!): Unit
```

Make this message like o. Performs a shallow copy of the data field. Does not copy the linked list fields, nor the timestamp or target/callback of the original message. 

### describeContents

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](Parcelable.md) |

### getCallback

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCallback(): Runnable!
```

Retrieve callback object that will execute when this message is handled. This object must implement Runnable. This is called by the*target* [Handler](Handler.md) that is receiving this Message to dispatch it. If not set, the message will be dispatched to the receiving Handler's [Handler.handleMessage(Message)](Handler.md)). 

### getData

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getData(): Bundle!
```

Obtains a Bundle of arbitrary data associated with this event, lazily creating it if necessary. Set this value by calling [setData(android.os.Bundle)](Message.md)). Note that when transferring data across processes via [Messenger](Messenger.md), you will need to set your ClassLoader on the Bundle via [Bundle.setClassLoader()](Bundle.md))so that it can instantiate your objects when you retrieve them. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/os/Message#peekData()>
- [#setData(Bundle)](Message.md)) 

### getTarget

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTarget(): Handler!
```

Retrieve the [Handler](Handler.md) implementation that will receive this message. The object must implement [Handler.handleMessage()](Handler.md)). Each Handler has its own name-space for message codes, so you do not need to worry about yours conflicting with other handlers. 

### getWhen

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getWhen(): Long
```

Return the targeted delivery time of this message, in milliseconds. 

### isAsynchronous

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isAsynchronous(): Boolean
```

Returns true if the message is asynchronous, meaning that it is not subject to [Looper](Looper.md) synchronization barriers.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the message is asynchronous. |

**See Also**

- [#setAsynchronous(boolean)](Message.md)) 

### obtain

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun obtain(): Message!
```

Return a new Message instance from the global pool. Allows us to avoid allocating new objects in many cases. 

### obtain

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun obtain(h: Handler!): Message!
```

Same as [obtain()](Message.md)), but sets the value for the*target*member on the Message returned.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `h` | [Handler](Handler.md)!:Handler to assign to the returned Message object's*target*member. |

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------|
| [Message](Message.md)! | A Message object from the global pool. |

### obtain

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun obtain(
    h: Handler!, 
    what: Int
): Message!
```

Same as [obtain()](Message.md)), but sets the values for both*target* and*what*members on the Message.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------|
| `h` | [Handler](Handler.md)!:Value to assign to the*target*member. |
| `what` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value to assign to the*what*member. |

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------|
| [Message](Message.md)! | A Message object from the global pool. |

### obtain

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun obtain(
    h: Handler!, 
    what: Int, 
    arg1: Int, 
    arg2: Int
): Message!
```

Same as [obtain()](Message.md)), but sets the values of the*target* ,*what* ,*arg1* , and*arg2*members.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------|
| `h` | [Handler](Handler.md)!:The*target*value to set. |
| `what` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The*what*value to set. |
| `arg1` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The*arg1*value to set. |
| --- | --- |
| `arg2` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The*arg2*value to set. |

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------|
| [Message](Message.md)! | A Message object from the global pool. |

### obtain

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun obtain(
    h: Handler!, 
    what: Int, 
    arg1: Int, 
    arg2: Int, 
    obj: Any!
): Message!
```

Same as [obtain()](Message.md)), but sets the values of the*target* ,*what* ,*arg1* ,*arg2* , and*obj*members.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------|
| `h` | [Handler](Handler.md)!:The*target*value to set. |
| `what` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The*what*value to set. |
| `arg1` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The*arg1*value to set. |
| --- | --- |
| `arg2` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The*arg2*value to set. |
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The*obj*value to set. |

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------|
| [Message](Message.md)! | A Message object from the global pool. |

### obtain

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun obtain(
    h: Handler!, 
    what: Int, 
    obj: Any!
): Message!
```

Same as [obtain()](Message.md)), but sets the values of the*target* ,*what* , and*obj*members.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------|
| `h` | [Handler](Handler.md)!:The*target*value to set. |
| `what` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The*what*value to set. |
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The*object*method to set. |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------|
| [Message](Message.md)! | A Message object from the global pool. |

### obtain

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun obtain(
    h: Handler!, 
    callback: Runnable!
): Message!
```

Same as [obtain(android.os.Handler)](Message.md)), but assigns a callback Runnable on the Message that is returned.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `h` | [Handler](Handler.md)!:Handler to assign to the returned Message object's*target*member. |
| `callback` | [Runnable](../java.lang/Runnable.md)!:Runnable that will execute when the message is handled. |

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------|
| [Message](Message.md)! | A Message object from the global pool. |

### obtain

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun obtain(orig: Message!): Message!
```

Same as [obtain()](Message.md)), but copies the values of an existing message (including its target) into the new one.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------|
| `orig` | [Message](Message.md)!:Original message to copy. |

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------|
| [Message](Message.md)! | A Message object from the global pool. |

### peekData

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun peekData(): Bundle?
```

Like getData(), but does not lazily create the Bundle. A null is returned if the Bundle does not already exist. See [getData](Message.md))for further information on this. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/os/Message#getData()>
- [#setData(Bundle)](Message.md)) 

### recycle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun recycle(): Unit
```

Return a Message instance to the global pool.

You MUST NOT touch the Message after calling this function because it has effectively been freed. It is an error to recycle a message that is currently enqueued or that is in the process of being delivered to a Handler. 

### sendToTarget

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun sendToTarget(): Unit
```

Sends this Message to the Handler specified by [getTarget](Message.md)). Throws a null pointer exception if this field has not been set. 

### setAsynchronous

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setAsynchronous(async: Boolean): Unit
```

Sets whether the message is asynchronous, meaning that it is not subject to [Looper](Looper.md) synchronization barriers.

Certain operations, such as view invalidation, may introduce synchronization barriers into the [Looper](Looper.md)'s message queue to prevent subsequent messages from being delivered until some condition is met. In the case of view invalidation, messages which are posted after a call to android.view.View#invalidate are suspended by means of a synchronization barrier until the next frame is ready to be drawn. The synchronization barrier ensures that the invalidation request is completely handled before resuming.

Asynchronous messages are exempt from synchronization barriers. They typically represent interrupts, input events, and other signals that must be handled independently even while other work has been suspended.

Note that asynchronous messages may be delivered out of order with respect to synchronous messages although they are always delivered in order among themselves. If the relative order of these messages matters then they probably should not be asynchronous in the first place. Use with caution.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------|
| `async` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):True if the message is asynchronous. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/os/Message#isAsynchronous()> 

### setData

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setData(data: Bundle!): Unit
```

Sets a Bundle of arbitrary data values. Use arg1 and arg2 members as a lower cost way to send a few simple integer values, if you can. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/os/Message#getData()>
- <https://developer.android.com/reference/kotlin/android/os/Message#peekData()> 

### setTarget

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setTarget(target: Handler!): Unit
```  

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<Message!>
```  

### arg1

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var arg1: Int
```

arg1 and arg2 are lower-cost alternatives to using [setData()](Message.md))if you only need to store a few integer values. 

### arg2

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var arg2: Int
```

arg1 and arg2 are lower-cost alternatives to using [setData()](Message.md))if you only need to store a few integer values. 

### obj

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var obj: Any!
```

An arbitrary object to send to the recipient. When using [Messenger](Messenger.md) to send the message across processes this can only be non-null if it contains a Parcelable of a framework class (not one implemented by the application). For other data transfer use [setData](Message.md)).

Note that Parcelable objects here are not supported prior to the [android.os.Build.VERSION_CODES#FROYO](../android/os/Build.VERSION_CODES.md) release. 

### replyTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var replyTo: Messenger!
```

Optional Messenger where replies to this message can be sent. The semantics of exactly how this is used are up to the sender and receiver. 

### sendingUid

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var sendingUid: Int
```

Optional field indicating the uid that sent the message. This is only valid for messages posted by a [Messenger](Messenger.md); otherwise, it will be -1. 

### what

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var what: Int
```

User-defined message code so that the recipient can identify what this message is about. Each [Handler](Handler.md) has its own name-space for message codes, so you do not need to worry about yours conflicting with other handlers. If not specified, this value is 0. Use values other than 0 to indicate custom message codes.
