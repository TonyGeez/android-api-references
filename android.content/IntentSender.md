# IntentSender

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IntentSender

Kotlin| [Java](https://developer.android.com/reference/android/content/IntentSender "View this page in Java") 
| --- | --- |

```
open class IntentSender : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender#) |

A description of an Intent and target action to perform with it. The returned object can be handed to other applications so that they can perform the action you described on your behalf at a later time.

By giving a IntentSender to another application, you are granting it the right to perform the operation you have specified as if the other application was yourself (with the same permissions and identity). As such, you should be careful about how you build the IntentSender: often, for example, the base Intent you supply will have the component name explicitly set to one of your own components, to ensure it is ultimately sent there and nowhere else.

A IntentSender itself is simply a reference to a token maintained by the system describing the original data used to retrieve it. This means that, even if its owning application's process is killed, the IntentSender itself will remain usable from other processes that have been given it. If the creating application later re-retrieves the same kind of IntentSender (same operation, same Intent action, data, categories, and components, and same flags), it will receive a IntentSender representing the same token if that is still valid.

Instances of this class can not be made directly, but rather must be created from an existing [android.app.PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#) with [PendingIntent.getIntentSender()](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#getIntentSender()).

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OnFinished](https://developer.android.com/reference/kotlin/android/content/IntentSender.OnFinished) Callback interface for discovering when a send operation has completed. |
| open | [SendIntentException](https://developer.android.com/reference/kotlin/android/content/IntentSender.SendIntentException) Exception thrown when trying to send through a PendingIntent that has been canceled or is otherwise no longer able to execute the request. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/content/IntentSender#describeContents())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/content/IntentSender#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Comparison operator on two IntentSender objects, such that true is returned then they both represent the same operation from the same package. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getCreatorPackage](https://developer.android.com/reference/kotlin/android/content/IntentSender#getCreatorPackage())`()` Return the package name of the application that created this IntentSender, that is the identity under which you will actually be sending the Intent. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCreatorUid](https://developer.android.com/reference/kotlin/android/content/IntentSender#getCreatorUid())`()` Return the uid of the application that created this PendingIntent, that is the identity under which you will actually be sending the Intent. |
| open [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle.html#)! | [getCreatorUserHandle](https://developer.android.com/reference/kotlin/android/content/IntentSender#getCreatorUserHandle())`()` Return the user handle of the application that created this PendingIntent, that is the user under which you will actually be sending the Intent. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getTargetPackage](https://developer.android.com/reference/kotlin/android/content/IntentSender#getTargetPackage())`()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/content/IntentSender#hashCode())`()` <br /> |
| openstatic [IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender#)! | [readIntentSenderOrNullFromParcel](https://developer.android.com/reference/kotlin/android/content/IntentSender#readIntentSenderOrNullFromParcel(android.os.Parcel))`(`in:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)!`)` Convenience function for reading either a Messenger or`null`pointer from a Parcel. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendIntent](https://developer.android.com/reference/kotlin/android/content/IntentSender#sendIntent(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20android.content.IntentSender.OnFinished,%20android.os.Handler))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context)!`, `code:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent)!`, `onFinished:` ` [IntentSender.OnFinished](https://developer.android.com/reference/kotlin/android/content/IntentSender.OnFinished)!`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!`)` Perform the operation associated with this IntentSender, allowing the caller to specify information about the Intent to use and be notified when the send has completed. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendIntent](https://developer.android.com/reference/kotlin/android/content/IntentSender#sendIntent(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20android.content.IntentSender.OnFinished,%20android.os.Handler,%20kotlin.String))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context)!`, `code:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent)!`, `onFinished:` ` [IntentSender.OnFinished](https://developer.android.com/reference/kotlin/android/content/IntentSender.OnFinished)!`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!`, `requiredPermission:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Perform the operation associated with this IntentSender, allowing the caller to specify information about the Intent to use and be notified when the send has completed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendIntent](https://developer.android.com/reference/kotlin/android/content/IntentSender#sendIntent(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20kotlin.String,%20android.os.Bundle,%20java.util.concurrent.Executor,%20android.content.IntentSender.OnFinished))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context)?`, `code:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent)?`, `requiredPermission:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `options:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)?`, `onFinished:` ` [IntentSender.OnFinished](https://developer.android.com/reference/kotlin/android/content/IntentSender.OnFinished)?`)` Perform the operation associated with this IntentSender, allowing the caller to specify information about the Intent to use and be notified when the send has completed. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/content/IntentSender#toString())`()` <br /> |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeIntentSenderOrNullToParcel](https://developer.android.com/reference/kotlin/android/content/IntentSender#writeIntentSenderOrNullToParcel(android.content.IntentSender,%20android.os.Parcel))`(`sender:` ` [IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender#)!`, `out:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)!`)` Convenience function for writing either a IntentSender or`null`pointer to a Parcel. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/content/IntentSender#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`out:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/content/IntentSender#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public methods

### describeContents

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

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

Return the user handle of the application that created this PendingIntent, that is the user under which you will actually be sending the Intent. The returned UserHandle is supplied by the system, so that an application can not spoof its user. See [Process.myUserHandle()](https://developer.android.com/reference/kotlin/android/os/Process.html#myUserHandle())for more explanation of user handles.

| Return ||
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle.html#)! | The user handle of the PendingIntent,`null`if there is none associated with it. |

### getTargetPackage

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTargetPackage(): String!
```

**Deprecated:** *Renamed to [getCreatorPackage()](https://developer.android.com/reference/kotlin/android/content/IntentSender#getCreatorPackage()).* 

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

Convenience function for reading either a Messenger or`null`pointer from a Parcel. You must have previously written the Messenger with [writeIntentSenderOrNullToParcel](https://developer.android.com/reference/kotlin/android/content/IntentSender#writeIntentSenderOrNullToParcel(android.content.IntentSender,%20android.os.Parcel)).

| Parameters ||
|------|--------------------------------------------------------------------------------------------------------------------------------|
| `in` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)!:The Parcel containing the written Messenger. |

| Return ||
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender#)! | Returns the Messenger read from the Parcel, or @code null} if @code null} had been written. |

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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context)!:The Context of the caller. This may be`null`if intent is also`null`. |
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Result code to supply back to the IntentSender's target. |
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent)!:Additional Intent data. See [Intent.fillIn()](https://developer.android.com/reference/kotlin/android/content/Intent#fillIn(android.content.Intent,%20kotlin.Int))for information on how this is applied to the original Intent. Use`null`to not modify the original Intent. |
| --- | --- |
| `onFinished` | [IntentSender.OnFinished](https://developer.android.com/reference/kotlin/android/content/IntentSender.OnFinished)!:The object to call back on when the send has completed, or`null`for no callback. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!:Handler identifying the thread on which the callback should happen. If`null`, the callback will happen from the thread pool of the process. |

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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context)!:The Context of the caller. This may be`null`if intent is also`null`. |
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Result code to supply back to the IntentSender's target. |
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent)!:Additional Intent data. See [Intent.fillIn()](https://developer.android.com/reference/kotlin/android/content/Intent#fillIn(android.content.Intent,%20kotlin.Int))for information on how this is applied to the original Intent. Use`null`to not modify the original Intent. |
| --- | --- |
| `onFinished` | [IntentSender.OnFinished](https://developer.android.com/reference/kotlin/android/content/IntentSender.OnFinished)!:The object to call back on when the send has completed, or`null`for no callback. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!:Handler identifying the thread on which the callback should happen. If`null`, the callback will happen from the thread pool of the process. |
| `requiredPermission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Name of permission that a recipient of the PendingIntent is required to hold. This is only valid for broadcast intents, and corresponds to the permission argument in [Context.sendOrderedBroadcast(Intent, String)](https://developer.android.com/reference/kotlin/android/content/Context#sendBroadcast(android.content.Intent,%20kotlin.String)). If`null`, no permission is required. |
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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context)?:The Context of the caller. This may be`null`if intent is also`null`. |
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Result code to supply back to the IntentSender's target. |
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent)?:Additional Intent data. See [Intent.fillIn()](https://developer.android.com/reference/kotlin/android/content/Intent#fillIn(android.content.Intent,%20kotlin.Int))for information on how this is applied to the original Intent. Use`null`to not modify the original Intent. |
| --- | --- |
| `onFinished` | [IntentSender.OnFinished](https://developer.android.com/reference/kotlin/android/content/IntentSender.OnFinished)?:The object to call back on when the send has completed, or`null`for no callback. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)?:Executor identifying the thread on which the callback should happen. If`null`, the callback will happen from the thread pool of the process. |
| `requiredPermission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:Name of permission that a recipient of the PendingIntent is required to hold. This is only valid for broadcast intents, and corresponds to the permission argument in [Context.sendOrderedBroadcast(Intent, String)](https://developer.android.com/reference/kotlin/android/content/Context#sendBroadcast(android.content.Intent,%20kotlin.String)). If`null`, no permission is required. |
| --- | --- |
| `options` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:Additional options the caller would like to provide to modify the sending behavior. Typically built from using [ActivityOptions](https://developer.android.com/reference/kotlin/android/app/ActivityOptions.html#) to apply to an activity start. This value may be`null`. |

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

Convenience function for writing either a IntentSender or`null`pointer to a Parcel. You must use this with [readIntentSenderOrNullFromParcel](https://developer.android.com/reference/kotlin/android/content/IntentSender#readIntentSenderOrNullFromParcel(android.os.Parcel))for later reading it.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| `sender` | [IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender#)!:The IntentSender to write, or`null`. |
| `out` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)!:Where to write the IntentSender. |

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
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<IntentSender!>
```
