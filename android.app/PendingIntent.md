Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PendingIntent

Kotlin | [Java](https://developer.android.com/reference/android/app/PendingIntent "View this page in Java")
| --- | --- |

```
class PendingIntent : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent#) |

A description of an Intent and target action to perform with it. Instances of this class are created with #getActivity, #getActivities, `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getBroadcast(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int)`, and `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getService(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int)`; the returned object can be handed to other applications so that they can perform the action you described on your behalf at a later time.

By giving a PendingIntent to another application, you are granting it the right to perform the operation you have specified as if the other application was yourself (with the same permissions and identity). As such, you should be careful about how you build the PendingIntent: almost always, for example, the base Intent you supply should have the component name explicitly set to one of your own components, to ensure it is ultimately sent there and nowhere else.

A PendingIntent itself is simply a reference to a token maintained by the system describing the original data used to retrieve it. This means that, even if its owning application's process is killed, the PendingIntent itself will remain usable from other processes that have been given it. If the creating application later re-retrieves the same kind of PendingIntent (same operation, same Intent action, data, categories, and components, and same flags), it will receive a PendingIntent representing the same token if that is still valid, and can thus call `https://developer.android.com/reference/kotlin/android/app/PendingIntent#cancel()` to remove it.

Because of this behavior, it is important to know when two Intents are considered to be the same for purposes of retrieving a PendingIntent. A common mistake people make is to create multiple PendingIntent objects with Intents that only vary in their "extra" contents, expecting to get a different PendingIntent each time. This does *not* happen. The parts of the Intent that are used for matching are the same ones defined by `https://developer.android.com/reference/kotlin/android/content/Intent.html#filterEquals(android.content.Intent)`. If you use two Intent objects that are equivalent as per `https://developer.android.com/reference/kotlin/android/content/Intent.html#filterEquals(android.content.Intent)`, then you will get the same PendingIntent for both of them.

There are two typical ways to deal with this.

If you truly need multiple distinct PendingIntent objects active at the same time (such as to use as two notifications that are both shown at the same time), then you will need to ensure there is something that is different about them to associate them with different PendingIntents. This may be any of the Intent attributes considered by `https://developer.android.com/reference/kotlin/android/content/Intent.html#filterEquals(android.content.Intent)`, or different request code integers supplied to #getActivity, #getActivities, `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getBroadcast(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int)`, or `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getService(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int)`.

If you only need one PendingIntent active at a time for any of the Intents you will use, then you can alternatively use the flags `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_CANCEL_CURRENT:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_UPDATE_CURRENT:kotlin.Int` to either cancel or modify whatever current PendingIntent is associated with the Intent you are supplying.

Also note that flags like `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_ONE_SHOT:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_IMMUTABLE:kotlin.Int` describe the PendingIntent instance and thus, are used to identify it. Any calls to retrieve or modify a PendingIntent created with these flags will also require these flags to be supplied in conjunction with others. E.g. To retrieve an existing PendingIntent created with FLAG_ONE_SHOT, **both** FLAG_ONE_SHOT and FLAG_NO_CREATE need to be supplied.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/app/PendingIntent.CanceledException` Exception thrown when trying to send through a PendingIntent that has been canceled or is otherwise no longer able to execute the request. |
| abstract | `https://developer.android.com/reference/kotlin/android/app/PendingIntent.OnFinished` Callback interface for discovering when a send operation has completed. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_ALLOW_UNSAFE_IMPLICIT_INTENT:kotlin.Int` Flag indicating that the created PendingIntent with `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_MUTABLE:kotlin.Int` is allowed to have an unsafe implicit Intent within. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_CANCEL_CURRENT:kotlin.Int` Flag indicating that if the described PendingIntent already exists, the current one should be canceled before generating a new one. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_IMMUTABLE:kotlin.Int` Flag indicating that the created PendingIntent should be immutable. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_MUTABLE:kotlin.Int` Flag indicating that the created PendingIntent should be mutable. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_NO_CREATE:kotlin.Int` Flag indicating that if the described PendingIntent does not already exist, then simply return null instead of creating it. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_ONE_SHOT:kotlin.Int` Flag indicating that this PendingIntent can be used only once. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_UPDATE_CURRENT:kotlin.Int` Flag indicating that if the described PendingIntent already exists, then keep it but replace its extra data with what is in this new Intent. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/PendingIntent#cancel()()` Cancel a currently active PendingIntent. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/PendingIntent#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/PendingIntent#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Comparison operator on two PendingIntent objects, such that true is returned then they both represent the same operation from the same package. |
| --- | --- |
| static [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent#)! | `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getActivities(android.content.Context,%20kotlin.Int,%20kotlin.Array,%20kotlin.Int)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, requestCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, intents: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/content/Intent.html#!>, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Like `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getActivity(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int)`, but allows an array of Intents to be supplied. |
| static [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent#)! | `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getActivities(android.content.Context,%20kotlin.Int,%20kotlin.Array,%20kotlin.Int,%20android.os.Bundle)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, requestCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, intents: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/content/Intent.html#!>, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Like `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getActivity(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int)`, but allows an array of Intents to be supplied. |
| static [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent#)! | `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getActivity(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, requestCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Retrieve a PendingIntent that will start a new activity, like calling `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent)`. |
| --- | --- |
| static [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent#)! | `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getActivity(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int,%20android.os.Bundle)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, requestCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Retrieve a PendingIntent that will start a new activity, like calling `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent)`. |
| static [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent#)! | `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getBroadcast(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, requestCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Retrieve a PendingIntent that will perform a broadcast, like calling `https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent)`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getCreatorPackage()()` Return the package name of the application that created this PendingIntent, that is the identity under which you will actually be sending the Intent. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getCreatorUid()()` Return the uid of the application that created this PendingIntent, that is the identity under which you will actually be sending the Intent. |
| [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle.html#) | `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getCreatorUserHandle()()` Return the user handle of the application that created this PendingIntent, that is the user under which you will actually be sending the Intent. |
| static [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent#)! | `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getForegroundService(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, requestCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Retrieve a PendingIntent that will start a foreground service, like calling `https://developer.android.com/reference/kotlin/android/content/Context.html#startForegroundService(android.content.Intent)`. |
| --- | --- |
| [IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender.html#) | `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getIntentSender()()` Retrieve a IntentSender object that wraps the existing sender of the PendingIntent |
| static [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent#)! | `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getService(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, requestCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Retrieve a PendingIntent that will start a service, like calling `https://developer.android.com/reference/kotlin/android/content/Context.html#startService(android.content.Intent)`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getTargetPackage()()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/PendingIntent#hashCode()()` Returns a hash code value for the object. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/PendingIntent#isActivity()()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/PendingIntent#isBroadcast()()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/PendingIntent#isForegroundService()()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/PendingIntent#isImmutable()()` Check if this PendingIntent is marked with `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_IMMUTABLE:kotlin.Int`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/PendingIntent#isService()()` <br /> |
| --- | --- |
| static [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent#)? | `https://developer.android.com/reference/kotlin/android/app/PendingIntent#readPendingIntentOrNullFromParcel(android.os.Parcel)(in: https://developer.android.com/reference/kotlin/android/os/Parcel.html#)` Convenience function for reading either a PendingIntent or null pointer from a Parcel. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/PendingIntent#send()()` Perform the operation associated with this PendingIntent. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/PendingIntent#send(android.content.Context,%20kotlin.Int,%20android.content.Intent)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, code: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#?)` Perform the operation associated with this PendingIntent, allowing the caller to specify information about the Intent to use. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/PendingIntent#send(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20android.app.PendingIntent.OnFinished,%20android.os.Handler)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, code: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#?, onFinished: https://developer.android.com/reference/kotlin/android/app/PendingIntent.OnFinished?, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?)` Perform the operation associated with this PendingIntent, allowing the caller to specify information about the Intent to use and be notified when the send has completed. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/PendingIntent#send(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20android.app.PendingIntent.OnFinished,%20android.os.Handler,%20kotlin.String)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, code: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#?, onFinished: https://developer.android.com/reference/kotlin/android/app/PendingIntent.OnFinished?, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?, requiredPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Perform the operation associated with this PendingIntent, allowing the caller to specify information about the Intent to use and be notified when the send has completed. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/PendingIntent#send(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20android.app.PendingIntent.OnFinished,%20android.os.Handler,%20kotlin.String,%20android.os.Bundle)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, code: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#?, onFinished: https://developer.android.com/reference/kotlin/android/app/PendingIntent.OnFinished?, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?, requiredPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Perform the operation associated with this PendingIntent, allowing the caller to specify information about the Intent to use and be notified when the send has completed. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/PendingIntent#send(android.os.Bundle)(options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Perform the operation associated with this PendingIntent, supplying additional options for the operation. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/PendingIntent#send(kotlin.Int)(code: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Perform the operation associated with this PendingIntent. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/PendingIntent#send(kotlin.Int,%20android.app.PendingIntent.OnFinished,%20android.os.Handler)(code: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, onFinished: https://developer.android.com/reference/kotlin/android/app/PendingIntent.OnFinished?, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?)` Perform the operation associated with this PendingIntent, allowing the caller to be notified when the send has completed. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/PendingIntent#toString()()` Returns a string representation of the object. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/PendingIntent#writePendingIntentOrNullToParcel(android.app.PendingIntent,%20android.os.Parcel)(sender: https://developer.android.com/reference/kotlin/android/app/PendingIntent#?, out: https://developer.android.com/reference/kotlin/android/os/Parcel.html#)` Convenience function for writing either a PendingIntent or null pointer to a Parcel. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/PendingIntent#writeToParcel(android.os.Parcel,%20kotlin.Int)(out: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent#)!\> | `https://developer.android.com/reference/kotlin/android/app/PendingIntent#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### FLAG_ALLOW_UNSAFE_IMPLICIT_INTENT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_ALLOW_UNSAFE_IMPLICIT_INTENT: Int
```

Flag indicating that the created PendingIntent with `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_MUTABLE:kotlin.Int` is allowed to have an unsafe implicit Intent within.

Starting with `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, for apps that target SDK `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int` or higher, creation of a PendingIntent with `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_MUTABLE:kotlin.Int` and an implicit Intent within will throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` for security reasons. To bypass this check, use `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_ALLOW_UNSAFE_IMPLICIT_INTENT:kotlin.Int` when creating a PendingIntent. However, it is strongly recommended to not to use this flag and make the Intent explicit or the PendingIntent immutable, thereby making the Intent safe.

 Value: 16777216

### FLAG_CANCEL_CURRENT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_CANCEL_CURRENT: Int
```

Flag indicating that if the described PendingIntent already exists, the current one should be canceled before generating a new one. For use with #getActivity, `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getBroadcast(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int)`, and `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getService(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int)`.

You can use this to retrieve a new PendingIntent when you are only changing the extra data in the Intent; by canceling the previous pending intent, this ensures that only entities given the new data will be able to launch it. If this assurance is not an issue, consider `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_UPDATE_CURRENT:kotlin.Int`.

 Value: 268435456

### FLAG_IMMUTABLE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_IMMUTABLE: Int
```

Flag indicating that the created PendingIntent should be immutable. This means that the additional intent argument passed to the send methods to fill in unpopulated properties of this intent will be ignored.

`https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_IMMUTABLE:kotlin.Int` only limits the ability to alter the semantics of the intent that is sent by #send by the invoker of #send. The creator of the PendingIntent can always update the PendingIntent itself via `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_UPDATE_CURRENT:kotlin.Int`.

 Value: 67108864

### FLAG_MUTABLE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_MUTABLE: Int
```

Flag indicating that the created PendingIntent should be mutable. This flag cannot be combined with `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_IMMUTABLE:kotlin.Int`.

Up until `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int`, PendingIntents are assumed to be mutable by default, unless `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_IMMUTABLE:kotlin.Int` is set. Starting with `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, it will be required to explicitly specify the mutability of PendingIntents on creation with either `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_IMMUTABLE:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_MUTABLE:kotlin.Int`. It is strongly recommended to use `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_IMMUTABLE:kotlin.Int` when creating a PendingIntent. `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_MUTABLE:kotlin.Int` should only be used when some functionality relies on modifying the underlying intent, e.g. any PendingIntent that needs to be used with inline reply or bubbles.

 Value: 33554432

### FLAG_NO_CREATE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_NO_CREATE: Int
```

Flag indicating that if the described PendingIntent does not already exist, then simply return null instead of creating it. For use with #getActivity, `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getBroadcast(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int)`, and `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getService(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int)`.

 Value: 536870912

### FLAG_ONE_SHOT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_ONE_SHOT: Int
```

Flag indicating that this PendingIntent can be used only once. For use with #getActivity, `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getBroadcast(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int)`, and `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getService(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int)`.

If set, after `https://developer.android.com/reference/kotlin/android/app/PendingIntent#send()` is called on it, it will be automatically canceled for you and any future attempt to send through it will fail.

 Value: 1073741824

### FLAG_UPDATE_CURRENT

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_UPDATE_CURRENT: Int
```

Flag indicating that if the described PendingIntent already exists, then keep it but replace its extra data with what is in this new Intent. For use with #getActivity, `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getBroadcast(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int)`, and `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getService(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int)`.

This can be used if you are creating intents where only the extras change, and don't care that any entities that received your previous PendingIntent will be able to launch it with your new extras even if they are not explicitly given to it.

`https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_UPDATE_CURRENT:kotlin.Int` still works even if `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_IMMUTABLE:kotlin.Int` is set - the creator of the PendingIntent can always update the PendingIntent itself. The IMMUTABLE flag only limits the ability to alter the semantics of the intent that is sent by #send by the invoker of #send.

 Value: 134217728

## Public methods

### cancel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun cancel(): Unit
```

Cancel a currently active PendingIntent. Only the original application owning a PendingIntent can cancel it.

### describeContents

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Comparison operator on two PendingIntent objects, such that true is returned then they both represent the same operation from the same package. This allows you to use #getActivity, `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getBroadcast(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int)`, or `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getService(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int)` multiple times (even across a process being killed), resulting in different PendingIntent objects but whose equals() method identifies them as being the same operation.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |
| `otherObj` | This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getActivities

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getActivities(
    context: Context!, 
    requestCode: Int, 
    intents: Array<Intent!>, 
    flags: Int
): PendingIntent!
```

Like `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getActivity(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int)`, but allows an array of Intents to be supplied. The last Intent in the array is taken as the primary key for the PendingIntent, like the single Intent given to `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getActivity(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int)`. Upon sending the resulting PendingIntent, all of the Intents are started in the same way as they would be by passing them to `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivities(kotlin.Array)`.

The *first* intent in the array will be started outside of the context of an existing activity, so you must use the `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_NEW_TASK:kotlin.Int` launch flag in the Intent. (Activities after the first in the array are started in the context of the previous activity in the array, so FLAG_ACTIVITY_NEW_TASK is not needed nor desired for them.)

The *last* intent in the array represents the key for the PendingIntent. In other words, it is the significant element for matching (as done with the single intent given to `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getActivity(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int)`, its content will be the subject of replacement by `https://developer.android.com/reference/kotlin/android/app/PendingIntent#send(android.content.Context,%20kotlin.Int,%20android.content.Intent)` and `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_UPDATE_CURRENT:kotlin.Int`, etc. This is because it is the most specific of the supplied intents, and the UI the user actually sees when the intents are started.

For security reasons, the `https://developer.android.com/reference/kotlin/android/content/Intent.html#` objects you supply here should almost always be *explicit intents* , that is specify an explicit component to be delivered to through `https://developer.android.com/reference/kotlin/android/content/Intent.html#setClass(android.content.Context,%20java.lang.Class)`

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: The Context in which this PendingIntent should start the activity. |
| `requestCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Private request code for the sender |
| `intents` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!\>: Array of Intents of the activities to be launched. This value cannot be `null`. |
| --- | --- |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): May be `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_ONE_SHOT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_NO_CREATE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_CANCEL_CURRENT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_UPDATE_CURRENT:kotlin.Int`, or any of the flags as supported by `https://developer.android.com/reference/kotlin/android/content/Intent.html#fillIn(android.content.Intent,%20kotlin.Int)` to control which unspecified parts of the intent that can be supplied when the actual send happens. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_ONE_SHOT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_NO_CREATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_CANCEL_CURRENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_UPDATE_CURRENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_IMMUTABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_MUTABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_ALLOW_UNSAFE_IMPLICIT_INTENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_ACTION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_DATA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_CATEGORIES:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_COMPONENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_PACKAGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_SOURCE_BOUNDS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_SELECTOR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_CLIP_DATA:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/PendingIntent#!` | Returns an existing or new PendingIntent matching the given parameters. May return null only if `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_NO_CREATE:kotlin.Int` has been supplied. |

### getActivities

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getActivities(
    context: Context!, 
    requestCode: Int, 
    intents: Array<Intent!>, 
    flags: Int, 
    options: Bundle?
): PendingIntent!
```

Like `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getActivity(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int)`, but allows an array of Intents to be supplied. The last Intent in the array is taken as the primary key for the PendingIntent, like the single Intent given to `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getActivity(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int)`. Upon sending the resulting PendingIntent, all of the Intents are started in the same way as they would be by passing them to `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivities(kotlin.Array)`.

The *first* intent in the array will be started outside of the context of an existing activity, so you must use the `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_NEW_TASK:kotlin.Int` launch flag in the Intent. (Activities after the first in the array are started in the context of the previous activity in the array, so FLAG_ACTIVITY_NEW_TASK is not needed nor desired for them.)

The *last* intent in the array represents the key for the PendingIntent. In other words, it is the significant element for matching (as done with the single intent given to `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getActivity(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int)`, its content will be the subject of replacement by `https://developer.android.com/reference/kotlin/android/app/PendingIntent#send(android.content.Context,%20kotlin.Int,%20android.content.Intent)` and `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_UPDATE_CURRENT:kotlin.Int`, etc. This is because it is the most specific of the supplied intents, and the UI the user actually sees when the intents are started.

For security reasons, the `https://developer.android.com/reference/kotlin/android/content/Intent.html#` objects you supply here should almost always be *explicit intents* , that is specify an explicit component to be delivered to through `https://developer.android.com/reference/kotlin/android/content/Intent.html#setClass(android.content.Context,%20java.lang.Class)`

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: The Context in which this PendingIntent should start the activity. |
| `requestCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Private request code for the sender |
| `intents` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!\>: Array of Intents of the activities to be launched. This value cannot be `null`. |
| --- | --- |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): May be `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_ONE_SHOT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_NO_CREATE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_CANCEL_CURRENT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_UPDATE_CURRENT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_IMMUTABLE:kotlin.Int` or any of the flags as supported by `https://developer.android.com/reference/kotlin/android/content/Intent.html#fillIn(android.content.Intent,%20kotlin.Int)` to control which unspecified parts of the intent that can be supplied when the actual send happens. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_ONE_SHOT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_NO_CREATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_CANCEL_CURRENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_UPDATE_CURRENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_IMMUTABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_MUTABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_ALLOW_UNSAFE_IMPLICIT_INTENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_ACTION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_DATA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_CATEGORIES:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_COMPONENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_PACKAGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_SOURCE_BOUNDS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_SELECTOR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_CLIP_DATA:kotlin.Int` |
| `options` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?: This value may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/PendingIntent#!` | Returns an existing or new PendingIntent matching the given parameters. May return null only if `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_NO_CREATE:kotlin.Int` has been supplied. |

### getActivity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getActivity(
    context: Context!, 
    requestCode: Int, 
    intent: Intent!, 
    flags: Int
): PendingIntent!
```

Retrieve a PendingIntent that will start a new activity, like calling `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent)`. Note that the activity will be started outside of the context of an existing activity, so you must use the `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_NEW_TASK:kotlin.Int` launch flag in the Intent.

For security reasons, the `https://developer.android.com/reference/kotlin/android/content/Intent.html#` you supply here should almost always be an *explicit intent* , that is specify an explicit component to be delivered to through `https://developer.android.com/reference/kotlin/android/content/Intent.html#setClass(android.content.Context,%20java.lang.Class)`

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: The Context in which this PendingIntent should start the activity. |
| `requestCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Private request code for the sender |
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!: Intent of the activity to be launched. |
| --- | --- |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): May be `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_ONE_SHOT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_NO_CREATE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_CANCEL_CURRENT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_UPDATE_CURRENT:kotlin.Int`, or any of the flags as supported by `https://developer.android.com/reference/kotlin/android/content/Intent.html#fillIn(android.content.Intent,%20kotlin.Int)` to control which unspecified parts of the intent that can be supplied when the actual send happens. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_ONE_SHOT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_NO_CREATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_CANCEL_CURRENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_UPDATE_CURRENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_IMMUTABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_MUTABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_ALLOW_UNSAFE_IMPLICIT_INTENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_ACTION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_DATA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_CATEGORIES:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_COMPONENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_PACKAGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_SOURCE_BOUNDS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_SELECTOR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_CLIP_DATA:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/PendingIntent#!` | Returns an existing or new PendingIntent matching the given parameters. May return null only if `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_NO_CREATE:kotlin.Int` has been supplied. |

### getActivity

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getActivity(
    context: Context!, 
    requestCode: Int, 
    intent: Intent, 
    flags: Int, 
    options: Bundle?
): PendingIntent!
```

Retrieve a PendingIntent that will start a new activity, like calling `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent)`. Note that the activity will be started outside of the context of an existing activity, so you must use the `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_NEW_TASK:kotlin.Int` launch flag in the Intent.

For security reasons, the `https://developer.android.com/reference/kotlin/android/content/Intent.html#` you supply here should almost always be an *explicit intent* , that is specify an explicit component to be delivered to through `https://developer.android.com/reference/kotlin/android/content/Intent.html#setClass(android.content.Context,%20java.lang.Class)`

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: The Context in which this PendingIntent should start the activity. |
| `requestCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Private request code for the sender |
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#): Intent of the activity to be launched. This value cannot be `null`. |
| --- | --- |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): May be `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_ONE_SHOT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_NO_CREATE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_CANCEL_CURRENT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_UPDATE_CURRENT:kotlin.Int`, or any of the flags as supported by `https://developer.android.com/reference/kotlin/android/content/Intent.html#fillIn(android.content.Intent,%20kotlin.Int)` to control which unspecified parts of the intent that can be supplied when the actual send happens. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_ONE_SHOT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_NO_CREATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_CANCEL_CURRENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_UPDATE_CURRENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_IMMUTABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_MUTABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_ALLOW_UNSAFE_IMPLICIT_INTENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_ACTION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_DATA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_CATEGORIES:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_COMPONENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_PACKAGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_SOURCE_BOUNDS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_SELECTOR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_CLIP_DATA:kotlin.Int` |
| `options` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?: Additional options for how the Activity should be started. May be null if there are no options. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/PendingIntent#!` | Returns an existing or new PendingIntent matching the given parameters. May return null only if `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_NO_CREATE:kotlin.Int` has been supplied. |

### getBroadcast

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getBroadcast(
    context: Context!, 
    requestCode: Int, 
    intent: Intent, 
    flags: Int
): PendingIntent!
```

Retrieve a PendingIntent that will perform a broadcast, like calling `https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent)`.

For security reasons, the `https://developer.android.com/reference/kotlin/android/content/Intent.html#` you supply here should almost always be an *explicit intent* , that is specify an explicit component to be delivered to through `https://developer.android.com/reference/kotlin/android/content/Intent.html#setClass(android.content.Context,%20java.lang.Class)`

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: The Context in which this PendingIntent should perform the broadcast. |
| `requestCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Private request code for the sender |
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#): The Intent to be broadcast. This value cannot be `null`. |
| --- | --- |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): May be `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_ONE_SHOT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_NO_CREATE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_CANCEL_CURRENT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_UPDATE_CURRENT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_IMMUTABLE:kotlin.Int` or any of the flags as supported by `https://developer.android.com/reference/kotlin/android/content/Intent.html#fillIn(android.content.Intent,%20kotlin.Int)` to control which unspecified parts of the intent that can be supplied when the actual send happens. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_ONE_SHOT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_NO_CREATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_CANCEL_CURRENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_UPDATE_CURRENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_IMMUTABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_MUTABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_ALLOW_UNSAFE_IMPLICIT_INTENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_ACTION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_DATA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_CATEGORIES:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_COMPONENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_PACKAGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_SOURCE_BOUNDS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_SELECTOR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_CLIP_DATA:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/PendingIntent#!` | Returns an existing or new PendingIntent matching the given parameters. May return null only if `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_NO_CREATE:kotlin.Int` has been supplied. |

### getCreatorPackage

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCreatorPackage(): String?
```

Return the package name of the application that created this PendingIntent, that is the identity under which you will actually be sending the Intent. The returned string is supplied by the system, so that an application can not spoof its package.

Be careful about how you use this. All this tells you is who created the PendingIntent. It does **not** tell you who handed the PendingIntent to you: that is, PendingIntent objects are intended to be passed between applications, so the PendingIntent you receive from an application could actually be one it received from another application, meaning the result you get here will identify the original application. Because of this, you should only use this information to identify who you expect to be interacting with through a #send call, not who gave you the PendingIntent.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | The package name of the PendingIntent. This value may be `null`. |

### getCreatorUid

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCreatorUid(): Int
```

Return the uid of the application that created this PendingIntent, that is the identity under which you will actually be sending the Intent. The returned integer is supplied by the system, so that an application can not spoof its uid.

Be careful about how you use this. All this tells you is who created the PendingIntent. It does **not** tell you who handed the PendingIntent to you: that is, PendingIntent objects are intended to be passed between applications, so the PendingIntent you receive from an application could actually be one it received from another application, meaning the result you get here will identify the original application. Because of this, you should only use this information to identify who you expect to be interacting with through a #send call, not who gave you the PendingIntent.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The uid of the PendingIntent, or -1 if there is none associated with it. |

### getCreatorUserHandle

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCreatorUserHandle(): UserHandle
```

Return the user handle of the application that created this PendingIntent, that is the user under which you will actually be sending the Intent. The returned UserHandle is supplied by the system, so that an application can not spoof its user. See `https://developer.android.com/reference/kotlin/android/os/Process.html#myUserHandle()` for more explanation of user handles.

Be careful about how you use this. All this tells you is who created the PendingIntent. It does **not** tell you who handed the PendingIntent to you: that is, PendingIntent objects are intended to be passed between applications, so the PendingIntent you receive from an application could actually be one it received from another application, meaning the result you get here will identify the original application. Because of this, you should only use this information to identify who you expect to be interacting with through a #send call, not who gave you the PendingIntent.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/UserHandle.html#` | The user handle of the PendingIntent. This value cannot be `null`. |

### getForegroundService

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getForegroundService(
    context: Context!, 
    requestCode: Int, 
    intent: Intent, 
    flags: Int
): PendingIntent!
```

Retrieve a PendingIntent that will start a foreground service, like calling `https://developer.android.com/reference/kotlin/android/content/Context.html#startForegroundService(android.content.Intent)`. The start arguments given to the service will come from the extras of the Intent.

For security reasons, the `https://developer.android.com/reference/kotlin/android/content/Intent.html#` you supply here should almost always be an *explicit intent* , that is specify an explicit component to be delivered to through `https://developer.android.com/reference/kotlin/android/content/Intent.html#setClass(android.content.Context,%20java.lang.Class)`

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: The Context in which this PendingIntent should start the service. |
| `requestCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Private request code for the sender |
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#): An Intent describing the service to be started. This value cannot be `null`. |
| --- | --- |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): May be `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_ONE_SHOT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_NO_CREATE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_CANCEL_CURRENT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_UPDATE_CURRENT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_IMMUTABLE:kotlin.Int` or any of the flags as supported by `https://developer.android.com/reference/kotlin/android/content/Intent.html#fillIn(android.content.Intent,%20kotlin.Int)` to control which unspecified parts of the intent that can be supplied when the actual send happens. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_ONE_SHOT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_NO_CREATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_CANCEL_CURRENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_UPDATE_CURRENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_IMMUTABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_MUTABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_ALLOW_UNSAFE_IMPLICIT_INTENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_ACTION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_DATA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_CATEGORIES:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_COMPONENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_PACKAGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_SOURCE_BOUNDS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_SELECTOR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_CLIP_DATA:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/PendingIntent#!` | Returns an existing or new PendingIntent matching the given parameters. May return null only if `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_NO_CREATE:kotlin.Int` has been supplied. |

### getIntentSender

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getIntentSender(): IntentSender
```

Retrieve a IntentSender object that wraps the existing sender of the PendingIntent

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/IntentSender.html#` | Returns a IntentSender object that wraps the sender of PendingIntent. This value cannot be `null`. |

### getService

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getService(
    context: Context!, 
    requestCode: Int, 
    intent: Intent, 
    flags: Int
): PendingIntent!
```

Retrieve a PendingIntent that will start a service, like calling `https://developer.android.com/reference/kotlin/android/content/Context.html#startService(android.content.Intent)`. The start arguments given to the service will come from the extras of the Intent.

For security reasons, the `https://developer.android.com/reference/kotlin/android/content/Intent.html#` you supply here should almost always be an *explicit intent* , that is specify an explicit component to be delivered to through `https://developer.android.com/reference/kotlin/android/content/Intent.html#setClass(android.content.Context,%20java.lang.Class)`

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: The Context in which this PendingIntent should start the service. |
| `requestCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Private request code for the sender |
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#): An Intent describing the service to be started. This value cannot be `null`. |
| --- | --- |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): May be `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_ONE_SHOT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_NO_CREATE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_CANCEL_CURRENT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_UPDATE_CURRENT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_IMMUTABLE:kotlin.Int` or any of the flags as supported by `https://developer.android.com/reference/kotlin/android/content/Intent.html#fillIn(android.content.Intent,%20kotlin.Int)` to control which unspecified parts of the intent that can be supplied when the actual send happens. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_ONE_SHOT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_NO_CREATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_CANCEL_CURRENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_UPDATE_CURRENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_IMMUTABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_MUTABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_ALLOW_UNSAFE_IMPLICIT_INTENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_ACTION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_DATA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_CATEGORIES:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_COMPONENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_PACKAGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_SOURCE_BOUNDS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_SELECTOR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_CLIP_DATA:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/PendingIntent#!` | Returns an existing or new PendingIntent matching the given parameters. May return null only if `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_NO_CREATE:kotlin.Int` has been supplied. |

### getTargetPackage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTargetPackage(): String?
```

**Deprecated:** *Renamed to `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getCreatorPackage()`.*

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | This value may be `null`. |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### isActivity

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isActivity(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | TRUE if this `https://developer.android.com/reference/kotlin/android/app/PendingIntent#` was created with #getActivity or #getActivities. |

### isBroadcast

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isBroadcast(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | TRUE if this `https://developer.android.com/reference/kotlin/android/app/PendingIntent#` was created with `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getBroadcast(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int)`. |

### isForegroundService

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isForegroundService(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | TRUE if this `https://developer.android.com/reference/kotlin/android/app/PendingIntent#` was created with `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getForegroundService(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int)`. |

### isImmutable

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isImmutable(): Boolean
```

Check if this PendingIntent is marked with `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_IMMUTABLE:kotlin.Int`.

### isService

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isService(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | TRUE if this `https://developer.android.com/reference/kotlin/android/app/PendingIntent#` was created with `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getService(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int)`. |

### readPendingIntentOrNullFromParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun readPendingIntentOrNullFromParcel(in: Parcel): PendingIntent?
```

Convenience function for reading either a PendingIntent or null pointer from a Parcel. You must have previously written the PendingIntent with `https://developer.android.com/reference/kotlin/android/app/PendingIntent#writePendingIntentOrNullToParcel(android.app.PendingIntent,%20android.os.Parcel)`.

| Parameters ||
|---|---|
| `in` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): The Parcel containing the written PendingIntent. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/PendingIntent#?` | Returns the PendingIntent read from the Parcel, or null if null had been written. |

### send

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun send(): Unit
```

Perform the operation associated with this PendingIntent.

| Exceptions ||
|---|---|
| `android.app.PendingIntent.CanceledException` | Throws CanceledException if the PendingIntent is no longer allowing more intents to be sent through it. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/PendingIntent#send(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20android.app.PendingIntent.OnFinished,%20android.os.Handler,%20kotlin.String,%20android.os.Bundle)`

### send

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun send(
    context: Context!, 
    code: Int, 
    intent: Intent?
): Unit
```

Perform the operation associated with this PendingIntent, allowing the caller to specify information about the Intent to use.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: The Context of the caller. |
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Result code to supply back to the PendingIntent's target. |
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)?: Additional Intent data. See `https://developer.android.com/reference/kotlin/android/content/Intent.html#fillIn(android.content.Intent,%20kotlin.Int)` for information on how this is applied to the original Intent. If flag `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_IMMUTABLE:kotlin.Int` was set when this pending intent was created, this argument will be ignored. This value may be `null`. |
| --- | --- |

| Exceptions ||
|---|---|
| `android.app.PendingIntent.CanceledException` | Throws CanceledException if the PendingIntent is no longer allowing more intents to be sent through it. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/PendingIntent#send(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20android.app.PendingIntent.OnFinished,%20android.os.Handler,%20kotlin.String,%20android.os.Bundle)`

### send

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun send(
    context: Context!, 
    code: Int, 
    intent: Intent?, 
    onFinished: PendingIntent.OnFinished?, 
    handler: Handler?
): Unit
```

Perform the operation associated with this PendingIntent, allowing the caller to specify information about the Intent to use and be notified when the send has completed.

For the intent parameter, a PendingIntent often has restrictions on which fields can be supplied here, based on how the PendingIntent was retrieved in #getActivity, `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getBroadcast(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int)`, or `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getService(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int)`.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: The Context of the caller. This may be null if intent is also null. |
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Result code to supply back to the PendingIntent's target. |
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)?: Additional Intent data. See `https://developer.android.com/reference/kotlin/android/content/Intent.html#fillIn(android.content.Intent,%20kotlin.Int)` for information on how this is applied to the original Intent. Use null to not modify the original Intent. If flag `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_IMMUTABLE:kotlin.Int` was set when this pending intent was created, this argument will be ignored. |
| --- | --- |
| `onFinished` | [PendingIntent.OnFinished](https://developer.android.com/reference/kotlin/android/app/PendingIntent.OnFinished)?: The object to call back on when the send has completed, or null for no callback. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?: Handler identifying the thread on which the callback should happen. If null, the callback will happen from the thread pool of the process. |

| Exceptions ||
|---|---|
| `android.app.PendingIntent.CanceledException` | Throws CanceledException if the PendingIntent is no longer allowing more intents to be sent through it. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/PendingIntent#send(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20android.app.PendingIntent.OnFinished,%20android.os.Handler,%20kotlin.String,%20android.os.Bundle)`

### send

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun send(
    context: Context!, 
    code: Int, 
    intent: Intent?, 
    onFinished: PendingIntent.OnFinished?, 
    handler: Handler?, 
    requiredPermission: String?
): Unit
```

Perform the operation associated with this PendingIntent, allowing the caller to specify information about the Intent to use and be notified when the send has completed.

For the intent parameter, a PendingIntent often has restrictions on which fields can be supplied here, based on how the PendingIntent was retrieved in #getActivity, `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getBroadcast(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int)`, or `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getService(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int)`.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: The Context of the caller. This may be null if intent is also null. |
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Result code to supply back to the PendingIntent's target. |
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)?: Additional Intent data. See `https://developer.android.com/reference/kotlin/android/content/Intent.html#fillIn(android.content.Intent,%20kotlin.Int)` for information on how this is applied to the original Intent. Use null to not modify the original Intent. If flag `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_IMMUTABLE:kotlin.Int` was set when this pending intent was created, this argument will be ignored. |
| --- | --- |
| `onFinished` | [PendingIntent.OnFinished](https://developer.android.com/reference/kotlin/android/app/PendingIntent.OnFinished)?: The object to call back on when the send has completed, or null for no callback. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?: Handler identifying the thread on which the callback should happen. If null, the callback will happen from the thread pool of the process. |
| `requiredPermission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: Name of permission that a recipient of the PendingIntent is required to hold. This is only valid for broadcast intents, and corresponds to the permission argument in `https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent,%20kotlin.String)`. If null, no permission is required. |
| --- | --- |

| Exceptions ||
|---|---|
| `android.app.PendingIntent.CanceledException` | Throws CanceledException if the PendingIntent is no longer allowing more intents to be sent through it. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/PendingIntent#send(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20android.app.PendingIntent.OnFinished,%20android.os.Handler,%20kotlin.String,%20android.os.Bundle)`

### send

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun send(
    context: Context!, 
    code: Int, 
    intent: Intent?, 
    onFinished: PendingIntent.OnFinished?, 
    handler: Handler?, 
    requiredPermission: String?, 
    options: Bundle?
): Unit
```

Perform the operation associated with this PendingIntent, allowing the caller to specify information about the Intent to use and be notified when the send has completed.

For the intent parameter, a PendingIntent often has restrictions on which fields can be supplied here, based on how the PendingIntent was retrieved in #getActivity, `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getBroadcast(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int)`, or `https://developer.android.com/reference/kotlin/android/app/PendingIntent#getService(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int)`.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: The Context of the caller. This may be null if intent is also null. |
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Result code to supply back to the PendingIntent's target. |
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)?: Additional Intent data. See `https://developer.android.com/reference/kotlin/android/content/Intent.html#fillIn(android.content.Intent,%20kotlin.Int)` for information on how this is applied to the original Intent. Use null to not modify the original Intent. If flag `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_IMMUTABLE:kotlin.Int` was set when this pending intent was created, this argument will be ignored. |
| --- | --- |
| `onFinished` | [PendingIntent.OnFinished](https://developer.android.com/reference/kotlin/android/app/PendingIntent.OnFinished)?: The object to call back on when the send has completed, or null for no callback. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?: Handler identifying the thread on which the callback should happen. If null, the callback will happen from the thread pool of the process. |
| `requiredPermission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: Name of permission that a recipient of the PendingIntent is required to hold. This is only valid for broadcast intents, and corresponds to the permission argument in `https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent,%20kotlin.String)`. If null, no permission is required. |
| --- | --- |
| `options` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?: Additional options the caller would like to provide to modify the sending behavior. May be built from an `https://developer.android.com/reference/kotlin/android/app/ActivityOptions` to apply to an activity start. This value may be `null`. |

| Exceptions ||
|---|---|
| `android.app.PendingIntent.CanceledException` | Throws CanceledException if the PendingIntent is no longer allowing more intents to be sent through it. |

### send

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun send(options: Bundle?): Unit
```

Perform the operation associated with this PendingIntent, supplying additional options for the operation.

| Parameters ||
|---|---|
| `options` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?: Additional options the caller would like to provide to modify the sending behavior. May be built from an `https://developer.android.com/reference/kotlin/android/app/ActivityOptions` to apply to an activity start. This value may be `null`. |

| Exceptions ||
|---|---|
| `android.app.PendingIntent.CanceledException` | Throws CanceledException if the PendingIntent is no longer allowing more intents to be sent through it. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/PendingIntent#send(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20android.app.PendingIntent.OnFinished,%20android.os.Handler,%20kotlin.String)`

### send

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun send(code: Int): Unit
```

Perform the operation associated with this PendingIntent.

| Parameters ||
|---|---|
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Result code to supply back to the PendingIntent's target. |

| Exceptions ||
|---|---|
| `android.app.PendingIntent.CanceledException` | Throws CanceledException if the PendingIntent is no longer allowing more intents to be sent through it. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/PendingIntent#send(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20android.app.PendingIntent.OnFinished,%20android.os.Handler,%20kotlin.String,%20android.os.Bundle)`

### send

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun send(
    code: Int, 
    onFinished: PendingIntent.OnFinished?, 
    handler: Handler?
): Unit
```

Perform the operation associated with this PendingIntent, allowing the caller to be notified when the send has completed.

| Parameters ||
|---|---|
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Result code to supply back to the PendingIntent's target. |
| `onFinished` | [PendingIntent.OnFinished](https://developer.android.com/reference/kotlin/android/app/PendingIntent.OnFinished)?: The object to call back on when the send has completed, or null for no callback. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?: Handler identifying the thread on which the callback should happen. If null, the callback will happen from the thread pool of the process. |
| --- | --- |

| Exceptions ||
|---|---|
| `android.app.PendingIntent.CanceledException` | Throws CanceledException if the PendingIntent is no longer allowing more intents to be sent through it. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/PendingIntent#send(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20android.app.PendingIntent.OnFinished,%20android.os.Handler,%20kotlin.String,%20android.os.Bundle)`

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writePendingIntentOrNullToParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun writePendingIntentOrNullToParcel(
    sender: PendingIntent?, 
    out: Parcel
): Unit
```

Convenience function for writing either a PendingIntent or null pointer to a Parcel. You must use this with `https://developer.android.com/reference/kotlin/android/app/PendingIntent#readPendingIntentOrNullFromParcel(android.os.Parcel)` for later reading it.

| Parameters ||
|---|---|
| `sender` | [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent#)?: The PendingIntent to write, or null. |
| `out` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): Where to write the PendingIntent. This value cannot be `null`. |

### writeToParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    out: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<PendingIntent!>
```
