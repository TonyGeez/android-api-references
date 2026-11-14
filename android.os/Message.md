# Message

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Message

Kotlin| [Java](https://developer.android.com/reference/android/os/Message "View this page in Java") 
| --- | --- |

```
class Message : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.Message](https://developer.android.com/reference/kotlin/android/os/Message#) |

Defines a message containing a description and arbitrary data object that can be sent to a [Handler](https://developer.android.com/reference/kotlin/android/os/Handler). This object contains two extra int fields and an extra object field that allow you to not do allocations in many cases.

While the constructor of Message is public, the best way to get one of these is to call #obtain or one of the android.os.Handler#obtainMessage methods, which will pull them from a pool of recycled objects.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable) |----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Message](https://developer.android.com/reference/kotlin/android/os/Message#Message())`()` Constructor (but the preferred way to get a Message is to call [Message.obtain()](https://developer.android.com/reference/kotlin/android/os/Message#obtain())). |

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [copyFrom](https://developer.android.com/reference/kotlin/android/os/Message#copyFrom(android.os.Message))`(`o:` ` [Message](https://developer.android.com/reference/kotlin/android/os/Message#)!`)` Make this message like o. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/os/Message#describeContents())`()` <br /> |
| [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)! | [getCallback](https://developer.android.com/reference/kotlin/android/os/Message#getCallback())`()` Retrieve callback object that will execute when this message is handled. |
| --- | --- |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle)! | [getData](https://developer.android.com/reference/kotlin/android/os/Message#getData())`()` Obtains a Bundle of arbitrary data associated with this event, lazily creating it if necessary. |
| [Handler](https://developer.android.com/reference/kotlin/android/os/Handler)! | [getTarget](https://developer.android.com/reference/kotlin/android/os/Message#getTarget())`()` Retrieve the [Handler](https://developer.android.com/reference/kotlin/android/os/Handler) implementation that will receive this message. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getWhen](https://developer.android.com/reference/kotlin/android/os/Message#getWhen())`()` Return the targeted delivery time of this message, in milliseconds. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAsynchronous](https://developer.android.com/reference/kotlin/android/os/Message#isAsynchronous())`()` Returns true if the message is asynchronous, meaning that it is not subject to [Looper](https://developer.android.com/reference/kotlin/android/os/Looper) synchronization barriers. |
| static [Message](https://developer.android.com/reference/kotlin/android/os/Message#)! | [obtain](https://developer.android.com/reference/kotlin/android/os/Message#obtain())`()` Return a new Message instance from the global pool. |
| static [Message](https://developer.android.com/reference/kotlin/android/os/Message#)! | [obtain](https://developer.android.com/reference/kotlin/android/os/Message#obtain(android.os.Handler))`(`h:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler)!`)` Same as [obtain()](https://developer.android.com/reference/kotlin/android/os/Message#obtain()), but sets the value for the*target*member on the Message returned. |
| --- | --- |
| static [Message](https://developer.android.com/reference/kotlin/android/os/Message#)! | [obtain](https://developer.android.com/reference/kotlin/android/os/Message#obtain(android.os.Handler,%20kotlin.Int))`(`h:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler)!`, `what:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Same as [obtain()](https://developer.android.com/reference/kotlin/android/os/Message#obtain()), but sets the values for both*target* and*what*members on the Message. |
| static [Message](https://developer.android.com/reference/kotlin/android/os/Message#)! | [obtain](https://developer.android.com/reference/kotlin/android/os/Message#obtain(android.os.Handler,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`h:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler)!`, `what:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `arg1:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `arg2:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Same as [obtain()](https://developer.android.com/reference/kotlin/android/os/Message#obtain()), but sets the values of the*target* ,*what* ,*arg1* , and*arg2*members. |
| static [Message](https://developer.android.com/reference/kotlin/android/os/Message#)! | [obtain](https://developer.android.com/reference/kotlin/android/os/Message#obtain(android.os.Handler,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Any))`(`h:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler)!`, `what:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `arg1:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `arg2:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Same as [obtain()](https://developer.android.com/reference/kotlin/android/os/Message#obtain()), but sets the values of the*target* ,*what* ,*arg1* ,*arg2* , and*obj*members. |
| --- | --- |
| static [Message](https://developer.android.com/reference/kotlin/android/os/Message#)! | [obtain](https://developer.android.com/reference/kotlin/android/os/Message#obtain(android.os.Handler,%20kotlin.Int,%20kotlin.Any))`(`h:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler)!`, `what:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Same as [obtain()](https://developer.android.com/reference/kotlin/android/os/Message#obtain()), but sets the values of the*target* ,*what* , and*obj*members. |
| static [Message](https://developer.android.com/reference/kotlin/android/os/Message#)! | [obtain](https://developer.android.com/reference/kotlin/android/os/Message#obtain(android.os.Handler,%20java.lang.Runnable))`(`h:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler)!`, `callback:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`)` Same as [obtain(android.os.Handler)](https://developer.android.com/reference/kotlin/android/os/Message#obtain(android.os.Handler)), but assigns a callback Runnable on the Message that is returned. |
| static [Message](https://developer.android.com/reference/kotlin/android/os/Message#)! | [obtain](https://developer.android.com/reference/kotlin/android/os/Message#obtain(android.os.Message))`(`orig:` ` [Message](https://developer.android.com/reference/kotlin/android/os/Message#)!`)` Same as [obtain()](https://developer.android.com/reference/kotlin/android/os/Message#obtain()), but copies the values of an existing message (including its target) into the new one. |
| --- | --- |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle)? | [peekData](https://developer.android.com/reference/kotlin/android/os/Message#peekData())`()` Like getData(), but does not lazily create the Bundle. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [recycle](https://developer.android.com/reference/kotlin/android/os/Message#recycle())`()` Return a Message instance to the global pool. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendToTarget](https://developer.android.com/reference/kotlin/android/os/Message#sendToTarget())`()` Sends this Message to the Handler specified by [getTarget](https://developer.android.com/reference/kotlin/android/os/Message#getTarget()). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAsynchronous](https://developer.android.com/reference/kotlin/android/os/Message#setAsynchronous(kotlin.Boolean))`(`async:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether the message is asynchronous, meaning that it is not subject to [Looper](https://developer.android.com/reference/kotlin/android/os/Looper) synchronization barriers. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setData](https://developer.android.com/reference/kotlin/android/os/Message#setData(android.os.Bundle))`(`data:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle)!`)` Sets a Bundle of arbitrary data values. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTarget](https://developer.android.com/reference/kotlin/android/os/Message#setTarget(android.os.Handler))`(`target:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler)!`)` <br /> |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/os/Message#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Message#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator)\< [Message](https://developer.android.com/reference/kotlin/android/os/Message#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/os/Message#CREATOR:android.os.Parcelable.Creator) <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [arg1](https://developer.android.com/reference/kotlin/android/os/Message#arg1:kotlin.Int) arg1 and arg2 are lower-cost alternatives to using [setData()](https://developer.android.com/reference/kotlin/android/os/Message#setData(android.os.Bundle))if you only need to store a few integer values. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [arg2](https://developer.android.com/reference/kotlin/android/os/Message#arg2:kotlin.Int) arg1 and arg2 are lower-cost alternatives to using [setData()](https://developer.android.com/reference/kotlin/android/os/Message#setData(android.os.Bundle))if you only need to store a few integer values. |
| --- | --- |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [obj](https://developer.android.com/reference/kotlin/android/os/Message#obj:kotlin.Any) An arbitrary object to send to the recipient. |
| [Messenger](https://developer.android.com/reference/kotlin/android/os/Messenger)! | [replyTo](https://developer.android.com/reference/kotlin/android/os/Message#replyTo:android.os.Messenger) Optional Messenger where replies to this message can be sent. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [sendingUid](https://developer.android.com/reference/kotlin/android/os/Message#sendingUid:kotlin.Int) Optional field indicating the uid that sent the message. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [what](https://developer.android.com/reference/kotlin/android/os/Message#what:kotlin.Int) User-defined message code so that the recipient can identify what this message is about. |

## Public constructors

### Message

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Message()
```

Constructor (but the preferred way to get a Message is to call [Message.obtain()](https://developer.android.com/reference/kotlin/android/os/Message#obtain())).

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getCallback

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCallback(): Runnable!
```

Retrieve callback object that will execute when this message is handled. This object must implement Runnable. This is called by the*target* [Handler](https://developer.android.com/reference/kotlin/android/os/Handler) that is receiving this Message to dispatch it. If not set, the message will be dispatched to the receiving Handler's [Handler.handleMessage(Message)](https://developer.android.com/reference/kotlin/android/os/Handler#handleMessage(android.os.Message)). 

### getData

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getData(): Bundle!
```

Obtains a Bundle of arbitrary data associated with this event, lazily creating it if necessary. Set this value by calling [setData(android.os.Bundle)](https://developer.android.com/reference/kotlin/android/os/Message#setData(android.os.Bundle)). Note that when transferring data across processes via [Messenger](https://developer.android.com/reference/kotlin/android/os/Messenger), you will need to set your ClassLoader on the Bundle via [Bundle.setClassLoader()](https://developer.android.com/reference/kotlin/android/os/Bundle#setClassLoader(java.lang.ClassLoader))so that it can instantiate your objects when you retrieve them. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/os/Message#peekData()>
- [#setData(Bundle)](https://developer.android.com/reference/kotlin/android/os/Message#setData(android.os.Bundle)) 

### getTarget

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTarget(): Handler!
```

Retrieve the [Handler](https://developer.android.com/reference/kotlin/android/os/Handler) implementation that will receive this message. The object must implement [Handler.handleMessage()](https://developer.android.com/reference/kotlin/android/os/Handler#handleMessage(android.os.Message)). Each Handler has its own name-space for message codes, so you do not need to worry about yours conflicting with other handlers. 

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

Returns true if the message is asynchronous, meaning that it is not subject to [Looper](https://developer.android.com/reference/kotlin/android/os/Looper) synchronization barriers.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the message is asynchronous. |

**See Also**

- [#setAsynchronous(boolean)](https://developer.android.com/reference/kotlin/android/os/Message#setAsynchronous(kotlin.Boolean)) 

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

Same as [obtain()](https://developer.android.com/reference/kotlin/android/os/Message#obtain()), but sets the value for the*target*member on the Message returned.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `h` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler)!:Handler to assign to the returned Message object's*target*member. |

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------|
| [Message](https://developer.android.com/reference/kotlin/android/os/Message#)! | A Message object from the global pool. |

### obtain

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun obtain(
    h: Handler!, 
    what: Int
): Message!
```

Same as [obtain()](https://developer.android.com/reference/kotlin/android/os/Message#obtain()), but sets the values for both*target* and*what*members on the Message.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------|
| `h` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler)!:Value to assign to the*target*member. |
| `what` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value to assign to the*what*member. |

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------|
| [Message](https://developer.android.com/reference/kotlin/android/os/Message#)! | A Message object from the global pool. |

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

Same as [obtain()](https://developer.android.com/reference/kotlin/android/os/Message#obtain()), but sets the values of the*target* ,*what* ,*arg1* , and*arg2*members.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------|
| `h` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler)!:The*target*value to set. |
| `what` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The*what*value to set. |
| `arg1` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The*arg1*value to set. |
| --- | --- |
| `arg2` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The*arg2*value to set. |

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------|
| [Message](https://developer.android.com/reference/kotlin/android/os/Message#)! | A Message object from the global pool. |

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

Same as [obtain()](https://developer.android.com/reference/kotlin/android/os/Message#obtain()), but sets the values of the*target* ,*what* ,*arg1* ,*arg2* , and*obj*members.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------|
| `h` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler)!:The*target*value to set. |
| `what` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The*what*value to set. |
| `arg1` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The*arg1*value to set. |
| --- | --- |
| `arg2` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The*arg2*value to set. |
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The*obj*value to set. |

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------|
| [Message](https://developer.android.com/reference/kotlin/android/os/Message#)! | A Message object from the global pool. |

### obtain

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun obtain(
    h: Handler!, 
    what: Int, 
    obj: Any!
): Message!
```

Same as [obtain()](https://developer.android.com/reference/kotlin/android/os/Message#obtain()), but sets the values of the*target* ,*what* , and*obj*members.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------|
| `h` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler)!:The*target*value to set. |
| `what` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The*what*value to set. |
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The*object*method to set. |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------|
| [Message](https://developer.android.com/reference/kotlin/android/os/Message#)! | A Message object from the global pool. |

### obtain

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun obtain(
    h: Handler!, 
    callback: Runnable!
): Message!
```

Same as [obtain(android.os.Handler)](https://developer.android.com/reference/kotlin/android/os/Message#obtain(android.os.Handler)), but assigns a callback Runnable on the Message that is returned.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `h` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler)!:Handler to assign to the returned Message object's*target*member. |
| `callback` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!:Runnable that will execute when the message is handled. |

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------|
| [Message](https://developer.android.com/reference/kotlin/android/os/Message#)! | A Message object from the global pool. |

### obtain

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun obtain(orig: Message!): Message!
```

Same as [obtain()](https://developer.android.com/reference/kotlin/android/os/Message#obtain()), but copies the values of an existing message (including its target) into the new one.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------|
| `orig` | [Message](https://developer.android.com/reference/kotlin/android/os/Message#)!:Original message to copy. |

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------|
| [Message](https://developer.android.com/reference/kotlin/android/os/Message#)! | A Message object from the global pool. |

### peekData

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun peekData(): Bundle?
```

Like getData(), but does not lazily create the Bundle. A null is returned if the Bundle does not already exist. See [getData](https://developer.android.com/reference/kotlin/android/os/Message#getData())for further information on this. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/os/Message#getData()>
- [#setData(Bundle)](https://developer.android.com/reference/kotlin/android/os/Message#setData(android.os.Bundle)) 

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

Sends this Message to the Handler specified by [getTarget](https://developer.android.com/reference/kotlin/android/os/Message#getTarget()). Throws a null pointer exception if this field has not been set. 

### setAsynchronous

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setAsynchronous(async: Boolean): Unit
```

Sets whether the message is asynchronous, meaning that it is not subject to [Looper](https://developer.android.com/reference/kotlin/android/os/Looper) synchronization barriers.

Certain operations, such as view invalidation, may introduce synchronization barriers into the [Looper](https://developer.android.com/reference/kotlin/android/os/Looper)'s message queue to prevent subsequent messages from being delivered until some condition is met. In the case of view invalidation, messages which are posted after a call to android.view.View#invalidate are suspended by means of a synchronization barrier until the next frame is ready to be drawn. The synchronization barrier ensures that the invalidation request is completely handled before resuming.

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

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

arg1 and arg2 are lower-cost alternatives to using [setData()](https://developer.android.com/reference/kotlin/android/os/Message#setData(android.os.Bundle))if you only need to store a few integer values. 

### arg2

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var arg2: Int
```

arg1 and arg2 are lower-cost alternatives to using [setData()](https://developer.android.com/reference/kotlin/android/os/Message#setData(android.os.Bundle))if you only need to store a few integer values. 

### obj

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var obj: Any!
```

An arbitrary object to send to the recipient. When using [Messenger](https://developer.android.com/reference/kotlin/android/os/Messenger) to send the message across processes this can only be non-null if it contains a Parcelable of a framework class (not one implemented by the application). For other data transfer use [setData](https://developer.android.com/reference/kotlin/android/os/Message#setData(android.os.Bundle)).

Note that Parcelable objects here are not supported prior to the [android.os.Build.VERSION_CODES#FROYO](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES#FROYO:kotlin.Int) release. 

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

Optional field indicating the uid that sent the message. This is only valid for messages posted by a [Messenger](https://developer.android.com/reference/kotlin/android/os/Messenger); otherwise, it will be -1. 

### what

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var what: Int
```

User-defined message code so that the recipient can identify what this message is about. Each [Handler](https://developer.android.com/reference/kotlin/android/os/Handler) has its own name-space for message codes, so you do not need to worry about yours conflicting with other handlers. If not specified, this value is 0. Use values other than 0 to indicate custom message codes.
