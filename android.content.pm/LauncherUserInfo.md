# LauncherUserInfo

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LauncherUserInfo

Kotlin| [Java](LauncherUserInfo.md) 
| --- | --- |

```
class LauncherUserInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.pm.LauncherUserInfo](LauncherUserInfo.md) |

The LauncherUserInfo object holds information about an Android user that is required to display the Launcher related UI elements specific to the user (like badges).

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PRIVATE_SPACE_ENTRYPOINT_HIDDEN](LauncherUserInfo.md) A boolean extra indicating whether the private space entrypoint should be hidden when locked. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](LauncherUserInfo.md))`()` <br /> |
| [Bundle](../android.os/Bundle.md) | [getUserConfig](LauncherUserInfo.md))`()` Returns additional configs for this launcher user |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getUserSerialNumber](LauncherUserInfo.md))`()` Returns serial number of user as returned by [UserManager.getSerialNumberForUser(UserHandle)](../android.os/UserManager.md)) |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getUserType](LauncherUserInfo.md))`()` Returns type of the user as defined in [UserManager](../android.os/UserManager.md). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](LauncherUserInfo.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [LauncherUserInfo](LauncherUserInfo.md)!\> | [CREATOR](LauncherUserInfo.md) <br /> |

## Constants

### PRIVATE_SPACE_ENTRYPOINT_HIDDEN

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PRIVATE_SPACE_ENTRYPOINT_HIDDEN: String
```

A boolean extra indicating whether the private space entrypoint should be hidden when locked. 

 Value: "private_space_entrypoint_hidden"

**See Also**

- [#getUserConfig](LauncherUserInfo.md))

## Public methods

### describeContents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### getUserConfig

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUserConfig(): Bundle
```

Returns additional configs for this launcher user

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [Bundle](../android.os/Bundle.md) | This value cannot be`null`. |

**See Also**

- [#PRIVATE_SPACE_ENTRYPOINT_HIDDEN](LauncherUserInfo.md) 

### getUserSerialNumber

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUserSerialNumber(): Int
```

Returns serial number of user as returned by [UserManager.getSerialNumberForUser(UserHandle)](../android.os/UserManager.md))

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the serial number associated with the user |

### getUserType

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUserType(): String
```

Returns type of the user as defined in [UserManager](../android.os/UserManager.md). e.g., UserManager.USER_TYPE_PROFILE_MANAGED or UserManager.USER_TYPE_PROFILE_ClONE or UserManager.USER_TYPE_PROFILE_PRIVATE

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
| `dest` | [Parcel](../android.os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<LauncherUserInfo!>
```
