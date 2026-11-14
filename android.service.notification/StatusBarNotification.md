Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StatusBarNotification

Kotlin | [Java](StatusBarNotification.md)
| --- | --- |

```
open class StatusBarNotification : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.notification.StatusBarNotification](StatusBarNotification.md) |

Class encapsulating a Notification. Sent by the NotificationManagerService to clients including the status bar and any `https://developer.android.com/reference/kotlin/android/service/notification/NotificationListenerService`s.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/service/notification/StatusBarNotification#StatusBarNotification(android.os.Parcel)(in: https://developer.android.com/reference/kotlin/android/os/Parcel.html#!)` <br /> |
| `https://developer.android.com/reference/kotlin/android/service/notification/StatusBarNotification#StatusBarNotification(kotlin.String,%20kotlin.String,%20kotlin.Int,%20kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.app.Notification,%20android.os.UserHandle,%20kotlin.Long)(pkg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, opPkg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, tag: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, initialPid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, score: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, notification: https://developer.android.com/reference/kotlin/android/app/Notification.html#!, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#!, postTime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` <br /> |

| Public methods ||
|---|---|
| open [StatusBarNotification](StatusBarNotification.md)! | `https://developer.android.com/reference/kotlin/android/service/notification/StatusBarNotification#clone()()` Creates and returns a copy of this object. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/notification/StatusBarNotification#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/service/notification/StatusBarNotification#getGroupKey()()` A key that indicates the group with which this message ranks. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/notification/StatusBarNotification#getId()()` The id supplied to `https://developer.android.com/reference/kotlin/android/app/NotificationManager.html#notify(kotlin.Int,%20android.app.Notification)`. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/service/notification/StatusBarNotification#getKey()()` A unique instance key for this notification record. |
| open [Notification](../android.app/Notification.md)! | `https://developer.android.com/reference/kotlin/android/service/notification/StatusBarNotification#getNotification()()` The `https://developer.android.com/reference/kotlin/android/app/Notification.html#` supplied to `https://developer.android.com/reference/kotlin/android/app/NotificationManager.html#notify(kotlin.Int,%20android.app.Notification)`. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/service/notification/StatusBarNotification#getOpPkg()()` The package that posted the notification. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/service/notification/StatusBarNotification#getOverrideGroupKey()()` Returns the override group key. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/service/notification/StatusBarNotification#getPackageName()()` The package that the notification belongs to. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/service/notification/StatusBarNotification#getPostTime()()` The time (in `https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()` time) the notification was posted, which may be different than `https://developer.android.com/reference/kotlin/android/app/Notification.html#when:kotlin.Long`. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/service/notification/StatusBarNotification#getTag()()` The tag supplied to `https://developer.android.com/reference/kotlin/android/app/NotificationManager.html#notify(kotlin.Int,%20android.app.Notification)`, or null if no tag was specified. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/notification/StatusBarNotification#getUid()()` The notifying app's (`https://developer.android.com/reference/kotlin/android/service/notification/StatusBarNotification#getPackageName()`'s) uid. |
| --- | --- |
| open [UserHandle](../android.os/UserHandle.md)! | `https://developer.android.com/reference/kotlin/android/service/notification/StatusBarNotification#getUser()()` The `https://developer.android.com/reference/kotlin/android/os/UserHandle.html#` for whom this notification is intended. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/notification/StatusBarNotification#getUserId()()` Returns a userid for whom this notification is intended. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/service/notification/StatusBarNotification#isAppGroup()()` Returns true if application asked that this notification be part of a group. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/service/notification/StatusBarNotification#isClearable()()` Convenience method to check the notification's flags for either `https://developer.android.com/reference/kotlin/android/app/Notification.html#FLAG_ONGOING_EVENT:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/app/Notification.html#FLAG_NO_CLEAR:kotlin.Int`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/service/notification/StatusBarNotification#isGroup()()` Returns true if this notification is part of a group. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/service/notification/StatusBarNotification#isOngoing()()` Convenience method to check the notification's flags for `https://developer.android.com/reference/kotlin/android/app/Notification.html#FLAG_ONGOING_EVENT:kotlin.Int`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/service/notification/StatusBarNotification#setOverrideGroupKey(kotlin.String)(overrideGroupKey: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Sets the override group key. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/service/notification/StatusBarNotification#toString()()` Returns a string representation of the object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/service/notification/StatusBarNotification#writeToParcel(android.os.Parcel,%20kotlin.Int)(out: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [StatusBarNotification](StatusBarNotification.md)!\> | `https://developer.android.com/reference/kotlin/android/service/notification/StatusBarNotification#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public constructors

### StatusBarNotification

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
StatusBarNotification(in: Parcel!)
```

### StatusBarNotification

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
StatusBarNotification(
    pkg: String!, 
    opPkg: String!, 
    id: Int, 
    tag: String!, 
    uid: Int, 
    initialPid: Int, 
    score: Int, 
    notification: Notification!, 
    user: UserHandle!, 
    postTime: Long)
```

**Deprecated:** *Non-system apps should not need to create StatusBarNotifications.*

## Public methods

### clone

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clone(): StatusBarNotification!
```

Creates and returns a copy of this object. The precise meaning of "copy" may depend on the class of the object. The general intent is that, for any object `x`, the expression:

```kotlin
x.clone() != x
```
will be true, and that the expression:

```kotlin
x.clone().getClass() == x.getClass()
```
will be `true`, but these are not absolute requirements. While it is typically the case that:

```kotlin
x.clone().equals(x)
```
will be `true`, this is not an absolute requirement.

<br />

By convention, the returned object should be obtained by calling `super.clone`. If a class and all of its superclasses (except `Object`) obey this convention, it will be the case that `x.clone().getClass() == x.getClass()`.

By convention, the object returned by this method should be independent of this object (which is being cloned). To achieve this independence, it may be necessary to modify one or more fields of the object returned by `super.clone` before returning it. Typically, this means copying any mutable objects that comprise the internal "deep structure" of the object being cloned and replacing the references to these objects with references to the copies. If a class contains only primitive fields or references to immutable objects, then it is usually the case that no fields in the object returned by `super.clone` need to be modified.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/service/notification/StatusBarNotification#!` | a clone of this instance. |

| Exceptions ||
|---|---|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the `Cloneable` interface. Subclasses that override the `clone` method can also throw this exception to indicate that an instance cannot be cloned. |

### describeContents

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getGroupKey

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getGroupKey(): String!
```

A key that indicates the group with which this message ranks.

### getId

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getId(): Int
```

The id supplied to `https://developer.android.com/reference/kotlin/android/app/NotificationManager.html#notify(kotlin.Int,%20android.app.Notification)`.

### getKey

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getKey(): String!
```

A unique instance key for this notification record.

### getNotification

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNotification(): Notification!
```

The `https://developer.android.com/reference/kotlin/android/app/Notification.html#` supplied to `https://developer.android.com/reference/kotlin/android/app/NotificationManager.html#notify(kotlin.Int,%20android.app.Notification)`.

### getOpPkg

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOpPkg(): String
```

The package that posted the notification.

Might be different from `https://developer.android.com/reference/kotlin/android/service/notification/StatusBarNotification#getPackageName()` if the app owning the notification has a `https://developer.android.com/reference/kotlin/android/app/NotificationManager.html#setNotificationDelegate(kotlin.String)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### getOverrideGroupKey

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOverrideGroupKey(): String!
```

Returns the override group key.

### getPackageName

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPackageName(): String!
```

The package that the notification belongs to.

### getPostTime

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPostTime(): Long
```

The time (in `https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()` time) the notification was posted, which may be different than `https://developer.android.com/reference/kotlin/android/app/Notification.html#when:kotlin.Long`.

### getTag

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTag(): String!
```

The tag supplied to `https://developer.android.com/reference/kotlin/android/app/NotificationManager.html#notify(kotlin.Int,%20android.app.Notification)`, or null if no tag was specified.

### getUid

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getUid(): Int
```

The notifying app's (`https://developer.android.com/reference/kotlin/android/service/notification/StatusBarNotification#getPackageName()`'s) uid.

### getUser

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getUser(): UserHandle!
```

The `https://developer.android.com/reference/kotlin/android/os/UserHandle.html#` for whom this notification is intended.

### getUserId

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getUserId(): Int
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/service/notification/StatusBarNotification#getUser()` instead.*

Returns a userid for whom this notification is intended.

### isAppGroup

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isAppGroup(): Boolean
```

Returns true if application asked that this notification be part of a group.

### isClearable

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isClearable(): Boolean
```

Convenience method to check the notification's flags for either `https://developer.android.com/reference/kotlin/android/app/Notification.html#FLAG_ONGOING_EVENT:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/app/Notification.html#FLAG_NO_CLEAR:kotlin.Int`.

### isGroup

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isGroup(): Boolean
```

Returns true if this notification is part of a group.

### isOngoing

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isOngoing(): Boolean
```

Convenience method to check the notification's flags for `https://developer.android.com/reference/kotlin/android/app/Notification.html#FLAG_ONGOING_EVENT:kotlin.Int`.

### setOverrideGroupKey

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOverrideGroupKey(overrideGroupKey: String!): Unit
```

Sets the override group key.

### toString

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun writeToParcel(
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

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<StatusBarNotification!>
```
