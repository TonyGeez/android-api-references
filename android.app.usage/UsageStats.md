Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UsageStats

Kotlin | [Java](https://developer.android.com/reference/android/app/usage/UsageStats "View this page in Java")
| --- | --- |

```
class UsageStats : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.usage.UsageStats](https://developer.android.com/reference/kotlin/android/app/usage/UsageStats#) |

Contains usage statistics for an app package for a specific time range.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/usage/UsageStats#UsageStats(android.app.usage.UsageStats)(stats: https://developer.android.com/reference/kotlin/android/app/usage/UsageStats#!)` <br /> |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/usage/UsageStats#add(android.app.usage.UsageStats)(right: https://developer.android.com/reference/kotlin/android/app/usage/UsageStats#!)` Add the statistics from the right `https://developer.android.com/reference/kotlin/android/app/usage/UsageStats#` to the left. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/usage/UsageStats#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/usage/UsageStats#getFirstTimeStamp()()` Get the beginning of the time range this `https://developer.android.com/reference/kotlin/android/app/usage/UsageStats#` represents, measured in milliseconds since the epoch. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/usage/UsageStats#getLastTimeForegroundServiceUsed()()` Get the last time this package's foreground service was used, measured in milliseconds since the epoch. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/usage/UsageStats#getLastTimeStamp()()` Get the end of the time range this `https://developer.android.com/reference/kotlin/android/app/usage/UsageStats#` represents, measured in milliseconds since the epoch. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/usage/UsageStats#getLastTimeUsed()()` Get the last time this package's activity was used, measured in milliseconds since the epoch. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/usage/UsageStats#getLastTimeVisible()()` Get the last time this package's activity is visible in the UI, measured in milliseconds since the epoch. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/app/usage/UsageStats#getPackageName()()` <br /> |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/usage/UsageStats#getTotalTimeForegroundServiceUsed()()` Get the total time this package's foreground services are started, measured in milliseconds. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/usage/UsageStats#getTotalTimeInForeground()()` Get the total time this package spent in the foreground, measured in milliseconds. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/usage/UsageStats#getTotalTimeVisible()()` Get the total time this package's activity is visible in the UI, measured in milliseconds. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/usage/UsageStats#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [UsageStats](https://developer.android.com/reference/kotlin/android/app/usage/UsageStats#)!\> | `https://developer.android.com/reference/kotlin/android/app/usage/UsageStats#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public constructors

### UsageStats

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
UsageStats(stats: UsageStats!)
```

## Public methods

### add

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun add(right: UsageStats!): Unit
```

Add the statistics from the right `https://developer.android.com/reference/kotlin/android/app/usage/UsageStats#` to the left. The package name for both `https://developer.android.com/reference/kotlin/android/app/usage/UsageStats#` objects must be the same.

| Parameters ||
|---|---|
| `right` | [UsageStats](https://developer.android.com/reference/kotlin/android/app/usage/UsageStats#)!: The `https://developer.android.com/reference/kotlin/android/app/usage/UsageStats#` object to merge into this one. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the package names of the two `https://developer.android.com/reference/kotlin/android/app/usage/UsageStats#` objects are different. |

### describeContents

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getFirstTimeStamp

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getFirstTimeStamp(): Long
```

Get the beginning of the time range this `https://developer.android.com/reference/kotlin/android/app/usage/UsageStats#` represents, measured in milliseconds since the epoch.

<br />

See `https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()`.

### getLastTimeForegroundServiceUsed

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLastTimeForegroundServiceUsed(): Long
```

Get the last time this package's foreground service was used, measured in milliseconds since the epoch.

<br />

See `https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()`.

### getLastTimeStamp

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLastTimeStamp(): Long
```

Get the end of the time range this `https://developer.android.com/reference/kotlin/android/app/usage/UsageStats#` represents, measured in milliseconds since the epoch.

<br />

See `https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()`.

### getLastTimeUsed

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLastTimeUsed(): Long
```

Get the last time this package's activity was used, measured in milliseconds since the epoch.

<br />

See `https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()`.

### getLastTimeVisible

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLastTimeVisible(): Long
```

Get the last time this package's activity is visible in the UI, measured in milliseconds since the epoch.

### getPackageName

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPackageName(): String!
```

### getTotalTimeForegroundServiceUsed

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTotalTimeForegroundServiceUsed(): Long
```

Get the total time this package's foreground services are started, measured in milliseconds.

### getTotalTimeInForeground

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTotalTimeInForeground(): Long
```

Get the total time this package spent in the foreground, measured in milliseconds. When in the foreground, the user is actively interacting with the app.

### getTotalTimeVisible

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTotalTimeVisible(): Long
```

Get the total time this package's activity is visible in the UI, measured in milliseconds. Note: An app may be visible but not considered foreground. Apps in the foreground must be visible, so visible time includes time in the foreground.

### writeToParcel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<UsageStats!>
```
