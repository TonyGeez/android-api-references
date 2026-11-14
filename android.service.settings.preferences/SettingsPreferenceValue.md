Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SettingsPreferenceValue

```
class SettingsPreferenceValue : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.settings.preferences.SettingsPreferenceValue](../android/service/settings/preferences/SettingsPreferenceValue.md) |

This objects represents a value that can be used for a particular settings preference.

The data type for the value will correspond to `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceValue#getType()`. For possible types, see constants below, such as `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceValue#TYPE_BOOLEAN:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceValue#TYPE_STRING:kotlin.Int`. Depending on the type, the corresponding getter will contain its value.

See documentation on the constants for which getter method should be used.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceValue.Builder` Builder to construct `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceValue#`. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceValue#TYPE_BOOLEAN:kotlin.Int` Value is of type boolean. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceValue#TYPE_DOUBLE:kotlin.Int` Value is of type double. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceValue#TYPE_INT:kotlin.Int` Value is of type int. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceValue#TYPE_LONG:kotlin.Int` Value is of type long. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceValue#TYPE_STRING:kotlin.Int` Value is of type string. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceValue#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceValue#getBooleanValue()()` Returns the boolean value for Preference, the type must be `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceValue#TYPE_BOOLEAN:kotlin.Int`. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceValue#getDoubleValue()()` Returns the double value for Preference, the type must be `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceValue#TYPE_DOUBLE:kotlin.Int`. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceValue#getIntValue()()` Returns the int value for Preference, the type must be `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceValue#TYPE_INT:kotlin.Int`. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceValue#getLongValue()()` Returns the long value for Preference, the type must be `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceValue#TYPE_LONG:kotlin.Int`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceValue#getStringValue()()` Returns the string value for Preference, the type must be `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceValue#TYPE_STRING:kotlin.Int`. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceValue#getType()()` Returns the type indicator for Preference value. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceValue#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [SettingsPreferenceValue](../android/service/settings/preferences/SettingsPreferenceValue.md)!\> | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceValue#CREATOR:android.os.Parcelable.Creator` Parcelable Creator for `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceValue#`. |

## Constants

### TYPE_BOOLEAN

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_BOOLEAN: Int
```

Value is of type boolean. Access via `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceValue#getBooleanValue()`.

 Value: 0

### TYPE_DOUBLE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_DOUBLE: Int
```

Value is of type double. Access via `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceValue#getDoubleValue()`.

 Value: 2

### TYPE_INT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_INT: Int
```

Value is of type int. Access via `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceValue#getIntValue()`.

 Value: 4

### TYPE_LONG

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_LONG: Int
```

Value is of type long. Access via `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceValue#getLongValue()`.

 Value: 1

### TYPE_STRING

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_STRING: Int
```

Value is of type string. Access via `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceValue#getStringValue()`.

 Value: 3

## Public methods

### describeContents

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getBooleanValue

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getBooleanValue(): Boolean
```

Returns the boolean value for Preference, the type must be `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceValue#TYPE_BOOLEAN:kotlin.Int`.

### getDoubleValue

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDoubleValue(): Double
```

Returns the double value for Preference, the type must be `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceValue#TYPE_DOUBLE:kotlin.Int`.

### getIntValue

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getIntValue(): Int
```

Returns the int value for Preference, the type must be `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceValue#TYPE_INT:kotlin.Int`.

### getLongValue

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLongValue(): Long
```

Returns the long value for Preference, the type must be `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceValue#TYPE_LONG:kotlin.Int`.

### getStringValue

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getStringValue(): String?
```

Returns the string value for Preference, the type must be `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceValue#TYPE_STRING:kotlin.Int`.

### getType

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getType(): Int
```

Returns the type indicator for Preference value.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceValue#TYPE_BOOLEAN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceValue#TYPE_LONG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceValue#TYPE_DOUBLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceValue#TYPE_STRING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceValue#TYPE_INT:kotlin.Int` |

### writeToParcel

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android/os/Parcel.md): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<SettingsPreferenceValue!>
```

Parcelable Creator for `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceValue#`.
