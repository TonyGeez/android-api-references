# IntentSender

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IntentSender

Kotlin| [Java](IntentSender.md) 
| --- | --- |

```
open class IntentSender : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.IntentSender](IntentSender.md) |

A description of an Intent and target action to perform with it. The returned object can be handed to other applications so that they can perform the action you described on your behalf at a later time.

By giving a IntentSender to another application, you are granting it the right to perform the operation you have specified as if the other application was yourself (with the same permissions and identity). As such, you should be careful about how you build the IntentSender: often, for example, the base Intent you supply will have the component name explicitly set to one of your own components, to ensure it is ultimately sent there and nowhere else.

A IntentSender itself is simply a reference to a token maintained by the system describing the original data used to retrieve it. This means that, even if its owning application's process is killed, the IntentSender itself will remain usable from other processes that have been given it. If the creating application later re-retrieves the same kind of IntentSender (same operation, same Intent action, data, categories, and components, and same flags), it will receive a IntentSender representing the same token if that is still valid.

Instances of this class can not be made directly, but rather must be created from an existing [android.app.PendingIntent](../android.app/PendingIntent.md) with [PendingIntent.getIntentSender()](../android.app/PendingIntent.md)).

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OnFinished](../android/content/IntentSender.OnFinished.md) Callback interface for discovering when a send operation has completed. |
| open | [SendIntentException](../android/content/IntentSender.SendIntentException.md) Exception thrown when trying to send through a PendingIntent that has been canceled or is otherwise no longer able to execute the request. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](IntentSender.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](IntentSender.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Comparison operator on two IntentSender objects, such that true is returned then they both represent the same operation from the same package. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getCreatorPackage](IntentSender.md))`()` Return the package name of the application that created this IntentSender, that is the identity under which you will actually be sending the Intent. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCreatorUid](IntentSender.md))`()` Return the uid of the application that created this PendingIntent, that is the identity under which you will actually be sending the Intent. |
| open [UserHandle](../android.os/UserHandle.md)! | [getCreatorUserHandle](IntentSender.md))`()` Return the user handle of the application that created this PendingIntent, that is the user under which you will actually be sending the Intent. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getTargetPackage](IntentSender.md))`()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](IntentSender.md))`()` <br /> |
| openstatic [IntentSender](IntentSender.md)! | [readIntentSenderOrNullFromParcel](IntentSender.md))`(`in:` ` [Parcel](../android.os/Parcel.md)!`)` Convenience function for reading either a Messenger or`null`pointer from a Parcel. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendIntent](IntentSender.md))`(`context:` ` [Context](Context.md)!`, `code:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `intent:` ` [Intent](Intent.md)!`, `onFinished:` ` [IntentSender.OnFinished](../android/content/IntentSender.OnFinished.md)!`, `handler:` ` [Handler](../android.os/Handler.md)!`)` Perform the operation associated with this IntentSender, allowing the caller to specify information about the Intent to use and be notified when the send has completed. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendIntent](IntentSender.md))`(`context:` ` [Context](Context.md)!`, `code:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `intent:` ` [Intent](Intent.md)!`, `onFinished:` ` [IntentSender.OnFinished](../android/content/IntentSender.OnFinished.md)!`, `handler:` ` [Handler](../android.os/Handler.md)!`, `requiredPermission:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Perform the operation associated with this IntentSender, allowing the caller to specify information about the Intent to use and be notified when the send has completed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendIntent](IntentSender.md))`(`context:` ` [Context](Context.md)?`, `code:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `intent:` ` [Intent](Intent.md)?`, `requiredPermission:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `options:` ` [Bundle](../android.os/Bundle.md)?`, `executor:` ` [Executor](../java.util.concurrent/Executor.md)?`, `onFinished:` ` [IntentSender.OnFinished](../android/content/IntentSender.OnFinished.md)?`)` Perform the operation associated with this IntentSender, allowing the caller to specify information about the Intent to use and be notified when the send has completed. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](IntentSender.md))`()` <br /> |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeIntentSenderOrNullToParcel](IntentSender.md))`(`sender:` ` [IntentSender](IntentSender.md)!`, `out:` ` [Parcel](../android.os/Parcel.md)!`)` Convenience function for writing either a IntentSender or`null`pointer to a Parcel. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](IntentSender.md))`(`out:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [IntentSender](IntentSender.md)!\> | [CREATOR](IntentSender.md) <br /> |

## Public methods

### describeContents

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### equals

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Comparison operator on two IntentSender objects, such that true is returned then they both represent the same operation from the same package.

| Parameters ||
|------------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `otherObj` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getCreatorPackage

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCreatorPackage(): String!
```

Return the package name of the application that created this IntentSender, that is the identity under which you will actually be sending the Intent. The returned string is supplied by the system, so that an application can not spoof its package.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The package name of the PendingIntent, or`null`if there is none associated with it. |

### getCreatorUid

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCreatorUid(): Int
```

Return the uid of the application that created this PendingIntent, that is the identity under which you will actually be sending the Intent. The returned integer is supplied by the system, so that an application can not spoof its uid.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The uid of the PendingIntent, or -1 if there is none associated with it. |

### getCreatorUserHandle

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCreatorUserHandle(): UserHandle!
```

Return the user handle of the application that created this PendingIntent, that is the user under which you will actually be sending the Intent. The returned UserHandle is supplied by the system, so that an application can not spoof its user. See [Process.myUserHandle()](../android.os/Process.md))for more explanation of user handles.

| Return ||
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [UserHandle](../android.os/UserHandle.md)! | The user handle of the PendingIntent,`null`if there is none associated with it. |

### getTargetPackage

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTargetPackage(): String!
```

**Deprecated:** *Renamed to [getCreatorPackage()](IntentSender.md)).* 

### hashCode

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### readIntentSenderOrNullFromParcel

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun readIntentSenderOrNullFromParcel(in: Parcel!): IntentSender!
```

Convenience function for reading either a Messenger or`null`pointer from a Parcel. You must have previously written the Messenger with [writeIntentSenderOrNullToParcel](IntentSender.md)).

| Parameters ||
|------|--------------------------------------------------------------------------------------------------------------------------------|
| `in` | [Parcel](../android.os/Parcel.md)!:The Parcel containing the written Messenger. |

| Return ||
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [IntentSender](IntentSender.md)! | Returns the Messenger read from the Parcel, or @code null} if @code null} had been written. |

### sendIntent

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun sendIntent(
    context: Context!, 
    code: Int, 
    intent: Intent!, 
    onFinished: IntentSender.OnFinished!, 
    handler: Handler!
): Unit
```

Perform the operation associated with this IntentSender, allowing the caller to specify information about the Intent to use and be notified when the send has completed.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](Context.md)!:The Context of the caller. This may be`null`if intent is also`null`. |
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Result code to supply back to the IntentSender's target. |
| `intent` | [Intent](Intent.md)!:Additional Intent data. See [Intent.fillIn()](Intent.md))for information on how this is applied to the original Intent. Use`null`to not modify the original Intent. |
| --- | --- |
| `onFinished` | [IntentSender.OnFinished](../android/content/IntentSender.OnFinished.md)!:The object to call back on when the send has completed, or`null`for no callback. |
| `handler` | [Handler](../android.os/Handler.md)!:Handler identifying the thread on which the callback should happen. If`null`, the callback will happen from the thread pool of the process. |

| Exceptions ||
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| `android.content.IntentSender.SendIntentException` | Throws CanceledIntentException if the IntentSender is no longer allowing more intents to be sent through it. |

### sendIntent

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun sendIntent(
    context: Context!, 
    code: Int, 
    intent: Intent!, 
    onFinished: IntentSender.OnFinished!, 
    handler: Handler!, 
    requiredPermission: String!
): Unit
```

Perform the operation associated with this IntentSender, allowing the caller to specify information about the Intent to use and be notified when the send has completed.

| Parameters ||
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](Context.md)!:The Context of the caller. This may be`null`if intent is also`null`. |
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Result code to supply back to the IntentSender's target. |
| `intent` | [Intent](Intent.md)!:Additional Intent data. See [Intent.fillIn()](Intent.md))for information on how this is applied to the original Intent. Use`null`to not modify the original Intent. |
| --- | --- |
| `onFinished` | [IntentSender.OnFinished](../android/content/IntentSender.OnFinished.md)!:The object to call back on when the send has completed, or`null`for no callback. |
| `handler` | [Handler](../android.os/Handler.md)!:Handler identifying the thread on which the callback should happen. If`null`, the callback will happen from the thread pool of the process. |
| `requiredPermission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Name of permission that a recipient of the PendingIntent is required to hold. This is only valid for broadcast intents, and corresponds to the permission argument in [Context.sendOrderedBroadcast(Intent, String)](Context.md)). If`null`, no permission is required. |
| --- | --- |

| Exceptions ||
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| `android.content.IntentSender.SendIntentException` | Throws CanceledIntentException if the IntentSender is no longer allowing more intents to be sent through it. |

### sendIntent

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun sendIntent(
    context: Context?, 
    code: Int, 
    intent: Intent?, 
    requiredPermission: String?, 
    options: Bundle?, 
    executor: Executor?, 
    onFinished: IntentSender.OnFinished?
): Unit
```

Perform the operation associated with this IntentSender, allowing the caller to specify information about the Intent to use and be notified when the send has completed.

| Parameters ||
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](Context.md)?:The Context of the caller. This may be`null`if intent is also`null`. |
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Result code to supply back to the IntentSender's target. |
| `intent` | [Intent](Intent.md)?:Additional Intent data. See [Intent.fillIn()](Intent.md))for information on how this is applied to the original Intent. Use`null`to not modify the original Intent. |
| --- | --- |
| `onFinished` | [IntentSender.OnFinished](../android/content/IntentSender.OnFinished.md)?:The object to call back on when the send has completed, or`null`for no callback. |
| `executor` | [Executor](../java.util.concurrent/Executor.md)?:Executor identifying the thread on which the callback should happen. If`null`, the callback will happen from the thread pool of the process. |
| `requiredPermission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:Name of permission that a recipient of the PendingIntent is required to hold. This is only valid for broadcast intents, and corresponds to the permission argument in [Context.sendOrderedBroadcast(Intent, String)](Context.md)). If`null`, no permission is required. |
| --- | --- |
| `options` | [Bundle](../android.os/Bundle.md)?:Additional options the caller would like to provide to modify the sending behavior. Typically built from using [ActivityOptions](../android.app/ActivityOptions.md) to apply to an activity start. This value may be`null`. |

| Exceptions ||
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| `android.content.IntentSender.SendIntentException` | Throws CanceledIntentException if the IntentSender is no longer allowing more intents to be sent through it. |

### toString

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeIntentSenderOrNullToParcel

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun writeIntentSenderOrNullToParcel(
    sender: IntentSender!, 
    out: Parcel!
): Unit
```

Convenience function for writing either a IntentSender or`null`pointer to a Parcel. You must use this with [readIntentSenderOrNullFromParcel](IntentSender.md))for later reading it.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| `sender` | [IntentSender](IntentSender.md)!:The IntentSender to write, or`null`. |
| `out` | [Parcel](../android.os/Parcel.md)!:Where to write the IntentSender. |

### writeToParcel

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
    out: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<IntentSender!>
```
