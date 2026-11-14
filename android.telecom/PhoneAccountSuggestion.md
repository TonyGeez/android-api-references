# PhoneAccountSuggestion

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PhoneAccountSuggestion

Kotlin| [Java](../android/telecom/PhoneAccountSuggestion.md) 
| --- | --- |

```
class PhoneAccountSuggestion : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telecom.PhoneAccountSuggestion](../android/telecom/PhoneAccountSuggestion.md) |

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REASON_FREQUENT](../android/telecom/PhoneAccountSuggestion.md) Indicates that the [PhoneAccountHandle](../android/telecom/PhoneAccountHandle.md) is suggested because the user uses it frequently for the number that we are calling. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REASON_INTRA_CARRIER](../android/telecom/PhoneAccountSuggestion.md) Indicates that the [PhoneAccountHandle](../android/telecom/PhoneAccountHandle.md) is suggested because the number we're calling is on the same carrier, and therefore may have lower rates. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REASON_NONE](../android/telecom/PhoneAccountSuggestion.md) Indicates that this account is not suggested for use, but is still available. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REASON_OTHER](../android/telecom/PhoneAccountSuggestion.md) Indicates that the [PhoneAccountHandle](../android/telecom/PhoneAccountHandle.md) is suggested for a reason not otherwise enumerated here. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REASON_USER_SET](../android/telecom/PhoneAccountSuggestion.md) Indicates that the [PhoneAccountHandle](../android/telecom/PhoneAccountHandle.md) is suggested because the user explicitly specified that it be used for the number we are calling. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PhoneAccountSuggestion](../android/telecom/PhoneAccountSuggestion.md))`(`handle:` ` [PhoneAccountHandle](../android/telecom/PhoneAccountHandle.md)`, `reason:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `shouldAutoSelect:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a new instance of [PhoneAccountSuggestion](../android/telecom/PhoneAccountSuggestion.md). |

| Public methods ||
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/telecom/PhoneAccountSuggestion.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/telecom/PhoneAccountSuggestion.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [PhoneAccountHandle](../android/telecom/PhoneAccountHandle.md) | [getPhoneAccountHandle](../android/telecom/PhoneAccountSuggestion.md))`()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getReason](../android/telecom/PhoneAccountSuggestion.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/telecom/PhoneAccountSuggestion.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [shouldAutoSelect](../android/telecom/PhoneAccountSuggestion.md))`()` Suggests whether the dialer should automatically place the call using this account without user interaction. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/telecom/PhoneAccountSuggestion.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [PhoneAccountSuggestion](../android/telecom/PhoneAccountSuggestion.md)!\> | [CREATOR](../android/telecom/PhoneAccountSuggestion.md) <br /> |

## Constants

### REASON_FREQUENT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REASON_FREQUENT: Int
```

Indicates that the [PhoneAccountHandle](../android/telecom/PhoneAccountHandle.md) is suggested because the user uses it frequently for the number that we are calling. 

 Value: 2

### REASON_INTRA_CARRIER

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REASON_INTRA_CARRIER: Int
```

Indicates that the [PhoneAccountHandle](../android/telecom/PhoneAccountHandle.md) is suggested because the number we're calling is on the same carrier, and therefore may have lower rates. 

 Value: 1

### REASON_NONE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REASON_NONE: Int
```

Indicates that this account is not suggested for use, but is still available. 

 Value: 0

### REASON_OTHER

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REASON_OTHER: Int
```

Indicates that the [PhoneAccountHandle](../android/telecom/PhoneAccountHandle.md) is suggested for a reason not otherwise enumerated here. 

 Value: 4

### REASON_USER_SET

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REASON_USER_SET: Int
```

Indicates that the [PhoneAccountHandle](../android/telecom/PhoneAccountHandle.md) is suggested because the user explicitly specified that it be used for the number we are calling. 

 Value: 3

## Public constructors

### PhoneAccountSuggestion

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PhoneAccountSuggestion(
    handle: PhoneAccountHandle, 
    reason: Int, 
    shouldAutoSelect: Boolean)
```

Creates a new instance of [PhoneAccountSuggestion](../android/telecom/PhoneAccountSuggestion.md). This constructor is intended for use by apps implementing a`PhoneAccountSuggestionService`, and generally should not be used by dialer apps other than for testing purposes.

| Parameters ||
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `handle` | [PhoneAccountHandle](../android/telecom/PhoneAccountHandle.md):The [PhoneAccountHandle](../android/telecom/PhoneAccountHandle.md) for this suggestion. This value cannot be`null`. |
| `reason` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The reason for this suggestion Value is [android.telecom.PhoneAccountSuggestion#REASON_NONE](../android/telecom/PhoneAccountSuggestion.md), [android.telecom.PhoneAccountSuggestion#REASON_INTRA_CARRIER](../android/telecom/PhoneAccountSuggestion.md), [android.telecom.PhoneAccountSuggestion#REASON_FREQUENT](../android/telecom/PhoneAccountSuggestion.md), [android.telecom.PhoneAccountSuggestion#REASON_USER_SET](../android/telecom/PhoneAccountSuggestion.md), or [android.telecom.PhoneAccountSuggestion#REASON_OTHER](../android/telecom/PhoneAccountSuggestion.md) |
| `shouldAutoSelect` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether the dialer should automatically place the call using this account. See [shouldAutoSelect()](../android/telecom/PhoneAccountSuggestion.md)). |
| --- | --- |

## Public methods

### describeContents

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### equals

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getPhoneAccountHandle

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPhoneAccountHandle(): PhoneAccountHandle
```

| Return ||
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PhoneAccountHandle](../android/telecom/PhoneAccountHandle.md) | The [PhoneAccountHandle](../android/telecom/PhoneAccountHandle.md) for this suggestion. This value cannot be`null`. |

### getReason

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getReason(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The reason for this suggestion Value is [android.telecom.PhoneAccountSuggestion#REASON_NONE](../android/telecom/PhoneAccountSuggestion.md), [android.telecom.PhoneAccountSuggestion#REASON_INTRA_CARRIER](../android/telecom/PhoneAccountSuggestion.md), [android.telecom.PhoneAccountSuggestion#REASON_FREQUENT](../android/telecom/PhoneAccountSuggestion.md), [android.telecom.PhoneAccountSuggestion#REASON_USER_SET](../android/telecom/PhoneAccountSuggestion.md), or [android.telecom.PhoneAccountSuggestion#REASON_OTHER](../android/telecom/PhoneAccountSuggestion.md) |

### hashCode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### shouldAutoSelect

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun shouldAutoSelect(): Boolean
```

Suggests whether the dialer should automatically place the call using this account without user interaction. This may be set on multiple [PhoneAccountSuggestion](../android/telecom/PhoneAccountSuggestion.md) s, and the dialer is free to choose which one to use.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the hint is to auto-select,`false`otherwise. |

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
| `dest` | [Parcel](../android/os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<PhoneAccountSuggestion!>
```
