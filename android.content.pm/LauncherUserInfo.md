# LauncherUserInfo

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LauncherUserInfo

Kotlin| [Java](https://developer.android.com/reference/android/content/pm/LauncherUserInfo "View this page in Java") 

```
class LauncherUserInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.content.pm.LauncherUserInfo](https://developer.android.com/reference/kotlin/android/content/pm/LauncherUserInfo#) |

The LauncherUserInfo object holds information about an Android user that is required to display the Launcher related UI elements specific to the user (like badges).

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PRIVATE_SPACE_ENTRYPOINT_HIDDEN](https://developer.android.com/reference/kotlin/android/content/pm/LauncherUserInfo#PRIVATE_SPACE_ENTRYPOINT_HIDDEN:kotlin.String) A boolean extra indicating whether the private space entrypoint should be hidden when locked. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/content/pm/LauncherUserInfo#describeContents())`()` <br /> |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | [getUserConfig](https://developer.android.com/reference/kotlin/android/content/pm/LauncherUserInfo#getUserConfig())`()` Returns additional configs for this launcher user |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getUserSerialNumber](https://developer.android.com/reference/kotlin/android/content/pm/LauncherUserInfo#getUserSerialNumber())`()` Returns serial number of user as returned by [UserManager.getSerialNumberForUser(UserHandle)](https://developer.android.com/reference/kotlin/android/os/UserManager.html#getSerialNumberForUser(android.os.UserHandle)) |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getUserType](https://developer.android.com/reference/kotlin/android/content/pm/LauncherUserInfo#getUserType())`()` Returns type of the user as defined in [UserManager](https://developer.android.com/reference/kotlin/android/os/UserManager.html#). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/content/pm/LauncherUserInfo#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [LauncherUserInfo](https://developer.android.com/reference/kotlin/android/content/pm/LauncherUserInfo#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/content/pm/LauncherUserInfo#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### PRIVATE_SPACE_ENTRYPOINT_HIDDEN

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PRIVATE_SPACE_ENTRYPOINT_HIDDEN: String
```

A boolean extra indicating whether the private space entrypoint should be hidden when locked. 

 Value: "private_space_entrypoint_hidden"

**See Also**

- [#getUserConfig](https://developer.android.com/reference/kotlin/android/content/pm/LauncherUserInfo#getUserConfig())

## Public methods

### describeContents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getUserConfig

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUserConfig(): Bundle
```

Returns additional configs for this launcher user

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | This value cannot be`null`. |

**See Also**

- [#PRIVATE_SPACE_ENTRYPOINT_HIDDEN](https://developer.android.com/reference/kotlin/android/content/pm/LauncherUserInfo#PRIVATE_SPACE_ENTRYPOINT_HIDDEN:kotlin.String) 

### getUserSerialNumber

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUserSerialNumber(): Int
```

Returns serial number of user as returned by [UserManager.getSerialNumberForUser(UserHandle)](https://developer.android.com/reference/kotlin/android/os/UserManager.html#getSerialNumberForUser(android.os.UserHandle))

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the serial number associated with the user |

### getUserType

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUserType(): String
```

Returns type of the user as defined in [UserManager](https://developer.android.com/reference/kotlin/android/os/UserManager.html#). e.g., UserManager.USER_TYPE_PROFILE_MANAGED or UserManager.USER_TYPE_PROFILE_ClONE or UserManager.USER_TYPE_PROFILE_PRIVATE

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the userType for the user whose LauncherUserInfo this is This value cannot be`null`. |

### writeToParcel

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<LauncherUserInfo!>
```
