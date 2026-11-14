# RecoverableSecurityException

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RecoverableSecurityException

Kotlin| [Java](https://developer.android.com/reference/android/app/RecoverableSecurityException "View this page in Java") 

```
class RecoverableSecurityException : SecurityException, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) |||
| | | | ↳ | [java.lang.SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#) ||
| | | | | ↳ | [android.app.RecoverableSecurityException](https://developer.android.com/reference/kotlin/android/app/RecoverableSecurityException#) |

Specialization of [SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#) that contains additional information about how to involve the end user to recover from the exception.

This exception is only appropriate where there is a concrete action the user can take to recover and make forward progress, such as confirming or entering authentication credentials, or granting access.

If the receiving app is actively involved with the user, it should present the contained recovery details to help the user make forward progress.

Note: legacy code that receives this exception may treat it as a general [SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#), and thus there is no guarantee that the messages contained will be shown to the end user.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RecoverableSecurityException](https://developer.android.com/reference/kotlin/android/app/RecoverableSecurityException#RecoverableSecurityException(kotlin.Throwable,%20kotlin.CharSequence,%20android.app.RemoteAction))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`, `userMessage:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)`, `userAction:` ` [RemoteAction](https://developer.android.com/reference/kotlin/android/app/RemoteAction)`)` Create an instance ready to be thrown. |

| Public methods ||
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/app/RecoverableSecurityException#describeContents())`()` <br /> |
| [RemoteAction](https://developer.android.com/reference/kotlin/android/app/RemoteAction) | [getUserAction](https://developer.android.com/reference/kotlin/android/app/RecoverableSecurityException#getUserAction())`()` Return primary action that will initiate the recovery. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [getUserMessage](https://developer.android.com/reference/kotlin/android/app/RecoverableSecurityException#getUserMessage())`()` Return short message describing the issue for end user audiences, which may be shown in a notification or dialog. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/app/RecoverableSecurityException#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [RecoverableSecurityException](https://developer.android.com/reference/kotlin/android/app/RecoverableSecurityException#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/app/RecoverableSecurityException#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public constructors

### RecoverableSecurityException

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RecoverableSecurityException(
    cause: Throwable, 
    userMessage: CharSequence, 
    userAction: RemoteAction)
```

Create an instance ready to be thrown.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html):original cause with details designed for engineering audiences. This value cannot be`null`. |
| `userMessage` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html):short message describing the issue for end user audiences, which may be shown in a notification or dialog. This should be localized and less than 64 characters. For example:*PIN required to access Document.pdf* This value cannot be`null`. |
| `userAction` | [RemoteAction](https://developer.android.com/reference/kotlin/android/app/RemoteAction):primary action that will initiate the recovery. The title should be localized and less than 24 characters. For example:*Enter PIN* . This action must launch an activity that is expected to set [Activity.setResult(int)](https://developer.android.com/reference/kotlin/android/app/Activity#setResult(kotlin.Int))before finishing to communicate the final status of the recovery. For example, apps that observe [Activity.RESULT_OK](https://developer.android.com/reference/kotlin/android/app/Activity#RESULT_OK:kotlin.Int) may choose to immediately retry their operation. This value cannot be`null`. |

## Public methods

### describeContents

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getUserAction

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUserAction(): RemoteAction
```

Return primary action that will initiate the recovery.

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------|
| [RemoteAction](https://developer.android.com/reference/kotlin/android/app/RemoteAction) | This value cannot be`null`. |

### getUserMessage

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUserMessage(): CharSequence
```

Return short message describing the issue for end user audiences, which may be shown in a notification or dialog.

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | This value cannot be`null`. |

### writeToParcel

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<RecoverableSecurityException!>
```
