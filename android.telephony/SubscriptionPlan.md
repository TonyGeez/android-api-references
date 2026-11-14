# SubscriptionPlan

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SubscriptionPlan

Kotlin| [Java](../android/telephony/SubscriptionPlan.md) 
| --- | --- |

```
class SubscriptionPlan : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.SubscriptionPlan](../android/telephony/SubscriptionPlan.md) |

Description of a billing relationship plan between a carrier and a specific subscriber. This information is used to present more useful UI to users, such as explaining how much mobile data they have remaining, and what will happen when they run out. If specifying network types, the developer must supply at least one plan that applies to all network types (default), and all additional plans may not include a particular network type more than once. This is enforced by [SubscriptionManager](../android/telephony/SubscriptionManager.md) when setting the plans. Plan selection will prefer plans that have specific network types defined over plans that apply to all network types.

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/telephony/SubscriptionPlan.Builder.md) Builder for a [SubscriptionPlan](../android/telephony/SubscriptionPlan.md). |

| Constants ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [BYTES_UNKNOWN](../android/telephony/SubscriptionPlan.md) Value indicating a number of bytes is unknown. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [BYTES_UNLIMITED](../android/telephony/SubscriptionPlan.md) Value indicating a number of bytes is unlimited. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LIMIT_BEHAVIOR_BILLED](../android/telephony/SubscriptionPlan.md) When a resource limit is hit, the user is billed automatically. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LIMIT_BEHAVIOR_DISABLED](../android/telephony/SubscriptionPlan.md) When a resource limit is hit, access is disabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LIMIT_BEHAVIOR_THROTTLED](../android/telephony/SubscriptionPlan.md) When a resource limit is hit, access is throttled to a slower rate. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LIMIT_BEHAVIOR_UNKNOWN](../android/telephony/SubscriptionPlan.md) When a resource limit is hit, the behavior is unknown. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUBSCRIPTION_STATUS_ACTIVE](../android/telephony/SubscriptionPlan.md) Subscription is active. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUBSCRIPTION_STATUS_INACTIVE](../android/telephony/SubscriptionPlan.md) Subscription is inactive. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUBSCRIPTION_STATUS_SUSPENDED](../android/telephony/SubscriptionPlan.md) Subscription is suspended. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUBSCRIPTION_STATUS_TRIAL](../android/telephony/SubscriptionPlan.md) Subscription is in a trial period. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUBSCRIPTION_STATUS_UNKNOWN](../android/telephony/SubscriptionPlan.md) Subscription status is unknown. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [TIME_UNKNOWN](../android/telephony/SubscriptionPlan.md) Value indicating a timestamp is unknown. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\< [Range](../android/util/Range.md)\< [ZonedDateTime](../java/time/ZonedDateTime.md)!\>!\>! | [cycleIterator](../android/telephony/SubscriptionPlan.md))`()` Return an iterator that will return all valid data usage cycles based on any recurrence rules. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/telephony/SubscriptionPlan.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/telephony/SubscriptionPlan.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDataLimitBehavior](../android/telephony/SubscriptionPlan.md))`()` Return the behavior of data access when usage reaches [getDataLimitBytes()](../android/telephony/SubscriptionPlan.md)). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getDataLimitBytes](../android/telephony/SubscriptionPlan.md))`()` Return the usage threshold at which data access changes according to [getDataLimitBehavior()](../android/telephony/SubscriptionPlan.md)). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getDataUsageBytes](../android/telephony/SubscriptionPlan.md))`()` Return a snapshot of currently known mobile data usage at [getDataUsageTime()](../android/telephony/SubscriptionPlan.md)). |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getDataUsageTime](../android/telephony/SubscriptionPlan.md))`()` Return the time at which [getDataUsageBytes()](../android/telephony/SubscriptionPlan.md))was valid. |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getNetworkTypes](../android/telephony/SubscriptionPlan.md))`()` Return an array containing all network types this SubscriptionPlan applies to. |
| [ZonedDateTime](../java/time/ZonedDateTime.md)? | [getPlanEndDate](../android/telephony/SubscriptionPlan.md))`()` Return the end date of this plan, or null if no end date exists. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSubscriptionStatus](../android/telephony/SubscriptionPlan.md))`()` Returns the status of the subscription plan. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getSummary](../android/telephony/SubscriptionPlan.md))`()` Return the short summary of this plan. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getTitle](../android/telephony/SubscriptionPlan.md))`()` Return the short title of this plan. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/telephony/SubscriptionPlan.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/telephony/SubscriptionPlan.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/telephony/SubscriptionPlan.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [SubscriptionPlan](../android/telephony/SubscriptionPlan.md)!\> | [CREATOR](../android/telephony/SubscriptionPlan.md) <br /> |

## Constants

### BYTES_UNKNOWN

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BYTES_UNKNOWN: Long
```

Value indicating a number of bytes is unknown. 

 Value: -1L

### BYTES_UNLIMITED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BYTES_UNLIMITED: Long
```

Value indicating a number of bytes is unlimited. 

 Value: 9223372036854775807L

### LIMIT_BEHAVIOR_BILLED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LIMIT_BEHAVIOR_BILLED: Int
```

When a resource limit is hit, the user is billed automatically. 

 Value: 1

### LIMIT_BEHAVIOR_DISABLED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LIMIT_BEHAVIOR_DISABLED: Int
```

When a resource limit is hit, access is disabled. 

 Value: 0

### LIMIT_BEHAVIOR_THROTTLED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LIMIT_BEHAVIOR_THROTTLED: Int
```

When a resource limit is hit, access is throttled to a slower rate. 

 Value: 2

### LIMIT_BEHAVIOR_UNKNOWN

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LIMIT_BEHAVIOR_UNKNOWN: Int
```

When a resource limit is hit, the behavior is unknown. 

 Value: -1

### SUBSCRIPTION_STATUS_ACTIVE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUBSCRIPTION_STATUS_ACTIVE: Int
```

Subscription is active. 

 Value: 1

### SUBSCRIPTION_STATUS_INACTIVE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUBSCRIPTION_STATUS_INACTIVE: Int
```

Subscription is inactive. 

 Value: 2

### SUBSCRIPTION_STATUS_SUSPENDED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUBSCRIPTION_STATUS_SUSPENDED: Int
```

Subscription is suspended. 

 Value: 4

### SUBSCRIPTION_STATUS_TRIAL

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUBSCRIPTION_STATUS_TRIAL: Int
```

Subscription is in a trial period. 

 Value: 3

### SUBSCRIPTION_STATUS_UNKNOWN

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUBSCRIPTION_STATUS_UNKNOWN: Int
```

Subscription status is unknown. 

 Value: 0

### TIME_UNKNOWN

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIME_UNKNOWN: Long
```

Value indicating a timestamp is unknown. 

 Value: -1L

## Public methods

### cycleIterator

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun cycleIterator(): MutableIterator<Range<ZonedDateTime!>!>!
```

Return an iterator that will return all valid data usage cycles based on any recurrence rules. The iterator starts from the currently active cycle and walks backwards through time. 

### describeContents

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### equals

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|--------------------------|
| `obj` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getDataLimitBehavior

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDataLimitBehavior(): Int
```

Return the behavior of data access when usage reaches [getDataLimitBytes()](../android/telephony/SubscriptionPlan.md)).

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.telephony.SubscriptionPlan#LIMIT_BEHAVIOR_UNKNOWN](../android/telephony/SubscriptionPlan.md), [android.telephony.SubscriptionPlan#LIMIT_BEHAVIOR_DISABLED](../android/telephony/SubscriptionPlan.md), [android.telephony.SubscriptionPlan#LIMIT_BEHAVIOR_BILLED](../android/telephony/SubscriptionPlan.md), or [android.telephony.SubscriptionPlan#LIMIT_BEHAVIOR_THROTTLED](../android/telephony/SubscriptionPlan.md) |

### getDataLimitBytes

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDataLimitBytes(): Long
```

Return the usage threshold at which data access changes according to [getDataLimitBehavior()](../android/telephony/SubscriptionPlan.md)). 
Value is a non-negative number of bytes.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Value is a non-negative number of bytes. |

### getDataUsageBytes

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDataUsageBytes(): Long
```

Return a snapshot of currently known mobile data usage at [getDataUsageTime()](../android/telephony/SubscriptionPlan.md)). 
Value is a non-negative number of bytes.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Value is a non-negative number of bytes. |

### getDataUsageTime

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDataUsageTime(): Long
```

Return the time at which [getDataUsageBytes()](../android/telephony/SubscriptionPlan.md))was valid. 
Value is a non-negative timestamp measured as the number of milliseconds since 1970-01-01T00:00:00Z.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Value is a non-negative timestamp measured as the number of milliseconds since 1970-01-01T00:00:00Z. |

### getNetworkTypes

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNetworkTypes(): IntArray
```

Return an array containing all network types this SubscriptionPlan applies to.

| Return ||
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | This value cannot be`null`. Value is [android.telephony.TelephonyManager#NETWORK_TYPE_UNKNOWN](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_GPRS](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_EDGE](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_UMTS](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_CDMA](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_EVDO_0](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_EVDO_A](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_1xRTT](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_HSDPA](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_HSUPA](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_HSPA](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_IDEN](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_EVDO_B](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_LTE](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_EHRPD](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_HSPAP](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_GSM](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_TD_SCDMA](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_IWLAN](../android/telephony/TelephonyManager.md), or [android.telephony.TelephonyManager#NETWORK_TYPE_NR](../android/telephony/TelephonyManager.md) |

**See Also**

- [android.telephony.TelephonyManager](../android/telephony/TelephonyManager.md) 

### getPlanEndDate

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPlanEndDate(): ZonedDateTime?
```

Return the end date of this plan, or null if no end date exists. 

### getSubscriptionStatus

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSubscriptionStatus(): Int
```

Returns the status of the subscription plan.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The subscription status, or [SUBSCRIPTION_STATUS_UNKNOWN](../android/telephony/SubscriptionPlan.md) if not available. Value is [android.telephony.SubscriptionPlan#SUBSCRIPTION_STATUS_UNKNOWN](../android/telephony/SubscriptionPlan.md), [android.telephony.SubscriptionPlan#SUBSCRIPTION_STATUS_ACTIVE](../android/telephony/SubscriptionPlan.md), [android.telephony.SubscriptionPlan#SUBSCRIPTION_STATUS_INACTIVE](../android/telephony/SubscriptionPlan.md), [android.telephony.SubscriptionPlan#SUBSCRIPTION_STATUS_TRIAL](../android/telephony/SubscriptionPlan.md), or [android.telephony.SubscriptionPlan#SUBSCRIPTION_STATUS_SUSPENDED](../android/telephony/SubscriptionPlan.md) |

### getSummary

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSummary(): CharSequence?
```

Return the short summary of this plan.

| Return ||
|------------------------------------------------------------------------------------------------|--------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | This value may be`null`. |

### getTitle

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTitle(): CharSequence?
```

Return the short title of this plan.

| Return ||
|------------------------------------------------------------------------------------------------|--------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | This value may be`null`. |

### hashCode

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<SubscriptionPlan!>
```
